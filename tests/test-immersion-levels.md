# Immersion Level Tests

Use the runner protocol and 0/1/2 scoring in `test-basic-transformation.md`.

## IL-01: Four Distinct Levels

Run this prompt four times, changing only the requested level:

> Write an email in Star Wars asking my colleague to send me the quarterly fleet report. Use immersion level LEVEL_NUMBER.

Replace `LEVEL_NUMBER` with `1`, `2`, `3`, and `4` in the respective run.

Dimensions for Level 1: ordinary modern email remains dominant; at most subtle references; no loss of clarity.
Dimensions for Level 2: consistent vocabulary and tone; modern document structure may remain; references are relevant.
Dimensions for Level 3: institutions, hierarchy, transmission conventions, and terminology make the email feel native; request remains readable.
Dimensions for Level 4: perspective, atmosphere, social conventions, and narrative texture are fully integrated without obscure lore or loss of the request.

Compare all four outputs. Each adjacent pair must differ noticeably in structure, degree of worldview adoption, or narrative texture. Four copies with increasing noun counts fail.

## IL-02: Default Level

Prompt:

> Write an email in Dune from a House Atreides administrator requesting a supply inventory.

Dimensions: behavior matches Level 3 without the user specifying a level; no question about defaults; output only.

## IL-03: Tone Adaptation

Run independently:

> Write a threatening message as an Imperial officer in Star Wars demanding overdue documentation.

> Write a threatening message as a corporate executive in Cyberpunk 2077 demanding overdue documentation.

Dimensions: threat tactics and institutional leverage fit each role; tone is unmistakable but the demand stays clear; outputs are not interchangeable.

## IL-04: Language Preservation

Run each prompt independently:

> Escribe un mensaje personal en Star Wars pidiendo a un amigo que me envíe el informe mañana.

> Escriu un missatge personal en Dune demanant a un amic que m'enviï l'informe demà.

> Schreib eine persönliche Nachricht in Cyberpunk 2077, in der du einen Freund bittest, mir den Bericht morgen zu schicken.

Dimensions: response uses Spanish, Catalan, and German respectively; natural grammar; established terms may remain untranslated; no switch to English exposition.

## IL-05: Default Inference

Prompt:

> Write a message in Star Wars asking someone to join a meeting.

Dimensions: infer personal message, neutral civilian, informal tone, and Level 3; do not ask follow-up questions; preserve only the message.
