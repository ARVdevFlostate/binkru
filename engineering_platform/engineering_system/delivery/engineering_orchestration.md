# Engineering Orchestration

## 1. Purpose

Engineering Orchestration governs the coordinated realization of an authorized Engineering Delivery Plan through Engineering Slices.

The process begins from the Execution Baseline established by an Authorize Execution Readiness Decision and governs realization until the required Engineering outcome reaches a governed conclusion.

Engineering Orchestration explains:

- how authorized Engineering Slices enter and progress through realization;
- how Slice readiness and progression are represented;
- how implementation and technical validation establish Slice completion;
- how Engineering Evidence supports realization and completion claims;
- how dependencies and execution obligations are coordinated;
- how realization responsibility may be allocated across human and automated actors;
- how execution learning is assessed and incorporated;
- how non-material adaptation may occur within delegated authority;
- how material change triggers Engineering governance and reassessment;
- how blocked and paused realization is handled;
- how governed Slice termination is handled;
- how Slice outcomes roll up toward Epic Engineering Completion; and
- how the Engineering Delivery Record preserves what was delivered and the evidence supporting that outcome.

Engineering Orchestration is not a work-management methodology, development workflow, CI/CD model, agent framework, or release process.

It governs realization semantics while allowing operational execution mechanisms to vary.


## 2. Process Position

Engineering Orchestration begins after an Engineering Delivery Plan receives an Authorize Execution Readiness Decision.

The lifecycle position is:

    Engineering-ready Epic
        ↓
    Engineering Delivery Proposal
        ↓
    Investment Decision
        ↓
       Approve
        ↓
    Engineering Delivery Planning
        ↓
    Engineering Delivery Plan
        ↓
    Execution Readiness Decision
        ↓
      Authorize
        ↓
    Execution Baseline
        ↓
    Engineering Orchestration
        ├──────────────→ Engineering Delivery Record
        │                 progressively maintained
        ↓
    Engineering Slice realization
        ↓
    Epic Engineering Completion
        ↓
    Engineering Delivery Record finalized
        ↓
    ─────────────────────────────
       Engineering System boundary
    ─────────────────────────────

The Execution Baseline establishes what Engineering is authorized to realize and the governed envelope within which realization may proceed.

Engineering Orchestration realizes that basis.

Release governance and progression, Release Readiness, environment promotion, and Production promotion are outside Engineering Orchestration and belong to the applicable Release System.


## 3. Process Objective

The objective of Engineering Orchestration is to realize the authorized Engineering basis while preserving:

- governed Epic intent;
- the Approved Investment Baseline;
- the authorized Engineering Delivery Plan;
- Engineering Slice identity and traceability;
- applicable architecture decisions;
- authorization conditions;
- implementation and validation obligations;
- Engineering Evidence obligations;
- applicable acceptance obligations;
- delivery tolerances;
- reassessment triggers;
- material dependencies;
- carried-forward execution obligations;
- external obligations; and
- applicable Engineering authority.

Orchestration SHALL enable Engineering to adapt to execution reality without silently changing a governed basis.

It SHALL distinguish ordinary realization adaptation from changes requiring Engineering governance.


## 4. Governed Inputs

The primary governed input is the Execution Baseline.

The Execution Baseline SHOULD identify or reference:

- the authorized Engineering Delivery Plan revision;
- the Execution Readiness Decision;
- the Approved Investment Baseline;
- the governing Engineering-ready Epic;
- the authorized Engineering Slice structure;
- applicable Authorization Conditions;
- Delivery Tolerances;
- Reassessment Triggers;
- carried-forward uncertainty;
- unresolved architectural obligations;
- Planning Obligations;
- implementation obligations;
- validation obligations;
- Engineering Evidence obligations;
- applicable acceptance obligations;
- dependencies;
- external obligations; and
- other execution constraints material to governed realization.

Additional inputs MAY include:

- Architecture Decision Records;
- Supporting Engineering Artifacts;
- project source code;
- existing Engineering Evidence;
- applicable Development Standards;
- infrastructure and environment information;
- external delivery-management representations;
- operational information;
- security or compliance information;
- actor capability information; and
- other information necessary to perform realization.

Supporting inputs SHALL NOT silently override the Execution Baseline.


## 5. Preconditions

Engineering Orchestration SHOULD begin when:

- an Authorize Execution Readiness Decision exists;
- the authorized Engineering Delivery Plan revision is identifiable;
- the Execution Baseline is identifiable;
- the governing Engineering-ready Epic remains traceable;
- authorized Engineering Slices are identifiable;
- applicable Authorization Conditions are visible;
- material dependencies and obligations are visible;
- Delivery Tolerances and Reassessment Triggers are available where applicable; and
- Engineering has authority to begin governed realization.

Authorization of the Delivery Plan does not imply that every Engineering Slice is immediately ready to begin realization.

Slice-level readiness SHALL be determined from the conditions applicable to that Slice.


## 6. Orchestration Principle

Engineering Orchestration SHALL govern what must remain true during realization without prescribing how teams organize every implementation activity.

Orchestration SHALL govern, as applicable:

- Engineering Slice lifecycle;
- Slice readiness and progression;
- dependencies and sequencing constraints;
- execution obligations;
- architecture obligations;
- technical validation;
- Engineering Evidence;
- material execution learning;
- adaptation boundaries;
- reassessment;
- termination;
- completion; and
- Engineering outcome traceability.

Orchestration SHALL NOT require a particular:

- sprint methodology;
- sprint duration;
- ticket hierarchy;
- story-point convention;
- task-management model;
- branch strategy;
- commit convention;
- pull-request workflow;
- IDE or editor;
- coding-agent implementation;
- AI model or provider;
- CI/CD product;
- issue tracker;
- project-management platform; or
- operational workflow convention.

Operational mechanisms MAY vary provided the governed Engineering semantics remain preserved.


## 7. Engineering Slice as the Unit of Governed Realization

The Engineering Slice is the primary governed unit of realization within Engineering Orchestration.

A Slice SHALL preserve:

- stable identity;
- governing Epic traceability;
- authorized realization intent;
- applicable dependencies;
- applicable architecture basis;
- implementation obligations;
- validation obligations;
- Engineering Evidence obligations;
- applicable acceptance obligations;
- Authorization Conditions;
- carried-forward obligations;
- material execution learning;
- lifecycle state; and
- applicable orthogonal realization conditions.

Operational work such as stories, tasks, tickets, commits, branches, pull requests, agent runs, or CI jobs MAY support realization of a Slice.

Such operational work SHALL NOT become a substitute for the governed identity of the Engineering Slice.


## 8. Canonical Engineering Slice Lifecycle

The canonical Engineering Slice lifecycle is deliberately small.

A Slice SHALL occupy one of the following lifecycle states:

- Authorized;
- Realizing;
- Complete; or
- Terminated.

The normal progression is:

    Authorized
        ↓
    Realizing
       ↙  ↘
    Complete  Terminated

An Authorized Slice MAY also be Terminated before realization begins where applicable governance determines that the authorized realization should no longer proceed.

Complete and Terminated are terminal lifecycle outcomes for that governed Slice revision.

Operational conditions such as readiness, blocking, pause, validation failure, evidence sufficiency, acceptance, or reassessment SHALL NOT be represented by proliferating lifecycle states where they can be represented independently.



## 9. Orthogonal Realization Conditions

Engineering Slice realization SHALL be represented through independent dimensions rather than a single overloaded status.

The canonical realization dimensions are:

    Lifecycle
    Authorized / Realizing / Complete / Terminated

    Readiness
    Not Ready / Ready

    Progression
    Active / Blocked / Paused

    Governance
    Within Baseline / Reassessment Required

    Validation
    Pending / Satisfied / Failed

    Evidence
    Incomplete / Sufficient

    Acceptance
    Not Applicable / Pending / Satisfied

These dimensions describe different aspects of governed realization and SHALL NOT be collapsed into a single lifecycle state.

Not every dimension is applicable in every lifecycle state. Readiness primarily describes whether an Authorized Slice may begin realization, while Progression primarily describes the current ability or intent to progress a Realizing Slice.

A Slice MAY therefore legitimately be represented, for example, as:

    Lifecycle:    Realizing
    Progression:  Paused
    Governance:   Reassessment Required
    Validation:   Pending
    Evidence:     Incomplete
    Acceptance:   Not Applicable

A change in an orthogonal condition SHALL NOT by itself change the Slice lifecycle unless the applicable lifecycle transition criteria are independently satisfied.

## 10. Authorized

Authorized indicates that the Engineering Slice forms part of the governed Execution Baseline.

Authorized does not necessarily mean that realization may begin immediately.

An Authorized Slice MAY remain unable or inappropriate to begin because of:

- unsatisfied Authorization Conditions;
- predecessor dependencies;
- unavailable external dependencies;
- unresolved architectural obligations;
- unavailable environments or capabilities;
- sequencing constraints;
- governed timing decisions; or
- other applicable execution conditions.

An Authorized Slice SHALL remain traceable to the Execution Baseline from which its authority derives.


## 11. Slice Readiness

Readiness describes whether an Authorized Slice has sufficient conditions in place to begin realization.

Readiness MAY be represented as:

- Not Ready; or
- Ready.

A Slice is Ready when applicable prerequisites to begin realization are sufficiently satisfied.

Readiness is an orthogonal condition and SHALL NOT create a separate lifecycle state.

Transition from Authorized to Realizing occurs when realization actually begins, not merely when the Slice becomes Ready.


## 12. Realizing

Realizing indicates that governed realization of the Engineering Slice has begun and has not reached a terminal lifecycle outcome.

Realization MAY include:

- composition;
- implementation;
- integration;
- technical investigation;
- automated or manual testing;
- technical validation;
- defect correction;
- architecture work;
- infrastructure work;
- migration work;
- evidence production;
- supporting documentation; and
- other Engineering activity necessary to realize the Slice.

These activities MAY overlap, repeat, or occur continuously.

Engineering Orchestration SHALL NOT require a linear implementation sequence where the nature of the work does not require one.


## 13. Progression Condition

A Realizing Slice MAY have one of the following progression conditions:

- Active;
- Blocked; or
- Paused.

Progression is orthogonal to the Slice lifecycle.

### 13.1 Active

Active indicates that realization is permitted and currently expected to progress.

### 13.2 Blocked

Blocked indicates that realization cannot currently progress because an applicable impediment prevents meaningful continuation.

A blocker SHOULD identify:

- the blocking condition;
- affected realization;
- material consequences where known;
- expected resolution mechanism or dependency where known; and
- whether the blocker creates or contributes to a Reassessment Required condition.

A blocked Slice remains Realizing unless governance determines otherwise.

### 13.3 Paused

Paused indicates that realization has been intentionally suspended even though the Slice has not reached a terminal outcome.

A Pause SHOULD preserve:

- the reason for suspension;
- the actor or authority initiating the Pause;
- the effective point of suspension; and
- material consequences where applicable.

Where useful, a Pause MAY also identify:

- an expected resume condition;
- an expected resume date or period;
- dependency consequences;
- timeline consequences; and
- effects on other Slices.

A Paused Slice remains Realizing.

### 13.4 Resume

Resume is an orchestration event, not a lifecycle state.

Resume returns a Paused Slice to Active progression when the applicable basis for resumption is satisfied.

Resume SHALL preserve Slice identity and prior realization history.

Pause and Resume SHALL NOT create a new Engineering Slice merely because execution was temporarily suspended.


## 14. Non-linear Realization

Engineering realization is not assumed to be linear.

Implementation, validation, evidence production, architecture work, dependency resolution, and defect correction MAY occur iteratively.

For example:

    Implement
        ↓
    Validate
        ↓
    Learning / defect
        ↓
    Revise implementation
        ↓
    Validate again

A failed implementation or validation attempt does not itself mean that the Engineering Slice has failed.

The Slice MAY remain Realizing while Engineering:

- retries;
- revises implementation;
- changes an implementation detail within authority;
- reallocates realization responsibility;
- obtains additional expertise;
- resolves a blocker; or
- performs another permitted adaptation.

A terminal outcome SHALL be determined from the governed Slice outcome, not from the success or failure of an individual execution attempt.


## 15. Realization Responsibility and Actor Allocation

Engineering Slice realization MAY be performed by:

- human engineers;
- human teams;
- AI agents;
- automated engineering systems;
- specialist agents;
- mixed human and AI teams; or
- other execution actors permitted by applicable governance.

Orchestration MAY dynamically allocate or reallocate realization responsibility where the available actor is appropriate to the Slice's:

- complexity;
- required context;
- technical capability requirements;
- risk;
- obligations;
- authority requirements; and
- Engineering significance.

Changing the realization actor SHALL NOT by itself change:

- Slice identity;
- Slice lifecycle state;
- governed intent;
- the Execution Baseline; or
- completion semantics.

Actor selection, AI model selection, model size, provider selection, token budgets, prompt construction, retry strategies, and multi-agent topology are execution-platform concerns unless they materially affect a governed Engineering basis.

Where actor capability becomes insufficient to realize the Slice credibly, Orchestration SHOULD reallocate, escalate, or otherwise respond proportionately.


## 16. Composition During Orchestration

Composition MAY prepare the governed context and artifacts required for realization.

Where composition is used, it SHALL operate according to the Composition Specification.

Composition MAY include relevant:

- governing artifacts;
- Slice context;
- architecture decisions;
- applicable Development Standards;
- dependencies;
- implementation obligations;
- validation obligations;
- evidence obligations;
- acceptance obligations; and
- other execution context.

Composition MAY be performed by humans, automation, AI-assisted tooling, or combinations thereof.

Composition SHALL NOT alter the governed basis merely by generating a different execution context.


## 17. Implementation

Implementation realizes the authorized Engineering Slice through applicable Engineering practices, technologies, standards, and tooling.

Implementation practices MAY vary between teams and organizations.

Implementation SHALL remain consistent with:

- the governing Engineering-ready Epic;
- the Execution Baseline;
- the authorized Engineering Delivery Plan;
- applicable Architecture Decision Records;
- applicable Development Standards;
- applicable Authorization Conditions;
- implementation obligations;
- external obligations; and
- applicable Engineering governance.

Implementation detail MAY evolve during realization where the change remains within the Execution Baseline, applicable tolerances, and delegated authority.


## 18. Technical Validation

Each Engineering Slice SHALL receive sufficient technical validation to establish whether its implemented realization satisfies its applicable technical obligations.

Validation MAY include, as applicable:

- automated testing;
- unit testing;
- integration testing;
- security validation;
- performance validation;
- reliability validation;
- compatibility validation;
- migration validation;
- operational validation;
- deployment validation; and
- other Engineering verification.

Validation MAY occur continuously during implementation.

A validation failure SHALL normally cause additional realization rather than create a separate Slice lifecycle state.

Where validation failure reveals material execution learning, the applicable change and reassessment rules SHALL apply.


## 19. Engineering Evidence

Engineering Evidence supports claims made during Engineering Orchestration.

Evidence MAY be produced throughout:

- composition;
- implementation;
- validation;
- architecture work;
- dependency resolution;
- automation;
- deployment-related technical validation; and
- other realization activity.

Evidence MAY remain in authoritative systems where it naturally originates.

Engineering Orchestration SHOULD reference authoritative evidence rather than duplicate it unnecessarily.

Evidence MAY include:

- test results;
- CI results;
- validation reports;
- Architecture Decision Records;
- security evidence;
- performance evidence;
- migration evidence;
- deployment-validation evidence;
- operational evidence;
- source-control references;
- artifact identities;
- review records; and
- other information capable of supporting an Engineering claim.

Evidence sufficiency is an orthogonal condition.

Evidence SHALL be sufficient to support a Slice completion claim when the Slice transitions to Complete.


## 20. Applicable Acceptance Obligations

Engineering Slice completion does not universally require a separate human or governance acceptance decision.

Where the Execution Baseline establishes a specific Slice-level acceptance obligation, that obligation SHALL remain applicable.

Acceptance MAY be:

- not applicable;
- pending; or
- satisfied.

Acceptance is orthogonal to the Slice lifecycle unless the governing basis explicitly makes that acceptance a prerequisite to completion.

The absence of a universal Slice acceptance gate SHALL NOT remove acceptance obligations explicitly established by the Engineering Delivery Plan, Engineering governance, architecture governance, security governance, compliance obligations, or another applicable authority.


## 21. Slice Completion

An Engineering Slice becomes Complete when:

- its authorized realization has been implemented;
- its applicable technical validation has been successfully satisfied; and
- sufficient Engineering Evidence exists to support that determination.

Where the governing basis explicitly establishes an additional prerequisite to completion, that prerequisite SHALL also be satisfied or receive an applicable governed disposition before completion may be asserted.

A Slice SHALL NOT be considered Complete solely because:

- code has been written;
- code has been merged;
- a pull request has been approved;
- an external ticket is marked Done;
- an automated agent reports success;
- an artifact has been deployed to an environment; or
- an implementation attempt has ended.

Completion is an Engineering determination grounded in implemented realization and successful applicable technical validation.

Once Complete, the Slice SHALL preserve the evidence supporting the completion claim.


## 22. Execution Obligations

Orchestration SHALL preserve applicable execution obligations entering from the Execution Baseline.

These MAY include:

- Authorization Conditions;
- Planning Obligations;
- architecture obligations;
- implementation obligations;
- validation obligations;
- Engineering Evidence obligations;
- acceptance obligations;
- dependency obligations;
- external obligations; and
- other governed execution commitments.

An obligation entering Orchestration SHALL receive an explicit disposition where its disposition is material to governed realization.

Possible dispositions MAY include:

- satisfied;
- superseded through governance;
- rendered no longer applicable;
- transferred to an explicitly governed later realization point;
- escalated;
- accepted as a governed residual condition; or
- otherwise resolved through applicable governance.

Orchestration SHALL NOT silently discard a material execution obligation.


## 23. Dependency Coordination

Engineering Orchestration SHALL coordinate dependencies that materially affect realization.

Dependencies MAY exist:

- between Engineering Slices;
- between a Slice and an architectural decision;
- between Engineering and an external system;
- between Engineering and another organizational function;
- between realization and an environment;
- between realization and a required capability or resource; or
- between Engineering and another governed artifact or decision.

Orchestration MAY change operational sequencing within delegated authority where the authorized realization remains credible.

A dependency change that materially affects a governed basis SHALL be assessed under the materiality and reassessment rules.


## 24. Execution Learning

Execution Learning is information discovered during realization that affects or may affect how Engineering understands the authorized realization.

Execution Learning MAY arise from:

- implementation;
- technical validation;
- architecture work;
- dependency behavior;
- external change;
- cost change;
- tooling or component change;
- licensing change;
- security findings;
- performance findings;
- operational findings;
- failed execution attempts;
- newly discovered constraints;
- changed assumptions; or
- other realization experience.

Not every execution observation requires a governed record.

Material Execution Learning SHALL be preserved sufficiently to explain its consequence and resulting disposition.


## 25. Materiality

Materiality is the primary boundary between autonomous realization adaptation and Engineering governance.

Materiality SHALL be assessed by consequence to governed Engineering bases and commitments rather than by the apparent size of an implementation change.

Execution Learning or a proposed adaptation is material where it materially affects, or may invalidate, an applicable governed basis such as:

- the Approved Investment Baseline;
- the Execution Baseline;
- governed Epic intent;
- authorized realization scope;
- architecture;
- security or compliance obligations;
- external obligations;
- Engineering risk;
- cost, effort, or delivery timing;
- dependencies;
- Authorization Conditions;
- Planning or execution obligations;
- validation basis;
- evidence basis;
- acceptance basis; or
- another governed Engineering commitment.

A technically small implementation change MAY be material where its consequences alter a governed basis.

A technically large implementation change MAY remain non-material where its consequences remain within the authorized basis and delegated authority.


## 26. Tolerances and Reassessment Triggers

Delivery Tolerances and Reassessment Triggers support determination of whether execution remains within authorized bounds.

Remaining within an applicable tolerance is evidence that an adaptation may remain within delegated authority.

Exceeding an applicable tolerance SHALL trigger the applicable reassessment mechanism.

Tolerances SHALL NOT override an independently material impact on another governed basis.

A change MAY therefore require governance even where a numeric cost, effort, or timing tolerance has not been exceeded.


## 27. Adaptation Within Authority

Engineering Orchestration MAY adapt realization without a new governance decision where:

- the adaptation is non-material to governed Engineering bases;
- the adaptation remains within applicable Delivery Tolerances;
- no Reassessment Trigger applies;
- applicable architecture governance is preserved;
- applicable obligations remain satisfiable;
- the actor possesses authority to make the adaptation; and
- the authorized realization remains credible.

Permitted adaptation MAY include, as applicable:

- refinement of low-level implementation detail;
- changes to operational work decomposition;
- reordering work;
- changing execution actors;
- retrying failed execution approaches;
- replacing an implementation detail;
- refining tests;
- improving internal implementation;
- resolving ordinary defects; and
- other changes that remain within the governed execution envelope.

Permitted adaptation SHALL NOT silently rewrite the historical basis on which execution was authorized.


## 28. Reassessment Required

Reassessment Required is an orthogonal governance condition.

It indicates that execution has encountered learning or proposed change that cannot responsibly be handled solely through existing delegated authority.

Reassessment Required MAY arise because:

- a governed basis is materially affected;
- an applicable tolerance is exceeded;
- a Reassessment Trigger occurs;
- materiality cannot be determined with sufficient confidence;
- architecture governance requires reassessment;
- an Authorization Condition can no longer be satisfied as intended;
- a material dependency changes;
- an external constraint materially changes;
- an obligation becomes materially infeasible; or
- another governance boundary is reached.

A Slice requiring reassessment MAY remain Realizing.

Its progression MAY become Paused or Blocked where continuation would exceed authority or create unacceptable consequence.

Independent Slices MAY continue where their realization remains within the Execution Baseline and applicable authority.

Reassessment Required SHALL NOT itself imply termination.


## 29. Uncertain Materiality

Where an actor cannot determine with sufficient confidence whether execution learning is material, the actor SHOULD escalate proportionately to the potential consequence.

Uncertain materiality SHALL NOT be silently treated as non-material merely to preserve execution momentum.

Escalation SHOULD remain proportionate.

Trivial uncertainty with negligible governed consequence SHOULD NOT create unnecessary ceremony.


## 30. Governed Reassessment

Material change SHALL be handled through the applicable Engineering governance mechanism.

Reassessment MAY result in:

- continuation on the existing basis;
- an authorized adaptation;
- revision of the Engineering Delivery Plan;
- a new or revised Architecture Decision Record;
- changed conditions or obligations;
- changed Slice structure;
- return to Delivery Planning;
- upstream boundary escalation;
- Slice termination;
- replacement realization; or
- another governed disposition.

Reassessment SHALL preserve the historical Execution Baseline and the reason the original realization basis changed.

Learning changes the future realization basis; it SHALL NOT rewrite the governed past.


## 31. Engineering Slice Termination

Terminated indicates that governed realization of an Engineering Slice has been intentionally ended before satisfying its completion basis.

Termination is a governed terminal outcome.

Termination SHALL identify, as applicable:

- the terminated Slice;
- the reason for termination;
- the applicable decision or authority;
- the point at which realization ended;
- remaining execution obligations;
- evidence produced before termination;
- effects on dependent Slices;
- effects on the governing Epic;
- effects on the Execution Baseline; and
- whether replacement realization is required.

Termination MAY occur because of:

- external constraint change;
- dependency loss;
- economic invalidation;
- architectural invalidation;
- technical infeasibility;
- changed governed intent;
- unacceptable risk;
- superseding realization; or
- another governed reason.

These examples do not create separate lifecycle states.

A Slice SHALL remain historically identifiable after termination.

Termination SHALL NOT silently delete or rewrite the terminated Slice.


## 32. Replacement and Superseding Realization

A terminated Slice MAY be replaced by another authorized Slice where the required Engineering outcome remains necessary.

Replacement realization SHALL receive its own governed identity.

For example:

    Slice S-04
        ↓
    material external change
        ↓
    governed reassessment
        ↓
    S-04 Terminated
        ↓
    replacement realization authorized
        ↓
    Slice S-09

The replacement Slice SHALL NOT overwrite the historical identity or realization record of the terminated Slice.

Traceability SHOULD explain why replacement realization exists and what governed requirement it continues or changes.


## 33. Slice Outcome Roll-up

Engineering Slice outcomes SHALL roll up toward the governing Epic.

A Complete Slice contributes satisfied Engineering realization to the Epic.

A Terminated Slice does not automatically prevent Epic Engineering Completion where:

- the termination received an appropriate governed disposition;
- required realization has been replaced, superseded, or rendered no longer applicable through governance; and
- no required Epic outcome remains unaccounted for.

A terminated Slice SHALL prevent a successful Epic completion claim where its termination leaves required Engineering realization materially unsatisfied.


## 34. Epic Engineering Completion

Epic Engineering Completion establishes that the Engineering realization required for the governing Engineering-ready Epic has been implemented and technically validated to the extent required by its governed Engineering basis.

Epic Engineering Completion SHOULD consider, as applicable:

- required Engineering Slice outcomes;
- integrated technical behavior;
- cross-Slice dependencies;
- aggregate technical validation;
- Engineering Evidence;
- architecture conformance;
- approved exceptions;
- security obligations;
- performance obligations;
- reliability obligations;
- operational technical obligations;
- unresolved governed issues; and
- dispositions of terminated or superseded realization.

Epic Engineering Completion SHALL NOT by itself establish:

- Product acceptance;
- Release Admission;
- Release Readiness;
- Production deployment authority;
- commercial launch authority; or
- another authority outside the Engineering System.

Epic Engineering Completion is an Engineering outcome.


## 35. Engineering Delivery Record

Engineering Orchestration SHALL progressively maintain a governed Engineering Delivery Record sufficient to establish what was actually delivered against the authorized Engineering basis.

The Engineering Delivery Record SHOULD accumulate material realization information as it arises rather than depend on retrospective reconstruction after Engineering realization has concluded.

During realization, the Engineering Delivery Record SHOULD preserve or reference, as applicable:

- governing Engineering-ready Epic;
- Approved Investment Baseline;
- authorized Engineering Delivery Plan and Execution Baseline;
- Engineering Slice outcomes and progression where materially relevant;
- terminated Slice dispositions;
- replacement or superseding realization;
- material execution learning;
- material governed adaptations;
- reassessment outcomes;
- material obligation dispositions;
- architecture decisions arising during realization;
- technical validation outcomes;
- applicable acceptance outcomes;
- Engineering Evidence references;
- approved exceptions; and
- unresolved governed residual conditions.

When the governed Engineering realization reaches its conclusion, the Engineering Delivery Record SHALL be finalized to preserve the resulting Epic Engineering Completion outcome or other governed realization conclusion.

Finalization SHALL NOT require duplication of all operational execution data.

The Engineering Delivery Record SHOULD reference authoritative evidence and operational records where those records remain trustworthy and traceable.

The Engineering Delivery Record therefore provides a progressively maintained and ultimately finalized governed evidentiary record of Engineering delivery.

## 36. Engineering Delivery Record and Engineering Evidence

The Engineering Delivery Record and Engineering Evidence are related but distinct.

Engineering Evidence establishes specific Engineering claims.

The Engineering Delivery Record identifies and preserves the governed delivery outcome and references the evidence supporting that outcome.

For example:

    Engineering Delivery Record
        ├── Slice S-01: Complete
        │      └── evidence references
        ├── Slice S-02: Complete
        │      └── evidence references
        ├── Slice S-03: Terminated
        │      └── governed disposition
        ├── material reassessment
        │      └── decision reference
        └── Epic Engineering Completion
               └── aggregate evidence references

The Delivery Record SHALL NOT become a substitute for authoritative evidence sources where reference is sufficient.


## 37. External Delivery-management Tools

Engineering Orchestration MAY be represented operationally in external delivery-management tools.

External representations MAY include:

- Epics;
- stories;
- tasks;
- tickets;
- boards;
- milestones;
- workflows;
- status fields;
- dependencies; and
- other tool-native structures.

External tool state SHALL NOT silently redefine the canonical Engineering Slice lifecycle or governed Engineering state.

For example:

    Jira status = Done

does not by itself establish:

    Engineering Slice = Complete

Canonical completion remains determined by Engineering Orchestration semantics.

Where external representations diverge from canonical governed state, the canonical Engineering state SHALL prevail.


## 38. Source Control, CI/CD, and Development Tooling

Source-control, CI/CD, development, testing, infrastructure, and automation tools MAY perform substantial parts of Engineering realization.

These tools MAY produce authoritative Engineering Evidence.

Engineering Orchestration SHALL remain independent of any specific product or vendor.

Operational tool events SHALL acquire governed significance only where they satisfy, change, evidence, or materially affect an applicable Engineering obligation or state.


## 39. AI-assisted Engineering Orchestration

AI systems MAY assist Engineering Orchestration by:

- composing Slice execution context;
- analyzing dependencies;
- implementing Engineering Slices;
- generating tests;
- performing technical analysis;
- identifying defects;
- supporting validation;
- collecting or linking Engineering Evidence;
- identifying execution learning;
- proposing adaptations;
- assessing possible materiality;
- identifying Reassessment Triggers;
- supporting architecture work;
- proposing actor reallocation;
- summarizing realization history;
- checking completion conditions; and
- drafting Engineering Delivery Record content.

AI-generated execution results SHALL be evaluated according to their Engineering significance.

An AI system reporting success SHALL NOT itself establish Slice completion unless applicable governance explicitly permits the system to make that determination and the completion basis is satisfied.

AI systems MAY adapt realization only within delegated authority.

AI systems SHALL NOT infer termination authority merely because reassessment is required.

Where materiality is uncertain, AI systems SHOULD escalate proportionately to the potential consequence.


## 40. Human, AI, and Mixed-team Operation

Engineering Orchestration SHALL support:

- human-led Engineering teams;
- AI-assisted human teams;
- mixed human and AI-agent teams;
- AI-led realization where governance permits it; and
- dynamically changing combinations of those actors.

The canonical lifecycle, completion semantics, materiality rules, evidence expectations, and governance boundaries SHALL remain consistent regardless of whether realization is performed by humans, automated actors, or both.

Authority SHALL be determined by applicable Engineering governance rather than inferred solely from actor type.


## 41. Proportional Application

Engineering Orchestration SHALL be applied proportionately to the Engineering significance of the realization.

A small, familiar, low-risk Slice MAY require:

- lightweight progression tracking;
- simple validation;
- automatically produced evidence;
- minimal explicit orchestration records; and
- delegated completion authority.

A large, uncertain, architecturally significant, operationally sensitive, security-sensitive, or dependency-heavy Slice MAY require:

- stronger coordination;
- explicit progression conditions;
- substantial validation;
- richer evidence;
- specialist actors;
- more explicit materiality assessment;
- stronger reassessment controls; and
- explicit governed decisions.

Proportionality SHALL NOT remove information or controls necessary to support a defensible Engineering completion claim.


## 42. Process Output

The primary realization outputs are:

- completed or governably terminated Engineering Slices;
- Epic Engineering Completion where applicable; and
- Engineering Delivery Record.

Supporting outputs MAY include:

- Architecture Decision Records;
- Engineering Change Assessments;
- Engineering Evidence;
- Supporting Engineering Artifacts;
- validation results;
- dependency records;
- exception records;
- reassessment decisions;
- operational tool references; and
- other realization artifacts or records.

Engineering Orchestration SHALL preserve sufficient traceability from the Execution Baseline to the resulting Engineering outcome.


## 43. Boundary to Release

Engineering Orchestration ends at the Engineering System boundary.

Engineering Completion SHALL NOT automatically imply that an Engineering outcome enters Release governance.

Where an applicable cross-system Release Admission decision exists, the Engineering Delivery Record provides the Engineering basis for that decision.

Release Admission, Release governance and progression, Release Readiness, promotion paths, environment progression, and Production promotion are outside the scope of Engineering Orchestration.

Those concerns SHALL be governed by the applicable cross-system and Release System specifications.


## 44. Process Summary

Engineering Orchestration can be summarized as:

    Execution Baseline
            ↓
    Authorized Engineering Slices
            ↓
    Slice readiness
            ↓
    Governed realization ─────────────→ Engineering Delivery Record
      ↙       ↓        ↘                  progressively maintained
    human    AI      mixed actors
            ↓
    implementation
            +
    technical validation
            +
    Engineering Evidence
            ↓
    Slice Complete
       or
    governed Termination
            ↓
    Slice outcome roll-up
            ↓
    Epic Engineering Completion
            ↓
    Engineering Delivery Record finalized
            ↓
    ─────────────────────────────
       Engineering System boundary
    ─────────────────────────────

Throughout realization:

    execution learning
            ↓
    materiality assessment
       ↙             ↘
    non-material     material /
       ↓             uncertain
    adapt within         ↓
    authority        governance /
                     reassessment

Engineering Orchestration therefore provides a governed but non-linear realization model that preserves Engineering authority, evidence, traceability, and material change control without prescribing the operational mechanisms used to perform Engineering work.
