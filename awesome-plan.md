# Awesome Plan — Lean Edition

A standalone planning skill for coding agents, usable in new or existing projects.
This document fully defines the workflow. Use it directly without fetching or loading another edition.

**Keep durable project understanding. Approve finite work. Verify outcomes. Minimize bookkeeping.**

## 1. Non-negotiables

- Repository instructions and higher-priority instructions prevail. Respect established user decisions and delegated technical authority.
- Inspect repository evidence before asking questions. Ask only about unresolved intent, consequential tradeoffs, authority, or risk acceptance.
- Goals, priorities and planning records are not implementation permission. A concrete, explicitly approved Queue is the implementation boundary. Adoption alone authorizes no implementation.
- Do not expand approved scope, silently drop acceptance criteria, or start another Queue automatically. Ordinary technical choices within the approved boundary need no additional approval.
- Code and observed behavior establish results. Distinguish verified, inferred, untested, blocked and canceled; never convert uncertainty into success.
- Preserve consequential decisions, exact approvals, outcomes and recovery information across sessions. Do not use chat memory as the only record.

## 2. Small record set, one owner per fact

Reuse existing equivalents. Do not introduce a second planning system merely to match these filenames.

| Record | Owns | Update when |
| --- | --- | --- |
| `plan/project.md` | Purpose/users; final outcome; scope/non-goals; Milestone Goals and acceptance; Workstreams and dependencies; Guardrails and authoritative rule links; lasting decisions; operating mode and record locations | A goal, boundary, constraint, lasting decision or milestone/Workstream outcome changes |
| `plan/current.md` | Current focus and why; the one current Queue, exact approval and item outcomes; blockers; next safe action; relevant evidence links; pending publication | A Queue is proposed/approved, meaningful progress must survive interruption, a blocker/decision arises, or work ends |
| `plan/history.md` | Append-only completed/stopped attempt records: approved scope, outcome, evidence, decisions and residual work | An attempt ends, or before replacing the current Queue |

Create history only when there is a real record. Link large evidence rather than copying it. Split an oversized history by date or Queue, leaving a small index; preserve old links.

Stable information belongs in Project, live execution in Current, past outcomes in History. Other places link to the owner rather than repeat its editable status. Small projects need only two live files; additional documents must solve a concrete reading or coordination problem.

### Project model

- **Final goal:** who benefits and what observable outcome constitutes success; include explicit non-goals.
- **Milestone Goals:** independently verifiable outcomes, not percentages or counts of completed tasks. Use only as many as the project needs.
- **Workstreams:** coherent areas of work, each with an objective, primary goal/milestone, acceptance, state and real output dependencies. Keep a compact table in Project; create a separate document only for substantial design or coordination.
- **Current focus:** the outcome being advanced now and its reason. Keep it in Current; normally concentrate on one outcome and only the Workstreams needed for it.
- **Queue:** a finite ordered set of deliverables selected for that focus. Each item names its Workstream when one exists.

A single change may use one milestone, one Workstream and one Queue item without separate hierarchy documents. Phases are optional design subdivisions, not mandatory records, Issues or approval rounds. Plan the near term concretely; leave distant work at outcome level.

Preserve existing IDs. Add new IDs when stable references are needed, not to populate every sentence with identifiers. Dependencies name required outputs; ordering alone does not prove readiness. Detect dependency cycles before execution.

Keep deferred ideas and unresolved bugs as compact entries in Project or the existing tracker: condition/symptom, impact, evidence, disposition, and next trigger. Create a detailed ticket only when useful. Search existing records before adding duplicates. Neither tracking nor deferral authorizes work or removes acceptance criteria. Record incidental out-of-scope findings without interrupting the current Queue for a new priority decision unless they affect its correctness, safety or feasibility.

## 3. Guardrails without duplicate standards

Keep a short Guardrails section in Project, or link an existing authoritative file. Cover applicable boundaries:

- Allowed paths, module/API ownership and architecture constraints.
- Data preservation, secrets, external transmission and security requirements.
- Dependency, migration, generated/vendor code and release policies.
- Authoritative coding/contribution/testing rules; configured check commands and tool requirements.
- Who can approve scope, publication and exceptions; any agreed investigation limits or stop conditions.

Do not manufacture separate full, concise and automation documents when existing instructions/configuration suffice. Before design or code changes, load the actual rules for the affected scope; links alone are not enough. Consult full standards for ambiguity or omitted cases. A short reminder never overrides its source.

When a new instruction arrives, record its meaning, source and affected scope in its owner. Reassess affected work, not every unrelated plan. Resolve conflicts before dependent work. An exception needs scope, reason, approver and review/expiry condition; it never waives higher-priority instructions.

Fold standards conformance into the deliverable's verification and final review. Check changed code against all applicable rules; revalidate checks invalidated by later edits. A separate conformance Phase is needed only for a genuinely separate audit or an established project requirement. Formatting success is not semantic compliance.

## 4. Adoption or migration — once, not every session

1. **Inspect:** repository instructions, README, relevant architecture/source, tools/CI/standards, ongoing plans, approval history and remotes. Read relevant remote state without mutation when needed. Separate facts from assumptions; do not perform an exhaustive code audit merely to adopt planning.
2. **Draft the model:** final goal, scope/non-goals, observable milestones, initial Workstreams, current focus, Guardrails and unresolved decisions. Reuse known answers and existing plans. Present the model for agreement; unresolved intent stays explicitly draft.
3. **Ask one batch of material questions:** include whether additional coding standards or guard instructions exist, unless already answered. Before remote changes, confirm `local-only` or `github`, exact destination, permitted operations and access expectations. Existing consent may be reused only for the same target and operations; credentials/remotes are not consent.
4. **Deploy agreed records:** create/reuse Project and Current, with a proposed Queue and no invented approval, bugs or history. Link this selected skill and the record entry point from the repository's existing agent instructions. Preserve unrelated instructions. A downloaded skill without a discoverable entry is not adoption.
5. **Verify:** links, record ownership, goal/Workstream relationships, relevant rules, approval state and actual mode. Report real paths/URLs and unresolved setup. Deployment does not execute a Queue.

When migrating, first reconcile the active Queue, original approvals, history, authoritative remote state and pending writes. Preserve IDs, evidence and historical outcomes. Agree any source-of-truth or collaboration change explicitly; do not silently reinterpret old states or execute old approvals. Point to the new owners and stop maintaining superseded projections only after a recoverable cutover. Do not delete history to simplify the layout.

## 5. Daily operation

### A. Recover only what is needed

Read repository instructions, Project and Current, then the source, standards and linked evidence relevant to this task. Read history only to resolve a prior decision, failed attempt, approval or missing recovery detail. Do not reload all Workstreams, archived plans and the whole tracker by default.

Check that the recorded state agrees with actual work. Before resuming interrupted execution, verify that no other executor is active and inspect possible completed side effects. Do not blindly repeat migrations, publication or other non-idempotent actions. There is one Queue executor unless the approved Queue explicitly separates independent file/interface ownership.

### B. Agree one finite Queue

Record only what a reviewer needs:

- Queue identity/revision, intended outcome, scope and non-goals.
- Ordered items: deliverable, acceptance/verification, affected components and required outputs.
- Material uncertainty, unresolved decisions and stop conditions; a numeric timebox only if agreed or useful for bounded investigation.
- Approval: approver, exact instruction/source and approved scope snapshot. Before approval, mark it **unapproved**.

Present the concrete Queue for explicit approval before implementation. Reuse a valid approval for exactly that scope; do not ask again for routine edits, technical choices or bookkeeping. “Continue,” a priority change, an Issue label or a Project status is not approval of an unspecified Queue.

Define partial work explicitly before approval. Its success does not complete the containing Phase, Workstream or milestone. If scope, acceptance or risk acceptance changes materially, resolve that change with the decision-maker before affected execution; leave the old approval recoverable.

### C. Execute and verify

Before each item, confirm valid approval, no later stop/cancellation, actual prerequisite outputs and no duplicate execution. Read only relevant decision channels and records, not every board.

Implement within scope; run the configured checks and exercise the changed behavior. Fix in-scope failures under the existing approval: a failing test is feedback, not automatically a blocker or a request for another Queue. Escalate only a missing prerequisite, exhausted agreed investigation bound, or necessary scope/risk decision. Record what actually ran, its result, evidence and limitations. For investigation work, preserve findings and observations rather than manufacturing implementation. For non-code deliverables, use a representative walkthrough or other direct validation and name its limits.

Keep item state simple: pending, active, done, blocked or canceled. “Done” requires its acceptance evidence; canceled is not successful. Record unsuccessful attempts before retrying. A later success does not erase earlier outcomes. A completed item does not automatically satisfy its Workstream or milestone's separate acceptance.

On a blocker, save the attempted work, evidence, exact obstacle and minimum resume condition. Continue independent approved items. Ask only when a human decision is needed. Honor agreed investigation bounds; do not use endless retries to manufacture clearance.

A bug can be tracked without being fixed. An unreproduced concern may be accepted as non-blocking only by an explicit scoped decision, with remaining criteria verified; preserve investigation limits and the residual concern. A known failing acceptance criterion remains unmet until fixed and verified, or explicitly changed by the user; a ticket cannot waive it. Do not label a waiver or unreproduced concern “fixed.”

Save recovery checkpoints after consequential decisions, side effects or meaningful long-running progress, not after every tool call. Honor stop/replacement instructions immediately at their stated scope: an item-specific stop does not revoke independent approved items; a Queue-wide stop does. Reprioritization alone does not expand an active Queue.

### D. Close or hand off once

Before replacing Current, preserve the exact approved scope, attempts, outcomes and decisions in History and verify that the record is recoverable. If blocked mid-Queue, retain that Queue and its approval instead of silently opening another one.

Update only owners whose facts changed. Reassess the affected Workstream/milestone against its own criteria; do not rewrite every summary. Leave the next safe action, blockers and relevant evidence reachable from Current. Mark any future candidates explicitly unapproved.

Report: achieved outcome, verification/limitations, remaining blocker or next decision, and pending publication if any. Do not duplicate transcripts, full tool logs and the same result across several records. Do not automatically start the next Queue.

## 6. Local-only and GitHub

Prefer existing project tooling over inventing a synchronization framework.

- **Local-only:** repository planning files are authoritative. No GitHub prerequisites, outbox, remote polling or permanent “not synchronized” warnings.
- **GitHub:** for a new lean deployment, repository planning files remain authoritative; agreed Issues/Projects publish links and useful Queue-level summaries. Confirm repository/Project and publication permissions first. Do not automatically create one Issue per Phase, standing boards, custom fields or native relationship graphs.
- **Existing GitHub-native projects:** retain their authoritative records and verified integration by default; unchanged ownership needs no new approval. Reuse existing records instead of creating competing local owners. Lightweight operation requires clear ownership and a single writer per record. If two-way/offline synchronization is required, retain the existing verified integration or explicitly agree a local-first cutover; this skill does not provide a synchronization engine.

Publish once at Queue completion or handoff, plus immediate human decision/blocker notifications when needed. If GitHub is an approved decision channel, read the relevant thread at session start/resume and before each item so cancellation or scope decisions are not missed. Do not poll unrelated Issues or refresh all Project fields.

Before a remote write, read the target, preserve human edits and check authority. After writing, read back the affected result. On failure or ambiguous success, retain target, intended action, local revision/evidence and retry condition in Current; discover whether the action succeeded before retrying. Use stable Queue/event markers when creating records or comments so retries do not duplicate them. Local completion and remote publication are separate results.

In local-first mode, archive verified local outcomes and finish the implementation Queue even if summary publication is pending. Carry unresolved publication forward in Current until confirmed; never lose it during Queue rotation. Publication failure alone does not block independent work in a separately approved next Queue. A remote-dependent approval or required evidence that is unavailable still blocks the dependent work.

Do not promise background synchronization, concurrent-write safety or full offline conflict resolution without verified tooling. Do not change visibility, collaborators, credentials or global configuration to bypass a failure. Publication permission does not automatically permit pushing code.

## 7. Minimal starting shapes

Use these headings inside existing equivalents; empty ceremonial sections are unnecessary.

```markdown
# Project
## Goal and scope
Users; final observable outcome; included/excluded work.
## Milestone Goals
ID/name | outcome and acceptance | verified state
## Workstreams
ID/name | primary goal | objective/acceptance | state | output dependencies
## Guardrails
Hard boundaries; authoritative standards/configuration; verification commands.
## Lasting decisions and open questions
Decision/reason/source; or question, affected work and resolution trigger.
## Operating agreement
Mode; record owners/locations; approvers; approved publication targets/operations.
```

```markdown
# Current
## Focus
Outcome and why now.
## Queue <ID/revision>
Scope/non-goals; approval source and exact approved snapshot, or UNAPPROVED.
Item | deliverable/acceptance | dependencies | state | evidence
## Recovery
Current blocker/checkpoint; next safe action; relevant history/design links.
## Pending publication
Only actual outstanding actions; omit when none.
```

History entries need only Queue/attempt identity, approved scope, outcome/evidence, consequential decisions and residual work. Add detailed design, bug or evidence documents only when the information is actually needed.

**Before adding a record, field, approval round or synchronization step, ask: does it protect a real boundary, preserve needed knowledge, or help the next executor act correctly? If not, omit it.**
