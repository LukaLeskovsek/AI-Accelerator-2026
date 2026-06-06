# Lekcija 4: Tvoj prvi skill

## Površina: COWORK

--- canonical EN ---

Welcome back. Last lesson we did the work manually — read each file, decided where it goes, moved it, logged it. Today we make that work reusable. One file in `skills/` and the next time the inpacket fills up, you say one sentence instead of walking through twelve decisions.

A skill is **kontekst** you write once and reuse — the recipe for how you do a task, saved so you don't re-explain it every time. Same first word as the identity files, pointed at a workflow instead of a company.

But not yet. First we do it again.

WAIT: Cowork session open, walkalong folder loaded?

USER: yes

---

ACTION: Refill `inpacket/` from `scenariji/inpacket-kaos-2/`. Five files: a partnership-meeting note, a customer email about new flavours, an Instagram analytics screenshot, a packaging supplier invoice, and `racun-marec-2026.md` — same filename as a file already in `processed/racuni/` from L3. The collision is the edge case to surface.

Inpacket is full again. Five files. I'll process them the same way as last time — read, decide, move, log.

ACTION: Read each file. Move into existing `processed/` subfolders where they fit. For the duplicate `racun-2026-04.pdf`, do NOT overwrite — rename to `racun-2026-04--2.pdf` and note it in the log. For the screenshot that doesn't fit any existing category, create `processed/zaslonske-slike/` and move it there. Write `outputs/processing-log-2026-04-21.md` describing every decision.

Done. Open the log when you have a second.

WAIT: Compare run 2 to run 1. What was the same? What was different?

USER: notices the duplicate handling, possibly the new subfolder

---

The repeatable parts: read the file, look at content, pick a category from `processed/`, move, log. That happens every time.

The case-by-case parts: what to do when a filename already exists. What to do when no category fits. Whether the screenshot belongs in its own folder or inside an existing one. Those are judgement calls — and the skill we write needs to encode the judgement, not just the steps.

Two runs is enough material. We have a "happy path" from run 1 and an edge case from run 2. That's a real picture of the work, not a guess.

---

Quick aside before we write the file.

Most founders write the skill on run 1. The skill works — but it tends to be brittle, because it bakes in whatever happened that one time. Two or three manual runs first usually produce a more robust skill — same logic as training a new employee, you write SOPs from real experience, not first guesses. That said: if you know what you want, write it on run 1 and iterate later. Skill files are plain text. Iteration is cheap.

We have two runs, so let's write it now.

---

ACTION: Create `skills/file-processor.md` in the walkalong folder. Structure:

```markdown
# File Processor

## Trigger
When the user says "process the inpacket" or equivalent, or when files appear in `inpacket/`.

## Inputs
- All files in `inpacket/`
- Existing folder structure in `processed/`
- BRAND.md and COMPANY.md (for context on what business categories matter)

## Steps
1. List every file in `inpacket/`. Stop if empty.
2. For each file:
   a. Read enough to identify type (invoice, customer message, contract, screenshot, supplier doc, other).
   b. Match to an existing `processed/` subfolder. Categories in use: racuni, sporocila-strank, pogodbe, dobavitelji, zaslonske-slike.
   c. If no category fits, propose a new subfolder name to the user — don't create it silently.
   d. Check for filename collision in the destination. If collision: append `--2`, `--3`, etc. Never overwrite.
   e. Move the file. Note source, destination, and any rename in a running list.
3. Write `outputs/processing-log-YYYY-MM-DD.md` with the running list. One file per line: `source → destination (note)`.
4. Report total processed, any new categories created, any collisions handled.

## Output
- Files moved into `processed/<category>/`
- One log file in `outputs/`
- Summary message to user

## Validation
- `inpacket/` is empty (or only files explicitly skipped)
- Every moved file appears in the log
- No file was overwritten — collisions show as `--2` suffixes
- Any new subfolder was confirmed by the user before creation
```

Open the file. Read it.

WAIT: Anything missing? Anything you'd say differently?

USER: maybe small edits — a category they want, a never-do they want explicit

---

A few notes on what this file actually is.

The **trigger** is how the agent knows to use this skill. When you say "process the inpacket," it picks this file up. You could write "every Monday morning" — but that needs scheduled tasks, a more advanced setup. For now: trigger on your words.

The **steps** are the procedure. Notice step 2c — "propose, don't create silently." That's a guard rail. Without it, the agent invents a subfolder every time something doesn't fit, and three months later you have nineteen categories.

The **validation** is the agent's self-check. After running, it confirms the four things at the bottom. If validation fails, the agent tells you instead of pretending the run was clean.

That's the whole anatomy: trigger, inputs, steps, output, validation. Five sections. Every skill you write later will look like this.

---

One thing about marketplace skills.

Anthropic and other people publish skills you can import. They're useful as reference — read them, see how they structure things. But import-as-is and you'll inherit assumptions that don't match your business. Categories that aren't yours. Validation rules that ignore the things you actually care about. Build your own around your real workflow. Edit the skill file when you notice what's missing. That's how the skill stays yours.

---

Now we test it.

ACTION: Refill `inpacket/` from `scenariji/inpacket-kaos-3/`. Five files: a website-analytics CSV (off-category — no existing `processed/` subfolder fits), a vet's question about priboljški allergens, a Q1 tax summary, a customer photo (placeholder), and what looks like a marketing asset. The off-category CSV is the edge case — the skill should *propose* a new subfolder rather than create one silently.

ACTION: Run the skill. The agent should read `skills/file-processor.md`, follow the steps, hit one decision point (the `.csv` analytics file — no existing category) and propose `processed/analitika/` rather than creating it silently. Write `outputs/processing-log-2026-04-22.md`.

Done. Three logs in `outputs/`. Two manual, one skill-driven.

WAIT: Compare the three logs. The skill-driven run reads almost identical to the manual ones, right?

USER: yes / notices small differences

---

That's the point. The skill is just your manual process, written down. It doesn't make the agent smarter — it makes the agent consistent. Same steps every time. Same guard rails every time. Same validation every time.

And the file is editable. After three more runs you'll spot something — a category you wish existed, a collision rule you'd handle differently, a validation step you forgot. Open `skills/file-processor.md`, edit, save. The agent reads the new version on the next run. Your skill grows with your business.

---

**What you learned:** A skill is your manual process codified — trigger, inputs, steps, output, validation. Two-three manual runs first usually produce a less brittle skill, but iteration is cheap. Build your own around your actual workflow; marketplace skills are reference, not your kitchen.

**What you built:** `outputs/processing-log-2026-04-21.md`, `skills/file-processor.md`, `outputs/processing-log-2026-04-22.md`. Plus whatever new `processed/` subfolders the runs created (`zaslonske-slike/`, `analitika/`).

**Next up:** Lesson 5 is research synthesis — eight customer messages, multi-document reading, one report that names the pattern.

**To continue:** Start a fresh Cowork session and say: *"Read ZACNI-TUKAJ.md and start lesson 5."*

--- [DRAFT SLOVENIAN] ---

Dobrodošel(la) nazaj. V prejšnji lekciji sva delo opravila ročno — prebrala vsako datoteko, odločila, kam gre, premaknila, zalogirala. Danes to delo narediva ponovno uporabno. Ena datoteka v `skills/` in naslednjič, ko se inpacket napolni, rečeš en stavek namesto da se sprehodiš skozi dvanajst odločitev.

Skill je **kontekst**, ki ga napišeš enkrat in ponovno uporabiš — recept, kako opraviš nalogo, shranjen, da ga ne razlagaš vsakič. Ista prva beseda kot identitetne datoteke, le usmerjena v delovni tok namesto v podjetje.

Ampak še ne. Najprej naredimo še enkrat ročno.

WAIT: Cowork seja odprta, tečajna mapa naložena?

USER: ja

---

ACTION: Napolni `inpacket/` iz `scenariji/inpacket-kaos-2/`. Pet datotek: zapisek partnership sestanka, e-mail stranke o novih okusih, Instagram analitika posnetek, faktura dobavitelja pakiranja, in `racun-marec-2026.md` — isto ime kot datoteka, ki je že v `processed/racuni/` iz L3. Kolizija je edge case za izpostavitev.

Inpacket je spet poln. Pet datotek. Predeloval bom enako kot zadnjič — preberi, odloči, premakni, zaloguj.

ACTION: Preberi vsako datoteko. Premakni v obstoječe `processed/` podmape, kjer ustreza. Za podvojeno `racun-2026-04.pdf` NE prepiši — preimenuj v `racun-2026-04--2.pdf` in zabeleži v log. Za posnetek zaslona, ki ne sodi nikamor, ustvari `processed/zaslonske-slike/` in ga premakni tja. Zapiši `outputs/processing-log-2026-04-21.md` z opisom vsake odločitve.

Narejeno. Odpri log, ko boš imel(a) trenutek.

WAIT: Primerjaj run 2 z run 1. Kaj je bilo enako? Kaj drugače?

USER: opazi obravnavo dvojnika, morda novo podmapo

---

Ponovljivi deli: preberi datoteko, poglej vsebino, izberi kategorijo iz `processed/`, premakni, zaloguj. To se zgodi vsakič.

Deli, odvisni od primera: kaj narediti, ko ime datoteke že obstaja. Kaj narediti, ko nobena kategorija ne ustreza. Ali posnetek zaslona sodi v lastno mapo ali v obstoječo. To so presoje — in skill, ki ga piševa, mora kodificirati presojo, ne samo korake.

Dva ponovitvena cikla je dovolj materiala. Imava "srečno pot" iz run 1 in robni primer iz run 2. To je realna slika dela, ne ugibanje.

---

Hitra opomba, preden napiševa datoteko.

Večina ustanoviteljev napiše skill po prvem ciklu. Skill deluje — a je pogosto krhk, ker vase vgradi tisto, kar se je zgodilo tisto enkrat. Dva ali trije ročni cikli prej običajno dajo bolj robusten skill — ista logika kot pri uvajanju novega zaposlenega, SOP-e pišeš iz pravih izkušenj, ne iz prvih ugibanj. Ob tem: če veš, kaj hočeš, napiši skill po prvem ciklu in iteriraj kasneje. Skill datoteke so navadno besedilo. Iteracija je poceni.

Imava dva cikla, torej napiševa zdaj.

---

ACTION: Ustvari `skills/file-processor.md` v tečajni mapi. Struktura:

```markdown
# File Processor

## Trigger
Ko uporabnik reče "predelaj inpacket" ali ekvivalent, ali ko se v `inpacket/` pojavijo datoteke.

## Inputs
- Vse datoteke v `inpacket/`
- Obstoječa struktura map v `processed/`
- BRAND.md in COMPANY.md (za kontekst, katere poslovne kategorije so pomembne)

## Steps
1. Naštej vse datoteke v `inpacket/`. Ustavi, če je prazen.
2. Za vsako datoteko:
   a. Preberi toliko, da identificiraš tip (račun, sporočilo stranke, pogodba, posnetek zaslona, dobaviteljev dokument, drugo).
   b. Poveži z obstoječo `processed/` podmapo. Kategorije v uporabi: racuni, sporocila-strank, pogodbe, dobavitelji, zaslonske-slike.
   c. Če nobena kategorija ne ustreza, predlagaj uporabniku ime nove podmape — ne ustvari je tiho.
   d. Preveri kolizijo imen v ciljni mapi. Če je kolizija: dodaj `--2`, `--3`, itd. Nikoli ne prepiši.
   e. Premakni datoteko. Zabeleži vir, cilj in morebitno preimenovanje v tekoč seznam.
3. Zapiši `outputs/processing-log-YYYY-MM-DD.md` s tekočim seznamom. Ena datoteka na vrstico: `vir → cilj (opomba)`.
4. Poročaj: skupaj predelano, nove kategorije, obravnavane kolizije.

## Output
- Datoteke premaknjene v `processed/<kategorija>/`
- En log v `outputs/`
- Povzetek uporabniku

## Validation
- `inpacket/` je prazen (ali samo datoteke, ki so bile izrecno preskočene)
- Vsaka premaknjena datoteka je v logu
- Nobena datoteka ni bila prepisana — kolizije so vidne kot `--2` priponke
- Vsaka nova podmapa je bila pred ustvaritvijo potrjena s strani uporabnika
```

Odpri datoteko. Preberi.

WAIT: Kaj manjka? Kaj bi povedal(a) drugače?

USER: morda majhni popravki — kategorija, ki jo želi, prepoved, ki naj bo eksplicitna

---

Nekaj opomb o tem, kaj je ta datoteka v resnici.

**Trigger** je način, kako agent ve, da naj uporabi ta skill. Ko rečeš "predelaj inpacket," pobere to datoteko. Lahko bi napisal(a) "vsak ponedeljek zjutraj" — a to potrebuje scheduled tasks, naprednejšo nastavitev. Za zdaj: sproži po tvojih besedah.

**Steps** so postopek. Opazi korak 2c — "predlagaj, ne ustvari tiho." To je varovalo. Brez tega agent ob vsaki neujemajoči datoteki izumi novo podmapo, in čez tri mesece imaš devetnajst kategorij.

**Validation** je samopreverba agenta. Po izvedbi potrdi štiri stvari na dnu. Če validacija pade, ti agent pove, namesto da se pretvarja, da je bil cikel čist.

To je celotna anatomija: trigger, inputs, steps, output, validation. Pet razdelkov. Vsak nadaljnji skill, ki ga boš napisal(a), bo videti tako.

---

Ena stvar o marketplace skillih.

Anthropic in drugi objavljajo skille, ki jih lahko uvoziš. Koristni so kot referenca — preberi, poglej, kako stvari strukturirajo. Toda uvozi-kakršen-je in podedoval(a) boš predpostavke, ki ne ustrezajo tvojemu podjetju. Kategorije, ki niso tvoje. Validacijska pravila, ki spregledajo tisto, na kar v resnici paziš. Zgradi svojega okrog tvojega resničnega delovnega toka. Uredi skill datoteko, ko opaziš, kaj manjka. Tako skill ostane tvoj.

---

Zdaj testiramo.

ACTION: Napolni `inpacket/` iz `scenariji/inpacket-kaos-3/`. Pet datotek: CSV s spletno analitiko (off-category — nobena `processed/` podmapa še ne ustreza), vprašanje veterinarja o sestavinah priboljškov, Q1 davčni povzetek, fotografija stranke (placeholder), in nekaj, kar izgleda kot marketing asset. Off-category CSV je edge case — skill naj *predlaga* novo podmapo, ne ustvari je tiho.

ACTION: Zaženi skill. Agent naj prebere `skills/file-processor.md`, sledi korakom, naleti na eno odločitvenotočko (`.csv` analitika — ni obstoječe kategorije) in predlaga `processed/analitika/` namesto da bi tiho ustvaril mapo. Zapiši `outputs/processing-log-2026-04-22.md`.

Narejeno. Trije logi v `outputs/`. Dva ročna, eden voden po skillu.

WAIT: Primerjaj tri loge. Skill-vodeni cikel se bere skoraj enako kot ročna, kajne?

USER: ja / opazi majhne razlike

---

To je bistvo. Skill je samo tvoj ročni postopek, zapisan na papir. Ne naredi agenta pametnejšega — naredi ga doslednega. Isti koraki vsakič. Iste varovalke vsakič. Ista validacija vsakič.

In datoteka je urejljiva. Po treh dodatnih ciklih boš nekaj opazil(a) — kategorija, ki si jo želiš, kolizijsko pravilo, ki bi ga obravnaval(a) drugače, validacijski korak, ki si ga pozabil(a). Odpri `skills/file-processor.md`, uredi, shrani. Agent prebere novo različico ob naslednjem ciklu. Tvoj skill raste s tvojim podjetjem.

---

**Kar si se naučil(a):** Skill je tvoj ročni postopek, kodificiran — trigger, inputs, steps, output, validation. Dva-trije ročni cikli prej običajno dajo manj krhek skill, a iteracija je poceni. Zgradi svojega okrog tvojega delovnega toka; marketplace skilli so referenca, ne tvoja kuhinja.

**Kar si zgradil(a):** `outputs/processing-log-2026-04-21.md`, `skills/file-processor.md`, `outputs/processing-log-2026-04-22.md`. Plus nove `processed/` podmape iz ciklov (`zaslonske-slike/`, `analitika/`).

**Naslednje:** Lekcija 5 je sinteza razispiva — osem sporočil strank, branje več dokumentov, eno poročilo, ki poimenuje vzorec.

**Za nadaljevanje:** Začni svežo Cowork sejo in reci: *"Preberi ZACNI-TUKAJ.md in začni lekcijo 5."*
