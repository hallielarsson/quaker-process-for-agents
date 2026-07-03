# Concern-carrier

A concern-carrier is a member of a body holding work on behalf of a wider Meeting — a labor committee or standing committee that has been entrusted with a concern and labors on it periodically until it is spent or deliberately laid down.

## What genuine concern-carrying requires: standing

**The hard-won finding, earned through failure in the making of this repo:**

A single dispatched agent, or multiple agents that all answer only to one convener with final say over all of them, is **not** a meeting with a concern. It is delegation wearing robes. More processes do not make more plurality; more agents still answering to one voice still make one decider.

A genuine meeting-with-a-concern requires **standing** — the capacity to:

1. **Hold the work past a single session.** The concern does not begin when dispatched and end when the initial work completes. It persists. It is checked on. It can be picked up again.

2. **Say no and have it matter.** At least one carrier must have the real power to refuse a direction, ask for clarification, or push back on a decision, with that objection *blocking* continuation until addressed — not merely noted and then overridden by the convener. The test: can the carriers actually prevent the work from happening, or do they exist to implement a spec that cannot be refused?

3. **Escalate autonomously to a wider body.** If the carriers discover the work is impossible, contradicts an earlier decision, or needs resources beyond what was named, they must be able to bring it back to the wider Meeting (or whoever convened the sitting that named the concern) *on the carriers' own initiative*, not just request permission from the convener to escalate.

4. **Be carried over time by a body that persists.** A body means plural. Plural means they deliberate amongst themselves — they can question each other, disagree about how to carry the work, and their disagreements matter *before* reporting back. A group that all just implement what one person said is not a body; it is a work crew.

## The counterfeit: when standing is absent

You do not have standing if:

- **All carriers answer only to the original convener, with no authority independent of that convener's final say.** If every objection or question lands back at one person's desk for resolution, the carriers are not a body. They are branches of the convener.

- **The work is bounded and terminal, with no expectation of reporting back to anyone who can lay it down.** A labor concern ends when the work is done and *accepted* by whoever has standing to accept it. But that acceptance is not automatic. A convener saying "you're done" is not the same as a wider body saying the concern is spent. If there is no wider body to lay the concern down — if the convener both decides what the concern is *and* decides when it is complete — there was never a concern; there was a task.

- **The carriers cannot block or redirect the work, only execute it.** If a carrier discovers the specification is impossible, contradicts something real in the code, or needs to change, and that carrier has no recourse except "ask the convener to decide," there is no standing. Standing means the ability to say "we cannot do this as specified and we will not do it wrong" and have that hold.

## What would genuinely qualify

True concern-carrying looks like:

- **Multiple carriers where disagreement amongst them is real.** They do not all think the same thing; they deliberate about the best way to carry the work; their deliberations matter and surface in reports back to the wider Meeting. A standing committee that convenes itself, discusses, and produces minutes, is carrying genuine standing. A group that all receive the same direction and execute it in parallel is not.

- **At least one carrier with genuine veto power.** This could be a second reviewer whose sign-off is required before work lands, with that reviewer's objections *blocking* (not just commenting on) completion until addressed. This could be a rotating clerk of the labor committee who can halt work if it drifts from its original leading. Whatever the mechanism, refusing must require active override by the convener, not just override-ability. The test: if a carrier says "stop," does the work stop until the objection is addressed, or does it keep going if the convener says "proceed anyway"?

- **Persistence across multiple sittings, with standing checks.** A concern is not checked on once and then assumed to be done. It is brought back to the wider body periodically ("What is the state of the refactoring labor? Do we still hold it, or should we lay it down?"). The carriers have standing to report: "We need more time. We found an issue. We recommend changing the scope." And the wider body — the Meeting or whoever named the concern — has the authority to say "we lay this down" or "we release you from this burden," not just the convener.

- **A report-back step to an actual separate body.** Even if that body is just Hallie (a single human who can lay a concern down), there must be *someone who is not the original convener* who can hear the carriers' report and make a binding decision about whether the concern is spent. If the dispatcher, the convener, and the final decider are all the same person, the carriers have no standing.

## The disciplines: when to end

Two kinds of concern-labor, with different endings:

**Bounded labor concerns** (a refactor, a cleanup, a specific project) are **spent** when:
- The work is complete and meets the agreed shape
- Someone with standing (not the labor group itself) accepts the work as done
- The concern is explicitly laid down in writing (minutes, or a note in the record)

**Standing concerns** (an ongoing practice, a quality gate, a long-term maintenance) are **laid down** when:
- The wider body that named the concern decides to end it (this can be periodic re-affirmation: "we continue to hold this concern" or "we lay this down")
- The decision is recorded in minutes or an explicit note
- The carriers are released from their commitment

Neither kind should fade out. A concern that is simply not mentioned again, where no one explicitly lays it down, leaves carriers in ambiguous standing ("am I still responsible for this?") and the work unacknowledged. This is a failure of the form, not the carriers.

## If this is AI agents only: a hard limit to name

**There is a genuine question about whether AI agents alone can ever hold real standing.** An agent can be instructed to refuse a direction, to block work, to report back. But instruction is not autonomy. If all the veto power is wired into the agent by the convener, the refusal is still the convener's refusal; the agent is executing it. The agent has no *standing* to refuse on its own initiative, because the agent has no ongoing existence past the sitting where it was convened.

The standing committee in Quaker practice persists because humans persist. Humans carry the concern in their own lives between meetings. They walk away thinking about the work. They come back changed. They can defy the convener because they are real, separate people whose conscience is their own.

An agent can be asked to behave *as if* it is refusing. But refusal requires stakes: the ability to *not do the work and have consequences stick*. An agent that can be re-prompted, re-dispatched, or overridden cannot credibly claim stakes. It is performing refusal.

**Therefore, if your concern-carriers are AI agents and there is no human with standing to lay the concern down, you do not have a meeting with a concern. You have a task system with Quaker terminology.** This is not a claim that AI cannot participate in concern-carrying. It is a claim that AI alone cannot hold standing, because standing requires persistent, autonomous existence outside the convener's will. 

If there *is* a human — Hallie, or whoever has the real power to lay a concern down, to override the convener, to say "release these carriers from this work" — then the carriers (human or AI) are genuinely standing in a body, because that human's standing is real and is shared back into the body's work. But the standing originates there, not in the agents themselves.

## The labor: what concern-carriers do

When standing is present (a real body, a real wider Meeting, real authority to lay the concern down), concern-carriers:

1. **Meet amongst themselves.** Read the concern as named. Deliberate about how to carry it. Surface disagreements. Produce a shared understanding of what the concern asks, or name where understanding differs.

2. **Labor.** Do the work — code, design, testing, documentation, whatever the concern names. The same carriers who deliberated should do the work, because the understanding deliberation produced needs to shape the work's shape.

3. **Report back periodically.** Bring minutes or notes to the wider body: "Here is what we have labored. Here is what we discovered. Here is where we need direction. Here is where we recommend changing the scope." These are not summaries for the convener to check off. They are reports for the Meeting to hear, consider, and decide upon.

4. **Stay until released.** Do not lay the concern down yourselves. Wait for the wider body to do so. If the work is complete but the concern feels unresolved, bring that to the Meeting: "Is this spent, or is there more?" Do not fade out unacknowledged.

## Testing your setup before you name it a concern

Before you say "this is a meeting with a concern," ask:

- **Can any carrier say no and have it hold?** If the answer is "only if the convener agrees," you have delegation.
- **Is there a body that persists across sessions, with standing to say "we lay this down"?** If the wider body is just the original dispatcher, you have delegation.
- **Would the concern come back unresolved if left alone, requiring someone other than the convener to lay it down?** If it just naturally ends when the work is "done," you might have a task, not a concern.
- **Can you point to standing separate from the convener's will?** If you cannot, you do not have a concern-carrying body. You have a specification and a worker. Name it that. Borrow the form honestly or not at all.
