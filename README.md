# Kingdom Chronicles 🎮

**Explore the World. Discover the Word.**

Kingdom Chronicles is a browser-first, bilingual (Sinhala / English), cinematic 2D/2.5D Bible adventure game for Christian teenagers and beginner-to-intermediate learners. Players explore environments, interact with scripted characters, solve puzzles, and discover Scripture through gameplay.

## Non-negotiable product direction
- **A real adventure game, not an LMS or quiz website.**
- Scriptural events and outcomes are not changed by player choices.
- Biblical quotations, paraphrases, historical background, interpretation, and fictional gameplay dialogue must be clearly distinguished.
- Target Bible editions: **SROV** and **NKJV**, subject to permission for digital reproduction. Do not commit Bible text without authorization.
- No paid AI APIs or other paid subscriptions are required for the MVP.

## Technology (initial plan)
- Next.js + TypeScript + Tailwind CSS for app shell
- Phaser for the actual playable game
- LDtk for map authoring, procedurally generated / approved original game art
- Supabase free tier for auth and saved progress (introduced after offline prototype)
- Static export to Cloudflare Pages
- Vitest + Playwright for testing

## Development workflow
- **Cursor Pro:** primary implementation.
- **ChatGPT Plus:** gameplay/visual design, artwork concepts, story research, editorial review.
- **Codex within ChatGPT Plus:** selected code review and debugging.
- GitHub tracks issues, pull requests, and source code.

Start with [AGENTS.md](AGENTS.md) and [docs/MVP.md](docs/MVP.md). Other design documents are in `docs/`.

## First playable milestone
An animated ancient Israelite village with a controllable explorer, collision/camera, one interactable NPC, a scripted conversation, a mission trigger, and mobile controls. **Implement and test this vertical slice before adding more Bible stories.**

## Local development
The repository begins with planning and agent rules only. Use the implementation plan in `docs/MVP.md` to generate the application. Do not claim this README implies the app is already running.

## License and rights
Code license not selected. Do not copy copyrighted Bible text, music, art, or third-party software into this repository without permission and license review.
