# Diegetic Writer

Diegetic Writer is an Agent Skill that transforms ordinary communication into original text shaped by a fictional universe's institutions, terminology, social relationships, technology, culture, period, and communication conventions. It aims for contextual immersion rather than superficial word replacement.

Version 1.0 includes complete packs for Star Wars, Dune, and Cyberpunk 2077. The skill itself requires no API key, server, database, runtime package, or network access.

## Installation

Clone the repository and expose its directory to an Agent Skills-compatible client:

```bash
git clone https://github.com/pauvilanovaors/diegetic-writer.git
mkdir -p ~/.agents/skills
ln -s "$PWD/diegetic-writer" ~/.agents/skills/diegetic-writer
```

Start a new session and ask for an in-universe transformation. Clients that scan `.agents/skills` should discover `diegetic-writer` automatically.

For a client with a native user skills directory, link the same directory there instead. For example, in Claude Code:

```bash
mkdir -p ~/.claude/skills
ln -s "$PWD/diegetic-writer" ~/.claude/skills/diegetic-writer
```

Use only one installation link per client scope to avoid duplicate skill names. To verify the directory contract during development, run `uvx --from skills-ref agentskills validate ./diegetic-writer`; this is not a runtime requirement.

## Usage

Provide a communication objective and universe. Add perspective, format, tone, immersion, period, audience, and language when they matter.

```text
Write a message in Star Wars asking someone to join a meeting.
```

```text
Write an email to my manager asking for a salary increase as if I were a senior executive working for the Galactic Empire.
```

```text
As a Bene Gesserit in Dune, write a diplomatic invitation to a political meeting.
```

```text
Write a threatening message as a corporate executive in Cyberpunk 2077 demanding overdue documentation. Use immersion level 4.
```

Unspecified values are inferred. Defaults are Level 3, a neutral appropriate perspective, the universe's documented default period, and the request language. The skill returns only the transformed communication unless explanation or provenance is requested.

## Available Universes and Perspectives

| Identifier | Universe | Default context | Documented perspectives |
|---|---|---|---|
| `star-wars` | Star Wars | Galactic Civil War of the original trilogy | Imperial officer, Rebel operative, Jedi, Sith, smuggler, merchant, neutral civilian |
| `dune` | Dune | Late Corrino Imperium during the first novel, before Paul's accession | Bene Gesserit, Fremen, House Atreides, House Harkonnen, Spacing Guild, Imperial court, neutral administrator |
| `cyberpunk-2077` | Cyberpunk 2077 | 2077 base-game Night City | Corporate executive, netrunner, fixer, mercenary, street kid, corporate employee, neutral civilian |

The identifiers `lord-of-the-rings`, `harry-potter`, `the-matrix`, `game-of-thrones`, and `fallout` are planned extensions, not installed packs.

## Communication Formats

The skill supports email, letters, WhatsApp-style messages, corporate announcements, internal memorandums, official documents, historical chronicles, newspaper articles, recruitment advertisements, invitations, speeches, reports, personal diaries, mission briefings, conversations, social media posts, personal messages, and general narratives.

Related formats share seven canonical templates:

| Requested format | Template |
|---|---|
| Email, letter, invitation | `email` |
| Personal message, WhatsApp message, conversation, social media post | `personal-message` |
| Corporate announcement, recruitment advertisement | `corporate-announcement` |
| Internal memorandum, official document, report | `corporate-memo` |
| Mission briefing | `mission-briefing` |
| Historical chronicle, newspaper article | `historical-document` |
| Speech, personal diary, narrative | `narrative` |

New format templates can be added under `references/formats/` and mapped in `SKILL.md`. Unlike universe packs, new formats intentionally require a mapping update.

## Immersion Levels

| Level | Behavior |
|---|---|
| 1 — Inspired | Ordinary communication with one or two subtle relevant references. |
| 2 — Immersive | Consistent vocabulary, tone, and institutions with a familiar structure. |
| 3 — In-Universe | Native document conventions, hierarchy, medium, and social expectations. |
| 4 — Deep Immersion | Full worldview and narrative atmosphere while retaining the practical objective. |

Higher immersion is not a terminology count, a demand for obscure lore, or permission to invent canon.

## Tones

Formal, informal, humorous, threatening, mysterious, epic, bureaucratic, militaristic, diplomatic, satirical, philosophical, and dystopian tones are adapted to the selected role and universe. A threat uses the sender's plausible institutional or social leverage rather than a generic aggressive voice.

## Examples and Quality Guidance

See `references/examples/before-after.md` for superficial versus contextual transformations and `references/examples/quality-examples.md` for four-level, perspective, tone, and language comparisons. These are original quality references, not stock passages to reuse.

## Create a Universe

1. Create `references/universes/NEW-IDENTIFIER/` using lowercase letters, numbers, and single hyphens.
2. Add nonempty `universe.md`, `terminology.md`, `factions.md`, `communication.md`, `technology.md`, and `perspectives.md` files.
3. Include every required section and a Sources section in each file.
4. Add one `- NEW-IDENTIFIER: Display Name` line to `references/universes/index.md`.
5. Run behavior tests for the new universe and `uvx --from skills-ref agentskills validate ./diegetic-writer`.

Do not edit `SKILL.md` to add a universe. Read `packs/README.md` for the full authoring and source-attribution contract.

## Testing

The Markdown scenarios under `tests/` evaluate real generated behavior, not file existence alone. Follow the fresh-context runner and 0/1/2 rubric in `tests/test-basic-transformation.md`. Baseline and verification evidence is stored under `tests/results/` with harness, model, raw outputs, scores, and limitations.

Run structural validation:

```bash
uvx --from skills-ref agentskills validate ./diegetic-writer
```

Then run all `BT-*`, `PC-*`, `IL-*`, and `CC-*` scenarios in an installed compatible agent. Use fresh reviewers, retain failed outputs, and never convert a behavior failure into a keyword-only test.

## Limitations

- Only three universes are installed; their references prioritize communication over exhaustive lore.
- Default continuity is documented per pack. Other periods may require more specific references and testing.
- Generated details can be creative additions. Ask for provenance when canonical fidelity matters.
- Universe blending, selectable strict/creative modes, character-archetype libraries, semantic retrieval, and RAG are not implemented.
- Output quality depends on the agent and model. Only environments documented in `tests/results/verification.md` have been behavior-tested.

## Contributing

Keep generation logic universe-neutral, format templates independent of universe knowledge, and universe facts inside their own pack. Prefer primary works and official references, summarize rather than reproduce copyrighted text, and record source URLs when available, coverage, access dates, and usage restrictions.

For universe contributions, follow `packs/README.md`, add registry and behavior evidence, and do not change the core solely to make a pack work. For core or format changes, supply baseline/after behavior comparisons and run the full regression scenarios. Keep optional advanced features out of version 1.0.

## License

MIT. See `LICENSE`.
