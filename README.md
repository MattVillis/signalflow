# SignalFlow

AV signal-flow schematic editor for live event production.

## Open the app

**https://mattvillis.github.io/signalflow/** — nothing to install.

Works in any modern browser. Your custom symbols are kept in that browser
(localStorage); the shared symbol library is synced in automatically from
[signalflow-symbols](https://github.com/MattVillis/signalflow-symbols).
Projects save as `.signalflow.json` files via the **Save** button.

## Optional: AI symbol research

The **AI symbol builder** can research a device's rear panel from the web and
build the symbol for you. It runs through a small local bridge on your machine
using your own Claude Code login, so nothing is metered to a shared key.

1. Install [Node.js](https://nodejs.org) (LTS).
2. Install Claude Code and sign in:
   `npm install -g @anthropic-ai/claude-code` then `claude login`.
3. Download **SignalFlow-bridge.zip** from the
   [latest release](../../releases/latest), unzip it anywhere, and double-click
   **SignalFlow.bat** (Windows) or **signalflow.command** (macOS).

That starts the bridge (a minimised window) and opens the app. The AI
builder's engine switches to **bridge** on its own when it sees one running.
Run `node sf-bridge.mjs test` in the unzipped folder if it doesn't.

Without the bridge you can still use the AI builder with your own Anthropic
API key (engine: **Claude API**) or paste JSON from any agent (engine: **Agent prompt**).

## Sharing symbols

Hover a custom symbol in the library sidebar and click **⇡** — that opens a
pre-filled submission in the
[symbols repo](https://github.com/MattVillis/signalflow-symbols). Approved
symbols reach everyone on their next sync.

---
This repo holds the built app only; it is deployed automatically. Bug reports
and feature requests are welcome as [issues](../../issues).
