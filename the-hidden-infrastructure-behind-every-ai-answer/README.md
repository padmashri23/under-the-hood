# The Hidden Infrastructure Behind Every AI Answer: GPUs, Inference, and Compute Costs

What actually happens between the moment you hit "Send" and the moment an AI's answer appears on your screen? This article follows a single prompt from your keyboard to a GPU cluster and back, and looks at the hardware, energy and money it takes to answer it.

## What it covers

- The journey of a prompt: the HTTPS request, the data center, tokenization and embeddings
- How transformers and self-attention work, and why text streams one token at a time
- Why GPUs run AI: NVIDIA Hopper (H100), Blackwell and Vera Rubin, memory bandwidth and HBM
- The cost per query: energy per prompt, reasoning models, API pricing, prompt caching and batching
- Hyperscaler capital expenditure in 2026 (Amazon, Alphabet, Microsoft, Meta)
- Data center power demand (IEA projections to 2035), liquid cooling and PUE
- A numbered source list (17 references) at the end

## Contents

| File | What it is |
|---|---|
| `index.html` | Styled web version of the article, the entry point |
| `the-hidden-infrastructure-behind-every-ai-answer.md` | Markdown source of the article |
| `images/prompt-journey.jpg` | The path a prompt takes from your device to a GPU cluster |
| `images/token-generation.jpg` | How autoregressive generation produces one token at a time |
| `images/gpu-architecture.jpg` | Stylized cross-section of a modern AI GPU |
| `images/tech-capex-chart.jpg` | Estimated 2026 capex of the four largest hyperscalers |
| `images/energy-projection.jpg` | Projected global data center electricity use, 2024 to 2035 |
| `images/liquid-cooling-datacenter.jpg` | Inside a liquid-cooled AI data center |

The illustrations were created for this article. The charts use data from company earnings guidance, analyst estimates and the IEA's *Energy and AI* (2025) report, as credited in their captions.

## Viewing it

Open `index.html` in a browser. Images load from the `images/` folder next to it, so keep the folder together if you move it.
