# Query Lens

A browser-only prototype that turns a parameterized SQL template and a JSON array of values into a readable, escaped debugging view. It supports PostgreSQL `$1`, `$2`, … placeholders and `?` placeholders, renders array values explicitly, and flags missing/unused parameters. It never connects to a database or executes SQL.

## Try it

Open `index.html` in any modern browser. Enter parameters as a JSON array in placeholder order (for example, `["alice", 42, true]` for `$1`, `$2`, and `$3`). The preloaded example demonstrates array substitution. Use **Explain query** to format edits; **Reset example** restores the sample.

## Iteration

After reviewing the first layout, I made the output explicitly a debugging-only representation, rendered arrays as `ARRAY[...]`, surfaced missing/unused-parameter warnings, and added malformed-JSON feedback. The interface also explains that all work stays in the browser and warns against pasting secrets or customer data.

## Scope

No server, dependencies, storage, network calls, or database access. This is a visualization aid, not a SQL parser or execution tool.
