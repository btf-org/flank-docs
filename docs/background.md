# Backstory

### A modest v1
We were writing a lot of SQL for business people, so we had these **text files with SQL saved on our computers**. Initially we wondered, *could we take those text files and turn them into reusable tools?*

The first version was not text files but stored procs. First we built an API that wrapped our stored procs, then we built a UI layer on top of that, which provided some **guardrails for running the stored procs**.

This app allowed us to expose stored procs to teammates, one at a time.

### More coverage
Then we realized that if our API wrapped stored procs, it could wrap *any* "function" that's exposed over the internet -- API endpoints, AWS Lambdas, etc. Interesting... 

Next we added a little functionality to pipe the output of one stored proc into the input of another. We realized that most internal tools (at least, the simple ones) can be modeled as a combination of two stored procedures -- get a table of data, do something to each row.

### Unexpected benefits

As we've used the system ourselves, there are a few unexpected benefits we've come to like about it.

One is that it's **easy to maintain**, because if you add a parameter to a stored proc, the Flank API picks up on it, and then the UI updates accordingly.

Also, it **scales well** (better than GUI apps in certain ways) because each stored proc gets its own page and has its own RBAC. In a lot of GUI apps, each incremental feature makes the whole system more complicated.

Also it's **easy to boot out of**. The Flank API "wraps" or "sits on top of" your stored procs, so there's no lock-in. We've actually used this feature ourselves. We launched a simple product with Flank, one that we've sold into other orgs. And then booted out of it at a certain point.