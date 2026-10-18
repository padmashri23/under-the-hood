# Large Language Models vs Small Language Models: Which Is Better for Production Applications?

**📖 Read it here: https://padmashri23.github.io/under-the-hood/llm-vs-slm-production/**

Your prototype works on a frontier model, then you do the math on production costs and it doesn't add up. This article is a practical guide for engineering teams choosing between large and small language models (or a mix of both) for real production workloads.

## What it covers

- What "large" and "small" actually mean, and why parameter count is a poor dividing line
- The engineering trade-offs: latency and throughput, hardware and memory, accuracy and hallucinations, context windows
- Use cases where each approach works best
- Making models smaller and cheaper: quantization, distillation, fine-tuning, speculative decoding, effort settings
- Hybrid routing, and why it is becoming the default architecture
- Cost beyond token pricing: an API pricing snapshot, self-hosting economics and total cost of ownership
- Open weights vs open source, and privacy, compliance and data residency
- Evaluation and monitoring after deployment
- A worked cost example for 50,000 users, and a decision framework
- Fact-checked against primary sources, with the full list at the end of the article

## Contents

| File | What it is |
|---|---|
| `index.html` | Styled web version of the article, the entry point |
| `llm-vs-slm-production.md` | Earlier Markdown draft of the article (not yet updated to match the web version) |
| `images/model-selection-framework.png` | Decision framework for choosing a small model, a large model or hybrid routing |
| `images/hybrid-routing-savings.png` | Stat cards: monthly cost with and without hybrid routing |
| `images/self-hosting-break-even.png` | Stat cards: self-hosting cost floor and break-even volumes |
| `images/cost-chart-2560.png` | Monthly cost by deployment strategy (web size) |
| `images/cost-chart-8k.png` | The same chart at 8K (7680×4320), opened by clicking the chart |

Pricing and model details were researched as of October 2026. Prices change often, so check primary sources for current figures.

## Viewing it

Open `index.html` in a browser.
