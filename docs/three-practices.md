# Three Quaker-adapted practices for agent discernment

This document describes three distinct process forms that an AI agent or agent team can use to discern high-stakes or contested decisions: **clearness committee**, **meeting for business**, and **meeting with a concern**. The three are often confused because they can use similar procedures (agents convened, standpoints invited, synthesis produced), but they rest on fundamentally different standpoints and serve different purposes. Using the wrong form for the wrong situation produces a recognizable failure.

This is adapted from Quaker practice and rests on tests that distinguish them in their source tradition. The tests here are stated in the framing that emerged from using these practices on real code.

**How these three sit in practice** (business minute, 2026-07-03): concern-carried plural work is the ordinary ground state — work commissioned, carried, reported, laid down. The two meetings are forks that arise *within* that work, not alternatives you arrive at from outside. The dividing tests below answer "a fork is live — which meeting fits it?", and the standing test answers whether the ground state is genuinely being carried at all. `SKILL.md` is the synthesis written from that ground floor; this document is the treatment — the full tests and worked examples.

## Clearness committee

A clearness committee is convened for **one participant's leading** — one voice with its own concern or decision to discern, discerning the right shape of its own condition. Everyone else acts as a querying body. They ask questions, they listen, they do not advocate a position of their own.

**The dividing test:** Does the sitting focus on helping one participant discern something about *their own leading*? If yes, it is clearness.

**Example:** "How should this overblown `main.ts` be refactored?" In this case, the file (or its owner) holds a leading: the sense that something is broken, unclear, or needs a different structure. A clearness committee asks questions to help that voice discern what shape the refactoring should take. Questions might include: "What would help someone reading this file know where to start? What are the mental steps you find yourself repeating? If we removed this section, what would we lose?" The convened standpoints — other agents, other concerns, the file's own first-person reflection — all support that one voice coming clearer about its own condition.

The sitting does not try to decide *for* the leading voice. It does not resolve disagreement by taking a vote. It attends to the voice that holds the concern, and helps it discern its own way forward.

## Meeting for business

A meeting for business addresses decisions that affect the whole ongoing process — decisions about shape, scope, schedule, or resource allocation that the process as a whole must hold and reflect on. The standpoints speak **as the whole ongoing process reflecting on itself**, not as individual voices each with a personal leading.

**The dividing test:** Is the standpoint speaking as an individual voice with its own leading about its own condition, or is it speaking as a slice of the whole ongoing process reflecting on itself? If the latter, it is business-meeting.

This can be confusing because business meetings can look procedurally identical to clearness sittings. Both may invite multiple standpoints. Both may sound like they contain advocacy. The distinction is not in advocacy vs. querying (both forms can contain either), and it is not in whether the outcome "binds" or carries authority. The distinction is in *who the standpoint claims to be speaking as*.

**First worked example:** "What's the schedule and scaffold for the resulting work after this refactor completes?" This is not one voice discerning its own leading. This is the body organizing its own ongoing affairs: Which other files need to be touched? In what order should the work land? How will we know when this concern is spent? These questions surface the process as a whole reflecting on its own shape.

**Second worked example:** A concrete instance from practice: two files in different codebases (one TypeScript: `society.ts` in penelope-gen4; one Rust: `scher-core/src/lib.rs`) each spoke in first person about whether a shared type should be more extensible. Neither voice held a personal "leading" about their own condition — each was reasoning about a decision that affected the whole shared concern. Neither asked the other for permission to extend the type, and neither was asking "help me see what I should do about this." Instead, each was a slice of the whole system reasoning aloud about a trade-off the system itself had to hold. The standpoint of the Rust file was "here's what I need to make sense here," and the standpoint of the TypeScript file was "here's what I'm carrying," and the process was reflecting on how to reconcile both. That was business-meeting shaped, even though it used the same file-speaks-in-first-person mode that a clearness sitting might use.

A business meeting produces a sense of the meeting — a shared understanding of what the whole process has seen, and what the next step should be. It does not necessarily produce unanimous agreement (Quaker tradition uses the language "sense of the meeting," not "consensus"). It does require that dissenting voices be heard and held, not overruled.

## Meeting with a concern (labor or standing committee)

A meeting with a concern is work that a Meeting has taken under its care after a leading or business decision named it. It is bounded or ongoing work, carried out by however many are laboring on it, with periodic reports back to the wider body, until the concern is spent or laid down.

**The dividing test:** Is there standing — the capacity to hold the concern past the session, to refuse parts of a convener's direction, or to escalate to a wider body on its own initiative? If the answer is no, it is not a meeting with a concern; it is delegation.

This test is subtle and worth dwelling on. A single dispatched agent executing a spec is not a meeting with a concern, no matter how the work is named or how many procedural steps are added. The missing ingredient is standing. Standing means the concern has the autonomy to:

- Hold the work over time, past a single dispatch
- Say no to a convener or initial decision if the concern disagrees
- Escalate to a wider body or bring the question back to the wider Meeting if the work runs into something it cannot resolve alone

A group of agents all answering to one convener with final say is still delegation wearing borrowed language — "more processes, not more plurality." True plurality in holding a concern requires actual autonomy; without it, the form becomes misleading and the work collapses under the illusion that it is held by a body when it is still held only by the convener.

**Example:** Suppose a Meeting has decided to refactor a problematic area of a codebase. A concern-labor group takes this under its care: multiple agents or multiple humans and agents, with standing to refuse parts of the specification, to ask for more time or resources, or to bring the question back to the wider Meeting if the refactor needs redirection. The group reports back periodically: "We've completed the first phase; we've found an unexpected dependency; we recommend changing the scope." The wider body hears these reports; it may affirm them, modify them, or lay down the concern if circumstances change. The concern-labor group is not executing a fixed plan; it is holding the work on behalf of the Meeting and discerning how to carry it.

## Who speaks is orthogonal to which practice is running

One source of confusion in using these forms: **the mode of staffing (how many speak, from where) is independent of which practice is running**.

A standpoint in either a clearness sitting or a business meeting can be embodied as:
- A person (an agent, a human, a role like "convener")
- A concern or lens (not a person, but "the correctness eye," "the newcomer's cold read," "the performance lens")
- A **file speaking in its own first-person voice** about its own condition or situation

That last mode — files speaking in first person — can appear in clearness sittings (helping a file discern its own refactoring), in business meetings (the TypeScript and Rust files reasoning aloud about a shared type), or in concern-labor work (a file reporting on its own changes). The mode is *how* the standpoints are staffed; the practice is *which discernment form is running*. They are orthogonal.

This matters because someone reading "we convened the file's voice in first person as a standpoint" might assume it was a clearness sitting. But if the file was reasoning about a shared decision affecting the whole process, it was a business meeting. The procedure can look the same; the practice is determined by the standpoint test, not the staffing.

## The relationship to Quaker source practice

These forms are adapted from real Quaker practice, which has centuries of depth. However, this is an adaptation, not a claim of equivalence. Actual Quaker discernment is situated in worship, in the gathered Spirit, and in the discipline of Friends who know each other and carry each other over time. The adapted forms here can be useful for agent teams or human-agent teams discerning hard decisions on code, but they are not a substitute for the real thing — and if you have familiarity with actual Quaker practice, you'll notice where the analogy stretches.

See `docs/quaker-correspondence.md` for an honest mapping of what's preserved and where the practice had to bend.
