# Tableau, PowerBI, Looker

BI tools are used to build dashboards for executives. Basically, someone looking at a pretty visualization.

Flank is used to build quick-and-dirty functionality for *all* business people.

Phrased differently, BI tools read data. Flank can read data, but it can also be used to build tools that create, update, and delete data too (CRUD).  

|                      | Flank                                                                             | Tableau, Power BI, Looker                                                               |
| -------------------- | --------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------- |
| Used by              | Engineers (to build tools) and all manner of business people (to do stuff)        | Data analysts (to make dashboards) and executives (to never look at them)               |
| Problem it solves    | Quick-and-dirty functionality                                                     | Pretty data visualization                                                               |
| Best for             | Putting a SQL query in the hands of a business person                             | Building a dashboard for an executive                                                   |
| Typical workflow     | Write SQL in your IDE, Flank creates a page for it, share the URL with a teammate | Connect a DB, write SQL in the tool, create a visualization using drag-and-drop builder |
| Technically speaking | A wrapper around your DB that automatically creates quick-and-dirty BI pages      | Client (web or desktop) that queries DB and displays charts                             |
| Key simplification   | Simple dashboards can be *derived* from SQL                                       | Dashboards can be built with SQL + drag-and-drop                                        |
| Key difference       | Quick-and-dirty, point-and-click tool                                             | Rich data visualization, auto-refreshing data                                           |
| Throwback analogy    | Excel spreadsheets                                                                | Excel charts                                                                            |