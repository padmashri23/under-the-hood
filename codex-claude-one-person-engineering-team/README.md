# 7 Codex & Claude Tricks That Turn You Into a One-Person Engineering Team

**📖 Read it here: https://padmashri23.github.io/under-the-hood/codex-claude-one-person-engineering-team/**

Seven practical, documented techniques for OpenAI Codex and Anthropic's Claude Code that help one developer cover the roles of a small team: tech lead, developer, QA, reviewer and DevOps. Every feature and command comes from the official docs, and the article says plainly where the two tools differ instead of treating them as the same thing. It makes no speed or productivity claims.

## What it covers

- The problem with building alone, and what a coding agent is
- A key points box and an "In this article" list of section links
- Codex and Claude Code side by side: where each runs, which plans include it, when to reach for which, and a "Which one should I start with?" box
- Seven tricks, one at a time:
  1. Give the agent a notes file (`AGENTS.md`, `CLAUDE.md`, `@AGENTS.md` imports, `/init`)
  2. Ask for a plan before any code (plan mode, `/plan`, `Shift+Tab`), also the fastest way into an unfamiliar codebase
  3. Give the agent a test it can run (failing test first, debugging from a stack trace)
  4. Hand side jobs to subagents (Claude Code's Explore and `.claude/agents/`, Codex's `.codex/agents/`)
  5. Run several agents at the same time (`claude --worktree`, Codex worktrees, `claude --cloud`, Codex Cloud with best-of-N attempts)
  6. Automate chores with skills and hooks (`SKILL.md`, `$skill-creator`, `PostToolUse` and `PreToolUse` hooks, `codex exec` and `claude -p` for CI)
  7. Let one agent review the other (`/review`, `codex review`, `@codex review`, `/code-review`, `/security-review`, Claude Code Review for Team and Enterprise)
- Putting it together: a worked example of one day with two agents covering tech lead, developer, QA and reviewer
- Six more tips: rewind a bad edit with checkpoints (`Esc` twice, `/rewind`), keep CLAUDE.md under 200 lines, connect tools with MCP (`codex mcp add`, `claude mcp add`), start work from a Linear issue or an `@claude` GitHub mention, pull a cloud session home with `claude --teleport`, and run Codex chores as scheduled tasks
- Stay safe while agents work: Codex permission modes and Claude Code permission modes, and what to avoid
- Common beginner mistakes
- A cheat sheet: the main commands for both tools in one table, plus the three prompts to copy
- Where to start: four steps in order
- A short conclusion
- A link to the earlier Under the Hood article on AI agent guardrails

Figure 1 doubles as the at-a-glance command comparison. Written for beginners and tech starters: a key points box, a glossary of the basic terms (terminal, IDE, branch, pull request, tokens, CI), sentences averaging about 13 words, and every trick in the same pattern (the idea in plain words, then a Codex bullet and a Claude Code bullet, then a prompt to try or a "Good to know" note). Emoji section headings with subheadings so the outline shows up in Notion's table of contents. About 2,510 words above Sources & References, counting headings, captions, tables and about 90 words of copy-and-paste starter files (a notes file, a SKILL.md and a formatter hook).

## Visuals

Figures are static images and the one animation is a plain MP4, so the article copies cleanly into Notion. Media load from the live GitHub Pages URL first, with the local `images/` copy as a fallback for previewing before publishing.

| Visual | What it shows |
|---|---|
| `images/codex-vs-claude-code.png` | Figure 1. Comparison infographic: where each feature lives in Codex and in Claude Code, plus when to reach for each |
| `images/parallel-agents.mp4` | Figure 2. 15-second animation, 1920 × 1080 (216 KB): five jobs done alone one after another, then shared out to agents in worktrees and the cloud that run tests before a second agent reviews |
| `images/parallel-agents-poster.png` | Poster frame for the video |
| `images/parallel-agents.gif` | 960 × 540 GIF copy of the animation for Notion, where a pasted video may not come through. Linked from Figure 2's caption |
| `images/agent-workflow.png` | Figure 3. Workflow diagram: one developer plans, three jobs run side by side, checks run, the other agent reviews, the developer merges |
| `images/tricks-roles.png` | Figure 4. Matrix of the seven tricks against six engineering roles, with a task to try each on |
| `images/social-card.png` | 1200 × 630 preview image shown when the link is shared |

Each figure opens full size when tapped. The three figures, the video and its poster are all 1920 × 1080 (16:9), laid out at 1280 × 720 and rendered at 1.5× so text stays sharp; the social card stays at the standard 1200 × 630. All visuals were built as HTML and rendered with Chrome (the video encoded to H.264 MP4 with ffmpeg). None of them contains invented numbers: Figures 2 and 3 are labeled illustrative workflows, and Figure 4 is labeled an editorial mapping. Every image and the video carry a thin Close Future green (`#619e2f`) frame drawn into the file itself.

## Contents

| File | What it is |
|---|---|
| `index.html` | Styled web version of the article, the entry point |
| `images/` | Three figures, the animation (MP4, GIF copy and poster), and the social preview image |

Every feature, command and quote was checked on October 30, 2026 against OpenAI's Codex docs (now at learn.chatgpt.com; developers.openai.com redirects there) and Anthropic's Claude Code docs at code.claude.com. The full list is at the end of the article.

## Viewing it

Open `index.html` in a browser.
