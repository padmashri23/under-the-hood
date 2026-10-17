# Under the Hood

Long-form, fact-checked articles on AI: how the technology works, what it costs, and how the products compare. Each article lives in its own folder with everything it needs to render.

## Articles

| Article | Folder | What it covers |
|---|---|---|
| The Hidden Infrastructure Behind Every AI Answer: GPUs, Inference, and Compute Costs | [`the-hidden-infrastructure-behind-every-ai-answer/`](the-hidden-infrastructure-behind-every-ai-answer/) | What happens between hitting "Send" and seeing an answer: tokenization, GPUs, data centers, energy, cooling and the money behind it |
| Grok Bot vs Instinct vs Dots vs Hermes Bot: The AI Agent Showdown of 2026 | [`grokbot-vs-instinct-vs-dots-vs-hermesbot/`](grokbot-vs-instinct-vs-dots-vs-hermesbot/) | A side-by-side comparison of four AI agent platforms: what each can do, how it works, pricing, security and who it suits |

## Folder structure

```
under-the-hood/
├── README.md                     <- this file, the index of all articles
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
5. Add a row to the **Articles** table above.
6. Commit and push:

   ```bash
   git add <article-slug>/ README.md
   git commit -m "Add <article title>"
   git push
   ```

## Viewing an article locally

Open the article's `index.html` in a browser, or serve the folder so relative paths and embeds behave as they would online:

```bash
cd <article-slug>
python -m http.server 8000
# then open http://127.0.0.1:8000/
```
