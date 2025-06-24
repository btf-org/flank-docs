# Results so far

Flank is running in 4 companies. We've been pleasantly surprised with the results so far.

## How they see Flank
- **1-person data science operation** - _Just write code_. In other words, don't spend time on things that aren't core data science tasks: ~~configuring AWS Batch jobs, containerizing R scripts, setting up Airflow pipelines, searching through Cloudwatch logs, constantly checking job statuses, memory profiling, breaking down the costs of big runs.~~
- **10-person SaaS company** - _Stop using expensive consultants_. Before, the backend engineer had to wait on their frontend consultants. Now, he can single-handedly ship features to the sales and executive team.
- **60-person SaaS company** - _Build apps without engineers_. They have a ton of customer service workflows that are just connections between 3rd-party API calls (e.g. Stripe) and production API calls. These endpoints have already been written. Their team just needs to wire them together.
- **300-person marketplace with warehouse** - _Ship like they're a tiny startup again_. In other words, allow engineers to single-handedly ship features without prior approval. This requires an approach to building software where everything is tracked and mistakes can easily be reversed.

## What was it like to onboard?
- **1-person data science operation** - Data Scientist 1) pushed an R script to GitHub and 2) created a Personal Accesss Token for Flank to discover the script
- **10-person SaaS company** - Backend Engineer created an AWS role that allowed Flank to discover/execute Lambdas
- **60-person SaaS company** - Product Manager exported a Postman collection to JSON, then imported that file into Flank
- **300-person marketplace with warehouse** - Database Engineer punched in the DB creds and Flank discovered hundreds of existing SPROCs

## Integrations
- **1-person data science operation** - R scripts on GitHub
- **10-person SaaS company** - AWS Lambdas (Python)
- **60-person SaaS company** - REST APIs (internal and external)
- **300-person marketplace with warehouse** - MSSQL SPROCs, Postgres Functions, REST APIs (external)

## Self-hosting
|Company                        |Flank site/API|Job execution|
|-------------------------------|--------------|-------------|
|1-person data science operation|              |             |
|10-person SaaS company         |              |Self-hosted  |
|60-person SaaS company         |              |Self-hosted  |
|300-person marketplace         |Self-hosted   |Self-hosted  |


## Stories

- An engineer was on his way to dinner when a teammate asked him to re-run a SQL query. Instead of going back to his desk, he logged into Flank and shared the query like you'd share a Google Doc.