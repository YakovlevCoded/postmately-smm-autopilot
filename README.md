# SMM Autopilot

A skill for AI agents that turns a website or topic into a month of social media posts, carousels and videos, gets approval, schedules through Postmately MCP, and measures what worked.

## Install

```bash
npx skills add YakovlevCoded/postmately-smm-autopilot
```

Or copy `SKILL.md` into your agent's skills folder.

## What it does

- builds a monthly content plan with four buckets: utility, process, trust and sale;
- generates carousels and vertical videos from a link or topic;
- validates every post for the chosen social network;
- waits for explicit approval before publishing;
- schedules through Postmately MCP;
- reads post and channel metrics and helps pick the next month.

## Setup

1. Create an API key in Postmately under Settings, then API.
2. Keep it in the environment as `POSTMATELY_API_KEY`.
3. Connect MCP: `https://api.postmately.com/mcp` with `Authorization: Bearer $POSTMATELY_API_KEY`.

## Guardrails

- No fake reviews, engagement farming or purchased followers.
- No auto-publish without explicit approval.
- No misleading claims or invented numbers.
- Respect each platform's rules and the channels the user owns.

## Links

- Postmately: https://postmately.com/
- Skill file: https://postmately.com/skills/smm-autopilot/SKILL.md
- MCP endpoint: https://api.postmately.com/mcp
