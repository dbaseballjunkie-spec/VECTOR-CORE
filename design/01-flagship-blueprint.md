# THE FLAGSHIP BLUEPRINT
# **BIG RIG TYCOON**
### *Own the rig. Own the road.*

**Exact genre:** Idle Freight Tycoon — an idle/incremental business-management simulator with a
card-draft **load-board** decision layer and asynchronous **convoy** social competition.

**Platform:** Android + iOS native, plus a browser/PWA build (same core, WebGL-lite).
Portrait orientation, one thumb. Midcore-casual.

**Session spec:** 90 seconds minimum · 4–12 minutes typical · 20-minute deep session optional.
8–14 sessions per day is the *expected* behaviour, not the aspirational one.

**Install:** ≤ 130 MB core, ≤ 60 MB "truck stop" data pack. Fully playable offline for 72 hours.

**Store title (ASO):** *Big Rig Tycoon: Truck Empire* — carries the four highest-value keywords in
this niche (truck, tycoon, idle, empire) and is instantly legible at a glance in a crowded store search.

---

## 1. THE FANTASY

> **You get to run the trucking business that should have been yours — where the clock obeys you,
> the brokers pay, and the number at the end of the week is honest.**

The player is not driving. The player is **dispatching, owning and growing.** The truck rolling
across the map is *theirs*. This is the critical inversion: real life already gives him 11 hours
of driving a day; what it never gives him is **margin he can defend and respect he doesn't have to
beg for.** The game delivers exactly the thing that's missing and none of the thing that's already
ruining his back.

**Emotional promise (in the player's own register):**
*"This is my company. I decide what I haul and who I haul it for. Every Friday the settlement is
clean. And when I hire a driver, I get my life back."*

---

## 2. THE FIVE DESIGN PILLARS

| # | Pillar | What it means in practice |
|---|---|---|
| 1 | **Respect the trade** | Real economics, real geography, real equipment, real vocabulary. No jokes at the driver's expense. He is the boss, never the punchline. |
| 2 | **Your time is the resource** | 90-second sessions, no forced ads, no play-blocking timers, offline-first, interruption-proof. The game earns his minute; it never takes it. |
| 3 | **Decisions, not reflexes** | Deterministic strategy and card-draft decisions. Zero twitch, zero reaction tests, zero timed taps. Mastery = better judgment, which is how he already thinks about his job. |
| 4 | **The clock is the villain, and you can beat it** | Hours-of-service is the central tension of the early game and the central *relief* of the late game. The win condition of the fantasy is *getting out of the driver's seat*. |
| 5 | **Nobody hauls alone** | Async belonging with zero obligation: no voice chat, no scheduled raids, no social debt. A convoy you can leave for three days and come back to. |

---

## 3. THE CORE LOOP — THREE NESTED CYCLES

### LOOP 1 — THE MINUTE (90 sec – 4 min) · *the dock wait*
```
  ┌──────────────────────────────────────────────────────────────────────┐
  │  OPEN THE BOARD  →  DRAFT 1 OF 3–5 LOAD CARDS  →  NEGOTIATE          │
  │        ↓                    ↓                         ↓              │
  │  Choose your truck   Compare rate/mile,        THE HANDSHAKE:        │
  │  and driver          deadhead, weight,         drag to counter the   │
  │                      window, detention risk,   broker's rate. Win =  │
  │                      broker rating             more money; lose =    │
  │                                                he moves on.          │
  │        ↓                                                             │
  │  PLAN THE RUN  →  fuel stop · weigh station · split break · weather  │
  │        ↓                                                             │
  │  HAMMER DOWN  →  the rig rolls. Miles and dollars accrue in real time.│
  │        ↓                                                             │
  │  DELIVER  →  collect, rate the receiver, learn which customers lie.  │
  └──────────────────────────────────────────────────────────────────────┘
```
**One session = 3 to 8 meaningful decisions.** Same decision density as a hand of Balatro, same
emotional texture as a good hand of cards — but every card is a load, and the numbers are real.

### LOOP 2 — THE WEEK (5–20 min) · *the business*
Fuel hedging · maintenance windows and DOT inspections · insurance renewal · hiring and
firing · repair vs. replace · factoring vs. waiting 45 days · a lane going cold because a
mega-carrier undercut you · produce season opening in Florida · a blizzard closing I-80.
This is the **idle layer**: your trucks run your chosen lanes while you are away, and the money
accrues at `(rate/mile − cost/mile) × miles driven`.

> **The narrative of the mechanic:** he was out on the road for eleven hours and money piled up
> without him. That is the only idle mechanic that is literally true to his life.

### LOOP 3 — THE CAREER (weeks–months) · *the authority*
```
  LEASED-ON DRIVER  →  OWN AUTHORITY  →  2 TRUCKS  →  5  →  10  →  TERMINAL
        (MC number)      (prestige 1)     ...each "AUTHORITY RESET" widens the
                                          whole game and grants permanent Legacy perks
```
Each reset is a **"New Authority"** event: you sell the fleet, keep the Reputation, and start
bigger. The endgame is not a bigger number. It's **"Hang Up the Keys"** — deciding what your name
on the door means after you stop driving.

---

## 4. WHAT THE PLAYER LITERALLY DOES (the job description)

1. **Reads a board** every session and decides what to haul (the moment-to-moment game).
2. **Negotiates** with brokers via the Handshake gesture (the dopamine beat).
3. **Routes** the load against a 14-hour clock, fuel prices, weather and weigh stations.
4. **Assigns a driver** — including himself — and watches the run resolve.
5. **Solves a problem** once or twice a day: a breakdown, a lost receiver, a driver calling off,
   a DOT inspector at the scale, a broker who won't pay.
6. **Reads the settlement** every Friday and pays the bills.
7. **Invests**: a trailer, a second truck, a driver, an APU, a chrome kit, a new lane.
8. **Builds a name**: reputation, CSA score, convoy rank, the wall of trophies in the terminal.
9. **Makes one irreversible decision per chapter** — a lane, a partner, a hire, an exit.

---

## 5. SYSTEM DEEP DIVE

### 5.1 THE LOAD BOARD — the card layer *(the game's beating heart)*

Every load is a card. Cards have **real, legible attributes**, all drawn from the industry:

| Card attribute | In-game meaning |
|---|---|
| **Origin → Destination** | Real freight corridors with real lane economics |
| **Loaded miles / Deadhead miles** | Deadhead is subtracted at full cost — *the* skill check |
| **Weight** | Affects fuel burn, mountain grades, scale risk |
| **Commodity** | Produce, dry goods, steel, chemicals, livestock, auto, hazmat |
| **Rate & Rate/Mile** | The number he already argues about for a living |
| **Appointment window** | Tight windows = detention risk + clock pressure |
| **Receiver reputation** | ★ rating — *the player learns which *parody-branded* customers waste his day* |
| **Detention risk** | A visible probability, informed by the receiver's history (data-accurate: 39.3% of stops, 14 hrs/wk) |
| **Broker rating** | Pays fast, pays fair, or ghosts (only 29.3% of detention invoices get collected) |
| **Equipment required** | Van / reefer / flatbed / tanker / step-deck / hotshot |
| **Backhaul potential** | Chaining a return load is the core strategic skill |

**Deck-building is literal:**
- Your **"Book of Business"** is your deck. Every broker relationship, dedicated lane and
  contract you earn becomes a **permanent card** you can draw from.
- **Contracts** are persistent cards with lower rates and guaranteed volume. **Spot** is
  higher variance, higher pay. Building a deck that survives a soft market is the *entire
  long-term strategy* — and it mirrors the advice real owner-operators give each other.
- **Combos:** *Triangulation* (three loads forming a loop) · *Backhaul* (pair a headhaul and a
  return) · *Dedicated Lane* (repeat a lane three times for a rate bonus) · *Seasonal Spike*
  (haul produce out of Lakeland in April for a multiplier).
- **Rarity, but earned, never gambled:** Bronze → Iron → Silver → **Gold Seal** → **Black Book**
  contracts. No gacha. Rarity comes from reputation and relationships.

### 5.2 THE CLOCK — hours-of-service as the game's tension engine

- The 11-hour drive / 14-hour on-duty clock is a **visible, physical dial** on the HUD.
- Every load you accept consumes clock. Bad routes strand you. Running the clock hot increases
  **fatigue risk**, which increases repair, insurance and CSA consequences.
- **The mechanic's emotional arc:** in Chapter 1 the clock rules you. By Chapter 4 you have a
  second driver and the clock finally belongs to someone else. By Chapter 8 you haven't thought
  about it in weeks.
- **Never punitive:** no hard game-over. Fatigue produces cost and consequence, not a fail state.
  (A game about a man's real livelihood must not kill him for being tired.)

### 5.3 THE LANE MARKET — a living economy

- **Regional rate model** driven by real, documented cycles: Q1 freight recession → spring produce
  (FL/CA) → summer construction flatbed → fall harvest → Q4 retail peak.
- **Two economies:** *spot* (volatile, $1.88–2.13/mile per the data) vs *contract* (steady, lower).
- **Global modifiers:** diesel price, load-to-truck ratio, a mega-carrier entering a lane,
  a port strike, a hurricane rebuild.
- **Your decisions move your own market**: dominating a lane raises your rate there and degrades
  competitors' — the exact dynamic of spot-market capacity.
- **Real cost model on screen:** fuel $0.48/mi · truck payment $0.39 · maintenance $0.198 ·
  insurance $0.102. A permanent, expandable **"Where the Money Goes"** panel. Teaching is respect.

### 5.4 TRUCKS & EQUIPMENT

| Class | Role |
|---|---|
| **Day cab / box truck** | Chapter 1 starter; local runs; low cost, low ceiling |
| **Class 8 sleeper (used)** | The workhorse. Cheap, high mile, high maintenance |
| **Class 8 sleeper (new)** | Expensive, reliable, financing pressure |
| **Hotshot (pickup + gooseneck)** | Cheap entry to high-rate freight; the Gen Z / rookie on-ramp |
| **Specialty trailers** | Reefer, flatbed, step-deck, tanker, car hauler, livestock, end dump |

Each truck is a *character* with a service history, a personality of failure modes, and an odometer
that visibly climbs. Players will name their trucks. That is free retention.

**Upgrades:** APU, aero kit, tires, re-gearing, ELD, dashcam, fridge, bunk, CB, inverters.
Each has a **cost** and a **real-world benefit** (fuel, comfort, safety score, morale).

### 5.5 DRIVERS & THE TERMINAL — the "get out of the seat" system

Hiring is the game's central progression and its emotional payoff.

- **Named hires with arcs**, each drawn from Phase-B personas: **Renata** (reefer specialist),
  **Hector** (family authority / cross-border), **Six** (veteran; convoy ops), **Deej** (rookie;
  succession), **Hoss** (near retirement; legacy). Plus procedurally generated drivers with
  light personality traits and real-world quirks (a driver who refuses night runs; one who's
  great in the mountains; one who keeps failing inspections).
- **Traits are legible, not hidden:** *Steady*, *Speedster*, *Homebody*, *Fixer*, *Talker*.
- **The Spouse Dispatcher** hire (Phase B) boosts settlement efficiency — real small-fleet pattern.
- **The Terminal:** a visual home base that grows with you — a gravel lot → a rented yard → a
  shop with your name on it → your own fuel island. **The player's name is on the door and he can
  photograph it.**

### 5.6 SETTLEMENT FRIDAY — the game's single most important screen

Every in-game week ends with **the settlement sheet**:

```
  ═══════════════════════════════════════════════════════
   SETTLEMENT — WEEK 14          BLUE BONNET HAULING LLC
  ═══════════════════════════════════════════════════════
   Gross revenue                        $  19,480
   Fuel                                 −$  4,610
   Truck payment                        −$  1,760
   Insurance                            −$    455
   Maintenance & tires                  −$    980
   Factoring fee                        −$    312
   Permits, tolls, lumpers              −$    204
  ───────────────────────────────────────────────────────
   NET                                $  11,159      ✓
   Miles driven                            8,910
   Your cost per mile                    $  0.934
   ═══════════════════════════════════════════════════════
```
- **This is the emotional destination of the whole game.** It is the honest number that real life
  never delivers — and it's the asset he'll screenshot and post. **Every element is shareable as a
  clean image.** (This is the game's organic marketing engine: a settlement card posted to a
  trucker Facebook group is worth more than any ad buy.)
- **"Settlement Friday" becomes a weekly cultural ritual** in the community — the game creates a
  real weekly appointment that doesn't require an appointment.

### 5.7 REPUTATION, CSA & AUTHORITY — the progression currencies

| Currency | Earned by | Spent on |
|---|---|---|
| **Cash** | Hauling | Everything |
| **Reputation** | Clean runs, on-time delivery, well-rated receivers, contract completion | Unlocking premium brokers, dedicated lanes, hires |
| **Safety Score (CSA-like)** | Speed, fatigue, inspection outcomes, maintenance discipline | Insurance rates, authority tiers, hazmat endorsements |
| **Miles** | Driving | The literal scoreboard and prestige unit |
| **Legacy** | Prestige resets + completed chapter decisions | Permanent multipliers that survive every reset |

**Failure, handled with dignity:** run the business into the ground and you don't lose the game —
you **take a job at Meridian Logistics for a season**. You keep your handle, your truck knowledge
and your dog. You earn your way back out. (The 2023–25 freight recession destroyed ~88,000
authorities; a comeback arc is the most authentic story available, and it's far kinder than a
"Game Over" screen.)

### 5.8 THE CHROME SHOP — customisation *(the deep cosmetic economy)*

Truckers spend real money making their rigs *theirs*. So does the player.

**Categories:** paint & wraps (incl. period-correct 1970s schemes), chrome bumpers, grilles,
bull bars, stacks, air horns (with real horn *audio*, a delight), wheels, lights & cab markers,
mud flaps, hood ornaments, dash trinkets (bobblehead dog, a bullet casing, a St. Christopher
medal, a laminated photo of the kids), CB radios, gear-shift knobs, bunk interior, and —
critically — **your company logo and your name on the door**, created in a simple in-game paint shop.

**Why it matters:** it's the audience's primary real-world status language, it drives genuine
emotional investment, and it is **ethical monetisation** — you sell self-expression, not advantage.

### 5.9 COLLECTIONS & THE WALL

- **The Slang Codex** — a collectible encyclopedia of CB/highway culture: *bear in the air,
  chicken coop, bobtail, hammer down, four-wheeler, lot lizard, county mounty, full-grown bear.*
  **This is the bridge feature that makes the game work for non-truckers too:** they learn the
  language as a *reward*, while truckers get the pleasure of recognition. It doubles as an
  organic social asset ("what's your favourite entry?").
- **The Wall** — a visual trophy wall in the terminal: state plates from all 48, shipper coffee
  mugs, a scale ticket from every state, a framed first dollar, photos of each truck you've owned.
- **The Handshake Book** — every broker you've beaten in a negotiation, logged with the final rate.
  **Pure flex. Pure shareability.**
- **Endorsements** (see below) as the achievement/skill tree.

### 5.10 THE CONVOY — social, asynchronous, obligation-free

Design rules: **no voice chat, no scheduled events, no leaderboard pressure on the core loop.**

| Feature | How it works | Why it fits the cohort |
|---|---|---|
| **Your handle is your username** | You pick a CB handle at first launch; it's your identity everywhere | Instant identity, word-of-mouth currency: *"What's your handle?"* |
| **Convoys** (guilds) | Join 5–50 drivers; pool resources for a shared terminal upgrade | Belonging without a raid schedule |
| **Convoy Lane Push** | A shared weekly goal: the convoy commits loads to one corridor to hold the rate | Collective action — the fantasy of truckers organising (CB-organised stoppages are documented history) |
| **Handshake Board** | Post your best negotiation of the week; others react | Low-pressure boasting, the trade's favourite pastime |
| **Ghost Convoys** | Race a convoy-mate's recorded haul up the same lane (fully async, no live opponent) | Competition with zero scheduling |
| **Chat = the CB channel** | Text-only, 10-4 formatted, profanity filter, per-convoy channels | Feels native to the culture; safe and simple |
| **Mentorship** | Veterans get Reputation for teaching rookies | Turns the ageing workforce into the *heroes* of the game's story |

---

## 6. PROGRESSION: THE ENDORSEMENT TREE

The skill tree is the real CDL endorsement list. It is instantly legible to the player, requires
zero explanation, and gives the game an authentic, expandable progression spine.

```
 CORE  ───────────────────────────────────────────────────────────────
  Class A CDL  →  Double/Triple  →  Tanker  →  Hazmat  →  Tank+Hazmat
  Tanker      →  Oversize / Heavy Haul  →  Auto Transport
  Reefer cert →  Produce season access →  Food-grade (higher rates)
  Logbook mastery →  Split sleeper →  Recap hours →  The 34-hour reset

 BUSINESS ─────────────────────────────────────────────────────────────
  Own Authority  →  Broker relations  →  Direct shipper contracts
  Factoring      →  Net-30 discipline  →  Your own invoicing
  Lease-purchase →  Fleet financing   →  Terminal ownership

 LEGACY ───────────────────────────────────────────────────────────────
  2nd truck  →  5 trucks  →  10 trucks  →  Dispatcher  →  Terminal  →  Hang Up the Keys
```

Each endorsement unlocks **real freight** with **real constraints**: hazmat opens $3.25/mile loads
and closes more routes; oversize pays the most and requires escorts and permits; reefers carry the
detention penalty of their sector (56% of stops) but win the produce season.

---

## 7. STORY & PLOT: **"THE HAMMER DOWN SHOW"**

**Delivery mechanic:** the story arrives **as radio**. Every chapter unfolds in 60–90 second
episodes of an AM talk-radio program that plays while the game idles — with a written logbook
transcript for players who play muted (which is most of them, in a cab). It costs almost nothing
to produce, it's the exact medium this audience consumes for 11 hours a day, and it turns the
game's downtime into appointment listening.

**The frame:** *The Hammer Down Show* — a late-night AM call-in program hosted by **"Preacher,"
the mentor who taught you the trade** and who left you his truck, his spot on the board, and
$18,000 of debt. Every chapter, Preacher's show draws another driver's story out of the dark,
and the anthology slowly becomes a single plot.

### The eight chapters (one freight season each)

| # | Chapter | The turn |
|---|---|---|
| **1** | **"Borrowed Time"** *(Winter — slow season)* | You inherit a 2007 Freightliner, a CB handle and a note that says *"Don't haul cheap. Haul smart."* You learn the board, lose money, and learn what deadhead actually costs. |
| **2** | **"Detention"** *(Early spring)* | You sit nine hours at a receiver who won't take your call. You learn that billing detention and *collecting* it are different things. Your first act of defiance: refusing a load. |
| **3** | **"Produce"** *(Spring — FL/CA produce season)* | Reefer rates spike. You meet **Renata**, who out-earns you and won't let you forget it. You buy your first trailer and learn that the best money in trucking is seasonal and unforgiving. |
| **4** | **"Second Seat"** *(Summer — construction)* | **The pivot.** You hire your first driver. The clock finally stops ruling you. The moment the truck rolls without you in it is the emotional centre of the entire game. |
| **5** | **"The Shakedown"** *(Late summer)* | A broker ghosts you on a $14,000 invoice. You meet the antagonist properly: **MERIDIAN LOGISTICS** — a faceless mega-carrier buying up lanes, undercutting independents, and now buying the truck stop your father ate breakfast in. |
| **6** | **"Hard Winter"** *(Winter — recession)* | Rates collapse to $1.72/mile. A breakdown, a loan, a divorce in the convoy, a driver who quits on Christmas Eve. You find out whether you're a trucker or a business owner. Players may lose the company here — and take a season at Meridian to buy it back. |
| **7** | **"The Convoy"** *(Spring — the stand)* | With a dozen independent operators, you refuse a corridor. The CB channels light up. Preacher's last broadcast airs. **The plot's thesis:** independence is not the same thing as being alone. |
| **8** | **"Legacy"** *(Harvest — the endgame)* | You choose: sell to Meridian and take the money · franchise and put your name on fifty doors · or hand the keys to someone like **Deej**, who's twenty-four and has your old fire. Preacher's show signs off, and it's your handle on the air next. |

**Tone law:** the villain is never a driver. The villain is the system that eats drivers.
Truckers are the heroes, the rivals and the community. Brokers are individuals — some are snakes,
some are decent, and the game makes you learn which is which *by playing*.

**The ending that matters:** *Hang Up the Keys* is a real, playable, dignified ending for a man
who is, statistically, 56 years old and knows it. No game has ever given this audience a story
about how to be remembered. That is the thing they will tell each other about.

---

## 8. STYLE — THE LOOK AND THE SOUND

### Art direction: **"Sun-Faded Americana"**
- **2D/2.5D painted cards** with a warm dusk palette — amber, rust, sodium-vapour orange, asphalt
  grey, chrome. Think **1970s truck-stop sign painting** and gas-station paperback cover art,
  executed in clean modern UI.
- **The map** is a stylised, hand-painted U.S. with real interstate corridors and freight markets,
  not a satellite render. Beautiful at a glance, readable at 4.7 inches.
- **Typography:** bold, condensed, slab — a sign-painter's letterforms — but **large**. Body text
  ≥16sp, key numbers ≥24sp. **Readability in direct sunlight is a hard art requirement.**
- **No mascots. No wide-eyed cartoon face. No winks.** Dignity is the aesthetic.
- **Trucks are drawn with love** and are the visual reward of the whole game.

### Audio: **the radio is a feature, not a soundtrack**
- **Channels, not tracks:** *AM 1170 The Roadhouse* (classic country), *Channel 6* (classic rock),
  *The Talker* (sports & call-in), *The Preacher's Show* (story), *The Ranch Report* (weather &
  road conditions), *Static* (silence, for players who mute — and one of the most evocative
  sounds in the game).
- **Ambience:** jake brake, air dryer, gravel under tires, the *thunk* of a fifth wheel, a reefer
  unit cycling, rain on the roof, a cb squelch. **The sound design is the authenticity moat.**
- **Music:** original or licensed roots/country/blues instrumentals. Even 12 tracks reused across
  channels create the illusion of a real radio dial. **Radio is also where licensed music becomes a
  marketing asset** (a real artist's song as "this week on The Roadhouse").
- **Full mute-viability:** 100% of the game is playable silently, because that's how it will
  actually be played.

---

## 9. UX & ACCESSIBILITY SPEC (non-negotiable list)

| Requirement | Reason |
|---|---|
| **Zero forced interstitials** | 52% quit; the #1 complaint about every competitor in this niche |
| **Offline-first**; 72 hrs fully playable without signal | Dead zones are the norm, not the exception |
| **Interruption-proof**: kill the app mid-decision and return to the identical state | A CALL, A DOCK LIGHT, A SHIPPER — real life interrupts constantly |
| **Autosave on every single tap** | Drivers will lose a session to a bump in the road |
| **One-thumb, bottom-third controls** | Phone is in a windshield mount |
| **No timed decisions** (optional "pressure" toggle for advanced players) | Timed decisions are twitch, and twitch excludes this cohort |
| **Contrast and size verified in direct sunlight** | Test on a phone on a dashboard at noon. Ship what survives. |
| **Never signal with red/green alone** — arrows + the words PAYS / DOESN'T | ~8% of men have colour-vision deficiency; it's higher in this age band |
| **No login wall.** Play as guest; account is optional and never required for the core loop | Driver surveys name 2FA and forced password changes as top irritants |
| **Low-data mode**: playable on 200 MB/month | Data plans are watched closely |
| **Battery discipline**: < 5%/hour, no background GPS, no wake locks | It has to charge on a 12V socket while he sleeps |
| **Data-saver sync**: batch everything, sync on wifi when available | Rural coverage reality |
| **"Explain this number" tooltips everywhere** | He is numerate and will not tolerate a black box |

---

## 10. MONETISATION — THE RESPECT MODEL

**Governing rule:** *Sell self-expression and convenience. Never sell advantage, never sell
interruption, never sell escape from a timer we invented.*

| Product | Price | Notes |
|---|---|---|
| **Free core** | $0 | A complete, satisfying game is playable for free indefinitely. Generous. |
| **"GET YOUR OWN AUTHORITY"** | **$7.99 one-time** | The signature purchase — and the exact dream the audience has. Unlocks premium broker contracts, a bonus slot, the paint shop's premium templates, and *permanently* removes every optional ad prompt. **Framed as the real-world dream, priced like a sandwich.** |
| **Rewarded ads** | Free | **Optional only, capped at 6/day, never on the settlement or reward screens.** Framed in-world: *"Call in a favour to the broker — watch a 30s spot for a 5% rate bump."* Rewarded ads are accepted by ~85% of mobile gamers and 4.5× increase later IAP conversion. |
| **The Chrome Shop** | $1.99–14.99 | Cosmetics. Deep, desirable, and ethically clean. This is the LTV engine. |
| **Terminal Pass** | $4.99 / 8-week season | Aligned to the **real freight calendar** (Produce, Construction, Harvest, Peak). Cosmetic + convenience track. Never gates content the base game needs. |
| **Founder's Rig Pack** | $19.99 | One-time launch bundle for the first 90 days: a period-correct 1970s paint scheme, a chrome kit, a Preacher's-show audio archive, and a permanent 2% fuel discount. **Collector value, not power.** |

**Explicitly forbidden — written into the design doc:**
loot boxes · gacha · real-money or simulated-cash gambling · energy/lives that block play ·
timer-skips sold as relief · pay-to-win stat advantage · forced interstitials ·
ad on the settlement screen · notification spam · selling the player's anxiety back to him.

> This isn't only ethics — it's strategy. The audience is small, tight, loud, financially squeezed
> and deeply suspicious of being farmed. One viral "this game is a ripoff" post inside a trucker
> Facebook group of 400,000 people is an existential event. **Trust is the actual moat.**

---

## 11. ONBOARDING — THE FIRST FIVE MINUTES

1. **0:00 — "What's your handle?"** Pick one or accept a generated one. No account, no email.
2. **0:20 — You're at a kitchen table with a key, a title and a note.** Preacher's voice on the
   radio, 40 seconds. You own a 2007 Freightliner and $18,000 of debt. *No cutscene longer than 40s.*
3. **1:00 — You have three loads on the board.** One is obvious, one is a trap (the deadhead will
   eat the whole margin), one is a risk. **The tutorial is the decision.** No text walls.
4. **2:30 — The Handshake.** The first negotiation. A win here is the hook: you got $2.31/mile
   instead of $1.88. *"I beat the broker."* **That's the feeling that gets him back at 4:45 a.m.**
5. **3:30 — The truck rolls.** You watch 340 miles of I-40 tick by, and $784 accrue. You close the
   app. You're in the bunk.
6. **4:00 — The game is still running when you wake up**, and the dock light is finally green.

**Taught, not told:** no jargon is explained by a mascot. Every concept is introduced by
*asking the player to make the decision that requires it*, then explained the moment he wonders
about it. Tooltips, never lectures.

---

## 12. LIVE OPS — THE FREIGHT CALENDAR

The seasonal freight cycle is real, documented and *free content structure*: the entire industry
already lives on it, so the game's live-ops calendar requires no invention.

| Season | In-game event | Industry reality |
|---|---|---|
| **Jan–Feb** | *"Slow Season"* — hard-mode economy, cost-cutting challenges, survival scoring | Q1 freight recession; rate floors |
| **Mar–May** | *"Produce Rush"* — reefer vertical unlocks; FL/CA lanes spike; rate volatility | Produce season; reefer rates jump |
| **Jun–Aug** | *"Build Season"* — flatbed & oversize; hurricane relief contracts; tarping labour | Construction & disaster freight |
| **Sep–Oct** | *"Harvest"* — grain & livestock; ag lanes; long-run bonuses | Midwest harvest surge |
| **Nov–Dec** | *"Peak"* — retail volume; brutal detention; the biggest paychecks of the year | Q4 retail peak |
| Weekly | **Settlement Friday** — the shareable weekly number and a convoy leaderboard reset | Weekly settlements are the industry's real rhythm |
| Monthly | **The Hammer Down Show** audio episode + a new Anthology story | Radio as the live-ops narrative delivery |
| Per season | New **freight vertical**, new hire, new truck, new corridor, new chapter | Endless content from public data |

---

## 13. WHAT SUCCESS LOOKS LIKE (metrics & validation plan)

**Validation sequencing (this is the research phase of the product, not just the game):**
1. **30 in-person intercept interviews** at three truck stops (MS/TN/TX corridor, chosen for the
   highest BLS location quotients) with a $20 cash incentive — the same method used in the
   published trucker mental-health literature.
2. **Paper-prototype the load board** on index cards in a truck stop parking lot. If a driver
   doesn't argue with the card, the card is wrong.
3. **Web build of the load board alone** — one screen, no art, 60 seconds of play — tested with
   200 drivers recruited from trucker Facebook groups and r/Truckers. Measure: *do they want a
   second hand?*
4. **Soft launch geofenced** to Mississippi, Tennessee and Texas — the three states with the
   highest driver location quotients — plus Florida, using truck-stop-radius ad buys.
5. **The Facebook group test:** post a mocked-up Settlement Friday image. If drivers screenshot
   and argue about it, the core emotional beat is validated before a single engineer is hired.

**Target metrics:**
| Metric | Target | Why |
|---|---|---|
| D1 | ≥ 45% | Narrow, self-identified audience |
| D7 | ≥ 22% | Idle genre benchmark is high |
| Sessions/day | ≥ 4 | The design is built for the dock wait |
| Session length | 3–9 min median | Fits the window |
| Organic share rate | ≥ 8% of WAU share a settlement | The marketing engine |
| Convoy join rate | ≥ 35% of D7 players | Retention & network effect |
| Rewarded-ad participation | ≤ 15% of players watch any optional ad on a given day | Confirms the respect model is working |
| Review score | ≥ 4.5★ | The audience reviews honestly and loudly. This is the real KPI. |

---

## 14. RISKS & MITIGATIONS

| Risk | Mitigation |
|---|---|
| **"Only truckers will play it."** | The beachhead is 3.5M U.S. drivers *plus* the 40M+ Americans who play idle/tycoon sims. The **Slang Codex** makes the culture a reward rather than a barrier, and the fantasy — *own a small business that actually works* — is universal. Global expansion works too: truck-sim culture is huge in Europe, Brazil and India. |
| **Authenticity vs. accessibility.** | Every industry term is introduced *by decision*, never by lecture; jargon is a collectible, not a gate. |
| **Trademark / brand exposure.** | Parody shippers and receivers (*Vall-Mart, America-Cold, Kro-Grr, Titan Foods*). Actively license 2–3 real truck OEMs — OEMs market aggressively to this exact demographic and a game partnership is an easy, mutually beneficial sell. |
| **Monetisation backlash.** | The respect model + a public "no dark patterns" pledge + an in-game **Driver Council** (a player advisory board recruited from OOIDA/Facebook groups) with a public changelog written in the game's voice. |
| **Ethical risk of designing at a stressed, isolated audience.** | Hard prohibitions on gambling-adjacent mechanics, no social-comparison shaming, no loss-framed notifications, and mental-health resources surfaced respectfully in the game's "Coffee Shop" tab. Do not sell a lonely man the cure for loneliness; just don't make him lonelier. |
| **Idle games go stale.** | The card layer carries the moment-to-moment, and the freight calendar carries the year. 18+ months of content is already sitting in public FMCSA/ATRI data. |
| **The incumbent copies it.** | They've had 50M downloads and a 3.8★ rating for years. Their monetisation *is* their product. You'd have to rebuild the whole company to copy this. |

---

## 15. ONE-PAGE SUMMARY

> **BIG RIG TYCOON** is an **idle freight tycoon** for the 3.5M American truck drivers and the
> 40M+ people who play business sims.
>
> **The player** reads a load board, wins a handshake with a broker, routes a haul against a
> 14-hour clock, buys a truck, hires a driver, and reads a clean settlement statement every Friday.
> **Seventy-five percent of play happens in 90-second bursts** during a dock wait, with the money
> still accruing while the app is closed.
>
> **The genre answer is exact:** idle business-management sim + card-draft decision layer +
> asynchronous convoy competition — because card is the highest daily-playtime genre for men his
> age, strategy is the most age-stable motivation, idle is the only mechanic that literally mirrors
> his working life, and async social is the only way to give the loneliest workforce in America
> belonging without adding one more obligation to a man who already has too many.
>
> **The story** is delivered as an AM radio show: eight chapters, one per freight season, an
> anthology of drivers' stories that becomes a single fight against a faceless mega-carrier — and
> ends with the only question that matters to a 56-year-old man: *what happens to the name on
> the door?*
>
> **The moat** is that every competitor has built truck games that are wrong about trucks.
> This one is right.
