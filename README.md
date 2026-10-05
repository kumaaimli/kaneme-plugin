# Kaneme

Kaneme makes your writing identity measurable and portable. You build a voice from texts you really wrote, Kaneme measures whether a new text still carries that voice rather than the generic voice of an AI, and your assistant can then write with it.

## What this plugin does

This plugin connects Claude to the Kaneme MCP server at `https://kaneme.com/api/mcp`. It adds no skill, hook, command or local program: every tool runs on Kaneme's servers, under your own Kaneme account.

- **Connection:** you sign in to Kaneme once, through OAuth, in your browser. Claude Code receives the authorization on the local port `33418`, which the plugin fixes so that a later re-authorization lands on the same address.
- **Data sent:** only what you ask a tool to use: the texts you choose to measure or to add to a voice, and the voice you name. Nothing is read from your files or your conversation history.
- **Network destination:** `kaneme.com` only. The plugin contacts no other service.
- **Cost:** measurements and writing use your Kaneme credits; the tools say what an action costs before you run it.

## Install in Claude Code

```
/plugin marketplace add kumaaimli/kaneme-plugin
/plugin install kaneme@kaneme
```

Then run `/mcp` and sign in to Kaneme when asked.

## Privacy and terms

- Privacy policy: https://kaneme.com/en/legal/privacy
- Terms: https://kaneme.com/en/legal/terms
- Support: https://kaneme.com/en/contact

## License

MIT.
