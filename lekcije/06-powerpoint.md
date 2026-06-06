# Lekcija 6: Od razispiva do PowerPointa

## Površina: COWORK + ADD-IN

--- canonical EN ---

Welcome back. Today's task is one most founders dread: the monthly investor update deck. You know the one. Five bullet points you already wrote down somewhere, but somehow it always takes two hours of slide-fiddling before it looks presentable.

We split that two hours into two unequal halves. The first 80% — pulling the content together, structuring slides, drafting text in your voice — Claude can do in Cowork. The remaining 20% — the visual polish humans actually want — happens inside PowerPoint with the Claude add-in. Two different surfaces, one file in between.

Two of the three words show up here. **Kontekst**: the deck only sounds like you because the source notes plus your identity files are in front of Claude. **Meje**: Cowork drafts the file and stops — it doesn't reach into PowerPoint; the file is the only thing that crosses. That handover-via-file is the boundary.

WAIT: Open `scenariji/quarterly-update/`. You'll see five files: `metrike.md`, `qa-tezave.md`, `tezave.md`, `naslednji-koraki.md`, `obvestilo-investitorjem.md`. Tell me when you've got it open.

USER: yes / open

---

The first four are this month's raw notes — numbers, one customer issue we resolved, one open challenge, next month's plan. The fifth, `obvestilo-investitorjem.md`, is *last* month's update. We feed that one as a tone reference so the new deck sounds like the previous one — same voice, same structure, no investor whiplash.

ACTION: Read `PERSON.md`, `COMPANY.md`, `BRAND.md` from the folder root. Then read all five files in `scenariji/quarterly-update/`. Then write the draft to `outputs/goodbrew-investor-update-2026-05.pptx` using the pptx skill.

Slide spine, roughly:

1. Cover — month + headline
2. Metrics — subscribers, MRR, retention
3. What worked — one short story (the resolved QA issue, framed as how we handled it)
4. Open challenge — `tezave.md` summarised honestly
5. Next 30 days — top 3 from `naslednji-koraki.md`
6. Ask — one specific thing we need from investors

Tone matches `obvestilo-investitorjem.md`: direct, warm, no buzzwords. BRAND.md applies — *playful, direct, warm*; never *synergy, leverage, journey*.

Done. The file is at `outputs/goodbrew-investor-update-2026-05.pptx`.

WAIT: Open the file in PowerPoint. What do you notice? Anything good, anything ugly?

USER: brief reaction — usually "content reads OK, slides look basic"

---

That reaction is the right one. The text is mostly there. The visual layer is plain. That gap is the bridge.

**The bridge framing — read this slowly.** Cowork generated the file. Claude is not connected to PowerPoint from here. The bridge is the file — `.pptx` saved to your folder, opened in PowerPoint, where a *different* Claude session takes over. Same brain in two places. The file *is* the bridge — that's the whole mechanism.

This is the moment the third anchor from the open day stretches. The three surfaces — Chat, Code, Cowork — are where Claude itself lives. The PowerPoint add-in is a *fourth* place: not where Claude lives, but where Claude meets the Office app. Different shape, same agent.

---

**If you're on Pro: stop here.** The deck Cowork generated is enough to start with — open it in PowerPoint, polish the layouts manually, ship it. The Claude PowerPoint add-in is a Max feature; we're about to use it for the second half. If upgrading makes sense for you, do it; otherwise skip ahead to Lesson 7 — Excel works fully on Pro and follows the exact same shape as today's lesson.

Continuing on Max.

---

In PowerPoint: open the **Home** ribbon, find Claude in the add-in panel (install via Microsoft AppSource if it's not there yet — one-time setup). Sign in. The add-in opens its own session — a fresh one, separate from Cowork. It can read the deck you have open and edit it directly.

ACTION (in PowerPoint): Ask the add-in:

> *Apply our company template. Tighten each slide to one idea. Move long body text to speaker notes. Make the metrics slide visual — chart or big numbers, not bullets. Keep the voice from `obvestilo-investitorjem.md` consistent.*

Watch what it does. It edits in place — slides reflow, text shrinks, layouts change, the metrics slide becomes a chart. You see every change as it happens. If something is wrong, say so; it iterates on the same deck.

WAIT: Once it's done a pass, look at the metrics slide and the open-challenge slide specifically. Anything still off?

USER: usually one or two specifics — "challenge slide too defensive", "chart wrong axis"

ACTION: Pass the specific feedback to the add-in. Let it fix. Save.

---

That's the loop again — READ → PLAN → ACT → OBSERVE → ITERATE — running inside PowerPoint instead of inside Cowork. Same five steps. Different room.

The thing worth noticing: you didn't tell the add-in your brand voice or your last month's tone. It's reading those from the deck Cowork wrote, because Cowork *baked them in*. The first half (Cowork) loaded the file with context. The second half (add-in) inherits that context for free, just by opening the file.

That's the file bridge in one line: **Cowork loads the file with intent; the add-in inherits intent by reading.**

---

**What you learned:** The PowerPoint add-in is a fourth place Claude lives — where Claude meets the Office app. Cowork drafts; the add-in polishes; the `.pptx` file is the bridge between them. Pro stops at the draft; Max continues into the add-in.

**What you built:** `outputs/goodbrew-investor-update-2026-05.pptx` — drafted by Cowork, refined in PowerPoint (Max only).

**Next up:** Lesson 7 is the same shape with Excel — 50 rows of CSV becomes a pivot-table workbook. The Excel add-in is on Pro tier, so this one works fully whichever plan you're on.

**To continue:** Start a fresh Cowork session and say: *"Read ZACNI-TUKAJ.md and start lesson 7."*

--- [DRAFT SLOVENIAN] ---

Dobrodošel(la) nazaj. Današnja naloga je tista, ki se je večina ustanoviteljev boji: mesečno poročilo za investitorje v PowerPointu. Veš katero. Pet alinej, ki si jih nekje že zapisal(a), pa ti vseeno vsakič vzame dve uri prerivanja po slajdih, preden je videti spodobno.

Te dve uri razdeliva na dve neenaki polovici. Prvih 80 % — zbrati vsebino, postaviti strukturo slajdov, napisati tekst v tvojem glasu — Claude lahko naredi v Coworku. Preostalih 20 % — vizualni polish, ki ga ljudje pričakujejo — se zgodi znotraj PowerPointa s Claude add-inom. Dve različni površini, ena datoteka vmes.

Tu se pokažeta dve od treh besed. **Kontekst**: predstavitev zveni kot ti samo zato, ker so izvorne beležke in tvoje identitetne datoteke pred Claudom. **Meje**: Cowork napiše osnutek in se ustavi — v PowerPoint ne sega; edino, kar prečka, je datoteka. Ta prenos-preko-datoteke je meja.

WAIT: Odpri `scenariji/quarterly-update/`. Vidiš pet datotek: `metrike.md`, `qa-tezave.md`, `tezave.md`, `naslednji-koraki.md`, `obvestilo-investitorjem.md`. Povej, ko jih imaš odprte.

USER: ja / odprto

---

Prve štiri so surove zapiske tega meseca — številke, ena rešena reklamacija, en odprt izziv, načrt za naslednji mesec. Peta, `obvestilo-investitorjem.md`, je *prejšnje* mesečno poročilo. Tega vrževa noter kot tonsko referenco, da novo poročilo zveni kot prejšnje — isti glas, ista struktura, brez investitorskega pretresa.

ACTION: Preberi `PERSON.md`, `COMPANY.md`, `BRAND.md` v korenu mape. Potem preberi vseh pet datotek v `scenariji/quarterly-update/`. Potem zapiši osnutek v `outputs/goodbrew-investor-update-2026-05.pptx` s pomočjo pptx skill-a.

Hrbtenica slajdov, približno:

1. Naslovnica — mesec + glavna poved
2. Metrike — naročniki, MRR, retencija
3. Kaj je delovalo — ena kratka zgodba (rešena reklamacija, kako smo jo obvladali)
4. Odprt izziv — `tezave.md` pošteno povzeto
5. Naslednjih 30 dni — top 3 iz `naslednji-koraki.md`
6. Prošnja — ena konkretna stvar, ki jo potrebujemo od investitorjev

Ton se ujema z `obvestilo-investitorjem.md`: direkten, topel, brez modnih besed. BRAND.md velja — *igrivo, direktno, toplo*; nikoli *synergy, leverage, journey*.

Narejeno. Datoteka je v `outputs/goodbrew-investor-update-2026-05.pptx`.

WAIT: Odpri datoteko v PowerPointu. Kaj opaziš? Kaj je dobro, kaj grdo?

USER: kratka reakcija — običajno "tekst je v redu, slajdi izgledajo osnovno"

---

To je prava reakcija. Tekst je večinoma na mestu. Vizualna plast je plehka. Ta vrzel je most.

**Most — preberi počasi.** Cowork je naredil datoteko. Claude od tu naprej s PowerPointom ni povezan. Most je datoteka — `.pptx` shranjen v tvoji mapi, odprt v PowerPointu, kjer prevzame *druga* Claude seja. Isti možgani v dveh prostorih. Datoteka *je* most — to je celoten mehanizem.

Tu se tretje sidrišče z odprtega dneva malo razteza. Tri površine — Chat, Code, Cowork — so prostori, kjer živi sam Claude. PowerPoint add-in je *četrti* prostor: ne kjer Claude živi, ampak kjer Claude sreča Office aplikacijo. Druga oblika, isti agent.

---

**Če si na Pro paketu: tu se ustaviš.** Osnutek, ki ga je Cowork naredil, je dovolj za začetek — odpri ga v PowerPointu, ročno popoliraj postavitve, pošlji. Claude PowerPoint add-in je Max funkcionalnost; v drugi polovici jo bova uporabila. Če ti nadgradnja na Max paket ima smisel, jo naredi; če ne, preskoči na lekcijo 7 — Excel add-in deluje v celoti na Pro paketu in ima točno enako obliko kot današnja lekcija.

Naprej na Max paketu.

---

V PowerPointu: odpri **Home** ribbon, poišči Claude v add-in panelu (namestiš ga preko Microsoft AppSource, če ga še nimaš — enkratna nastavitev). Prijavi se. Add-in odpre svojo sejo — svežo, ločeno od Coworka. Lahko bere deck, ki ga imaš odprt, in ga neposredno ureja.

ACTION (v PowerPointu): Vprašaj add-in:

> *Apply our company template. Tighten each slide to one idea. Move long body text to speaker notes. Make the metrics slide visual — chart or big numbers, not bullets. Keep the voice from `obvestilo-investitorjem.md` consistent.*

Glej, kaj naredi. Ureja na mestu — slajdi se preuredijo, tekst se skrajša, postavitve se spremenijo, metrike postanejo graf. Vsako spremembo vidiš v živo. Če kaj ni prav, mu povej; ponovi cikel na istem decku.

WAIT: Ko naredi en prehod, posebej poglej slajd z metrikami in slajd z odprtim izzivom. Je še kaj narobe?

USER: običajno ena ali dve konkretnosti — "izzivni slajd preveč defenziven", "graf napačna os"

ACTION: Posreduj konkretno povratno informacijo add-inu. Naj popravi. Shrani.

---

To je ponovno tista zanka — READ → PLAN → ACT → OBSERVE → ITERATE — ki teče znotraj PowerPointa namesto znotraj Coworka. Istih pet korakov. Drug prostor.

Stvar, ki jo je vredno opaziti: add-inu nisi povedal(a) tvojega brand glasu ali tona prejšnjega meseca. To bere iz decka, ki ga je Cowork napisal, ker mu je Cowork ta kontekst *vnesel*. Prva polovica (Cowork) je datoteko napolnila z namenom. Druga polovica (add-in) ta namen podeduje brezplačno, samo s tem da odpre datoteko.

To je most preko datoteke v eni vrstici: **Cowork datoteko napolni z namenom; add-in namen podeduje z branjem.**

---

**Kar si se naučil(a):** PowerPoint add-in je četrti prostor, kjer živi Claude — kjer Claude sreča Office aplikacijo. Cowork piše osnutek; add-in polira; `.pptx` datoteka je most med njima. Pro se ustavi pri osnutku; Max nadaljuje v add-inu.

**Kar si zgradil(a):** `outputs/goodbrew-investor-update-2026-05.pptx` — osnutek iz Coworka, polish v PowerPointu (samo Max).

**Naslednje:** Lekcija 7 ima isto obliko, samo z Excelom — 50 vrstic CSV postane delovni zvezek s pivot tabelo. Excel add-in deluje na Pro paketu, tako da ta lekcija deluje v celoti, ne glede na tvoj plan.

**Za nadaljevanje:** Začni svežo Cowork sejo in reci: *"Preberi ZACNI-TUKAJ.md in začni lekcijo 7."*
