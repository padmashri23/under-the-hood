# Under the Hood

**📖 Read them here: https://padmashri23.github.io/under-the-hood/**

Long-form, fact-checked articles on AI: how the technology works, what it costs, and how the products compare. Each article lives in its own folder with everything it needs to render.

## Articles

| Article | Read it | Folder | What it covers |
|---|---|---|---|
| The Hidden Infrastructure Behind Every AI Answer: GPUs, Inference, and Compute Costs | [Live](https://padmashri23.github.io/under-the-hood/the-hidden-infrastructure-behind-every-ai-answer/) | [`the-hidden-infrastructure-behind-every-ai-answer/`](the-hidden-infrastructure-behind-every-ai-answer/) | What happens between hitting "Send" and seeing an answer: tokenization, GPUs, data centers, energy, cooling and the money behind it |
| Grok Bot vs Instinct vs Dots vs Hermes Bot: The AI Agent Showdown of 2026 | [Live](https://padmashri23.github.io/under-the-hood/grokbot-vs-instinct-vs-dots-vs-hermesbot/) | [`grokbot-vs-instinct-vs-dots-vs-hermesbot/`](grokbot-vs-instinct-vs-dots-vs-hermesbot/) | A side-by-side comparison of four AI agent platforms: what each can do, how it works, pricing, security and who it suits |
| Large Language Models vs Small Language Models: Which Is Better for Production Applications? | [Live](https://padmashri23.github.io/under-the-hood/llm-vs-slm-production/) | [`llm-vs-slm-production/`](llm-vs-slm-production/) | A practical guide to choosing between LLMs, SLMs or hybrid routing in production: latency, hardware, accuracy, cost and evaluation |
| Open Weights vs Open Source AI: The Technical and Licensing Differences That Matter | [Live](https://padmashri23.github.io/under-the-hood/open-weights-vs-open-source-ai/) | [`open-weights-vs-open-source-ai/`](open-weights-vs-open-source-ai/) | What open weights and open source AI actually mean, the OSI definition, how model licenses differ, and how to choose a model you can legally ship |

## Folder structure

```
under-the-hood/
├── README.md                     <- this file, the index of all articles
├── index.html                    <- the site's home page, links to every article
├── .nojekyll                     <- tells GitHub Pages to serve files as-is
└── <article-slug>/
    ├── README.md                 <- summary, contents and how to view
    ├── index.html                <- the styled web version (entry point)
    ├── <article-slug>.md         <- Markdown source, if there is one
    └── images/                   <- images used by the article, if any
```

## Adding a new article

1. Create a folder named after the article in lowercase kebab-case, for example `why-ai-models-hallucinate/`.
2. Put the web version in it as `index.html`. Keep images in an `images/` subfolder and reference them with relative paths (`images/foo.jpg`), so the folder works on its own.
3. Add the Markdown source next to it if you have one.
4. Add a `README.md` inside the folder (copy one of the existing ones as a template).
5. Add a row to the **Articles** table above, with its live link: `https://padmashri23.github.io/under-the-hood/<article-slug>/`.
6. Add a card for it to the root `index.html` (copy an existing `<a class="card">` block).
7. Commit and push:

   ```bash
   git add <article-slug>/ README.md index.html
   git commit -m "Add <article title>"
   git push
   ```

   GitHub Pages redeploys automatically, usually within a minute or two.

## Viewing an article locally

Open the article's `index.html` in a browser, or serve the folder so relative paths and embeds behave as they would online:

```bash
cd <article-slug>
python -m http.server 8000
# then open http://127.0.0.1:8000/
```
