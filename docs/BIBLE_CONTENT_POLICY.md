# Scripture and Content Policy

## Target corpus
66-book Protestant Bible. Intended translations: Sinhala Revised Old Version (SROV), New King James Version (NKJV).

## Rights rule
Never import, scrape, embed or publish substantial SROV or NKJV Bible text until rights to the exact electronic use, territory, caching, storage, quotation and redistribution are confirmed. Subscription to a Bible website or access to a Bible API is **not** a license to reproduce its contents. For development, use references and original narrative summaries. Keep Bible-text providers behind an interface.

## Evidence
All statements presented as biblical facts include book/chapter/verse source references. Validate names, chronology, relationships and details against approved source material.

## Classification per text field
- `quotation`: exact source wording, version identifier and permissions required.
- `paraphrase`: original summary of canonical text, explicitly non-quoted.
- `historical_background`: externally sourced contextual claim.
- `interpretation`: theological explanation; may require denominational review.
- `fictional_game_dialogue`: utility dialogue invented for navigation, never portrayed as scriptural words.

## Review process
1. Research agent extracts cited facts.
2. Second pass checks references and labels uncertainty.
3. Game designer creates play mechanics while preserving outcomes.
4. Human biblical/theological reviewer approves content before publication.
5. Any corrections propagate to saved content and version history.

## Localization
Maintain separate English and Sinhala fields. Never infer an official Sinhala verse translation from an English paraphrase. Make clear whether narration is original adaptation or an exact authorized Bible quotation. Verify Sinhala rendering, cultural appropriateness and typography with real users.

## Difficult material
Handle biblical violence, slavery, sexuality, and potentially distressing themes age-appropriately, without erasing relevant meaning. Consider optional content notices and younger-player alternatives. Avoid assigning motivations not stated in Scripture.

## Content schema hints
`canonical_reference`, `characters`, `locations`, `event_sequence`, `fact_source_ids`, `dialogue_kind`, `language`, `review_state`, `reviewer`, `revision`.

## MVP sample
David and Goliath: 1 Samuel 17. Journal can point to a reference and show an original clearly labeled summary. It must not store NKJV/SROV verse text without permission.
