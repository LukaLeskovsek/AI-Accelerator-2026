# Lekcija 7: Prodajne številke v Excel pivot tabelo

## Površina: COWORK + ADD-IN

--- canonical EN ---

Welcome back. Lesson 6 had a tier gate at the halfway mark — the PowerPoint plugin needs Max. This lesson does not. The Excel add-in works on Pro. If you're on Pro, you finish the whole thing today. Small relief after L6.

The shape is the same as L6, though. Cowork drafts the file. You open it in Excel. Claude *inside* Excel — separate session, runs locally as an add-in — keeps working. The bridge is the file. Same pattern, different native app.

WAIT: Pro or Max — either works. Ready?

USER: yes

---

The founder workflow we're solving today: you exported 50 rows of invoice data from Stripe. Subscriptions, gift packetes, three-month bundles. You need a monthly review — revenue by category, revenue by region, channel breakdown, a chart of the month-on-month trend. The kind of thing you used to spend two hours on, fighting pivot tables and cleaning up the chart axis.

The three words from the open day, on this task: your **kontekst** is the CSV and what a monthly review needs to show; the **meje** is that Cowork drafts the file and the add-in polishes it — Cowork doesn't touch Excel directly; the **limit** is scope — pivots, a chart, formatting, nothing fancier. Operational sales review: the work that has to happen every month whether you feel like it or not.

The plan: one Cowork prompt builds the workbook. One Excel session polishes it. Ten minutes total once you've done it twice.

---

ACTION: Read `scenariji/prodajne-stevilke.csv`. Confirm columns: `datum, stranka, znesek, kategorija, kanal, regija`. 50 rows spanning April–May 2026.

I have the data. Six columns, 50 invoices, two months. Exactly what a monthly Stripe export looks like.

ACTION: Use the xlsx skill. Generate `outputs/goodbrew-prodaja-2026-04.xlsx` with two sheets:
1. `data` — the raw 50 rows with header formatting and currency on `znesek`.
2. `pivot-summary` — a pre-built summary: total revenue, count of orders, revenue by `kategorija`, revenue by `regija`, revenue by `kanal`. Plain tables. Numbers, not pivots yet.

Done. The file is in your `outputs/` folder. Open it.

WAIT: Open `outputs/goodbrew-prodaja-2026-04.xlsx` in Excel. What do you see?

USER: describes the two sheets

---

Good. The data sheet is clean. The summary sheet is a starting point — numbers laid out, but not interactive. You can't slice it. You can't drag a region into the columns and watch it update. That's why we cross the bridge.

Same framing as L6. **Cowork is not connected to Excel from here.** The Cowork session built the file and stopped. Now we open Claude *inside* Excel — the add-in. Separate session, runs locally. It reads the workbook, writes formulas, builds pivots, draws charts. It's the same Claude in spirit, different surface in practice.

If you haven't installed the Excel add-in yet: Insert → Get Add-ins → search "Claude" → install. One-time. Sign in with your Anthropic account.

ACTION: Open the Claude pane in Excel. Point it at the `data` sheet.

WAIT: Add-in is open and you can see your data sheet?

USER: yes

---

Now we ask for three pivots and one chart. Plain prompt — Claude in Excel reads the active workbook automatically.

Try this:

> *"Use the data sheet. Build three pivot tables on a new sheet called `pivots`:
> 1. Revenue (sum of znesek) by kategorija, with month as columns.
> 2. Revenue by regija.
> 3. Revenue by kanal.
> Then on the same sheet, add a line chart showing total revenue per month — month on the x-axis, revenue on the y-axis."*

Watch what happens. Claude proposes the steps, you approve, it builds the pivots and the chart. If the chart axis is off, ask for the fix in plain words. If a category is missing, point at it. Same READ → PLAN → ACT → OBSERVE → ITERATE loop you've been running since lesson 1, just with a different toolset under it.

WAIT: Pivots and chart in place?

USER: yes / something needs fixing

---

One paragraph of honesty before we close.

The Excel add-in does not do macros. It does not do VBA. It does not do Data Tables (the what-if kind). If you ask, it'll refuse — politely, but firmly. What it does well: pivot tables, charts, conditional formatting, formulas, basic cleanup. Stay inside that lane and it's fast. Push outside and you'll hit the wall. That's fine — those edges are still you. Most monthly reviews never need them anyway.

---

Same shape as L6. Cowork drafts, native app polishes, the file is the bridge. You now have the pattern in two places — PowerPoint and Excel. The next time you face a Word doc, a PDF that needs a markup, or any other Office artefact, you know what to try first: build the rough version in Cowork, open it in the native app, let the add-in finish.

The monthly Stripe review just went from a two-hour chore to a ten-minute habit. Save the prompt above somewhere. Next month you change the date in the filename and run it again.

---

**What you learned:** The file-bridge pattern works for Excel exactly like it does for PowerPoint. Cowork builds the workbook from a CSV; the Excel add-in turns it into pivots and charts. The add-in is on Pro. Macros, VBA, and Data Tables are out of scope — pivots, charts, and formatting are in.

**What you built:** `outputs/goodbrew-prodaja-2026-04.xlsx` — data sheet, summary sheet, pivots sheet with three pivot tables and an MoM revenue chart.

**Next up:** Lesson 8 — enriching a list of leads from a CSV, and the third word: limit (a spend cap on bulk work).

**To continue:** Začni svežo Cowork sejo in reci: *"Preberi ZACNI-TUKAJ.md in začni lekcijo 8."*

--- [DRAFT SLOVENIAN] ---

Dobrodošel(la) nazaj. Lekcija 6 je imela tier-prepreko na polovici — PowerPoint plugin potrebuje Max. Ta lekcija je nima. Excel add-in dela na Pro. Če si na Pro, danes prideš do konca. Majhno olajšanje za L6.

Oblika je sicer ista kot v L6. Cowork pripravi datoteko. Ti jo odpreš v Excelu. Claude *znotraj* Excela — ločena seja, teče lokalno kot add-in — nadaljuje. Most je datoteka. Isti vzorec, drugačna domača aplikacija.

WAIT: Pro ali Max — oboje deluje. Pripravljen(a)?

USER: ja

---

Founderjev tok dela, ki ga danes rešujeva: izvozil(a) si 50 vrstic računov iz Stripe-a. Naročnine, gift-packeti, tri-mesečni bundli. Potrebuješ mesečni pregled — promet po kategorijah, promet po regijah, razrez po kanalih, graf trenda iz meseca v mesec. Stvar, za katero si prej porabil(a) dve uri, se boril(a) s pivot tabelami in čistil(a) os grafa.

Tri besede z odprtega dneva, na tej nalogi: tvoj **kontekst** je CSV in to, kaj mora mesečni pregled pokazati; **meje** so, da Cowork piše osnutek in add-in zgladi — Cowork se Excela ne dotika neposredno; **limit** je obseg — pivoti, graf, oblikovanje, nič bolj zapletenega. Operativni pregled prodaje: delo, ki se mora zgoditi vsak mesec, ne glede na to, ali se ti ljubi.

Načrt: en Cowork prompt zgradi workbook. Ena Excel seja zgladi. Skupaj deset minut, ko si to naredil(a) dvakrat.

---

ACTION: Preberi `scenariji/prodajne-stevilke.csv`. Potrdi stolpce: `datum, stranka, znesek, kategorija, kanal, regija`. 50 vrstic, april–maj 2026.

Imam podatke. Šest stolpcev, 50 računov, dva meseca. Točno to, kar izgleda kot mesečni Stripe izvoz.

ACTION: Uporabi xlsx skill. Ustvari `outputs/goodbrew-prodaja-2026-04.xlsx` z dvema listoma:
1. `data` — surovih 50 vrstic z oblikovano glavo in valuto na `znesek`.
2. `pivot-summary` — pripravljen povzetek: skupni promet, število naročil, promet po `kategorija`, promet po `regija`, promet po `kanal`. Navadne tabele. Številke, še ne pivoti.

Narejeno. Datoteka je v tvoji `outputs/` mapi. Odpri jo.

WAIT: Odpri `outputs/goodbrew-prodaja-2026-04.xlsx` v Excelu. Kaj vidiš?

USER: opiše oba lista

---

V redu. Data list je čist. Summary list je izhodišče — številke razporejene, a niso interaktivne. Ne moreš jih sekati. Ne moreš povleči regije v stolpce in gledati, kako se posodablja. Zato gremo čez most.

Ista uokvirjenost kot v L6. **Cowork od tu ni povezan z Excelom.** Cowork seja je zgradila datoteko in se ustavila. Zdaj odpreva Claude *znotraj* Excela — add-in. Ločena seja, teče lokalno. Bere workbook, piše formule, gradi pivote, riše grafe. Po duhu isti Claude, po površini drug.

Če Excel add-in še nisi namestil(a): Insert → Get Add-ins → poišči "Claude" → namesti. Enkraten korak. Prijavi se z Anthropic računom.

ACTION: Odpri Claude panel v Excelu. Usmeri ga na `data` list.

WAIT: Add-in je odprt in vidiš svoj data list?

USER: ja

---

Zdaj prosiva za tri pivote in en graf. Navaden prompt — Claude v Excelu samodejno bere aktiven workbook.

Poskusi to:

> *"Uporabi list `data`. Na novem listu `pivots` zgradi tri pivot tabele:
> 1. Promet (vsota znesek) po kategorija, z mesecem v stolpcih.
> 2. Promet po regija.
> 3. Promet po kanal.
> Na istem listu dodaj črtni graf, ki prikazuje skupni promet po mesecih — mesec na x-osi, promet na y-osi."*

Opazuj, kaj se zgodi. Claude predlaga korake, ti potrdiš, on zgradi pivote in graf. Če je os grafa narobe, popravek prosi z navadnimi besedami. Če manjka kategorija, pokaži nanjo. Ista zanka READ → PLAN → ACT → OBSERVE → ITERATE, ki jo poganjaš od lekcije 1, samo z drugim orodjem pod njo.

WAIT: Pivoti in graf so na svojem mestu?

USER: ja / nekaj je treba popraviti

---

En odstavek iskrenosti, preden zaključiva.

Excel add-in ne dela makrov. Ne dela VBA. Ne dela Data Tables (those what-if). Če vprašaš, bo zavrnil — vljudno, a odločno. Kar dobro dela: pivot tabele, grafe, pogojno oblikovanje, formule, osnovno čiščenje. Ostani v tem pasu in je hitro. Stopi ven in se zaletiš v steno. To je v redu — ti robovi so še vedno tvoji. Večina mesečnih pregledov jih tako ali tako ne potrebuje.

---

Ista oblika kot L6. Cowork piše osnutek, domača aplikacija polira, datoteka je most. Vzorec imaš zdaj na dveh mestih — PowerPoint in Excel. Naslednjič, ko boš pred Word dokumentom, PDF-jem za pripombe ali katerimkoli drugim Office artefaktom, veš, kaj poskusiti najprej: surovo različico zgradi v Coworku, odpri v domači aplikaciji, naj add-in zaključi.

Mesečni Stripe pregled je iz dvourne dolžnosti postal desetminutna navada. Zgornji prompt si shrani nekam. Naslednji mesec spremeniš datum v imenu datoteke in ga znova pognaš.

---

**Kar si se naučil(a):** Vzorec datoteka-kot-most v Excelu deluje enako kot v PowerPointu. Cowork zgradi workbook iz CSV-ja; Excel add-in ga spremeni v pivote in grafe. Add-in je na Pro. Makri, VBA in Data Tables so zunaj — pivoti, grafi in oblikovanje so znotraj.

**Kar si zgradil(a):** `outputs/goodbrew-prodaja-2026-04.xlsx` — list `data`, list `pivot-summary`, list `pivots` s tremi pivot tabelami in grafom prometa po mesecih.

**Naslednje:** Lekcija 8 — obogatitev seznama leadov iz CSV-ja in tretja beseda: limit (spend cap pri bulk delu).

**Za nadaljevanje:** Začni svežo Cowork sejo in reci: *"Preberi ZACNI-TUKAJ.md in začni lekcijo 8."*
