# Results so far

Flank is running in 4 companies: 

- 1-person data science operation
- 10-person SaaS company
- 60-person SaaS company
- 350-person marketplace with warehouse

We've been pleasantly surprised with the results so far. 

## Vision for a different way of working

### 1-person data science operation

- **Before:** When an R script needs to be run in parallel, or on a schedule, or on a machine with more memory, the Data Scientist has to dive into AWS
- **Vision:** Data Scientist just writes R scripts. No AWS.
- **Onboarding:** Data Scientist created a Personal Access Token in GitHub and gave that to Flank. Then Flank discovered his R script.
- **Elimination of...:**
    - **Tools:** Docker, AWS Batch, EC2, Linux, SSH, Airflow
    - **Meetings:** N/A
    - **Urgent messages:** N/A

### 10-person SaaS company

- **Before:** For the Data Engineer to build a reusable tool for the Sales team, he needs the frontend consultants to build it into their app
- **Vision:** Data Engineer ships features by himself. Not reliant on consultants.
- **Onboarding:** Backend Engineer created an AWS role that could read and execute Lambdas. He gave that to Flank, which then discovered the Lambda he wanted to share.
- **Elimination of tools:** React, AWS EventBridge, JSON to CSV converter
- **Elimination of meetings:** Backend Engineer + frontend consultants + Sales team
- **Elimination of urgent Slacks:** Sales team needs the data run it now!

### 60-person SaaS company

- **Before:** The Customer Service team can't wait for apps to get built, so they resolve problems by manually triggering API calls in Postman. This is error-prone and difficult to scale.
- **Vision:** New Customer Service hires can quickly be onboarded to a safe, intuitive platform
- **Onboarding:** Product Manager exported a Postman collection to a JSON file. She uploaded that file to Flank, which created a web page with user guardrails for each endpoint.
- **Elimination of tools:** Postman (for non-engineers), React, JSON to CSV converter, API keys, passing secrets over Slack
- **Elimination of meetings:** Backend Engineers + Frontend Engineers + Product Manager + Customer Service Lead

### 350-person

- **Before:** Every little feature now requires a meeting between a PM, a designer, a React dev, a database engineer, and an API engineer.
- **Vision:** Ship like it's a tiny startup again.
- **Onboarding:** Database Engineer created a user for Flank, and then gave Flank the credentials. Flank scanned the database and discovered hundreds of stored procedures, which he imported.

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
| Code               | Discovered Through... | Executed on...  |
| ------------------ | --------------------- | --------------- |
| R scripts          | GitHub                | AWS Batch       |
| Python functions   | AWS Lambda            | AWS Lambda      |
| API (internal)     | Postman export        | Customer infra  |
| API (3rd-party)    | Postman export        | 3rd-party infra |
| MSSQL SPROCs       | MSSQL system table    | MSSQL           |
| Postgres Functions | Postgres system table | Postgres        |

## Self-hosting
|Company                        |Flank site/API|Job execution|
|-------------------------------|--------------|-------------|
|1-person data science operation|              |             |
|10-person SaaS company         |              |Self-hosted  |
|60-person SaaS company         |              |Self-hosted  |
|300-person marketplace         |Self-hosted   |Self-hosted  |


## Stories

- An engineer was on his way to dinner when a teammate asked him to re-run a SQL query. Instead of going back to his desk, he logged into Flank and shared the query like you'd share a Google Doc.