# Engineering Artifact Model Specification

## 1. Purpose

This specification defines the canonical model for governed Engineering
information within the Engineering System.

It establishes:

-   the categories of governed Engineering objects;
-   the distinction between processes, artifacts, records, baselines,
    realization units, evidence, decisions, conditions, and outcomes;
-   canonical identities and relationships between those objects;
-   ownership and authority semantics;
-   traceability requirements;
-   lifecycle and historical-integrity expectations;
-   representation rules for human, AI, automated, and mixed-team
    operation; and
-   boundaries between canonical Engineering semantics and external tool
    representations.

The Artifact Model exists so that Engineering information can be
interpreted consistently regardless of whether it is represented in
Markdown, a database, an issue tracker, an AI-agent runtime, a
source-control system, a CI/CD platform, or another Engineering tool.

This specification SHALL NOT require every canonical concept to exist as
a standalone file.

A governed Engineering object MAY be represented as a document,
structured record, database entity, linked external record,
machine-native object, or another durable representation provided its
canonical semantics remain preserved.

## 2. Model Principle

The Engineering System contains multiple kinds of governed things.

They SHALL NOT all be treated as interchangeable "artifacts."

The canonical model distinguishes at least:

-   Engineering processes;
-   governed Engineering artifacts;
-   governed Engineering records;
-   governed baselines;
-   governed realization units;
-   Engineering Evidence;
-   governed decisions;
-   realization conditions;
-   Engineering outcomes; and
-   operational representations.

These categories describe semantic roles.

Canonical categories identify the primary semantic role of a governed
Engineering object.

A governed Engineering object MAY participate in relationships
associated with other semantic roles without changing its primary
classification.

For example:

-   an Architecture Decision Record is a Governed Record that preserves
    a material architecture decision; it does not therefore become a
    Governed Decision;
-   an Engineering Slice is a Governed Realization Unit that may reach
    an Engineering Outcome; it does not therefore become an Engineering
    Outcome object itself; and
-   a governed baseline is established by a Governed Decision without
    therefore becoming that decision.

Semantic roles are therefore compositional through governed
relationships, not through uncontrolled category collapse.

A concrete implementation MAY persist several categories within one
physical system or representation without collapsing their canonical
meaning.

## 3. Canonical Engineering Object Model

The Engineering System MAY be understood through the following semantic
model:

    Engineering System
    │
    ├── Processes
    │   ├── Engineering Delivery Proposal development
    │   ├── Engineering Delivery Planning
    │   └── Engineering Orchestration
    │
    ├── Governed Artifacts
    │   ├── Engineering Delivery Proposal
    │   └── Engineering Delivery Plan
    │
    ├── Governed Records
    │   ├── Architecture Decision Record
    │   └── Engineering Delivery Record
    │
    ├── Governed Baselines
    │   ├── Approved Investment Baseline
    │   └── Execution Baseline
    │
    ├── Governed Realization Units
    │   └── Engineering Slice
    │
    ├── Governed Decisions
    │   ├── Investment Decision
    │   ├── Execution Readiness Decision
    │   └── applicable reassessment decisions
    │
    ├── Engineering Evidence
    │   └── authoritative evidence supporting Engineering claims
    │
    ├── Realization Conditions
    │   ├── Slice Readiness
    │   ├── Progression Condition
    │   ├── Governance Condition
    │   ├── Validation Condition
    │   ├── Evidence Condition
    │   └── Acceptance Condition
    │
    └── Engineering Outcomes
        ├── Slice Complete
        ├── Slice Terminated
        ├── Epic Engineering Completion
        └── Non-Completion Engineering Conclusion

This model is semantic rather than storage-prescriptive.

The categories SHALL be interpreted according to the definitions in this
specification and the applicable detailed Engineering System
specifications.

## 4. Engineering Processes

An Engineering process is governed activity that transforms, evaluates,
coordinates, or maintains Engineering information and realization.

A process is not a governed artifact merely because it appears in the
Engineering lifecycle.

Canonical Engineering processes include:

-   Engineering Delivery Proposal development;
-   Engineering Delivery Planning; and
-   Engineering Orchestration.

Processes MAY produce, revise, evaluate, or maintain governed
Engineering objects.

For example:

    Engineering Delivery Planning
            ↓ produces
    Engineering Delivery Plan

and:

    Engineering Orchestration
            ↓ progressively maintains
    Engineering Delivery Record

A process MAY have operational execution state without requiring a
separately persisted canonical process artifact.

## 5. Governed Engineering Artifacts

A governed Engineering artifact is an intentionally authored Engineering
representation that defines or proposes a governed basis for Engineering
decision or execution.

Canonical governed Engineering artifacts are:

-   Engineering Delivery Proposal; and
-   Engineering Delivery Plan.

A governed artifact:

-   SHALL have stable identity;
-   SHALL preserve applicable revision history;
-   SHALL remain traceable to its governing inputs;
-   MAY evolve before or through applicable governance;
-   SHALL preserve material historical versions where required for
    governed decisions; and
-   SHALL NOT silently acquire authority merely because it has been
    authored.

Artifacts become authoritative for a particular purpose only through the
applicable governed decision or baseline semantics.

## 6. Engineering Delivery Proposal

The Engineering Delivery Proposal is the governed artifact used to
establish the proposed Engineering investment and realization basis for
an Engineering-ready Epic.

It supports the Investment Decision.

The Proposal MAY evolve through analysis, discovery, clarification,
Return, or revision before a final applicable Investment Decision.

An approved Proposal remains historically identifiable as part of the
Approved Investment Baseline.

The Proposal SHALL NOT be treated as:

-   the Engineering Delivery Plan;
-   the Execution Baseline;
-   the Engineering Delivery Record; or
-   proof that Engineering execution has been authorized.

## 7. Engineering Delivery Plan

The Engineering Delivery Plan is the governed artifact that defines the
proposed execution basis for realizing an Approved Investment Baseline.

It is produced through Engineering Delivery Planning and supports the
Execution Readiness Decision.

The Plan MAY evolve before authorization and MAY subsequently be revised
through applicable reassessment and governance.

The authorized Plan revision forms a principal part of the Execution
Baseline.

The Plan SHALL NOT be treated as:

-   Engineering Delivery Planning itself;
-   execution authorization merely because it is complete;
-   the Execution Baseline in its entirety;
-   actual Engineering realization; or
-   the Engineering Delivery Record.

## 8. Governed Engineering Records

A governed Engineering record preserves the durable historical
representation of a governed Engineering fact, decision rationale,
realization history, or other information whose historical integrity is
significant.

A governed decision and the record or representation that preserves
information about that decision are distinct semantic concepts.

A governed decision establishes an authoritative determination.

A governed record preserves governed historical information.

A persisted representation of an Investment Decision, Execution
Readiness Decision, or reassessment decision SHALL NOT therefore cause
that decision to be reclassified as a Governed Record unless the
Engineering System explicitly defines a separate canonical record type
for that purpose.

Canonical governed Engineering records include:

-   Architecture Decision Record; and
-   Engineering Delivery Record.

A governed record:

-   SHALL have stable identity;
-   SHALL preserve historical integrity;
-   SHALL identify or reference its governing basis;
-   SHALL remain traceable to applicable authority and evidence;
-   SHALL not silently rewrite historical fact; and
-   MAY permit governed correction without erasing prior history.

Records preserve governed historical information about what was decided,
why it was decided, or what occurred, according to the applicable record
semantics.

They SHALL NOT be treated as prospective plans merely because they
influence future Engineering activity.

## 9. Architecture Decision Record

An Architecture Decision Record is the governed Engineering record of a
material architecture decision.

An ADR is cross-cutting and MAY arise during:

-   Engineering Delivery Proposal development;
-   Engineering Delivery Planning;
-   Engineering Orchestration; or
-   another applicable Engineering governance activity.

An ADR SHALL NOT be treated as a mandatory lifecycle stage or mandatory
per-Epic, per-Plan, or per-Slice artifact.

An ADR SHOULD be created where a material architecture decision requires
durable governance and reasoning history.

An ADR MAY:

-   inform an Engineering Delivery Proposal;
-   become part of an Approved Investment Baseline;
-   inform or constrain an Engineering Delivery Plan;
-   become part of the architecture basis represented by the Execution
    Baseline;
-   arise from material execution learning;
-   result from governed reassessment;
-   influence one or more Engineering Slices;
-   be referenced by the Engineering Delivery Record; and
-   remain authoritative across multiple Engineering realizations until
    superseded or otherwise dispositioned.

The ADR preserves the architecture decision.

The Engineering Delivery Record preserves the material delivery
consequence of that decision where applicable.

These responsibilities SHALL remain distinct.

## 10. Engineering Delivery Record

The Engineering Delivery Record is the governed record of actual
Engineering realization and its resulting Engineering conclusion.

The EDR is instantiated when Engineering Orchestration begins and
maintains one stable identity for one governed Engineering realization
through progressive maintenance and finalization.

The EDR has Record State:

-   Active; or
-   Finalized.

The EDR MAY preserve or reference:

-   governing Engineering basis;
-   Slice outcomes;
-   terminated realization;
-   replacement or superseding realization;
-   material execution learning;
-   governed adaptations;
-   reassessment outcomes;
-   material execution obligation dispositions;
-   architecture decisions;
-   technical validation outcomes;
-   applicable acceptance outcomes;
-   Engineering Evidence;
-   approved exceptions;
-   residual conditions; and
-   the Engineering conclusion.

The EDR SHALL NOT replace:

-   the Engineering Delivery Proposal;
-   the Engineering Delivery Plan;
-   the Execution Baseline;
-   Architecture Decision Records;
-   authoritative Engineering Evidence; or
-   downstream Release records.

A Finalized EDR is the concluded governed historical record of the
applicable Engineering realization.

## 11. Governed Baselines

A governed baseline is an authoritative snapshot of a governed basis
established by an applicable decision.

Canonical Engineering baselines are:

-   Approved Investment Baseline; and
-   Execution Baseline.

A baseline:

-   SHALL identify the decision that established it;
-   SHALL preserve the governed basis applicable at that point;
-   SHALL remain historically identifiable after subsequent change;
-   SHALL NOT be silently rewritten by later realization;
-   MAY reference multiple governed objects rather than duplicate them;
    and
-   MAY be represented as a logical governed set rather than a
    standalone document.

A baseline is therefore not necessarily a file.

Its canonical meaning is the authoritative governed basis established at
a decision boundary.

## 12. Approved Investment Baseline

The Approved Investment Baseline is established by an Approve Investment
Decision.

It preserves the Engineering investment basis authorized for Engineering
Delivery Planning.

It MAY consist of or reference:

-   the Engineering-ready Epic;
-   approved Engineering Delivery Proposal revision;
-   Investment Decision;
-   approved realization framing;
-   approved assumptions and conditions;
-   approved investment basis;
-   material dependencies and constraints;
-   material Engineering risks;
-   accepted uncertainty; and
-   other governed investment information.

The Approved Investment Baseline SHALL remain distinguishable from the
Proposal artifact itself.

The Proposal is authored Engineering analysis.

The Approved Investment Baseline is the governed investment basis
established by decision.

## 13. Execution Baseline

The Execution Baseline is established by an Authorize Execution
Readiness Decision.

It defines what Engineering is authorized to realize.

It MAY consist of or reference:

-   authorized Engineering Delivery Plan revision;
-   Execution Readiness Decision;
-   Approved Investment Baseline;
-   Engineering Slice structure;
-   architecture basis;
-   implementation obligations;
-   validation obligations;
-   Engineering Evidence obligations;
-   applicable acceptance obligations;
-   dependencies;
-   Authorization Conditions;
-   Delivery Tolerances;
-   Reassessment Triggers; and
-   other governed execution commitments.

The Execution Baseline SHALL remain distinguishable from the Engineering
Delivery Plan.

The Plan proposes the execution basis.

The Execution Baseline is the governed execution basis established by
authorization.

## 14. Governed Realization Units

A governed realization unit is a canonical bounded unit through which
authorized Engineering realization is performed and governed.

The canonical governed realization unit is the Engineering Slice.

A realization unit is neither merely a planning artifact nor merely an
operational task.

It carries governed Engineering identity and lifecycle semantics through
realization.

## 15. Engineering Slice

An Engineering Slice is the canonical governed unit of Engineering
realization.

A Slice SHALL:

-   have stable identity;
-   remain traceable to the governing Engineering Delivery Plan and
    Execution Baseline;
-   preserve applicable realization responsibility;
-   preserve applicable obligations and dependencies;
-   expose canonical lifecycle state;
-   remain traceable to validation and Engineering Evidence; and
-   preserve its terminal outcome.

The canonical Slice lifecycle is:

    Authorized
        ↓
    Realizing
       ↙  ↘

Complete Terminated

Complete and Terminated are terminal lifecycle states.

A Slice MAY have orthogonal readiness, progression, governance,
validation, evidence, and acceptance conditions without introducing
those concepts as additional lifecycle states.

A Slice MAY be decomposed operationally into tasks, stories, work items,
subtasks, agent jobs, or other tool-native units.

Such operational decomposition SHALL NOT create additional canonical
governed Engineering realization units unless explicitly established by
Engineering governance.

## 16. No Canonical Engineering Work Item Layer

The Engineering System SHALL NOT require a separate canonical
Engineering Work Item layer between Engineering Slice and operational
execution.

Teams MAY use any useful operational decomposition beneath a Slice.

For example:

    Engineering Slice
       ├── task
       ├── story
       ├── issue
       ├── subtask
       ├── agent job
       └── implementation step

These objects MAY be important operationally.

They do not automatically acquire canonical Engineering identity,
lifecycle, acceptance, or governance semantics.

This separation permits Engineering teams and AI-agent systems to choose
realization granularity without expanding the canonical Engineering
governance model.

## 17. Governed Decisions

A governed Engineering decision is an authoritative determination made
through an applicable Engineering governance boundary.

Canonical governed decision types include:

-   Investment Decision;
-   Execution Readiness Decision; and
-   applicable reassessment decisions.

A governed decision SHALL preserve or reference, as applicable:

-   decision identity;
-   decision type;
-   outcome;
-   authority;
-   rationale;
-   date or effective point;
-   affected governed object or realization;
-   conditions;
-   resulting disposition; and
-   required return, reconsideration, or escalation path.

A decision MAY establish a baseline.

A decision SHALL NOT be conflated with the artifact or baseline upon
which it acts.

## 18. Investment Decision

The Investment Decision acts upon an Engineering Delivery Proposal.

Canonical outcomes are:

-   Approve;
-   Return;
-   Defer; or
-   Reject.

Approve establishes the Approved Investment Baseline and authorizes
Engineering Delivery Planning.

The decision SHALL remain historically identifiable independently of
later Proposal, Plan, or realization changes.

## 19. Execution Readiness Decision

The Execution Readiness Decision acts upon an Engineering Delivery Plan
and its applicable governed basis.

An Authorize outcome establishes the Execution Baseline and permits
Engineering Orchestration to begin.

The Execution Readiness Decision SHALL remain distinguishable from:

-   a readiness recommendation;
-   the Engineering Delivery Plan;
-   the Execution Baseline; and
-   actual execution.

Canonical outcome semantics are defined by the applicable Delivery
Planning and Engineering Governance specifications.

## 20. Reassessment Decisions

A reassessment decision determines how governed Engineering realization
proceeds when material execution learning, tolerance exceedance, a
Reassessment Trigger, or another material concern challenges the current
basis.

A reassessment decision MAY result in:

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

Reassessment SHALL preserve the relationship between:

    original governed basis
            ↓
    material learning / trigger
            ↓
    reassessment decision
            ↓
    resulting governed basis
            ↓
    resulting realization

A reassessment decision SHALL NOT erase the prior governed basis.

## 21. Engineering Evidence

Engineering Evidence is traceable information supporting a specific
Engineering claim.

Engineering Evidence MAY originate from:

-   source control;
-   build systems;
-   CI/CD;
-   automated tests;
-   manual technical validation;
-   security validation;
-   performance validation;
-   reliability validation;
-   compatibility validation;
-   migration validation;
-   deployment validation;
-   operational systems;
-   reviews;
-   generated artifacts; or
-   other governed Engineering sources.

Engineering Evidence SHALL be:

-   attributable;
-   traceable to the claim it supports;
-   sufficiently trustworthy;
-   sufficiently durable;
-   accessible according to applicable governance; and
-   proportionate to Engineering significance.

Engineering Evidence MAY remain in its authoritative source.

The Engineering System SHOULD reference evidence rather than duplicate
it where stable authoritative references are sufficient.

Engineering Evidence SHALL NOT be treated as:

-   an Engineering Delivery Record;
-   an Architecture Decision Record;
-   a decision;
-   a baseline; or
-   an Engineering outcome merely because it supports one.

## 22. Realization Conditions

A realization condition describes an orthogonal condition affecting
governed realization without redefining the Engineering Slice lifecycle.

Canonical condition dimensions MAY include:

-   Slice Readiness;
-   Progression Condition;
-   Governance Condition;
-   Validation Condition;
-   Evidence Condition; and
-   Acceptance Condition.

For example, a Slice may simultaneously be:

    Lifecycle State: Realizing
    Progression Condition: Paused
    Validation Condition: Pending
    Evidence Condition: Incomplete

These conditions SHALL remain semantically distinct from the Slice
lifecycle.

Pause, Resume, Blocked, validation status, evidence status, acceptance
status, or reassessment SHALL NOT become additional canonical Slice
lifecycle states merely because an implementation tool represents them
as statuses.

## 23. Engineering Outcomes

An Engineering outcome is a governed result established through
Engineering realization or conclusion.

Canonical Engineering outcomes include:

-   Slice Complete;
-   Slice Terminated;
-   Epic Engineering Completion; and
-   Non-Completion Engineering Conclusion.

An outcome is not necessarily a separately persisted artifact.

It MAY be represented through the governed realization unit, EDR,
decision record, or another authoritative representation.

The representation SHALL preserve the canonical outcome semantics.

## 24. Slice Complete

Slice Complete is a terminal Engineering Slice lifecycle outcome.

It establishes that the Slice has satisfied its applicable governed
completion basis.

At minimum:

-   authorized realization has been implemented;
-   applicable technical validation has succeeded;
-   sufficient Engineering Evidence supports the completion claim; and
-   any additional governed completion prerequisite has been satisfied
    or received an applicable governed disposition.

Slice Complete SHALL NOT be inferred solely from operational tool state.

## 25. Slice Terminated

Slice Terminated is a terminal Engineering Slice lifecycle outcome.

It establishes that governed realization of the Slice ended without
Slice completion.

Termination SHALL preserve or reference, as applicable:

-   reason;
-   authority or decision;
-   realization performed;
-   evidence produced;
-   remaining obligations;
-   dependency consequences;
-   Epic consequences;
-   Execution Baseline consequences;
-   replacement or superseding realization; and
-   resulting disposition.

Termination SHALL remain historically visible.

## 26. Engineering Conclusion

A governed Engineering realization SHALL conclude with exactly one
canonical Engineering conclusion:

-   Epic Engineering Completion; or
-   Non-Completion Engineering Conclusion.

The Engineering conclusion is an Engineering outcome.

It SHALL remain distinct from:

-   Product acceptance;
-   Release Admission;
-   Release Readiness;
-   deployment authority;
-   Production promotion authority; and
-   commercial launch authority.

The Engineering Delivery Record SHALL preserve the conclusion and its
supporting governed basis.

## 27. Epic Engineering Completion

Epic Engineering Completion is the successful Engineering conclusion.

It establishes that required Engineering realization has been
implemented and technically validated to the extent required by the
governed Engineering basis.

Epic Engineering Completion SHALL account for the governed realization
as a whole rather than being inferred from a simple count of Complete
Slices.

Required Engineering realization SHALL NOT remain materially unaccounted
for.

## 28. Non-Completion Engineering Conclusion

A Non-Completion Engineering Conclusion is the canonical Engineering
conclusion where governed Engineering realization concludes without Epic
Engineering Completion.

It SHALL preserve or reference:

-   the specific governed reason;
-   applicable authority or decision;
-   resulting disposition; and
-   sufficient traceability explaining why Epic Engineering Completion
    was not established.

Reason-specific outcomes SHALL NOT become additional canonical
Engineering conclusion states merely because they explain
non-completion.

## 29. Relationship Between Decision, Artifact, Baseline, Realization, Record, and Outcome

The Engineering System SHALL preserve the following distinctions:

    Engineering Delivery Proposal
        = authored proposal artifact

    Investment Decision
        = governed decision acting on proposal

    Approved Investment Baseline
        = investment basis established by decision

    Engineering Delivery Planning
        = lifecycle process

    Engineering Delivery Plan
        = authored execution artifact

    Execution Readiness Decision
        = governed decision acting on execution basis

    Execution Baseline
        = execution basis established by authorization

    Engineering Orchestration
        = continuous governed realization process

    Engineering Slice
        = governed realization unit

    Engineering Evidence
        = authoritative support for Engineering claims

    Architecture Decision Record
        = governed record of a material architecture decision

    Engineering Conclusion
        = governed Engineering outcome

    Engineering Delivery Record
        = governed historical record of actual realization and conclusion

These semantic distinctions SHALL remain preserved even where several
objects are stored in the same system or rendered together in one
interface.

## 30. Canonical Relationship Chain

The primary governed relationship chain is:

    Engineering-ready Epic
            ↓ governs
    Engineering Delivery Proposal
            ↓ evaluated by
    Investment Decision
            ↓ establishes
    Approved Investment Baseline
            ↓ refined through
    Engineering Delivery Planning
            ↓ produces
    Engineering Delivery Plan
            ↓ evaluated by
    Execution Readiness Decision
            ↓ establishes
    Execution Baseline
            ↓ authorizes
    Engineering Orchestration
            ↓ realizes through
    Engineering Slice(s)
            ↓ outcomes contribute to
    Engineering Conclusion
            ↓ preserved by
    Finalized Engineering Delivery Record

Engineering Evidence is orthogonal to this progression.

It MAY support claims throughout governed Engineering realization,
including:

    Engineering Evidence
        ├── supports Slice realization and completion claims
        ├── supports technical validation claims
        ├── supports architecture or conformance claims
        ├── supports reassessment and disposition where applicable
        └── supports the Engineering Conclusion

Engineering Evidence SHALL NOT be interpreted as an intermediate
lifecycle stage between Engineering Slice realization and Engineering
Conclusion.

Architecture Decision Records MAY intersect the primary relationship
chain wherever material architecture decisions arise.

Reassessment decisions MAY alter future realization while preserving
prior governed history.

## 31. Identity

Canonical governed Engineering objects requiring independent
traceability SHALL have stable identities.

Stable identity SHOULD apply, as appropriate, to:

-   Engineering Delivery Proposal;
-   Engineering Delivery Plan;
-   Engineering Slice;
-   Architecture Decision Record;
-   Engineering Delivery Record;
-   Investment Decision;
-   Execution Readiness Decision;
-   material reassessment decisions; and
-   other governed objects where independent historical reference is
    necessary.

Baselines SHALL have sufficient identity or referenceability to
reconstruct the governed basis they represent.

Identity SHALL NOT depend solely on:

-   filename;
-   directory path;
-   issue number in a replaceable operational tool;
-   transient agent execution ID; or
-   mutable display name.

External identifiers MAY participate in canonical identity where their
governance and durability are sufficient.

## 32. Revision and Historical Integrity

Governed Engineering objects MAY evolve according to their semantic
role.

Artifacts MAY be revised.

Records MAY be progressively maintained or corrected according to
applicable record semantics.

Baselines MAY be superseded by later governed bases without rewriting
the historical baseline.

Slices MAY progress through their canonical lifecycle.

Decisions SHALL preserve their historical outcome and authority.

ADRs MAY be superseded according to Architecture Decision governance.

The EDR MAY progress from Active to Finalized.

Historical Engineering information SHALL NOT be silently rewritten
merely to make current realization appear consistent with an earlier
basis.

## 33. Authority

Authorship, maintenance, execution, and decision authority are distinct.

An actor MAY be authorized to:

-   author an artifact;
-   maintain a record;
-   realize a Slice;
-   collect evidence;
-   perform validation;
-   make a governed decision; or
-   establish an Engineering conclusion.

Authorization for one activity SHALL NOT imply authorization for all
others.

AI capability SHALL NOT imply governance authority.

A tool's ability to mutate a stored object SHALL NOT by itself establish
authority to change the governed Engineering meaning of that object.

## 34. Ownership and Maintenance

Each governed Engineering object SHALL have sufficient responsibility
for maintenance appropriate to its semantic role.

Responsibility MAY be assigned to:

-   an individual;
-   an Engineering team;
-   an architecture authority;
-   an authorized AI agent;
-   an automated Engineering system;
-   a mixed human/AI team; or
-   another governed actor.

Changing the maintaining actor SHALL NOT by itself change:

-   canonical object identity;
-   governing basis;
-   historical meaning;
-   applicable authority; or
-   evidence requirements.

## 35. Traceability

The Artifact Model SHALL support traceability sufficient to reconstruct
the governed Engineering path.

At minimum, it SHOULD be possible to determine, as applicable:

-   what Engineering intent entered the system;
-   what investment was proposed;
-   what Investment Decision was made;
-   what investment basis was approved;
-   what execution basis was planned;
-   what execution basis was authorized;
-   what Engineering Slices were realized;
-   what material architecture decisions applied;
-   what material changes occurred;
-   how those changes were governed;
-   what evidence supports material Engineering claims;
-   what Engineering outcome was established; and
-   what Finalized EDR preserves that realization.

Traceability SHALL preserve relationships between canonical identities
rather than rely solely on physical document hierarchy.

## 36. Cross-object References

Canonical governed objects SHOULD reference other governed objects by
stable identity where the relationship is material.

References MAY include:

-   governing input;
-   derived-from;
-   decision-on;
-   establishes-baseline;
-   authorized-by;
-   part-of;
-   realizes;
-   depends-on;
-   constrained-by;
-   validated-by;
-   evidenced-by;
-   decided-by;
-   supersedes;
-   replaces;
-   terminated-by;
-   reassessed-by;
-   contributes-to; and
-   preserved-by.

Implementations MAY use different physical relationship representations
provided canonical meaning remains determinable.

## 37. Source of Truth

The Engineering System SHALL distinguish canonical Engineering semantics
from the systems that physically store or expose them.

A source of truth MAY be:

-   an Engineering repository;
-   a governed database;
-   an architecture decision repository;
-   an issue-tracking system;
-   a source-control platform;
-   a CI/CD platform;
-   a test system;
-   an AI orchestration platform;
-   an artifact store; or
-   another governed information source.

No product category is inherently authoritative for every Engineering
object.

Authority derives from Engineering governance and the role assigned to
the source.

## 38. External Tool Representation

Canonical Engineering objects MAY be projected into external tools.

For example:

    Engineering Slice
        ↔ issue / story / ticket / agent job group

    Engineering Evidence
        ↔ CI result / test report / deployment record

    Engineering Delivery Plan
        ↔ planning document / structured planning object

    Engineering Delivery Record
        ↔ governed record / database entity / generated representation

Tool-native objects SHALL NOT silently redefine canonical Engineering
semantics.

In particular:

-   issue `Done` SHALL NOT independently establish Slice Complete;
-   deployment success SHALL NOT independently establish Epic
    Engineering Completion;
-   a workflow status SHALL NOT redefine Record State;
-   a ticket approval SHALL NOT automatically establish governed
    acceptance;
-   an AI-agent result SHALL NOT independently establish evidence
    sufficiency; and
-   a tool user role SHALL NOT automatically establish Engineering
    decision authority.

## 39. Machine-readable Representation

Canonical Engineering objects SHOULD be representable in
machine-readable form sufficient for human, AI, and automated operation.

Machine-readable representations SHOULD preserve, as applicable:

-   object type;
-   stable identity;
-   revision;
-   state or outcome;
-   governing relationships;
-   authority;
-   conditions;
-   evidence references;
-   decision references;
-   timestamps where material;
-   historical relationships; and
-   lifecycle or record-state semantics.

Machine readability SHALL NOT require one universal physical schema for
every Engineering object.

A conforming implementation MAY maintain canonical semantics in
structured storage while generating Markdown or other human-readable
representations as views.

## 40. Human, AI, and Mixed-team Operation

Canonical object semantics SHALL remain consistent regardless of actor
type.

Human and AI actors MAY create, maintain, analyze, or realize governed
Engineering objects according to applicable authority.

AI systems MAY assist with:

-   artifact drafting;
-   planning;
-   Slice decomposition;
-   traceability;
-   architecture analysis;
-   ADR drafting;
-   realization;
-   validation;
-   evidence collection;
-   EDR maintenance;
-   conformance checking; and
-   identification of possible inconsistencies.

AI systems SHALL remain grounded in authoritative governed sources and
SHALL NOT invent governed facts, evidence, decisions, outcomes,
exceptions, or authority.

## 41. Proportional Application

The Artifact Model SHALL be applied proportionately.

A small Engineering realization MAY use:

-   concise artifacts;
-   logical baselines represented largely by references;
-   one or few Slices;
-   lightweight evidence links;
-   few or no ADRs; and
-   a concise EDR.

A large or materially significant realization MAY require:

-   richer artifact structures;
-   more explicit baseline representation;
-   many Slices;
-   multiple ADRs;
-   extensive evidence;
-   substantial reassessment traceability; and
-   a richer EDR.

Proportionality SHALL NOT remove canonical distinctions necessary for
defensible Engineering governance.

## 42. Cross-system Boundaries

The Artifact Model SHALL preserve boundaries between Engineering and
other systems.

The Engineering-ready Epic enters Engineering through the applicable
upstream Collaboration System boundary.

Engineering SHALL NOT silently redefine upstream Product or
Collaboration intent through an Engineering artifact or record.

A Finalized Engineering Delivery Record MAY provide the Engineering
basis for an applicable downstream cross-system Release Admission
decision.

The Finalized EDR SHALL NOT itself establish:

-   Release Admission;
-   Release Authorization;
-   Release Readiness;
-   environment promotion authority;
-   Production promotion authority; or
-   commercial launch authority.

Downstream Release records MAY reference the Finalized EDR.

The EDR does not require a reverse reference to a subsequently
established Release Admission decision.

## 43. Canonical Model Summary

The Engineering Artifact Model establishes the following semantic
distinctions:

    PROCESS
      Engineering Delivery Proposal development
      Engineering Delivery Planning
      Engineering Orchestration

    GOVERNED ARTIFACT
      Engineering Delivery Proposal
      Engineering Delivery Plan

    GOVERNED RECORD
      Architecture Decision Record
      Engineering Delivery Record

    GOVERNED BASELINE
      Approved Investment Baseline
      Execution Baseline

    GOVERNED REALIZATION UNIT
      Engineering Slice

    GOVERNED DECISION
      Investment Decision
      Execution Readiness Decision
      applicable reassessment decision

    ENGINEERING EVIDENCE
      authoritative support for Engineering claims

    REALIZATION CONDITION
      readiness / progression / governance /
      validation / evidence / acceptance

    ENGINEERING OUTCOME
      Slice Complete
      Slice Terminated
      Epic Engineering Completion
      Non-Completion Engineering Conclusion

These categories are semantic roles rather than storage formats.

The Engineering System remains coherent when each object preserves its
canonical identity, authority, relationships, history, and meaning while
allowing implementation technology, operational decomposition, and
representation to vary.
