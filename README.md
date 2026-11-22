### What is Relational Database ?
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
