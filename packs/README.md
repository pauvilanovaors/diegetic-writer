# Knowledge Pack Authoring

A knowledge pack supplies communication-relevant fictional knowledge without changing generation logic. A valid contribution is independently readable, internally consistent, sourced, and tested with real agent outputs.

## Required Structure

```text
references/universes/NEW-IDENTIFIER/
├── universe.md
├── terminology.md
├── factions.md
├── communication.md
├── technology.md
└── perspectives.md
```

Use lowercase letters, numbers, and single hyphens for the identifier. Register only a complete pack in `references/universes/index.md` as `- NEW-IDENTIFIER: Display Name`.

## File Contracts

### universe.md

Use the top-level heading `# Universe: Display Name` and sections `Overview`, `Historical Context`, `Political Structure`, `Society and Culture`, `Technology`, `Geography`, `Important Concepts`, `Canonical Boundaries`, and `Sources`. Name the default period explicitly. Explain how institutions and culture affect everyday communication rather than writing an encyclopedia.

### terminology.md

Group terms by function. For each term, record meaning and appropriate context. Include misuse boundaries where confusion is likely. Do not include a term solely because it is recognizable.

### factions.md

Describe each relevant organization's purpose, relationships, communication characteristics, preferred concepts, authority, and limits. Distinguish public identity from secret aims.

### communication.md

Document media, formality, hierarchy, greetings, closings, military/corporate/cultural conventions, linguistic patterns, and security practices. Label inferred writing conventions as interpretation rather than canonical quotation.

### technology.md

For each relevant technology, explain communication or logistical use and capability boundaries. Remove decorative technical entries.

### perspectives.md

For each role, describe social position, personality tendencies, language, relationships, resources, knowledge limits, and communication preferences. Include a neutral fallback role.

## Research and Attribution

1. Prefer primary works and official references.
2. Cross-check political relationships, historical period, technology limits, and faction-specific language.
3. Summarize facts in original wording. Do not scrape or reproduce books, scripts, game dialogue, or substantial reference text.
4. End every file with `## Sources`.
5. For each source, record name, URL when available, information covered, access date in `YYYY-MM-DD` form, and relevant usage restriction.
6. Keep adaptation-specific facts separate when book, film, and game continuities differ.

## Quality Checklist

- All six files are nonempty and use the shared headings.
- Default period and neutral perspective are explicit.
- Every important term includes meaning, context, and necessary boundaries.
- Faction relationships do not contradict world history.
- Communication guidance explains behavior, not just lore.
- Sources and usage restrictions are present in all six files.
- No core file contains pack-specific terms.
- Adding the directory and one registry line works without a `SKILL.md` change.

## Behavior Evidence

Add scenarios for basic transformation, two contrasting perspectives, a technical request, default Level 3, cross-universe isolation, and one non-English language where practical. Run them without the skill for a baseline when developing new generic guidance, then with the completed pack. Preserve raw outputs, file-read observations, scores, reviewer rationale, harness, model, and limitations in `tests/results/`.

Reject a pack that merely swaps nouns, requires unrelated universe files, copies stock passages, contradicts its selected period, or needs a core edit to activate.
