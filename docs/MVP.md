# MVP and Implementation Sequence

## Goal
Build a **real browser game**, not an LMS UI. First milestone is an ancient Israelite village exploration scene with a playable explorer and scripted NPC interaction. No API keys, no paid AI services, no Bible text licensing assumptions.

## Phase A — Foundation
1. Scaffold Next.js + TS + Tailwind app with strict lint/typecheck/build scripts.
2. Embed Phaser via client-only dynamic loading and implement resize handling.
3. Establish `GameScene`, `WorldScene`, `PlayerController`, and separation between game code and React app UI.
4. Provide an entry screen with **Play Adventure** leading directly to the Phaser scene.
5. Use procedural/original placeholder graphics until approved art exists.
6. Add Vitest, Playwright, GitHub Actions.

**Acceptance:** application boots and a browser displays a responsive working canvas with scene navigation; tests and build pass.

## Phase B — Explorer Movement
1. Add arrow/WASD movement with normalized diagonals.
2. Add touch joystick or on-screen direction control for phones.
3. Add top-down collision geometry for environment props/buildings.
4. Add camera tracking with world bounds, smooth follow, and responsive scaling.
5. Add animated terrain details: moving foliage, dust, or water.

**Acceptance:** player walks across map but not through solid objects, controls work on touch and keyboard, and frame rate remains acceptable.

## Phase C — NPC, Mission, Journal
1. Add a single approachable NPC with interaction indicator.
2. Create accessible dialogue overlay: keyboard/touch advances and close behavior.
3. Introduce mission objective: *Talk to the village messenger*.
4. After dialogue, mark objective complete and unlock *A challenge in the valley*.
5. Unlock the first Living Journal entry with reference **1 Samuel 17**; do not paste licensed translation text.
6. Persist mission progress locally and recover after refresh.
7. Include Sinhala/English UI dictionaries, not machine-translated quotations.

**Acceptance:** player can reach NPC, converse, trigger mission objective, open journal, and reload without losing progress; E2E test verifies the sequence.

## Phase D — Vertical Slice: David and Goliath (1 Samuel 17)
1. Research and human-review narrative facts/character links.
2. Add valley and camp environments and several NPCs.
3. Build inventory/puzzle prototypes: information clues, five smooth stones.
4. Add a scripted cinematic outcome faithful to 1 Samuel 17.
5. Add story reconstruction challenge and evidence references.
6. Add complete journal story record and autosave.

**Acceptance:** 10–15 minute continuous adventure with a beginning, middle and end; gameplay is demonstrably interactive rather than a slideshow.

## Explicitly Out of Scope for MVP
Multiplayer, open chat, AI chatbot NPCs, paid API integrations, full 66-book content import, unlicensed Bible text, ads, monetization, subscriptions.

## Agent task delivery format
For each task report: objective, changed files, implementation decisions, tests run + outcomes, manual verification, screenshots if possible, outstanding issues, next task.
