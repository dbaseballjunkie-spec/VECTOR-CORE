# STUDY 2 — Gaming Genre Vectors: Where This Cohort Actually Plays

**Input:** the five VECTOR-CORE traits from Study 1.
**Question:** What is the *most specific* genre or sub-genre of browser/mobile game that a
male, 50–58, married, veteran-household, South/Midwest, Android, time-rich/attention-poor,
stressed, proud, numerate, ad-hostile owner-operator will play — for months, not minutes?

Spoiler: **idle/incremental business tycoon, with a card-draft "load board" decision layer and
asynchronous "convoy" social competition.** Everything below is the argument for why that exact
combination is the answer and not, say, a truck driving sim or a slot machine.

---

## 1. The platform facts (non-negotiable constraints)

| Constraint | Evidence | Design consequence |
|---|---|---|
| **Mobile dominates** for 45–64s | 77% of 45–54s and 79% of 55–64s who game do so on mobile; 80%+ of gamers 50+ play primarily on mobile/tablet (AARP) | Mobile-first, browser-compatible second |
| **Older cohorts have the highest daily playtime in casual/lower-intensity genres** | 50+ spends 22.8 min/day in casual and 18.4 in social casino vs 14.1 in hardcore | Build a casual/midcore loop, not a hardcore one |
| **Sessions must be 90 sec – 25 min** | Dock waits 3.5 hr but *interruptible*; 10-hr break at night | Session = one decision cluster. Never a 30-min raid. |
| **Android ~63% of this audience** | Eleos: 37% iOS among working truckers | Android performance tier governs the engine budget |
| **Patchy connectivity** | Driver surveys name "lack of internet access in remote areas" as a leading app failure | Offline-first core loop, sync-on-reconnect |
| **Sunlight + small screen + one hand** | 58% cite small-screen friction; cab phone mounts; direct sun | High-contrast, ≥16sp type, one-thumb, no drag precision |
| **Ad intolerance is extreme** | 52% quit after repeated disruptive ads (Deloitte/AdMob 2025); reward-screen ads *triple* quit rates | Zero forced interstitials, ever |

---

## 2. Genre engagement ranked against this cohort

**Daily minutes spent per genre by age (adjoe, Feb 2024):**

| Genre | 0–19 | 20–29 | 30–39 | **40–49** | **50+** |
|---|---|---|---|---|---|
| **Card** | 19.1 | 22.8 | 25.3 | **25.8** | **25.5** |
| Casino | 13.4 | 15.8 | 18.9 | 20.4 | 19.8 |
| Puzzle | 15.5 | 16.8 | 20.3 | **21.4** | **21.5** |
| Strategy | 21.7 | 21.4 | 21.9 | 22.4 | 20.4 |

> **Finding:** for men in their 40s and 50s, **card mechanics are the single highest-time genre**
> (~26 min/day) — and *strategy* is the flattest, most age-stable line on the chart.

**Genre preference, all U.S. gamers (Attest 2026):** Puzzle/strategy **48%** › Action/adventure 41% ›
FPS 30% › Simulation 27% › RPG 25% › Sports 25% › Casual 19% › Horror 13%.
Among 55–64s, **puzzle preference hits 64%** vs 32% for 18–24s.

**Social casino app players by age (Q2 2020, n=1,208):**
45–54 = **21%** (largest single band) › 35–44 = 19% › 55–64 = 17% › 65–74 = 13% › 25–34 = 14% ›
18–24 = 10%. **60% of the social-casino audience is aged 36–70.** Slots are the most-played type
(53% of social casino players); social casino slots alone have ~120M monthly players.

**Card/casino monetisation split:** Card 46.5% ads / 53.5% IAP · Casino 23.8% ads / 76.2% IAP ·
Puzzle 25.2% / 74.8% · Strategy 29.4% / 70.6%.
→ *The older-skewing genres monetise through IAP, not ads.* A respectful IAP model is the
genre-native model, not a compromise.

---

## 3. The genre-by-genre verdict

| Candidate genre | Fit against VECTOR-CORE | Verdict |
|---|---|---|
| **Truck driving sim (3D)** | Authentic; but demands attention, twitch steering, GPU, 1.5 GB installs, battery. Incumbent *Truck Simulator USA* has **50M+ downloads at 3.8★** and review after review complains about **forced ads, monthly charges "as expensive as a real load board," and greed**. Players want *to be a trucker*, not to *re-drive their shift* while exhausted. | **Reject as the core.** Use as visual flavour only. |
| **Match-3 / puzzle** | Best raw reach, but the audience is majority-female and the theme has no connection to the persona. Zero moat. | Reject |
| **4X base-builder (Clash of Clans / Whiteout Survival)** | Async, cohort-based, no twitch, 55–77% male; proven with older men; but the fantasy is "warlord," not "trucker," and build timers frustrate the clock-dominated player. | **Partially adopt** — steal the async social architecture. |
| **Real-money / social casino** | Perfect demographic match (45–54 is the largest single band) and the strongest monetisation DNA in mobile. But: 40% of slot players report feeling addicted at least occasionally; this cohort is stressed, isolated and financially squeezed. Dark-pattern gambling design aimed at them is both unethical and commercially self-defeating (they review-bomb greed — see §4). | **Reject the math, adopt the satisfaction architecture** (collection, near-miss tension, event cadence) over a deterministic economy. |
| **Card roguelite / deckbuilder** | 40–49s spend more daily time on card games than any other genre. Truckers *self-report* playing **Balatro** during dock waits. Decision-dense, zero twitch, offline-clean, tiny install. But pure roguelites reset progress → weak for the "come back and find more than you left" need. | **Adopt as the decision layer.** |
| **Idle / incremental tycoon** | Audience "skews older and broader than most twitch-skill genres"; attracts players who like **optimization, math and slow-burn progress**; ~64% male in survey data; male-dominated when themed industrial (Idle Miner Tycoon). The core promise — *you were away and you still earned* — is a **literal mirror of the owner-operator's actual life**. | **ADOPT AS THE CORE.** |
| **Sim/tycoon business management** | "Classic simulation" themes skew older and broader; *Idle Miner Tycoon* / *Idle Factory Tycoon* proved the idle-sim business case for a male audience. | **Adopt** |

---

## 4. The competitor gap (this is the moat)

| Competitor | Scale | The gap |
|---|---|---|
| **Truck Simulator USA / Revolution** (Ovilex) | **50M+ downloads, 518K reviews, 3.8★** | Reviews complain about forced ads on *pause*, a subscription "as expensive as a real load board," incorrect units ("meters" in an American truck sim), traffic-light fairness, and paywalled upgrades. They built the demand and left the service on the table. |
| **American Truck Simulator** (SCS) | Premium PC/console; large, loyal, older-skewing community | Requires a PC/console and 20–60 min focused sessions. Not a dock-wait game. Its community proves the *appetite for authenticity*. |
| **Farm Sim / Ranch Sim / Construction Sim** mobile | Proven blue-collar sim demand | No trucking-specific micro-business fantasy; no US freight authenticity. |
| **Idle Miner / AdVenture Capitalist** | Proven idle-tycoon retention | Generic, non-American, non-blue-collar. No identity hook. |
| **Coin Master / MONOPOLY GO** | **$650M–$1.58B/yr; top-grossing casual in the U.S.** | Proves that a *collection + async social raid + seasonal event* loop with a light dice/spin tension can top the charts — with a casual, older-leaning, non-twitch audience. |

> **Nobody has built a game for truckers that a trucker would recognise as true.**
> That is a genuine, defensible, uncrowded position — and the entire audience is reachable through
> a handful of concentrated channels (trucker Facebook groups, r/Truckers, trucking YouTube,
> Overdrive / Land Line / CCJ, truck-stop geofenced ad inventory, and podcast ad reads, which this
> cohort over-indexes on).

---

## 5. The synthesis: the exact sub-genre

> ### IDLE FREIGHT TYCOON
> ### *Idle business-management sim + card-draft load-board decision layer + async "convoy" social competition, wrapped in authentic U.S. freight culture.*

**The four-component recipe:**

| Component | Borrowed from | Why |
|---|---|---|
| **Idle accrual economy** | AdVenture Capitalist, Idle Miner Tycoon | Mirrors the driver's life (miles accrue, money accrues while he's gone); rewards checking in, never punishes absence |
| **Card-draft decision layer** ("the load board") | Balatro, MONOPOLY GO's tension, casino satisfaction architecture | Card is the highest daily-time genre for 40–49s; determinism, not RNG; gives *decision density* so the game doesn't reduce to a progress bar |
| **Async social competition** ("Convoys") | Clash of Clans, Coin Master raids | The loneliest workforce in America gets belonging *without obligation* — no voice chat, no scheduled raids, no pressure |
| **Authenticity / craft pride** | American Truck Simulator's community | The moat. Every competitor is generic; this one is *true*. |

**Genre label to use with publishers/stores:**
*Idle Tycoon / Management Sim (midcore-casual)* — the store keywords are **truck, tycoon, idle,
empire, business sim**, all of which carry strong existing search volume.

---

## 6. Why this gets played more than the alternatives

1. **It fits the actual window.** 90 seconds at a dock light; 20 minutes in the bunk at night.
2. **It needs no twitch skill** — competition appeal declines with age, strategy does not.
3. **It accrues while he drives.** The single mechanic that matches his lived experience.
4. **It's built on the highest-time genre for his age band** (card ≈ 26 min/day) buried inside the
   highest-retention format (idle).
5. **It's IAP-native, not ad-native.** His genre monetises by respect, not interruption.
6. **The identity hook is a network effect.** CB handle as username; "Convoys" as guilds; a
   shareable weekly settlement. One game with critical social mass beats three with a third each.
7. **The incumbent left a 3.8★ hole** at 50M downloads.

---

## 7. Explicitly rejected design moves (and why)

| Rejected | Reason |
|---|---|
| Forced interstitial ads | 52% outright quit; 3× quit rate when placed on reward screens; and this cohort's most-quoted competitor complaint |
| Energy/lives gates that stop play | The player's real life is already a 14-hour clock. A second clock he can't beat is cruelty, not challenge. |
| Real-money slot/wager mechanics | Audience is stress- and money-vulnerable; 40% of slot players report addictive feelings; app-store and regulatory risk; reputationally fatal with a group that punishes greed publicly |
| Loot boxes / gacha for trucks | Truckers will call it what it is. It also destroys the "earned my rig" fantasy that is the whole point. |
| Forced account creation / 2FA | Driver-app surveys name repeated password changes and 2FA as a top irritant |
| Precision touch controls / reaction tests | Older players, gloves, sunlight, moving vehicle, one thumb |
| Real brand names as villains | Legal exposure. Parody: *Vall-Mart, America-Cold, Kro-Grr, Titan Foods, Sysco→Sys-Go* |

---

## 8. Sources

- **adjoe / Statista**, *Global daily mobile gaming engagement by genre and age* (Feb 2024) — card 25.8 min/day at 40–49
- **AdColony / Statista**, U.S. casino gaming app players by age (Q2 2020)
- **Newzoo**, *Social Casino Consumer Insights* — 60% of the audience aged 36–70; slots 53%
- **Attest**, *Game on: what 2026's gamers are playing* — puzzle/strategy 48% overall; 64% among 55–64s
- **AARP / ESA**, older-adult gaming: 80%+ mobile-first; 45% of 55+ game weekly; motivations = challenge, cognition, connection
- **JMIR Serious Games**, *Mobile Game Design Guide for Middle-Aged and Older Adults* — puzzle/card/board/strategy preference; challenge is the #1 motive; solo play preferred
- **Quantic Foundry** — competition declines most with age; strategy is the most age-stable motivation
- **adjoe**, *Idle Games: Demographics* — idle audience older/broader; male-skewed for industrial themes
- **Deloitte × Google AdMob** (2025, n=7,000) — 52% quit after repeated disruptive ads; reward-screen ads triple quit rate
- **Sensor Tower / Business of Apps / mobilegamer.biz** — card +18% and puzzle +10% growth; MONOPOLY GO $1.58B in 2024; Coin Master structural longevity
- **Google Play / App Store listings** for Truck Simulator USA (50M+ downloads, 3.8★, 518K reviews) and reader reviews
- **r/Truckers** threads: "What's your go-to activity while waiting to load or unload?" — Balatro, Steam Deck, Minecraft, console, exercise
