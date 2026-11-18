# Guardrails for Multi-Agent Systems: How to Keep Agents Safe, Scoped and Under Control in Production

**📖 Read it here: https://padmashri23.github.io/under-the-hood/multi-agent-guardrails-production/**

A beginner-friendly guide to the guardrails a multi-agent AI system needs before it goes to production. In a team of agents, one agent's mistake becomes the next agent's input, so guardrails have to be designed into every layer, not bolted on at the end. Every fact comes from a primary source (Anthropic, OpenAI, Meta, OWASP, the MCP specification, the original research papers and the legal texts); modeled data and made-up examples are labeled as such.

## What it covers

1. **Why guardrails are different in multi-agent systems:** the running example (a made-up support team of triage, research and refund agents), compounding errors, a bigger attack surface, OWASP ASI07 and ASI08
2. **Input guardrails:** direct and indirect prompt injection, validation, declining early, masking PII, and why front-door checks only cover the first agent
3. **Agent scope and trust:** written roles, enforcing scope through tools, Prompt Infection between agents, and Meta's Agents Rule of Two
4. **Permissions and tool access:** read, write and irreversible tiers, one key per agent, sandboxing, vetting and pinning MCP servers (the postmark-mcp case)
5. **Action control:** caps, loop limits, kill switches, argument checks and dry runs, with UC Berkeley's MAST failure data
6. **Human-in-the-loop:** approval by risk, three approval patterns, and approval fatigue (Anthropic's 84% fewer prompts)
7. **Output guardrails:** content, schema and grounding checks, and the limits of a reviewer agent
8. **Data and privacy controls:** data minimisation, clean logs and memory, memory poisoning (ASI06), GDPR transfers and India's DPDP Rules
9. **Audit trail:** what to log, one trace ID per request, EU AI Act Article 12
10. **A practical guardrails checklist** as a one-page image, and a conclusion that follows one attack through every layer

Written for beginners and tech starters: a key points box, one example business followed through every section, a short glossary, every technical term explained where it first appears (orchestrator, attack surface, classifier, schema, API key, sandbox, MCP server, pinning, kill switch, trace ID), an everyday comparison in every section (a relay race, airport security, a hotel keycard, a company card with a spending limit, a manager signing off expenses, an editor, receipts and a security camera), and the same shape in each section: "In plain words", bullets, then a "Good to know" note. About 8.5 words per sentence on average (Flesch reading ease about 74). Links to the 7 risks, prompt injection, multi-agent architecture and memory articles where they go deeper. 1,800 words above Sources & References, counting headings, captions and tables. No video.

## Visuals

| Visual | What it shows |
|---|---|
| `images/errors-multiply.png` | Figure 1. Chance a run is error-free over 1 to 10 steps at 99%, 95% and 90% per step (illustrative model) |
| `images/guardrail-layers.png` | Figure 2. The six guardrail checkpoints in one request, with the audit trail underneath (conceptual) |
| `images/rule-of-two.png` | Figure 3. Meta's Agents Rule of Two with the example support team mapped onto it (made-up mapping) |
| `images/permission-tiers.png` | Figure 4. Read, write and irreversible permission tiers for the example support team (conceptual, made-up example) |
| `images/mast-failures.png` | Figure 5. Five system design failure modes from 1,642 multi-agent runs (research data, Cemri et al. 2025; failures labelled by an AI model checked against human experts) |
| `images/approval-matrix.png` | Figure 6. Which actions need human approval, by impact and reversibility (conceptual framework) |
| `images/checklist.png` | Figure 7. The one-page guardrails checklist with tick boxes (editorial) |
| `images/one-attack.png` | Figure 8. One poisoned attachment against every guardrail layer (made-up scenario) |
| `images/social-card.png` | 1200 × 630 preview image shown when the link is shared |

All visuals were built as HTML and rendered with Chrome. Each carries the Close Future green (`#619e2f`) frame.

## Contents

| File | What it is |
|---|---|
| `index.html` | Styled web version of the article, the entry point |
| `images/` | Eight figures and the social preview image |

Facts were checked on November 18, 2026. Agent SDKs, the MCP spec and data protection rules change often.

## Viewing it

Open `index.html` in a browser.
