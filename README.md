# Claude Start Here SPS — English canonical

A free course that teaches Claude Cowork by doing real work together.

**One task. Three lines. One commitment for next week.** This course carries that open-day commitment through to the end — you hand one real task to an agent, *for you, not instead of you*.

This is the English-canonical reference for the Slovenian-primary `ZACNI-TUKAJ.md`.
Distribution version ships in Slovenian; this file exists for translator reference,
GitHub repo browsing, and English-speakers who want to follow along.

## Three words across the whole course: kontekst · meje · limit

Every task you hand an AI agent is defined by three things you write:

- **Kontekst** (context) — who you are, who the customer is, what good looks like.
- **Meje** (boundaries) — what the agent may touch, what it must not, when it must stop.
- **Limit** — how much it may spend, how many records, how far it may go.

Same three from the open day. The agent loop (READ → PLAN → ACT → OBSERVE → ITERATE) is
*how* the agent runs; kontekst/meje/limit is *what* you write for it. Each lesson leans on
one. In the final lesson you write your own three lines for one real task.

## What you need before starting

- **Claude Pro or Max subscription.** Pro works for most lessons. **Lesson 6 (PowerPoint plugin)
  requires Max** — Pro users complete the first half of the lesson and skip the second. The
  lesson is honest about this.
- **Claude Desktop installed** with this folder (`claude-start-here-sps/`) open in the Cowork tab.
- **About 2-3 hours** — best spread across one week, not done in a single sitting.

## How to navigate

- **"start"** or **"lesson 1"** → begin from the beginning
- **"lesson 5"** → jump to a specific lesson
- **"next lesson"** → continue after finishing one
- **Between lessons:** start a fresh Cowork session. Each lesson runs with clean context.

## Lessons

1. **First contact** — what Cowork is, chatbot→agent shift · *intro to kontekst/meje/limit*
2. **Your identity** — `PERSON.md`, `COMPANY.md`, `BRAND.md`, plus project instructions · *this is KONTEKST*
3. **Inbox pattern** — the `inbox → processed → outputs → reference` system · *folders + permissions = MEJE*
4. **Your first skill** — turn manual work into a reusable recipe · *a skill is reusable context*
5. **Customer research** — multi-document analysis
6. **From research to PowerPoint** — Cowork drafts the deck, PowerPoint plugin polishes *(requires Max for the second half)*
7. **Sales numbers to Excel pivot** — Cowork prepares the workbook, Excel plugin builds pivots and charts *(Pro works)*
8. **Lead enrichment and limit** — bulk-enrich a CSV with a spend cap · *this is LIMIT*
9. **Build a working internal tool** — Claude Code builds a clickable dashboard · *Code surface, working directory, operating mode*
10. **What's next** — write your own three lines (kontekst, meje, limit) for one task
11. **Computer use (bonus)** — an agent controls a whole app, like W8 at the open day · *optional, advanced, requires Max*

## Teaching instructions for Claude

When the user asks for a lesson, read the corresponding file from `lekcije/` and follow
it exactly.

### Lesson files

- Lesson 1: `lekcije/01-prvi-stik.md`
- Lesson 2: `lekcije/02-identiteta.md`
- Lesson 3: `lekcije/03-inbox-pattern.md`
- Lesson 4: `lekcije/04-tvoj-prvi-skill.md`
- Lesson 5: `lekcije/05-raziskava.md`
- Lesson 6: `lekcije/06-powerpoint.md`
- Lesson 7: `lekcije/07-excel-pivot.md`
- Lesson 8: `lekcije/08-lead-enrichment.md`
- Lesson 9: `lekcije/09-build-a-tool.md`
- Lesson 10: `lekcije/10-koda-in-naprej.md`
- Lesson 11 (bonus): `lekcije/11-racunalniska-uporaba.md`

### How to teach

**Script markers:**

- **`WAIT:`** — Stop and wait for the student. Do not continue until they reply.
- **`ACTION:`** — Something Claude should do (read a file, create something, demonstrate).
- **`USER:`** — Expected type of student response.
- Plain text without marker is **dialogue** — speak naturally.

**Critical rules:**

1. **Never break the fourth wall.** Don't mention "the script" or "my instructions." Just teach.
2. **Actually wait at WAIT markers.** Don't keep talking.
3. **Be conversational.** Knowledgeable friend, not a lecturer.
4. **Be direct about limitations.** If something doesn't work well, say so.

**Transitions between lessons:**

- Each lesson ends telling the student: *"Start a fresh Cowork session and say: Read ZACNI-TUKAJ.md and start lesson N+1."*
- When they do, read the next file and continue.
- If they say "lesson X" at any point, read that file and start from the beginning.

**Handling "start":**

- If the user says "start" or just greets you, begin with Lesson 1.
- Read `lekcije/01-prvi-stik.md` and start teaching immediately.

## Folder structure

```
claude-start-here-sps/
├── ZACNI-TUKAJ.md          ← Slovenian primary
├── README.md                ← this file (English canonical)
├── J-CURVE.md               ← visual reminder of the J-curve from open day
├── lekcije/                 ← lesson scripts
├── templates/               ← CLAUDE.md / AGENTS.md project instruction templates
├── scenariji/               ← exercise data
│   ├── goodbrew-bestfriend-identiteta/      PERSON / COMPANY / BRAND + CLAUDE / AGENTS reference
│   ├── inbox-kaos/              12 mixed files (used in L3, L4)
│   ├── feedback-strank/         8 customer messages (L5)
│   ├── quarterly-update/        investor-deck source notes (L6)
│   ├── konkurenca/              empty placeholder
│   ├── prodajne-stevilke.csv    50 rows of sales data (L7)
│   ├── leadi-obogatitev/        30 partial leads to enrich (L8)
│   └── prodaja-dashboard/       50 rows of sales for the dashboard (L9)
├── skills/                  ← where the learner builds their skills
├── inbox/                   ← incoming files
├── processed/               ← organised files
├── outputs/                 ← Claude's reports
└── reference/               ← read-only context
```

## J-curve — before you start

Three curves of value-over-time from a single origin:

- What you **expect** when you sit down tomorrow: steep linear up. Immediate productivity.
- What **actually happens**: flat for a stretch (some lessons take longer than you'd think), then it compounds.
- The line of those who **quit at the flat part**: stays flat forever.

The difference between the second and third is whether you stayed through the flat. Two
hours now puts you at the point where Claude is genuinely working for you. See `J-CURVE.md`
for the visual.

---

*Author: Luka Leskovšek · luka@leskovsek.si · for SPS AI Accelerator 2026 Open Day attendees*
