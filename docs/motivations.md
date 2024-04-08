# Motivations

In our past jobs, we built business software. Things like dashboards, automations, internal products, tools, and admin panels.

Which is to say, if you’re an embedded systems engineer, you’re probably in the wrong place.

There were three motivations for building Flank:

### Urgent requests for data and product fixes

We all worked at companies that relied on the engineers to fix things. A quick query. Kicking off a job that failed. Changing a value in the database.

Dealing with these requests sucked, but it was better than the alternatives. Giving people access to the database could create WAY more work. And building them an app to do the job wasn’t worth it, especially for just that once.

But it always starts with just that one time… at what point do you build an app? The third time? The tenth time?

We wondered to ourselves, “Is there a way we could get leverage on these so-called one off fixes?”

### Requirements would change, and our work would get scrapped

When we did commit to building tools, half the time they’d get thrown away. Either the spec made no sense, or the business focus would change, or someone from another department would step into a meeting and say, “We’ve already got something that solves this problem.”

We wondered to ourselves, “Is there a way to prototype features more quickly? To build less while still learning the same amount?”

### The tools that we built spawned _even more_ urgent fixes

We built tools to take ourselves out of the loop, but then… The tools would go down. Our users would punch a string into a field that required an int. The backend API would change and the frontend would be out of date.

We wondered to ourselves, “Could we templatize guardrails in some way? Could we make it easier to get visibility into the system?”

## Goals

With those goals in mind, we set out to build a dashboard / app / tool builder that…

1. Had an upfront cost close to 0
2. Covered 90% of our internal tooling / dashboarding / admin panel use cases
3. Provided out-of-the-box guardrails and access control
4. Allowed the engineers to quickly figure out who did what whenever things did go wrong
