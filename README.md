# Quaker-adapted process for multi-agent use

This repo adapts three distinct Quaker process forms — clearness committee, meeting for
business, and meeting-with-a-concern (labor or standing committee) — into practices an
AI coding agent (or a team of them) can run, so that contested or high-stakes decisions get
a discernment process instead of either a unilateral call or a vote.

It grew out of using these forms for real, on a real codebase, over several months. It is
Penelope-agnostic and tool-agnostic: nothing here depends on a particular graph database,
planner, or CLI. Wherever the originating practice used tool-specific commands, this repo
states the general shape instead and leaves the wiring to whatever system of record you use.

**This is an adaptation, not a claim of equivalence.** None of this is a substitute for an
actual Meeting, actual worship, or the actual discipline of gathered Friends discerning
together in the Spirit. It borrows structure and vocabulary from Quaker process because that
structure turned out to solve real problems in agent-assisted software work — genuine
disagreement among readings of a codebase, decisions that are expensive to get wrong, taste
that only one person can rule on. `docs/quaker-correspondence.md` is explicit about where the
analogy holds and where it strains.

## The core finding: these are three different practices, not one

Early drafts of this material treated "convene several agent standpoints and synthesize" as a
single technique. It isn't. Three different situations call for three different forms, and
using the wrong one produces a specific, recognizable failure (a business decision run as a
clearness sitting quietly usurps someone's discernment of their own leading; a clearness
question run as a business meeting turns "help me see" into "vote on my behalf").

1. **Clearness committee** (`roles/`, this is the default association most people have with
   "Quaker process") — convened for **one participant's leading**: one voice with its own
   concern, discerning the right shape of its own condition. Everyone else queries. They do
   not advocate a position of their own.

2. **Meeting for business** — the standpoints speak **as the whole ongoing process reflecting
   on itself**, not as individual voices each with a personal leading. It is not distinguished
   by whether the outcome binds, and not by whether standpoints "advocate" (both business and
   clearness sittings can look identical procedurally) — it is distinguished by *who the
   standpoint claims to be speaking as*.

3. **Meeting with a concern** (labor / standing committee) — bounded or ongoing work a Meeting
   has taken under its care after a leading or business decision named it, carried out by
   however many are laboring, reported back on periodically, until spent or laid down.

The dividing test, in full, with worked examples, is `docs/three-practices.md`. Read that
before using anything else in this repo — it is the single most load-bearing document here.

**The hierarchy among them, made explicit** (business minute, 2026-07-03): in building and
maintaining code, concern-carried plural work is the ordinary state; the two meetings are
convened when a fork arises inside that work. The three forms remain distinct by their
structure and failure modes, not by their frequency. `SKILL.md` is the installable synthesis
written from that ground floor — if you want the fast path, start there and come back here
for the reasons.

**One thing these three are NOT the same axis as:** *who speaks.* A standpoint in either a
clearness sitting or a business meeting can be embodied as a person, as a concern ("the
correctness eye," "the newcomer's cold read"), or as a **file speaking in its own first-person
voice** about its own condition. That's a *mode* — how the standpoints are staffed — and it is
orthogonal to *which of the three practices is running*. See the callout in
`docs/three-practices.md`.

## Who this is for

Anyone running an AI coding agent (or agent team) who wants a real discernment discipline for
decisions that are contested, expensive to redo, or genuinely a matter of someone's taste
rather than a fact anyone could resolve. No familiarity with Quaker process is assumed, but if
you have some, `docs/quaker-correspondence.md` will tell you exactly what's preserved and what
had to bend.

## What's in here

- `docs/three-practices.md` — the dividing test between the three practices, with worked examples
- `docs/quaker-correspondence.md` — honest mapping to real Quaker terms and where it strains
- `docs/when-not-to-convene.md` — the anti-pattern list; when a full sitting is overhead in robes
- `roles/` — convener, clerk, recording clerk, light (participant), concern-carrier
- `templates/` — minutes template and light-prompt template
- `examples/` — one full worked example per practice
- `SKILL.md` — an installable Claude Code skill synthesizing all of the above

## What this deliberately does not include

An earlier, more experimental variant lets files not just speak but *refuse the work, ask to
be retired, or hold out as a standpoint that persists across sittings* — this depends on a
specific tool's graph/versioning model for representing "retired, not deleted" state, and
does not travel to a general audience. It is not documented here beyond this note; ask if you
want to know more.
