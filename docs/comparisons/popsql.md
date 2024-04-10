# PopSQL

PopSQL and Flank both allow teams to "share queries", but they're actually attacking different problems at different levels of abstraction.

PopSQL allows engineers to share **SQL code** with **other engineers**.

Flank allows engineers to share the **ability to execute SQL** with **business people**.

|                      | Flank                                                                                                                                | PopSQL                                                                                                                          |
| -------------------- | ------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------- |
| Used by              | Engineers, to expose SQL (among other things), and business people, to run it                                                        | Engineers, to write and reuse SQL                                                                                               |
| Problem it solves    | Hard to safely expose SQL queries to business people                                                                                 | Sharing SQL queries is clunky                                                                                                   |
| Best for             | Exposing a stored procedure to a business person                                                                                     | Writing a SQL query that your teammate could reuse later                                                                        |
| Typical workflow     | Write SQL in your IDE, point Flank at it, share with a business person                                                               | Write SQL query in PopSQL, another teammate grabs it and runs it                                                                |
| Technically speaking | API that wraps stored procs, with a UI layer on top, which provides guardrails for business people to interact with the stored procs | Cloud-based SQL IDE that enables collaboration                                                                                  |
| Key simplification   | The UI to interact with stored procs can be derived from the procedure's parameters                                                  | Moving the "reusability" layer from stored procs to the cloud allows for some nice features (e.g. pretty names, usage tracking) |
| Key difference       | Collaborative SQL runner                                                                                                             | Collaborative SQL IDE                                                                                                           |
| Throwback analogy    | A web app that sits on top of a folder in git with a bunch of "team" queries                                                         | A folder in git with a bunch of "team" queries                                                                                  |
