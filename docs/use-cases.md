# Use Cases


## Classic "internal tooling" use cases
- Dashboards
- Forms
- Approval flows
- Runbooks
- Report running
- Scheduled jobs
- CRUD apps

## Specific engineering use cases

Flank can be used in a lot of different ways. These are just some ideas...

### SQL Writers
- **Reuse ad hoc queries.** If you get into the practice of wrapping every ad-hoc query in a stored procedure, you'll get an app for free every time you write SQL!

### Backend Engineering

### Frontend Engineering
- **Self-serve cron.** Set up scheduled jobs without going through backend engineers

### Data Engineering
- **Democratize re-running.** Create quick apps for teammates to re-run failed jobs, without giving them full access to Airflow
- **Offload one-off data correction.** Create lots of little apps for one-off data corrections to single rows
- **Review dead letter queues.** Create a quick app for QA on data that is put into a dead letter queue

### Engineering Management
- **Deprecate unused code.** If you run your internal tooling through Flank, you can get metrics on which procedures/endpoints are not being used.