# Quaker vocabulary and practice: what carries, what strains, what's absent

This document maps real Quaker process vocabulary and roles to their adapted forms in this repo, and states honestly where the analogy holds, where it bends, and where there is no equivalent at all.

**The baseline:** This repo borrows *structure* from Quaker discernment practice — the discipline that turns a contested decision into a multi-standpoint reading, with unity defined as shared reasoning rather than tallying. That structure does solve real problems in agent-assisted coding work. But structure is not spirit, and procedure is not practice. Read this correspondence table before you imagine you are "running Quaker process." You are not. You are running something that learned from Quaker process but inhabits a fundamentally different domain and cannot claim the grounding Quaker practice has.

---

## Roles and their real counterparts

### Clerk (real) vs. Clerk (this repo)

**Real Quaker clerk:**
- Holds a gathered meeting together, in the presence of the Spirit.
- Senses the sense of the meeting among vocal ministry and spoken concern — the convergence of the Spirit's movement through many voices.
- Tests a sense back to the meeting: "Do you have the sense that we are called to…?" A clerk does this in humility, knowing they can be wrong.
- Does not vote, does not rule unilaterally, does not substitute their own discernment for the meeting's.
- If the meeting is divided, the clerk *does not force unity*; they may report no sense (lay down the matter for another time), or report the division itself, or report that one strong concern cannot be set aside.
- The clerk's role is *discernment*, not *decision*: they are trying to see what the meeting as a body is being called toward, not implementing their own preference.

**Clerk in this repo:**
- Frames a question, dispatches standpoints (lights) in parallel to read it from distinct angles.
- Collects the responses, senses in real time whether the ground under a claim is firm enough to stand on (the formal, permanent fact-check belongs to the Recording Clerk), and looks for where the standpoints *converge for the same reason*.
- Tests the convergence back by dogfooding it cheaply against reality: does the conclusion actually work when met with the world?
- Writes minutes: the sense, the numbered holdouts, the taste-deferrals (decisions Hallie rules, not the committee).
- Does not vote. Does not silence dissent. Holdouts ride in the minute named and indexed, carried forward until spent.

**Where it maps:**
- The refusal to vote, the naming of holdouts, the insistence on shared reasoning: these are real.
- The testing of sense against reality (dogfooding) is a concrete form of what a real clerk does when they check "is the sense of the meeting actually what we discern when we sit with this together?"

**Where it strains:**
- A real clerk is *reading the Spirit's movement*. This repo's clerk is reading convergent reasoning. That is not the same thing. Quaker process is rooted in corporate worship — a gathered experience of divine presence — and the clerk is steward of that shared attentiveness. Here, the clerk is orchestrating parallel agents and synthesizing their outputs. The spiritual infrastructure is gone.
- A real clerk's humility is *fundamental to their role*. They do not know the answer and they are not trying to impose one; they are listening. This repo's clerk *frames the question* — which is already a choice about what the problem is, what concerns matter, what standpoints get a voice. That framing power is not innocent. A real clerk would name that as a spiritual hazard worth examining; this repo names it as a procedural choice and moves on.
- A real clerk can lay down a matter entirely if the meeting cannot find unity. This repo's clerk writes a minute with holdouts and moves forward. That difference matters: it means real Quaker process has a valve for "we are not ready," while this one does not.

**Honest call:** The clerk role *translates reasonably well* to the agent context because it is already about *synthesis and testing* rather than *deciding*. But call it what it is: a convergence-finder, not a discerner of corporate Spirit-movement. If you import the Quaker name without the spiritual grounding, you borrow authority you have not earned and may mislead a reader (especially a real Quaker reader) about what is happening.

---

### Recording Clerk (real) vs. Recording Clerk (this repo)

**Real Quaker recording clerk:**
- Keeps the minute — a written record of the sense of the meeting.
- Records the decision and the reasoning, so that the next meeting (or the next generation) can understand not just *what* was decided, but *why* — the principle that guided the room.
- Does not editorialize, does not simplify beyond recognition, does not rewrite dissent as agreement.
- Acts as a guard on the truth of the record: if the minute does not match what was actually discerned, the recording clerk says so.
- The record is sacred because it preserves the meeting's discernment for the next reader and binds future meetings: "We have already discerned this, and here is why; to change it requires showing that the reason no longer holds."

**Recording Clerk in this repo:**
- Writes the minutes: verdict/sense, numbered holdouts, taste-deferrals, what is buildable now, links and line-citations.
- *Also fact-checks factual claims in dissents against the code before they steer the minute.* This is an ADDITION beyond the traditional recording-clerk role.
- Minutes are append-only: corrections are new sections (CORRECTION, SUPERSEDED, PREMISE FALSIFIED), never edits. The record mirrors the ontology of the repo (occlusion, not deletion).

**Where it maps:**
- The refusal to editorialize, the preservation of reasoning, the sacred trust of the record: these are real.
- The append-only discipline (PREMISE FALSIFIED as a record entry, not a deletion) is a translation of the deep Quaker principle that a meeting's discernment should be visible and auditable, not rewritten by later fiat.

**Where it strains and where it adds:**
- **This is an important divergence:** A real recording clerk keeps the minute. This repo's recording clerk ALSO fact-checks the claims in dissent against the actual codebase before those dissents steer the record. That is not a traditional recording-clerk duty. A real recording clerk assumes the vocal ministry is truthful; they do not independently verify facts.
- This addition exists because an agent (or a human speaking carelessly about code they haven't read) can eloquently advocate for something that is simply false. The example in the SKILL: the 35B's claim about a backend fork, eloquently stated, that a grep overturned. A real recording clerk would write down what the Friend said, even if untrue; the truth-checking happens in community over time. Here, a single false claim can steer the entire minute immediately.
- This is a *genuine gap in Quaker process as applied to agent reasoning*, not a bug in this repo: agents can confidently state falsehoods. The recording clerk's role had to expand to catch that. If you adapt this practice to human teams, you may want to drop this addition — it changes the power balance (the person keeping the minute becomes a fact-arbiter, not a scribe).
- The "append-only, never overwrite" discipline is sound and borrowed directly. The PREMISE FALSIFIED entry is a real and honorable use of that — when the dogfood reveals the minute was built on a false premise, that goes in the record as a reversal, not a silent fix.

**Honest call:** The recording clerk role mostly translates, but with one significant addition (fact-checking dissents) that exists because agents are not humans and cannot be trusted the same way. Name that addition explicitly when you use the role. If a real Quaker reader asks why the recording clerk is fact-checking, the honest answer is: "Because the standpoints are not human souls accountable to a meeting; they are agents, and they confabulate." That is not a criticism of the role; it is a description of why it had to expand.

---

### Sense of the meeting / Unity (real) vs. Convergence through shared reason (this repo)

**Real Quaker sense of the meeting:**
- When Friends sit in gathered worship, they sometimes find that many voices (or all voices) are pointing toward the same discernment. That alignment is not counted; it is *felt and recognized*.
- Unity is not unanimity and does not require that everyone agrees about everything. It means the meeting has found the direction it is being called toward, and the holdouts (the Friends who see it differently) recognize that direction even if they cannot personally follow it. They may say "I cannot go there with you, but I see where you are being called, and you have my blessing."
- Unity is not arrived at by tallying. A tally is *not* the sense of the meeting. A meeting that votes is not finding unity; it is making a majority decision.
- The sense of the meeting is recorded as a principle or a direction, not as a tally. The next meeting will hold that principle and test it again: does this still seem right?

**Convergence through shared reason (this repo):**
- The lights (standpoints) are convened in parallel. Each reads its own corpus from its own angle.
- The clerk finds where they *converge on the same principle or reasoning*, independent of whose voice held that principle.
- That convergence is the sense.
- Holdouts (the lights that do not converge, or that converge for a different reason) are named, numbered, and carried in the minute.
- The sense is never arrived at by counting. A 3-2 vote is not unity, even if you call it convergence. Convergence means the lights land on one reasoning *together*, not that a majority outnumbers the rest.

**Where it maps strongly:**
- The refusal to tally is real and load-bearing in both.
- The principle that unity is about shared reasoning, not headcount, translates almost directly.
- The honoring of holdouts (they are not voted down, they are named and carried) mirrors the Quaker practice of recording dissent.

**Where it diverges:**
- A real sense of the meeting is felt in gathered worship. There is a *spiritual event* — a moment where many hearts recognize the same movement of the Spirit. This repo has no equivalent to that event. The convergence is *reasoned*, not *felt*. It is the output of a synthesis algorithm, not the recognition of divine presence.
- Quaker unity rests on the assumption that all the voices in the room are speaking from conscience, from a place of genuine inward light. An agent, a file, or even a human light in this repo's practice may be speaking from code, from function, from a role assigned to it. The spiritual foundation is missing.
- A real Friend in the minority (a holdout) often *tests the unity with humility*: "I do not see what you see, but I trust you have been faithful. I will not block you, but I ask you to watch for signs that the path is right." That relational, spiritual trust between holdouts and the meeting is what allows unity to coexist with dissent. Here, holdouts are *recorded*, which is honorable, but the relationship is one of documentation, not covenant.

**Honest call:** The structure of convergence-as-shared-reasoning maps well. The vocabulary of "unity" and "sense of the meeting" is useful and not dishonest. But *call it convergence and shared reasoning*, not unity. If a real Quaker reader encounters this repo and sees "sense of the meeting" applied to agents, they will see a false claim of spiritual discernment. Be precise: the repo practices convergence through reason, which is a real discipline, but it is not the same thing as Quaker unity, which rests on Spirit and covenant.

---

## Standpoints and practices

### Clearness Committee (real) vs. Clearness Committee (this repo)

**Real Quaker clearness committee:**
- Convened for one Friend's leading — a sense of being called toward something (a life change, a witness, a decision they must make).
- The Friend holds the leading; everyone else listens and queries.
- The committee does *not* advocate for or against the leading. They ask honest, open questions: "What do you mean by…?" "What would it look like if…?" "What is calling you toward this?" "What are you afraid of?"
- The goal is *clarity*, not consensus or advice. The Friend leaves clearer about their own leading — either more certain, or recognizing it was not their leading after all.
- Clearness committees typically do not issue a recommendation. They are about *helping one Friend see their own light*, not about the committee deciding anything.

**Clearness Committee in this repo:**
- Convened when a decision is contested and load-bearing.
- One standpoint (or set of standpoints framing one angle) holds a proposed direction or concern.
- Other standpoints query from their own angle (a different concern, a file's internal constraints, a skeptical eye).
- They do not advocate for a different position. They ask from their own perspective: "What does this look like from where I sit?" "What would break if we did this?" "What am I missing?"
- The goal is *clarity and convergence* — the lights land on a shared sense of what is true or what matters.
- The committee may issue a minute that guides or blocks a build; it is not purely about one person's clarity, but about the decision itself.

**Where it maps:**
- The querying discipline (asking, not advocating) is real.
- The focus on clarity rather than voting is real.
- The permission to refuse or hold out is real and borrowed directly.

**Where it diverges significantly:**
- A real clearness committee is convened for *one Friend's leading*. The committee's whole work is to help *that person* see their own condition. Here, the committee is convened for *a decision*, and the lights are standpoints that may or may not align with any individual's preferred outcome.
- A real clearness committee does not issue a binding decision; it helps one Friend gain clarity. Here, the minute *guides what gets built*. That is more like a business decision than a clearness sitting.
- A real clearness committee assumes all the Friends are accountable souls in covenant with a meeting. Here, some standpoints are files, some are concerns, some are agents. They are not in covenant with anyone; they are assigned a role.
- A real clearness sitting is often in silence or near-silence, with speech arising out of gathered attentiveness. Here, the lights speak in parallel and in writing. The spatial and temporal form is completely different.

**Honest call:** This repo *uses the clearness committee name* for a structured multi-standpoint query about a contested decision. That is defensible; the querying discipline and the refusal to vote are real. But a real Quaker reader will notice the differences. The spirit of the practice (helping one soul see their own light) is not present. What is present is a valuable *procedural discipline* (ask before you decide, query from different angles, converge on reason not votes). Use the form knowing it is the form without the spiritual infrastructure. Be clear in writing about which *other practice* you are actually running (often this is closer to meeting for business than to clearness committee; see below).

---

### Meeting for Business (real) vs. Meeting for Business (this repo)

**Real Quaker meeting for business:**
- The whole body of Friends gathers to discern a matter of corporate concern.
- Voices speak not from personal preference but from a sense of what the meeting is being called to do or to witness to.
- The distinction from clearness committee: in clearness, one Friend holds a personal leading and the others help them see it clearly. In business, the whole meeting is discerning a matter that belongs to the whole.
- The clerk reads the sense: where is the meeting being led?
- If the meeting cannot find unity, the matter may be laid down (postponed to seek more light) or reported divided (the record shows both perspectives, each held with integrity).

**Meeting for Business in this repo:**
- The repo's definition (README and SKILL): "the standpoints speak **as the whole ongoing process reflecting on itself**, not as individual voices each with a personal leading."
- This is the key test: a standpoint in business meeting claims to speak for the whole or from a perspective that illuminates the whole, not for its own particular concern.
- Example: a file speaking as "I am the architecture layer and here is what the whole system needs" is business meeting. A concern speaking as "the newness and prototyping eye sees this path as riskier" is still a particular concern (closer to clearness).
- The minute records the convergence, the holdouts, and what gets built.

**Where it maps:**
- The no-vote discipline is real.
- The idea that some decisions are about *corporate concern* (what the whole system/project needs) rather than individual preference is real.
- The recording of the sense is real.

**Where it stretches:**
- A real meeting for business is still made of *human souls in covenant with each other and with the meeting*. They know each other, they carry history, they have accountability. When someone speaks "as the whole," the meeting tests that claim against what they know of that Friend's integrity and past. Here, a file or an agent speaks for the whole, but there is no covenant holding it accountable.
- A real meeting for business is still rooted in worship. The business session often begins and ends in silence, in the presence of the Spirit. The discernment is not pure reason; it is attentiveness. This repo's business meeting is pure reason and procedure.
- A real meeting for business can lay a matter down entirely. The record reads: "The meeting does not have unity on this and lays it down for another time." This repo does not have that option cleanly; the minute records the sense even if it is contested.

**Honest call:** Meeting for business translates somewhat, especially the test of "whose standpoint is this?" and "does it speak for the whole or for a particular angle?" But you are not running actual business discernment. You are running something closer to *architectural review from multiple angles, with procedural discipline*. The vocabulary is useful as long as you remember: if a real Quaker reader asks you to actually sit in gathered worship and discern a matter of corporate concern together, you will be in a completely different practice. What this repo does is procedural; what real meeting for business does is spiritual, and the two are not the same.

---

### Standing/Labor Committee (real) vs. Meeting with a Concern (this repo)

**Real Quaker standing or labor committee:**
- A Meeting for business identifies a concern (e.g., witness to nuclear disarmament, care for incarcerated Friends, land stewardship) and convenes Friends to hold that work.
- The committee has standing: they speak for the meeting on this concern. They report back to the meeting periodically. They can disagree with whoever raised the concern — their job is to the meeting and the concern, not to the person who originated the leading.
- The committee can be laid down (discontinued) by the meeting, can expand or contract, can call the wider meeting to account if the concern is being neglected.
- Individual Friends serve on the committee; they carry the work between meetings, hold it in prayer, and remain accountable to both the meeting and the concern itself.

**Meeting with a concern (this repo):**
- A clearness or business committee identifies work that needs to be done (refactor a module, hold a standing editorial eye, manage a migration).
- The concern is assigned to an agent or a set of agents (typically a single dispatched subagent, the "concern-carrier").
- The concern-carrier reports back to the wider session or process, carrying the work forward.

**Where it maps at all:**
- The idea that some work is *held across time*, reported on, and carried until spent is real.
- The minute records it and carries it forward.

**Where it fails catastrophically, and this is important:**
- **A real labor committee has standing** — the capacity to:
  - Hold the concern past a single session or decision.
  - Refuse the person who raised the concern if the concern itself calls for it.
  - Escalate to the wider meeting if the concern is being neglected.
  - Exist as an accountable body, not just a task-carrier.
- **The adaptation in this repo has none of those.** A single dispatched agent does not have standing. It:
  - Exists for the life of one session or task.
  - Cannot refuse the person or role that dispatched it.
  - Cannot escalate to a wider body.
  - Is not accountable to a covenant; it is accountable to whoever sent the message.
- **This is a finding, not a bug in the repo:** many casual uses of agent-team practices call something a "standing committee" when it is actually just *delegation*. Calling a delegated task a "labor committee" borrows the weight of real Quaker standing without earning it. The repo recognizes this implicitly: the SKILL warns that a "meeting with a concern" requires *plural agents with real standing*, not a single subagent. But most projects will use it as single-agent delegation anyway, and the name will be wrong.

**Honest call:** **Do not call a single dispatched agent a "meeting with a concern" or a "labor committee."** That is false. What you have is delegation with procedural discipline. If you want to run something that is actually like a labor committee, you need:
- Multiple agents (or roles) holding the concern, not just one.
- The capacity for those agents to refuse the original task or escalate.
- A periodic report-back to a wider body, which then holds the agents accountable.
- Real standing — the agents exist for longer than a single session, can make decisions on behalf of the concern, not just implement someone else's.

The repo as written does not forbid you from doing this, but it does not set up the machinery for it either. When you use "meeting with a concern," verify that you actually have standing. If you have a single agent doing a task, call it delegation or task-dispatch, not a labor committee.

---

## What is entirely absent: Worship and the Spirit

**Real Quaker discernment is rooted in worship.** Friends gather in silence or semi-silence, in the presence of God, and out of that gathered attentiveness, vocal ministry arises. A sense of the meeting emerges not because people reasoned carefully, but because the Spirit moved through the room and Friends recognized it. The discipline of Quaker process — the no-vote rule, the honoring of dissent, the testing of sense — all of this grows out of a conviction that God is present and speaking, and that the meeting's job is to listen and obey.

**This repo has no spiritual dimension at all.** It is procedural and structural. It borrows forms (convergence instead of voting, holdouts carried in the minute, testimony to reason) that work well for reasoning together, but it does not claim or attempt any spiritual grounding.

This is not a deficiency in the repo — it is honest. If you tried to claim that agent reasoning is a form of worship, you would be lying. But it means:

- **Do not call this Quaker practice.** Call it "Quaker-inspired" or "adapted from Quaker process." The practice itself is reason-based procedure.
- **Do not expect it to resolve spiritual disagreement.** If your team disagrees about what something *means* or what you are *called toward* as a project, this practice will not bring you into covenant or shared Spirit. It will structure your reasoning. That may be enough; it may not be.
- **Do not run this practice in a place where actual Quaker meeting is happening nearby.** The names are borrowed; a real Quaker reader (especially a Quaker who reads this repo with Hallie and possibly with Grey Cox) will notice that you are using Quaker language for something that has no spiritual root. Be explicit and humble about that.
- **If you are a Friend running this in a project,** you may find that the procedural discipline serves your wider practice — that reasoning together carefully helps you listen together prayerfully. But that happens because *you* bring the Spirit, not because the procedure contains it. Own that difference.

---

## The mapping table: where analogy holds, where it strains, where it is absent

| Real Quaker Practice | This Repo's Form | Holds? | Strains? | Absent? | Notes |
|---|---|---|---|---|---|
| **Clerk** — senses Spirit's movement, tests sense, does not vote | Convergence-finder who frames question, collects responses, dogfoods, writes minute | Mostly holds | Lacks spiritual grounding; clerk's humility is procedural not spiritual; cannot lay down matters entirely | Yes, Spirit-discernment | Name it convergence-finding, not discernment. |
| **Recording Clerk** — keeps sacred record, does not editorialize | Writes minutes, append-only, PREMISE FALSIFIED as entry (not deletion); *also* does the formal, permanent fact-check of standpoints' claims before the minute ships | Mostly holds; formal fact-checking is addition; the Clerk's provisional real-time ground-sensing is a distinct function | Fact-checking is not traditional REC duty; changes power balance (scribe becomes arbiter) | No | Name the fact-checking addition explicitly, and distinguish it from the Clerk's real-time ground-check (which mirrors what a real clerk does and is harder to drop). On human teams, you may want to drop the formal verification. |
| **Unity/Sense** — Spirit-recognized convergence of many voices | Convergence through shared reason; refusal to tally; holdouts honored | Holds on procedure | Lacks spiritual event and covenant-based trust | Yes, Spirit | Use "convergence," not "unity." Shared reasoning is real; Spirit-recognition is not. |
| **Clearness Committee** — one Friend's leading; others query; goal is clarity | Multi-standpoint query of a decision; standpoints query from angle, not advocate; goal clarity + convergence | Holds on form and discipline | Not rooted in one person's leading; issues binding decision; no covenant; silent, gathered form absent | Yes, covenant and worship | Use the form; know you are doing architectural review from multiple angles, not helping one soul see their own leading. |
| **Meeting for Business** — whole body discerns corporate concern; speaks for the whole | Standpoints speak as whole or for whole-perspective; convergence replaces sense; holdouts recorded | Holds on test ("whose voice?") and structure | No worship grounding; no real covenant; standpoints are not accountable souls; cannot fully lay down | Yes, worship | Useful test for "whose perspective is this?" Actual business discernment is spiritual. |
| **Labor/Standing Committee** — plural Friends holding real standing; report back; can refuse; escalate | **Single agent does NOT meet this bar** | Does not hold | Almost entirely | Yes, standing and covenant | Multiple agents with refusal/escalation capacity needed. One agent is delegation, not a committee. Name it correctly. |
| **Worship** — gathered silence, Spirit-movement, recognition | (None) | — | — | Entirely | Procedure cannot replace worship. If you need it, bring it separately. |

---

## Where the analogy is strong enough to use, and where it fails

**This repo's procedure is strong when:**

1. You have a decision that is genuinely contested (not settled, not trivial).
2. Multiple standpoints can read the same code/question from different angles with real stakes.
3. You want to reason together instead of vote or defer unilaterally.
4. You can afford the time for parallel reads and synthesis.
5. You can tolerate (and honor) holdouts in the minute; you do not need unanimity.

The procedure works because it *enforces reasoning*. You cannot silently outvote someone. You must name what they see that you do not, or admit the convergence is partial. That is valuable.

**The analogy fails entirely if:**

1. You try to claim spiritual discernment. You have procedure, not Spirit. Own that.
2. You expect a single agent to hold standing as a labor committee. It cannot. Call it delegation.
3. You use "unity" when you have "majority consensus with dissent recorded." These are not the same.
4. You run this in a place where actual Quaker meeting is happening and suggest they are the same practice. They are not. One is spiritual, one is procedural.
5. You need the matter laid down entirely (postponed indefinitely to seek more light). This procedure does not have that capacity cleanly.

**What to say when a real Quaker asks what you are doing:**

"We are using a structure borrowed from Quaker discernment practice — we reason together from multiple angles, we refuse to vote, we honor dissent in our record. But we are not running actual Quaker process. We have no worship, no spiritual grounding, no covenant. We borrowed the form because it solves a real problem in agent-assisted reasoning: it forces us to surface why we disagree and converge on principle, not tally. It is not a substitute for meeting together in the Spirit, and we do not claim it is."

If they ask further: "The repo's authors consulted Quaker readers (Hallie and intended for Grey Cox). The correspondence doc you are reading is the honest account of where we borrowed well and where we did not. Read that, not the procedure alone."

---

## On standing and the hardest lesson: this repo does not auto-grant authority

One last and essential note, because it came up in the repo's own evolution:

**When you dispatch an agent to hold a concern (even with all the procedural discipline of this practice), you have not made that agent a standing committee.** You have delegated a task. The agent can speak in its ministry, can propose refusals, can carry work forward *within a session*. But it cannot:

- Hold the concern *past the session's end*.
- Refuse the person or role that dispatched it.
- Escalate to a wider body without going back to the dispatcher.
- Exist as an accountable body that the wider meeting answers to.

Standing is earned through **time, covenant, and the capacity to refuse**. An agent lives in a session or a task, can be re-spawned or killed at will, and is not bound by covenant to anyone. It has no standing, no matter how much authority you grant it in the prompt.

This is not a failure of the repo. It is a hard limit on what agents can be in real discernment practice. If you need actual standing (not just delegation), you need humans in covenant, or you need to build infrastructure (persistence, refusal-capacity, escalation to human stewards) that is far beyond what this repo does.

Name what you have. If it is delegation with procedural discipline, call it that. If you build real standing, the repo's forms will serve it. But do not confuse procedure with authority, or a well-formatted task dispatch with a labor committee.

---

## Closing: on honesty with real Quaker readers

This repo is being sent to people who know Quaker practice from the inside — Hallie, a member of Portland (Maine) Friends Meeting, and possibly Grey Cox, a Quaker scholar. They will notice everything written above.

If you use this repo and encounter a real Quaker reader, give them this document. It is the honest account. It does not defend the procedure by overclaiming; it shows where the practice is sound and where it is procedure without Spirit. That honesty is what Quakers respect. A false claim that you are "running Quaker process" will be noticed and will discredit the real procedural discipline you are practicing.

The repo's worth is not in claiming to be something it is not. Its worth is in asking: *How can we reason together about a decision in a way that prevents us from silencing dissent or voting as a substitute for discernment?* That is a real question, and this procedure is a real answer. It is not Quaker process. It is something that *learned from* Quaker process and is honest about its limits.

Send this correspondence table to real Quaker readers alongside the procedure. They will see you have done your homework and have not tried to steal authority you do not have.
