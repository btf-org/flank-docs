# Retool

You should use Retool if

- you need to build an internal-facing website (think: admin panel)

You should use Flank if

- you only need to expose a single query / script to a non-engineer (think: run a query)

You should both if

- you have a lot of internal tooling, most of which (say, 80%) can be prototyped as a single query / endpoint / script (Flank) before being moved into a more sophisticated application (Retool)

You should something else entirely if:

- you need to build a customer facing website (custom build or Squarespace / Shopify / Webflow/ Wix / Bubble)
- You need an admin panel that loads lots of data in complex ways (custom build)
- You need to test an API (Postman, SwaggerUI)
- You need to store data (Airtable)

How does Retool work

- Retool replaces a React/Vue/Angular SPA
- Sweet spot: set up data connections, load all the data when the page loads, route that data into drag-and-dropped components

How does Flank work

- Flank is a proxy runner. It takes the “run” button that is SELECT \* in a database IDE, or Postman, or the AWS Console, and makes it accessible to non-engineers
- Sweet spot: Engineer writes backend code, Flank scans code and extracts parameters, Flank creates a simple, shareable “run” button

Retool killer features

- Huge library of drag and drop components that replace React, component libraries, etc
- JavaScript “glue” between data sources (eg API and SQL) provides _just enough_ business logic to not have to write a little backend service

Flank killer features

- developer doesn’t have to learn a new tool of configure UI — Flank sits on top of existing services and automatically extracts parameters
