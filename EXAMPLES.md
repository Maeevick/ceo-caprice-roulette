# CEO CAPRICE ROULETTE — EXAMPLES

Three reference pitches illustrating the canonical template.
Use these to calibrate tone, scope, and Gherkin depth.

---

# 🎯 RECON JOURNAL — CEO CAPRICE ROULETTE #1

---

## 📢 THE CAPRICE

> "I'm tired of losing my recon notes across 5 browser tabs and a Notion graveyard. In two weeks we ship a dedicated bug bounty recon workspace or we don't ship at all."

---

## ⚡ THE PROBLEM

A bug bounty hunter loses their reconnaissance thread mid-session because their notes, scope, and found endpoints live in three different unconnected tools.

## 🎮 THE PRODUCT

A scoped recon workspace: one target, one session, structured note-taking with technique tagging, endpoint registry, and exportable markdown report.

## 👤 ICP

Intermediate bug bounty hunter, 6-18 months in, earning occasional bounties, wants to level up methodology discipline before attempting OSCP.

## 📡 DISTRIBUTION SPARK

Post a "building my own recon notebook in public" thread on CTFtime + r/bugbounty on day 1. First 10 users before launch.

## 💶 PRICING

9€/mo — cheaper than any pro recon tool, positioned as "methodology notebook not scanner."

---

## 📐 SMART SPEC

### SPECIFIC — One problem, one journey

Hunter opens a new target → defines scope → runs through recon phases (passive, active, enumeration) → logs findings per technique → exports a clean markdown report to paste into HackerOne submission.

---

### MEASURABLE — The Gherkin

```gherkin
Feature: Structured recon session for a bug bounty target

  # HAPPY PATH — mandatory, exactly 1
  Scenario: Hunter completes a recon session and exports report
    Given a hunter has created a target with a defined scope
    When they log findings across at least 3 technique tags
    Then they can export a structured markdown report
         containing scope, findings, and technique summary

  # SUPPORTING — 1
  Scenario: Hunter resumes an interrupted session
    Given a hunter has a saved session with partial findings
    When they reopen the target
    Then all previous findings and scope are intact
         and the session continues from last state

  # EDGE / ERROR — 1
  Scenario: Hunter attempts to export an empty session
    Given a hunter has created a target but logged no findings
    When they trigger the export
    Then the export is blocked with a clear message
         indicating minimum findings are required
```

> ⚠️ Total scenarios: 3 — within bounds.

**✅ Done when:** create target → log findings → export report works end-to-end without data loss.

**KPIs:**

| Horizon | Acquisition | Activation            | Retention        | Revenue   |
| ------- | ----------- | --------------------- | ---------------- | --------- |
| D+30    | 50 signups  | 20 completed sessions | —                | —         |
| D+90    | 200 signups | —                     | 40% still active | 15 paying |

---

### ACHIEVABLE — Solo constraints

- **Stack:** SvelteKit 5, PostgreSQL, Scaleway
- **Assets:** none — pure UI, no external data
- **Infra cost:** ~2€/mo at zero revenue
- **Out of v1:** scanner integration, team sharing, CVE lookup, automation, mobile view

---

### RELEVANT — Why you, why now

Directly accelerates your own bug bounty learning while building the product — dogfooding from day one.

---

### TIME-BOUND

- ⏱ **Duration:** 2 weeks
- 🚀 **Ship date:** D+14 from start

---

---

---

# 🎯 PLOT KNOT — CEO CAPRICE ROULETTE #2

---

## 📢 THE CAPRICE

> "Every writer I know has a drawer full of broken first drafts. We're shipping an AI consistency checker in one month — no features, no fluff, just the thing that unblocks the story."

---

## ⚡ THE PROBLEM

A fiction writer 30,000 words into a sci-fi novel discovers their character was in two places at once in chapter 12 — and has no tool to catch these contradictions before a reader does.

## 🎮 THE PRODUCT

Paste your manuscript, get a flagged list of character/timeline/location contradictions and unresolved plot threads — nothing else.

## 👤 ICP

Serious amateur or self-publishing fiction writer, 20k-100k word projects, genre fiction (sci-fi, fantasy, thriller), no editor budget.

## 📡 DISTRIBUTION SPARK

NaNoWriMo forum post + r/worldbuilding launch thread. Writers are vocal about their pain — one honest "I built this for myself" post converts.

## 💶 PRICING

9€/mo or 29€ one-time per manuscript — one-time anchors trust for the "I just need this once" crowd, subscription for serial writers.

---

## 📐 SMART SPEC

### SPECIFIC — One problem, one journey

Writer pastes or uploads manuscript → selects check type (character, timeline, location) → receives annotated list of flagged inconsistencies with chapter references → exports as PDF or markdown.

---

### MEASURABLE — The Gherkin

```gherkin
Feature: Manuscript consistency analysis

  # HAPPY PATH — mandatory, exactly 1
  Scenario: Writer detects a character contradiction
    Given a writer has uploaded a manuscript of at least 10.000 words
    When they request a character consistency check
    Then the tool returns a list of flagged contradictions
         each with chapter reference and conflicting excerpts

  # SUPPORTING — 1
  Scenario: Writer selects a specific check type
    Given a writer has uploaded a manuscript
    When they select "timeline only" as the check type
    Then only timeline-related flags are returned
         and character/location checks are skipped

  # EDGE / ERROR — 2
  Scenario: Clean manuscript returns no false panic
    Given a writer uploads a structurally clean short story
    When they request a full consistency check
    Then the tool returns zero critical flags
         and confirms which elements were successfully tracked

  Scenario: Manuscript exceeds processable size
    Given a writer uploads a file above the size limit
    When the upload is submitted
    Then the tool rejects it with a clear size limit message
         and suggests splitting the manuscript by act
```

> ⚠️ Total scenarios: 4 — within bounds.

**✅ Done when:** upload → analyse → flagged report delivered, reproducible across 3 test manuscripts.

**KPIs:**

| Horizon | Acquisition | Activation      | Retention                     | Revenue   |
| ------- | ----------- | --------------- | ----------------------------- | --------- |
| D+30    | 80 signups  | 30 analyses run | —                             | —         |
| D+90    | 300 signups | —               | 25% return for new manuscript | 20 paying |

---

### ACHIEVABLE — Solo constraints

- **Stack:** SvelteKit 5, Claude API (Haiku for cost), minimal backend
- **Assets:** none
- **Infra cost:** ~5€/mo + API usage (covered by first 2 subscribers)
- **Out of v1:** prose suggestions, style feedback, collaboration, Word/Google Docs plugin, per-chapter upload

---

### RELEVANT — Why you, why now

Combines your AI integration speed with a creative domain you consume as a reader — you can evaluate output quality immediately without deep domain expertise.

---

### TIME-BOUND

- ⏱ **Duration:** 1 month
- 🚀 **Ship date:** D+30 from start

---

---

---

# 🎯 FIVE ROOM DUNGEON — CEO CAPRICE ROULETTE #3

---

## 📢 THE CAPRICE

> "I want a dungeon crawl I can finish in my lunch break. No installs, no accounts, playable in a browser in 30 seconds. Ship it in one week or the idea dies."

---

## ⚡ THE PROBLEM

A casual gamer wants a complete, satisfying tactical experience in under 15 minutes but every roguelite asks for 2 hours of onboarding before the fun starts.

## 🎮 THE PRODUCT

A browser-based, procedurally generated 5-room dungeon crawl: enter, fight, loot, boss, done — shareable as a unique URL, no install, no account.

## 👤 ICP

25-40 casual gamer, plays during commute or lunch break, nostalgic for old-school dungeon crawlers, zero patience for tutorials.

## 📡 DISTRIBUTION SPARK

Post the shareable URL mechanic on r/roguelikes and itch.io new releases on launch day — the unique seed URL is the hook, not the game.

## 💶 PRICING

Free to play → 8€ one-time "Deluxe" unlock (extra classes, visual themes, dungeon seeds) — itch.io + own site.

---

## 📐 SMART SPEC

### SPECIFIC — One problem, one journey

Player lands on URL → picks a class in one click → plays through 5 procedurally generated rooms → reaches boss → wins or dies → gets a shareable result card URL.

---

### MEASURABLE — The Gherkin

```gherkin
Feature: Complete a procedurally generated dungeon run

  # HAPPY PATH — mandatory, exactly 1
  Scenario: Player completes a full run and shares it
    Given a player has selected a class on the landing page
    When they navigate through 5 rooms and defeat the boss
    Then they reach an end screen with run stats
         and a unique shareable URL for that exact dungeon seed

  # SUPPORTING — 1
  Scenario: Player replays a friend's shared seed
    Given a player receives a shared dungeon seed URL
    When they open it and select a class
    Then they play the exact same room layout as the sharer
         with their own independent run outcome

  # EDGE / ERROR — 2
  Scenario: Player dies mid-dungeon
    Given a player has entered room 3 with low health
    When their health reaches zero
    Then they see a death screen with cause and room reached
         and a one-click option to restart with a new seed

  Scenario: Player tries to access an invalid seed URL
    Given a player opens a malformed or expired seed URL
    When the game attempts to load
    Then a friendly error is shown
         and a new random dungeon is offered instead
```

> ⚠️ Total scenarios: 4 — within bounds.

**✅ Done when:** full run playable start to finish, shareable URL works, mobile-playable in browser.

**KPIs:**

| Horizon | Acquisition        | Activation             | Retention        | Revenue             |
| ------- | ------------------ | ---------------------- | ---------------- | ------------------- |
| D+30    | 200 unique players | 60% complete first run | —                | —                   |
| D+90    | 1000 players       | —                      | 15% play 5+ runs | 30 Deluxe purchases |

---

### ACHIEVABLE — Solo constraints

- **Stack:** Svelte (no backend), localStorage for run state, Vercel
- **Assets:** Kenney Assets (CC0), no budget required
- **Infra cost:** 0€
- **Out of v1:** save system, leaderboard, multiplayer, story, sound, mobile app

---

### RELEVANT — Why you, why now

Shippable in one week with zero external dependencies — pure outcome-oriented sprint, dogfoods your own lean delivery muscle.

---

### TIME-BOUND

- ⏱ **Duration:** 1 week
- 🚀 **Ship date:** D+7 from start
