# UniversalBench

Give your AI a cloud computer behind one URL. Connect once and your agent can run code, read and write databases, commit to GitHub, search the web, and call any LLM. The platform does the heavy work and returns only the result, cutting token use by up to 96.5 percent on data-heavy tasks.

Three guarantees are enforced in code: your AI never ships code that fails to load, never spends past your ceiling, and can never reach your internal network. Works with Claude, Cursor, and any MCP-compatible client.

## Tools

- `ub_read`: inspect databases and GitHub, fetch files, check account status
- `ub_write`: run code, write to databases, commit to GitHub, deliver files
- `ub_ai`: call any LLM with cost safety on by default

## Connect

1. Create a free account at https://universalbench.dev (1000 free calls per month, no card)
2. Copy your API key from the dashboard
3. Open `mcp.json` and replace `YOUR_API_KEY` in the server URL with your key:

   `https://universalbench-mcp.penantiaglobal.workers.dev/u/YOUR_API_KEY`

Your agent can then use `ub_read`, `ub_write`, and `ub_ai`.

## Docs

https://docs.universalbench.dev
