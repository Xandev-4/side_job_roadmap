# 03. SQL and PostgreSQL

Priority: **Core** = learn first, **Next** = after Core / when a project needs it, **Later** = just know it exists.

## A. Database basics

| Done | Concept                                                 | Priority | What you should be able to do      |
| ---- | ------------------------------------------------------- | -------- | ---------------------------------- |
| ☐    | What a database is, relational model                    | Core     | Explain tables, rows, columns      |
| ☐    | Primary key, foreign key, unique, not null              | Core     | Choose keys for a table            |
| ☐    | Data types (int, text, varchar, boolean, date, numeric) | Core     | Pick the right type                |
| ☐    | Relationships: one-to-one, one-to-many, many-to-many    | Core     | Model a real app                   |
| ☐    | Junction (join) tables                                  | Core     | Build a many-to-many               |
| ☐    | Entity-relationship diagrams                            | Core     | Sketch a schema before writing SQL |

## B. SQL fundamentals

| Done | Concept                                                            | Priority | What you should be able to do            |
| ---- | ------------------------------------------------------------------ | -------- | ---------------------------------------- |
| ☐    | `SELECT`, `FROM`, `WHERE`                                          | Core     | Filter rows                              |
| ☐    | `AND`, `OR`, `NOT`, `IN`, `BETWEEN`, `LIKE`, `IS NULL`             | Core     | Combine conditions                       |
| ☐    | `ORDER BY`, `LIMIT`, `OFFSET`                                      | Core     | Sort and paginate                        |
| ☐    | `DISTINCT`                                                         | Core     | Remove duplicates                        |
| ☐    | `INSERT`, `UPDATE`, `DELETE`                                       | Core     | Change data safely (always with `WHERE`) |
| ☐    | `CREATE TABLE`, `ALTER TABLE`, `DROP TABLE`                        | Core     | Define and change schema                 |
| ☐    | Aggregates: `COUNT`, `SUM`, `AVG`, `MIN`, `MAX`                    | Core     | Summarise data                           |
| ☐    | `GROUP BY`, `HAVING`                                               | Core     | Group and filter groups                  |
| ☐    | Joins: `INNER`, `LEFT`, `RIGHT`, `FULL`                            | Core     | Combine tables; explain each             |
| ☐    | Self join, cross join                                              | Next     | Compare rows within a table              |
| ☐    | Subqueries (in `WHERE`, `FROM`, `SELECT`)                          | Next     | Nest queries                             |
| ☐    | `CASE WHEN`                                                        | Next     | Conditional logic in queries             |
| ☐    | `COALESCE`, `NULLIF`, handling NULLs                               | Next     | Avoid NULL surprises                     |
| ☐    | Set operations (`UNION`, `INTERSECT`, `EXCEPT`)                    | Next     | Combine query results                    |
| ☐    | CTEs (`WITH`)                                                      | Next     | Break a big query into steps             |
| ☐    | Window functions (`ROW_NUMBER`, `RANK`, `LAG`, `LEAD`, `SUM OVER`) | Next     | Rankings, running totals                 |
| ☐    | Recursive CTEs                                                     | Later    | Hierarchies, trees                       |
| ☐    | String, date and number functions                                  | Next     | Clean and format data                    |

## C. Schema design

| Done | Concept                                         | Priority | What you should be able to do |
| ---- | ----------------------------------------------- | -------- | ----------------------------- |
| ☐    | Normalization (1NF, 2NF, 3NF)                   | Core     | Fix a messy table             |
| ☐    | When to denormalise                             | Next     | Trade-offs for speed          |
| ☐    | Constraints (`CHECK`, `DEFAULT`, `UNIQUE`)      | Core     | Let the DB reject bad data    |
| ☐    | Foreign key actions (`ON DELETE CASCADE`, etc.) | Core     | Decide what happens on delete |
| ☐    | Naming conventions                              | Core     | Keep schemas readable         |
| ☐    | Soft delete vs hard delete                      | Next     | Pick one for a use case       |
| ☐    | Audit columns (`created_at`, `updated_at`)      | Core     | Add to every table            |
| ☐    | Many-to-many with extra attributes              | Next     | Order items with quantity     |

## D. PostgreSQL specifics

| Done | Concept                                                                 | Priority | What you should be able to do         |
| ---- | ----------------------------------------------------------------------- | -------- | ------------------------------------- |
| ☐    | Installing Postgres, `psql` basics (`\dt`, `\d`, `\l`, `\c`)            | Core     | Navigate a database from the terminal |
| ☐    | Users, roles, databases, schemas                                        | Core     | Create a DB and a user for an app     |
| ☐    | Postgres types: `SERIAL` / `IDENTITY`, `UUID`, `TIMESTAMPTZ`, `BOOLEAN` | Core     | Choose proper IDs and timestamps      |
| ☐    | `JSON` / `JSONB`                                                        | Next     | Store and query flexible data         |
| ☐    | Arrays, enums                                                           | Next     | Know when to use them                 |
| ☐    | `RETURNING` clause                                                      | Core     | Get inserted rows back                |
| ☐    | `ILIKE`, full-text search                                               | Next     | Simple search                         |
| ☐    | `UPSERT` (`ON CONFLICT`)                                                | Next     | Insert or update                      |
| ☐    | Views, materialized views                                               | Next     | Reuse queries                         |
| ☐    | Sequences                                                               | Next     | Understand how auto IDs work          |
| ☐    | Extensions (`pgcrypto`, `uuid-ossp`, `pg_trgm`)                         | Later    | Know they exist                       |
| ☐    | `pgvector` extension                                                    | Next     | Vector search for the AI stage        |
| ☐    | Triggers, stored procedures, functions (PL/pgSQL)                       | Later    | Know what they do                     |
| ☐    | Partitioning, foreign data wrappers                                     | Later    | Skip for now                          |

## E. Performance

| Done | Concept                                         | Priority | What you should be able to do            |
| ---- | ----------------------------------------------- | -------- | ---------------------------------------- |
| ☐    | What an index is and why it speeds up reads     | Core     | Explain it in simple words               |
| ☐    | Creating indexes (single, composite, unique)    | Next     | Index a slow column                      |
| ☐    | `EXPLAIN` / `EXPLAIN ANALYZE`                   | Next     | Read a basic query plan                  |
| ☐    | Index types (B-tree, hash, GIN, GiST)           | Later    | Know when GIN is used (JSONB, full text) |
| ☐    | N+1 query problem                               | Next     | Spot it in app code                      |
| ☐    | Pagination: offset vs keyset                    | Next     | Know why offset gets slow                |
| ☐    | Connection pooling (PgBouncer, app-level pools) | Next     | Explain why it's needed                  |
| ☐    | Vacuum, autovacuum, bloat                       | Later    | Know it exists                           |

## F. Transactions and safety

| Done | Concept                                              | Priority | What you should be able to do             |
| ---- | ---------------------------------------------------- | -------- | ----------------------------------------- |
| ☐    | Transactions (`BEGIN`, `COMMIT`, `ROLLBACK`)         | Next     | Make multi-step changes atomic            |
| ☐    | ACID                                                 | Next     | Explain each letter                       |
| ☐    | Isolation levels, dirty/non-repeatable/phantom reads | Later    | Know the names                            |
| ☐    | Locks, deadlocks                                     | Later    | Know the idea                             |
| ☐    | SQL injection and parameterised queries              | Core     | Never build SQL with string concatenation |
| ☐    | Backups (`pg_dump`, `pg_restore`)                    | Next     | Back up and restore a DB                  |
| ☐    | Migrations (Alembic)                                 | Next     | Change schema with version history        |

## G. Using a database from Python

| Done | Concept                                          | Priority | What you should be able to do |
| ---- | ------------------------------------------------ | -------- | ----------------------------- |
| ☐    | Connect with `psycopg` (raw SQL)                 | Next     | Run a query from Python       |
| ☐    | SQLAlchemy ORM (models, sessions, relationships) | Next     | Map tables to classes         |
| ☐    | SQLModel (optional, pairs with FastAPI)          | Later    | Know it exists                |
| ☐    | Async DB access (`asyncpg`, SQLAlchemy async)    | Later    | Know it exists                |

## H. NoSQL (awareness only)

| Done | Concept                               | Priority | What you should be able to do |
| ---- | ------------------------------------- | -------- | ----------------------------- |
| ☐    | SQL vs NoSQL tradeoffs                | Core     | Explain when each fits        |
| ☐    | Redis (key-value, caching)            | Next     | Cache something, set a TTL    |
| ☐    | MongoDB (documents)                   | Next     | Do basic CRUD                 |
| ☐    | Column stores, graph DBs, time-series | Later    | Know they exist               |

## Practice

- [ ] SQLBolt lessons
- [ ] pgexercises.com
- [ ] Design and query a schema for: users, posts, comments, likes
- [ ] 30+ queries including joins, group by, CTEs and window functions
