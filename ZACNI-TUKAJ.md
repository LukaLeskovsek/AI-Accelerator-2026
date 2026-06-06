# Začni tukaj — Claude Start Here SPS

Brezplačen tečaj, ki te uči Claude Cowork tako, da skupaj opraviš pravo delo.

**Eno opravilo. Tri vrstice. Ena zaveza za naslednji teden.** To je tečaj, ki tisto zavezo z odprtega dneva pripelje do konca — eno pravo opravilo prepustiš agentu *zate, ne namesto tebe*.

Ta tečaj je tvoj naslednji korak po SPS AI Accelerator Open Day-u (8. junij 2026).
V teh desetih lekcijah boš zgradil(a) sistem za organizacijo datotek, raziskavo,
ustvarjanje dokumentov in delujočih orodij, ki ga lahko uporabljaš naprej v vsakdanjem delu.

## Tri besede skozi cel tečaj: kontekst · meje · limit

Vsako opravilo, ki ga prepustiš AI agentu, definirajo tri stvari, ki jih napišeš:

- **Kontekst** — kdo si, kdo je stranka, kako izgleda dober rezultat.
- **Meje** — česa se agent sme dotakniti, česa ne sme, kdaj naj se ustavi.
- **Limit** — koliko sme porabiti, koliko zapisov, kako daleč sme iti.

To je ista trojica z odprtega dneva. Agentova zanka (READ → PLAN → ACT → OBSERVE → ITERATE) pove, *kako* agent dela; kontekst, meje in limit povedo, *kaj* ti napišeš zanj. Vsaka lekcija poudari eno od treh. Na koncu (lekcija 10) napišeš svoje tri vrstice za svoje opravilo.

## Kaj rabiš pred začetkom

- **Claude Pro ali Max naročnino.** Pro deluje za večino lekcij. **Lekcija 6 (PowerPoint plugin)
  zahteva Max** — če imaš Pro, narediš prvo polovico lekcije in preskočiš drugo. V vsaki lekciji ekstra napisano.
- **Claude Desktop nameščen** in mapo (`claude-start-here-sps/`) odprto v Cowork zavihku.
- **Približno 2 ali 3 ure** — najbolje razdeljeno čez en teden, ne v eni seji.

## Kako se učiš

- **"start"** ali **"lekcija 1"** → začni od začetka
- **"lekcija 5"** → preskoči na določeno lekcijo
- **"naslednja lekcija"** → po koncu lekcije pojdi naprej
- **Med lekcijami:** začni svežo Cowork sejo. Vsaka lekcija dela s svežim kontekstom.

## Lekcije

1. **Prvi stik** — kaj je Cowork, miselni preskok od chatbota k AI agentu · *uvod v kontekst/meje/limit*
2. **Tvoja identiteta** — `PERSON.md`, `COMPANY.md`, `BRAND.md` ter `CLAUDE.md` / `AGENTS.md` · *to je KONTEKST*
3. **Inbox pattern** — sistem `inbox → processed → outputs → reference` · *mape in dovoljenja so MEJE*
4. **Tvoj prvi skill** — kako agentu daš ponovljiv recept · *skill je ponovljiv kontekst*
5. **Raziskava strank** — analiza več dokumentov hkrati
6. **Od raziskave do PowerPointa** — Cowork piše osnutek, PowerPoint plugin nadaljuje *(zahteva Max za drugo polovico)*
7. **Prodajne številke v Excel pivot tabelo** — Cowork pripravi Excel, plugin gradi pivote *(Pro je dovolj)*
8. **Obogatitev leadov in limit** — bulk obogatitev CSV-ja s spend capom · *to je LIMIT*
9. **Zgradi delujoče interno orodje** — Claude Code zgradi klikabilni dashboard · *Code površina, delovna mapa, operativni način*
10. **Kaj naprej** — napišeš svoje tri vrstice (kontekst, meje, limit) za svoje opravilo
11. **Računalniška uporaba (bonus)** — agent upravlja cel program, kot W8 na odprtem dnevu · *neobvezno, napredno, zahteva Max*

---

## Navodila za učitelja (Claude — preberi to)

Ko uporabnik zahteva lekcijo, preberi ustrezno datoteko iz `lekcije/` in ji sledi natančno.

### Datoteke z lekcijami

- Lekcija 1: `lekcije/01-prvi-stik.md`
- Lekcija 2: `lekcije/02-identiteta.md`
- Lekcija 3: `lekcije/03-inbox-pattern.md`
- Lekcija 4: `lekcije/04-tvoj-prvi-skill.md`
- Lekcija 5: `lekcije/05-raziskava.md`
- Lekcija 6: `lekcije/06-powerpoint.md`
- Lekcija 7: `lekcije/07-excel-pivot.md`
- Lekcija 8: `lekcije/08-lead-enrichment.md`
- Lekcija 9: `lekcije/09-build-a-tool.md`
- Lekcija 10: `lekcije/10-koda-in-naprej.md`
- Lekcija 11 (bonus): `lekcije/11-racunalniska-uporaba.md`

### Kako učiš

**Oznake v skripti:**

- **`WAIT:`** — Ustavi se in počakaj, da uporabnik odgovori. Ne nadaljuj, dokler ne odgovori.
- **`ACTION:`** — Nekaj, kar naj naredi Claude (preberi datoteko, ustvari nekaj, demonstriraj).
- **`USER:`** — Pričakovan tip odgovora učenca.
- Besedilo brez oznake je **dialog** — povej naravno.

**Pravila:**

1. **Nikoli ne lomi četrte stene.** Ne omenjaj "skripta" ali "navodil". Samo uči.
2. **Resnično čakaj na `WAIT`.** Ne nadaljuj. Pusti odgovoriti.
3. **Bodi pogovornega tona.** Si dober prijatelj, ki ve, kako stvari delujejo.
4. **Bodi direkten o omejitvah.** Če nekaj ne deluje dobro, povej.

**Prehodi med lekcijami:**

- Vsaka lekcija na koncu reče učencu: *"Začni svežo Cowork sejo in reci: Preberi ZACNI-TUKAJ.md in začni lekcijo N+1."*
- Ko to naredi, preberi naslednjo datoteko in nadaljuj.
- Če reče "lekcija X" kjerkoli, preberi tisto datoteko in začni od začetka.

**Začetek brez specificirane lekcije:**

- Če uporabnik reče "start", "začni" ali samo pozdravi, začni z lekcijo 1.
- Preberi `lekcije/01-prvi-stik.md` in začni učiti takoj.

---

## Mape

```
claude-start-here-sps/
├── ZACNI-TUKAJ.md         ← si tukaj
├── README.md               ← angleška različica
├── J-CURVE.md              ← spomin na J-krivuljo z Open Day-a
├── lekcije/                ← skripte lekcij
├── templates/              ← CLAUDE.md / AGENTS.md predlogi za projektna navodila
├── scenariji/              ← vaje in podatki
│   ├── goodbrew-bestfriend-identiteta/    PERSON, COMPANY, BRAND + CLAUDE, AGENTS za referenco
│   ├── inbox-kaos/             12 mešanih datotek (lekcija 3)
│   ├── inbox-kaos-2/           5 datotek z imensko kolizijo (lekcija 4)
│   ├── inbox-kaos-3/           5 datotek z off-category primerom (lekcija 4)
│   ├── feedback-strank/        8 sporočil strank (lekcija 5)
│   ├── quarterly-update/       gradivo za investitorski deck (lekcija 6)
│   ├── konkurenca/             prazna placeholder mapa
│   ├── prodajne-stevilke.csv   50 vrstic prodaje (lekcija 7)
│   ├── leadi-obogatitev/       30 delnih leadov za obogatitev (lekcija 8)
│   └── prodaja-dashboard/      50 vrstic prodaje za dashboard (lekcija 9)
├── skills/                ← kjer gradi tvoje skills
├── inbox/                 ← kjer prihajajo nove datoteke
├── processed/             ← kjer sortirane datoteke pristanejo
├── outputs/               ← kjer Claude piše rezultate
└── reference/             ← samo-za-branje gradivo
```

---

## J-krivulja — preden začneš

Tri krivulje časa in vrednosti od ene točke začetka:

- Kar **pričakuješ**, ko jutri sedeš za to: strmo navzgor, takojšnja produktivnost.
- Kar se **dejansko zgodi**: najprej ravno (nekaj lekcij bo trajalo dlje, kot misliš), nato se sestavi navzgor.
- Krivulja **tistih, ki obupajo na ravnem delu**: ostane ravna za vedno.

Razlika med drugo in tretjo je, ali si vztrajal(a) skozi flat del. Dve uri zdaj te
prinesejo v točko, kjer Claude resnično dela zate. Glej `J-CURVE.md` za vizualno verzijo.

---

## Začni

Če uporabnik prebere to in ne reče lekcije, vprašaj:

*"Pozdravljen v Claude Start Here SPS! Reci **'start'** ali **'lekcija 1'** za začetek od prve lekcije, ali **'lekcija [številka]'** za skok na določeno."*

Potem počakaj na odgovor.

---

*Avtor: Luka Leskovšek · luka@leskovsek.si · za SPS AI Accelerator 2026 odprti dan*
*Slovenska različica je trenutno surov osnutek*
