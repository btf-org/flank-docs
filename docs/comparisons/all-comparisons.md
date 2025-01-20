# Comparisons
Flank is like a **barebones Retool**, or **Postman with guardrails**. Unlike other internal tool / BI apps, there's no drag-and-drop, no "extra" JS to write, and nothing to maintain.

## Internal Tools

### Retool, PowerApps, Budibase, etc.

Retool and Flank are both general purpose tools for building business software.

Retool is great for **rich UIs** and **interactive apps**. 

Flank is great for building **lots of small tools**, where the UI just needs to look as good as a Google Form.


|                      | Flank                                                                        | Retool                                                                                                           |
| -------------------- | ---------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------- |
| Used by              | Engineers and business people                                                | Ditto                                                                                                            |
| Best for             | Releasing functionality as quickly as possible, where UI doesn't matter much | Building internal websites with rich UIs                                                                         |
| Typical workflow     | Deploy SPROC/API endpoint, Flank generates a web page, you it share with teammmate like a Google Doc | Design a website by dragging and dropping a library of components onto the screen, then wire it up to SQL and JS |
| Technically speaking | Wrapper around SPROCs/API endpoints that provides guardrails and RBAC    | Drag-and-drop WYSIWYG website builder, with code editor and execution built in                                   |
| Key simplification   | 90% of features don't need a designed interface                              | Wiring up components is easier in a drag-and-drop editor than in pure HTML                                       |
| Key difference       | You write and deploy your code on your terms. Flank merely wraps it.         | Your code is written, stored, and executed in Retool's platform.                                                 |
| Throwback analogy    | GUI for the CLI                                                            | MS Access for the web                                                                                            |

### Slackbots
Slackbots and Flank are both great for quick-and-dirty tools that are often-built and over-designed.

Slackbots are great for real-time **alerting** and any functionality that can get away with **no interface** (either to input parameters or consume data in a table).

Flank is great for quick-and-dirty apps where you need some **guardrails** on input fields and you want to **view data** in a table.

|                      | Flank                                                                  | Slackbots                                                            |
| -------------------- | ---------------------------------------------------------------------- | -------------------------------------------------------------------- |
| Used by              | Engineers, to quickly expose functionality to business people          | Ditto                                                                |
| Problem it solves    | Creating a UI with guardrails                                          | Alerting, quick ways for people to ping a backend                    |
| Best for             | Tools that benefit from guardrails               | Tools that fit into a "message" paradigm                             |
| Typical workflow     | Deploy SPROC/API endpoint, Flank generates a web page, you it share with teammmate like a Google Doc           | Write backend service, write Slackbot to connect to it               |
| Technically speaking | A wrapper around your DB/API that creates UI for individual functions | A microservice responsible for receiving/sending messages to/from Slack |
| Key simplification   | A lot of "apps" are just a few input fields and a button               | A lot of "apps" are best consumed in a messaging paradigm            |
| Key difference       | Flank has input fields, buttons, and tables                                      | Slack is just messages                                                             |
| Throwback analogy    | GUI for the CLI                                                     | IRC bot                                                              |


### React & SPAs
Flank and React (and other SPAs like Angular & Vue) are both used to build websites.

React is a great framework for a **frontend engineer** to build a **completely custom** website **from the ground up**.

Flank is a tool for **any engineer** to **shortcut** the traditional development lifecycle and get quick functionality into the hands of business users.

|                      | Flank                                                        | SPAs                                                                                                                |
| -------------------- | ------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------- |
| Used by              | Engineers, to build apps super quickly                       | Engineers, to build anything                                                                                        |
| Problem it solves    | Traditional SDLC is overkill for quick functionality         | Vanilla HTML/JS/CSS doesn't model the way that engineers think about decomposing web apps                           |
| Best for             | Quick-and-dirty business applications                        | Highly interactive web sites, where data is constantly being passed back and forth to a backend                     |
| Typical workflow     | Deploy SPROC/API endpoint, Flank generates a web page, you it share with teammmate like a Google Doc                | Write backend service, write frontend code, test locally, host it, deploy it                                        |
| Technically speaking | A hosted app that transforms backend code into business apps | A way to write HTML + JS that more closely mirrors the way engineers think about web pages                          |
| Key simplification   | Many websites can be derived from the backend code           | Engineers look at a web page and think in terms of "components" that are hierarchical and distinct from one another |
| Key difference       | App that saves you from having to use a programming language | Programming language                                                                                                |
| Throwback analogy    | Autogenerated (and hosted) HTML/JS/CSS                       | Programming language that compiles to HTML/JS/CSS                                                                   |

### Rails & SSRs

Flank and Rails (and other SSRs like Django and ASP.NET) are both used to build websites.

Rails is a great framework for a **web developer** to build a **completely custom** website **from the ground up**.

Flank is a tool for **any engineer** to **shortcut** the traditional development lifecycle and get quick functionality into the hands of business users.

|                      | Flank                                                        | SSRs                                                                                                      |
| -------------------- | ------------------------------------------------------------ | --------------------------------------------------------------------------------------------------------- |
| Used by              | Engineers, to build apps super quickly                       | Engineers, to build anything                                                                              |
| Problem it solves    | Traditional SDLC is overkill for quick functionality         | Vanilla HTML/JS/CSS doesn't model the way that engineers think about decomposing web apps                 |
| Best for             | Quick-and-dirty business applications                        | Full featured websites where there isn't a ton of interactivity and data being passed to/from the backend |
| Typical workflow     | Deploy SPROC/API endpoint, Flank generates a web page, you it share with teammmate like a Google Doc                | Write backend service, write frontend code, test locally, host it, deploy it                              |
| Technically speaking | A hosted app that transforms backend code into business apps | A way to write HTML + JS that more closely mirrors the way engineers think about web pages                |
| Key simplification   | Many websites can be derived from the backend code           | Engineers look at a web application and think in terms of data that is wired up to views                  |
| Key difference       | App that saves you from having to use a programming language | Programming language                                                                                      |
| Throwback analogy    | Autogenerated (and hosted) HTML/JS/CSS                       | Programming language that compiles to HTML/JS/CSS + backend code + SQL                                    |

## DevTools

### Postman

Postman and Flank are similar in that they both sit on top existing code/services and don't house any app logic themselves.

Postman is a tool for **building and testing APIs** that's used by **engineers**.

Flank is a tool for quickly building **UI with guardrails** to put in front of **business people**.


|                      | Flank                                                                                                           | Postman                                                |
| -------------------- | --------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------ |
| Used by              | Engineers and Business People                                                                                   | Just Engineers                                         |
| Problem it solves    | It's difficult to quickly and safely expose API functionality to business people                                | Difficult to develop and test an API in the terminal   |
| Best for             | Building business software                                                                                      | Developing and testing APIs                            |
| Typical workflow     | Deploy an API endpoint, Flank generates a web page for it, can be combined with other endpoints to create tools | Import an API spec, make API requests                  |
| Technically speaking | A wrapper around your API that provides autogenerated UI                                                        | Thin client for making HTTP requests                   |
| Key simplification   | 90% of internal apps are just input boxes and buttons that are wired up to API endpoints                        | Everything you do with \`curl\` is much easier in a UI |
| Key difference       | Intended to be used by business people                                                                          | Many more testing and debugging utilities              |
| Throwback analogy    | An API => HTML compiler                                                                                         | Interface for \`curl\`                                 |

### Swagger UI

Swagger UI and Flank are similar in that they both autogenereate UI from backend code.

Swagger UI is great for quickly **testing API endpoints**. It's like a quick-and-dirty [Postman](postman.md).

Flank is used to **build business applications** -- it has RBAC, guardrails and everything else necessary to safely expose functionality to business users. Not to mention the ability to combine two endpoints to make a more sophisicated tool.

|                      | Flank                                                                                                                   | SwaggerUI                                                            |
| -------------------- | ----------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------- |
| Used by              | Engineers and Business People                                                                                           | Just Engineers                                                       |
| Problem it solves    | It's difficult to quickly and safely expose API functionality to business people                                        | Difficult to lookup API endpoints and make calls in the terminal     |
| Best for             | Building business software                                                                                              | Quickly testing APIs                                                 |
| Typical workflow     | Deploy an API endpoint, Flank generates a web page for it, can be combined with other endpoints to create tools         | Create an API spec, SwaggerUI is generated, make some test requests  |
| Technically speaking | A wrapper around your API that provides auth + RBAC + guardrails + history                                              | Web page for making API requests                                     |
| Key simplification   | 90% of internal apps can be modeled as a SwaggerUI input, with just a \*little\* more guardrails and ability to combine | Input fields are easier than wrangling with JSON and curl in the CLI |
| Key difference       | Intended to be used by business people                                                                                  | Intended for engineers (no guardrails, RBAC, etc)                    |
| Throwback analogy    | Visual Unix pipes                                                                                                       | An API => HTML compiler                                              |

### PopSQL

PopSQL and Flank both allow teams to "share queries", but they're actually attacking different problems at different levels of abstraction.

PopSQL allows engineers to share **SQL code** with **other engineers**.

Flank allows engineers to share a **UI with guardrails** with **business people**.

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

### Snowflake Worksheets

Snowflake Worksheets and Flank both allow teams to "share queries", but they're actually attacking different problems at different levels of abstraction.

Snowflake Worksheets allow engineers to share **SQL code** with **other engineers**.

Flank allows engineers to safely share the **ability to execute SQL** with **business people** by autogenerating **UI with guardrails**.

|                      | Flank                                                                                                                                | Snowflake Worksheets                                                                                                            |
| -------------------- | ------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------- |
| Used by              | Engineers, to expose SQL (among other things), and business people, to run it                                                        | Engineers, to write and reuse SQL                                                                                               |
| Problem it solves    | Hard to safely expose SQL queries to business people                                                                                 | Sharing SQL queries is clunky                                                                                                   |
| Best for             | Exposing a stored procedure to a business person                                                                                     | Writing a SQL query that your teammate could reuse later                                                                        |
| Typical workflow     | Write SQL in your IDE, point Flank at it, share with a business person                                                               | Write SQL query in Snowflake, another teammate grabs it and runs it                                                             |
| Technically speaking | API that wraps stored procs, with a UI layer on top, which provides guardrails for business people to interact with the stored procs | Cloud-based SQL IDE that enables collaboration                                                                                  |
| Key simplification   | The UI to interact with stored procs can be derived from the procedure's parameters                                                  | Moving the "reusability" layer from stored procs to the cloud allows for some nice features (e.g. pretty names, usage tracking) |
| Key difference       | SQL runner with guardrails                                                                                                           | Collaborative SQL IDE                                                                                                           |
| Throwback analogy    | A web app that sits on top of a folder in git with a bunch of "team" queries                                                         | A folder in git with a bunch of "team" queries                                                                                  |

## Business Intelligence (BI)

### Tableau, PowerBI, Looker

BI tools and Flank can both be used to get data into the hands of the right business person.

BI tools are used to build **dashboards** for **executives**. Basically, someone looking at a **pretty visualization**.

Flank is used to build **quick-and-dirty functionality** for ***all* business people**.


|                      | Flank                                                                             | Tableau, Power BI, Looker                                                               |
| -------------------- | --------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------- |
| Used by              | Engineers (to build tools) and all manner of business people (to do stuff)        | Data analysts (to make dashboards) and executives (to never look at them)               |
| Problem it solves    | Quick-and-dirty functionality                                                     | Pretty data visualization                                                               |
| Best for             | Putting a SQL query in the hands of a business person                             | Building a dashboard for an executive                                                   |
| Typical workflow     | Write SQL in your IDE, Flank creates a page for it, share the URL with a teammate | Connect a DB, write SQL in the tool, create a visualization using drag-and-drop builder |
| Technically speaking | A wrapper around your DB that automatically creates quick-and-dirty BI pages      | Client (web or desktop) that queries DB and displays charts                             |
| Key simplification   | Simple dashboards can be *derived* from SQL                                       | Dashboards can be built with SQL + drag-and-drop                                        |
| Key difference       | Quick-and-dirty, point-and-click tool                                             | Rich data visualization, auto-refreshing data                                           |
| Throwback analogy    | Excel spreadsheets                                                                | Excel charts                                                                            |

### Metabase

Metabase and Flank can both be used to get data into the hands of the right business person.

Metabase is a simpler open-source alternative to [BI tools like Tableau and Power BI](bi.md). Like those tools, it is focused on **dashboards** for **decision-makers**.

Flank is used to build **quick-and-dirty functionality** for ***all* business people**.

|                      | Flank                                                                             | Metabase                                                                 |
| -------------------- | --------------------------------------------------------------------------------- | ------------------------------------------------------------------------ |
| Used by              | Engineers (to build tools) and all manner of business people (to do stuff)        | Data analysts (to make dashboards) and business people (to look at them) |
| Problem it solves    | Quick-and-dirty functionality                                                     | Searchable tables and data visualization                                 |
| Best for             | Putting a SQL query in the hands of a business person                             | Building a dashboard for a decision-maker                                |
| Typical workflow     | Write SQL in your IDE, Flank creates a page for it, share the URL with a teammate | Connect a DB, write SQL in the tool, create a visualization              |
| Technically speaking | A wrapper around your DB that automatically creates quick-and-dirty BI pages      | Web-based SQL editor + visualizations                                    |
| Key simplification   | Simple dashboards can be \*derived\* from SQL                                     | Dashboards can be built with SQL + drag-and-drop                         |
| Key difference       | Quick-and-dirty, point-and-click tool                                             | Rich data visualization, auto-refreshing data                            |
| Throwback analogy    | Excel spreadsheets                                                                | Excel charts                                                             |

### Streamlit

Streamlit and Flank both empower a single engineer/data scientist to build a quick app without involving other people/process.

Streamlit is the amazing tool for **turning a Python script into a interactive web app**. It empowers **data scientists** to build sharable apps on their own, which removes their dependency on engineers. Highly recommend.

Flank is a tool for **turning any "function" on the internet into a tool** ("function" = API endpoint, cloud function, stored proc). It empowers **all engineers** to release features without many of the burdens of the traditional development lifecycle.

|                      | Flank                                                                                                         | Streamlit                                                                                                                |
| -------------------- | ------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------ |
| Used by              | Engineers, to build general-purpose business software                                                         | Data scientists, to build interactive visualizations                                                                     |
| Problem it solves    | Building a webpage to do some CRUD operation, and hosting it                                                  | Building a webpage with interactive graphics, and hosting it                                                             |
| Best for             | Making some backend code (safely) accessible, and sharing it                                                  | Making a Jupyter notebook beautiful, and sharing it                                                                      |
| Typical workflow     | Write Python and deploy it, Flank detects it and creates a UI for it                                          | Write a Python script, run the streamlit server locally, make your visualizations and interactions rock, then publish it |
| Technically speaking | A "pointer" to run Python code (or any other type) that is hosted elsewhere                                   | Web framework for scripty Python code, with a graphing library, and then hosting services on top of it all               |
| Key simplification   | It's simpler to use autogenerated UI for the long tail of little things, and then to focus your time elswhere | It's simpler (and cheaper!) to build a data app using Python than it is to learn Tableau                                 |
| Key difference       | Interactive CRUD functionality, built from any hosted service                                                 | Interactive visualizations, built from Python                                                                            |
| Throwback analogy    | Single page application (SPA), decoupled from API, but automatically generated                                | It is to Python / data science what Rails + Heroku was to Ruby / web apps                                                |

## Automations

### Zapier

Zapier and Flank both abstract over API endpoints, but the use cases are very different.

Zapier is great for sync'ing data between **3rd-party tools** when some **event** happens. For example, you get an email in GMail with "Feature Request" in the subject, Zapier automatically creates a new ticket in Trello.

Flank is for situations where an engineers needs to put **custom software** in front of a business person, and that person will **manually** click the button at unpredictable times.

|                      | Flank                                                                                                         | Zapier                                                                                         |
| -------------------- | ------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------- |
| Used by              | Engineers and Business People                                                                                 | Business people                                                                                |
| Problem it solves    | It's time-consuming for an engineer to build a button for a business person                                   | It's a pain to sync data between business products                                             |
| Best for             | Building *custom* business software where a human will be clicking around                                     | Connecting 3rd-party tools with event-based triggers                                           |
| Typical workflow     | Example: Business person needs to fetch a dataset, they go into Flank and remotely trigger a stored procedure | Example: When you receive an email in GMail with <these> keywords, create a new card in Trello |
| Technically speaking | A wrapper around your API/DB that gives business people a way to safely trigger functions/procs               | A listener on certain events in 3rd party tools, with chainable actions                        |
| Key simplification   | 90% of point-and-click apps/tools/dashboards can be derived from the backend code                             | A lot of ETL / reverse ETL is just a webhook + some chained API calls                          |
| Key difference       | Used by engineers to put a button in front of a business person                                               | Used by business people to fully automate data sync'ing                                        |
| Throwback analogy    | MSFT Access view layer (forms, reports)                                                                       | Excel macros, but instead of working across sheets, it's working across 3rd-party APIs         |

### dbt

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

### Pipedream

Flank and Pipedream are both opinionated bundlings of cloud services that allow engineers to quickly build quick-and-dirty tools.

Pipedream is used by engineers to build **event-based automations**. It's particularly good at connecting **3rd-party APIs**.

Flank is used by engineers to build **business applications** where there's a **human in-the-loop**.

|                      | Flank                                                                                                         | Pipedream                                                                            |
| -------------------- | ------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------ |
| Used by              | Engineers, to build apps for business people                                                                  | Engineers, to build automations                                                      |
| Problem it solves    | It's time-consuming for an engineer to build a button for a business person                                   | It's a pain to build event-driven automations that connect a bunch of 3rd party APIs |
| Best for             | Building business software where a human will be clicking around                                              | Building event-based automations around 3rd-party APIs                               |
| Typical workflow     | Example: Business person needs to fetch a dataset, they go into Flank and remotely trigger a stored procedure | Example: Snowflake task fails, call the chatGPT API, then pipe the result into Slack |
| Technically speaking | A wrapper around your API/DB that gives business people a way to safely trigger functions/procs               | Web-based JS editor that deploys apps with webhooks that execute chains of functions |
| Key simplification   | 90% of point-and-click apps/tools/dashboards can be derived from the backend code                             | Many automations follow the pattern of webhook + function + function + function      |
| Key difference       | Button clicks                                                                                                 | Automations                                                                          |
| Throwback analogy    | Google Forms, that are wired up to backend services                                                           | Zapier, where you write JS                                                           |