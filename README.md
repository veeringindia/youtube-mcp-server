# YouTube MCP server

A hosted [Model Context Protocol](https://modelcontextprotocol.io) server that lets AI apps read YouTube: transcripts, search, and channel and playlist listings. Nothing to install: add the URL to your app and sign in.

```
https://youtubetranscriptapi.com/mcp
```

- **Hosted.** Works in Claude and ChatGPT on the web, where local servers can't run.
- **Sign in or use a key.** OAuth for Claude, ChatGPT and other clients that support it. An API key as `Authorization: Bearer tk_live_…` for IDEs, CLIs and automation.
- **No YouTube blocks to deal with.** Local caption scripts often get rate-limited or IP-blocked. Here you don't see YouTube's 429 errors.
- **Failed calls are free.** Only successful calls use credits. New accounts get 100 free credits, no card.

## Set it up

| App | How | Guide |
| --- | --- | --- |
| Claude (web, desktop, mobile) | Customize → Connectors → Add custom connector, then sign in | [Guide](https://youtubetranscriptapi.com/youtube-mcp-server/claude?ref=github) |
| ChatGPT | chatgpt.com/plugins → + → Add custom MCP server, then sign in | [Guide](https://youtubetranscriptapi.com/youtube-mcp-server/chatgpt?ref=github) |
| Claude Code | `claude mcp add --transport http youtube https://youtubetranscriptapi.com/mcp` | [Guide](https://youtubetranscriptapi.com/youtube-mcp-server/claude-code?ref=github) |
| Cursor | Install link, or `mcp.json` with a key | [Guide](https://youtubetranscriptapi.com/youtube-mcp-server/cursor?ref=github) |
| VS Code (Copilot) | Install link, or `.vscode/mcp.json` with a key | [Guide](https://youtubetranscriptapi.com/youtube-mcp-server/vs-code?ref=github) |
| n8n | MCP Client Tool, HTTP Streamable, Bearer credential | [Guide](https://youtubetranscriptapi.com/youtube-mcp-server/n8n?ref=github) |

## Tools

All tools are read-only. Costs apply only when a call succeeds.

| Tool | What it does | Credits |
| --- | --- | --- |
| `get_transcript` | The spoken text of a video, optionally with `[m:ss]` timestamps. Long videos come in parts; later parts are free for 24 hours. | 1 |
| `search_youtube` | Search YouTube for videos or channels | 4 |
| `search_channel` | Search one channel's videos for a topic | 1 |
| `list_channel_videos` | A channel's latest uploads, up to 100 | 20 |
| `get_latest_videos` | A channel's 15 newest videos | free |
| `resolve_channel` | An @handle or URL to the channel's ID | free |
| `list_playlist_videos` | The videos in a playlist, up to 100 | 20 |

Free tools need a balance of at least 1 credit. Full reference: [youtubetranscriptapi.com/docs/mcp](https://youtubetranscriptapi.com/docs/mcp?ref=github).

## Example prompts

- "Summarize this video in five bullet points: <link>"
- "What did the speaker say about pricing, with timestamps? <link>"
- "What has @channel posted this week? Two lines per video."

## Support

[youtubetranscriptapi.com/contact](https://youtubetranscriptapi.com/contact?ref=github)
