# dbt

dbt and Flank are both tools that sit on top of SQL queries.

dbt is a tool for data analysts to build production **data pipelines** using nothing more than SQL (well, not really the whole pipeline, just the "T" in ETL/ELT)

Flank is a tool for building quick-and-dirty **business applications**.

|                      | Flank                                                                                                                                | dbt                                                                                                                      |
| -------------------- | ------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------ |
| Used by              | Engineers, to expose SQL (among other things), and business people, to run it                                                        | SQL writers, to build data pipelines with just SQL (well, really the T in ETL/ELT)                                       |
| Problem it solves    | Hard to safely expose SQL queries to business people                                                                                 | Data engineers become bottlenecks for transformation tasks that are conceptually simple enough for any SQL writer to do  |
| Best for             | Exposing a stored procedure to a business person                                                                                     | Writing data pipelines in SQL                                                                                            |
| Typical workflow     | Write SQL in your IDE, point Flank at it, share with a business person                                                               | Write SQL query in dbt, set up a pipeline task that runs automatically                                                   |
| Technically speaking | API that wraps stored procs, with a UI layer on top, which provides guardrails for business people to interact with the stored procs | Web-based GUI for writing SQL and setting up data pipelines                                                              |
| Key simplification   | Making a GUI for every stored proc fosters better collaboration between engineers and business people                                | Making a GUI for pipelining / deployment allows a new class of engineers (SQL writers) to contribute to data engineering |
| Key difference       | Business application builder                                                                                                         | Data pipeline builder                                                                                                    |
| Throwback analogy    | A web app that sits on top of a folder in git with a bunch of "team" queries                                                         | An orchestration tool that points at a folder in git with a bunch of "team" queries                                      |