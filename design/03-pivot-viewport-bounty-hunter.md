# Design Pivot: Viewport Bounty Hunter

**Status:** Concept direction, pending owner decisions. Supersedes the trucking theme in `01-flagship-blueprint.md`.
**Brand:** Juggernaut Nexus. **Companion product:** Outlier (DOT/FMCSA HOS auditor, compliance assistant, document vault).

---

## 1. Why the pivot

Owner decisions that change the design:

1. **The game must not resemble the job.** No trucks, loads, dispatch, HOS clocks, settlements, detention, or freight vocabulary. The previous flagship's core mechanics were all job-shaped, so they are retired as a theme (see §10 for what survives in abstract form).
2. **The game is a viewport.** The Outlier SaaS is designed as a retro-futuristic space-western cockpit, with a viewport onto space. The game launches out of that window, so the handoff is the product's signature moment, not a loading screen.
3. **It is a break, not a grind.** The player should come back from the game calmer, not more keyed up. Compliance tension stays in Outlier. The game is the release valve.
4. **Safety by default.** The game locks while the vehicle is moving (§6).

---

## 2. Genre

**Working genre:** *Tactical arcade bounty RPG, with a persistent crew and a frontier-galaxy warrant chain.*

Breakdown:
- **Core fantasy:** You are a bounty hunter with a battered ship, a code, and a past. You track people down, make choices about them, and go home to a ship that remembers you.
- **Arcade layer:** Short hunts (3–8 min), retro pixel-art combat, readable telegraphs, pause anywhere.
- **RPG layer:** Stats, gear, ship upgrades, crew relationships, a story that accumulates across hunts.
- **Session shape:** A hunt, then return to the viewport. There is no timer on the hub, and nothing is lost to being away.

**Comparable proof points (mobile/browser-scale, to be verified in prototyping):**
- *Bounty Hunter Space Lizard* — turn-based tactical roguelike, 4.6★ on Google Play with 255 reviews, 10K+ downloads, described by reviewers as "a highly tactical turn-based roguelike," no ads. Evidence that tactical arcade with readable rules works on phones.
- *Space Bounties Inc.* — 2015 mobile space-bounty RPG with retro 8-bit graphics and a risk/reward system, praised by multiple outlets. Evidence that the retro-space-bounty RPG niche has reviewer appetite.
- *Bounty Stars* (DeNA, 2016) — mobile space-bounty RPG on iOS/Android. Evidence that the theme has been tried on mobile at scale.
- *Huntdown* (Easy Trigger Games) — 2D run-and-gun bounty hunting, 97% positive on Steam recent reviews, but reviewers note it only suits players who "really, really like the old-school arcade approach." Warning: pure reflex combat is a narrower audience.
- *Space Hunters* (Purple Tree/Purple Play) — 2D beat-'em-up with bounty hunters, PC/Switch; an example of the theme in action form outside mobile.

**Honest market read:** The space-bounty theme has proven appeal and a loyal, small audience. The most successful versions in this space lean tactical, not twitchy. This is consistent with Study 2: our audience is older, reflex-averse, and drawn to strategy and card-like decisions.

---

## 3. Reconciling "arcade" with the audience

Study 2 found that older players are frustrated by speed and reflex demands. The retro arcade layer therefore needs three rules:

| Rule | What it means |
|---|---|
| **Readable over reflexive** | Every enemy telegraphs its next move for at least 0.6 seconds. Dodging is a choice, not a race. |
| **Slow time on demand** | A "Steady Hand" meter slows the action to a crawl. Always available, never required. |
| **Easy Ride tier** | A difficulty setting with no fail states beyond losing gear and returning to the ship. |

Arcade intensity sets the feel. It is never a timer on the player.

---

## 4. Core loop (draft)

1. **Viewport (hub).** Your ship sits in a parking orbit. The viewport shows stars and a slow drift. A console holds the **Wanted Wall** (warrants, not jobs), crew, and the ship's systems.
2. **Pick a warrant.** Each warrant is a person with a story (see §7). You see the target, the crime, the reward, and the danger. No timers.
3. **Launch through the viewport.** The space view becomes the game. Descend through a planet's atmosphere to a frontier town or wasteland. The transition is part of the game: the view tilts, the stars shrink, and the ground comes up. No separate loading animation.
4. **Hunt.** A short arcade stage: track the target through a town, a ruin, or a canyon. Combine stealth, dialogue choices, and tactical shootouts. Pause at any moment.
5. **Resolve.** Bring them in alive for a higher reward, or let them go for a story choice. Each resolution changes the warrant chain.
6. **Return to the viewport.** Rewards, gear, ship upgrades, crew moments, and a short quiet moment before the next choice.

---

## 5. Systems (draft)

- **Stats:** Four stats, named in-world rather than by genre jargon: **Nerve** (combat), **Read** (tracking and deduction), **Grit** (survival and endurance), **Words** (negotiation and bluffing). Each maps to a play style.
- **Ship:** Upgrade the viewport (wider view, better scanners), engine, hold, and weapons. The ship's cockpit changes visibly as you upgrade.
- **Crew:** Named companions with relationships, dialogue, and small favors. Crew members join hunts or stay aboard and run the console.
- **Gear:** Earned, never gacha. Rarity is shown on the item and never hidden behind a pull.
- **Reputation:** Two tracks: **Lawful** (the authorities trust you) and **Street** (the outskirts trust you). Both lead to different warrant chains and endings.
- **Persistent ledger:** Your record across hunts is visible, so the player can see their own history.

---

## 6. Driving lockout (safety feature)

Priority: **non-negotiable, default-on, cannot be turned off while moving.**

**Trigger:** Vehicle motion detected by either:
- Platform activity recognition (Android "in vehicle" from the Activity Recognition API; iOS automotive activity from CoreMotion), or
- GPS speed sustained above a threshold (propose ~5 mph / 8 km/h for 10+ seconds).

**Response, in order:**
1. Game auto-pauses and saves the current state (hunt progress, dialogue, inventory).
2. The screen changes to a **Parked Mode** screen: the viewport slowly drifts, the ship idles, and a calm "Eyes on the road" message appears. No interactive controls, no notifications, no ads, no sound effects.
3. Nothing resumes until the device has been stationary for a sustained period (propose 3 minutes).
4. Resume is a deliberate action on the parked screen. There is no override while moving.

**Why this matters for this audience:**
- Federal rules (49 CFR 392.80 and 392.82) bar commercial drivers from texting and handheld phone use while driving, and many states go further. A game that lets a driver play while rolling is a liability to the very people Outlier is built to protect.
- The lockout is the same promise Outlier makes: the app should make the road safer, not compete with it.

**Platform limits:**
- **Mobile (Play Store): reliable.** Activity recognition plus GPS.
- **Browser: not reliable.** Browsers lack consistent motion or in-vehicle signals and have limited geolocation. The browser build should be treated as a **stationary-only** version, or not shipped at all in this mode.

**Engineering note:** Activity recognition is probabilistic. False positives (a passenger, a train) should resolve gently, by pausing and asking the player to confirm they're parked, not by losing progress.

---

## 7. Story (seed)

**Working title:** *Warrant Chain* (alternates: *Wanted Dead or Alive*, *Frontier Warrants*).

**Premise:** The galaxy's frontier is run by a patchwork of Lawful Concord outposts and independent Street syndicates. Warrants are issued by whoever still has the paperwork. You hunt for whoever pays. Every target is a person whose story you can read, and many are not what their warrant says.

**Spine:** A warrant comes in for an old debt you owe. Chasing it turns up a larger conspiracy: a Concord ledger that has been erasing and reissuing warrants to clean out witnesses. The question at the center is what you owe the people on the list, and whether the paperwork is more dangerous than the criminals.

**Ending themes (not a checklist):**
- **Carry the debt:** you keep working the frontier, and your ship becomes a home for the people you couldn't save.
- **Clear the ledger:** you burn the warrant system, at a cost.
- **Hang up the holster:** you retire to a quiet post and let the crew carry the next chapter.

**Personal note (owner's call):** Redemption, debt, and the question of who you were before the work are the natural spine of this genre. If you want those themes to carry some of your own story, it can be done in the writing without it being your memoir. Only include what you're comfortable seeing in a product.

**Legal:** Keep Cowboy Bebop as a *tone* reference only. Do not use its characters, names (Spike, Jet, Faye, Ein), music, or specific plot beats. The live-action series was canceled after one season in December 2021, so it's a nostalgia hook, not a proven commercial one.

---

## 8. Visual and audio direction

- **Art:** Retro pixel art in the arcade stages, with a warmer, painted look in the viewport and hub. The palette should match Outlier's cockpit: amber instruments, deep space blue, and a clean glow.
- **Viewport:** The viewport is the main image. Stars, planets, and traffic lanes are always visible from the cockpit.
- **Audio:** Synth-and-guitar retro score. Clean, calm, and fully mute-viable. The viewport ambience should be pleasant to leave on in the background.
- **Accessibility:** No red/green-only signals. Sunlight-readable contrast. Captions for all radio-style dialogue.

---

## 9. Monetization and respect rules (carried forward)

- Free core. One-time unlock for the full game.
- Optional rewarded ads only, never on Parked Mode, never on results screens, never interrupting a hunt.
- Cosmetics for the ship and viewport.
- **Forbidden:** loot boxes, gacha, gambling mechanics, energy gates, timer-skips, forced interstitials, notification spam, anything that makes the player feel they must return.

---

## 10. What survives from the trucking blueprint (abstract only)

| Mechanic | Survives as | Retired as |
|---|---|---|
| Card-draft decision layer | Warrant selection | Load board |
| Idle accrual | Ship's passive drift and salvage | Haul-while-away money |
| Async social | Crew visits and shared warrant leaderboards | Convoy/handshake |
| Clean results screen | Ship's ledger | Settlement Friday |
| No gacha, no ads, no timers | All of it | — |

---

## 11. Open decisions for the owner

1. **Arcade intensity:** tactical (turn-based or slow-time, closest to Space Lizard) vs. real-time arcade with Steady Hand slow-mo.
2. **World structure:** open frontier map vs. chaptered story arc vs. both.
3. **Session length target:** 3–5 minutes per hunt, or longer stages?
4. **Story tone:** serious frontier noir, cheerful space western, or a balance?
5. **Lockout thresholds:** confirm the speed threshold and stationary timer, and whether passenger mode should be supported.

---

## 12. Next steps (proposed, not started)

- Paper prototype of one hunt (index cards, one town, one target) with 5–8 players 45+ to test the readable-combat rule.
- Test the lockout on two Android devices and two iPhones, including a passenger, a train, and a parking-lot creep.
- Mock the viewport-to-planet handoff in a static prototype before any engine work.
- Revisit the validation plan in `01-flagship-blueprint.md` §12 and adapt it to this concept.
