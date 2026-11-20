# Observability for Multi-Agent Systems: How to Trace, Debug and Evaluate Every Agent in Production

**📖 Read it here: https://padmashri23.github.io/under-the-hood/multi-agent-observability-production/**

A beginner-friendly guide to watching a team of AI agents in production: what to trace, what to measure, how to evaluate before and after launch, and how to go from a customer complaint to the exact step that broke. Every fact comes from a primary source (Anthropic, OpenTelemetry, the W3C, the MCP project, OpenAI, the original LLM-as-judge paper, GDPR, and the Langfuse, Arize Phoenix and LangSmith docs and license files). Modeled data and made-up examples are labeled as such.

## What it covers

1. **Why observability is harder in multi-agent systems:** one request fans out across agents and tools, Anthropic's 4× and 15× token multipliers, and non-determinism
2. **Logging vs. monitoring vs. tracing vs. evaluation:** a definition of each, with tracing as the backbone
3. **Anatomy of a trace:** root span, nested spans, the five span kinds and what each span records
4. **Tracing agent decisions:** routing reasons, tool choices, loops and the context an agent actually had
5. **Tracing across agent boundaries:** W3C traceparent, parallel and queued work, MCP's params._meta (SEP-414), outside APIs, and a short OpenTelemetry Python example (tested against opentelemetry-sdk 1.45.2)
6. **Key metrics to monitor:** latency (p95), cost, reliability, quality (task completion, escalation) and guardrail events
7. **Offline evaluation:** test sets from real cases, code checks vs. LLM-as-judge vs. human review, Anthropic's content-farm example, and regression runs
8. **Online evaluation:** sampled live scoring, user feedback and quality drift
9. **Debugging with traces:** the missing-refund example, step by step, and turning failures into test cases
10. **Privacy and retention:** recording text only when needed, masking (with a before-and-after figure), retention periods and access
11. **Platforms:** OpenTelemetry, then Langfuse, Arize Phoenix and LangSmith compared on features, free options, starting prices and licenses, and how to choose
12. **Closing checklist:** five "where to start" steps and the one-page checklist image

Written for beginners and tech starters: a key points box, one made-up support team (the same one as the guardrails article) followed through every section, a short glossary, every technical term explained in plain words where it first appears (orchestrator, span, root span, latency, retrieval, context, context propagation, traceparent, queue, API, p95, escalation rate, test set, grader, LLM-as-judge, regression, drift, root cause, masking, retention, self-hosting), an everyday comparison in most sections (a shop receipt, a flight recorder, a parcel tracking number, a car dashboard, a driving test), and the same shape in each section ("In plain words", short bullets, then a "Good to know" note where useful). Figure text uses the same plain words as the article. About 9.4 words per sentence on average (Flesch reading ease about 71, counting the technical names). Links to the guardrails and evaluation articles where they go deeper. 1,800 words above Sources & References, counting headings, captions, tables and code. No video.

## Visuals

| Visual | What it shows |
|---|---|
| `images/token-multiplier.png` | Figure 1. Tokens per task vs. a chat: about 4× for an agent, about 15× for a multi-agent system (Anthropic data, June 2025) |
| `images/four-signals.png` | Figure 2. Logging, monitoring and evaluation tied together by tracing (conceptual, made-up values) |
| `images/trace-waterfall.png` | Figure 3. A 13-span trace of the missing-refund request, with the failed issue_refund span (illustrative, made-up data and prices) |
| `images/trace-propagation.png` | Figure 4. One trace ID through handoffs, a queue, an MCP server and an outside API (conceptual) |
| `images/quality-drift.png` | Figure 5. A weekly judge pass rate that drops after a model update while errors stay flat (illustrative, made-up data) |
| `images/failure-to-test.png` | Figure 6. The loop from test set to live scoring to a new test case (conceptual) |
| `images/masking.png` | Figure 7. One span's input before and after masking personal data (made-up example) |
| `images/checklist.png` | Figure 8. The pre-launch observability checklist, in plain words (editorial) |
| `images/social-card.png` | 1200 × 630 preview image shown when the link is shared |

All visuals were built as HTML and rendered with Chrome. Each carries the Close Future green (`#619e2f`) frame.

## Contents

| File | What it is |
|---|---|
| `index.html` | Styled web version of the article, the entry point |
| `images/` | Eight figures and the social preview image |

Facts and prices were checked on November 20, 2026. The OpenTelemetry GenAI conventions are still in Development, and platform plans and prices change often. Arize's pricing page could not be read, so no Arize AX price is given.

## Viewing it

Open `index.html` in a browser.
