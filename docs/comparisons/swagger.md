# Swagger UI / OpenAPI

Swagger UI is a web page that is generated from an API specification (an OpenAPI spec, formerly known as a Swagger Spec). Flank is similar to Swagger UI in that it too autogerates UI. The big difference is that Flank has more ability to "pipe" one API call into another (e.g. to create a dropdown) and it is designed for business applications -- it has RBAC, guardrails and everything else necessary to safely expose functionality to business users. 

|                      | Flank                                                                                                                   | Postman                                                              |
| -------------------- | ----------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------- |
| Used by              | Engineers and Business People                                                                                           | Just Engineers                                                       |
| Problem it solves    | It's difficult to quickly and safely expose API functionality to business people                                        | Difficult to lookup API endpoints and make calls in the terminal     |
| Best for             | Building business software                                                                                              | Quickly testing APIs                                                 |
| Typical workflow     | Deploy an API endpoint, Flank generates a web page for it, can be combined with other endpoints to create tools         | Create an API spec, SwaggerUI is generated, make some test requests  |
| Technically speaking | A wrapper around your API that provides auth + RBAC + guardrails + history                                              | Web page for making API requests                                     |
| Key simplification   | 90% of internal apps can be modeled as a SwaggerUI input, with just a \*little\* more guardrails and ability to combine | Input fields are easier than wrangling with JSON and curl in the CLI |
| Key difference       | Intended to be used by business people                                                                                  | Intended for engineers (no guardrails, RBAC, etc)                    |
| Throwback analogy    | Visual Unix pipes                                                                                                       | An API => HTML compiler                                              |
