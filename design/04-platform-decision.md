# Platform Decision: Game + Outlier

**Status:** Recommendation. Nothing has been built yet.
**Scope:** One codebase family for the viewport bounty-hunter game (`03-pivot-viewport-bounty-hunter.md`) and the Outlier DOT/HOS compliance app.

---

## 1. Recommendation

**Build the UI and game as a web app (Vite + TypeScript), then wrap it with Capacitor for Android.**

| Layer | Choice | Why |
|---|---|---|
| UI / cockpit | Stitch export (HTML/CSS), restyled with the Mistral image as a background asset | Reuses existing front-end work. Web is the natural home for a cockpit-style interface. |
| Game engine | Phaser (JavaScript/TypeScript) | Mature 2D engine for retro pixel arcade. Runs in a browser and inside Capacitor. |
| Android wrapper | Capacitor | Ships the same web app as an APK for sideloading to the Galaxy S25. Also produces an AAB for Play later. |
| Native pieces | Small Kotlin plugin (Android Activity Recognition, "in vehicle") | The driving lockout needs native motion detection. Web can't do this reliably. |
| Browser build | Same web app, served as a PWA | Lets you test on the Linux Mint machine without a phone. Browser build is stationary-only (see lockout rules). |
| Backend jobs | Ubuntu VPS: n8n and Kestra | Scheduled jobs, reminders, document pipelines. Not in the phone's critical path. |

**Why not React Native / Expo:** It's a strong framework, but it would mean rewriting the Stitch UI into native components. Capacitor keeps your existing front end and fits the sideload path you already use. Expo is the better choice if you later need heavy native animation or an iOS App Store launch as a priority.

**Why not native Kotlin only:** Best sensor access, but it's the slowest path to a playable prototype and locks the game to one platform.

---

## 2. Mapping your tools

| Tool you have | Where it fits |
|---|---|
| **Linux Mint + VS Code** | Main dev machine. Build the web app, run Vite locally, test in the browser. |
| **Dyad** | Scaffold and iterate on components. Treat its output as a draft and review it in VS Code. |
| **Claude Desktop** | Design review, code review, and writing the compliance-rule logic against the FMCSA text. |
| **Freebuff** | Not evaluated in this session. Use it for what it does well, but check its output the same way as any AI draft. |
| **Ubuntu VPS: n8n** | Reminders (e.g., "your logbook has a gap"), scheduled exports, email/notification routing for Outlier. |
| **Ubuntu VPS: Kestra** | Heavier workflows: nightly HOS-log checks, document OCR pipeline, test-data generation. |
| **Ubuntu VPS: Vibe CLI** | Agentic coding on the server for refactors and test runs. |
| **Ubuntu VPS: Open-Design** | Not evaluated. Possibly useful for mockups; confirm it fits before relying on it. |
| **Galaxy S25 + F-Droid + sideloading** | The Android test device. Install debug APKs directly. |
| **Kai 9000** | Not evaluated; I don't know this tool well enough to recommend a role for it. |
| **Vibe/Mistral app** | Image generation (the cockpit art) and quick reference on the phone. |

**Build path to the phone:** Build the APK either locally (needs Android SDK on Mint) or in GitHub Actions (builds a debug APK on push and uploads it as an artifact, which you download and sideload). The GitHub Actions route avoids installing the Android SDK.

---

## 3. Free API keys: what to use them for

The rule: **do not send real driver data to free tiers.** Outlier handles HOS logs, driver identities, and vehicle/DOT records. That is personal and operational data.

| Provider | Free-tier data terms (as published, October 2026) | Use it for |
|---|---|---|
| **Google AI Studio / Gemini API (unpaid)** | Google may use submitted content to improve its products, and human reviewers may read it. The terms say not to submit sensitive or personal information. Users in the EEA, Switzerland, or UK get paid-tier terms. | Game dialogue, story drafts, placeholder text, synthetic test data. Never real driver data. |
| **Mistral free mode** | Free-mode inputs and outputs may be used for training. Vibe (non-Enterprise) is not opted out by default. You can opt out in settings. Labs/Preview models can train regardless of opt-out. | Image generation for art. Opt out of training before using any text features. Avoid Labs/Preview models for anything sensitive. |
| **OpenRouter** | Routes to many providers, each with its own policy. | Dev experiments. Restrict routing to providers you've checked. |
| **Groq** | Not checked in this session. | Fast dev testing with synthetic data. Check its current data policy first. |
| **Hetzner Inference / Compactif.ai** | Not checked in this session. | Check each provider's terms before any real use. |

**Outlier-specific rule:** Process HOS and document data on the phone or on your VPS first. Any LLM call touching real records should go to a **paid tier with a no-training commitment** (or zero data retention where available). Free keys are for development with synthetic data only.

Note: if Outlier is ever sold to fleets, the data terms become part of the product promise. Plan for that before launch.

---

## 4. Stitch front end vs Mistral image

Keep the Stitch layout and code. Swap in the Mistral image as the viewport background. Practical notes:

- **Resolution:** Export at the S25's full screen size or larger, and use `background-size: cover`.
- **Keep instrument text as live text.** AI images often garble gauges, labels, and small print. Put real text in HTML/CSS layers over the image.
- **Commercial use:** Confirm that your Mistral plan's terms allow commercial use of generated images. Keep a record of the prompt, tool, plan, and date.
- **No real brands or logos** in the art, which keeps you clear of trademark issues.

---

## 5. Next steps (when you're ready)

1. Create a monorepo with `apps/game`, `apps/outlier`, and a shared `packages/ui` for the cockpit design.
2. Set up Vite + TypeScript + Capacitor and produce a first APK through GitHub Actions.
3. Sideload the APK to the S25 and confirm the viewport image, the Stitch layout, and a placeholder game screen all render.
4. Write the Kotlin lockout plugin and test it on the S25 (stationary, walking, in a car, as a passenger).
5. Get a legal review of the Outlier compliance logic against the current FMCSA rules before any user-facing claim goes live.

---

## Sources (checked October 2026)

- Google Gemini API Additional Terms (ai.google.dev/gemini-api/terms): unpaid-service data use and human review; paid-service no-training.
- Mistral Help Center: "Do you use my user data to train your AI models?" and "Can I opt out of my input or output data being used for training?"
- Mistral Commercial Terms, section 4.3 on Labs and Preview models.
- Capacitor vs Expo comparisons (didof.dev, otakit.app, pkgpulse.com, 2026). Used for the framework trade-off only; confirm current versions before starting.
