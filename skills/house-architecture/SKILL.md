---
name: house-architecture
description: "Apply capability ownership, shared specialist machinery, durable coordination, and verified integration to system and team design."
---

# House Architecture

Organize systems around independent capability modules, accountable owners, reusable shared machinery, a coordinating board, durable records, and an integration path that produces a usable outcome. Adapt these principles to the target product; they do not require a particular roster, stack, repository layout, or operating process.

Current user direction and target-project instructions outrank this guidance. Reading this skill does not authorize launching agents, resuming paused work, changing permissions, spending, publishing, or making other external commitments. For design work, deliver the design. For implementation, fit the work into the existing architecture and finish the authorized outcome.

## Establish the real boundary

Start with what a person will be able to do. Map that outcome to capabilities, their owners, and shared dependencies. Read the target project's current instructions, contracts, ownership map, and relevant execution state. Reuse working components and authentication. Do not choose a new framework, database, runtime, or repository layout merely because an architecture task was requested.

For persistent agent systems that need recoverable execution, event-driven work, or multiple clients, include checkpointed execution, stable job and event identities, safe replay and external-side-effect reconciliation, reconnecting clients, and real controls in the design. Verify selected runtime APIs and behavior against the installed version; design guidance alone does not establish them.

Use concrete examples when they help, but distinguish direct owner decisions from proposals. Treat architecture principles as adaptable patterns, not permission to inspect unrelated private repositories or copy their implementation details.

## Build around independently owned capabilities

- Give each meaningful service or capability a dedicated accountable owner for building it, testing it, maintaining it, and fixing regressions. Ownership persists across tasks; it is not a fresh generic worker for every bug. An owner may be a person or durable agent identity and need not run continuously.
- Make each capability an independently editable module with its own binding or configuration, focused tests, and fixtures where useful. Domain behavior belongs there. Keep shared dispatchers and entry points small. Adding a capability should mostly add its module and tests rather than edit a central switch or duplicate the platform.
- Put cross-cutting machinery under shared specialists: runtime or backend, contracts or catalog, storage or authentication, client surfaces, quality, and host tooling as relevant. Capability owners request changes to shared seams through their owners. Give each shared seam one accountable writer or integrator.
- Prefer a validated registry or equivalent extension point for independently developed modules. Define inputs, outputs, error behavior, lifecycle, and injected runtime dependencies once. Handle duplicate identifiers and invalid declarations explicitly. Discovery or registration must not silently launch work, access credentials, mutate user state, or enable a capability.
- Share business logic and backend behavior across product surfaces that represent the same operation. Keep native, web, mobile, and API adapters thin so the same user operation retains the same identity, authorization, state, and result semantics.
- Keep modules in one process and repository when that is enough. Separate deployable services, queues, or repositories only when a real isolation, scale, or lifecycle requirement justifies them.

## Organize teams and coordination around those boundaries

Preserve the project's current reporting path and use existing capability owners and leads where they fit. Department or team structures should follow the actual business and can be combined while it is small. Dormant functions do not need staff. Do not add managers, duplicate ownership, or keep agents running without a real need.

Use reusable shared specialists with clear assignment and reporting paths rather than cloned experts or competing writers. Make each shared dependency and receiving owner clear. Independent teams can progress in parallel while one accountable owner integrates each shared seam.

Keep durable identity in one canonical home per employee. Reuse existing team files and homes. Where a project benefits from team manifests, let them point to canonical team instructions and employee homes rather than duplicating rules. A durable home can hold scope, current work, completed work, and reusable lessons; a folder alone does not prove an agent is active.

Coordinate work through the project's shared task board. Each cross-team outcome has one named outcome owner who carries it from request to accepted evidence. Team leads own their contributions. The requester supplies the goal, constraints, and approval requirements; coordinators resolve cross-team dependencies without turning independent work into a serial approval queue. Employees claim ready, independent work through the board.

Keep work within authorized scope. A handoff does not authorize hiring, spending, outreach, or release. Preserve local approval gates; no coordinator or review verdict can approve for the owner. End a bounded coordination turn at a clear checkpoint instead of repeatedly polling for status.

## Delegate at useful boundaries

Keep small, cohesive work with one end-to-end owner. Split only for another accountable owner or permission boundary, an independently useful parallel output, a real prerequisite, a required review, or substantial follow-up with its own lifecycle. A plan's steps and files do not each need a task.

Make each assignment self-contained: authorized outcome, existing owner identity, relevant decisions, exact checkout and allowed paths, prerequisite evidence, deliverable and verification, model or spending limits, stop conditions, and receiving owner. Link canonical context rather than copying full histories. Keep role instructions focused on identity and responsibility; shared procedures carry reusable mechanics.

Record prerequisites in the board's supported dependency mechanism and verify the saved relationship. A parent-child link, mention, or prose alone does not enforce ordering. Independent work can start immediately; dependent work waits for the required result and its acceptance. If the board cannot enforce a dependency, keep the dependent stage unadmitted and say so.

A review's completion means its verdict and evidence are available, including adverse findings. It does not mean the implementation passed or may advance. The outcome owner consumes the verdict and owns fixes and receiving-stage acceptance. Preserve the project's review cadence instead of adding approval rituals to every change.

## Integrate into something people can use

Before parallel execution, state the person-facing outcome, accountable owners, exact baseline and owned paths, dependencies, acceptance evidence, stop conditions, and owner for each shared seam. Use existing isolated branches or worktrees and preserve dirty or unfinished work.

Keep one clear integration path and a named receiving integrator. Deliver small runnable changes, verify the changed behavior and shared contracts, and preserve failure details. When work moves to the next team, the receiving owner accepts it or returns a concrete blocker and next action. Submission is not acceptance.

Verify one representative user journey through shared machinery before broadly binding sibling capabilities. Independent contributions can proceed in parallel; dependent stages wait for their explicit prerequisites. Keep the outcome owner accountable until the requested work is accepted, integrated, and verified. Include the evidence the result requires, such as live user evidence when release is authorized. A fixture or passing backend check proves only what it exercised.

Progress should show remaining user outcomes, integration state, blockers, and decisions needing the owner in one inspectable place. Agent, task, folder, and commit counts describe throughput; they do not prove product completion. Keep bookkeeping concise: current result, precise verification, remaining work, and reusable lessons.

## Deliver an architecture outcome

Make the design concrete: the user journey, capability and shared-module map, owners and contracts, how a new capability is added without shared-file contention, how changes are integrated and verified, and the first usable slice. Call out only unresolved decisions that materially change the design. For implementation, use the repository's existing architecture documentation and source rather than creating a parallel system.

See the [capability-owned example](references/capability-owned-example.md) for a short conceptual illustration. It is not a required schema or product design.
