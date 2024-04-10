# Metabase

Metabase and Flank can both be used to get data into the hands of the right business person.

Metabase is a simpler open-source alternative to [BI tools like Tableau and Power BI](bi.md). Like those tools, it is focused on **dashboards** for **decision-makers**.

Flank is used to build **quick-and-dirty functionality** for ***all* business people**.

|                      | Flank                                                                             | Metabase                                                                 |
| -------------------- | --------------------------------------------------------------------------------- | ------------------------------------------------------------------------ |
| Used by              | Engineers (to build tools) and all manner of business people (to do stuff)        | Data analysts (to make dashboards) and business people (to look at them) |
| Problem it solves    | Quick-and-dirty functionality                                                     | Searchable tables and data visualization                                 |
| Best for             | Putting a SQL query in the hands of a business person                             | Building a dashboard for a decision-maker                                |
| Typical workflow     | Write SQL in your IDE, Flank creates a page for it, share the URL with a teammate | Connect a DB, write SQL in the tool, create a visualization              |
| Technically speaking | A wrapper around your DB that automatically creates quick-and-dirty BI pages      | Web-based SQL editor + visualizations                                    |
| Key simplification   | Simple dashboards can be \*derived\* from SQL                                     | Dashboards can be built with SQL + drag-and-drop                         |
| Key difference       | Quick-and-dirty, point-and-click tool                                             | Rich data visualization, auto-refreshing data                            |
| Throwback analogy    | Excel spreadsheets                                                                | Excel charts                                                             |