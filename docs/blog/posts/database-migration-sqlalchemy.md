---
date: 2024-05-30
authors:
  - almightyPush
categories:
  - Database
---

# Database Migration in SQLAlchemy

Database migration is basically keeping any changes you want to make to your database into code and the code that undo the changes you made. This will help you to revert changes you made to the database anytime you want and more over if you have testing and production environment deploying database changes into production is done by just running a script.

<!-- more -->

!!! note "Note"

    This is a short explanation of how to setup database migration in SQLAlchemy, if you don't know the basics of database migration, there are plenty of resources online. Checkout your chosing and get back.

We are goint to use [alembic](https://alembic.sqlalchemy.org/en/latest/) to manage our database migration.

## Project setup

In SQLAlchemy we have 3 components we should care about when structuring our project, `engine`, `declarative_base`, and `models`. For modularity I like to separate `engine` into a module but I usually merge `declarative_base` and `models` into a subpackage.

There are two way to setup your SQLAlchemy project. 
- Define `declarative_base` inside model module.
- Have a separate module to store `declarative_base`

If you go with the first one, all models and the `declarative_base` are define in a separe module and alembic imports `declarative_base` from this module. 

<--folder structure-->

On the second one `declarative_base` is defined in its own module and for alembic to trace the models they have to be imported with the `declarative_base`, instead of doing that in alembic I prefer doing it in the database module and from alembic import `declarative_base` from the database module.

<--folder structure-->

## Alembic setup

Now we have the SQLAlchemy project setup, let's add database migration. After [installing](https://alembic.sqlalchemy.org/en/latest/front.html#project-homepage) alembic use `init` command to create the migration at the application level (along side the source code). 

```bash
# alembic init <directory>
alembic init migrations
```

env.py the file alembic run. This file is used to link declarive base and the engine with alembic. 
alembic.ini contains configuration alembic use when it run. This contains values like database url,  location where migration scripts are stored.
versions/ directory where migration scripts are stored. This can be manually changed to different name.

## Let's do some migration

Let's create a new model hero and generate a migration script for it. 

```python
# models/hero.py
from sqlalchemy import Column, Integer, String
from src.models.base import Base

class Hero(Base):
    __tablename__ = 'heros'

    id = Column(Integer, primary_key=True)
    name = Column(String)
    power = Column(String,)
```


having multiple database
