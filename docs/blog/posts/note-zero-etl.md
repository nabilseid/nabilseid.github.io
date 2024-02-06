---
date: 2024-02-06
authors:
  - almightyPush
categories:
  - Note
  - ETL
---

# Notes: Zero-ETL

At the time of writing Zero ETL is an integration tool that makes transactional data available in Redshift in near real time. This is useful if real time analytical data in Redshift is necessary. It support Aurora and RDS MySQL as data source.

### What problem zero ETL solve?

- Remove the complexity of ETL management, monitoring and maintenance
- Low latency data integration. Data is updated imidiately when the source is updated. E.g when RDBMS updated, Redshift will get updated updated right after.
- It is particularly useful if real time data is necessary

### Disadvantage of zero ETL

- There is no stagings, which means data is highly transformed. Which means you will most likely will end up creating a new zero ETL for new scenarios.
- For none real time data, I don’t see the advantage
