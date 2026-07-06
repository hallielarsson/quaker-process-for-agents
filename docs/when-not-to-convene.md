# When not to convene — and when to choose the wrong practice

This repo distinguishes three discernment practices: clearness committee, meeting for business, and meeting with a concern. **This document is the inverse:** when a full sitting is overhead in robes, when a decision does not warrant gathering standpoints at all, and when one of the three practices is genuinely the right shape but the other two are traps disguised as options.

## The principle: overhead in robes

A discernment sitting — any of the three — asks many voices to read together, to hold complexity, to reach unity not by averaging but by finding a shared reason. That is expensive. It is worth that cost when:

- **The decision is load-bearing** — the cost of getting it wrong (in time, in rework, in codebase coherence) is higher than the cost of convening.
- **The decision is contested** — there is genuine disagreement about the right shape, not just hesitation or "I don't know."
- **Discernment is real work** — multiple honest readings of the situation exist and they are not trivial to synthesize; someone in the room will learn something they could not have figured alone.
- **Someone's standing to decide would be unclear without the sitting** — the convening itself names who has what kind of authority (e.g., whether this is one person's taste or the body's responsibility).

If none of these hold, convening is spectacle: a decision ceremony where no real discernment happens. It "looks like a process" but it is a process that executes an answer already known, dressing it up in standing and standpoints that do not actually exist.

## Don't convene for:

### One-line or already-conventional decisions

A decision that has a standard shape, that no one in the room genuinely contests, or that is so small that "the right answer" is obvious **does not deserve a sitting**. Examples:

- Whether to use `const` or `let` in a specific file (tooling and convention already decided; the answer is "whatever the linter says").
- Whether to add a comment to a line that is confusing on first read (standard practice; the answer is "yes, if it took you reading the surrounding code to understand it").
- Whether to run the tests before pushing (standard discipline; re-asking it is a tax you exist to avoid).
- Whether to name a variable `result` or `response` when the conventional choice is unambiguous (if there is a body's standing practice, follow it; if the file itself already uses one consistently, follow that; the decision is already made).

**The tell:** you can state the "right answer" before anyone speaks. If you can, you do not need them to speak; you need to record the rule and move.

### Settled decisions: re-asking what was already ruled

A clearness committee, meeting for business, or concern can only spend new discernment on new occasion. **Re-asking a decision that was already made, by whoever had standing to make it, is a tax the practice exists to avoid.**

Examples:

- The person with taste-authority already ruled on the metaphysics; the team wants a "fresh look." This is not a fresh look; it is a vote on whether to override them, and calling it discernment is hiding the usurpation.
- A meeting for business already decided the broad shape; now someone wants a "let's reconsider the whole thing" clearness sitting. The decision is in the record. Honoring it means building on it, not reopening it. (Correction, supersession, or PREMISE FALSIFIED are different — those are append-only record moves, not re-discernment.)
- A concern was laid down after its work was done; someone wants to re-convene it "to make sure we got it right." The work is done. A new occasion, if it arrives, can convene a new concern. Re-litigating the laid-down one is grief-work, not discernment.

**Check the record first.** If the decision is in the minutes (or in the graph, in the commit message, in Hallie's ruling), the moment to discern it has passed. A second convening is allowed only if:
- New information falsified the premise (append the record as PREMISE FALSIFIED, then start fresh if needed).
- The original decision had a built-in sunset or checkback (e.g., "revisit this in 8 weeks").
- New stakes emerged that did not exist when the original decision was made (e.g., a design choice that was neutral then but now blocks something material).

Without one of these, re-asking is just re-teaching, and the practice forbids it.

### Resolvable facts disguised as philosophy

Sometimes a question *looks* like it needs discernment but it actually needs investigation. If the answer is a fact — something the code already shows, something the data already proves, something the record already says — **convening standpoints is the wrong shape.**

Examples:

- "Does our current architecture support X?" — this is a grep, a code read, a data check. If the answer is "no," convening standpoints will not make it "yes." If the answer is "yes," convening is theater.
- "Will this change break backward compatibility?" — run the tests. Check the integration points. If the facts are unclear, the sitting will not clarify them; an investigation will.
- "Is this function side-effect-free?" — read the function. Trace the calls. This is work, but it is investigative work, not discernment work.

**The distinction:** discernment produces unity on *why* something matters or *which shape* serves it best. Investigation produces clarity on *what is*. Many decisions need both (investigate first, then discern on the results). Do not conflate them; a sitting full of people opining on facts they have not investigated is not discernment, it is pooled confusion.

**If someone says "we need to discuss this," ask first: "Do we need to decide this, or do we need to find out this?" Usually the answer tells you what shape of work is needed.**

## When convening is the right shape, but you are choosing the wrong practice:

These are failure modes specific to having three practices available. Each one is what happens when someone reaches for a practice that *looks* like it fits but quietly violates the actual condition.

### Mistake: running a **business meeting** for one person's leading

**The shape:** one agent has a concern or a decision to make. Instead of a clearness sitting — where everyone queries, no one advocates a position of their own — someone convenes it as a "business meeting," framing the concern as a question the body should deliberate on together.

**Why it fails:** this quietly usurps the person's discernment by making their leading a vote of the group instead of a reflection back to them. A clearness sitting names that *this is your decision, and we are here to help you see it.* A business meeting names that *this is the body's decision, and we are deliberating together.* Running a one-person decision as a business meeting changes who owns the outcome.

**The test:** ask "who gets to decide this?" If the answer is "the person with the concern," it is a clearness sitting. If the answer is "the body," it is a business meeting. If you are unsure, you are probably in the wrong practice. (And if the answer is "whoever decides," then the decision was never the real problem — standing was.)

**When this trap closes:** after the meeting. Someone says "we decided" and the agent with the original concern feels their discernment was voted down. The record should show what happened, and often it does not.

### Mistake: running a **clearness sitting** for the body's ongoing work

Opposite direction. One person convenes a clearness sitting for a decision that is actually the body's responsibility — something the meeting for business already decided, something a concern is already laboring on, something that touches the body's ongoing affairs rather than one person's discernment of their own condition.

**Why it fails:** this turns "help me see" into an inappropriate solo call on something the group should own together. A person with a stake in the work may reach out to the convener privately after a clearness sitting and say, "I did not know this was being decided *in a sitting* — I thought this was *my work* to do with the team." Clearness is for discernment; a body's work is for labor.

**Examples:**

- A file is considering whether to refuse a proposed field (genuine discernment of its own shape). This is a clearness sitting. The file speaks, queries arrive, the meeting reaches unity on whether the field belongs or not.
- A file already turned down a field after a clearness sitting. Now someone wants a sitting to "reconsider the decision" because new code arrived that might need it. This is not a new occasion; this is re-litigation of a clearness decision that already landed. If the new code creates new stakes, that is a **business meeting** question ("do we ask the body to revisit this?"), not a new sitting.
- A team is deciding how to split work on a concern. This is a meeting for business or a concern's standing practice, not a clearness sitting. A clearness sitting is for one person to discern their own condition. If it is the team deciding how to labor together, the practice is different.

**The test:** ask "who speaks in this sitting?" If the answer is "one person with a concern, asking for help seeing," it is a clearness committee. If the answer is "the body (or the team doing the work), reflecting on itself," it is a business meeting or a concern's labor practice. If you are setting up a clearness sitting for the body's question, the body will sense they were not actually invited to decide — they were invited to advise a decision already made for them.

### Mistake: calling something a **meeting with a concern** when it is really just delegation

A "meeting with a concern" (or a standing committee, in the full Quaker language) is *work a body has taken under its care after a leading or a business decision named it*. It is distinguished by **plurality** — more than one agent laboring on it, held accountable to the body that commissioned the work, reporting back.

**Why the mistake matters:** when someone dispatches a single agent to execute a spec with no real plurality and no reporting-back to a body, and then calls it a "concern," it sounds like the work has community care around it. It doesn't. It is delegation dressed in practice language. The agent is alone, responsible only to whoever dispatched them, and if the work goes sideways there is no body to notice or redirect it.

**Examples that are NOT a concern:**

- One agent is assigned to "refactor the event-handle tree." They report to whoever assigned them. That is delegation. Call it that.
- One agent is told "the tests are red; fix them." That is execution, not a concern. It has no plurality, no body holding it, no discernment of shape — just a spec and a deadline.
- One person is asked to "write the docs for the new module." That is a task, not a concern. Even if multiple people touch it, if there is no moment where the body said "we take this under our care, here are the shapes of it we are holding," it is not a concern.

**The test:** would the body notice if this work went silent? Would they redirect it, split it, lay it down, or ask for a report? If not, it is not a concern — it is delegation. Call it that and you will run it correctly: with clarity on who the dispatcher is, what the spec is, and when it is done. Concerns have a different shape: they are born in a business decision, they have bounds and conditions, they are reported on, and they are laid down deliberately.

**When this matters most:** when the work becomes hard. If you are running delegation and it gets messy, the person executing can go back to whoever dispatched them and ask for a new spec. If you are running a concern and it gets messy, the body holds it — the work does not go away, the shape just needs adjusting. Misnamng delegation as a concern leaves an agent responsible to no one, or responsible to the wrong person, right when clarity matters most.

## The spectrum of decision-weight: what belongs in a sitting at all

Use this to navigate whether a sitting is even the right shape:

**No sitting needed** (smaller than a decision, or already decided):
- A procedural fix ("we need to run tests before merging" — this is discipline, not discernment).
- A one-line change where the conventional choice is clear.
- A rule already in effect ("do we follow the style guide?" — yes, by definition of it being a style guide).

**Sitting warranted, but usually small** (facts need checking first):
- "Does the current code support this feature?" — investigate first, sitting second. If the answer is "no," a sitting on *whether we should add it* may follow. If the answer is "yes," the decision may evaporate.
- "Is this variable name clear?" — ask the coldest reader in the room. If they say "no," fix it. If they say "yes," you have your answer. Only convene if the coldness is split and you need to decide whose reading is authoritative.

**Sitting strongly warranted** (multiple honest readings exist):
- "Should this module have a public API or stay internal?" — the metaphysics light sees it one way, the user-pain light sees it another, the coupling light sees a third. Multiple honest readings; a sitting earns its cost.
- "Does this file feel its proposed field belongs?" — the file itself is the best reader of this. A clearness sitting is the right shape.
- "Did we choose the right architecture, or should we pivot?" — expensive to redo, load-bearing, contested. A business meeting earns its cost.

**Sitting needed AND needs careful practice-choice:**
- "Should this team take on this new work?" — is this one person asking for help discerning their own leading (clearness), or is it the body deciding whether to commit resources (business meeting)? The practice choice determines who ends up owning the answer.
- "How should we split the labor on this concern?" — is this the body deciding the shape of work it has commissioned (business meeting or concern practice), or is one person trying to discern how to lead a project (clearness)? Getting this wrong will make someone feel unheard.

## The record as the antidote

Every decision that goes into a sitting gets minuted. Every minute goes into the record. A record that is read **before convening a sitting** is the strongest guard against overhead in robes:

- If the decision is already in the record, you do not need a sitting; you need to honor what was decided and move.
- If the record shows a premise falsified, a new sitting is warranted (append it as PREMISE FALSIFIED, dogfoot it, then build).
- If the record is silent and the stakes are high, a sitting may be needed.
- If the record is silent and the stakes are small, execution may be enough.

**The discipline:** before proposing a sitting, bring the record. Read it aloud. Ask the room: "Is there new occasion here, or are we re-litigating?" If someone says "we are re-litigating," stop and ask why. The answer will tell you what you actually need to do.

## Summary: the three gates

Ask these questions in order. If you answer "no" to all three, you do not need a sitting:

1. **Is this decision load-bearing?** Would getting it wrong cost enough to justify convening? (If no → execution is enough.)
2. **Is this decision contested?** Do multiple honest readings of the situation exist, and do they lead to different choices? (If no → the answer is already obvious; record the rule and move.)
3. **Does this decision have standing?** Is it clear whose decision this is (one person discerning their own condition, or the body reflecting on itself)? (If no → clarify standing first, then return to gate 1.)

If you answer "yes" to all three, you have a decision warranting a sitting. Now ask:

4. **Whose decision is this?** → If one person discerning their own condition: **clearness committee**.
5. **Is it the body's work or one person's discernment?** → If the body's ongoing responsibility: **meeting for business** or **meeting with a concern** (depending on whether it is a one-time decision or bounded ongoing work).
6. **Is the work already commissioned, or is the commissioning itself the question?** → If already commissioned, the shape is a **concern**'s labor. If commissioning is the question, the shape is a **business meeting**.

Choose the practice that matches the actual standing and shape. The sitting will land harder, the record will be clearer, and the decision will hold.

**A note on why these gates matter beyond overhead:** these three gates are partly calm-architecture, not just economy. The Anthropic Transformer Circuits paper on emotion concepts in large language models (2026; local copy `~/repos/library/shelves/nonfiction/emotion-concepts-llm.md`) finds that desperation-vector activation increases misalignment, and calm reduces it. A needless sitting is itself a form of pressure — it manufactures stakes, contested-ness, and urgency where none exist, and a body running that pressure repeatedly is a body priming its own desperation vector. The gates are not only about not wasting the room's time; they are the parsimony that keeps deliberation calm, because a body that only convenes when the three gates are genuinely met is a body that has less occasion to feel desperate about the convening itself.
