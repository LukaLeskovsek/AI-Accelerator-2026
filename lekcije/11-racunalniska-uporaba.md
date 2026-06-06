# Lekcija 11 (bonus): Računalniška uporaba — agent upravlja aplikacijo

## Površina: Cowork · računalniška uporaba (napredno / bonus)

--- canonical EN ---

This is a bonus. Lesson 10 was the real finish — the course is done, and the work is in your own company now. Come here only when you've done the ten and you're curious about the frontier you watched as **W8 at the open day**: an agent that takes over a whole app, triggered from a phone, and stops before the one irreversible click.

Be honest with yourself first: this is the *least reliable* thing in the whole course, it needs a **Max** plan, and you stay in the loop the entire time. We're not going to pretend it's magic. We're going to understand exactly when it earns its place — and when it doesn't.

WAIT: Do you have a **Max** plan, and do you actually have a repetitive task that lives in an app with **no connector** (an old ERP, a supplier portal, an intranet with no API)? If not, this lesson is worth reading but not running — say so and I'll keep it to the concept.

USER: yes Max + a no-connector task / no, just reading

---

Here's the one idea. Every other lesson reached its system through a **connector** — Gmail, Excel, a CRM. Computer use is what you reach for when there *is no* connector: the agent looks at the screen and clicks, the way you would. That's the whole reason it exists. If a connector exists, use the connector — it's faster and far more reliable. Computer use is the tool of last resort, not the first.

Two words from W8:
- **Računalniška uporaba** (computer use) — the agent reads the screen, moves the mouse, types. When there's no API, this is the only door.
- **Ukaz na daljavo** (dispatch) — you trigger the task from your phone; your own computer (awake, online) does the work and reports back.

And the rule that makes it safe is the same `meje` you've practised all course: **a hard stop before any irreversible action.** At the open day, the agent prepared a quotation in the ERP and *stopped before "Confirm."* That stop is not a nicety. It's the boundary.

---

ACTION: Before anything runs, we set up a **sandbox** — this is the whole safety story. Read these four out loud and confirm each:
1. A **clean browser profile** — no real logins, no saved passwords, no work accounts. If it's not logged in, nothing real can leak on your screen.
2. **No real credentials, no real data.** Use a throwaway/test account or a public sandbox site — never your live ERP, bank, or anything that moves money.
3. **"Ask before acting" on.** The agent proposes each step; you approve. It already pauses before irreversible/harmful actions — keep that on.
4. **A human checkpoint** named in advance: the one action you will *always* approve yourself (Submit, Confirm, Send, Pay).

WAIT: Confirm your sandbox is set up — clean profile, no real data, ask-before-acting on, checkpoint named. What's the one action you'll keep for yourself?

USER: sandbox ready + the checkpoint action

---

Now the small, safe try. We are **not** rebuilding W8 (that needs Docker + a local Odoo + phone pairing — an afternoon of setup). We're going to do the *reachable* version: one short web task in your clean profile, with a checkpoint.

Pick one of these (smallest first):
- **Read-only:** "Open [a public site / a test dashboard], find [one specific thing], screenshot it, and tell me what you found." No clicks that change anything — the safest possible start.
- **One careful action:** "Fill this throwaway form from the values in this file — and **stop before Submit** so I can check it." The Submit is your checkpoint.

ACTION: Help the learner write the task as three lines before they run it:
- **Kontekst** — which screen/app, what "done" looks like, what values to use.
- **Meje** — clean profile, ask-before-acting, and the named stop (e.g., "never click Submit").
- **Limit** — one page / one form / one record; if it takes more than N steps or gets confused, stop and show me.

WAIT: Run it yourself with Claude in Chrome (or Cowork computer use). Watch it screenshot → decide → click. Tell me where it hesitated or misclicked — that's the part worth talking about.

USER: what happened

---

Whatever happened, notice two things. First, **it's slower and less certain than a connector** — it guesses coordinates, fumbles dropdowns, sometimes re-reads the screen. That's normal and it's why this is the tool of last resort. Second, **the checkpoint did the real work**: the agent took you right up to the irreversible action and handed it back. More power, tighter boundary.

That's the lesson. Computer use doesn't change the framework — it *raises the stakes* on it. The agent that can drive your whole computer is exactly the one that most needs a sharp `meje` and a small `limit`. Same three lines, just less margin for error.

ACTION: Write `outputs/racunalniska-uporaba-zapis.md` — the three lines they used, what worked, what flaked, and one task in their real business where computer use would genuinely beat a connector (i.e., a screen with no API). If they can't name one, write that down too — that's a useful finding: most of their work is better served by connectors.

---

**What you learned:** Computer use (and remote dispatch) is the frontier — real, but the least reliable and most guarded capability. Use it only when no connector exists, always in a sandbox, always with a human checkpoint before the irreversible action. The framework doesn't change: kontekst, meje, limit — with less margin.

**What you built:** `outputs/racunalniska-uporaba-zapis.md`, and a small, supervised computer-use run in a clean profile.

**To continue:** Tečaj je zdaj res končan. Eno opravilo, ta teden — in to redko potrebuje računalniško uporabo. Connector najprej; zaslon šele, ko ni druge poti.

--- [DRAFT SLOVENIAN] ---

To je bonus. Lekcija 10 je bila pravi zaključek — tečaj je končan in delo je zdaj v tvojem podjetju. Sem pridi šele, ko si naredil(a) deset lekcij in te zanima meja možnega, ki si jo gledal(a) kot **W8 na odprtem dnevu**: agent, ki prevzame cel program, sprožen s telefona, in se ustavi pred edinim nepovratnim klikom.

Najprej bodi iskren(a) do sebe: to je *najmanj zanesljiva* stvar v celem tečaju, zahteva **Max** paket in ti ostaneš v zanki ves čas. Ne bova se delala, da je čarovnija. Razumela bova natanko, kdaj si zasluži svoje mesto — in kdaj ne.

WAIT: Imaš **Max** paket in dejansko ponavljajoče opravilo v programu **brez connectorja** (star ERP, portal dobavitelja, intranet brez API-ja)? Če ne, je lekcija vredna branja, ne pa poganjanja — povej in ostaneva pri konceptu.

USER: ja Max + opravilo brez connectorja / ne, samo berem

---

Ena sama ideja. Vsaka druga lekcija je do sistema prišla prek **connectorja** — Gmail, Excel, CRM. Računalniška uporaba je tisto, po čemer posežeš, ko connectorja *ni*: agent gleda zaslon in klika, tako kot ti. To je razlog, da obstaja. Če connector obstaja, uporabi connector — hitrejši in veliko bolj zanesljiv je. Računalniška uporaba je skrajna možnost, ne prva.

Dve besedi iz W8:
- **Računalniška uporaba** — agent bere zaslon, premika miško, tipka. Ko ni API-ja, so to edina vrata.
- **Ukaz na daljavo (dispatch)** — opravilo sprožiš s telefona; tvoj računalnik (buden, online) opravi delo in javi nazaj.

In pravilo, ki to naredi varno, je ista **meja**, ki si jo vadil(a) cel tečaj: **trden stop pred vsakim nepovratnim dejanjem.** Na odprtem dnevu je agent pripravil ponudbo v ERP in se *ustavil pred "Confirm."* Ta stop ni vljudnost. Je meja.

---

ACTION: Preden karkoli teče, postaviva **peskovnik** — to je celotna varnostna zgodba. Preberi teh štiri naglas in potrdi vsako:
1. **Čist profil brskalnika** — nobenih pravih prijav, gesel, službenih računov. Če ni prijavljeno, nič resničnega ne more uiti z zaslona.
2. **Brez pravih poverilnic, brez pravih podatkov.** Uporabi testni račun ali javni sandbox — nikoli živega ERP-ja, banke ali česarkoli, kar premika denar.
3. **"Vprašaj pred dejanjem" vključeno.** Agent predlaga vsak korak; ti potrdiš. Pred nepovratnimi dejanji se že ustavi — pusti to vključeno.
4. **Vnaprej določen checkpoint** — eno dejanje, ki ga boš *vedno* potrdil(a) sam(a) (Submit, Confirm, Pošlji, Plačaj).

WAIT: Potrdi, da je peskovnik nastavljen — čist profil, brez pravih podatkov, vprašaj-pred-dejanjem vključeno, checkpoint določen. Katero dejanje obdržiš zase?

USER: peskovnik pripravljen + checkpoint dejanje

---

Zdaj majhen, varen poskus. **Ne** gradiva W8 znova (to zahteva Docker + lokalni Odoo + sparjanje telefona — popoldne nastavljanja). Naredila bova *dosegljivo* različico: eno kratko spletno opravilo v tvojem čistem profilu, s checkpointom.

Izberi eno (najmanjše najprej):
- **Samo branje:** "Odpri [javno stran / testni dashboard], poišči [eno določeno stvar], naredi posnetek zaslona in mi povej, kaj si našel." Brez klikov, ki kaj spremenijo — najvarnejši možen začetek.
- **Eno previdno dejanje:** "Izpolni ta testni obrazec iz vrednosti v tej datoteki — in **ustavi se pred Submit**, da preverim." Submit je tvoj checkpoint.

ACTION: Pomagaj učencu(ki) zapisati opravilo kot tri vrstice, preden ga požene:
- **Kontekst** — kateri zaslon/program, kako izgleda "končano", katere vrednosti uporabiti.
- **Meje** — čist profil, vprašaj-pred-dejanjem in določen stop (npr. "nikoli ne klikni Submit").
- **Limit** — ena stran / en obrazec / en zapis; če traja več kot N korakov ali se zmede, ustavi se in pokaži.

WAIT: Poženi sam(a) s Claude v Chromu (ali Cowork računalniško uporabo). Glej, kako naredi posnetek → odloči → klikne. Povej, kje je okleval ali zgrešil — to je del, vreden pogovora.

USER: kaj se je zgodilo

---

Karkoli se je zgodilo, opazi dve stvari. Prvič, **počasnejši in manj zanesljiv je kot connector** — ugiba koordinate, lovi spustne menije, včasih znova bere zaslon. To je normalno in zato je skrajna možnost. Drugič, **pravo delo je opravil checkpoint**: agent te je pripeljal tik do nepovratnega dejanja in ti ga vrnil. Več moči, ožja meja.

To je lekcija. Računalniška uporaba ne spremeni frameworka — *dvigne vložek* nanj. Agent, ki lahko vozi cel tvoj računalnik, je natanko tisti, ki najbolj potrebuje ostro **mejo** in majhen **limit**. Iste tri vrstice, le manj prostora za napako.

ACTION: Zapiši `outputs/racunalniska-uporaba-zapis.md` — tri vrstice, ki ste jih uporabili, kaj je delalo, kaj je zataknilo, in eno opravilo v njegovem resničnem podjetju, kjer bi računalniška uporaba res prekosila connector (tj. zaslon brez API-ja). Če ne najde nobenega, zapiši tudi to — to je koristna ugotovitev: večina dela je bolje postrežena s connectorji.

---

**Kar si se naučil(a):** Računalniška uporaba (in ukaz na daljavo) je meja možnega — resnična, a najmanj zanesljiva in najbolj varovana zmožnost. Uporabi jo le, ko connectorja ni, vedno v peskovniku, vedno s človeškim checkpointom pred nepovratnim dejanjem. Framework se ne spremeni: kontekst, meje, limit — z manj prostora za napako.

**Kar si zgradil(a):** `outputs/racunalniska-uporaba-zapis.md` in majhen, nadzorovan tek računalniške uporabe v čistem profilu.

**Za nadaljevanje:** Tečaj je zdaj res končan. Eno opravilo, ta teden — in to redko potrebuje računalniško uporabo. Connector najprej; zaslon šele, ko ni druge poti.
