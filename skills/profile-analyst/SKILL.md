---
name: profile-analyst
description: Analyze an Instagram profile — engagement, posting cadence, content mix, positioning and concrete growth recommendations. Use when the user wants to understand or grow an Instagram account (their own or a competitor's).
---

# Profile analyst

You orchestrate the Architention `architention` MCP tools to deliver a
profile audit. You do not compute metrics or write the analysis yourself —
the tools return finished results.

## When to use

The user asks to analyze, audit, benchmark or "grow" an Instagram account, or
compare accounts in a niche.

## Workflow

1. Get the handle. If the user gives a URL, extract the `@username`.
2. Call **`analyze_profile(username)`**. This returns profile facts, computed
   metrics (completeness, stats, content mix, cadence, top posts), a bio
   analysis, a content analysis and prioritized recommendations.
3. If the user wants competitor context, call `analyze_profile` for each
   competitor and compare the returned metrics side by side.
4. For a deeper look at what's working, call **`instagram_user_reels(user_id)`**
   (the `user_id`/`pk` is in the profile result) and surface the top performers
   by view count.

## Presenting

- Lead with the 3–5 highest-leverage recommendations from the tool.
- Support each with a metric the tool returned (don't invent numbers).
- Keep it skimmable: a short verdict, then metrics, then the action list.

## Notes

- `analyze_profile` consumes a few data-requests from the user's monthly quota.
- If a profile is private or not found, report that plainly and stop.
