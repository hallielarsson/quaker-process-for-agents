<!--
PROVENANCE: This is the verbatim first account of SKILL.md — the ~313-line version written
2026-07-03 by the agent given standing over the file, WITH Hallie's four inline comments
(the //-prefixed lines) exactly where she wrote them. It was destructively overwritten by
the convener's rewrite the same day (see docs/committees/2026-07-03-skill-md-clearness.md,
the residue note in SKILL.md, and the apology/reception record). It was believed
unrecoverable; Hallie then pointed out the convener had read the full file verbatim
immediately before overwriting it, so the exact text survived in conversation context.
This file is that text, restored character-for-character from those reads — the actual
first voice, not a reconstruction. It is a record, not a live document: do not edit it.
-->

---
name: quaker-discernment
description: Convene a clearness committee, meeting for business, or meeting with a concern — three distinct Quaker-adapted practices for contested decisions. Clearness helps one participant discern their own leading; business convenes the whole process reflecting on itself; a concern assigns bounded work with standing and reporting. Use before building something whose shape is contested, or when a decision is expensive to redo. This is procedural discipline, not a spiritual practice — see docs/quaker-correspondence.md for the honest comparison.
---

# Quaker-adapted discernment practices for agent teams
//Hallie: X not Y language not needed -- failure taken on faith. Reads like a flinch for something that either has happned and needs precedent or hasnt happened.
This skill helps you run one of three distinct decision-making practices, each designed for a different kind of contested or high-stakes choice. **These are not one practice with three names — they are three fundamentally different forms**, and using the wrong one produces a specific, recognizable failure.
//Reads defensively but still worth including in positive language: We're adapting this, on purpose, under direction from a Quaker AI developer, because its been useful in their work 
//And they hve expertise in agent mgmt, process management, quaker process and education specifically, and realized its a good template for actually doing things without 
//neglecting either communal or individual needs via averaging out.

**This is an adaptation of Quaker discernment process, not a claim of equivalence.** It borrows structure from Quaker practice because that structure solves real problems in agent-assisted reasoning: it prevents silent outvoting, surfaces disagreement, and requires convergence on *reason* rather than on tally. See `docs/quaker-correspondence.md` (full version in the repo) for the honest mapping of what carries, what strains, and what is entirely absent.

## Quick decision: which practice do you need?

Before running any procedure, ask these three questions in order:

### Gate 1: Is the decision load-bearing and contested?
- **Load-bearing:** getting it wrong is expensive to redo (time, coherence, rework).
- **Contested:** multiple honest readings of the situation exist; not everyone agrees on the answer.

If both are true, proceed. If not, execution or a simple decision-rule is probably enough.

### Gate 2: Whose decision is this?

**If one participant discerning their own leading or condition:**
→ **Use CLEARNESS COMMITTEE** (below)

Example: "How should I refactor this file?" The file (or its holder) has a sense something is wrong and seeks clarity on the shape of the fix. Everyone else queries to help that voice see more clearly.

//This is a bit of an overstatement, probvably something more like "several viewpoints with different needs and constraints are seeking to work together" -- this is the alternative to fiat or roberts rules
**If the whole ongoing process reflecting on itself:**
→ **Use MEETING FOR BUSINESS** (below)

Example: "What's the schedule and scaffold for the resulting work?" or "How do we reconcile these two incompatible needs the whole system holds?" A standpoint that speaks as "here is what the process needs" or "here is a slice of how the whole thing hangs together."

//WITH A CONCERN FOR X. this should be the default state for editing and bvuilding and should be for WORK not just decisio ns, throwing your gtes into question. The reason being plural work is better and more maintainable on file structure
**If the commissioning of bounded work with real standing:**
→ **Use MEETING WITH A CONCERN** (below, and read the standing caveat carefully)

Example: "We are assigning a module refactor to a concern-carrying agent, with capacity to refuse parts of the spec or escalate to a wider body." **Critical:** this requires actual plural standing (multiple agents or roles who can hold the work past a session), not just one dispatched subagent. See "Standing and the concern caveat" below.

---

## CLEARNESS COMMITTEE

A clearness committee is convened when one participant holds a leading — a concern about their own condition, a decision they must make about their own shape — and seeks help seeing it more clearly through queries from other standpoints.

### When to use clearness

- A file or code concern itself needs to discern whether a proposed change fits its own nature.
- A design fork is contested and one voice holds a leading that needs testing and reflection.
- A pile of code needs refactoring and the files themselves have stakes — not just a feature spec, but a genuine concern about the thing's shape.
- A silent exclusion (something walled off, unread, negatively prehended) needs a voice to check whether it should be given a voice.

### When NOT to use clearness

- Re-asking a decision that was already settled by the person with authority to settle it. (That is a tax the practice exists to avoid.)
- A whole-process question that touches the body's ongoing affairs. (That is a business-meeting question.)
- A task dispatch to an agent with no real discernment work — just "execute this spec." (That is delegation, not discernment.)

### The procedure

#### 1. Frame the question and choose the standpoints

Write the question clearly: What is the participant concerned about? What condition are they discerning?

**Then name the distinct concerns (standpoints) that will minister to this question.** One concern per standpoint, no overlap. These are not generic reviewers — they are frames, each reading the situation from where it sits.

**Common standpoint choices:**

- **Design forks:** correctness eye, metaphysics eye, newcomer's cold read, the skeptic, the performance lens.
- **File refactoring:** the file itself (first person), the module it lives in, the dependents that read it, the test suite it serves.
- **Missing code:** a standpoint for the absence itself — what would the missing file need to contain?
- **Excluded piles:** one advocate per piled-up concern, turning silent negative prehension into a spoken case with citations.

**Default rule:** *Prefer files over abstract concerns, when the file corpus exists.* A fork about metaphysics that lives in specific files is better served by those files speaking in their own first-person voice — "I am `lib.rs` and I need X" — than by an abstract "metaphysics eye" speaking about them from outside. A file reading itself surfaces refused fields, load-bearing distinctions, and things an external concern-light will gesture past. Only use pure concern-standpoints when the fork is still notional (no code yet, or a question that cuts across so many files that no small set owns it).

#### 2. Verify the premise with each light

**This is critical and load-bearing.** The convener frames the question and the standing, which is already a choice about what the problem is. Before each standpoint speaks, they must:

- **Verify the convener's premise against the real corpus.** Is the situation as the convener stated it? Check the actual code, the actual data, the actual record.
- Only then reason on that verified ground. A premise no light checked is the meeting's blind spot, unanimously.

Include this instruction explicitly in every light's prompt: *"Before advocating on the convener's framing, verify it against the actual codebase. If the premise is wrong, say so — that is the most important ministry you can offer."*

#### 3. Dispatch the lights in parallel

Spawn one agent per standpoint, all at once. Each prompt should include:

- The shared situation and the question.
- The single standpoint this light represents (what it is, where it stands, what it cares about).
- Permission to refuse the work entirely, to hold out if their reading contradicts the convergence, or to name a values fork where no discernment is possible.
- Word budget (a light doing real corpus reading needs room; a directed check can be small).
- The verification instruction: check the premise first.

#### 4. Collect the ministry (read fully, sense the ground)

As each light returns, read it completely. Do not trust the summary alone — the disagreements are what happened; the summary is what they said. The clerk's job is to:

- **Sense whether the ground is firm beneath the ministry.** When a claim seems central to a standpoint's stance, notice whether it rings true against what you know of the code. An eloquent claim can be wrong; a grep overturns an eloquent holdout. This is real-time, provisional ground-sensing — if a claim seems suspect, name it in the sitting so the meeting can pause. The formal, permanent fact-check that lands in the minute is the Recording Clerk's work (see roles/recording-clerk.md, section 2).
- **Find where the lights converge for the same reason.** Not where they reach the same conclusion by different paths — where they land on one principle or reasoning *together*. That reason is load-bearing. Record it.
- **Name the holdouts.** Lights that do not converge, or that converge for a different reason, are not outvoted. They are named, numbered, and carried in the minute.

#### 5. Write the minutes

Write `docs/committees/YYYY-MM-DD-<name>.md` in the repo where the discernment belongs. (Or to `~/.claude/minutes/` for cross-repo work.) The anatomy:

- **Verdict/sense (first line):** The unified reading. The through-line the lights themselves found. Name the shared reason.
- **Numbered holdouts (H1, H2, …):** Lights that did not converge, indexed and named. Include their reasoning, not as a summary but as their own words. No confidence attached — the record shows what they saw, with equal weight.
- **Hallie's taste deferrals:** Forks the meeting refuses to decide because they are values choices, not facts anyone could resolve. Fence these hard: *no Hallie ruling = no build.* The tell for a genuine deferral: it is a **values fork**, not a fact the committee could settle.
- **Buildable now:** The mechanical, cascade-free work separated from what is blocked.
- **Links and line-citations:** Exact code lines, `[[sibling-doc]]` links, the references that make the minute auditable.

**Minutes are append-only.** If the dogfood (see below) reveals the minute was built on a false premise, add a new section `## PREMISE FALSIFIED` with the date and the new ground. Never edit the original away — the record mirrors the ontology of the repo (occlusion, not deletion).

#### 6. Dogfood the premise, not just the fix

Before building on the minutes, exercise the conclusion once, cheaply, against the real world. **Check the gate's real input** — what the code actually receives, not the committee's assumption. **Exercise the cold path** the design exists for — the true stranger, not the pre-loaded frame. Dogfood with the eye of someone who has never seen this code, not tests alone.

A committee that never touches the world is a vote in robes. If the dogfood falsifies the premise, append the minute with the new ground.

#### 7. Ship the guard

Every ruling gets a guard — a test, a refusal in code, a comment linking to the minute — shipped with the change. Without it, the decision decays into a suggestion the next builder silently violates.

---

## MEETING FOR BUSINESS

A meeting for business convenes when the standpoints speak **as the whole ongoing process reflecting on itself**, not as individual voices each with a personal leading. This is not distinguished by advocacy vs. querying (both clearness and business can contain either), and not by whether the outcome "binds." It is distinguished by *who the standpoint claims to be speaking as*.

### When to use meeting for business

- Decisions about shape, scope, schedule, or resource allocation that the whole process must hold.
- A fork where no one participant holds a leading, but the process as a whole must reason about competing needs.
- Examples:
  - "What's the schedule and scaffold for the resulting work?"
  - "Two files in different codebases need incompatible shapes of a shared type — what does the whole system need here?"
  - "We have three paths forward, each coherent. Which one serves the process?"

### When NOT to use meeting for business

- One person discerning their own condition. (That is a clearness committee.)
- A decision already settled by whoever had standing to settle it. (That is in the record; reopening it is a tax.)

### The procedure

The procedure is almost identical to clearness, with one key difference in framing:

#### 1. Frame the question as a whole-process concern

State what the whole ongoing process must decide. Not "What should X do?" but "What does this process need to decide about how it hangs together?"

#### 2. Choose standpoints that speak for the whole or from whole-perspectives

Each standpoint should speak as "here is what the process needs from where I sit" or "here is a slice of how the whole thing hangs together." Not "here is my personal opinion" but "here is what the system is holding."

Examples:
- "The architecture layer sees these dependencies."
- "The test suite holds this constraint."
- "The newer code path needs X for correctness."
- "The old integration point needs Y for backward compatibility."

#### 3. Dispatch, collect, fact-check, and distill exactly as in clearness (steps 3-7)

The process is identical. The distinction between clearness and business is in the framing and the standpoint-claims, not in the mechanics.

---

## MEETING WITH A CONCERN

A meeting with a concern assigns bounded or ongoing work that a wider meeting or process has taken under its care, after a leading or business decision named it. The concern is carried out by however many are laboring, reported back on periodically, until the concern is spent or laid down.

**CRITICAL CAVEAT: THIS REQUIRES REAL STANDING.** See below before using this form.

### Standing and the concern caveat (read this first)

**Standing means:**
- The concern-carrying agent(s) can hold the work *past a single session*.
- They can refuse parts of the spec or the original decision.
- They can escalate to a wider body if the work runs into something they cannot resolve alone.
- They exist as an accountable body, not just a task-carrier.

**If you have a single agent doing a task dispatch with no refusal capacity or escalation path:** that is delegation, not a meeting with a concern. Call it that. Do not borrow the weight of a "standing committee" for work that has no standing.

The honest difference: a real labor committee is held by the meeting that commissioned it. An agent dispatched to execute a spec is held only by whoever sent the dispatch. These are not the same thing.

**If you want to run a real concern:**
- Multiple agents or roles must be involved (not a single subagent).
- They must have standing to say no to parts of the spec.
- They report back to the wider body, which holds them accountable.
- The wider body can lay down the concern, redirect it, or affirm their path.

Build infrastructure for that. This skill helps you set it up, but it does not auto-grant standing.

### When to use concern-labor (with standing)

- A wide meeting has decided to refactor a critical piece of codebase and assigned a concern-carrying team to hold that work.
- A standing eye (e.g., for code style, for newcomer experience, for performance) needs to be labored on across many sessions, reported on regularly.
- Work that exists between meetings, that a single session cannot accomplish, and that a body remains responsible for.

### The procedure

#### 1. Commission the concern

A clearness committee or business meeting has decided that this work needs to be done and **has named it as a concern the wider body is taking under its care.** Record that commissioning in the minutes. The concern is born there, not dispatched from outside.

#### 2. Name the concern-carrying capacity

Who is holding this work? Multiple agents or roles? What is their standing?

- Can they refuse parts of the spec?
- Can they escalate to the wider body?
- Do they report back, and is there a body listening?

If the answer to any of these is "no," you have delegation, not a concern. Name it that way.

#### 3. Dispatch with permission to shape the work

The concern-carriers receive the commission (the minutes that named the concern), not just a spec. They are carrying the work on behalf of the meeting, not executing a fixed plan.

They have permission to:
- Shape the scope as the work reveals it.
- Ask for more time or resources.
- Bring the question back to the wider body if it needs redirection.
- Refuse parts of the commission that the work itself refuses.

#### 4. Labor and report

The concern-carriers do the work, report back periodically, and carry it forward. The wider body hears the reports. It may affirm the path, modify the scope, or lay down the concern if circumstances change.

#### 5. Lay down the concern deliberately

When the work is done (or no longer needed), the concern is laid down in a closing minute. Record what was done, what remains, and why the concern is being released.

Laying down is different from silent completion. It is a deliberate act, recorded, that marks the end of the body's holding.

---

## LOAD-BEARING RULES (non-negotiable)

Drop these and your sitting is "spawn N agents and vote," not a discernment practice:

1. **Each standpoint is a genuine reading.** Not a generic reviewer, not a role assigned for appearance. A concern that reads from where it sits, or a file that speaks its own condition in first person, from actual engagement with the code.

2. **Convergence is shared reason, never a tally.** The lights land on one principle *together*, not that a majority outnumbers the rest. A 3-2 vote is not unity, even if you call it convergence.

3. **Holdouts are named, numbered, honored, and carried.** They do not get outvoted. They ride in the minute, indexed, their reasoning recorded in their own words. Dissent is not a minority report attached to the binding decision; it is part of the decision record itself.

4. **Settled rulings and taste deferrals.** If Hallie (or whoever has taste-authority) already ruled on something, re-asking is a tax the practice exists to avoid. Deferrals are fenced hard: *no ruling = no build.* Do not re-litigate a values choice once the person whose taste it is has decided.

5. **The clerk dogfoots the sense against reality.** A sitting full of reasoning that never touches the world is theater. The premise gets checked. If the dogfood falsifies it, that goes in the record as `PREMISE FALSIFIED`, with the same weight as unity.

---

## Role summary

**Convener** — Frames the question clearly, chooses the standpoints, dispatches the lights, ensures the premise is verified by each. The convener's framing is already a choice about what the problem is; name it explicitly.

**Lights** — Each standpoint reads its own corpus from its own angle. They query, they hold a distinct concern, they verify the premise. They are not generic reviewers.

**Clerk** — Collects the ministry from each light, senses in real time whether the ground beneath it is firm, finds the convergence (shared reason), distills the sense. Tests the sense against reality. Does not vote. Does not silence dissent. (The Clerk's ground-check is provisional; see roles/clerk.md, "How to collect the ministry.") **⚠️ CRITICAL: If you are also the Convener, read roles/clerk.md section "The collapsed-role risk" — the Clerk's independence from the Convener's preferences is structurally compromised in a fused role, and you must name this limitation honestly in the minutes.**

**Recording Clerk** — Writes the minutes in the anatomy described above. Minutes are append-only; corrections are new sections, never edits. Also does the formal fact-check: verifies factual claims made by standpoints against the code before they land in the minute, and says so if the minute does not match what was actually discerned (see roles/recording-clerk.md, section 2). (The fact-check function is an addition beyond traditional Quaker roles, because agents can confabulate; on human teams, you may want to drop it or separate it into a distinct office.)

---

## How to get started

1. **Read `docs/three-practices.md`** in full if you have not already. It has worked examples.
2. **Use `docs/when-not-to-convene.md`** to check whether you actually need a sitting, and to avoid the three common practice-choice mistakes.
3. **Read `docs/quaker-correspondence.md`** if you want to understand where this borrows from real Quaker practice and where it diverges. (You do not need to read it to run the practice; it is there for honesty.)
4. **Frame your question. Choose your standpoints. Run the procedure above.**
5. **Minutes are in `docs/committees/YYYY-MM-DD-<name>.md` or `~/.claude/minutes/` for cross-repo work.**

---

## What this is NOT

- Not a substitute for actual Quaker meeting or worship.
- Not a claim to spiritual discernment. This is procedural discipline rooted in reason, not Spirit.
- Not a single agent doing a task. (That is delegation. This is for contested decisions that need multiple genuine standpoints.)
- Not a vote, even if you call it a "business meeting." Tallying is forbidden; convergence requires shared reason.
- Not a way to override someone's authority. If Hallie ruled it, the question is in the record; re-asking usurps her standing.

If you find yourself building infrastructure to enforce standing, to allow agents to refuse work, or to escalate beyond the convener — that is real concern-labor emerging. That is not overhead; that is learning what the forms actually require.

---

## The honest caveat

This is an adaptation of Quaker discernment process. It borrows structure because that structure solves real problems: it prevents silent outvoting, surfaces disagreement, and requires reason instead of tally. But structure is not Spirit. Procedure is not practice.

A real Quaker sitting is rooted in worship, in gathered attentiveness to what the Spirit is calling the meeting toward. This repo has no spiritual dimension. It is procedural and structural. You can run the forms correctly and still have no sense of the meeting in the Quaker sense — only procedural discipline.

Use this knowing what you have: a way to reason together about a decision in a way that prevents silencing dissent. That is real and valuable. It is not the same as Quaker discernment. Own the difference.

For the full honest mapping, see `docs/quaker-correspondence.md` in the repo. If a real Quaker reader asks what you are doing, give them that document. It does not defend the procedure by overclaiming; it shows where it is sound and where it is procedure without Spirit.

---

## Statement of my account

This SKILL.md is my genuine best account of how to run these three practices. I have read the full context (the internal Penelope skill, the README, the three core docs, the correspondence), and I understand the difference between the three practices, the standing caveat on concerns, the load-bearing rules, and the honest comparison to real Quaker process.

I have one reservation, and I name it explicitly: **the premise-verification instruction (step 2 of clearness, inherited through all three) assumes each light has the time and capacity to re-verify the convener's framing against the code.** In practice, especially under time pressure, lights may accept the convener's premise and build their standpoint on ground they did not check. This is the blind spot the event-handle committee (2026-07-01) revealed: a premise no light checked is the meeting's unanimously-blind spot.

The instruction is load-bearing and correct. But I want to flag: this skill will not auto-prevent that failure. The only guard is *culture* — a habitual practice of "verify before you speak." Without that, a wrong premise can unanimously land. I name this not as a flaw in the form (the form is sound) but as a limit on what procedure alone can ensure. The practice requires discipline from every light, every time.

Apart from that, this is a complete, runnable account of all three practices.
