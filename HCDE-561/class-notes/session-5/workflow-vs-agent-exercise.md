---
title: "Workflow vs Agent — Class Exercise Prompt"
---

# Workflow vs Agent — Class Exercise Prompt

> **Access caveat (confirmed):** the design URL below returns a **403 Forbidden** for anyone other than the originating Anthropic account session — even the instructor hit this. The prompt is recorded here for archival reference, but the design package is **not** generally fetchable.
>
> **Standalone offline copy:** [open Workflow vs Agent (offline)](https://spiffy-panda.github.io/HCDE-561-Notes/static/workflow-vs-agent-offline.html) — a self-contained HTML version of the artifact, hosted alongside this site. No auth required.

The prompt I'm running for the in-class "Workflow vs Agent" exercise:

```
Fetch this design file, read its readme, and implement the relevant aspects of the design. https://api.anthropic.com/v1/design/h/5jH2J3l30gH67q9l3hHNVA?open_file=Workflow+vs+Agent.html
Implement: Workflow vs Agent.html
```

## Notes

- The URL points to `api.anthropic.com/v1/design/...`, which is an authenticated endpoint — links of this shape appear tied to the Claude/Anthropic session that generated them, not to a generic share token. That matches the 403 behavior.
- "Implement" here means: read the design's README, then build out the `Workflow vs Agent.html` artifact according to whatever instructions/spec the design package contains. Without access to the README, the prompt is not self-executing.
- Run output and reflections will be added back here after the exercise (assuming a working version of the design link is reissued).

## Run log

*(to be filled in after running the prompt)*
