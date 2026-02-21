# SQL Query Engine

## What do you want to build?

Build a SQL database engine in Rust that can parse SQL queries, optimize query plans, and execute them against an on-disk storage engine. The engine should support a useful subset of SQL and handle tables with millions of rows efficiently.

The implementation must include:
- SQL parser supporting: SELECT (with WHERE, ORDER BY, GROUP BY, HAVING, LIMIT), INSERT, UPDATE, DELETE, CREATE TABLE, DROP TABLE, JOIN (INNER, LEFT)
- Query planner with cost-based optimization (join reordering, predicate pushdown, index selection)
- B-tree indexes for primary keys and secondary indexes
- Page-based storage engine with buffer pool management
- Aggregate functions: COUNT, SUM, AVG, MIN, MAX
- Data types: INTEGER, FLOAT, TEXT, BOOLEAN
- Transaction support with basic ACID properties (single-node)
- REPL interface for interactive queries

## How do you consider the project is success?

1. All supported SQL statements parse and execute correctly — validated with a test suite of at least 50 SQL queries
2. JOIN queries produce correct results matching SQLite output on the same data
3. B-tree indexes provide measurable speedup (>10x) on point queries against tables with 100K+ rows
4. Buffer pool limits memory usage — handles tables larger than available buffer pool
5. TPC-H queries Q1, Q3, Q6 execute correctly (correctness, not performance)
6. Predicate pushdown is applied automatically (verified via EXPLAIN output)
7. Transactions are atomic — incomplete transactions don't corrupt data after simulated crashes
8. Test suite passes with at least 50 test cases
