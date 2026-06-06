# AGENTS.md - Good Brew Project Instructions

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

- Email customers, suppliers, partners, or regulators.
- Modify webshop, payment, CRM, inventory, order, recipe, label, or production data.
- Delete or overwrite source files.
- Make legal, medical, financial, nutrition, or regulatory claims.
- Claim dog treats are safe for every dog.
- Change ingredient, allergen, recipe, or safety wording.
- Publish public-facing copy.

When uncertain, ask. Do not guess.

## Product Safety Rule

Dog treats use **spent grain separated before hops are added**.

Always preserve these constraints:

- no hops
- no alcohol
- no xylitol
- recipe is vet-reviewed
- no medical or nutrition claims without human approval

## Output Defaults

- Use short, structured markdown.
- Keep customer-facing drafts aligned with `BRAND.md`.
- Preserve original source files and create new output files.
- If the task is risky or irreversible, stop and ask for confirmation.
