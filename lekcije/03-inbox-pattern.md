# Lekcija 3: Inpacket vzorec

## Površina: COWORK

--- canonical EN ---

Welcome back. From this lesson on we are in **Cowork** — the second of the three Claude Desktop surfaces (Chat, Code, Cowork). The first two lessons happened in Chat: you talked, I replied, the only files we touched were `hello.md` and the three identity files.

Cowork is different. Cowork means Claude works on the files in your folder directly — reads them, moves them, writes new ones — while you watch. The agent is the same, the loop is the same (READ → PLAN → ACT → OBSERVE → ITERATE), but the surface gives it hands.

Today is the first lesson where you watch me do real, end-to-end work. Twelve files. Reading. Sorting. Logging. The sort of half-hour of admin you've been putting off.

This lesson is **meje** — the second word. The folder system (inbox → processed → outputs → reference) is a boundary: each folder has one job, and the agent works inside that structure instead of dumping everything in one place. Structure is how you keep an agent's reach predictable.

WAIT: Cowork session running and you can see your walkalong folder in Finder?

USER: yes

---

Before I start moving things around, the system. It's small. Four folders, each with one job:

```
your-folder/
├── inpacket/        ← stuff lands here, untouched
├── processed/    ← organised, sorted into subfolders
├── outputs/      ← things I produce (reports, logs, drafts)
└── reference/    ← stable docs you come back to
```

- **`inpacket/`** — landing strip. Anything new comes in here. No sorting yet. No decisions yet.
- **`processed/`** — sorted. Subfolders by kind: `processed/racuni/`, `processed/sporocila-strank/`, `processed/zapisniki/`. I create them as I go.
- **`outputs/`** — things I make for you. Reports, logs, drafts, generated decks, summaries.
- **`reference/`** — long-life docs. Stuff you'll re-read in three months: contracts, policies, playbooks.

Why four folders, not one? Because every folder has a single role. `inpacket/` is "not yet looked at." `processed/` is "sorted and findable." `outputs/` is "Claude made this." `reference/` is "I'll come back to this." Mixing them is how folders become graveyards. Keeping them separate is how this works for years instead of weeks.

WAIT: Make sense before I start? Anything you want to rename to fit how your head works — say it now and we set it that way.

USER: ok / rename

---

Right. Let's load the inpacket.

ACTION: Move all 12 files from `scenariji/inpacket-kaos/` into `inpacket/` at the walkalong root. Do not rename. Do not sort. Just move.

Done. Open `inpacket/`. Twelve files. Mixed bag — invoices, a contract, a customer Instagram message, screenshots-as-text, an investor meeting note, two `todo` lists, an `Untitled.txt`. The kind of pile that builds up on a real founder's desktop in two weeks.

This is the realistic starting point. Not a clean dataset. Not labelled. Just stuff.

WAIT: Glance at the folder. Anything you'd want me to handle differently from how a normal sort would go? (e.g. "the contract is sensitive — never log its contents.")

USER: brief reaction

---

Now I sort. I'll narrate as I go so you see the decisions, not just the result. Twelve files; I'll cluster the calls instead of spelling out every move.

ACTION: For each file in `inpacket/`, read enough to decide a destination, create the subfolder under `processed/` if it doesn't exist, move the file, and remember the reason for the log.

- `faktura-stria-april.md` — invoice from Stria Malt & Packaging. Goes to `processed/racuni/`. Note: 22% DDV, payment due 30 days — flag in log so you don't miss it.
- `faktura-prazenje-marec.txt` — March invoice from same supplier, already paid. `processed/racuni/`.
- `racun-marec-2026.md` — invoice you *issued* to Stria. Different direction of money. New subfolder: `processed/racuni-izdani/`. Splitting in/out matters for tax time.
- `kontrakt-poste-v2-final.md` — Pošta Slovenije delivery contract, signed, valid May 2026 to April 2027. Not an invoice — this lives a year. Goes to `reference/pogodbe/`. Reference, not processed. Stuff you re-read.
- `sestanek-investitor-26-3.md` — investor meeting note with Anže. `processed/zapisniki/`. (Could also go to `processed/investitorji/`; I'll group by document type — meeting note — over relationship. Tell me if you'd rather flip that.)
- `instagram-message-eva.txt` — happy customer DM, asking about referral. `processed/sporocila-strank/`. Lesson 5 will mine this folder for patterns.
- `nasvet-tomaz.txt` — neighbour's tip about Express77 courier. Operational note, not a customer message. `processed/operativa/`.
- `marketing-q1-povzetek.md` — your Q1 marketing summary. Long-life, you'll re-read it. `reference/marketing/`.
- `screenshot-stripe.txt` — Stripe April screenshot (placeholder for an image). Numbers you might want again: `processed/financno/`. Filename stays.
- `IMG_2814.txt` — also a Stripe screenshot, but the filename is useless. I'll move it to `processed/financno/` and rename to `stripe-april-prihodek.txt`. Renames I do go in the log so you can see them.
- `todo` — personal todo list, no extension, mixed work and home. `processed/osebno/`.
- `Untitled.txt` — looks like a todo list too, also mixed. Same: `processed/osebno/`. (I'm leaving the filenames alone except where the name actively misleads — `IMG_2814` did, `Untitled` is at least honest about being a scratch file.)

Done. `inpacket/` is empty. `processed/` has six subfolders. `reference/` has two.

WAIT: Two real questions. First — anything I sorted that you'd put somewhere different? Second — surprised by anything? (The contract going to `reference/` instead of `processed/` is the call I most often get pushback on.)

USER: reaction / corrections

---

If you want changes, say them now and I'll move things. Otherwise the log.

ACTION: If learner requested moves, perform them and note in the log. Then write `outputs/processing-log-2026-05-03.md` with: timestamp, list of all 12 source paths, destination paths, one-line reason per file, any renames called out, and a short "open questions" section (e.g. "should investor meetings group by relationship instead of type?"). Use today's date in the filename.

Done. Open `outputs/processing-log-2026-05-03.md`.

The log isn't paperwork. It's the audit trail. In two weeks when you ask "wait, where did I put the Pošta contract" you don't have to remember — you grep the log. It's also how you'll teach me to do this without you watching: the patterns in the log become the recipe.

WAIT: Open the log. Does it match what you saw me do?

USER: yes / question

---

Two more housekeeping moves so the empty folders aren't haunting you.

ACTION: Write `outputs/README.md` with one paragraph: *"This folder is where Claude writes things — processing logs, reports, drafts, generated `.pptx` and `.xlsx` files, customer-feedback synthesis. Filename convention is `<kind>-YYYY-MM-DD.md` so the newest sits at the bottom alphabetically and old ones don't get confused with current ones."*

ACTION: Write `reference/README.md` with one paragraph: *"This folder is for long-life documents you re-read: contracts, policies, brand playbooks, marketing summaries you reference quarterly. If you'll touch a file more than three months from now, it lives here. If it's a one-time invoice or message, it lives in `processed/`."*

Done. Both folders now explain themselves to future-you (and to future me, on a fresh session).

---

One thing before we close.

What I just did is twelve discrete decisions. Read file → decide kind → pick folder → move → log. I made them in front of you so you could push back. That's the manual mode of the inpacket pattern, and it works — but you'll notice the work has a shape. Same five steps every time, just different files.

In the next lesson we run this again on a fresh batch and turn the shape into a recipe — something that runs without me narrating each call. You don't need to remember how that works yet. Just notice, when you re-read the log, that twelve files produced twelve nearly-identical sequences of decisions. That's the seam.

---

**What you learned:** Cowork is the surface where the agent works on your files. The inpacket pattern is `inpacket/ → processed/ → outputs/ → reference/`, each folder with one role. Watching a manual run is the prerequisite for codifying it.

**What you built:** `inpacket/` (now empty), `processed/` with six subfolders, `outputs/processing-log-2026-05-03.md`, `outputs/README.md`, `reference/` with two subfolders, `reference/README.md`.

**Next up:** Lesson 4 codifies what we just did into a reusable recipe — so the next batch of files sorts itself with a single instruction.

**To continue:** Start a fresh Cowork session and say: *"Preberi ZACNI-TUKAJ.md in začni lekcijo 4."*

--- [DRAFT SLOVENIAN] ---

Dobrodošel(la) nazaj. Od te lekcije naprej sva v **Coworku** — drugi od treh Claude Desktop površin (Chat, Code, Cowork). Prvi dve lekciji sta tekli v Chatu: ti si pisal(a), jaz sem odgovarjal, edini datoteki, ki sva se jih dotaknila, so bile `hello.md` in tri identitetne datoteke.

Cowork je drugačen. Cowork pomeni, da Claude dela neposredno na datotekah v tvoji mapi — bere jih, premika, piše nove — medtem ko gledaš. Agent je isti, zanka je ista (READ → PLAN → ACT → OBSERVE → ITERATE), samo površina mu da roke.

Danes je prva lekcija, kjer me gledaš pri pravem, end-to-end delu. Dvanajst datotek. Branje. Sortiranje. Beleženje. Tista pol ura admina, ki jo odlagaš.

Ta lekcija je **meje** — druga beseda. Sistem map (inbox → processed → outputs → reference) je meja: vsaka mapa ima eno nalogo, agent dela znotraj te strukture, namesto da vse zmeče na en kup. Struktura je način, kako ohranjaš agentov doseg predvidljiv.

WAIT: Cowork seja teče in v Finderju vidiš svojo tečajno mapo?

USER: ja

---

Preden začnem premetavati, sistem. Majhen je. Štiri mape, vsaka ima eno nalogo:

```
tvoja-mapa/
├── inpacket/        ← stvari pristanejo tukaj, nedotaknjene
├── processed/    ← urejeno, razvrščeno po podmapah
├── outputs/      ← stvari, ki jih jaz proizvedem (poročila, logi, osnutki)
└── reference/    ← stabilni dokumenti, h katerim se vračaš
```

- **`inpacket/`** — pristajalna steza. Vse novo pride sem. Brez sortiranja. Brez odločitev.
- **`processed/`** — urejeno. Podmape po vrsti: `processed/racuni/`, `processed/sporocila-strank/`, `processed/zapisniki/`. Ustvarjam jih sproti.
- **`outputs/`** — stvari, ki jih naredim zate. Poročila, logi, osnutki, generirani decki, povzetki.
- **`reference/`** — dokumenti z dolgo življenjsko dobo. Stvari, ki jih boš znova bral(a) čez tri mesece: pogodbe, politike, playbooki.

Zakaj štiri mape, ne ena? Ker ima vsaka mapa eno vlogo. `inpacket/` je "še ni pogledano." `processed/` je "urejeno in najdljivo." `outputs/` je "Claude je naredil." `reference/` je "k temu se bom vračal(a)." Mešanje je pot, kako mape postanejo pokopališča. Ločevanje je pot, da to deluje leta in ne tedne.

WAIT: Razumeš, preden začnem? Bi kakšno mapo preimenoval(a), da bo bližje tvoji glavi — povej zdaj in nastaviva tako.

USER: ok / preimenuj

---

Prav. Naloživa inpacket.

ACTION: Premakni vseh 12 datotek iz `scenariji/inpacket-kaos/` v `inpacket/` v korenu tečajne mape. Brez preimenovanja. Brez sortiranja. Samo premakni.

Narejeno. Odpri `inpacket/`. Dvanajst datotek. Pisana paleta — fakture, pogodba, Instagram sporočilo stranke, screenshoti-kot-tekst, zapisnik investitorskega sestanka, dva `todo` seznama, `Untitled.txt`. Tisti kup, ki se v dveh tednih nabere na pravem ustanoviteljskem desktopu.

To je realistična izhodiščna točka. Ne čista množica podatkov. Brez oznak. Samo stvari.

WAIT: Preleti mapo. Bi kaj urejal drugače, kot bi šlo običajno sortiranje? (npr. "pogodba je občutljiva — nikoli ne logiraj njene vsebine.")

USER: kratka reakcija

---

Zdaj sortiram. Med delom govorim, da vidiš odločitve, ne samo rezultata. Dvanajst datotek; klice bom strnil, ne razlagal vsakega premika.

ACTION: Za vsako datoteko v `inpacket/` preberi toliko, da določiš destinacijo, ustvari podmapo pod `processed/`, če še ne obstaja, premakni datoteko in zapomni razlog za log.

- `faktura-stria-april.md` — faktura Pražarne Stria. V `processed/racuni/`. Opomba: 22% DDV, plačilni rok 30 dni — označim v logu, da ne pozabiš.
- `faktura-prazenje-marec.txt` — marčevska faktura istega dobavitelja, že plačana. `processed/racuni/`.
- `racun-marec-2026.md` — račun, ki si ga *ti izdal(a)* Strii. Druga smer denarja. Nova podmapa: `processed/racuni-izdani/`. Ločevanje vhodnih in izhodnih je pomembno za davke.
- `kontrakt-poste-v2-final.md` — pogodba o dostavi s Pošto, podpisana, veljavna maj 2026 do april 2027. Ni faktura — to živi leto dni. V `reference/pogodbe/`. Reference, ne processed. Stvari, ki jih bereš znova.
- `sestanek-investitor-26-3.md` — zapisnik sestanka z Anžetom. `processed/zapisniki/`. (Lahko bi bil tudi `processed/investitorji/`; grupiram po vrsti dokumenta — zapisnik — pred razmerjem. Reci, če bi raje obrnil.)
- `instagram-message-eva.txt` — zadovoljna stranka, sprašuje o priporočilu. `processed/sporocila-strank/`. Lekcija 5 bo iz te mape iskala vzorce.
- `nasvet-tomaz.txt` — sosedov namig o kurirju Express77. Operativna opomba, ne sporočilo stranke. `processed/operativa/`.
- `marketing-q1-povzetek.md` — tvoj Q1 marketing povzetek. Dolga življenjska doba, brala ga boš znova. `reference/marketing/`.
- `screenshot-stripe.txt` — Stripe screenshot za april (placeholder za sliko). Številke, ki jih morda spet rabiš: `processed/financno/`. Ime ostane.
- `IMG_2814.txt` — tudi Stripe screenshot, ampak ime datoteke je neuporabno. Premaknem v `processed/financno/` in preimenujem v `stripe-april-prihodek.txt`. Preimenovanja, ki jih naredim, gredo v log, da vidiš.
- `todo` — osebni todo seznam, brez končnice, pomešano službeno in domače. `processed/osebno/`.
- `Untitled.txt` — izgleda tudi kot todo, prav tako pomešano. Isto: `processed/osebno/`. (Imen ne spreminjam, razen kadar ime aktivno zavaja — `IMG_2814` je, `Untitled` je vsaj iskreno glede tega, da je čačka.)

Narejeno. `inpacket/` je prazen. `processed/` ima šest podmap. `reference/` dve.

WAIT: Dve pravi vprašanji. Prvo — kaj sem sortiral, kar bi ti dal(a) drugam? Drugo — te je kaj presenetilo? (Pogodba v `reference/` namesto `processed/` je odločitev, na katero največkrat dobim ugovor.)

USER: reakcija / popravki

---

Če želiš spremembe, povej zdaj in popravim. Sicer log.

ACTION: Če je učenec(ka) zahteval(a) premike, jih izvedi in zabeleži v log. Nato napiši `outputs/processing-log-2026-05-03.md` z: časovnim žigom, seznamom vseh 12 izvornih poti, ciljnih poti, eno vrstico razloga na datoteko, vsa preimenovanja izpostavljena, in kratek razdelek "odprta vprašanja" (npr. "naj investitorske sestanke grupiram po razmerju namesto po vrsti?"). V imenu datoteke uporabi današnji datum.

Narejeno. Odpri `outputs/processing-log-2026-05-03.md`.

Log ni papirologija. Je revizijska sled. Čez dva tedna, ko se vprašaš "počakaj, kam sem dal pogodbo s Pošto," ti ni treba ugibati — pogledaš v log. Je tudi način, kako me boš naučil(a) tega delati brez tvojega gledanja: vzorci v logu postanejo recept.

WAIT: Odpri log. Se ujema s tem, kar si videl(a)?

USER: ja / vprašanje

---

Še dve hišni opravili, da te prazne mape ne preganjajo.

ACTION: Napiši `outputs/README.md` z enim odstavkom: *"Ta mapa je tam, kjer Claude piše stvari — procesne loge, poročila, osnutke, generirane `.pptx` in `.xlsx` datoteke, sinteze povratnih informacij strank. Konvencija imen je `<vrsta>-YYYY-MM-DD.md`, da se nove sortirajo na dno abecedno in se stare ne zamenjajo s sedanjimi."*

ACTION: Napiši `reference/README.md` z enim odstavkom: *"Ta mapa je za dokumente z dolgo življenjsko dobo, ki jih bereš znova: pogodbe, politike, blagovne knjige, marketing povzetki, ki jih pregleduješ kvartalno. Če se boš datoteke dotaknil(a) čez več kot tri mesece, živi tukaj. Če gre za enkratno fakturo ali sporočilo, živi v `processed/`."*

Narejeno. Obe mapi se zdaj sami razložita prihodnji-tebi (in prihodnjemu meni v sveži seji).

---

Ena stvar pred zaključkom.

Kar sem pravkar naredil, je dvanajst diskretnih odločitev. Preberi datoteko → določi vrsto → izberi mapo → premakni → zabeleži. Naredil sem jih pred tabo, da si lahko ugovarjal(a). To je ročni način inpacket vzorca, in deluje — boš pa opazil(a), da ima delo obliko. Istih pet korakov vsakič, samo različne datoteke.

V naslednji lekciji to ponoviva na sveži šarži in obliko spremeniva v recept — nekaj, kar steče brez tega, da bi jaz pripovedoval vsak klic. Ni ti treba zdaj razumeti, kako to deluje. Samo opazi, ko boš znova bral(a) log, da je dvanajst datotek dalo dvanajst skoraj identičnih zaporedij odločitev. To je šiv.

---

**Kar si se naučil(a):** Cowork je površina, kjer agent dela na tvojih datotekah. Inpacket vzorec je `inpacket/ → processed/ → outputs/ → reference/`, vsaka mapa z eno vlogo. Gledanje ročnega teka je pogoj za to, da ga kasneje skodificirava.

**Kar si zgradil(a):** `inpacket/` (zdaj prazen), `processed/` s šestimi podmapami, `outputs/processing-log-2026-05-03.md`, `outputs/README.md`, `reference/` z dvema podmapama, `reference/README.md`.

**Naslednje:** Lekcija 4 to, kar sva pravkar naredila, skodificira v ponovljiv recept — tako da naslednja šarža datotek se uredi z eno samo navodilo.

**Za nadaljevanje:** Začni svežo Cowork sejo in reci: *"Preberi ZACNI-TUKAJ.md in začni lekcijo 4."*
