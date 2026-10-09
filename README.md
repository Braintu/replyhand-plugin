# Replyhand for AI assistants

<img src="assets/logo.png" width="96" height="96" alt="Replyhand logo">

Replyhand is the AI agent and live CRM for businesses that talk to their customers on WhatsApp, Instagram, Messenger and their website. Connect it to work with your own Replyhand workspace in plain language.

What you can do:
- Find what customers asked about, by topic, customer, channel or date, with a link to each conversation.
- Look up contacts, and read and move the deals in your sales pipeline.
- Count and compare conversations, messages and deals, and see the numbers as charts.
- Keep your product catalog current: add or edit products, or import a price list.
- Train the AI agent that answers your customers: its Instructions, Q&A and knowledge sources.
- Set up automatic WhatsApp messages, such as booking reminders.
- Run the team: invite people, change roles, set working hours and choose who replies, the AI agent or your team.
- Create and manage click-to-message ads on Facebook and Instagram, billed by Meta to your own ad account.

How it works:
You sign in with your Replyhand account and choose one workspace. Reading is always on; making changes is a separate permission you can leave off. Replyhand can do only what your role allows. Before an important change, such as inviting someone, editing the AI agent or deleting products, it shows you a preview and applies the change only after you say yes in the chat.

Limitations:
Requires a Replyhand account. One connection reaches one workspace. Replyhand does not reply to your customers from here: the AI agent and your team do that in Replyhand.

**Server URL:** `https://replyhand.com/mcp` (remote MCP server, Streamable HTTP). There is no API key: the first time, your assistant opens Replyhand in the browser for you to sign in. Disconnect it anytime in Replyhand, in Settings under Account.

## Install

### Cursor

Install Replyhand from the Cursor Marketplace, or add the server to `~/.cursor/mcp.json`:

```json
{
  "mcpServers": {
    "replyhand": {
      "url": "https://replyhand.com/mcp"
    }
  }
}
```

### Grok Bot

Grok Bot installs apps from the Cursor Marketplace: open Connect apps, find Replyhand and choose Add.

### Gemini CLI

```sh
gemini extensions install https://github.com/Braintu/replyhand-plugin
```

Then run `/mcp auth replyhand` in Gemini CLI to sign in.

### Claude Code

```sh
claude mcp add --transport http --scope user replyhand https://replyhand.com/mcp
claude mcp login replyhand
```

### Codex

```sh
codex mcp add replyhand --url https://replyhand.com/mcp
codex mcp login replyhand
```

### Claude (web, desktop and mobile)

Settings, Connectors, Add custom connector. Paste `https://replyhand.com/mcp` and choose Connect.

### ChatGPT

Turn on developer mode in Settings, then add `https://replyhand.com/mcp` as a custom MCP server under Plugins.

### Any other assistant

Add `https://replyhand.com/mcp` as a remote MCP server. The full guide covers more apps: [replyhand.com/mcp](https://replyhand.com/mcp), and its version for AI assistants: [replyhand.com/mcp.md](https://replyhand.com/mcp.md).

## What this repository contains

Nothing here runs on your computer: every file only points your assistant at `https://replyhand.com/mcp`.

| File | What it is |
| --- | --- |
| `.cursor-plugin/plugin.json` | The plugin manifest for Cursor and Grok Bot |
| `mcp.json` | The server address, for Cursor |
| `gemini-extension.json` | The extension manifest for Gemini CLI |
| `GEMINI.md` | Short instructions Gemini CLI gives the AI model |
| `assets/logo.png` | The Replyhand logo |

## Help, privacy and terms

- Help: [replyhand.com/help](https://replyhand.com/help) or support@replyhand.com
- Privacy policy: [replyhand.com/privacy](https://replyhand.com/privacy)
- Terms of service: [replyhand.com/terms](https://replyhand.com/terms)

## License

The files in this repository are released under the [MIT License](LICENSE). Replyhand and its logo are trademarks of Braintu Inc.; this license grants no right to use them.
