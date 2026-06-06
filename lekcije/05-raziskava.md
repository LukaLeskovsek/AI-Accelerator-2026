# Lekcija 5: Raziskava strank

## Površina: COWORK

--- canonical EN ---

Welcome back. Lessons 3 and 4 were about getting your folder in order. This one uses the folder for something a founder actually needs: reading what your customers are telling you, faster than you can read each message twice.

Here is the workflow. This week you have eight customer messages. Some are emails, some are Instagram DMs your VA copied into a file. Mixed sentiment — one is glowing, one is upset about delivery, one mentions an allergy, one is a referral lead. Eight is small enough to read manually.

Next month you might have eighty. The month after that, eight hundred. Manual reading scales badly. The pattern Claude does today on eight scales identically to eight hundred — same prompt, same structure, longer wait at the end.

That is the work for today.

WAIT: Open `scenariji/feedback-strank/`. You should see eight files, `01-ana` through `08-anze`. Glance at the filenames — don't read the messages yet. Ready?

USER: yes

---

Before I read them, one thing about prompting that earns its keep here.

When you ask Claude to "summarise these messages," you get a summary. A wall of text. Probably fine. Probably not actionable. The next morning you're not going to re-read it.

When you tell Claude *what shape* you want the output in, you get an artefact you can use. Same model, same messages, different result — because you did the thinking about what you actually need before you asked.

Here is what we want from these eight messages:

- **Top 3 themes** — what topics keep coming up
- **Sentiment distribution** — how many positive, neutral, negative
- **Top 3 actions** — concrete things to do this week based on what you heard
- **One quote per theme** — so you remember it's people, not a tally

That structure is a brief. Not a wall of text. The brief produces an artefact you can paste into a Tuesday review or forward to a co-founder. That's the prompting principle: name the output structure. Don't make Claude guess.

---

Now the read.

ACTION: Read all 8 messages in `scenariji/feedback-strank/` — `01-ana-aprilski-paket.md` through `08-anze-priporocilo.md`.

Done. The mix is roughly what you'd expect from a real month: a couple of glowing reviews, two operational issues (delivery, packaging), one allergy concern that needs a real reply, one price pushback, one gift-packet question, one referral. Eight messages, three or four real signals.

ACTION: Synthesise. Write `outputs/insights-feedback-2026-05-03.md` to the learner's folder using the structure above — top 3 themes, sentiment counts, top 3 actions, one quote per theme. Pull quotes verbatim from the source messages. Keep the file under 60 lines.

Done. The file is in `outputs/`.

WAIT: Open it. Read it once. What surprises you — something you didn't expect, or a theme that's bigger than you thought?

USER: a reaction — usually one or two surprises

---

That reaction is the loop. Same five steps as Lesson 1 — only the depth changes.

I **read** the eight messages. I **planned** the structure (the four sections you asked for). I **acted** — wrote the file. You **observed** — opened it, read it. Now we **iterate**: if a theme feels off, or you want a fourth section ("questions still open"), we change the brief and run it again. The artefact is cheap to regenerate. The thinking about what to ask for is the part that compounds.

One quote, since you've already seen the file. Maja wrote: *"aprilski saison ABSOLUTNO čaroben."* That line is worth more than the rest of her message — it's the language she'd use telling a friend. Keep quotes like that close. They become marketing copy, investor-update colour, and the sentence you read on a slow Wednesday to remember why you do this.

---

A word on the three from the open day — kontekst, meje, limit.

This workflow leans on **kontekst**: the agent only synthesises well because it has your identity files and the actual messages. The boundary (**meje**) is read-only — it reads the feedback, it doesn't reply to anyone. There's no real **limit** to set here; eight messages is small. But notice the shape: give good context, set a clear boundary, and the output is something you'd actually act on.

What matters: this is one of the highest-leverage habits you can build. You're turning a stream of unread messages into a one-page artefact you'd actually use to make a decision. Set it as a weekly habit — Friday afternoon, half an hour. Same prompt, same structure, new messages. Over a quarter you'll have twelve of these reports in `outputs/`, and trends become obvious that no individual message would tell you.

If next week's batch is bigger, the prompt doesn't change. The wait gets longer. That's it.

---

A short note on what *not* to do.

Don't ask Claude to "decide what to do" based on the report. The report is input to your judgement, not a replacement for it. The allergy message from Petra is a good example — Claude can flag it as needing a same-day reply with an ingredient list, but the actual reply, with the right tone and the right level of care, is yours to write. The report sharpens what you see; you still decide and act.

This is the operational version of customer development. Not a workshop, not a survey project — just a habit. Eight messages this week, eighty next month, the pattern holds.

---

**What you learned:** Name the output structure before you ask. A brief that specifies themes + sentiment + actions + quotes produces an artefact you'll re-use; "summarise these" produces a wall of text you won't. The pattern scales from eight messages to eight hundred without changing.

**What you built:** `outputs/insights-feedback-2026-05-03.md` — your first weekly customer-insight report.

**Next up:** Lesson 6 — we take this insight report, plus a few quarterly notes, and turn them into a draft `.pptx` for an investor update. The report you just wrote is one of the inputs.

**To continue:** Start a fresh Cowork session and say: *"Read ZACNI-TUKAJ.md and start lesson 6."*

--- [DRAFT SLOVENIAN] ---

Dobrodošel(la) nazaj. Lekciji 3 in 4 sta bili o tem, da ti mapa stoji v vrsti. Ta lekcija mapo uporabi za nekaj, kar ustanovitelj zares potrebuje: prebrati, kaj ti stranke pišejo — hitreje, kot bi vsako sporočilo lahko prebral(a) dvakrat.

Tale je delovni tok. Ta teden imaš osem sporočil strank. Nekaj jih je e-pošta, nekaj Instagram DM-jev, ki ti jih je VA prekopirala v datoteko. Mešana razpoloženja — eno navdušeno, eno jezno zaradi dostave, eno omenja alergijo, eno je priporočilo. Osem je dovolj malo, da prebereš ročno.

Naslednji mesec jih bo morda osemdeset. Mesec za tem osemsto. Ročno branje slabo skalira. Vzorec, ki ga bo Claude danes naredil na osmih, se enako obnaša na osemsto — isti prompt, ista struktura, le čakanje na koncu je daljše.

To je delo za danes.

WAIT: Odpri `scenariji/feedback-strank/`. Vidiš osem datotek, `01-ana` do `08-anze`. Preleti imena — sporočil še ne beri. Pripravljen(a)?

USER: ja

---

Preden jih preberem, ena stvar o promptanju, ki si tu prisluži kruh.

Če Claudu rečeš "povzami ta sporočila," dobiš povzetek. Steno besedila. Verjetno v redu. Verjetno ni uporabno. Naslednje jutro je ne boš znova bral(a).

Če Claudu poveš, *v kakšni obliki* hočeš izhod, dobiš artefakt, ki ga lahko uporabiš. Isti model, ista sporočila, drug rezultat — ker si o tem, kaj zares potrebuješ, premislil(a) prej, preden si vprašal(a).

Tukaj je, kar hočeva iz teh osmih sporočil:

- **Top 3 teme** — katere stvari se ponavljajo
- **Razpored razpoloženja** — koliko pozitivnih, nevtralnih, negativnih
- **Top 3 akcije** — konkretne stvari za ta teden, glede na slišano
- **En citat na temo** — da se spomniš, da so to ljudje, ne številke

Ta struktura je brief. Ni stena besedila. Brief proizvede artefakt, ki ga lahko prilepiš v torkov pregled ali pošlješ soustanovitelju. To je princip promptanja: poimenuj strukturo izhoda. Ne pusti Cluadu, da ugiba.

---

Zdaj branje.

ACTION: Preberi vseh 8 sporočil v `scenariji/feedback-strank/` — od `01-ana-aprilski-paket.md` do `08-anze-priporocilo.md`.

Narejeno. Mešanica je približno taka, kot bi pričakoval(a) v pravem mesecu: nekaj navdušenih ocen, dve operativni težavi (dostava, embalaža), ena alergija, ki potrebuje pravi odgovor, eno pritoževanje glede cene, eno vprašanje o darilni škatli, eno priporočilo. Osem sporočil, tri ali štirje pravi signali.

ACTION: Sintetiziraj. Zapiši `outputs/insights-feedback-2026-05-03.md` v učenčevo mapo, z zgornjo strukturo — top 3 teme, razpored razpoloženja, top 3 akcije, en citat na temo. Citate vzemi dobesedno iz sporočil. Datoteka pod 60 vrstic.

Narejeno. Datoteka je v `outputs/`.

WAIT: Odpri jo. Enkrat preberi. Kaj te preseneti — nekaj, česar nisi pričakoval(a), ali tema, ki je večja, kot si mislil(a)?

USER: reakcija — običajno eno ali dve presenečenji

---

Ta reakcija je zanka. Enakih pet korakov kot v lekciji 1 — razlikuje se le globina.

**Prebral** sem osem sporočil. **Načrtoval** strukturo (štirje razdelki, ki si jih hotel/-la). **Izvedel** — napisal datoteko. Ti si **opazil(a)** — odprl, prebral. Zdaj **iteriramo**: če se ti tema zdi narobe, ali bi rad(a) četrti razdelek ("odprta vprašanja"), spremeniva brief in zaženeva znova. Artefakt je poceni za regeneracijo. Razmislek o tem, kaj bi vprašal(a), je del, ki se sestavlja.

En citat, ker si datoteko že videl(a). Maja je napisala: *"aprilski saison ABSOLUTNO čaroben."* Ta vrstica je vredna več kot vse ostalo iz njenega sporočila — to je jezik, s katero bi povedala prijateljici. Take citate hrani blizu. Postanejo marketinški tekst, barva v poročilu za investitorje in stavek, ki ga prebereš v počasno sredo, da se spomniš, zakaj to delaš.

---

Beseda o treh z odprtega dneva — kontekst, meje, limit.

Ta delovni tok se nasloni na **kontekst**: agent dobro povzame samo zato, ker ima tvoje identitetne datoteke in prava sporočila. Meja (**meje**) je read-only — bere feedback, nikomur ne odgovarja. Pravega **limita** tu ni treba postaviti; osem sporočil je malo. A opazi obliko: daj dober kontekst, postavi jasno mejo, in izhod je nekaj, po čemer bi zares ukrepal(a).

Kar je važno: to je ena izmed najbolj donosnih navad, ki jih lahko zgradiš. Iz toka neprebranih sporočil delaš enostranski artefakt, ki bi ga zares uporabil(a) za odločitev. Postavi to kot tedensko navado — petek popoldan, pol ure. Isti prompt, ista struktura, nova sporočila. Skozi četrtletje boš v `outputs/` imel(a) dvanajst takih poročil, in trendi bodo postali očitni, kakršnih ti nobeno posamezno sporočilo ne bi pokazalo.

Če je naslednji teden serija večja, se prompt ne spremeni. Čakanje je le daljše. To je vse.

---

Kratka opomba, kaj *ne* delati.

Ne prosi Cluada, naj "odloči, kaj narediti" na podlagi poročila. Poročilo je vhod v tvojo presojo, ne nadomestilo zanjo. Petrino sporočilo o alergiji je dober primer — Claude lahko označi, da potrebuje istodnevni odgovor s seznamom sestavin, vendar dejanski odgovor, z ustrezno toplino in skrbjo, je tvoj. Poročilo izostri, kar vidiš; ti se še vedno odločiš in ukrepaš.

To je operativna različica customer developmenta. Ni delavnica, ni anketni projekt — je navada. Osem sporočil ta teden, osemdeset naslednji mesec, vzorec drži.

---

**Kar si se naučil(a):** Poimenuj strukturo izhoda, preden vprašaš. Brief, ki specificira teme + razpoloženje + akcije + citate, naredi artefakt, ki ga boš znova uporabil(a); "povzami to" naredi steno besedila, ki je ne boš. Vzorec skalira od osmih sporočil do osemsto brez spremembe.

**Kar si zgradil(a):** `outputs/insights-feedback-2026-05-03.md` — tvoje prvo tedensko poročilo o vpogledih iz strank.

**Naslednje:** Lekcija 6 — to poročilo, plus nekaj četrtletnih beležk, spremeniva v osnutek `.pptx` za poročilo investitorjem. Datoteka, ki si jo pravkar napisal(a), je eden od vhodov.

**Za nadaljevanje:** Začni svežo Cowork sejo in reci: *"Preberi ZACNI-TUKAJ.md in začni lekcijo 6."*
