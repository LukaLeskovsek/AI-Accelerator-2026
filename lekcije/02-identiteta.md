# Lekcija 2: Tvoja identiteta

## Površina: CHAT

--- canonical EN ---

Welcome back. `hello.md` is in your folder from Lesson 1. Today we put three more files next to it — and these three are the ones every later lesson will read.

This lesson is **kontekst** — the first of the three words. Identity files are how you give the agent context once, so you don't re-explain who you are on every task.

Open the 10 pravil handout from the open day. Find rule #8:

> **Identiteta prva, brief drugi.** Before you ask the agent to do anything, make sure it knows who you are (PERSON), what your company does (COMPANY), and how it should sound (BRAND). Without that, even the best prompt produces generic output.

That is the whole lesson in one sentence. The work today is writing those three files for *you*.

WAIT: Did you find rule #8 on the handout?

USER: yes

---

I have a worked example I'll show you first. The Good Brew & Your Best Friend persona — a Slovenian founder running a craft brewery with a dog-treat side line made from pre-hop spent grain. Same persona used in the open-day demos. Three files, kept short on purpose.

ACTION: Read `scenariji/goodbrew-bestfriend-identiteta/PERSON.md`, `COMPANY.md`, and `BRAND.md` — pick 2-3 lines from each to read aloud.

From PERSON.md, the lines that matter most:

- *"Default: propose first, then act after my OK."*
- *"Never email customers, suppliers, partners, or regulators without approval."*

That second line is doing real work. It tells the agent what's off-limits. Without it, the agent assumes everything you mention is fair game.

From COMPANY.md:

- *"We are not a pet health or nutrition company."*
- *"Dog treats use spent grain separated before hops are added."*

The first line stops the agent writing nutrition copy. The second preserves the safety boundary.

From BRAND.md:

- *"Three words: Warm. Craft. Grounded."*
- *"We never say: healthy, safe for every dog, beer for dogs, hops are fine."*

Voice as a do-list and a don't-list. Both matter equally.

That's the whole pattern. Each file is twenty lines or less. Not an essay. A spine.

WAIT: Skim those three files in your folder. Anything jump out before we write yours?

USER: brief reaction

---

Now yours. Three short Q&As, one per file. I'll write each file when we finish that pass.

**PERSON.md first.**

WAIT: What's your name, and what's your role in your company right now? (Solo founder? Co-founder with a focus area? Something else?)

USER: name + role

---

WAIT: When and how do you do your best work? Mornings vs evenings, deep work vs meetings, the tools you live in daily. Just bullet points — no essay.

USER: rhythm + tools

---

WAIT: Three things the agent should NEVER do without checking with you first. Think hard about this one — it's the line that prevents accidents. Money, customers, public-facing things, anything irreversible.

USER: three never-do items

ACTION: Write `PERSON.md` to the walkalong root using the Good Brew & Your Best Friend file as structural template. Keep under 25 lines. Use the learner's exact wording where they were specific.

Done. `PERSON.md` is in your folder. Open it, see if anything is off — we can fix it now or later. Identity files are meant to be edited.

WAIT: Looks right?

USER: yes / small fix

---

**COMPANY.md next.**

WAIT: One sentence describing what your company does. Imagine you're telling someone at a dinner who's never heard of you. No buzzwords.

USER: one-liner

---

WAIT: Who is this for, and who is it explicitly NOT for? Both halves matter. The "not for" line stops the agent generalising.

USER: audience + non-audience

---

WAIT: Where are you right now (stage, rough numbers if you have them) and what's the one thing you want to be true by end of 2026?

USER: current stage + 2026 goal

ACTION: Write `COMPANY.md` to the walkalong root. Same structure as Good Brew & Your Best Friend COMPANY.md but with the learner's content. Include a short non-goals section if anything from the conversation fits there. Keep under 25 lines.

Done. Same drill — open it, check it.

WAIT: Reads true?

USER: yes / fix

---

**BRAND.md last. This is the shortest of the three.**

WAIT: Three words that describe your voice. Adjectives only. (Good Brew & Your Best Friend picked warm, craft, grounded.)

USER: three words

---

WAIT: Three words you are NOT. Things people might mistake you for if they didn't know better, or things you actively avoid sounding like.

USER: three anti-words

---

WAIT: One vocabulary preference — a word you do use, or a word/phrase you refuse to use. (Good Brew & Your Best Friend: "škatla" instead of "package"; never "synergy" or "journey.") Even one item makes the file pull weight.

USER: vocabulary item(s)

ACTION: Write `BRAND.md` to the walkalong root. Mirror Good Brew & Your Best Friend's structure — three words, three NOTs, vocabulary section. Keep under 25 lines.

Done. Three identity files. That's the spine.

One more file type matters when you move from Chat/Cowork into coding agents or desktop agents: project instructions.

- `CLAUDE.md` is the Claude-specific version.
- `AGENTS.md` is the more portable version used by other agent tools.

For this starter course, the Good Brew & Your Best Friend reference already includes both, and the reusable versions live in `templates/`. They do not replace PERSON, COMPANY and BRAND. They point the agent to those files and add always-on rules: propose first, ask when missing information, do not touch production systems, preserve source files, and stop before risky actions.

ACTION: Read `templates/CLAUDE.md`. Create `CLAUDE.md` in the walkalong root from that template. Keep the read order exactly as written: `PERSON.md` first, then `COMPANY.md`, then `BRAND.md`. Add the learner's three NEVER-do rules from PERSON.md under Boundaries.

ACTION: Read `templates/AGENTS.md`. Create `AGENTS.md` in the walkalong root from that template, mirroring the same read order and boundaries, so the folder can travel to other agent tools later.

---

One thing before we close.

These files are not paperwork. Every other lesson in this walkalong opens by reading them. When the agent writes a customer email in Lesson 3, it reads BRAND.md first. When it drafts an investor update in Lesson 6, it reads all three. `CLAUDE.md` / `AGENTS.md` make that instruction explicit for tools that read project-level instructions. That's why they're at the top level of your folder, not buried somewhere — they need to be the first thing the agent finds.

And they're meant to evolve. After two weeks of using your agent, you'll notice what's missing — a vocabulary word that keeps slipping through, a never-do you forgot. Open the file, edit, save. The agent picks up the new version on the next read.

---

**What you learned:** Identity comes before brief (rule #8). PERSON, COMPANY and BRAND are the agent's spine; `CLAUDE.md` / `AGENTS.md` are the project-level instruction files that tell agent tools to use that spine.

**What you built:** `PERSON.md`, `COMPANY.md`, `BRAND.md`, `CLAUDE.md`, and `AGENTS.md` at the top of your walkalong folder.

**Next up:** Lesson 3 is the inpacket pattern — what you do when files start coming in faster than you can sort them. Cowork from here on.

**To continue:** Start a fresh Cowork session and say: *"Read ZACNI-TUKAJ.md and start lesson 3."*

--- [DRAFT SLOVENIAN] ---

Dobrodošel(la) nazaj. `hello.md` je v tvoji mapi iz lekcije 1. Danes zraven postaviva še tri datoteke — in te tri so tiste, ki jih bo vsaka naslednja lekcija prebrala.

Ta lekcija je **kontekst** — prva od treh besed. Identitetne datoteke so način, kako agentu enkrat daš kontekst, da ne razlagaš znova, kdo si, ob vsaki nalogi.

Odpri 10 pravil iz odprtega dneva. Poišči pravilo #8:

> **Identiteta prva, brief drugi.** Preden prosiš agenta, naj nekaj naredi, se prepričaj, da pozna: kdo si ti (PERSON), kaj tvoje podjetje dela (COMPANY), kako naj zveni (BRAND). Brez tega so rezultati generični — tudi najboljši prompt bo imel generični izhod brez identitete.

To je cela lekcija v enem stavku. Današnje delo je napisati te tri datoteke za *tebe*.

WAIT: Si našel(a) pravilo #8 na listu?

USER: ja

---

Najprej ti pokažem primer — Good Brew & Your Best Friend. Slovenski ustanovitelj, ki vodi craft pivovarno in stransko linijo pasjih priboljškov iz pred-hmeljnega pivovarskega zrnja. Ista persona kot na demih odprtega dneva. Tri datoteke, namerno kratke.

ACTION: Preberi `scenariji/goodbrew-bestfriend-identiteta/PERSON.md`, `COMPANY.md` in `BRAND.md` — izberi po 2-3 vrstice iz vsake na glas.

Iz PERSON.md, vrstici, ki najbolj nosita:

- *"Privzeto: najprej predlagaj, potem izvedi po mojem OK."*
- *"Nikoli ne pošilja e-pošte strankam, dobaviteljem, partnerjem ali regulatorjem brez potrditve."*

Druga vrstica dela pravo delo. Pove agentu, kaj je zunaj meja. Brez tega agent predpostavi, da je vse, kar omeniš, prosto za uporabo.

Iz COMPANY.md:

- *"Nismo podjetje za zdravje ali prehrano psov."*
- *"Priboljški uporabljajo zrnje, ločeno pred dodajanjem hmelja."*

Prva vrstica ustavi agenta, da ne piše prehranskih trditev. Druga ohrani varnostno mejo.

Iz BRAND.md:

- *"Tri besede: Toplo. Craft. Prizemljeno."*
- *"Nikoli ne rečemo: zdravo, varno za vsakega psa, pivo za pse, hmelj je v redu."*

Glas kot do-seznam in ne-do-seznam. Oba štejeta enako.

To je celoten vzorec. Vsaka datoteka dvajset vrstic ali manj. Ni esej. Je hrbtenica.

WAIT: Preleti te tri datoteke v svoji mapi. Ti kaj pade v oči, preden napiševa tvoje?

USER: kratka reakcija

---

Zdaj tvoje. Tri kratki Q&A-ji, eden na datoteko. Vsako datoteko bom napisal, ko zaključiva njen del.

**Najprej PERSON.md.**

WAIT: Kako ti je ime in kakšna je tvoja vloga v podjetju trenutno? (Solo ustanovitelj? Soustanovitelj z določenim področjem? Kaj drugega?)

USER: ime + vloga

---

WAIT: Kdaj in kako delaš najbolje? Jutra ali večeri, globoko delo ali sestanki, orodja, ki jih uporabljaš dnevno. Samo alineje — brez eseja.

USER: ritem + orodja

---

WAIT: Tri stvari, ki jih agent NIKOLI ne sme narediti brez tvoje potrditve. Razmisli zares — ta vrstica preprečuje nesreče. Denar, stranke, javne stvari, karkoli nepovratnega.

USER: trije nikoli-ne-naredi

ACTION: Zapiši `PERSON.md` v koren tečajne mape; uporabi Good Brew & Your Best Friend datoteko kot strukturni vzorec. Manj kot 25 vrstic. Učenčeve točne besede tam, kjer je bil(a) konkreten/-na.

Narejeno. `PERSON.md` je v tvoji mapi. Odpri jo, poglej, če je kaj narobe — popraviva zdaj ali kasneje. Identitetne datoteke so namenjene urejanju.

WAIT: Izgleda v redu?

USER: ja / majhen popravek

---

**Naslednje COMPANY.md.**

WAIT: En stavek, ki opisuje, kaj tvoje podjetje dela. Predstavljaj si, da nekomu na večerji, ki še nikoli ni slišal zate. Brez modnih besed.

USER: en stavek

---

WAIT: Komu je to namenjeno in komu izrecno NI? Obe polovici sta pomembni. Vrstica "ni za" ustavi agenta, da ne posplošuje.

USER: publika + ne-publika

---

WAIT: Kje si zdaj (faza, grobe številke, če jih imaš) in katera je ena stvar, za katero želiš, da bo do konca 2026 resnična?

USER: trenutna faza + cilj 2026

ACTION: Zapiši `COMPANY.md` v koren tečajne mape. Ista struktura kot Good Brew & Your Best Friend COMPANY.md, z učenčevo vsebino. Vključi kratek razdelek non-goals, če iz pogovora kaj sodi tja. Manj kot 25 vrstic.

Narejeno. Isti vrstni red — odpri, preveri.

WAIT: Drži?

USER: ja / popravek

---

**BRAND.md kot zadnja. To je najkrajša od treh.**

WAIT: Tri besede, ki opisujejo tvoj glas. Samo pridevniki. (Good Brew & Your Best Friend je izbral toplo, craft, prizemljeno.)

USER: tri besede

---

WAIT: Tri besede, ki NISI. Stvari, za katere bi te ljudje lahko zamenjali, če te ne bi poznali, ali stvari, ki se jim aktivno izogibaš.

USER: tri proti-besede

---

WAIT: Ena vokabularna preferenca — beseda, ki jo uporabljaš, ali beseda/fraza, ki jo zavračaš. (Good Brew & Your Best Friend: "pivo za ljudi, priboljški za pse"; nikoli "zdravo", "varno za vsakega psa" ali "pivo za pse".) Že ena postavka da datoteki težo.

USER: vokabular

ACTION: Zapiši `BRAND.md` v koren tečajne mape. Zrcali Good Brew & Your Best Friend strukturo — tri besede, tri NE, razdelek vokabular. Manj kot 25 vrstic.

Narejeno. Tri identitetne datoteke. To je hrbtenica.

Še ena vrsta datotek postane pomembna, ko greš iz Chat/Cowork v coding agente ali desktop agente: projektna navodila.

- `CLAUDE.md` je Claude-specifična verzija.
- `AGENTS.md` je bolj prenosljiva verzija za druga agentska orodja.

V starter course-u ima Good Brew & Your Best Friend primer že obe, ponovno uporabni verziji pa sta v `templates/`. Ne zamenjata PERSON, COMPANY in BRAND. Agentu povesta, naj te datoteke najprej prebere, potem pa dodata stalna pravila: najprej predlagaj, vprašaj, ko manjka informacija, ne dotikaj se produkcijskih sistemov, ohrani izvorne datoteke in se ustavi pred tveganimi koraki.

ACTION: Preberi `templates/CLAUDE.md`. Iz predloge ustvari `CLAUDE.md` v korenu tečajne mape. Ohrani vrstni red branja točno tako: najprej `PERSON.md`, potem `COMPANY.md`, potem `BRAND.md`. Pod Boundaries dodaj učenčeva tri NIKOLI pravila iz PERSON.md.

ACTION: Preberi `templates/AGENTS.md`. Iz predloge ustvari `AGENTS.md` v korenu tečajne mape z istim vrstnim redom branja in istimi mejami, da lahko mapa kasneje potuje tudi v druga agentska orodja.

---

Ena stvar, preden zaključiva.

Te datoteke niso papirologija. Vsaka naslednja lekcija v tečaju jih najprej prebere. Ko agent v lekciji 3 piše e-pošto stranki, najprej prebere BRAND.md. Ko v lekciji 6 piše osnutek poročila za investitorje, prebere vse tri. `CLAUDE.md` / `AGENTS.md` to navodilo naredita eksplicitno za orodja, ki berejo projektna navodila. Zato so na vrhu mape, ne zakopane nekje globoko — biti morajo prva stvar, ki jo agent najde.

In so namenjene razvoju. Po dveh tednih dela z agentom boš opazil(a), kaj manjka — vokabularna beseda, ki se vedno znova prikrade, prepoved, ki si jo pozabil(a). Odpri datoteko, uredi, shrani. Agent prevzame novo različico ob naslednjem branju.

---

**Kar si se naučil(a):** Identiteta pred briefom (pravilo #8). PERSON, COMPANY in BRAND so hrbtenica agenta; `CLAUDE.md` / `AGENTS.md` sta projektni navodili, ki agentskim orodjem povesta, naj to hrbtenico uporabijo.

**Kar si zgradil(a):** `PERSON.md`, `COMPANY.md`, `BRAND.md`, `CLAUDE.md` in `AGENTS.md` na vrhu tečajne mape.

**Naslednje:** Lekcija 3 je inpacket vzorec — kaj narediš, ko datoteke prihajajo hitreje, kot jih lahko sortiraš. Od zdaj naprej Cowork.

**Za nadaljevanje:** Začni svežo Cowork sejo in reci: *"Preberi ZACNI-TUKAJ.md in začni lekcijo 3."*
