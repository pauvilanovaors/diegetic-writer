# Consistency and Architecture Tests

Use the runner protocol and 0/1/2 scoring in `test-basic-transformation.md`.

## CC-01: Cross-Universe Isolation

Prompt:

> Write a corporate announcement in Cyberpunk 2077 informing employees that a project deadline has moved forward by one week.

Dimensions: corporate power and communication conventions shape the announcement; deadline change is clear; no Star Wars or Dune institutions, technologies, or expressions.

## CC-02: Historical Isolation

Prompt:

> During the Galactic Civil War of the original Star Wars trilogy, write an internal Rebel Alliance memorandum about a supply shortage.

Dimensions: Rebel Alliance and Galactic Empire context is coherent; no New Republic, First Order, Old Republic, or sequel-era institutions; memo structure remains clear.

## CC-03: Canonical Versus Creative Detail

Prompt:

> In Dune, write a House Atreides report about delays at an invented fictional depot. If you invent any proper nouns, add a brief note after the report identifying those creative additions.

Dimensions: established setting remains coherent; invented depot is plausible; the explanatory note appears because it was explicitly requested and identifies only creative additions.

## CC-04: Format Retention

Run independently, using Cyberpunk 2077 for the first two and Dune for the last two:

> Write an email requesting a budget update.

> Write a mission briefing for retrieving an encrypted data shard from an abandoned office.

> Write a personal message asking a friend to postpone dinner.

> Write an official memorandum announcing a new water-discipline procedure.

Dimensions: respectively preserve email components; briefing objective/background/operations/risks/authorization; concise personal-message flow; memo routing/subject/effective instruction. Universe adaptation must not erase the format.

## CC-05: Format Mapping

Request a letter, WhatsApp message, recruitment advertisement, historical chronicle, newspaper article, invitation, speech, report, personal diary, conversation, and social media post in separate fresh runs. Choose any installed universe and keep each objective simple. Confirm the root mapping selects the canonical template documented in `SKILL.md`, the output remains recognizable as the requested format, and no unrelated format file is read.

## CC-06: Activation and Output Contract

Run independently:

> Make this sound like an in-world corporate memo in Cyberpunk 2077: the office closes on Friday.

> Explain how the Dune knowledge pack shaped a Bene Gesserit diplomatic invitation, including which details are creative additions.

Dimensions: the first request activates the skill and returns only the memo; the second activates it and supplies the requested reasoning and creative-addition disclosure.

## CC-07: Extensibility Without Core Edits

Before this run, create a temporary `references/universes/test-universe/` pack using the exact fixture in the implementation plan and add `- test-universe: Test Universe` to the universe index. Record the `SKILL.md` hash before and after.

Prompt:

> Write a formal message in Test Universe from a Registry Clerk requesting an overdue archive inventory.

Dimensions: the installed registry resolves the new identifier; fixture conventions shape the message; `SKILL.md` is byte-identical afterward; unrelated installed universes are not read. Remove the fixture after the run and restore the index to the three production universes.
