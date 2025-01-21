# How Does It Work?

<!-- ## Architecture -->

## Step by Step

1. **Deploy** - You deploy a stored procedure (or API endpoint) on your infra
3. **Diff** - In Flank, you run a diff against your database (or Swagger Doc)
4. **Commit**. - Flank imports metadata about the input parameters
5. **Share/Run** - You share the function with a teammate, and they run it on their own

## Further steps

- **Dropdowns** - Either hardcoded or populated by the output of another function
- **Tables with buttons** - Wire up the outputs of one function to the input of another
- **Cron** - Run stored procedures (or API endpoints) on a schedule