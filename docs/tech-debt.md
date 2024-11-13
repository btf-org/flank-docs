# No tech debt?

Flank is inspired by the previous generations of internal tool builders, and designed to address some of their shortcomings when it comes to scaling.

## No "code seep"
You don't write any code in Flank. You write code in your IDE and deploy it with your CI/CD. Flank is just a proxy for running it on your infrastructure.

## No lock-in
There is effectively zero "app logic" in Flank. No JS, no loops, no conditionals.  You could put 100 stored procedures into Flank, throw Flank out the window, and you'd still have your 100 stored procedures.

## No design debt
There's no drag-and-drop in Flank. Nothing to design. No Frankenstein UIs that require a whole wiki to onboard new hires.

## No 2-D permissioning complexity
No conditionally rendered components if `userLevel == 'intern'`. Flank is organized at the level of individual queries/endpoints. Everything is permissioned at that level.

## No breaking changes
Flank stays in sync with changes to backend code (via an API schema or RDBMS metadata), so if you add or remove a parameter, it doesn't break the end user app.

## Deprecate with confidence
_Is it safe to deprecate this stored procedure? When was the last time anyone used it...?_ Flank provides out-of-the-box analytics on who ran what, and when they ran it.

## Track down errors with speed
If a button doesn't work in a React app, it takes a small army of people (and JIRA tickets) to figure out which API call failed. In Flank, you just look at failed executions and you can see exactly which call failed and what the user's input was.

## Arbitrarily large datasets
Most internal tool builders are simply replacements for your frontend, so they're constrained by browser memory. If Flank encounters a large dataset, it saves the data behind the scenes and only returns a truncated version to the frontend. Users can then download the full version to file.

## Manage PII deletion / location
If there's an endpoint/query that returns PII, you can flag it and have Flank auto-delete the data after a certain time period. If you have European data, and you have BLOB storage hooked up in a European availaiblity zone, you can just point and click and tell Flank to store the data there.