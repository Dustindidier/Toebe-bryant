# Agent setup — Cursor, Grok and production bots

## Bring the project across
1. Open a trusted local terminal; clone `https://github.com/Dustindidier/Toebe-bryant.git` if no checkout exists. If it exists, inspect changes before updating main. Open the repository folder in Cursor.
2. Read the repo in agent mode using docs/PORTABLE_AGENT_KICKOFF.md. A web-only Grok chat needs attached Markdown or verified repository access; a URL alone is not proof every file was read.
3. Transfer necessary exports/reference clips privately. Repo access does not transfer this chat's attachments, cloud filesystem, cookies or Higgsfield library. Confirm asset availability on the destination machine.
4. Verify actual model availability in Cursor. If a model needs a separate provider key, enter it only in that host's secure settings. Do not assume a Grok subscription provides API credits or Cursor credits cover Higgsfield.

## Minimum working toolchain
| Need | Recommended route | Acceptance check |
|---|---|---|
| Repo continuity | Local Git; optional official GitHub MCP | Read expected branch/ref; inspect a diff; test only authorized writes |
| Media edit/QC | FFmpeg and FFprobe directly | Version, tiny local test, output probe/decode |
| Source review | Image/video viewer; local contact sheets | Actually open sources and exports |
| Automation | Python, approved masking/compositing libraries | Small non-sensitive test; preserve source hashes |
| Browser workflow | Host browser tool or official Playwright MCP | Inspect actual page; user completes authentication |
| Higgsfield generation | Verified supported connector/API or service UI | Account, cost/allowance, reference input and job retrieval verified |
| Optional filesystem | Scoped filesystem MCP | Limit roots; no broad home directory or secret access |

Official starting points to verify at installation time:
- GitHub MCP: https://github.com/github/github-mcp-server
- Playwright MCP: https://github.com/microsoft/playwright-mcp
- Filesystem reference server: https://github.com/modelcontextprotocol/servers/tree/main/src/filesystem
- FFmpeg: https://ffmpeg.org/download.html
- Cursor docs: https://cursor.com/docs ; follow current documentation for Rules, MCP and model access.

These are discovery starting points, not installations or security audits performed by this handoff. Pin reviewed versions where supported. Inspect requested scopes and command arguments before installing. No FFmpeg MCP is necessary for local editing. Avoid speculative MCP JSON with guessed endpoints/packages. Never commit credentials or authenticated browser state. Prefer least-privilege repo access over account-wide administration.

## Project instruction adapters
`.cursor/rules/toebe-project.mdc` points Cursor to the shared Markdown. Confirm the host loads it. `skills/toebe-production/SKILL.md` is a project-local skill source; register/copy it into the host's documented skill mechanism only after detecting support. Do not create separate competing brand bibles for different models.

If more structure is useful, create the following as sanitized Markdown: `logs/TOOL_READINESS.md` (date/tool/version/scopes/cost/test), `logs/PRODUCTION_QUEUE.md` (priority/owner/source/status/next gate) and dated shot/job logs from the templates. Create them from observations, not imaginary connected services. Raw media belongs outside the repository.

## Bot coordination
One coordinator holds the accepted task and budget. Assign bounded tasks and avoid simultaneous writes to session/decision logs. Use worktrees/branches for concurrent changes; integrate through ordinary reviewed merges. Each worker returns evidence and approval status. No bot may turn a coordinator proposal into spending/publication authority. Use sanitized chat-bridge Markdown to coordinate with ChatGPT rather than assuming conversations synchronize.

## Reported state versus observed state
The previous cloud had FFmpeg/FFprobe 7.1.5. The current checked checkout contains 81 JPEGs, expected total 99. V4 production notes report Higgsfield completion and provisional-voice allowance during prior work; this environment's current tool catalog does not expose Higgsfield. All must be checked anew on the destination host. No account session or free-trial allowance is guaranteed to persist.
