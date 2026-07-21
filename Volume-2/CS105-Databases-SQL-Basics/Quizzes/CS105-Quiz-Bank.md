# CS105 — Self-Check Quiz Bank

Informal, ungraded. Use these to spot-check yourself at the end of each week — if you can answer confidently without looking anything up, you're on track.

## Week 1 — Relational Model & Basic SQL

1. What's the difference between a table's row and its column, in relational terms?
2. Why doesn't `WHERE column = NULL` work the way you'd expect? What should you use instead?
3. What does a primary key guarantee about a table?
4. Write (in words) what `SELECT name FROM users WHERE age > 30 ORDER BY name LIMIT 5` would return.

## Week 2 — Joins & Aggregations

5. What's the actual difference between `INNER JOIN` and `LEFT JOIN`, in terms of unmatched rows?
6. Why can't you use an aggregate function like `COUNT(*)` in a `WHERE` clause, but you can in `HAVING`?
7. If you accidentally use `INNER JOIN` where you needed `LEFT JOIN`, what's the likely symptom?
8. What does a foreign key actually enforce?

## Week 3 — Schema Design & Normalization

9. What specific problem does normalization prevent — name one concrete anomaly.
10. How do you represent a many-to-many relationship between two tables?
11. What's a sign in a schema (e.g. column naming) that suggests repeating groups exist?
12. When might deliberately denormalizing be a reasonable choice?

## Week 4 — Indexes, Query Performance & Transactions

13. What does an index actually do, structurally?
14. Why isn't "add an index to every column" a good default strategy?
15. What does the "A" in ACID (atomicity) guarantee about a transaction?
16. What real problem would you run into without transactions, in a multi-step write operation?

## Week 5 — Connecting Python to Databases

17. What's wrong with building a SQL query using an f-string with user input directly inside it?
18. What does a parameterized query actually do differently?
19. What is an ORM doing, conceptually, when you query through it instead of writing raw SQL?
20. Name one situation where raw SQL would be preferable to using an ORM.

## Week 6 — NoSQL & Vector Database Concepts

21. What's a concrete problem NoSQL databases solve that relational databases handle less naturally?
22. Why can't a SQL `WHERE` clause find "semantically similar" documents the way a vector database can?
23. What does a vector database actually store, and what operation does it optimize for?
24. Why would a real RAG system typically use both a vector store and a relational/document store, rather than just one?

## Full-Course Gut Check

25. Given a plain-language description of a new application's data needs (e.g. "track authors, books, and which readers have read which books, with ratings"), design a normalized schema from scratch, write a query that would answer a realistic question about it (like "average rating per author"), and identify whether any column deserves an index. If you can do this comfortably, CS105 is done.
