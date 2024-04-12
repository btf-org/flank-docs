# Design Decisions and Tradeoffs

## No deployment

*Flank doesn't help with deploying SQL / backend code / scripts.*

We started with SQL in .txt files on our computer. Initially we thought, "Let's get those text files hosted somewhere!" But then we realized it was simpler to just save all our SQL as stored procedures, and for Flank to sit on top of the DB. Also, a lot of people a lot smarter than us have put a lot of thought into how make deployment better...

**Pro:** Flank has one job

**Con:** You need to figure out some deployment stuff on your own

## No coding

*Flank is not a tool where engineers write code*

Once we built the Flank interface and we had a database connection set up, it was tempting to say, "Let's just write some SQL here in the browser so we don't have to pop into another app..." 

**Pro:** Backend code remains under your control, and there's no temptation to write it in Flank

**Con:** It's harder to write a little code to fix this or that

## No loops or conditionals

*Flank is not a low-code/visual programming tool*

Once we added the ability to put two (or three) stored procedures on the page, there was a temptation to add the ability to do things like: *Based on the result of stored procedure A, either execute B or C*. But there are lots of tools out there solving this problem -- Azure Logic Apps, AWS Step Functions, Airflow, Pipedream. Not to mention the aforementioend logic could be wrapped up in a *fourth* stored procedure, D, and then *that* could be exposed.

**Pro:** App logic remains under your control, and there's no temptation to let it sneak into Flank

**Con:** You can't quickly upgrade from a manual runbook to a nifty automation

## No conditional UI

*Flank doesn't support conditional or interactive UI*

Imagine you're building a booking system that presents a user with "Would you like to book a flight, hotel or car?" And then, based on their choice, different options appear below. Flank doesn't support the conditional rendering of UI. Our attitude is that there are already great tools and frameworks for building an app like that. Our philosophy has beeen to make the simple things fast, and to make it easy to "boot out" into another tool when an app outgrows Flank.

**Pro:** Flank doesn't creep into the tweener zone, where you're tempted to keep using it when you should just build a React app or something

**Con:** At some point, you'll be compelled to "boot out" of Flank

## No logging (sort of)

*Flank doesn't display logs out of the box*

We had some long-running tasks where it would have been helpful to see the logs in Flank. We were tempted to figure out some way to automatically pipe them into Flank. However, Flank is intended to be consumed by business people. Logs are for engineers. Instead, we added the ability for a task to explicitly write "logs" back to Flank.

**Pro:** Keeps interface user-friendly for business people

**Con:** Occasionally requires user to write code specifically to make something work with Flank, and, in this case, results in two sets of logging statements


## 15 minute timeout

*Flank's backend is hosted in Lambda, which as a 15 minute timeout per request*

When a user clicks the "run" button on a stored procedure, the Flank API just calls the stored proc on behalf of the user. That request has a 15 minute timeout. So Flank will lose track of any queries that take longer than 15 minutes. There was a temptation to simply host Flank in a container on a service with no timeout, like Fargate.

We decided to keep the backend in a Lambda and allow users to "write back" results for tasks that take longer than 15 minute. This requires users to write some code of their own to support Flank usage, which ruins a bit of the magic (and the claim that we're 100% decoupled). The reasoning was that, generally speaking, we should focus on supporting the 80% use cases out of the box, and then we should support the long tail of random stuff by making the system more hackable.

**Pro:** Makes *our* lives cheaper/simpler, which doesn't *directly* help you, but it allows us to move faster on the important stuff

**Con:** Occasionally requires user to write code specifically to make something work with Flank