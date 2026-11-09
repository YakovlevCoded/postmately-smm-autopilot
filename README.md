# SMM Autopilot

A skill for AI agents (Claude, ChatGPT, Claude Code, Codex, Cursor, Gemini CLI, OpenClaw) that turns a website or topic into a month of social media posts, carousels and short videos, gets your approval, publishes through [Postmately](https://postmately.com/en/) MCP, and measures what worked.

Publishes to TikTok, YouTube, Instagram, Facebook, Threads, Pinterest, Telegram channels, VK, Bluesky and Mastodon. LinkedIn is in platform review. One of the few MCP servers that posts to VK and Telegram.

## Try it

After setup, ask your agent:

> Run SMM for https://example.com: build a plan for next month, make 3 carousels and 1 video, and show me the drafts before anything is published.

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

The MCP server signs you in with OAuth: add it, approve access to your Postmately workspace once, done.

- **claude.ai / Claude Desktop:** Settings, Connectors, Add custom connector, `https://api.postmately.com/mcp`.
- **ChatGPT:** add `https://api.postmately.com/mcp` as a connector (developer mode) or install the Postmately app once it is listed.
- **Claude Code:**

  ```bash
  claude mcp add --transport http postmately https://api.postmately.com/mcp
  ```

- **Gemini CLI:**

  ```bash
  gemini extensions install https://github.com/YakovlevCoded/postmately-smm-autopilot
  ```

- **Cursor, Codex, scripts:** the same URL with OAuth, or an API key from Postmately Settings, API sent as
  `Authorization: Bearer <key>`.

The free plan covers a content plan, 3 carousels and 1 video, no card. The server is listed in the [official MCP Registry](https://registry.modelcontextprotocol.io/v0/servers?search=postmately) as `com.postmately/postmately`.

## Guardrails

- No fake reviews, engagement farming or purchased followers.
- No auto-publish without explicit approval.
- No misleading claims or invented numbers.
- Respect each platform's rules and the channels the user owns.

## Links

- Postmately: https://postmately.com/
- Skill file: https://postmately.com/skills/smm-autopilot/SKILL.md
- MCP endpoint: https://api.postmately.com/mcp
- Skills for AI agents: https://postmately.com/en/skills/

## License

MIT
