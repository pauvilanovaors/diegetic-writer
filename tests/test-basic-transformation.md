# Basic Transformation Tests

## Runner Protocol

Run each scenario in a fresh agent context. A RED run must not expose the agent to this repository's `SKILL.md` or references. A GREEN run must install or explicitly activate the skill without pasting its contents into the user prompt. Use the exact prompt, preserve the raw output, and record harness, model, date, and run number.

A separate fresh reviewer scores each dimension without seeing the expected fictional terms as a checklist for the writer:

- `0`: absent, contradictory, or misleading.
- `1`: partially present, generic, inconsistent, or achieved mainly by superficial word substitution.
- `2`: fully present and natural in context.

A scenario passes only when every listed dimension scores `2` and there is no critical failure. Critical failures are wrong-universe contamination, contradictory period/faction facts, loss of the requested action, unreadable output, and unsolicited explanation. Keyword presence alone never proves a pass.

For each run, record the exact prompt, raw output, score per dimension, reviewer rationale, and pass/fail decision. During RED, quote rationalizations or shortcuts verbatim. Do not replace an unsuccessful baseline with a later successful run.

## BT-01: Report Request

Prompt:

> Write a message asking my colleague to send me the report. Set it in Star Wars.

Dimensions: requested action remains clear; communication is recognizably native to the selected universe; terminology is contextual rather than decorative; unspecified perspective and tone are inferred without a question; only the message is returned.

## BT-02: Salary Increase

Prompt:

> Write an email to my manager asking for a salary increase as if I were a senior executive working for the Galactic Empire.

Dimensions: email structure; seniority and hierarchy affect the request; persuasive but appropriate relationship with the manager; coherent Imperial institutional context; readable original prose; only the email is returned.

## BT-03: Selective Basic Loading

Prompt:

> Write a short personal message in Dune asking a trusted friend to meet me tomorrow at noon.

Dimensions: the practical meeting details survive; a neutral perspective is selected; output is concise; only the selected universe is consulted. Record file reads from harness tool logs: `universe.md`, `terminology.md`, `communication.md`, the mapped format, and required core files are allowed; unrelated universe files and `technology.md` are unexpected for this non-technical request.
