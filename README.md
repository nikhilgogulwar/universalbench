<p align="center">
  <img src="./logo.svg" width="90" alt="UniversalBench" />
</p>

<h1 align="center">UniversalBench</h1>

<p align="center">
  <strong>Your AI finally has hands.</strong>
</p>

<p align="center">
  Connect once. Your AI can now run code, push to GitHub, query databases,<br/>
  deploy, call APIs, manage credentials, and invoke any AI model.<br/>
  Not describe how. Actually do it.
</p>

<p align="center">
  <a href="https://universalbench.dev">universalbench.dev</a> &nbsp;·&nbsp;
  <a href="https://docs.universalbench.dev">Docs</a> &nbsp;·&nbsp;
  <a href="https://universalbench.dev/#signup">Sign up free</a>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/free%20tier-1%2C000%20calls%2Fmonth-brightgreen" />
  <img src="https://img.shields.io/badge/MCP-compatible-blue" />
  <img src="https://img.shields.io/badge/works%20with-any%20AI-purple" />
</p>

---

## The problem

Your AI is genuinely intelligent. It can reason, plan, write code, and solve complex problems.

But it cannot do anything in the real world on its own.

It can write a Python script. It cannot run it. It can suggest a Git commit. It cannot push it. It can write a database query. It cannot execute it. It can describe a deployment. It cannot ship it.

It knows how to do the work. It has no hands to do it with.

---

## What UniversalBench does

UniversalBench gives your AI a cloud computer it can use as a tool.

Connect one URL to any MCP-compatible AI. From that moment your AI can:

- **Run the code it writes**, execute Python and bash in an isolated sandbox, see real output, fix errors, iterate
- **Push to GitHub**, read repos, commit files, validate code before it lands, roll back automatically if a smoke test fails
- **Deploy and verify**, push a change, hit a health check, confirm the new version is serving, roll back if not
- **Query your databases**, structured queries, raw SQL, keyword search, inserts, upserts, against any database you connect
- **Call any API**, HTTP requests to any public endpoint with network safety built in
- **Invoke any AI model**, route to Claude, GPT-4o, Gemini, or any other model, with a cost ceiling enforced before the call runs
- **Store credentials once**, save a GitHub token or database URL to the vault, and every relevant tool reads it automatically
- **Run tasks in parallel**, up to 8 concurrent execution threads for workflows that need speed
- **Snapshot any web page**, capture a full-page screenshot of any URL and get back a link that opens it, to show a result or confirm a page rendered correctly
- **Take files in and hand them back**, receive a file from someone through an upload link, work on it, and return a finished file as a clean branded download, with the file never passing through the chat

None of this is described. None of this is suggested. It is executed, confirmed, and returned.

---

## Connect in 30 seconds

**1.** Sign up free at [universalbench.dev](https://universalbench.dev). No credit card. 1,000 free calls per month from day one.

**2.** Copy your API key from the dashboard.

**3.** Paste this URL into any AI client:

```
https://universalbench-mcp.penantiaglobal.workers.dev/u/YOUR_API_KEY
```

### Claude.ai
Settings → Integrations → Add custom integration → paste the URL.

### Cursor / Windsurf / VS Code Copilot
```json
{
  "mcpServers": {
    "universalbench": {
      "url": "https://universalbench-mcp.penantiaglobal.workers.dev/u/YOUR_API_KEY"
    }
  }
}
```

### Claude Desktop
```json
{
  "mcpServers": {
    "universalbench": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/client-sse",
               "https://universalbench-mcp.penantiaglobal.workers.dev/u/YOUR_API_KEY"]
    }
  }
}
```

Works with any MCP-compatible client: Claude, ChatGPT, Gemini, GitHub Copilot, Cursor, Windsurf, and more.

---

## What this looks like in practice

### Your AI ships code, not just writes it

Without UniversalBench, your AI writes the function, you copy it, run it yourself, see an error, paste it back. Back and forth until something works.

With UniversalBench, your AI writes the function, runs it, sees the error, fixes it, runs it again, confirms it works, pushes the commit, hits the health check, and tells you it is live. You asked once. It shipped.

### Your AI works your data, not just talks about it

You have a log file with 50,000 lines. Without a runtime, your AI reads as much as fits in context and estimates the rest.

With UniversalBench, your AI writes a script, runs it against the full file in the sandbox, and returns the exact answer. Every row processed. One round trip.

### Your AI manages your infrastructure

> "Check the last 100 database rows for anomalies, open a GitHub issue if you find any, and send me a summary."

One prompt. Your AI queries the database, finds the anomaly, writes the GitHub issue, opens it, and responds with what it found. No copy-pasting. No manual steps. No back and forth.

### Your AI coordinates other AIs

> "Run this summarisation task through three models and tell me which gives the best result per dollar."

Your AI calls each model, compares outputs, calculates cost per call, and reports back. UniversalBench enforces your spending ceiling before each call goes out.

### Your AI hands you finished files, and shows you results

Drop a messy spreadsheet into a link your AI gives you. It cleans it in the sandbox and hands back a polished file you can download. Ask it to check a page you just shipped, and it captures a full snapshot and returns a link that opens it. The files never pass through the chat, so there is no size limit and nothing to copy and paste.

---

## Three safety guarantees built in

These are not settings you configure. They run on every call, for every customer, by default.

**Your AI cannot push code that breaks your service.**
Every push is validated before the commit lands. The previous version is captured automatically. Provide a health check URL and we run a smoke test after deploy. If it fails, the previous version is restored.

**Your AI cannot burn your API budget.**
Every AI model call is cost-estimated before it runs. Calls over your ceiling are rejected. You set the limit. Default is $0.50 per call. Hard cap is $50.

**Your AI cannot reach your internal network.**
Every outbound HTTP request is checked against a blocklist before it leaves. Private IP ranges, loopback, link-local, and cloud metadata endpoints are blocked at the infrastructure level.

---

## What your AI can do

One connection. Three tools (`ub_read`, `ub_write`, `ub_ai`). Underneath them, your AI can:

- **Run code and shell**, execute Python and shell commands in an isolated sandbox, with state and files that persist across a session
- **Install what it needs**, pull in any package before running
- **Work in parallel**, run multiple tasks at once for speed
- **Search the live web**, real results with sources
- **Call any public API**, with internal-network access blocked by default
- **Invoke any AI model**, Claude, GPT, Gemini, and more, with a cost ceiling enforced before each call
- **Read and ship code on GitHub**, read repos, commit with validation, and roll back automatically if a deploy check fails
- **Query your databases**, structured queries, raw SQL, search, inserts and updates, against any database you connect, using your own credentials
- **Capture and preview pages**, take a full-page snapshot of any URL, or show a page your AI built, as a shareable link
- **Take files in and hand them back**, receive a file through an upload link, work on it, and return a finished, correctly-typed download, with files never passing through the chat
- **Persist memory and state**, keep context across sessions
- **Store credentials safely**, save a credential once in an encrypted vault and the right tools use it automatically, your AI never sees the value

Every capability runs behind the same safety checks: validated before code lands, cost-estimated before a model runs, and network-checked before a request leaves.

---

## Credentials, saved once

Store a credential once and your AI uses it on every future call, without ever seeing the value. Encrypted at rest. Save once, and the relevant tools start working automatically.

---

## Pricing

| | |
|---|---|
| Free | 1,000 calls per month, no credit card |
| Pay as you go | $0.008 per call after the free tier |
| Minimum top-up | $5 |

No subscription. No lock-in. Credits do not expire.

---

## Documentation

Full capability reference, quickstart guides, and agent-ready prompts at [docs.universalbench.dev](https://docs.universalbench.dev).

---

<p align="center">
  <a href="https://universalbench.dev/#signup"><strong>Sign up free, no credit card →</strong></a>
</p>
