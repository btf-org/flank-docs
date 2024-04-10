# Flank

Flank is a really **simple** and really **scalable** way to build business software — dashboards, internal tools, simple automations, BI, admin panels, even simple products. 

It is **NOT** a tool for building custom websites, rich visualizations, or complicated interactions.

[Check out the 5 min Quick Start]("quickstarts/jupyter-fastapi.md")

## Background
We were writing a lot of ad-hoc SQL queries and saving them in text files locally. Initially we wondered, *could we take those text files and turn them into reusable tools?*

The first version was not text files but stored procs. First we built an API that wrapped our stored procs, then we built a UI layer on top of that, which provided some guardrails for running the stored procs.

Then we realized that if our API wrapped stored procs, it could wrap *any* "function" that's exposed over the internet -- API endpoints, AWS Lambdas, etc. Interesting... 

Next we added a little functionality to pipe the output of one into the input of another, and suddenly this system had the ability to quickly build 90% of the tools that we needed -- not the fancy stuff, but the long tail of ad-hoc queries and little features that don't need differentiated UI/UX. We've even used it ourselves to launch a simple product that we've sold into other orgs.

## Architecture

![arch](https://i.imgur.com/oSgKnRy.png)

...


