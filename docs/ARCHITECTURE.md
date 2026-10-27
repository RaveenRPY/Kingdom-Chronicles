# Technical Architecture (v0.1)

## Constraint
No additional paid subscriptions beyond existing Cursor Pro and ChatGPT Plus. No paid LLM/voice/image API runtime dependencies.

## MVP stack
- Next.js App Router, TypeScript, Tailwind CSS
- Phaser loaded **client-side only** (never SSR import Phaser at the server boundary)
- Game loop and scene state inside Phaser; React for menus and settings
- Data-driven authored JSON/TypeScript scene and mission definitions validated with Zod
- Browser localStorage initially for preferences and checkpoint progress
- Supabase Free (auth, Postgres with RLS, storage) **only after offline vertical slice works**
- Deploy Next.js static export through Cloudflare Pages where features permit
- LDtk JSON maps (or procedural tilemaps for initial scene)
- Vitest for pure mission logic; Playwright for E2E browser gameplay
- Free asset tools such as Krita, GIMP, and Audacity, if needed

## Components
```
apps/web Next.js UI
  -> game Phaser client
      -> SceneManager
      -> CharacterController
      -> InteractionSystem
      -> DialogueSystem
      -> MissionEngine
      -> CinematicTimeline
      -> Journal/Discoveries
  -> local persistence adapter
  -> future Supabase persistence adapter

packages/content (story JSON, localization, reference metadata)
packages/shared (schemas, types)
assets (approved optimized art / sound)
```

## Architectural contracts
- UI is separate from the rendered game engine.
- `SceneDefinition`: map references, collision data, triggers, NPC placements, audio, optional cutscene scripts.
- `MissionDefinition`: objectives, prerequisite IDs, state transitions, scriptural references, completion conditions.
- `DialogueNode`: speaker, language keys, classification (quotation/paraphrase/fictional/interpretive), references, choices.
- `Discovery`: facts, sources, link targets, journal visibility.
- Persist only stable progress state, not raw Phaser object instances.
- Localized text stored in language dictionaries (UTF-8 Sinhala and English).
- Content schema and validation must prevent broken scene/objective/references.

## First prototype acceptance criteria
- Runs locally without credentials or backend.
- Character can walk with WASD/arrows and mobile virtual joystick.
- Collision boundaries and camera movement work.
- At least one NPC can be approached and interacted with.
- Dialogue advances via keyboard, click, or touch.
- One mission objective is triggered and a journal entry appears.
- One short animated environmental loop is present.
- Resizing and reload do not break the game.
- Unit and E2E test coverage for the core interaction flow.

## Deployment cautions
Next.js static export cannot use features needing a Next.js request-time server. Keep the server API optional until a real backend is introduced. Supabase RLS must protect every player-owned table when authentication arrives.
