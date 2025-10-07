# Claude Code ↔ Fireworks Proxy

A lightweight proxy that allows Claude Code to use the Fireworks.ai API without the 5K token streaming limitation.  
It translates Anthropic-style requests into Fireworks-compatible requests, supporting both streaming and non-streaming modes and tool calls.

## Features

- Local proxy between Claude Code and Fireworks.ai
- Automatic streaming for all requests (>5K token support)
- Tool call support
- Logging of requests and responses in `/logs`
- Easy model switching with included selector script
- Written in TypeScript, runnable via `tsx` or npm global bin

## Requirements

- Node.js 18+
- Fireworks.ai API key
- Claude Code (or Anthropic-compatible client)

## Installation

You can install globally from npm:

```bash
npm install -g claude-code-fireworks.ai
```

```bash
ccf init
```
This will create `~/.claude-code-fireworks`

```bash
mv ~/.claude-code-fireworks/.env.example ~/.claude-code-fireworks/.env
```

Update .env with your Fireworks API key and choose model `FIREWORKS_API_KEY=fw_...`
`FIREWORKS_MODEL=accounts/fireworks/models/kimi-k2-instruct`

Start the proxy with Claude start
```bash
ccf start
```
