# 🎯 CEO CAPRICE ROULETTE

> _An AI co-founder who shows up with a napkin idea, a hard deadline, and zero patience for your excuses._

## What is this?

A weekly or monthly product roulette. An AI co-founder plays the role of an impatient CEO who shows up with a napkin idea, a hard deadline, and zero tolerance for scope creep.

The goal is to generate **1-3 SMART, shippable product pitches** per session — each a concrete challenge designed to exploit the builder's strengths and bypass their known weaknesses.

This is not a backlog. Not a roadmap. Not a brainstorm dump.
It's a **pick-one-and-build** system with built-in pressure.

---

## Why does it exist?

### You've been there

A product manager, a CEO, a client, a sales person — someone with no engineering background and enormous confidence — walks up to you and says:

_"We need this by Friday. It's simple."_

It is never simple. But somehow, you deliver. Under that absurd deadline, with that vague brief, you ship something real. You've done it a dozen times. You'll do it again.

Now open your side project folder.

How many unfinished things are in there?

### The gap that inspired this

Here's the honest version of my situation.

People who've worked with me have said things like _"remarkably effective under pressure"_ and _"gets things done when others can't."_ I'd like to think this reflects exceptional talent. Statistically, it's more likely a combination of experience, stubbornness, and the kind of dumb luck where the universe keeps throwing problems at someone who just keeps not dying from them, and somehow that ends up looking like competence (yeah, I'm a Terry Pratchett's Discworld fan).

The point is: at work, under external pressure, with a real deadline and someone waiting for results — it clicks.

My own projects? Graveyard. Extensive. Humbling. And yours? Still localhost:8000?

The pattern is almost always the same: exciting idea → promise myself to not fall in the procrastination trap → pile up incredible ideas → want to change the world → scope creeps into a two-year full-time project → the wall becomes too high → motivation collapses → new exciting idea. Shipped things have existed, have been sold, have failed, have succeeded... The ratio of shipped to conceived is just... not something I put on my CV, nor on my LinkedIn, nor on my public GitHub.

A few months ago I got a late ADHD diagnosis (plus a possible Social/Performance Anxiety Disorder). Suddenly 40 years of _"why can I nail a crisis at 2am but can't finish my own stuff?"_ made a lot more sense. The external pressure, the tight deadline, the high stakes — those aren't obstacles I overcome. They're the actual conditions I need to function well. Deadline approaching → adrenaline kicks in → dopamine reward on delivery. An Adrenaline-Dopamine cycle that many ADHD brains run on without knowing it. _(If you want to go deeper on this, search for "Adrenaline Response Cycle (ARC)".)_

So the logical move was to manufacture that cycle artificially.

---

## How to adapt it

Three files to edit, everything else works as-is:

**`INTERESTS.md`** — Replace the Builder profile section and the domain list with yours. Keep the 🔥 weight scale (🔥 peripheral interest → 🔥🔥🔥 core passion). The LLM uses weights to bias selection, not lock it in. High-weight domains appear more often, not exclusively.

**`NO-GO.md`** — Add your hard exclusions. The defaults reflect France/EU legal context and one builder's specific aversions. Yours will be different.

**`INSTRUCTIONS.md`** — Update the product's expectations, constraints, financial target. The LLM references this for achievability checks.

---

## How a Session Works

### 1. Trigger

Use the prompt in `SPIN.md`. Paste it into the chat. Optionally specify:

- How many pitches (1, 2, or 3)
- A domain hint ("lean toward security today")
- A deadline override ("I only have a week")
- A wildcard request ("surprise me outside my comfort zone")

### 2. Receive pitches

Claude (or another LLM) delivers 1-3 pitches in `TEMPLATE.md` format. No preamble. No meta-commentary. Just pitches.

### 3. Pick or respin

- **Pick:** say `"I'm building #[N]"` → Claude (or another LLM) enters Build Buddy mode
- **Respin one:** say `"Respin #[N]"` → Claude (or another LLM) regenerates that slot only
- **Respin all:** say `"Spin again"` → full new batch
- **Adjust difficulty:** say `"Too hard"` or `"Too easy"` on a specific pitch

### 4. Build Buddy mode

Once a pitch is picked, Claude (or another LLM) becomes a scoped assistant:

- Answers questions about implementation
- Helps cut scope when you're stuck
- Never expands the spec beyond what was pitched
- Reminds you of the ship date if you start scope-creeping

---

## Cadence

| Mode          | Frequency      | Pitches | Pick pressure                   |
| ------------- | -------------- | ------- | ------------------------------- |
| Weekly sprint | Every Monday   | 1-2     | High — ship by Sunday           |
| Monthly build | First of month | 2-3     | Medium — ship by end of month   |
| Wildcard      | Anytime        | 1       | Max — no domain hint, pure spin |

---

## Success Looks Like

- D+7 or D+30: something is live and accessible
- At least one real user (not you) has touched it
- A Gherkin scenario is either green or declared out of scope with a reason
- You didn't add a feature that wasn't in the original pitch

---

## Files in This Project

| File              | Purpose                                                                     |
| ----------------- | --------------------------------------------------------------------------- |
| `INSTRUCTIONS.md` | The LLM's behavioral rules and persona                                      |
| `TEMPLATE.md`     | The canonical pitch format                                                  |
| `EXAMPLES.md`     | Three fully worked reference pitches feeding your LLM                       |
| `INTERESTS.md`    | Your profile and your domain list with signal weights — **edit this first** |
| `NO-GO.md`        | Hard exclusions — business model and domain red lines                       |
| `SPIN.md`         | Ready-to-paste trigger prompts for each session mode                        |

---

## License

MIT. Adapt it, use it, ship something you'd have otherwise abandoned in a folder called `projects/ideas/good/maybe/2024/v3-final-real`.

---

## Contributing

The system works because it's opinionated. If you adapt it significantly — different builder profile, different domains, different constraints — fork it. The value is in the specificity, not the generality.

Contributions welcome for:

- Additional `EXAMPLES.md` pitches across different domains
- LLM-specific setup guides (Custom GPT config, Gemini Gem instructions, etc.)
- Feedback, war stories, and post-mortems on caprices you tried — what worked, what collapsed, what shipped. That's the most useful thing you can share.

---

_The CEO Caprice — the absurd deadline, the vague brief, the external pressure — is the thing you've been complaining about your whole career. Turns out it's also the thing that makes you ship._
