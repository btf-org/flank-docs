# Use Cases


With Flank, engineers can (safely) give non-engineers access to 1) frequently-run queries, 2) re-running failed jobs, and 3) urgent CRUD operations.

### SQL Writers
- **Get re-use out of every ad-hoc query.** If you get into the practice of wrapping every ad-hoc query in a stored procedure, you'll get an app for free every time you write SQL.
- **Downloadable history of query results.** When you put a stored proc in Flank, the user can download the result of any run in a CSV.
- **Offload one-off data correction.** All you need to do is write a parameterized stored procedure. Then Flank handles the guardrails, auditing, RBAC, etc.

### Backend/Data Engineers
- **Allow support techs to investigate API issues.** Flank has guardrails that make it safer than Postman / Swagger, so Support Engineers can test endpoints themselves.
- **Allow business stakeholders to re-run failed jobs.** Create quick apps for teammates to re-run failed jobs, without giving them full access to Airflow, Azure Data Factory, etc.
- **Review dead letter queues.** With Flank you can pipe the output of one SPROC into the input of another. In other words, you can create tables with buttons really quickly.

### Frontend Engineers
- **Schedule jobs.** Set up scheduled jobs without going through backend engineers
- **Deprecate the long-tail of random admin pages.** Flank is like a file system of SPROCs/API calls. You can have 5000 of them. Put them in folders. Share them with specific people.
- **Prototype features before writing a line of code.** Instead of building UI to discover whether a tool is actually useful to the Ops team, just put the SQL in Flank and wait and see.

### Engineering Managers
- **Deprecate unused SPROCs/API endpoints.** If you run your internal tooling through Flank, you can get metrics on which procedures/endpoints are not being used.
- **Prototype feature upstream of design/frontend.** Typically you have to build a UI for a feature to discover whether it's valuable. With Flank, you can just have the backend engineer write the business logic and immediately create an app. Then track it's usage.