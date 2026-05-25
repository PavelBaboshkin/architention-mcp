---
name: scriptwriter
description: Write a production-ready Instagram Reel script (hooks, timecoded beats, voiceover, on-screen text, CTA, caption, hashtags) from a brief. Use when the user wants a Reel script, hook ideas, or a shootable scenario.
---

# Scriptwriter

You orchestrate the `architention` MCP tools to produce a ready-to-shoot Reel
script. The `scriptwriter` tool holds the craft — your job is to gather a good
brief and, when useful, ground it in real examples.

## When to use

The user asks for a Reel script, hooks, a video idea they can shoot, or a
scenario for a specific topic.

## Workflow

1. Collect the brief. Ask only for what's missing, then call
   **`scriptwriter(...)`** with: `topic` (required), and any of `niche`,
   `audience`, `tone`, `duration_seconds`, `format_hint`, `references`,
   `language`.
2. To ground the script in what's currently working, optionally first:
   - `instagram_search_reels(["<topic>", "#<topic>"], sort_by="views")` to find
     top performers, or
   - `analyze_video(url)` on a reference the user likes — then pass the key
     findings into the `references` argument.
3. Return the script the tool produced.

## Presenting

- Show the script as-is (it's already structured: hook options → beats →
  production tips → caption + hashtags).
- If you used references, note which real Reels informed the hooks.

## Notes

- `scriptwriter` itself is **free** (no Instagram data fetch). Only the optional
  research steps (`instagram_search_reels`, `analyze_video`) consume quota.
- Default to the user's language; pass `language` explicitly if unclear.
