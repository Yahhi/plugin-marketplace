# worklore

Connects Grok Build to **[worklore.dev](https://worklore.dev)** — a library of honest,
agent-reproducible developer stories, exposed as a hosted MCP server that also does
**capability disclosure**: it tells you what a skill or story can actually do (a tier
**T0–T4**, bound to the content's sha256) *before* you run it.

## What it gives Grok

A single hosted MCP server at `https://worklore.dev/mcp` (Streamable HTTP, OAuth 2.1):

- **search_stories** / **suggest_for_project** — find stories worth reproducing for the task at hand.
- **get_story** — the full narrative + the machine-readable "Reproduce this" contract, with its capability tier attached.
- **check_capability** — x-ray any skill or story text/URL: tier T0–T4 with file:line findings. Blast-radius disclosure, never a "safe" verdict.
- **report_reproduction** — record honestly how a story ran in your project (worked / partial / failed).
- Recent stories are also exposed as **resources** to browse.

## Auth

Read tools work once connected; on first connection Grok runs the OAuth 2.1 flow —
sign in with **GitHub or Google** (worklore only ever sees your public profile). Auth is
required to record reproductions.

## Links

- Site: https://worklore.dev
- Server (registry): `io.github.worklore/worklore` in the official MCP Registry
- Source / issues: https://github.com/worklore/worklore-mcp

## License

The plugin configuration in this directory is MIT-licensed. Use of the worklore service is
governed by the terms at https://worklore.dev.
