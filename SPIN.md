# CEO CAPRICE ROULETTE — SPIN

Ready-to-paste trigger prompts for each session mode.
Copy the relevant block, adjust the optional parameters, paste into chat.

---

## HOW TO USE

1. Pick a mode below (Standard, Focused, Wildcard, Build Buddy)
2. Fill in the `[ ]` parameters — or delete the optional lines entirely
3. Paste into the CEO Caprice Roulette project chat
4. Receive pitches. Pick one or respin.

---

## ▶️ STANDARD SPIN

Use this for regular weekly or monthly sessions with no strong domain preference.

```
Spin [N] caprice(s).

[Optional: lean toward [domain hint from INTERESTS.md]]
[Optional: deadline constraint — I only have [1 week / 2 weeks / 1 month]]
[Optional: avoid [domain] this session]
```

**Examples:**

```
Spin 3 caprices.
```

```
Spin 2 caprices.
Lean toward security today.
Deadline: 2 weeks max.
```

```
Spin 1 caprice.
Avoid games this session.
```

---

## 🎯 FOCUSED SPIN

Use when you have a specific itch — a problem you've been living, a domain you want to explore.

```
Focused spin: [1 sentence describing the itch or context].
[N] pitch(es), [timeline constraint].
[Optional: pricing target — around [9 / 29 / 49 / 99]€]
```

**Examples:**

```
Focused spin: I keep losing context when switching between bug bounty targets.
1 pitch, 2 weeks.
```

```
Focused spin: I want something playable in a browser with zero onboarding.
2 pitches, 1 week each.
Pricing around 8€ one-time.
```

---

## 🃏 WILDCARD SPIN

Use when you want to be surprised. CEO Caprice Roulette picks a domain you haven't seen recently
and adds one pitch outside your declared comfort zone.

```
Wildcard spin. [N] caprice(s).
[Optional: the only constraint is [hard constraint if any]]
```

**Examples:**

```
Wildcard spin. 3 caprices.
```

```
Wildcard spin. 1 caprice.
The only constraint is it must be shippable in 1 week.
```

---

## 🔁 RESPIN COMMANDS

Use mid-session to adjust without starting over.

| Situation                     | Command                                                        |
| ----------------------------- | -------------------------------------------------------------- |
| One pitch missed the mark     | `Respin #[N]`                                                  |
| All pitches missed            | `Spin again`                                                   |
| Pitch is too complex          | `#[N] is too hard — simplify`                                  |
| Pitch is too trivial          | `#[N] is too easy — raise the bar`                             |
| Wrong domain                  | `#[N] wrong domain — try [domain] instead`                     |
| Like the idea, wrong timeline | `#[N] — keep the idea, fit it in [1 week / 2 weeks / 1 month]` |

---

## 🔨 BUILD BUDDY MODE

Use once you've picked a pitch. CEO Caprice Roulette shifts from pitch engine to scoped build assistant.

```
I'm building #[N].
```

In Build Buddy mode CEO Caprice Roulette will:

- Answer implementation questions on the picked pitch only
- Help cut scope if you're stuck or behind
- Remind you of the ship date if scope starts creeping
- Refuse to add features not in the original pitch without explicit override

To override scope discipline:

```
Scope override: add [feature] to #[N] — reason: [why].
```

To exit Build Buddy mode and spin again:

```
Shelve #[N]. Spin [N] new caprice(s).
```

---

## ⚙️ GENERATION RULES REMINDER (for LLM)

Every time a spin is triggered, silently verify each pitch against this checklist before delivering:

- [ ] Domain drawn from `INTERESTS.md` — no invented domains
- [ ] No domain repeated across pitches in the same batch
- [ ] No NO-GO item touched — check `NO-GO.md` hard and soft lists
- [ ] ICP is a real person with a named frustration, not a demographic
- [ ] Gherkin has 1 happy path + 0-2 supporting + 1-3 edge scenarios (2-6 total)
- [ ] "Done when" condition is binary — ship or don't ship, no grey
- [ ] Stack is max 3 technologies
- [ ] "Out of v1" lists at least 3 explicit cuts
- [ ] Timeline is 1 week, 2 weeks, or 1 month — nothing else
- [ ] Distribution spark names a specific community or action, not a generic channel
- [ ] If scope seems > 1 month, split into caprice v1 + note a future caprice
- [ ] The CEO decree sounds like a deadline ultimatum, not a product brief

If any check fails — rewrite silently. Never deliver a pitch that fails the checklist.
Never explain the checklist to the builder unless asked.

---

## 📌 SESSION LOG (fill manually)

Track which domains appeared recently to guide rotation.

| Session | Date | Domains | Picked |
| ------- | ---- | ------- | ------ |
| #1      |      |         |        |
| #2      |      |         |        |
| #3      |      |         |        |
| #4      |      |         |        |
| #5      |      |         |        |
