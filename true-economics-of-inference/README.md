# The True Economics of Inference: FinOps Strategies for Cutting Token Costs by 60% in Production

**📖 Read it here: https://padmashri23.github.io/under-the-hood/true-economics-of-inference/**

Where an AI bill actually comes from, why token spend grows so fast in production, and the FinOps habits that bring it back down. The article tests the "60%" in its title with a transparent worked example instead of promising it. It's written for beginners as well as engineering teams.

## What it covers

- Why AI bills surprise teams
- How inference costs work: tokens, input vs output pricing, a short glossary, and what one request really costs
- Why costs grow in production: scale, chats that re-send their history, hidden thinking tokens, and agents that call the model again and again
- What FinOps means for AI, and why cost per successful task beats cost per request
- Six ways to cut token costs (caching, less context, shorter answers, model routing, batching, plus semantic caching and quantization), with an at-a-glance comparison table
- Whether 60% is realistic: a worked example reaching a modeled 62% saving, the 50% and 36% cases, and why the math is the same on OpenAI's matching models
- Where to start: four steps in order
- Links to two earlier Under the Hood articles (LLM vs SLM, and the hidden infrastructure behind AI answers)

Written for beginners: short sentences, technical terms explained where they first appear, and emoji section headings with subheadings so the outline shows up in Notion's table of contents. About 1,450 words above Sources & References, counting headings, captions and tables (just under 1,500 including the title block).

## Visuals

The figures are static images, and the one animation is a plain looping video, so the article copies cleanly into Notion or a doc. Media load from the live GitHub Pages URL (so they survive a paste into Notion), with the local `images/` copy as a fallback for previewing before publishing.

| Visual | What it shows |
|---|---|
| `images/request-anatomy.png` | One illustrative request split by tokens and by cost: output is 8% of tokens but 29% of the cost |
| `images/context-growth.webm` | 14-second animation: a 10-turn chat re-sends its history each turn (8,000 tokens of chat, 54,000 billed), then prompt caching cuts the chat's cost from $0.143 to $0.059 |
| `images/context-growth-poster.png` | Poster frame for the video |
| `images/context-growth.gif` | 960 px GIF copy of the animation for Notion, where a pasted video may not come through. Drag it into the page or paste its live URL |
| `images/savings-waterfall.png` | Modeled monthly cost after each technique, $17,000 down to $6,424, with a sensitivity panel |
| `images/volume-spend.png` | Modeled monthly spend vs request volume, baseline and optimized |
| `images/social-card.png` | 1200 × 630 preview image shown when the link is shared |

All charts and the animation were built as HTML and rendered with Chrome (the video encoded to VP9 WebM with ffmpeg), so every number on them comes from the same cost model as the text. They are illustrative models built on published prices, not measured production data, and each says so on the image. Every image and the video carry a thin Close Future green (`#619e2f`) frame drawn into the file itself, so it survives a paste into Notion.

## Contents

| File | What it is |
|---|---|
| `index.html` | Styled web version of the article, the entry point |
| `images/` | Three charts, the animation (WebM, GIF copy and poster), and the social preview image |

Prices were checked against Anthropic's and OpenAI's pricing pages on October 28, 2026. Technical claims were checked against provider documentation (Anthropic, OpenAI, Google, vLLM), Anthropic's agents guide, the FinOps Foundation, the RouteLLM post and the vCache paper, with the full list at the end of the article.

## Viewing it

Open `index.html` in a browser.
