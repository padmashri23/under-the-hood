# The Architecture Behind Production-Ready Multi-Agent Systems

**📖 Read it here: https://padmashri23.github.io/under-the-hood/production-multi-agent-architecture/**

A beginner-friendly guide to how multi-agent systems are built when they have to work for real users, not just in a demo. One hub agent (the orchestrator) runs the job and calls helper agents (spokes) as tools. The article follows one running example, a travel assistant planning a 3-day Tokyo trip, through the plumbing that keeps that setup reliable. Every quote and number comes from a primary source; the illustrative examples are labeled as such.

## What it covers

1. **The orchestration loop:** receive, plan, call a sub-agent, read the result, decide, finish. Sub-agents exposed as tools (OpenAI Agents SDK `as_tool`). Stop conditions: turn limits (`max_turns`), a task-complete signal and a token budget. Includes a working code sample and the loop as pseudocode
2. **Routing:** LLM-based routing from tool names and descriptions, rule-based or intent-classifier routing, and hybrid routing
3. **Context isolation and passing:** fresh context per sub-agent, context rot, the four-part brief, and condensed 1,000 to 2,000 token results
4. **Structured input/output contracts:** why free text breaks, a JSON schema example, OpenAI Structured Outputs and Anthropic strict tool use, validation, and retry or reject
5. **State management:** the hub owns state, stateless spokes, LangGraph checkpointers and resuming after errors
6. **Parallel vs sequential execution:** independent jobs in parallel, dependent jobs in order, and aggregation at the hub
7. **Failure handling:** retry, fallback and human escalation, validation, delegation caps, and the MAST failure study
8. A start-to-finish walkthrough of one request, the token cost of multi-agent systems (2025 figures), a "when not to split the work" counterpoint from Cognition's 2025 and 2026 posts, a "Where to start" list, a glossary, and a short conclusion

Written for beginners and tech starters. Every key pointer from the brief has its own subheading, so it shows up in Notion's table of contents. Each section opens with an "In plain words" line and an everyday comparison, then the steps, then a "Good to know" note. Short sentences (about 9 words on average, Flesch reading ease about 80), every technical term defined, and the code explained line by line. Includes a start-to-finish table that follows one Tokyo request through all seven parts, and a "when not to split the work" counterpoint from Cognition. About 2,983 words above Sources & References (3,020 including the title block), counting headings, captions, tables and code.

## Visuals

| Visual | What it shows |
|---|---|
| `images/hub-and-spoke.png` | Figure 1. A travel assistant: the hub, four spokes (flights, hotels, weather, writer), the state store, and the request, brief and result arrows (conceptual) |
| `images/orchestration-loop.webm` | Figure 2. Animation of the hub's loop: round 1 sends flights, hotels and weather briefs at once, the hotels agent times out and is retried, round 2 calls the writer, then the task-complete signal stops it (illustrative). Also `orchestration-loop.gif` and `orchestration-loop-poster.png` for Notion |
| `images/routing-flow.png` | Figure 3. Hybrid routing flowchart: a rule match sends known paths straight to a spoke, ambiguous cases go to the LLM (conceptual) |
| `images/context-isolation.png` | Figure 4. The flights, hotels and weather spokes read 120,000 tokens; the hub receives 4,500 in summaries (illustrative, based on Anthropic's 1,000 to 2,000 token range) |
| `images/parallel-vs-sequential.png` | Figure 5. A trip-planning job takes 95 seconds in sequence and 50 seconds with independent jobs in parallel (illustrative) |
| `images/failure-ladder.png` | Figure 6. The failure ladder: retry, fall back, escalate to a human, plus validation and loop protection (conceptual) |
| `images/mast-failures.png` | Figure 7. The six most common failure modes in 1,642 annotated multi-agent runs, from the MAST study (measured) |
| `images/token-cost.png` | Figure 8. Token use vs a chat: single agent about 4×, multi-agent about 15× (measured by Anthropic, 2025) |
| `images/social-card.png` | 1200 × 630 preview image shown when the link is shared |

All visuals were built as HTML and rendered with Chrome. Each carries the Close Future green (`#619e2f`) frame.

## Contents

| File | What it is |
|---|---|
| `index.html` | Styled web version of the article, the entry point |
| `images/` | Seven figures, the animation (WebM, GIF, poster) and the social preview image |

Facts were checked on November 5, 2026, and the whole article was re-checked against every source in an editorial fact-check on November 6, 2026. The code sample was checked against `openai-agents` 0.24.0 without a live AI call. SDKs change often.

## Viewing it

Open `index.html` in a browser.
