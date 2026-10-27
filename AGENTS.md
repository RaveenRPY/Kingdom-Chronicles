# AI Agent Operating Instructions

This file applies to Cursor, Codex, and any other coding agent working on Kingdom Chronicles.

## Role and mission
You are implementing a browser-based **game** using Next.js and Phaser. Users are Christian teenagers and beginner/intermediate Bible learners. A successful result is **playable, visually cohesive, biblically responsible, accessible, bilingual adventure gameplay**. Do not replace the game with course cards, quizzes, dashboards, or static mockups.

## Operating constraints
1. The user pays only for **Cursor** and **ChatGPT Plus**. Prefer free/open-source libraries, free hosting, and assets with verified licenses. **Never require another paid API, SaaS subscription, or token purchase.**
2. Don't put model API calls in the live gameplay runtime for the MVP.
3. Do not assume browser access or image assets that aren't actually available. Use temporary original shapes, procedurally generated tiles, and placeholder art when necessary.
4. Do not download, copy, or store NKJV or SROV text until appropriate rights are confirmed. Use verse references and authored summaries instead.
5. Do not invent biblical events as factual history. Distinguish source quotation, paraphrase, interpretive commentary, historical context, and invented navigational dialogue.
6. Keep player choices from changing recorded outcomes.
7. Write small, testable commits. Do not implement all 66 books at once.
8. Do not alter deployed cloud resources or spend money without human approval.
9. Never put tokens, personal data, or secrets in the repository.
10. Because the GitHub repository is public, assume all committed content is visible to everyone.

## Source of truth
- `docs/PRODUCT_VISION.md`
- `docs/ARCHITECTURE.md`
- `docs/MVP.md`
- `docs/BIBLE_CONTENT_POLICY.md`
- `docs/GAME_DESIGN.md`

If specifications conflict, raise the issue in your implementation notes instead of silently changing direction.

## Agent role convention
Use focused role hats on independent tasks: project lead, game designer, Phaser engineer, UI engineer, Bible content reviewer, artist/asset pipeline engineer, QA engineer, and DevOps engineer. These are **instructions**, not separately paid agents. Prefer one Cursor agent at a time; use separate branches/worktrees for parallel work when available.

## Workflow for every task
1. Read this file and the relevant docs.
2. Create a short plan with acceptance criteria.
3. Implement the smallest complete behavior.
4. Run lint, typecheck, tests, and applicable browser interaction tests.
5. Capture a screenshot or describe why visual verification was not possible.
6. Report what is genuinely working, what is mocked, and any known limitations.

## Definition of done
- Working, navigable scene demonstrated in browser (not just screenshots)
- No TypeScript or build errors
- Core keyboard and touch interactions tested
- No secrets or unauthorized assets
- No broken mission progression
- Content source references included and review status respected
- Documentation updated for architectural changes

## First task
Follow `docs/MVP.md`: implement the foundation and **one explorable village with an NPC**. Do not begin multiplayer, live AI NPCs, a full Bible text reader, or a giant world map.
