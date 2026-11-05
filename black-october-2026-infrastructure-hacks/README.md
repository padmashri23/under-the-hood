# Black October 2026: Worst Infrastructure Hacks Analyzed

**📖 Read it here: https://padmashri23.github.io/under-the-hood/black-october-2026-infrastructure-hacks/**

A beginner-friendly breakdown of twelve security incidents from October 2026: what happened, how the attackers got in, what was hit, and what to do if it affects you. Each incident is checked against the company's own statement, a vendor advisory or a government notice. Claims made only by attackers or a single outlet are labeled as such.

## What it covers

In date order:

1. **GitLab (Oct 12 and 21):** two 10.0-severity flaws, CVE-2026-97229 (on CISA's exploited list) and CVE-2026-110264, with fixed versions
2. **Palo Alto PAN-OS (Oct 14):** CVE-2026-0322 firewall zero-day (short entry)
3. **Zeabur (Oct 14 to 15):** leaked admin tokens and AWS keys, never rotated, opened its systems; the company is shutting down
4. **OpenCode Console (Oct 16 to 17):** saved AI provider keys of 1.4% of Console users may be exposed
5. **eMudhra (Oct 17):** eight certificate keys could be guessed; browsers blocked them (short entry)
6. **GMO Onamae.com Desktop Cloud (Oct 20):** malicious program, customer data taken, ransom refused
7. **Railway (Oct 20 to 22):** customers' stored secrets decrypted
8. **LiteLLM 1.107.0 (Oct 21):** poisoned release with a credential stealer
9. **PHP2Shell (Oct 21):** two PHP flaws exploited by Oct 26, with fixed versions and the status of older branches
10. **Node.js "Node2Shell" (Oct 21):** a Brotli decompression bug exploited by Oct 27, with fixed versions (short entry)
11. **State Bank of India (Oct 21):** 3,897 customer records on the dark web, plus fraud advice (1930, cybercrime.gov.in)
12. **Binance (Oct 29 to 30):** about $6.3 billion withdrawn after a DevOps laptop was compromised

Every full entry follows the same three parts: what happened, how they got in, and what to do. Plus a "Does this affect you?" checklist, a glossary and a short conclusion with the main lessons. About 1,793 words above Sources & References (1,834 including the title block), counting headings, captions and tables.

## Visuals

| Visual | What it shows |
|---|---|
| `images/october-timeline.png` | Figure 1. The twelve incidents in date order |
| `images/one-key-cascade.mp4` | Figure 2. 15-second animation: Zeabur's 1,008-day-old token and everything it reached |
| `images/one-key-cascade.gif` | GIF copy of Figure 2 for Notion, linked from its caption |
| `images/one-key-cascade-poster.png` | Poster frame for the video |
| `images/litellm-window.png` | Figure 3. How long the poisoned LiteLLM release was downloadable (UTC) |
| `images/patch-now.png` | Figure 4. Fixed versions for GitLab, PHP2Shell, PAN-OS and Node2Shell |
| `images/binance-path.png` | Figure 5. The path of the Binance theft as Binance has described it, with TRM Labs' figures |
| `images/social-card.png` | 1200 × 630 preview image shown when the link is shared |

All visuals were built as HTML and rendered with Chrome at 1920 × 1080 (the video encoded to H.264 MP4). Every number comes from a primary source; none is modeled. Each carries the Close Future green (`#619e2f`) frame.

## Contents

| File | What it is |
|---|---|
| `index.html` | Styled web version of the article, the entry point |
| `images/` | Four figures, the animation (MP4, GIF copy and poster), and the social preview image |

Facts were checked on November 2, 3 and 5, 2026. Several investigations are still open (Binance has promised a post-mortem), so figures may change.

## Viewing it

Open `index.html` in a browser.
