# Results so far

Flank is running in 4 companies:

- 1-person data science operation
- 10-person SaaS company
- 60-person SaaS company
- 300-person marketplace

We've been pleasantly surprised with the results so far. Flank was originally conceived as a prototyping tool, but, as it has become more stable, it has replaced internal tools, BI dashboards, cron jobs, and (in some cases) deployment systems.

Also, people seem to enjoy ~~using the product~~ not futzing around with the cloud. Some experiences that we've heard about:

- Customer (engineer) was on his way to dinner and a teammate (non-engineer) asked him to re-run a SQL query. Instead of going back to his desk, he logged into Flank and shared the query like he’d share a Google Doc.
- Customer had written an R script locally, but then he needed to run it on a schedule with 64 GB of memory. He simply pushed the latest changes to GitHub, went into Flank and set it to run on a schedule. It just worked.
- Customer wrote a series of Lambdas to be consumed by other Lambdas. Then the sales team needed the same functionality. But the Lambdas returned JSON lists. He connected the Lambdas to Flank and Flank automatically converted the JSON lists to tables. No frontend work needed.