# Use Cases


## Classic "internal tooling" use cases
- Dashboards
- Forms
- Approval flows
- Runbooks
- Report running
- Scheduled jobs
- CRUD apps
- Business intelligence (BI)

## Specific engineering use cases

Flank is abstractly a really simple tool that can be used in a lot of ways. These are just some ideas...

### SQL Writers
- **Reusable library of ad hoc queries.** If you get into the practice of wrapping every ad-hoc query in a stored procedure, you'll get an app for free every time you write SQL!
- **Quick data exports.** When you put a stored proc in Flank, the user can download the result of any run in a CSV.

### Backend Engineering
- **Offload API endpoint testing.** Flank has guardrails that make it less scary / safer than Postman / Swagger, so you could have, e.g., Support Engineers test endpoints themselves.
- **Tool for configuration management.** If your app has a lot of "switches" that need to be controlled by the CX team, it's easy to create lots of apps very quickly in Flank for basic CRUD.

### Frontend Engineering
- **Schedule jobs.** Set up scheduled jobs without going through backend engineers
- **Deprecate the long-tail.** Most admin panels have a long tail of random pages that aren't tracked. You can throw all that into Flank and focus time on the imporant parts of the site.
- **Prototype features.** Instead of building UI to discover whether a tool is actually to the Ops team, just put a query in Flank and wait and see.

### Data Engineering
- **Democratize re-running.** Create quick apps for teammates to re-run failed jobs, without giving them full access to Airflow
- **Offload one-off data correction.** Create lots of little apps for one-off data corrections to single rows
- **Review dead letter queues.** Create a quick app for QA on data that is put into a dead letter queue

### Engineering Management
- **Deprecate unused code.** If you run your internal tooling through Flank, you can get metrics on which procedures/endpoints are not being used.
- **Prototype feature upstream of design/frontend.** Typically you have to build a UI for a feature to discover whether it's valuable. With Flank, you can just have the backend engineer write the business logic and immediately create an app. Then track it's usage.