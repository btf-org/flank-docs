# Miscellaneous
## Our stack

On the frontend, we use Vue, Tailwind, Buefy, and Typescript. We’re particularly fond of a VSCode extension called JavaScript REPL, which provides a live REPL inside JS files.

On the backend, we use Python, FastAPI, Pydantic, SQLAlchemy and Postgres. We make extensive use of iPython, which combined with VSCode, allows us to shoot our code into the REPL, a la SLIME from the EMacs world. We've also built an "entity" abstraction on top of SQLAlchemy and FastAPI that is trying to solve the same problem as EdgeDB. Big fan of FastAPI. Super easy to dive in and read the source code. 

We host the frontend in S3 (AWS) and Static Web Apps (Azure). We host the backend in Lambda (AWS) and Function Apps (Azure).

## Tools that inspire us

There are two tools that really influenced the way we think about programming. One is Unix pipes and the other is Jupyter Notebooks/REPLs. Then, from a UI/UX perspective, we really like how Notion does all the simple things really well and just gets out your way. In a weird way, Flank is sort of a mashup of those three things.

## Motivation

All of us were, at some point, engineers who were relied on to run stuff. We were turning into human run buttons, and that was annoying. The thinking was something like, _Once there's code in the cloud/database, shouldn't it be easy for anyone to run it? To recombine it with other programs?_