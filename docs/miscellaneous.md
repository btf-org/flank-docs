# Miscellaneous
## Our stack

On the frontend, we use Vue, Tailwind, Buefy, and Typescript. We’re particularly fond of a VSCode extension called JavaScript REPL, which provides a live REPL inside JS files.

On the backend, we use Python, FastAPI, Pydantic, SQLAlchemy and Postgres. We make extensive use of iPython, which combined with VSCode, allows us to shoot our code into the REPL, a la SLIME from the EMacs world. We've also built an "entity" abstraction on top of SQLAlchemy and FastAPI that is trying to solve the same problem as EdgeDB. Big fan of FastAPI. Super easy to dive in and read the source code. 

We host the frontend in S3 (AWS) and Static Web Apps (Azure). We host the backend in Lambda (AWS) and Function Apps (Azure).
