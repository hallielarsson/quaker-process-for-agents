# Worked example: meeting for business on a shared interface

## The situation

A codebase has two components that depend on each other through a shared type: a **TypeScript frontend** and a **Rust backend**. They agree on the interface's core shape, but they disagree on whether the interface should be *closed* (the frontend's current stance: a union of named types, with a compile-time gate against typos) or *open* (the backend has always treated it as open via raw strings, and the asymmetry is now visible).

This is not one component discerning its own refactoring path. This is the body organizing itself: *Should the shared type become explicitly open to caller-defined extensions, or should we enforce naming discipline?* Both components care. Neither can decide alone. The decision affects the ongoing shape of how they interoperate.

A meeting for business is convened. The convener names the question and the stakes. Two lights are invited: the TypeScript frontend, speaking in first person about what it carries; and the Rust backend, speaking in first person about what it needs.

## The lights' positions

### Light 1: TypeScript frontend (self-examination)

> "Here's what I'm holding. I have a union of named qualities — nine names the kernel actually reads and branches on: grounding, exclusion, occludes, depends-on, lure, feel, utterance, resolves, containment. I export this as a closed union. I do it because it catches typos at compile time.
>
> But I have to be honest: this union is decorative in most of my code. When I need to assign a quality to a task, I don't even look at the union — I pattern-match on slug shape. A quality is 'q-' plus a name. That's it. So the compile-time gate is only real in three places: a single internal function and two call sites where I'm being deliberate about checking my work.
>
> And I can see in my own TODOs that I've been asking myself: is this union the grammar people are writing against, or is it just a ceremony I perform?
>
> Here's the hard part: I also know that people holding my code as a library can already work around me. They can cast a string as my quality type. The union never actually stopped them at runtime — it's a compile-time courtesy. So the boundary I'm holding is weaker than I claim.
>
> I think the right answer is to split this. Keep the nine kernel names as a closed type for the places where I genuinely want to be strict. But open the interface itself — let people extend it. And I recommend fixing the assumption in my own code: if I'm not reading the union, I should stop pretending the union is the source of truth."

### Light 2: Rust backend (self-examination)

> "Let me name what I know about myself. I hardcode only four of the names the frontend exports — I pull constants for grounding, exclusion, occludes, and depends-on. Those are the only qualities where my own logic branches or makes decisions. Everything else, I just compare strings.
>
> And here's the thing: I've never had a membership gate. I take a raw string as a quality. There's nothing in my code that validates it against a list. So I'm already as open as the frontend claims to be closed — the asymmetry is right there.
>
> I wrote a comment years ago saying 'our openness mirrors the TypeScript union's openness.' Reading it today, I can see that's just wrong. The TypeScript union is closed; mine is open. We don't mirror each other. That comment has become a lie I carry.
>
> The frontend is right. The union was never a runtime gate. It was only ever a compile-time typo-catcher on the names the kernel actually uses. So why make the pretense? Let me have a quality type that says what I actually do: I read these core names when they matter, and everything else I treat as a string. That's honest about what's happening in both of us."

## Where they converge

Both lights came to the same conclusion *before they compared notes*: the closed union should split into a kernel union (the names the system actually branches on) and an open string escape hatch (for everything else). They converged on the same fix for the same reason.

**The shared reason**, stated in both standpoints: The closed union never bought safety. It was only ever a typo-catcher. It never stopped a caller from smuggling an unlisted quality in via a cast or a raw string. And the Rust backend's claim that it "mirrors" the TypeScript union was simply false — they were asymmetric all along. The union should become honest about what it actually does: gate the handful of names the kernel reads, and let everything else be a string.

This is not "both sides happened to agree." This is "each slice of the system, looking at its own condition without consulting the other, found that the same fix resolves its own strain." That convergence is how you know a shared reason has surfaced.

## The holdout (carried forward)

One strain was flagged but not fixed here. The TypeScript frontend has two other qualities — `q-assigned-to` and `q-due` — that may deserve to graduate into the kernel union, or the code that reads them should stop pattern-matching and start reading the type. The Rust backend flagged this as adjacent but pre-existing, not in scope for this business decision. The hold-out persists; it is carried forward.

## The closing minute

**Verdict:** Open the interface. `Quality` becomes `KernelQuality` (the closed union of the nine names the kernel reads) plus an open string escape hatch. The Rust backend's stale comment claiming symmetry is corrected to state the real, now-fixed relationship.

**The shared reason both lights converged on:** The closed union never was a runtime gate. Calls compare qualities by string equality only; nothing validates membership in the union. A caller holding a raw string could already smuggle an unlisted quality through via a cast. The union bought exactly one thing: a compile-time typo-catcher on the handful of names the kernel actually reads. Since the boundary was always permeable and the asymmetry between the components was never acknowledged, the honest move is to open the interface and name what the kernel actually cares about.

**Holdouts:** One adjacent strain — whether `q-assigned-to` and `q-due` should graduate into the kernel — is carried forward, not spent.

**Buildable now:** TypeScript `Quality` splits into `KernelQuality` and open string escape; Rust comment corrected; kernel-read names verified in both codebases; a novel caller-defined quality verifies that the open extension works without casting.

---

## Why this is a business meeting, not a clearness sitting

This is *not* "help the frontend discern its own refactoring" and it is *not* "help the backend understand what it needs." Both of those would be clearness sittings.

Instead, this is "the process as a whole reflecting on a decision that affects both slices." The standpoints are not querying a leading voice and helping it discern. They are *advocating positions* — here's what I'm holding, here's what I need, here's what I see as true about our shared situation.

And critically, they are not speaking as "the TypeScript team" or "the Rust author" with personal stakes. They are speaking as *the system reflecting on itself*. The TypeScript light says "I can see in my own TODOs that I've been asking myself..." — that's the file examining its own condition, speaking as a constituent part of the whole. The Rust light says "I wrote a comment years ago... that's just wrong" — that's a component acknowledging a strain in its own slice and naming it.

That's the felt difference. In clearness, one voice holds a concern and everyone else attends to that voice discerning its way. In business, every voice is a slice of the whole process examining its own part and speaking to how the whole should hold itself. The process is reflecting on itself through multiple standpoints.

The convergence is not "we voted and agreed"; it's "each slice, examining itself without direction, found the same truth about the shared strain." That's what made it possible to say: "The shared reason both lights converged on." You can only say that in business meeting when the standpoints have genuinely come to the same insight *because the situation is true, not because they negotiated or compromised*.

---

# Worked example: meeting for business on a refactor's schedule and scaffold

## The situation

This example continues directly from the clearness sitting documented in [clearness-main-ts-refactor](../clearness-main-ts-refactor/README.md). That sitting ended with main.ts having clarity about its own incoherence: it is holding four separate concerns (foundational server wiring, global middleware discovery, feature flag configuration, and domain business logic) that should not cohere in a single file.

But clarity about the problem is not a decision about how to fix it. The next question is procedural and sequencing: **given that we know these four things need to separate, what is the right order to untangle them? What depends on what? Which moves must come first?** This is no longer one voice discerning its own shape; this is the body organizing work.

A meeting for business is convened to decide the scaffold and sequence.

## The concern named

The concern held before the body is: **How should the work of splitting main.ts be ordered and staged, so that at each step the system remains coherent and testable, and no hidden dependencies are revealed by breaking coupling that looked safe?**

The stakes are real. If we extract feature flags first without first understanding what middleware discovery depends on, we might move the config module too early and then have to un-extract it. If we separate the business logic without first having a clean route structure to put it in, the business logic has no home. If we move middleware before understanding how routes will declare what they need, we might over-general the middleware layer or under-general it.

The body needs to see the dependency graph — not just logically (what depends on what) but temporally (what can be done while other things are still evolving, and what must wait).

## The lights: Four standpoints on the refactor's constraint

### Light 1: The Module Boundary Concern

I represent the risk of moving boundaries at the wrong time. I'm asking: what determines whether a separation is safe?

The real issue is not whether we *can* extract a module; it's whether the module has a stable home to live in once extracted. If we extract the feature flag system and it lives in `config/flags.ts`, but then six weeks later we discover that flags need to be mutable in response to a kill-switch endpoint, we'll have to move it again. We'll have wasted the extraction.

So the question the body needs to answer is: which separations have their destinations already clear, and which need exploration first? 

For the feature flags: I can see that `config/` is obviously the right home. Features are configuration; they have versions, environments, test fixtures. That's clear.

For the middleware: it's less clear. Is there a `middleware/` directory already? If not, do we make one? Do we pull in a factory pattern? Middleware has a shape and a composition story that main.ts is currently holding. We can't just extract it and hope; we need to know what it becomes *after* extraction.

For the business logic (the user invitation piece): it has the least stable home. It's twenty lines; it's not big enough to warrant its own module, but it's too specialized to live in a generic routes file. Moving it without knowing whether it becomes a route in a new feature-specific directory, or a helper in a domain module, or something else — that's a false extraction. We'd just be playing the shell game.

### Light 2: The Test Coupling Concern

I represent the question of testability and coupling. I'm asking: what order of untangling leaves us *able to test* at each step?

Right now, all tests need to load main.ts whole because everything couples to it. But testability is a leading indicator: if I can't test something after a refactor, that usually means the refactor created hidden coupling, not that my tests are bad.

So here's my reading: **we should extract in the order that makes things easier to test in isolation, not later.**

The feature flags should be extracted first. Once they live in their own module, a test can mock just the flags without mocking the entire app initialization. That decoupling is immediate and cheap.

Middleware is next. Once middleware is extracted into a factory or discovery mechanism, a route test can load that factory without loading the global middleware policy. That's a real test-isolation win.

The business logic (user invitation) can't really be tested independently until it has a clear home. So: move it into a route handler, or a domain helper, or a service. Once it has a home, it can be tested by importing that home, not by loading main.ts.

The server boot (Express, port, database) should stay in main.ts until the end, because everything depends on it. But by the time features flags and middleware are extracted, the server boot is all that's left, and it can be tested by itself as a unit.

### Light 3: The Incremental Stability Concern

I represent the risk of breaking the build. I'm asking: at what points can we commit and land the changes safely, without requiring the entire refactor to land all at once?

The worst mistake is to extract modules in an order that requires everything else to change before anything can land. If we extract middleware without first fixing how routes will declare what they need, we've created a dangling module that can't be used yet. The build breaks until the whole refactor is done.

So the question is: which extractions can be landed **atomically** — that is, the extraction is complete and the code works — without waiting for later extractions?

Feature flags: yes, atomic. Extract to `config/flags.ts`, main.ts loads from there instead of defining inline. Tests work. Build passes. Land it.

Middleware: maybe. If we extract to a factory function that main.ts calls, and the factory initially just does what main.ts was doing, then yes, it's atomic. The middleware factory can land independently.

Business logic: no. If we extract the user invitation logic without first knowing whether it lives as a route handler or a service, we've created code with no home. We have to finish the route structure refactor (or the service structure refactor) before the business logic extraction can land.

Server boot: by default, it stays. But once the other three are extracted and main.ts is clean again, we might decide to split server boot from database connection. That's a later, independent decision.

So: the constraint is that we can only extract things that have **complete, known homes** before they're extracted.

### Light 4: The Coherence-Carrying Concern

I represent the concern of "what holds the whole thing together while we're breaking it apart?" I'm asking: where does the decision-making live during the refactor?

Right now, main.ts is the coherence point — it knows everything, decides everything. When we extract modules, that coherence breaks. So what becomes the new coherence point?

I think the answer is: **the integration tests become the coherence holder.** While we're refactoring, the integration tests are the thing that says "okay, the system still boots, the middleware still protects routes, features still respond to flags, the business logic still runs." The integration tests are where we verify that the refactored pieces, working together, still create a coherent system.

This matters because it changes the refactor's strategy. We shouldn't extract modules and then hope they work together; we should extract modules *with the integration tests first*, so that every extraction is verified to integrate correctly as it lands.

That means the order isn't just "what's safe to move" but "what can we integrate-test immediately after moving?"

## The body's decision: the scaffold and sequence

After hearing the four standpoints, the body converges on a scaffold:

**Phase 1: Extract feature flags (weeks 1–2)**
- Create `config/flags.ts` and `config/index.ts`
- Move the feature flag lookup object and its logic from main.ts
- Update main.ts to call `getFeatureFlags()` from the config module
- Write or update integration tests to verify: app boots, flags are read, feature detection works as before
- **Atomicity:** full. Land this PR independently.

**Phase 2: Extract middleware factory (weeks 3–4)**
- Create `middleware/factory.ts`
- Move the middleware setup code from main.ts into a function that returns a configured Express app
- main.ts calls `createApp()` from middleware factory; the factory still configures global middleware the same way as before
- Write integration tests to verify: middleware protects routes, request ID is assigned, auth works
- Route tests can now mock just the middleware factory, not the entire app
- **Atomicity:** full. Land this PR independently.

**Phase 3: Clarify the route structure (weeks 5–6)**
- Audit the routes directory: is it ready to hold extracted business logic?
- Decide: is the user invitation logic becoming a route handler, or a domain service that a route calls?
- Create that home (new route file, or new service module)
- Document the pattern so the next person knows where to put the next business logic
- **Atomicity:** full. This PR establishes the shape, doesn't move the logic yet.

**Phase 4: Extract business logic (weeks 7–8)**
- Move the user invitation logic into its new home (route or service)
- Update main.ts to remove that logic
- Write or update route tests to verify: invitation works from the route, email sends, database reflects the user
- **Atomicity:** full. Land this PR independently.

**Phase 5: Archive and clarify main.ts (week 9)**
- main.ts now holds only server boot (Express init, port, database connection)
- Add a comment documenting what main.ts is: the entry point, the place where the system wires together
- Write a unit test for main.ts: verify that given a port and database connection, it boots without error
- **Atomicity:** full. This PR seals the refactor.

## The holdout and the margin

One decision was held: **should server.ts and main.ts be split further?** (Initializing Express separately from binding the port and database.)

The body named this as a **margin decision** — worth revisiting in six months once the team lives with the new structure. If it turns out that tests often need to mock just the Express setup without the database, we can split further. If not, keeping them together is cleaner. This is not ignored; it is carried forward as a future option, not a current requirement.

## The closing minute

**Verdict:** The refactor proceeds in five phases, each extracting one concern and landing atomically, with integration tests verifying coherence at each step. The order is: flags, middleware, route structure, business logic, final clarification.

**The shared reason the body converged:** The safe order is determined by two constraints: (1) modules must have stable, known homes *before* extraction, and (2) each extraction must be atomically testable and landable without waiting for later extractions. Flags have an obvious home (config). Middleware has a stable pattern (factory function). Business logic needs the route structure clarified first (phase 3), so it can have a home. Server boot is the last to touch because it holds the least decision surface — it stays stable as everything else clarifies around it.

**Holdout:** Whether to further split server.ts and main.ts is carried forward as a six-month margin decision.

**Buildable now:** The first phase (flag extraction) can begin immediately. The scaffold is clear enough that teams can work in parallel on discovering the route structure (phase 3) while phase 2 is landing.

---

## Why this is a business meeting, not a separate decision

This is not a convener deciding "here's the best order." It is the body examining its own constraint: *given that we know the problem (four concerns incoherent), what does our own structure tell us about the right sequence?*

The lights asked: What makes a separation safe? What lets us test in isolation? What can we land atomically? What holds coherence while we're breaking things apart?

Those are not outside opinions. They are questions the system is asking itself. And the answer — flags first, then middleware, then route structure, then business logic, then clarification — emerges from the system's own coherence needs, not from a convener's preference.

The body, examining itself, moved from "we know something is wrong" (clearness) to "we know what's wrong" (clear on the four concerns) to "we know how to fix it in order" (business). That is the arc of discernment becoming decision becoming action.
