# Flank

Flank is a really **simple** and really **scalable** way to build business software — dashboards, internal tools, simple automations, BI, admin panels. 

It is **NOT** a tool for building custom websites, rich visualizations, or complicated interactions.

We named it *Flank* because we like to think that it out*flanks* (ha) the typical development lifecycle. 

Scroll down for a 5-10 minute quickstart. 👇 Hope you enjoy!

## Background
Our initial goal was to take all those ad-hoc SQL queries in text files on our computers and turn them into reusable tools.

First, we built a system for putting some UI and guardrails around stored procs, but then we realized that abstracing over stored procs was no different than abstracting over any other function exposed over the internet (e.g. REST API endpoints, AWS Lambdas, etc). Then we added a little functionality to pipe the output of one into the input of another, and suddenly this system had the ability to quickly build 90% of the tools that we needed--not the fancy stuff, but the long tail of ad-hoc queries and little feature tests that don't need differentiated UI/UX.

We've even used it ourselves to launch a product that we've sold into other orgs. (We're literally selling a single Python script as a "SaaS app" 🙈)

## Architecture

![arch](https://i.imgur.com/oSgKnRy.png)


## Getting Started
...


