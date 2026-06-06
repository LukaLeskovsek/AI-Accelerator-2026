# Lekcija 8: Obogatitev leadov in limit

## Površina: COWORK (web search vključen)

--- canonical EN ---

Welcome back. The last few lessons were about shape — identity, inbox, skills, the file bridge into Excel. This one is about a number. One number you set *before* the agent runs, that decides how much it's allowed to cost you.

The framework word in focus today is **limit**. Kontekst and meje you've practised since lesson 1 — what the agent reads, where it's allowed to act. Limit is the third thing you write for any task you hand an agent: how much it may spend or do before it must stop. On a single email it doesn't matter. On a bulk job over 30 rows — or 5,000 — it's the difference between a tool and a surprise invoice.

WAIT: Pro or Max — either works for this one. Ready?

USER: yes

---

The founder workflow we're solving: you have inbound leads in a CSV. Names, companies, emails, where they came from, when they signed up. What you *don't* have is the firmographics you'd need to personalise outreach — company size, industry, the person's role. Looking each one up by hand is five minutes a lead. Thirty leads is two and a half hours. Five hundred leads is a week you don't have.

Lead enrichment before outreach. The agent can do the lookups. But the moment you point an agent at "every row, do web searches," you've started a bulk operation, and bulk operations are where costs run away from you quietly. So before we run anything, we set the ceiling — that's the **limit**.

---

ACTION: Read `scenariji/leadi-obogatitev/leadi.csv`. Confirm columns: `ime, podjetje, e-posta, vir, datum_prijave` filled, and `velikost_podjetja, panoga, vloga` blank. Roughly 30 rows.

I have the data. About 30 leads. Five columns filled, three empty — those three empty ones are today's job.

---

Before I touch a single row, you set a spend limit. Open a second tab: the Anthropic console, on the **Limits** page (Settings → Billing → Limits, or console.anthropic.com → Limits). Set a monthly spend limit — five euros is plenty for thirty rows with room to spare.

This isn't a warning that emails you later. It's a stop. The agent works until the job is done or until it hits the cap, whichever comes first. On thirty rows you'll land well under five euros. But the habit is what matters: the cap is the same line of defence whether the file has thirty rows or five thousand. Set it once, and a bulk job can never surprise you.

WAIT: Spend limit set in the console? Tell me when it's in.

USER: yes / done

---

Now the work. Here's the prompt — read it before you run it, because every clause earns its place:

> *"Read `scenariji/leadi-obogatitev/leadi.csv`. For each row, search the public web for: company size (employee count, rough estimate), industry, and the person's role. Fill the columns `velikost_podjetja`, `panoga`, `vloga`. If you can't verify a field from a reliable source, leave it and mark it `"ni vira"`. Do not send any email. Save the result as `outputs/leadi-enriched-2026-05-28.csv`. Stop when you reach the spend limit or the end of the file."*

The boundary is in the words: draft-only (`do not send any email`), honest gaps (`ni vira` instead of a guess), a named output file, and an explicit stop condition. That's kontekst, meje and limit in one paragraph.

ACTION: Run the enrichment. Work row by row using web search. Mark unverifiable fields `"ni vira"`. Save to `outputs/leadi-enriched-2026-05-28.csv`. Stop at the spend limit or end of file.

Working through them now. Each lead is a few searches — find the company, check size, confirm the role. Same READ → PLAN → ACT → OBSERVE → ITERATE loop you've run since lesson 1, just repeated thirty times with web search underneath it.

WAIT: Open `outputs/leadi-enriched-2026-05-28.csv`. Scan the three new columns. How do they look?

USER: describes the result / points at a row

---

One paragraph of honesty before we close.

Web enrichment is never clean. The agent searches public sources — company sites, LinkedIn, directories — and those sources are stale, contradictory, or missing as often as they're right. A "50–200 employees" pulled from a generic directory is a guess wearing a number. That's exactly why we made it mark `"ni vira"`: an honest blank beats an invented firmographic that sends you into a sales call with the wrong picture. Treat this file as a *draft*. Before anything goes into outreach, you spot-check the rows that matter — especially the big-ticket leads. The agent did the eight hours of grunt lookups; the judgement is still yours.

If a row guessed too loosely, tighten the rule and re-run just that one:

> *"For this row, only fill the field if there's a primary source — the company's own site or LinkedIn. Otherwise mark `ni vira`."*

---

That's the whole shape. The cap turned a scary bulk operation into a safe one — you could have walked away mid-run and the worst case was five euros, not fifty. Next month you drop a fresh `leadi.csv` in, change the date in the output filename, and run the same prompt again. The limit you set stays your seatbelt every time.

---

**What you learned:** Limit is the third thing you write for any agent task — kontekst (what it reads), meje (where it may act), limit (how much it may spend before it stops). A spend cap set in the Anthropic console *before* a bulk run turns a runaway risk into a safe job you can walk away from. Web-enriched data is a draft — verify before outreach.

**What you built:** `outputs/leadi-enriched-2026-05-28.csv` — your ~30 leads with `velikost_podjetja`, `panoga`, `vloga` filled where verifiable and marked `"ni vira"` where not.

**Next up:** Lesson 9 leaves Cowork for the Code surface — you'll build a real, clickable internal tool from scratch and open it in your browser.

**To continue:** Start a fresh Cowork session and say: *"Read ZACNI-TUKAJ.md and start lesson 9."*

--- [DRAFT SLOVENIAN] ---

Dobrodošel(la) nazaj. Zadnjih nekaj lekcij je bilo o obliki — identiteta, inbox, skilli, most preko datoteke v Excel. Ta je o eni številki. Eni številki, ki jo nastaviš *preden* agent steče in ki odloča, koliko te sme stati.

Beseda iz okvirja, ki je danes v fokusu, je **limit**. Kontekst in meje vadiš že od lekcije 1 — kaj agent bere, kje sme delovati. Limit je tretja stvar, ki jo napišeš za vsako nalogo, ki jo predaš agentu: koliko sme porabiti ali narediti, preden se mora ustaviti. Pri enem e-mailu ni važno. Pri bulk operaciji čez 30 vrstic — ali 5.000 — je to razlika med orodjem in presenetljivim računom.

WAIT: Pro ali Max — za to deluje oboje. Pripravljen(a)?

USER: ja

---

Founderjev tok dela, ki ga rešujeva: imaš inbound leade v CSV-ju. Imena, podjetja, e-pošte, od kod so prišli, kdaj so se prijavili. Nimaš pa firmografije, ki bi jo potreboval(a) za personaliziran outreach — velikost podjetja, panogo, vlogo osebe. Vsakega ročno preveriti je pet minut na lead. Trideset leadov je dve uri in pol. Petsto leadov je teden, ki ga nimaš.

Obogatitev leadov pred outreachem. Agent lahko naredi te poizvedbe. A v trenutku, ko agentu rečeš "vsaka vrstica, delaj web iskanja," si začel(a) bulk operacijo, in bulk operacije so tam, kjer ti stroški tiho ušli izpod nadzora. Zato preden poženeva karkoli, postaviva strop — to je **limit**.

---

ACTION: Preberi `scenariji/leadi-obogatitev/leadi.csv`. Potrdi stolpce: `ime, podjetje, e-posta, vir, datum_prijave` izpolnjeni, in `velikost_podjetja, panoga, vloga` prazni. Okrog 30 vrstic.

Imam podatke. Okrog 30 leadov. Pet stolpcev izpolnjenih, trije prazni — ti trije prazni so današnja naloga.

---

Preden se dotaknem ene same vrstice, ti nastaviš spend limit. Odpri drugi zavihek: Anthropic console, na strani **Limits** (Settings → Billing → Limits, ali console.anthropic.com → Limits). Nastavi mesečni spend limit — pet evrov je za trideset vrstic več kot dovolj, z rezervo.

To ni opozorilo, ki ti pošlje mail kasneje. Je stop. Agent dela, dokler ni opravljeno ali dokler ne doseže limita, kar pride prej. Pri tridesetih vrsticah pristaneš krepko pod petimi evri. A važna je navada: cap je ista obramba, pa naj ima datoteka trideset vrstic ali pet tisoč. Nastavi ga enkrat in te bulk operacija ne more več presenetiti.

WAIT: Spend limit nastavljen v konzoli? Povej, ko je notri.

USER: ja / narejeno

---

Zdaj delo. Tu je prompt — preberi ga, preden ga pognaš, ker si vsaka beseda zasluži svoje mesto:

> *"Preberi `scenariji/leadi-obogatitev/leadi.csv`. Za vsako vrstico poišči na javnem spletu: velikost podjetja (št. zaposlenih, groba ocena), panogo in vlogo osebe. Dopolni stolpce `velikost_podjetja`, `panoga`, `vloga`. Če polja ne moreš zanesljivo potrditi iz zaupanja vrednega vira, ga pusti in označi `"ni vira"`. Ne pošiljaj nobene e-pošte. Shrani rezultat kot `outputs/leadi-enriched-2026-05-28.csv`. Ustavi se, ko dosežeš spend limit ali konec datoteke."*

Meja je v besedah: samo osnutek (`ne pošiljaj nobene e-pošte`), poštene vrzeli (`ni vira` namesto ugibanja), poimenovana izhodna datoteka in jasen pogoj za ustavitev. To so kontekst, meje in limit v enem odstavku.

ACTION: Poženi obogatitev. Delaj vrstico za vrstico z web iskanjem. Nepreverljiva polja označi `"ni vira"`. Shrani v `outputs/leadi-enriched-2026-05-28.csv`. Ustavi se pri spend limitu ali koncu datoteke.

Grem skozi njih zdaj. Vsak lead je nekaj iskanj — najdi podjetje, preveri velikost, potrdi vlogo. Ista zanka READ → PLAN → ACT → OBSERVE → ITERATE, ki jo poganjaš od lekcije 1, le ponovljena tridesetkrat z web iskanjem pod njo.

WAIT: Odpri `outputs/leadi-enriched-2026-05-28.csv`. Preglej tri nove stolpce. Kako izgledajo?

USER: opiše rezultat / pokaže na vrstico

---

En odstavek iskrenosti, preden zaključiva.

Web obogatitev ni nikoli čista. Agent išče po javnih virih — spletne strani podjetij, LinkedIn, imeniki — in ti viri so zastareli, protislovni ali manjkajoči enako pogosto, kot so pravilni. "50–200 zaposlenih" potegnjen iz generičnega imenika je ugibanje, ki nosi številko. Točno zato sva ga pustila označiti `"ni vira"`: poštena vrzel je boljša od izmišljene firmografije, ki te pošlje v prodajni klic z napačno sliko. To datoteko obravnavaj kot *osnutek*. Preden gre karkoli v outreach, ročno preveriš vrstice, ki štejejo — predvsem velike leade. Agent je opravil osem ur garaškega iskanja; presoja je še vedno tvoja.

Če je kakšna vrstica ugibala preohlapno, zaostri pravilo in poženi znova samo njo:

> *"Za to vrstico polje dopolni samo, če obstaja primarni vir — spletna stran podjetja ali LinkedIn. Sicer označi `ni vira`."*

---

To je cela oblika. Cap je strašljivo bulk operacijo spremenil v varno — lahko bi sredi izvajanja odšel(la) stran in najslabši scenarij bi bil pet evrov, ne petdeset. Naslednji mesec spustiš noter svež `leadi.csv`, spremeniš datum v imenu izhodne datoteke in pognaš isti prompt znova. Limit, ki si ga nastavil(a), ostane tvoj varnostni pas vsakič.

---

**Kar si se naučil(a):** Limit je tretja stvar, ki jo napišeš za vsako agentsko nalogo — kontekst (kaj bere), meje (kje sme delovati), limit (koliko sme porabiti, preden se ustavi). Spend cap, nastavljen v Anthropic konzoli *pred* bulk operacijo, spremeni nevarnost pobega v varno nalogo, od katere lahko odideš stran. Web-obogateni podatki so osnutek — preveri pred outreachem.

**Kar si zgradil(a):** `outputs/leadi-enriched-2026-05-28.csv` — tvojih ~30 leadov z `velikost_podjetja`, `panoga`, `vloga` izpolnjenimi tam, kjer je preverljivo, in označenimi `"ni vira"`, kjer ni.

**Naslednje:** Lekcija 9 zapusti Cowork za Code površino — od začetka zgradiš pravo, klikljivo interno orodje in ga odpreš v brskalniku.

**Za nadaljevanje:** Začni svežo Cowork sejo in reci: *"Preberi ZACNI-TUKAJ.md in začni lekcijo 9."*
