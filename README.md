# Architention for Claude Code

Bring Architention's Instagram research and AI analytics into Claude Code as
ready-to-use tools and skills:

- **Instagram data** — profiles, posts, Reels, hashtag feeds and search.
- **Profile analytics** — engagement, cadence and content-mix metrics plus AI
  positioning insights and growth recommendations.
- **Video analytics** — hook / CTA / emotional tone / beat-by-beat scenario for
  any Reel.
- **Scriptwriter** — production-ready Reel scripts from a brief.
- **Content strategist** — structured content plans grounded in real data.

This is a **paid** plugin. You need an active [Architention](https://architention.com)
subscription and your personal **license key**.

## Setup

### 1. Install the plugin

```bash
claude plugin marketplace add PavelBaboshkin/architention-mcp
claude plugin install architention-mcp@architention
```

### 2. Set your license key

Copy your key from the Architention dashboard → **MCP**, then:

```bash
export ARCHITENTION_LICENSE_KEY="arch_mcp_xxxxxxxx..."
```

Add that line to your shell profile (`~/.zshrc`, `~/.bashrc`) so it persists.

That's it — restart Claude Code and the `architention` tools become available.

### Alternative: connect the MCP server directly

If you'd rather not install the plugin, add the remote server in one command
(the key is passed inline):

```bash
claude mcp add --transport http architention https://mcp.architention.com/mcp \
  --header "X-License-Key: arch_mcp_xxxxxxxx..."
```

## Usage

Just ask in natural language — the bundled skills know which tools to call:

- "Analyze the Instagram profile @nasa and tell me how to grow it."
- "Break down this Reel: <url>"
- "Write me a 30-second Reel script about cold brew for a coffee shop."
- "Build a 4-week content plan for a fitness coach, 3 posts a week."

## Quota

Your plan includes a monthly budget of Instagram **data requests**. Profile and
video analysis spend a few requests each; the scriptwriter and content
strategist are free (they don't fetch Instagram data). Track usage and rotate
your key any time in the dashboard.
