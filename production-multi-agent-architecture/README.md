# The Architecture Behind Production-Ready Multi-Agent Systems

**📖 Read it here: https://padmashri23.github.io/under-the-hood/production-multi-agent-architecture/**

A beginner-friendly guide to how multi-agent systems are built when they have to work for real users, not just in a demo. One hub agent (the orchestrator) runs the job and calls helper agents (spokes) as tools. The article walks through the plumbing that keeps that setup reliable. Every quote and number comes from a primary source; the illustrative examples are labeled as such.

## What it covers

1. **The orchestration loop:** receive, plan, call a sub-agent, read the result, decide, finish. Sub-agents exposed as tools (OpenAI Agents SDK `as_tool`). Stop conditions: turn limits (`max_turns`), a task-complete signal and a token budget. Includes a working code sample and the loop as pseudocode
2. **Routing:** model-based routing from tool descriptions, rules or a classifier, and hybrid, with an at-a-glance table
3. **Context isolation and passing:** fresh context per sub-agent, context rot, the four-part brief, and condensed 1,000 to 2,000 token results
4. **Structured input/output contracts:** JSON schemas, OpenAI Structured Outputs and Anthropic strict tool use, and why the hub still validates
5. **State management:** the hub owns state, stateless spokes, LangGraph checkpointers and resuming after errors
6. **Parallel vs sequential execution:** independent jobs in parallel, dependent jobs in order, and aggregation at the hub
7. **Failure handling:** retry, fallback and human escalation, validation, delegation caps, and the MAST failure study
8. The token cost of multi-agent systems, a "Where to start" list, a glossary, and a short conclusion

Written for beginners: short sentences and every term defined. About 1,573 words above Sources & References (1,612 including the title block), counting headings, captions, tables and code.

## Visuals

| Visual | What it shows |
|---|---|
| `images/hub-and-spoke.png` | Figure 1. The hub, three spokes, the state store, and the request, brief and result arrows (conceptual) |
| `images/orchestration-loop.webm` | Figure 2. Animation of the hub's loop calling three spokes, with iteration, budget and task-complete stop conditions (illustrative). Also `orchestration-loop.gif` and `orchestration-loop-poster.png` for Notion |
| `images/context-isolation.png` | Figure 3. Three spokes read 120,000 tokens; the hub receives 4,500 in summaries (illustrative, based on Anthropic's 1,000 to 2,000 token range) |
| `images/parallel-vs-sequential.png` | Figure 4. A trip-planning job takes 95 seconds in sequence and 50 seconds with independent jobs in parallel (illustrative) |
| `images/mast-failures.png` | Figure 5. The six most common failure modes in 1,642 annotated multi-agent runs, from the MAST study (measured) |
| `images/token-cost.png` | Figure 6. Token use vs a chat: single agent about 4×, multi-agent about 15× (measured by Anthropic) |
| `images/social-card.png` | 1200 × 630 preview image shown when the link is shared |

All visuals were built as HTML and rendered with Chrome. Each carries the Close Future green (`#619e2f`) frame.

## Contents

| File | What it is |
|---|---|
| `index.html` | Styled web version of the article, the entry point |
| `images/` | Five figures, the animation (WebM, GIF, poster) and the social preview image |

Facts were checked on November 5, 2026. The code sample was tested against `openai-agents` 0.24.0. SDKs change often.

## Viewing it

Open `index.html` in a browser.
