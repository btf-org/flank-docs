# Unexpected benefits

## More use cases than we realized

Initially, we had built a system that allowed business people to safely execute one stored procedure at a time, without the engineer having to build any UI. This was interesting and sort of useful, but the use cases were fairly limited. 

As we kept running into problems that we wanted immediately solutions for, we realized two things:

1. **If we could do stored procs, we could also do APIs** - Once you abstract over a stored procedure, you've really abstracted over any function that can be invoked over the internet (API endpoint, AWS Lambda, etc.)
2. **"Pipes" opened up a whole world of applications** - If you could figure out a way to "pipe" the output of a function into the input of another, that actually covers a lot of business use cases, like maybe 90%?

## Easy to maintain
Decoupled architectures are great and everything, but one of the annoying things is when the API interface changes and you have to rewire the frontend. Flank doesn't have the problem, since the UI is derived from the backend code. If the backend code changes, you just "refresh" everything in Flank.

## Scales well
In most web apps, the relationship between features and complexity is something like O(n^2). UI starts to clutter the screen. RBAC becomes complicated. Next thing you know, new employees have to be "trained" on the tool...

Flank is way simpler, for better or worse. Each stored procedure has it's own web page and it's own set of permissions. They're all independent of one another. Adding a new stored proc just makes the list grow longer. It's more like O(n).  

## No lock-in
Flank merely "sits on top of" or "wraps" existing stored procedures. There's no app logic in Flank. If you were to stop using Flank, your stored procedure would be right where you left it.

## Latent demand
If you give a mouse a cookie, he's going to ask for a glass of milk. Similarly, if you give a business person a button, they're going to press that thing a million times. 