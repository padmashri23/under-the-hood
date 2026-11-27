# Red-Teaming Your AI Before Your Customers Do: A Playbook for Structured Adversarial Testing of Deployed

**📖 Read it here: https://padmashri23.github.io/under-the-hood/red-teaming-your-ai-before-your-customers-do/**

A beginner-friendly, fact-checked playbook for red-teaming a customer-facing AI system before the public does it for you. Facts come from primary sources: NIST, Microsoft's AI Red Team paper and blog, the OWASP GenAI Security Project, the EU AI Act and the European Commission, Anthropic, and the garak, PyRIT and promptfoo project pages. The four chatbot incidents come from VentureBeat, TIME, The Markup and two law firms' summaries of the Air Canada decision.

## What it covers

1. **Your customers are already testing it:** Chevrolet of Watsonville, DPD, Air Canada and New York City's MyCity chatbot
2. **What red teaming actually means:** NIST's definition, a table comparing normal testing, penetration testing and red teaming, why it isn't a benchmark, and the EU AI Act's adversarial-testing duty for the biggest model makers
3. **What to test:** the OWASP Top 10 for LLM Applications 2026, and the five risks to try first on a customer chatbot
4. **The playbook:** scope, threat model, attack library (with a ten-row starter table of test messages, one per OWASP risk), run the tests, score and fix, retest, with Microsoft's lessons along the way
5. **Free tools:** garak, PyRIT and promptfoo compared
6. **Guardrails help, but don't get to zero:** Anthropic's 86% to 4.4% jailbreak result, its costs, and three rounds of human red teaming
7. **Where to start this month:** six ordered steps and a printable checklist

Written for beginners and tech starters: a key points box, a seven-term glossary, everyday comparisons (a shop owner testing for shoplifters, a recipe book, hospital triage, a lock, alarm and dog, a monthly smoke-alarm test), and the same pattern in every section ("In plain words", short bullets, then an example or a "Good to know" note). Every technical term is explained where it first appears. About 10 words per sentence on average. 2,000 words above Sources & References, counting headings, captions and tables. No video, as requested.

## Visuals

| Visual | What it shows |
|---|---|
| `images/incidents.png` | Figure 1. Timeline of four live chatbots whose flaws the public found first (2023 to 2024) |
| `images/owasp-2026.png` | Figure 2. The OWASP Top 10 for LLM Applications 2026, with plain-words summaries |
| `images/playbook-loop.png` | Figure 3. The six-step red-teaming loop (conceptual) |
| `images/severity-grid.png` | Figure 4. A likelihood vs. harm grid for ranking findings (illustrative, made-up findings) |
| `images/guardrail-effect.png` | Figure 5. Anthropic's jailbreak success rate, 86% without and 4.4% with guard classifiers, plus the costs |
| `images/human-rounds.png` | Figure 6. Three rounds of human red teaming against Anthropic's defences: hours spent and universal jailbreaks found |
| `images/checklist.png` | Figure 7. A one-page red-teaming checklist to print (editorial) |
| `images/social-card.png` | 1200 × 630 preview image shown when the link is shared |

All visuals were built as HTML and rendered with Chrome. Each carries the Close Future green (`#619e2f`) frame.

## Contents

| File | What it is |
|---|---|
| `index.html` | Styled web version of the article, the entry point |
| `images/` | Seven figures and the social preview image |

Facts were checked on November 27, 2026. The Air Canada tribunal's own site blocks automated reading, so its details come from two law firms' published summaries. Some source sites (VentureBeat, Microsoft's blog, Osler, the European Commission) refuse or time out for automated link checkers, but each page was read successfully during research.

## Viewing it

Open `index.html` in a browser.
