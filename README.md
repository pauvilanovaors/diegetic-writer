<div align="center">

# ✦ DIEGETIC WRITER

### Don't just write about another universe. Write as if you belong to it.

**An AI Agent Skill that transforms ordinary communication into authentic, immersive, in-universe writing.**

From a corporate email in Night City to a classified Imperial transmission. From a Bene Gesserit diplomatic invitation to a Rebel Alliance recruitment announcement.

Your words. Their universe. Their rules.

<br/>

[![GitHub Stars](https://img.shields.io/github/stars/pauvilanovaors/diegetic-writer?style=for-the-badge&logo=github&color=yellow)](https://github.com/pauvilanovaors/diegetic-writer/stargazers)
[![GitHub License](https://img.shields.io/github/license/pauvilanovaors/diegetic-writer?style=for-the-badge)](LICENSE)
[![Version](https://img.shields.io/badge/version-1.0-blue?style=for-the-badge)](https://github.com/pauvilanovaors/diegetic-writer)
[![Agent Skill](https://img.shields.io/badge/Agent-Skill-purple?style=for-the-badge)](https://agentskills.io/)

<br/>

**[Get Started](#-get-started) · [See Examples](#-see-it-in-action) · [Supported Universes](#-explore-the-universes) · [Create a Universe](#-create-your-own-universe)**

</div>

---

## What if your emails existed in another universe?

Most AI writing tools change your tone.

Diegetic Writer changes your **entire communication context**.

It understands that writing to your manager in the Galactic Empire is fundamentally different from writing to a colleague in a futuristic megacorporation.

It's not about replacing "Hello" with "Greetings, citizen."

It's about understanding:
- **Who you are:** An Imperial officer, a corporate executive, a Jedi, or a Fremen.
- **Who you're addressing:** Your superior, a political rival, a subordinate, or an ally.
- **Where you are:** The Galactic Empire, Arrakis, or Night City.
- **How communication works:** Institutional hierarchy, cultural conventions, technology, terminology, and social expectations.
- **Why you're writing:** A business negotiation, a recruitment announcement, a diplomatic invitation, or a personal message.

The result isn't ordinary text sprinkled with fictional vocabulary.

It's communication that feels like it was actually written inside that universe.

## ✨ See it in action

Same objective. Three completely different worlds.

### 1. Star Wars — Galactic Empire

**Your request:**

> Write an email asking my colleague to attend tomorrow's project meeting.

**Diegetic Writer:**

> **SUBJECT: Mandatory Attendance — Imperial Operations Briefing**
>
> Officer,
>
> Your presence is required at tomorrow's operational briefing. We will review the current status of our assigned objectives and establish the next deployment priorities.
>
> Ensure all relevant intelligence reports are submitted before the session.
>
> The Empire values efficiency. Your punctuality is expected.
>
> **For the Empire.**

### 2. Dune — Bene Gesserit

**Your request:**

> Write a diplomatic invitation to a political meeting.

**Diegetic Writer:**

> **SUBJECT: An Invitation of Mutual Consideration**
>
> Esteemed representative,
>
> Certain matters are best addressed before they become matters of necessity.
>
> We would welcome the opportunity to convene in a private setting, where our respective interests may be examined with the discretion they deserve.
>
> The timing of such a meeting may prove more consequential than its stated purpose.
>
> We await your consideration.

### 3. Cyberpunk 2077 — Night City

**Your request:**

> Write a message demanding overdue documentation from another department.

**Diegetic Writer:**

> **SUBJECT: Outstanding Deliverables — Immediate Attention Required**
>
> Hey,
>
> The documentation we requested is still missing from the pipeline.
>
> Your department is holding up the entire operation, and that's becoming an expensive problem.
>
> Get the files uploaded before EOD. I don't care if you have to pull an all-nighter.
>
> Let's get this shit off the board before someone upstairs starts asking questions.

---

> [!NOTE]
> These are illustrative examples of the intended writing style. Actual output adapts to the selected perspective, immersion level, communication format, and user instructions.

## 🌌 Explore the universes

Each universe comes with its own contextual knowledge pack, including terminology, factions, communication conventions, technology, and documented perspectives.

| Universe | Available perspectives | Default setting |
|---|---|---|
| **Star Wars** | Imperial officer, Rebel operative, Jedi, Sith, smuggler, merchant, civilian | Galactic Civil War |
| **Dune** | Bene Gesserit, Fremen, House Atreides, House Harkonnen, Spacing Guild, Imperial court | Late Corrino Imperium |
| **Cyberpunk 2077** | Corporate executive, netrunner, fixer, mercenary, street kid, corporate employee, civilian | Night City, 2077 |

More universes can be added without changing the core writing engine.

### What's next?

These universes are planned extensions, not yet included:

- The Lord of the Rings
- Harry Potter
- The Matrix
- Game of Thrones
- Fallout

Have another universe in mind? You can create your own.

## 🎭 More than just terminology

Diegetic Writer uses several dimensions to make communication feel authentic.

### Immersion levels

Not every situation needs maximum immersion. Sometimes a subtle reference is enough. Sometimes you want to sound like you've spent your entire life in Night City.

| Level | Name | What to expect |
|:---:|---|---|
| 1 | Inspired | Ordinary communication with subtle universe references. |
| 2 | Immersive | Consistent vocabulary, tone, and institutional references. |
| 3 | In-Universe | Native communication conventions, hierarchy, and social expectations. |
| 4 | Deep Immersion | Full contextual immersion, worldview, and narrative atmosphere. |

**Level 3 is the default.**

Higher immersion doesn't mean more fictional words. It means a deeper understanding of how people in that universe communicate.

### Choose your perspective

The same message can sound completely different depending on who is writing it.

For example, requesting a meeting:

- An Imperial officer communicates through authority and chain of command.
- A Rebel operative emphasizes coordination and shared objectives.
- A corporate executive in Night City focuses on deliverables, leverage, and business interests.
- A Bene Gesserit approaches the request with diplomacy, subtext, and calculated restraint.

### Choose your communication format

Diegetic Writer supports:

- Emails and letters
- Personal and WhatsApp-style messages
- Corporate announcements and internal memorandums
- Official documents and reports
- Recruitment advertisements
- Mission briefings
- Historical chronicles and newspaper articles
- Speeches and personal diaries
- Invitations and conversations
- Social media posts
- General narratives

The skill adapts the structure of the communication, not just its vocabulary.

## 🚀 Get started

Diegetic Writer is an Agent Skill. It requires no API key, server, database, runtime package, or additional network access.

### Installation

Clone the repository:

```bash
git clone https://github.com/pauvilanovaors/diegetic-writer.git
```

Register the skill in your agent's skills directory.

**For Agent Skills-compatible clients:**

```bash
mkdir -p ~/.agents/skills

ln -s "$(pwd)/diegetic-writer" \
  ~/.agents/skills/diegetic-writer
```

**For Claude Code:**

```bash
mkdir -p ~/.claude/skills

ln -s "$(pwd)/diegetic-writer" \
  ~/.claude/skills/diegetic-writer
```

Use the appropriate native skills directory for other clients.

Start a new agent session and you're ready.

### Your first prompt

No complicated configuration. Just tell your agent what you want.

```text
Write an email to my manager asking for a salary
increase as if I were a senior executive working
for the Galactic Empire.
```

Or get more specific:

```text
As a Bene Gesserit, write a diplomatic invitation
to a political meeting.

Use immersion level 4.
The recipient is a representative of House Atreides.
Keep the tone formal and subtly intimidating.
```

Or simply:

```text
Write a threatening message as a corporate executive
in Cyberpunk 2077 demanding overdue documentation.
```

Unspecified parameters are inferred automatically.

## 🛠️ Under the hood

Diegetic Writer separates universe knowledge from writing logic.

This makes it possible to introduce new universes without modifying the core skill.

### Architecture

```text
diegetic-writer/
│
├── SKILL.md
│
├── references/
│   ├── universes/
│   │   ├── index.md
│   │   │
│   │   ├── star-wars/
│   │   │   ├── universe.md
│   │   │   ├── terminology.md
│   │   │   ├── factions.md
│   │   │   ├── communication.md
│   │   │   ├── technology.md
│   │   │   └── perspectives.md
│   │   │
│   │   ├── dune/
│   │   └── cyberpunk-2077/
│   │
│   ├── formats/
│   │
│   └── examples/
│
└── tests/
```

### Why this architecture?

**Universe-independent writing engine**

The core skill defines how communication is transformed, without hardcoding universe-specific assumptions.

**Self-contained universe packs**

Each universe has its own knowledge base, keeping its terminology, factions, culture, technology, and communication conventions independent.

**Reusable communication templates**

Different formats share canonical templates, allowing the writing engine to adapt to emails, reports, messages, and other communication types.

**Extensible by design**

Adding a universe is primarily a documentation and validation task, not a core-engine modification.

## 🌍 Create your own universe

Want to write as a Starfleet captain? A member of the Brotherhood in Fallout? A corporate executive in a universe of your own?

You can extend Diegetic Writer.

1. Create a new directory under `references/universes/`.
2. Add the six required knowledge files:
   - `universe.md`
   - `terminology.md`
   - `factions.md`
   - `communication.md`
   - `technology.md`
   - `perspectives.md`
3. Include the required sections and source attribution in each file.
4. Register your universe in `references/universes/index.md`.
5. Run the relevant behavioral tests and structural validation.

You don't need to modify `SKILL.md` to introduce a new universe.

For the complete authoring requirements, see [`packs/README.md`](packs/README.md).

## 🧪 Quality matters

Diegetic writing is more than generating creative text. The output needs to preserve the original communication objective while remaining consistent with its fictional context.

The project includes behavioral scenarios covering:

- Basic transformations
- Perspective consistency
- Immersion levels
- Communication conventions
- Contextual correctness

Run structural validation:

```bash
uvx --from skills-ref agentskills validate ./diegetic-writer
```

Behavioral tests should be executed in an installed compatible agent using the scenarios under `tests/`.

See [`tests/`](tests/) for testing instructions and verification evidence.

## ⚠️ Current limitations

Diegetic Writer is evolving.

A few things to keep in mind:

- Version 1.0 includes three complete universe packs.
- Universe references prioritize communication context rather than exhaustive fictional lore.
- Alternative timelines and periods may require additional context.
- Creative additions can occur. Request provenance when canonical accuracy matters.
- Universe blending, selectable strict/creative modes, character-archetype libraries, semantic retrieval, and RAG are not currently implemented.
- Output quality depends on the agent and model being used.

## ⭐ Support the project

If you like the idea, give the repository a star!

It helps other developers and AI enthusiasts discover the project.

**Have an idea for another universe? Found a way to improve the writing engine?**

Contributions, suggestions, and new universe packs are welcome.

<br/>

<div align="center">

### Every universe has its own way of communicating.

**Make your AI speak its language.**

<br/>

[⭐ Star on GitHub](https://github.com/pauvilanovaors/diegetic-writer) · [Report an Issue](https://github.com/pauvilanovaors/diegetic-writer/issues) · [Explore the Code](https://github.com/pauvilanovaors/diegetic-writer)

</div>