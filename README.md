## What is Relational Database ?
A relational database is a type of database where data is organized into tables with rows and columns, and these tables are linked together using Primary Keys and Foreign Keys.Its called relation. Data validity is ensured through schemas and constraints (such as data types, NOT NULL, UNIQUE, FK, and CHECK). It keeps transactions safe by following ACID properties (Atomicity, Consistency, Isolation, Durability). Redundancy can be reduced through normalization, while SQL allows for powerful querying, including JOINs. Since core SQL is nearly the same across all relational databases, learning one makes it easy to master the others, even though each has its own specific dialect.


## SQL Data Types

A data type tells the database what kind of data a column can store. For example, a number, a text, a date, or true/false. It also protects the data, because the database will reject a value of the wrong type.

The 10 most common data types are:

| Type | Syntax | Example | Meaning |
|---|---|---|---|
| `INTEGER` | `age INTEGER` | `25` | Whole numbers (about -2.1 billion to 2.1 billion) |
| `BIGINT` | `views BIGINT` | `9000000000` | Very big whole numbers. Good for IDs in big tables |
| `NUMERIC(p,s)` | `price NUMERIC(12,2)` | `25999.50` | Exact decimal numbers. Use it for money. `p` = total digits, `s` = digits after the decimal point |
| `BOOLEAN` | `is_active BOOLEAN` | `TRUE` | Only true or false |
| `TEXT` | `bio TEXT` | `'I love SQL'` | Text with no length limit |
| `VARCHAR(n)` | `name VARCHAR(100)` | `'Rahim'` | Text with a maximum length of `n` characters |
| `DATE` | `birth_date DATE` | `'1998-05-14'` | Only the date, no time |
| `TIMESTAMPTZ` | `created_at TIMESTAMPTZ` | `'2026-11-22 10:30:00+06'` | Date and time with time zone. Stored in UTC, shown in your session time zone |
| `UUID` | `id UUID` | `'550e8400-e29b-41d4-a716-446655440000'` | A unique ID that can be created on any server without duplicates |
| `JSONB` | `attributes JSONB` | `'{"color": "black"}'` | JSON data stored in binary form. Fast to search and can be indexed |

## SQL Operators

An operator is a symbol or a word that we use to compare values, do calculations, or join conditions. Most of the time, operators are used in the `WHERE` clause to filter rows.

### 1. Comparison Operators

Used to compare two values.

| Operator | Syntax | Example | Meaning |
|---|---|---|---|
| `=` | `a = b` | `price = 750` | Equal to |
| `<>` or `!=` | `a <> b` | `stock_qty <> 0` | Not equal to |
| `>` | `a > b` | `price > 1000` | Greater than |
| `<` | `a < b` | `price < 1000` | Less than |
| `>=` | `a >= b` | `stock_qty >= 10` | Greater than or equal to |
| `<=` | `a <= b` | `price <= 1500` | Less than or equal to |


### 2. Logical Operators

Used to join more than one condition.

| Operator | Syntax | Example | Meaning |
|---|---|---|---|
| `AND` | `a AND b` | `price > 1000 AND stock_qty > 0` | Both conditions must be true |
| `OR` | `a OR b` | `price < 500 OR stock_qty = 0` | At least one condition must be true |
| `NOT` | `NOT a` | `NOT stock_qty = 0` | Reverses the condition |

### 3. Arithmetic Operators

Used to do calculations.

| Operator | Syntax | Example | Meaning |
|---|---|---|---|
| `+` | `a + b` | `price + 100` | Add |
| `-` | `a - b` | `price - 50` | Subtract |
| `*` | `a * b` | `price * stock_qty` | Multiply |
| `/` | `a / b` | `price / 2` | Divide |
| `%` | `a % b` | `stock_qty % 2` | Remainder after division |


### 4. Range, List and Pattern Operators

| Operator | Syntax | Example | Meaning |
|---|---|---|---|
| `BETWEEN` | `a BETWEEN x AND y` | `price BETWEEN 1000 AND 2000` | Value is inside a range. Both ends are included |
| `IN` | `a IN (x, y)` | `sku IN ('LPT00001', 'KBD00004')` | Value matches any item in the list |
| `NOT IN` | `a NOT IN (x, y)` | `stock_qty NOT IN (0, 5)` | Value matches none of the items |
| `LIKE` | `a LIKE pattern` | `name LIKE 'Wire%'` | Matches a text pattern. Case sensitive |
| `ILIKE` | `a ILIKE pattern` | `name ILIKE 'laptop%'` | Same as `LIKE`, but ignores upper and lower case. Only in PostgreSQL |

### 5. NULL Operators

| Operator | Syntax | Example | Meaning |
|---|---|---|---|
| `IS NULL` | `a IS NULL` | `attributes IS NULL` | Value is missing |
| `IS NOT NULL` | `a IS NOT NULL` | `attributes IS NOT NULL` | Value exists |
