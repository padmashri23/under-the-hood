# Tool design layer - Brain Needs Hand: The Art of Tool Design for AI Agents

**📖 Read it here: https://padmashri23.github.io/under-the-hood/tool-design-for-ai-agents/**

A beginner-friendly guide to the tools an AI agent uses to act in the world. The model is the brain and the tool is the hand: the model only asks, your code does the work. Every fact comes from a primary source; the made-up examples are labeled as illustrative.

## What it covers

1. **Introduction:** an agent as an LLM in a loop, tools as the layer to real data and systems, and a link back to the hub-and-spoke article
2. **What a tool is:** a function that fetches information or takes an action, and why the model never runs it itself
3. **Types of tools:** read, write, compute, agent-as-tool, and built-in vs custom tools
4. **Anatomy of a tool definition:** name, description (including when not to use it), JSON Schema inputs and parameter descriptions
5. **The tool-calling flow:** five steps, a flow diagram, and a full round trip in code explained part by part
6. **Designing tool outputs:** lean results, pagination and truncation, consistent formats and useful IDs
7. **Best practices:** the SWE-agent evidence, small and non-overlapping toolsets, task-sized tools, read/write split, idempotency, naming, and tool-count data
8. **Common mistakes:** nine mistakes with fixes, plus a poor vs good definition side by side
9. **Error handling** and **security and permissions:** readable errors (with a bad vs good error in code), validation, timeouts, logging, least privilege, credentials, approval and prompt injection
10. **Worked example:** a CRM lookup spoke with one read tool and one write tool behind human approval
11. **Testing and checklist:** how to test tools on real tasks, and a 12-point tool design checklist

Written for beginners: a short-version box, a glossary, every technical term explained, and about 10 words per sentence on average. Every section follows the same shape: an "In plain words" opener, bullets, then a "Good to know" or "Try this" note. One running example (Ana's CRM lead) ties the figures, code and worked example together. About 3,004 words above Sources & References (3,061 including the title block), counting headings, captions, tables and both code examples. No video.

## Visuals

| Visual | What it shows |
|---|---|
| `images/brain-and-hand.png` | Figure 1. The tool-calling flow: the model asks, your code acts (conceptual) |
| `images/concise-vs-detailed.png` | Figure 2. Detailed vs concise Slack tool response, 206 vs 72 tokens (Anthropic example) |
| `images/same-model-different-tools.png` | Figure 3. SWE-agent on SWE-bench Lite with GPT-4 Turbo under six toolsets, Yang et al. 2024 (measured) |
| `images/tool-definition-tokens.png` | Figure 4. Tokens used by tool definitions across five MCP servers, about 55K for 58 tools (Anthropic example) |
| `images/tool-search.png` | Figure 5. Accuracy and context use with and without Tool Search (Anthropic internal testing) |
| `images/tool-anatomy.png` | Figure 6. A poor and a good tool definition side by side (illustrative) |
| `images/crm-spoke.png` | Figure 7. Worked example: a CRM spoke with a read tool and a write tool behind approval (illustrative) |
| `images/social-card.png` | 1200 × 630 preview image shown when the link is shared |

All visuals were built as HTML and rendered with Chrome. Each carries the Close Future green (`#619e2f`) frame.

## Contents

| File | What it is |
|---|---|
| `index.html` | Styled web version of the article, the entry point |
| `images/` | Seven figures and the social preview image |

Facts were checked on November 7, 2026. Tool APIs and model results change often.

## Viewing it

Open `index.html` in a browser.
