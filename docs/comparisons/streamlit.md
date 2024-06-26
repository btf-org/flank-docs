# Streamlit

Streamlit and Flank both empower a single engineer/data scientist to build a quick app without involving other people/process.

Streamlit is the amazing tool for **turning a Python script into a interactive web app**. It empowers **data scientists** to build sharable apps on their own, which removes their dependency on engineers. Highly recommend.

Flank is a tool for **turning any "function" on the internet into a tool** ("function" = API endpoint, cloud function, stored proc). It empowers **all engineers** to release features without many of the burdens of the traditional development lifecycle.

|                      | Flank                                                                                                         | Streamlit                                                                                                                |
| -------------------- | ------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------ |
| Used by              | Engineers, to build general-purpose business software                                                         | Data scientists, to build interactive visualizations                                                                     |
| Problem it solves    | Building a webpage to do some CRUD operation, and hosting it                                                  | Building a webpage with interactive graphics, and hosting it                                                             |
| Best for             | Making some backend code (safely) accessible, and sharing it                                                  | Making a Jupyter notebook beautiful, and sharing it                                                                      |
| Typical workflow     | Write Python and deploy it, Flank detects it and creates a UI for it                                          | Write a Python script, run the streamlit server locally, make your visualizations and interactions rock, then publish it |
| Technically speaking | A "pointer" to run Python code (or any other type) that is hosted elsewhere                                   | Web framework for scripty Python code, with a graphing library, and then hosting services on top of it all               |
| Key simplification   | It's simpler to use autogenerated UI for the long tail of little things, and then to focus your time elswhere | It's simpler (and cheaper!) to build a data app using Python than it is to learn Tableau                                 |
| Key difference       | Interactive CRUD functionality, built from any hosted service                                                 | Interactive visualizations, built from Python                                                                            |
| Throwback analogy    | Single page application (SPA), decoupled from API, but automatically generated                                | It is to Python / data science what Rails + Heroku was to Ruby / web apps                                                |