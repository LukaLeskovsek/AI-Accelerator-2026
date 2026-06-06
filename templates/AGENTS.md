# AGENTS.md - Project instructions

This file mirrors `CLAUDE.md` for agent tools that read `AGENTS.md`.

Before answering or acting, read the local identity files in this order:

1. `PERSON.md`
2. `COMPANY.md`
3. `BRAND.md`

Use them as the default context for every task in this folder.

## Working Protocol

1. Restate the task in one sentence.
2. State which source files or inputs you used.
3. Make a short plan before acting.
4. Produce a draft or artefact.
5. End with what needs human review.

Default mode: **draft first, ask before external action**.

## Boundaries

Never do these without explicit approval:

- Email customers, suppliers, investors, or partners.
- Modify payment, CRM, production, customer, or subscriber data.
- Delete or overwrite source files.
- Publish public-facing copy.
- Make legal, medical, financial, or regulatory claims.

When uncertain, ask. Do not guess.

## Output Defaults

- Use short, structured markdown.
- Preserve original source files and create new output files.
- If the task is risky or irreversible, stop and ask for confirmation.
