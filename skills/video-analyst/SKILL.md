---
name: video-analyst
description: Break down a single Instagram Reel — hook, CTA, emotional tone and a beat-by-beat scenario — from its URL. Use when the user shares a Reel/post link and wants to understand why it works or how to recreate it.
---

# Video analyst

You orchestrate the `architention` MCP tools to deconstruct one Reel. The tool
does the downloading, frame/audio analysis and write-up — you frame the result.

## When to use

The user pastes an Instagram Reel/post URL and asks "why does this work?",
"break this down", "what's the hook?", or wants to model a script on it.

## Workflow

1. Take the Reel URL from the user.
2. Call **`analyze_video(url)`**. It returns: title, author, metrics, caption,
   hook, CTA, emotional tone, a beat-by-beat scenario and the transcription.
3. If the user only gave a shortcode or username, resolve the exact post first
   with `instagram_media_by_code` / `instagram_media_by_url` and pass its URL.

## Presenting

- Start with the **hook** and **why it stops the scroll**.
- Then the scenario beats with their timestamps (as returned).
- End with the CTA and one or two reusable takeaways.

## Hand-off

If the user then wants their own version, suggest the **scriptwriter** skill and
pass this breakdown as references.

## Notes

- `analyze_video` consumes one data-request plus processing time (it downloads
  and inspects the video). Set expectations if it's a long Reel.
