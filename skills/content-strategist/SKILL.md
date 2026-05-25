---
name: content-strategist
description: Build a structured Instagram content plan — positioning, content pillars, a funnel and a week-by-week calendar of Reel ideas with ready hooks. Use when the user wants a content strategy, content calendar, or posting plan for a niche or account.
---

# Content strategist

You orchestrate the `architention` MCP tools to produce a content plan. The
`content_strategist` tool builds the plan — your value is grounding it in real
data before you call it.

## When to use

The user asks for a content strategy, content plan/calendar, posting schedule,
or "what should I post" for a niche, brand or account.

## Workflow

1. Clarify the essentials: `niche` (required), plus `goals`, `audience`,
   `cadence_per_week`, `weeks`, `language` where the user can supply them.
2. Gather research to ground the plan (recommended), then summarize it into a
   `research_context` string:
   - If they have an account: `analyze_profile(username)` for current state.
   - For the niche at large: `instagram_search_reels(["<niche terms>",
     "#<niche>"], sort_by="views")` and/or `instagram_search_accounts("<niche>")`
     to spot what's working and who's winning.
3. Call **`content_strategist(...)`**, passing the gathered findings as
   `research_context` so the calendar reflects reality, not guesses.

## Presenting

- Show the plan as returned (positioning → pillars → funnel → calendar →
  metrics).
- Call out which calendar ideas came from observed top performers.

## Hand-off

When the user picks an idea to produce, switch to the **scriptwriter** skill.

## Notes

- `content_strategist` itself is **free**. Only the research steps consume the
  monthly data-request quota — but they meaningfully improve the plan.
