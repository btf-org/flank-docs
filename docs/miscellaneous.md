# Miscellaneous
## Our stack

We’ve tried to keep our stack as simple as possible. 

On the frontend, we use Vue, Tailwind, Buefy, and Typescript. We’re particularly fond of a VSCode extension called JavaScript REPL, which provides a live REPL inside JS files.

On the backend, we use Python, FastAPI, Pydantic, SQLAlchemy and Postgres. We make extensive use of iPython, which combined with VSCode, allows us to shoot our code into the REPL, a la SLIME from the EMacs world. We've also built an "entity" abstraction on top of SQLAlchemy and FastAPI that is trying to solve the same problem as EdgeDB. Love FastAPI. Super easy to dive in and read the source code. 

We host the frontend in S3 (AWS) and Static Web Apps (Azure). We host the backend in Lambda (AWS) and Function Apps (Azure).

## Inspirations

### Unix

One of our key features is the ability to take the output of one command and to pass it into the input of another command. That idea came from Unix pipes. We’re just doing it with APIs and stored procs in a web app, rather than text processing programs in the shell.

### REPLs and Jupyter Notebooks

The entire premise of Flank is that software will be built more quickly when it is built in smaller units. REPLs and Jupyter Notebooks are the tools that made us feel this, in our bones.

### Notion

Our goal is to take the upfront cost of building an app to near zero, and that requires an obsessive focus on little micro-frictions. Notion addresses nearly invisible micro-frictions really well, so much so that almost nobody can describe what they like about it.

## About us

Bryce - Penn State dropout. Tried to make it as an Overwatch player. Had to fall back on business software problems.

Mallory - Reads long books. Keeps getting bit by dogs. Hates Azure.

Angus - Burned out on coding while working for Michael Jordan. Took a break and got unburned-out. Oh also he’s super tall and his name is Angus.

You can get in touch with us at [name] at flank.cloud
