# Zapier

Zapier and Flank both abstract over API endpoints, but the use cases are very different.

Zapier is great for sync'ing data between **3rd-party tools** when some **event** happens. For example, you get an email in GMail with "Feature Request" in the subject, Zapier automatically creates a new ticket in Trello.

Flank is for situations where an engineers needs to put **custom software** in front of a business person, and that person will **manually** click the button at unpredictable times.

|                      | Flank                                                                                                         | Zapier                                                                                         |
| -------------------- | ------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------- |
| Used by              | Engineers and Business People                                                                                 | Business people                                                                                |
| Problem it solves    | It's time-consuming for an engineer to build a button for a business person                                   | It's a pain to sync data between business products                                             |
| Best for             | Building *custom* business software where a human will be clicking around                                     | Connecting 3rd-party tools with event-based triggers                                           |
| Typical workflow     | Example: Business person needs to fetch a dataset, they go into Flank and remotely trigger a stored procedure | Example: When you receive an email in GMail with <these> keywords, create a new card in Trello |
| Technically speaking | A wrapper around your API/DB that gives business people a way to safely trigger functions/procs               | A listener on certain events in 3rd party tools, with chainable actions                        |
| Key simplification   | 90% of point-and-click apps/tools/dashboards can be derived from the backend code                             | A lot of ETL / reverse ETL is just a webhook + some chained API calls                          |
| Key difference       | Used by engineers to put a button in front of a business person                                               | Used by business people to fully automate data sync'ing                                        |
| Throwback analogy    | MSFT Access view layer (forms, reports)                                                                       | Excel macros, but instead of working across sheets, it's working across 3rd-party APIs         |
