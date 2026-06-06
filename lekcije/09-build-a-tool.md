# Lekcija 9: Zgradi delujoče interno orodje

## Površina: CODE

--- canonical EN ---

Welcome back. This is the one where you build something you can click.

Until now you've worked in Cowork — files and folders. This lesson is the third surface: **Code**. Where Cowork organises and drafts, Code *builds* — it writes real files in a folder and you end up with a working thing. Today: a sales dashboard. A single HTML page that reads your sales CSV and shows totals, a breakdown by product and region, and a weekly trend chart. You open it in a browser. It works.

The framework word in focus today is **meje** — but you'll feel all three. Your **kontekst** is the sales data plus your brand. Your **meje** is the working directory: everything the agent builds happens in one folder, nowhere else. And the **operating mode** — assisted, supervised, scheduled — is how closely you watch it run. Today: supervised.

WAIT: Ready to build? You'll need the Code surface open in Claude Desktop.

USER: yes

---

The founder workflow: every Monday you want last week's sales — by product, by region, a trend line. The data sits in a POS export. Building this in PowerBI is two weeks of consulting you won't pay for. So instead you build a small tool, once, and reuse it every week.

The plan: three short iterations. Ugly-but-working first, then brand colours and a chart, then a clean layout. You approve each step. That's supervised mode — you're not walking away yet, because you're learning what the agent does.

---

ACTION: Confirm the working directory. We'll build inside a new folder `dashboard/` in this walkalong folder, so everything the tool creates is in one place. Read `scenariji/prodaja-dashboard/prodaja.csv` and confirm the columns: `datum, izdelek, kategorija, kolicina, znesek, regija, kanal`. 50 rows, April–May.

I have the data. Seven columns, 50 sales rows. The working directory is `dashboard/` — empty for now, so you'll watch files appear.

---

**Iteration 1 — skeleton.** Paste this:

> *"V mapi `dashboard/` zgradi `index.html`, ki prebere `../scenariji/prodaja-dashboard/prodaja.csv` in prikaže: skupni promet, število naročil, promet po izdelku (tabela) in promet po regiji (tabela). Vanilla HTML/CSS/JS, brez zunanjih knjižnic, da se odpre z dvoklikom. Naj bo grdo ampak delujoče."*

Watch the file appear in `dashboard/`. Open it: double-click `index.html`, or right-click → open in browser.

WAIT: Does it open and show the numbers?

USER: yes / it's blank / error

If it's blank: the CSV path is the usual culprit. Tell the agent *"stran je prazna, preveri pot do CSV in nalaganje"* and it'll fix it. Same READ → PLAN → ACT → OBSERVE → ITERATE loop — you observed, now it iterates.

---

**Iteration 2 — brand + chart.** If you built `BRAND.md` in lesson 2, the agent can use your colours. Paste:

> *"Dodaj barve iz `../BRAND.md` (če obstaja, sicer nevtralna paleta). Dodaj črtni graf skupnega prometa po tednih — uporabi canvas ali inline SVG, brez zunanjih knjižnic. Mesec/teden na x-osi, promet na y-osi."*

Refresh the browser (Cmd+R). The chart appears.

WAIT: Chart showing, colours applied?

USER: yes / chart axis is off

If the axis is off, say so in plain words — *"y-os naj se začne pri 0"* — and it fixes it. You don't touch the code. You describe the result you want.

---

**Iteration 3 — polish.** Paste:

> *"Naredi postavitev čisto in responsive: številke na vrhu kot kartice, tabeli pod njimi, graf na dnu. Naj bo berljivo na telefonu. Dodaj še tabelo top 10 strank po prometu, če podatki dopuščajo."*

Refresh once more.

WAIT: Looks clean on a normal window and a narrow one?

USER: yes

---

One paragraph of honesty before we close.

This is a real tool, but it's a *simple* one — a static page that reads one CSV. It doesn't update live, it doesn't connect to your POS, it doesn't handle a million rows. That's fine: most internal tools a founder needs are exactly this size. When you outgrow it, that's a signal to bring in real engineering — not a failure of the approach. The point today is that the gap between "I wish I had a dashboard" and "I have a dashboard" just went from two weeks to fifteen minutes.

And the **operating mode**: today you ran it *supervised* — approving each step. Once you trust the pattern, you change one line of the prompt — *"vsak ponedeljek ob 6h osveži dashboard z novim CSV"* — and it runs *scheduled*, without you. Assisted (you're typing alongside), supervised (you approve steps), scheduled (it runs alone). Pick the mode by how much the task can go wrong, not by how lazy you feel.

---

**What you learned:** Code is the surface where Claude *builds* — real files in a working directory. The working directory is the boundary (**meje**): everything happens in one folder. The operating mode — assisted / supervised / scheduled — is how closely you watch. You built supervised today.

**What you built:** `dashboard/index.html` — a working sales dashboard you open in a browser. Change the CSV next week and refresh.

**Next up:** Lesson 10 is the close — you write your own three lines (kontekst, meje, limit) for one real task in your company.

**To continue:** Start a fresh Cowork session and say: *"Read ZACNI-TUKAJ.md and start lesson 10."*

--- [DRAFT SLOVENIAN] ---

Dobrodošel(la) nazaj. To je tista lekcija, kjer zgradiš nekaj, kar lahko klikneš.

Doslej si delal(a) v Coworku — datoteke in mape. Ta lekcija je tretja površina: **Code**. Kjer Cowork ureja in piše osnutke, Code *gradi* — piše prave datoteke v mapo in na koncu imaš delujočo stvar. Danes: prodajni dashboard. Ena HTML stran, ki prebere tvoj prodajni CSV in prikaže skupne vrednosti, razrez po izdelku in regiji ter graf trenda po tednih. Odpreš jo v brskalniku. Deluje.

Beseda dneva je **meje** — a začutil(a) boš vse tri. Tvoj **kontekst** so prodajni podatki in tvoja znamka. Tvoje **meje** so delovna mapa: vse, kar agent zgradi, se zgodi v eni mapi, nikjer drugje. In **operativni način** — assisted, supervised, scheduled — je to, kako pozorno gledaš, ko teče. Danes: supervised.

WAIT: Pripravljen(a) graditi? Potrebuješ odprto Code površino v Claude Desktopu.

USER: ja

---

Founderjev tok dela: vsak ponedeljek bi rad videl prodajo prejšnjega tedna — po izdelku, po regiji, črto trenda. Podatki so v POS izvozu. Zgraditi to v PowerBI-ju je dva tedna konzultacij, ki jih ne boš plačal(a). Zato namesto tega zgradiš majhno orodje, enkrat, in ga uporabljaš vsak teden.

Načrt: tri kratke iteracije. Najprej grdo-a-delujoče, nato barve znamke in graf, nato čista postavitev. Vsak korak potrdiš. To je supervised način — še ne odhajaš stran, ker se učiš, kaj agent dela.

---

ACTION: Potrdi delovno mapo. Gradila bova v novi mapi `dashboard/` v tej tečajni mapi, da je vse, kar orodje ustvari, na enem mestu. Preberi `scenariji/prodaja-dashboard/prodaja.csv` in potrdi stolpce: `datum, izdelek, kategorija, kolicina, znesek, regija, kanal`. 50 vrstic, april–maj.

Imam podatke. Sedem stolpcev, 50 prodajnih vrstic. Delovna mapa je `dashboard/` — zaenkrat prazna, da gledaš, kako datoteke nastajajo.

---

**Iteracija 1 — skelet.** Prilepi to:

> *"V mapi `dashboard/` zgradi `index.html`, ki prebere `../scenariji/prodaja-dashboard/prodaja.csv` in prikaže: skupni promet, število naročil, promet po izdelku (tabela) in promet po regiji (tabela). Vanilla HTML/CSS/JS, brez zunanjih knjižnic, da se odpre z dvoklikom. Naj bo grdo ampak delujoče."*

Glej, kako datoteka nastane v `dashboard/`. Odpri jo: dvoklik na `index.html` ali desni klik → odpri v brskalniku.

WAIT: Se odpre in prikaže številke?

USER: ja / prazna je / napaka

Če je prazna: pot do CSV je običajni krivec. Reci agentu *"stran je prazna, preveri pot do CSV in nalaganje"* in popravi. Ista zanka READ → PLAN → ACT → OBSERVE → ITERATE — ti si opazil(a), zdaj on popravi.

---

**Iteracija 2 — znamka + graf.** Če si v lekciji 2 zgradil(a) `BRAND.md`, lahko agent uporabi tvoje barve. Prilepi:

> *"Dodaj barve iz `../BRAND.md` (če obstaja, sicer nevtralna paleta). Dodaj črtni graf skupnega prometa po tednih — uporabi canvas ali inline SVG, brez zunanjih knjižnic. Mesec/teden na x-osi, promet na y-osi."*

Osveži brskalnik (Cmd+R). Graf se pojavi.

WAIT: Graf je viden, barve nanesene?

USER: ja / os grafa je narobe

Če je os narobe, povej z navadnimi besedami — *"y-os naj se začne pri 0"* — in popravi. Kode se ne dotikaš. Opišeš rezultat, ki ga želiš.

---

**Iteracija 3 — polish.** Prilepi:

> *"Naredi postavitev čisto in responsive: številke na vrhu kot kartice, tabeli pod njimi, graf na dnu. Naj bo berljivo na telefonu. Dodaj še tabelo top 10 strank po prometu, če podatki dopuščajo."*

Še enkrat osveži.

WAIT: Izgleda čisto na normalnem oknu in na ozkem?

USER: ja

---

En odstavek iskrenosti, preden zaključiva.

To je pravo orodje, a *preprosto* — statična stran, ki prebere en CSV. Ne posodablja se v živo, ne povezuje se s tvojim POS-om, ne obvlada milijona vrstic. To je v redu: večina internih orodij, ki jih founder potrebuje, je točno te velikosti. Ko ga prerasteš, je to signal, da vključiš pravo inženirstvo — ne neuspeh pristopa. Bistvo danes je, da se je razdalja med "želim si dashboard" in "imam dashboard" skrčila z dveh tednov na petnajst minut.

In **operativni način**: danes si tekel(a) *supervised* — potrjeval(a) vsak korak. Ko vzorcu zaupaš, spremeniš eno vrstico prompta — *"vsak ponedeljek ob 6h osveži dashboard z novim CSV"* — in teče *scheduled*, brez tebe. Assisted (tipkaš poleg), supervised (potrjuješ korake), scheduled (teče sam). Način izberi po tem, kako zelo gre lahko narobe, ne po tem, kako se ti ljubi.

---

**Kar si se naučil(a):** Code je površina, kjer Claude *gradi* — prave datoteke v delovni mapi. Delovna mapa je meja (**meje**): vse se zgodi v eni mapi. Operativni način — assisted / supervised / scheduled — je to, kako pozorno gledaš. Danes si gradil(a) supervised.

**Kar si zgradil(a):** `dashboard/index.html` — delujoč prodajni dashboard, ki ga odpreš v brskalniku. Naslednji teden zamenjaš CSV in osvežiš.

**Naslednje:** Lekcija 10 je zaključek — napišeš svoje tri vrstice (kontekst, meje, limit) za eno pravo opravilo v svojem podjetju.

**Za nadaljevanje:** Začni svežo Cowork sejo in reci: *"Preberi ZACNI-TUKAJ.md in začni lekcijo 10."*
