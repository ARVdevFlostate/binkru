# Engineering Lifecycle Specification

## 1. Purpose

This specification defines the governed lifecycle through which the
Engineering System transforms an Engineering-ready Epic into a governed
Engineering conclusion.

The lifecycle establishes:

-   the entry and conclusion boundaries of the Engineering System;
-   the progression from Engineering Delivery Proposal through
    Engineering Delivery Record;
-   the decision gates that authorize Engineering investment and
    execution;
-   the Approved Investment Baseline and Execution Baseline;
-   the relationship between Engineering Delivery Proposal, Engineering
    Delivery Planning, Engineering Delivery Plan, Engineering
    Orchestration, and Engineering Delivery Record;
-   the role and lifecycle of Engineering Slices;
-   the treatment of architecture, validation, evidence, acceptance,
    execution learning, adaptation, and reassessment;
-   the conditions for Epic Engineering Completion;
-   the treatment of a Non-Completion Engineering Conclusion; and
-   the boundary between concluded Engineering realization and
    downstream Release governance.

This specification defines the top-level Engineering lifecycle.

Detailed process, artifact, record, governance, and decision semantics
SHALL remain authoritative in their applicable Engineering System
specifications.

The Engineering Lifecycle governs Engineering delivery without
prescribing a project-management or team-delivery framework.

Engineering teams MAY use Scrum, Kanban, Scrumban, continuous flow,
agentic realization, or other delivery practices provided those
practices operate within the governance boundaries defined by the
Engineering System.

## 2. Lifecycle Boundary

The Engineering System begins when it accepts an Engineering-ready Epic
through the applicable upstream Collaboration System boundary.

The Engineering System concludes when governed Engineering realization
reaches exactly one Engineering conclusion:

-   Epic Engineering Completion; or
-   Non-Completion Engineering Conclusion.

The Engineering Delivery Record is progressively maintained during
realization and finalized when the applicable Engineering conclusion is
established.

The canonical lifecycle is:

    Engineering-ready Epic
            ↓
    Engineering Delivery Proposal
            ↓
    Investment Decision
            ↓
         Approve
            ↓
    Approved Investment Baseline
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
            ↓
    Engineering Slice realization
            ↓
    Engineering Conclusion
       ├── Epic Engineering Completion
       └── Non-Completion Engineering Conclusion
            ↓
    Engineering Delivery Record finalized
            ↓
    ─────────────────────────────
       Engineering System boundary
    ─────────────────────────────

Return, Defer, Reject, reassessment, Pause/Resume, termination,
replacement realization, and other governed non-linear paths MAY occur
where permitted by the applicable specifications.

The lifecycle SHALL NOT be interpreted as requiring realization to
proceed linearly.

## 3. Lifecycle Principles

### 3.1 Governed Entry

Engineering realization SHALL begin from an Engineering-ready Epic
accepted through the applicable upstream governance boundary.

Engineering SHALL preserve traceability to that governing Epic
throughout the lifecycle.

### 3.2 Proposal Before Investment Commitment

Engineering SHALL establish an Engineering Delivery Proposal sufficient
to support a defensible Investment Decision before detailed delivery
planning is authorized.

Proposal analysis SHALL remain proportionate to the investment decision
being made.

### 3.3 Investment Authorization Before Delivery Planning

Engineering Delivery Planning SHALL begin only from an applicable
Approve Investment Decision.

An approved proposal establishes the governed investment basis for
planning.

### 3.4 Planning Before Execution

Engineering SHALL establish an Engineering Delivery Plan sufficient to
support an Execution Readiness Decision before governed realization
begins.

Implementation activity SHALL NOT be treated as authorized Engineering
realization merely because exploratory or preparatory technical work
occurred earlier.

### 3.5 Execution Baseline Before Orchestration

Engineering Orchestration SHALL begin only after an Authorize Execution
Readiness Decision establishes an Execution Baseline.

The Execution Baseline defines what Engineering is authorized to realize
and the governed envelope within which realization may proceed.

### 3.6 Engineering Slice as the Governed Unit of Realization

An authorized Engineering Delivery Plan SHALL be realized through one or
more Engineering Slices.

A Delivery Plan MAY contain a single Slice where further decomposition
would not provide meaningful realization or governance value.

### 3.7 Evidence Before Completion Claims

Engineering completion claims SHALL be supported by applicable technical
validation and sufficient Engineering Evidence.

Completion SHALL NOT be inferred solely from code completion, merge
status, ticket closure, agent-reported success, deployment, or another
operational signal.

### 3.8 Controlled Evolution

Engineering realization MAY evolve as technical knowledge increases.

Non-material adaptation MAY occur within applicable authority,
tolerances, and the Execution Baseline.

Material change SHALL be governed through reassessment rather than
silently absorbed into realization.

### 3.9 Historical Integrity

Governed Engineering history SHALL remain traceable.

Reassessment, Plan revision, Slice termination, replacement realization,
or another governed change SHALL NOT rewrite prior authorized bases or
erase historical realization.

### 3.10 Progressive Delivery Record

The Engineering Delivery Record SHALL be instantiated when Engineering
Orchestration begins and progressively maintained as material
realization information arises.

The EDR SHALL preserve the governed relationship between authorized
basis, actual realization, material change, evidence, and Engineering
conclusion.

### 3.11 Framework and Tool Independence

The Engineering Lifecycle SHALL remain independent of specific
project-management, issue-tracking, source-control, CI/CD, AI-agent, or
delivery-management products.

External tools MAY represent Engineering information but SHALL NOT
silently redefine canonical Engineering semantics.

## 4. Engineering-ready Epic

The Engineering-ready Epic is the authoritative lifecycle input.

It represents an Epic that has completed the applicable upstream
Collaboration System activities and is ready for Engineering
consideration.

The Engineering-ready Epic establishes or references the governed
capability intent, constraints, agreements, acceptance context, and
other information required for Engineering to begin technical
consideration.

Engineering MAY discover information that challenges assumptions or
agreements represented by the Engineering-ready Epic.

Where such information cannot be resolved within Engineering authority,
Engineering SHALL use the applicable upstream or cross-system governance
path rather than silently redefining Product or Collaboration intent.

## 5. Engineering Delivery Proposal

The Engineering Delivery Proposal establishes the proposed Engineering
investment and realization basis for the Engineering-ready Epic.

It answers:

> Should Engineering investment be committed to this realization, and on
> what basis?

The proposal SHALL provide sufficient Engineering understanding to
support a defensible Investment Decision without prematurely becoming a
detailed execution plan.

Proposal development MAY include, proportionate to Engineering
significance:

-   Engineering interpretation;
-   realization framing;
-   technical feasibility;
-   Engineering discovery;
-   realization alternatives;
-   architecture analysis;
-   dependencies and constraints;
-   capability and resource needs;
-   indicative effort and cost;
-   indicative delivery range;
-   basis of estimate;
-   confidence and uncertainty;
-   assumptions;
-   Engineering risks;
-   issues and blockers; and
-   an Engineering recommendation.

Proposal estimates SHALL remain indicative rather than execution
commitments.

Detailed proposal semantics are defined by the Engineering Delivery
Proposal specification.

## 6. Investment Decision

A ready Engineering Delivery Proposal SHALL pass through an Investment
Decision governed by the applicable Engineering authority.

Canonical Investment Decision outcomes are:

-   Approve;
-   Return;
-   Defer; or
-   Reject.

An Approve outcome authorizes transition to Engineering Delivery
Planning and establishes the Approved Investment Baseline.

Return sends the proposal for additional analysis, clarification, or
revision.

Defer retains the proposal and decision basis without authorizing
present investment progression.

Reject declines the proposed Engineering investment and preserves the
decision rationale and authority.

An Investment Decision MAY include explicit approved conditions where
permitted by the applicable governance specification.

The Investment Decision SHALL NOT silently alter upstream governed
intent outside Engineering authority.

## 7. Approved Investment Baseline

An Approve Investment Decision establishes the Approved Investment
Baseline.

The Approved Investment Baseline preserves the Engineering investment
basis that Delivery Planning is authorized to refine.

It SHOULD identify or reference, as applicable:

-   the governing Engineering-ready Epic;
-   approved Engineering Delivery Proposal revision;
-   Investment Decision;
-   approved realization framing;
-   approved assumptions and conditions;
-   approved investment basis;
-   material dependencies and constraints;
-   material Engineering risks;
-   accepted uncertainty; and
-   other governed information necessary to explain the investment
    authorization.

Engineering Delivery Planning MAY refine execution detail without
silently changing the Approved Investment Baseline.

Where planning discovery materially challenges that basis, applicable
reassessment or governance SHALL occur.

## 8. Engineering Delivery Planning

Engineering Delivery Planning transforms the Approved Investment
Baseline into an execution-ready Engineering realization.

It answers:

> How will the approved Engineering investment be realized under
> governed execution?

Planning SHALL refine the approved basis into sufficient realization
structure, including as applicable:

-   Engineering Slices;
-   Slice boundaries and traceability;
-   sequencing and incremental realization;
-   architecture planning;
-   dependencies;
-   implementation obligations;
-   validation obligations;
-   applicable acceptance obligations;
-   Engineering Evidence obligations;
-   capability and resource assumptions;
-   refined estimates;
-   delivery timeline and milestones;
-   execution risks;
-   assumptions and uncertainty;
-   approved conditions and Planning Obligations;
-   Delivery Tolerances; and
-   Reassessment Triggers.

Planning SHALL preserve the Approved Investment Baseline while making
execution sufficiently explicit for an Execution Readiness Decision.

Detailed planning semantics are defined by the Engineering Delivery
Planning specification.

## 9. Engineering Delivery Plan

The Engineering Delivery Plan is the governed output of Engineering
Delivery Planning.

It defines the proposed execution basis for realizing the approved
Engineering investment.

The Plan SHALL remain traceable to:

-   the Engineering-ready Epic;
-   approved Engineering Delivery Proposal;
-   Investment Decision;
-   Approved Investment Baseline; and
-   applicable architecture and governance decisions.

The Engineering Delivery Plan MAY evolve before authorization.

A Plan revision SHALL remain historically traceable where revision is
material to governed execution.

The Plan SHALL NOT itself authorize execution merely because it is
complete or internally ready.

## 10. Engineering Slice

An Engineering Slice is the canonical governed unit of Engineering
realization.

A Slice SHOULD be sufficiently bounded and technically coherent to
support controlled realization and applicable validation.

Engineering Slices SHALL remain traceable to the governing Engineering
Delivery Plan and Engineering-ready Epic.

Planning MAY decompose realization into Slices according to technical,
dependency, validation, evidence, risk, or delivery considerations.

The Engineering System SHALL NOT require a separate canonical
Engineering Work Item layer.

Teams and tools MAY decompose a Slice into tasks, stories, work items,
subtasks, agent jobs, or other operational units where useful.

Such operational decomposition SHALL NOT silently acquire canonical
Engineering governance semantics merely because an external tool
represents it.

## 11. Execution Readiness Decision

A ready Engineering Delivery Plan SHALL pass through an Execution
Readiness Decision before Engineering Orchestration begins.

The Execution Readiness Decision determines whether the Plan provides a
sufficiently governed basis for realization.

Canonical outcomes are defined by the applicable Delivery Planning and
Engineering Governance specifications.

An Authorize outcome establishes the Execution Baseline and permits
transition to Engineering Orchestration.

A readiness recommendation produced during planning SHALL NOT itself
constitute the Execution Readiness Decision unless the applicable
authority explicitly establishes it as such.

## 12. Execution Baseline

The Execution Baseline is the governed Engineering basis authorized for
realization.

It SHOULD identify or preserve, as applicable:

-   the authorized Engineering Delivery Plan revision;
-   Execution Readiness Decision;
-   Approved Investment Baseline;
-   Engineering Slice structure;
-   architecture basis;
-   implementation obligations;
-   validation obligations;
-   Engineering Evidence obligations;
-   applicable acceptance obligations;
-   dependencies;
-   authorization conditions;
-   Delivery Tolerances;
-   Reassessment Triggers; and
-   other governed execution commitments.

The Execution Baseline answers:

> What is Engineering authorized to realize?

The Execution Baseline SHALL remain historically identifiable when
subsequent governed reassessment changes future realization.

## 13. Engineering Orchestration

Engineering Orchestration is the continuous governed realization process
through which the Execution Baseline is realized.

It is not a single linear workflow.

Orchestration coordinates, as applicable:

-   Slice readiness;
-   realization responsibility;
-   composition;
-   implementation;
-   technical validation;
-   Engineering Evidence;
-   acceptance obligations;
-   dependencies;
-   execution obligations;
-   execution learning;
-   materiality assessment;
-   adaptation;
-   reassessment;
-   Pause/Resume;
-   blocked progression;
-   Slice termination;
-   replacement or superseding realization;
-   Slice outcome roll-up; and
-   Engineering Delivery Record maintenance.

Orchestration SHALL permit non-linear realization while preserving
canonical Engineering semantics and governance.

Detailed realization semantics are defined by the Engineering
Orchestration specification.

## 14. Engineering Slice Lifecycle

The canonical Engineering Slice lifecycle is:

    Authorized
        ↓
    Realizing
       ↙  ↘

Complete Terminated

Authorized indicates that the Slice forms part of the governed Execution
Baseline.

Realizing indicates that governed realization of the Slice has begun.

Complete indicates that the Slice has satisfied the applicable
implementation, technical validation, Engineering Evidence, and any
additional governed completion prerequisites.

Terminated indicates that realization of the Slice has ended without
Slice completion and has received or requires an applicable governed
disposition.

Complete and Terminated are terminal Slice lifecycle states.

Pause, Resume, Blocked, readiness, validation, evidence, acceptance, and
reassessment SHALL NOT be introduced as additional Slice lifecycle
states merely because they affect realization.

## 15. Orthogonal Realization Conditions

Engineering Orchestration SHALL distinguish the Slice lifecycle from
orthogonal realization conditions.

These MAY include:

-   Slice Readiness;
-   Progression Condition;
-   Governance Condition;
-   Validation Condition;
-   Evidence Condition; and
-   Acceptance Condition.

For example, a Realizing Slice MAY be Paused or Blocked without leaving
the Realizing lifecycle state.

A Slice MAY resume realization when the applicable progression condition
permits it.

This separation prevents lifecycle-state proliferation and permits
human, AI, and mixed-team implementations to reason consistently about
realization.

## 16. Composition, Implementation, Validation, Evidence, and Acceptance

Composition, implementation, validation, evidence, and applicable
acceptance are realization concerns coordinated through Engineering
Orchestration.

They SHALL NOT be interpreted as a mandatory linear sequence.

Composition MAY occur before or during implementation.

Implementation MAY reveal new technical information.

Validation MAY occur incrementally throughout realization.

Engineering Evidence MAY accumulate continuously.

Acceptance applies only where the governing basis establishes an
applicable acceptance obligation.

The Engineering System SHALL preserve the distinction between:

-   implementation activity;
-   technical validation;
-   Engineering Evidence; and
-   acceptance.

None SHALL silently substitute for another.

## 17. Slice Completion

An Engineering Slice reaches Complete only when its applicable governed
completion basis is satisfied.

At minimum, completion requires:

-   authorized realization has been implemented;
-   applicable technical validation has succeeded;
-   sufficient Engineering Evidence supports the completion claim; and
-   any additional completion prerequisite established by the governing
    basis has been satisfied or received an applicable governed
    disposition.

Operational tool signals SHALL NOT independently establish Slice
completion.

## 18. Execution Learning and Materiality

Engineering realization SHALL be allowed to produce new technical
knowledge.

Execution learning MAY affect:

-   the Approved Investment Baseline;
-   Execution Baseline;
-   governed Epic intent;
-   realization scope;
-   architecture;
-   security or compliance obligations;
-   Engineering risk;
-   cost, effort, or timing;
-   dependencies;
-   execution obligations;
-   validation;
-   evidence;
-   acceptance; or
-   another governed Engineering commitment.

Materiality SHALL be determined by consequence to governed commitments
rather than by the mere existence of change.

Non-material adaptation MAY proceed within applicable authority and
tolerances.

Material change SHALL trigger applicable reassessment.

Where materiality is uncertain and the consequence could be material,
the matter SHALL be treated through the applicable governance path
rather than silently assumed to be non-material.

## 19. Governed Reassessment

Reassessment is the governed mechanism for determining how realization
proceeds when material execution learning, a Reassessment Trigger,
tolerance exceedance, or another material concern challenges the current
basis.

Reassessment MAY result in:

-   continuation on the existing basis;
-   authorized adaptation;
-   revised Engineering Delivery Plan;
-   new or revised Architecture Decision Record;
-   changed conditions or obligations;
-   changed Slice structure;
-   return to Delivery Planning;
-   upstream boundary escalation;
-   Slice termination;
-   replacement realization; or
-   another governed disposition.

Reassessment SHALL preserve:

-   the historical basis;
-   the trigger or material concern;
-   applicable authority or decision;
-   resulting disposition; and
-   revised governed basis where applicable.

Governed reassessment SHALL NOT rewrite history.

## 20. Slice Termination and Replacement Realization

A Slice MAY reach Terminated where governed realization ends without
satisfying Slice completion.

Termination SHALL preserve, as applicable:

-   Slice identity;
-   reason;
-   authority or decision;
-   realization already performed;
-   evidence already produced;
-   remaining obligations;
-   dependency consequences;
-   Epic consequences;
-   Execution Baseline consequences; and
-   resulting disposition.

Where realization is replaced or superseded, the replacement SHALL
receive its own governed identity.

Replacement realization SHALL NOT overwrite the terminated Slice.

A Terminated Slice does not automatically prevent Epic Engineering
Completion where the required realization is governably replaced,
superseded, or rendered no longer applicable and no required Epic
outcome remains materially unaccounted for.

## 21. Architecture Decisions

Architecture decisions MAY arise during proposal development, planning,
or realization.

Material architecture decisions SHALL be governed according to the
Architecture Decision specification.

An Architecture Decision Record SHALL preserve the applicable decision
context and history without requiring the lifecycle to stop merely
because architectural understanding evolves.

Where execution learning materially changes architecture, the applicable
reassessment and architecture governance SHALL be invoked.

Architecture governance SHALL remain continuous rather than confined to
a single lifecycle stage.

## 22. Engineering Evidence

Engineering Evidence supports specific Engineering claims.

Evidence MAY arise throughout planning and realization and MAY include
authoritative information from source control, CI/CD, testing,
validation, security, performance, migration, deployment, operational
systems, reviews, or other governed sources.

Engineering Evidence SHALL be:

-   attributable;
-   traceable to the claim it supports;
-   sufficiently trustworthy for the applicable decision;
-   durable enough for required governance; and
-   proportionate to Engineering significance.

The Engineering Delivery Record SHALL reference authoritative
Engineering Evidence where duplication is unnecessary.

Evidence SHALL NOT be confused with the EDR itself.

## 23. Engineering Delivery Record

An Engineering Delivery Record SHALL be instantiated when Engineering
Orchestration begins.

One governed Engineering realization SHALL maintain one stable EDR
identity through progressive maintenance and finalization.

The EDR has two Record States:

-   Active; or
-   Finalized.

While Active, the EDR progressively preserves material realization
information, including as applicable:

-   governing Engineering basis;
-   Slice outcomes;
-   terminated and replacement realization;
-   material execution learning;
-   governed adaptation;
-   reassessment outcomes;
-   material obligation dispositions;
-   architecture decisions;
-   validation outcomes;
-   applicable acceptance outcomes;
-   Engineering Evidence references;
-   approved exceptions; and
-   residual conditions.

The EDR answers:

> What did Engineering actually realize, how did governed realization
> change where material, and what Engineering conclusion was
> established?

The EDR SHALL be finalized when the governed Engineering realization
reaches its applicable conclusion and the finalization requirements are
satisfied.

Detailed EDR semantics are defined by the Engineering Delivery Record
specification.

## 24. Slice Outcome Roll-up

Engineering Slice outcomes SHALL roll up toward the governing Epic.

A Complete Slice contributes satisfied Engineering realization.

A Terminated Slice contributes its governed disposition and any
applicable replacement, supersession, exception, or residual
consequence.

Epic-level outcome SHALL be determined from the governed realization as
a whole rather than from a simple count of Complete Slices.

No required Epic Engineering realization may remain materially
unaccounted for in a successful Epic Engineering Completion claim.

## 25. Epic Engineering Completion

Epic Engineering Completion is the successful Engineering conclusion.

It establishes that the Engineering realization required for the
governing Engineering-ready Epic has been implemented and technically
validated to the extent required by its governed Engineering basis.

Epic Engineering Completion SHOULD consider, as applicable:

-   required Engineering Slice outcomes;
-   integrated technical behavior;
-   cross-Slice dependencies;
-   aggregate technical validation;
-   Engineering Evidence;
-   architecture conformance;
-   approved exceptions;
-   security obligations;
-   performance obligations;
-   reliability obligations;
-   operational technical obligations;
-   unresolved governed issues; and
-   dispositions of terminated or superseded realization.

Epic Engineering Completion SHALL NOT by itself establish:

-   Product acceptance;
-   Release Admission;
-   Release Readiness;
-   Production deployment authority;
-   commercial launch authority; or
-   another authority outside the Engineering System.

Epic Engineering Completion is an Engineering outcome, not a Release
outcome.

## 26. Non-Completion Engineering Conclusion

Not every governed Engineering realization is required to conclude with
Epic Engineering Completion.

Where governed realization concludes without Epic Engineering
Completion, the canonical outcome SHALL be a Non-Completion Engineering
Conclusion.

A Non-Completion Engineering Conclusion SHALL preserve or reference:

-   the specific governed reason;
-   applicable authority or decision;
-   resulting disposition; and
-   sufficient traceability to explain why Epic Engineering Completion
    was not established.

The specific reason SHALL NOT become a separate canonical Engineering
conclusion state merely because it explains the Non-Completion
Engineering Conclusion.

A Non-Completion Engineering Conclusion SHALL NOT be represented as
successful Epic Engineering Completion.

## 27. Engineering Conclusion

A governed Engineering realization SHALL conclude with exactly one
canonical Engineering conclusion:

    Engineering Conclusion
        ├── Epic Engineering Completion
        └── Non-Completion Engineering Conclusion

The conclusion SHALL remain distinct from Product, Collaboration,
Release, deployment, operational, or commercial decisions outside
Engineering authority.

The Engineering Delivery Record SHALL preserve the resulting conclusion
and its supporting governed basis.

## 28. Engineering System Exit and Release Boundary

Establishment of the Engineering conclusion and finalization of the
Engineering Delivery Record are distinct lifecycle events.

The Engineering conclusion establishes the governed Engineering outcome.

EDR finalization establishes the concluded historical Engineering record
that preserves that outcome and its supporting governed basis.

The Engineering System lifecycle concludes only when:

-   the governed Engineering realization has reached its applicable
    Engineering conclusion;
-   the Engineering Delivery Record sufficiently preserves that
    conclusion and its basis; and
-   the EDR is Finalized according to applicable Engineering governance.

The lifecycle sequence is therefore:

    Engineering realization
            ↓
    Engineering Conclusion established
            ↓
    EDR preserves conclusion and satisfies finalization requirements
            ↓
    Engineering Delivery Record → Finalized
            ↓
    Engineering System lifecycle concluded

A Finalized EDR MAY provide the Engineering basis for an applicable
downstream cross-system Release Admission decision.

Engineering conclusion SHALL NOT itself establish Release Admission or
any downstream Release authority.

The downstream dependency is therefore:

    Finalized Engineering Delivery Record
                ↓
       may provide Engineering basis
                ↓
       cross-system Release Admission
                ↓
            Release System

A downstream Release process or record MAY reference the Finalized EDR.

The EDR does not require a reverse reference to a subsequently
established Release Admission decision.

## 29. Governed Decision Semantics

Engineering lifecycle decisions SHALL use the canonical outcomes defined
by the applicable process and governance specification.

Decision vocabularies SHALL NOT be generalized across distinct decision
gates where doing so would erase their specific semantics.

For example:

-   Investment Decision semantics are governed by the Engineering
    Delivery Proposal and Engineering Governance specifications;
-   Execution Readiness Decision semantics are governed by the
    Engineering Delivery Planning and Engineering Governance
    specifications; and
-   reassessment decisions are governed by Engineering Orchestration and
    applicable Engineering Governance.

Each governed decision SHOULD preserve, as applicable:

-   decision identity;
-   outcome;
-   authority;
-   rationale;
-   date;
-   affected artifact or realization;
-   conditions;
-   resulting disposition; and
-   required return or reconsideration path.

A governed decision SHALL NOT destroy or erase the artifact, baseline,
or decision history that preceded it.

## 30. Human, AI, and Mixed-team Operation

The Engineering Lifecycle MAY be operated by:

-   human Engineering teams;
-   AI agents;
-   automated Engineering systems;
-   mixed human and AI teams; or
-   other authorized actors.

Actor type SHALL NOT change canonical Engineering semantics.

AI systems MAY assist with analysis, planning, decomposition,
implementation, validation, evidence collection, orchestration, record
maintenance, traceability, and conformance checking according to
applicable authority.

AI systems SHALL NOT infer authority merely from technical capability.

An actor authorized to perform Engineering work SHALL NOT automatically
be treated as authorized to make every governed decision associated with
that work.

## 31. External Tool Representation

Engineering lifecycle concepts MAY be projected into external systems,
including:

-   project-management tools;
-   issue trackers;
-   source-control systems;
-   CI/CD platforms;
-   test systems;
-   infrastructure systems;
-   AI-agent platforms; and
-   delivery-management systems.

External representations MAY use tool-native objects such as Epics,
stories, tasks, tickets, jobs, workflows, milestones, or statuses.

The Engineering System SHALL retain authoritative Engineering identity,
intent, relationships, and governance.

Tool-native state SHALL NOT silently redefine:

-   Engineering Slice lifecycle;
-   Record State;
-   Engineering conclusion;
-   decision authority; or
-   another canonical Engineering semantic.

## 32. Traceability

The Engineering Lifecycle SHALL preserve sufficient traceability across
the governed delivery chain.

Lifecycle progression passes through Engineering Delivery Planning
between the Approved Investment Baseline and Engineering Delivery Plan.

Engineering Delivery Planning is a lifecycle process, not a separately
persisted governed artifact merely by virtue of being part of the
lifecycle. Artifact-level traceability SHALL preserve the relationship
between the Approved Investment Baseline and the resulting Engineering
Delivery Plan without requiring Engineering Delivery Planning itself to
exist as a separately persisted governed artifact.

At minimum, it SHOULD be possible to trace, as applicable:

    Engineering-ready Epic
            ↓
    Engineering Delivery Proposal
            ↓
    Investment Decision
            ↓
    Approved Investment Baseline
            ↓
    Engineering Delivery Plan
            ↓
    Execution Readiness Decision
            ↓
    Execution Baseline
            ↓
    Engineering Slice
            ↓
    realization outcome
            ↓
    Engineering Evidence
            ↓
    Engineering Conclusion
            ↓
    Finalized Engineering Delivery Record

Where material change occurs, traceability SHOULD additionally support:

    original governed basis
            ↓
    material learning / trigger
            ↓
    reassessment / decision
            ↓
    revised governed basis
            ↓
    resulting realization

Traceability SHOULD rely on stable governed identities and relationships
rather than filenames, directory locations, or external tool conventions
alone.

## 33. Proportional Application

The Engineering Lifecycle SHALL be applied proportionately to
Engineering significance.

A small, familiar, low-risk realization MAY use:

-   concise proposal analysis;
-   a small Delivery Plan;
-   one or few Engineering Slices;
-   lightweight evidence;
-   simple orchestration; and
-   a concise EDR.

A large, uncertain, architecturally significant, security-sensitive,
operationally sensitive, or dependency-heavy realization MAY require:

-   deeper proposal discovery;
-   richer planning;
-   more explicit architecture governance;
-   multiple Slices;
-   stronger validation and evidence;
-   substantial reassessment history;
-   explicit exception and residual-condition treatment; and
-   a richer EDR.

Proportionality SHALL reduce unnecessary ceremony without removing
governance necessary for a defensible Engineering outcome.

## 34. Lifecycle Summary

The canonical Engineering Lifecycle is:

    Engineering-ready Epic
            ↓
    Engineering Delivery Proposal
            ↓
    Investment Decision
            ↓
         Approve
            ↓
    Approved Investment Baseline
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
            ↓
    Engineering Slice realization
      ├── Complete
      ├── Terminated
      ├── Pause / Resume
      ├── Blocked progression
      ├── material learning
      ├── governed adaptation
      ├── reassessment
      └── replacement realization
            ↓
    Slice outcome roll-up
            ↓
    Engineering Conclusion
       ├── Epic Engineering Completion
       └── Non-Completion Engineering Conclusion
            ↓
    Engineering Delivery Record finalized
            ↓
    ─────────────────────────────
       Engineering System boundary
    ─────────────────────────────
            ↓
    possible cross-system
       Release Admission

The lifecycle is governed but adaptive.

Proposal governs the investment question.

Planning governs the execution basis.

The Execution Baseline authorizes realization.

Engineering Orchestration governs non-linear realization.

Engineering Slices provide the canonical units of realization.

Engineering Evidence supports Engineering claims.

The Engineering Delivery Record progressively preserves what actually
occurred and is finalized at the governed Engineering conclusion.

The resulting Finalized EDR concludes the Engineering lifecycle and may
provide the Engineering basis for downstream Release governance without
itself granting Release authority.
