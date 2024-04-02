---
draft: true
date: 2024-02-29
authors:
  - almightyPush
categories:
  - Soln
  - SQL
---

# Soln: SQL Challenge Solutions

The SQL Challenges are compromised from LeetCode and Hackerrank. Each challenge title is a link.
<!-- more -->


## Leetcode - SQL 50

### SELECT 

#### [Recyclable and Low Fat Products](https://leetcode.com/problems/recyclable-and-low-fat-products/description/?envType=study-plan-v2&envId=top-sql-50)

Table: `Products`

| Column Name | Type    |
|-------------|---------|
| product_id  | int     |
| low_fats    | enum    |
| recyclable  | enum    |

- Product_id is the primary key (column with unique values) for this table.
- Low_fats is an ENUM (category) of type ('Y', 'N') where 'Y' means this product is low fat and 'N' means it is not.
- Recyclable is an ENUM (category) of types ('Y', 'N') where 'Y' means this product is recyclable and 'N' means it is not.
 

Write a solution to find the ids of products that are both low fat and recyclable.

Return the result table in any order.

The result format is in the following example.

??? note "Further Explanation"

    **Example 1:**

    **Input:**
    Products table:
    
    | product_id  | low_fats | recyclable |
    |-------------|----------|------------|
    | 0           | Y        | N          |
    | 1           | Y        | Y          |
    | 2           | N        | Y          |
    | 3           | Y        | Y          |
    | 4           | N        | N          |

    **Output:**
    
    | product_id  |
    |-------------|
    | 1           |
    | 3           |

    **Explanation:** Only products 1 and 3 are both low fat and recyclable.

**Solution**

```sql
SELECT product_id
FROM Products
WHERE low_fats = 'Y' AND recyclable = 'Y';
```
