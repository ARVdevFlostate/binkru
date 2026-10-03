# Engineering Governance Specification

## 1. Purpose

This specification defines the canonical governance model for the
Engineering System.

It establishes:

-   the governance principles applied across Engineering;
-   the governed decision boundaries of the Engineering lifecycle;
-   authority and accountability semantics;
-   the relationship between decisions, artifacts, records, baselines,
    realization units, evidence, conditions, and outcomes;
-   materiality, tolerances, triggers, and reassessment;
-   governance of Engineering Slices during realization;
-   architecture governance;
-   validation, evidence, acceptance, exception, and residual-condition
    governance;
-   Engineering conclusion governance;
-   historical integrity and traceability requirements;
-   cross-system escalation and boundary semantics; and
-   governance expectations for human, AI, automated, and mixed-team
    operation.

This specification defines Engineering governance.

It SHALL NOT prescribe a project-management framework, organizational
hierarchy, approval product, issue-tracking workflow, or implementation
technology.

Detailed lifecycle, artifact, delivery, orchestration, record, and
architecture semantics remain authoritative in their applicable
Engineering System specifications.

## 2. Governance Principle

Engineering governance exists to ensure that material Engineering
commitments, decisions, changes, claims, and conclusions are made with
sufficient authority, evidence, traceability, and historical integrity.

Governance SHALL be proportionate to Engineering consequence.

Governance SHALL NOT be equated with ceremony.

A governed Engineering action requires explicit governance where its
consequence materially affects a governed basis, commitment, authority
boundary, or conclusion.

Operational activity MAY proceed without additional governance where it
remains within the applicable authorized basis, authority, conditions,
and tolerances.

## 3. Governance Scope

Engineering governance applies across the canonical Engineering
lifecycle:

    Engineering-ready Epic
            ↓
    Engineering Delivery Proposal
            ↓
    Investment Decision
            ↓
    Approved Investment Baseline
            ↓
    Engineering Delivery Planning
            ↓
    Engineering Delivery Plan
            ↓
    Execution Readiness Decision
            ↓
    Execution Baseline
            ↓
    Engineering Orchestration
            ↓
    Engineering Slice realization
            ↓
    Engineering Conclusion
            ↓
    Engineering Delivery Record finalized
            ↓
    Engineering System lifecycle concluded

Governance is not confined to decision gates.

Continuous governance MAY also apply during planning and realization
through:

-   architecture decisions;
-   materiality assessment;
-   Delivery Tolerances;
-   Reassessment Triggers;
-   reassessment decisions;
-   authorization conditions;
-   exception handling;
-   Slice termination;
-   replacement realization;
-   evidence sufficiency;
-   applicable acceptance obligations;
-   Engineering conclusion establishment; and
-   EDR finalization.

## 4. Governance Principles

The Engineering System SHALL apply the following principles.

### 4.1 Explicit Authority

Material governed decisions SHALL be made by an actor or authority
authorized for that decision.

Technical capability, authorship, tool permissions, organizational
seniority, or AI capability SHALL NOT independently imply governance
authority.

### 4.2 Separation of Roles

Authorship, recommendation, execution, validation, maintenance, and
decision authority are distinct responsibilities.

One actor MAY hold multiple responsibilities where permitted, but the
semantic distinctions SHALL remain preserved.

### 4.3 Decision Before Authority-dependent Progression

Where lifecycle progression requires a governed decision, the required
decision SHALL be established before progression dependent upon that
authority is treated as authorized.

### 4.4 Evidence-proportionate Governance

Governed decisions and conclusions SHALL be supported by information and
evidence proportionate to their Engineering significance.

### 4.5 Materiality-driven Intervention

Governance intervention SHALL be driven by material consequence rather
than by the mere existence of change.

### 4.6 Historical Integrity

Governed decisions, baselines, material changes, dispositions, and
conclusions SHALL remain historically traceable.

Governance SHALL NOT rewrite prior governed history to make current
realization appear consistent with an earlier basis.

### 4.7 Controlled Adaptation

Engineering SHALL be allowed to adapt within authorized authority,
conditions, and tolerances.

Material adaptation SHALL use applicable reassessment rather than silent
execution drift.

### 4.8 Cross-system Respect

Engineering governance SHALL NOT silently exercise Product,
Collaboration, Release, deployment, commercial, or other authority
outside the Engineering System.

### 4.9 Tool Independence

External workflow states, approvals, permissions, or automation SHALL
NOT redefine canonical Engineering governance semantics.

## 5. Governance Objects

Engineering governance acts upon or establishes governed Engineering
objects defined by the Engineering Artifact Model.

These include:

-   Engineering Delivery Proposal;
-   Engineering Delivery Plan;
-   Architecture Decision Record;
-   Engineering Delivery Record;
-   Approved Investment Baseline;
-   Execution Baseline;
-   Engineering Slice;
-   Investment Decision;
-   Execution Readiness Decision;
-   applicable reassessment decisions;
-   Engineering Evidence;
-   realization conditions; and
-   Engineering outcomes.

Governance SHALL preserve the primary semantic classification of these
objects.

For example:

-   a decision SHALL NOT be conflated with the artifact it evaluates;
-   a baseline SHALL NOT be conflated with the decision that establishes
    it;
-   an ADR SHALL remain a Governed Record even though it preserves an
    architecture decision; and
-   an Engineering Slice SHALL remain a Governed Realization Unit even
    when it reaches a terminal outcome.

## 6. Governance Authority

Governance authority is the explicitly established right to make a
governed Engineering determination.

Authority MAY be assigned to:

-   an individual;
-   an Engineering role;
-   an Engineering team;
-   an architecture authority;
-   a governance body;
-   an authorized automated mechanism;
-   an authorized AI-assisted governance mechanism; or
-   another explicitly governed actor.

Authority MAY vary by:

-   decision type;
-   Engineering significance;
-   architecture significance;
-   security or compliance consequence;
-   financial consequence;
-   operational consequence;
-   environment;
-   organizational boundary; or
-   another governed criterion.

Authority SHALL be determinable for every material governed decision.

Governance authority SHALL be scoped to the governed determination for
which it is established.

Authority for one governed decision SHALL NOT imply authority for
another governed decision, lifecycle boundary, architecture
determination, Engineering outcome, or record finalization unless such
authority has been explicitly established.

For example, authority to approve Engineering investment does not by
itself imply authority to authorize execution, approve a material
architecture decision, terminate a Slice, establish an Engineering
conclusion, or finalize the EDR.

The same actor MAY hold multiple authorities where governance permits,
but each applicable authority SHALL remain semantically explicit.

Where authority is ambiguous, the decision SHALL NOT be inferred from
action or tool state.

## 7. Delegation of Authority

Governance authority MAY be delegated where permitted by the applicable
Engineering governance model.

Delegation SHOULD identify:

-   delegating authority;
-   delegated actor or mechanism;
-   scope of delegated authority;
-   applicable decision types;
-   limits or conditions;
-   effective period where relevant; and
-   escalation path.

Delegation SHALL NOT silently expand beyond its governed scope.

An AI agent MAY exercise delegated governance authority only where such
authority has been explicitly established.

The ability of an AI agent to recommend or execute an action SHALL NOT
imply authority to approve that action.

## 8. Decision Integrity

A governed Engineering decision SHALL preserve or reference, as
applicable:

-   decision identity;
-   decision type;
-   governed subject;
-   outcome;
-   authority;
-   rationale;
-   date or effective point;
-   supporting basis;
-   material evidence;
-   conditions;
-   resulting disposition;
-   required follow-up;
-   return, reconsideration, or escalation path; and
-   relationship to any baseline established by the decision.

Decision rationale SHALL be sufficient to explain the governed
determination proportionately to its consequence.

A decision SHALL remain historically identifiable after subsequent
revision, reassessment, or realization.

## 9. Recommendation and Decision

A recommendation is not a governed decision unless an applicable
authority explicitly establishes it as such.

Engineering artifacts and processes MAY produce recommendations.

Examples include:

-   Engineering recommendation in an Engineering Delivery Proposal;
-   Execution Readiness recommendation from Engineering Delivery
    Planning;
-   architecture recommendation;
-   reassessment recommendation; and
-   Engineering conclusion recommendation.

A tool, agent, or human actor SHALL NOT treat a recommendation as
authorization merely because no objection has been recorded.

Where governance permits automated decision establishment, that
authority SHALL be explicit.

## 10. Investment Decision Governance

The Investment Decision determines whether Engineering investment should
progress from Proposal to Delivery Planning.

It acts upon a ready Engineering Delivery Proposal.

Canonical Investment Decision outcomes are:

-   Approve;
-   Return;
-   Defer; or
-   Reject.

### 10.1 Approve

Approve establishes the Approved Investment Baseline and authorizes
Engineering Delivery Planning.

Approval MAY include explicit approved conditions.

Approved conditions SHALL remain traceable into planning and subsequent
governance where applicable.

### 10.2 Return

Return sends the Proposal for additional Engineering analysis,
clarification, correction, or revision.

Return SHALL identify sufficient rationale or required reconsideration
to make the return actionable.

Return does not establish an Approved Investment Baseline.

### 10.3 Defer

Defer preserves the Proposal and decision basis while declining present
progression.

Defer SHALL NOT be treated as Approve or Reject.

The applicable reconsideration trigger, timing, dependency, or condition
SHOULD be recorded where known.

### 10.4 Reject

Reject declines the proposed Engineering investment.

The rejection rationale and authority SHALL remain historically
traceable.

Reject SHALL NOT silently rewrite or erase the Proposal that was
evaluated.

## 11. Approved Investment Baseline Governance

An Approve Investment Decision establishes the Approved Investment
Baseline.

The baseline preserves the investment basis authorized for Engineering
Delivery Planning.

The Approved Investment Baseline SHALL:

-   identify or reference the approved Proposal revision;
-   identify or reference the Investment Decision;
-   preserve applicable approved conditions;
-   preserve material assumptions, constraints, risks, and accepted
    uncertainty;
-   remain historically identifiable; and
-   remain distinguishable from later planning or execution bases.

Engineering Delivery Planning MAY refine execution detail.

It SHALL NOT silently redefine a material element of the Approved
Investment Baseline.

Where planning materially challenges the approved investment basis,
applicable reassessment, return, or cross-system governance SHALL occur.

## 12. Engineering Delivery Planning Governance

Engineering Delivery Planning operates within the Approved Investment
Baseline.

Planning MAY refine:

-   Engineering Slice structure;
-   sequencing;
-   architecture;
-   dependencies;
-   implementation obligations;
-   validation obligations;
-   Engineering Evidence obligations;
-   applicable acceptance obligations;
-   capability and resource assumptions;
-   estimates;
-   milestones;
-   execution risks;
-   Delivery Tolerances; and
-   Reassessment Triggers.

Planning SHALL surface material conflict with the Approved Investment
Baseline rather than silently absorb it.

Planning SHALL produce sufficient governed information for an Execution
Readiness Decision.

## 13. Execution Readiness Decision Governance

The Execution Readiness Decision determines whether the proposed
Engineering execution basis is sufficiently governed for realization.

It acts upon the Engineering Delivery Plan and its applicable governed
basis.

Canonical Execution Readiness Decision outcomes are:

-   Authorize;
-   Return;
-   Defer; or
-   Reject.

### 13.1 Authorize

Authorize establishes the Execution Baseline and permits Engineering
Orchestration to begin.

Authorization MAY include explicit Authorization Conditions.

### 13.2 Return

Return sends the proposed execution basis for additional planning,
clarification, correction, or revision.

Return SHALL identify sufficient rationale or required reconsideration.

### 13.3 Defer

Defer preserves the Plan and readiness basis while declining present
authorization.

The applicable reconsideration condition SHOULD be recorded where known.

### 13.4 Reject

Reject declines the proposed execution basis.

Reject does not necessarily reject the Approved Investment Baseline
unless the applicable authority explicitly establishes that consequence.

Where rejection materially challenges the approved investment itself,
applicable investment or upstream governance SHALL be invoked.

## 14. Execution Baseline Governance

An Authorize Execution Readiness Decision establishes the Execution
Baseline.

The Execution Baseline defines what Engineering is authorized to
realize.

It SHALL preserve or reference, as applicable:

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

Realization SHALL remain within the Execution Baseline unless adaptation
is permitted within applicable authority and tolerances or a governed
reassessment establishes a revised future basis.

## 15. Authorization Conditions

A governed decision MAY establish explicit conditions upon its
authorization.

Authorization Conditions SHALL be:

-   identifiable;
-   attributable to the establishing decision;
-   sufficiently clear to determine applicability;
-   traceable into the governed activity they constrain; and
-   dispositioned where required before an affected downstream claim or
    conclusion.

A condition SHALL NOT be silently treated as satisfied merely because
progression occurred.

Where a condition becomes impossible, invalid, or materially changed,
applicable reassessment SHALL occur.

## 16. Delivery Tolerances

Delivery Tolerances define the bounded range within which Engineering
realization may adapt without requiring material reassessment.

Tolerances MAY apply to:

-   scope interpretation within Engineering authority;
-   implementation approach;
-   sequencing;
-   effort;
-   cost;
-   timing;
-   dependency handling;
-   architecture implementation detail;
-   validation approach;
-   evidence method; or
-   another governed execution dimension.

A tolerance SHALL be sufficiently explicit for applicable actors to
determine whether adaptation remains within the authorized envelope.

Operating within tolerance does not remove the obligation to preserve
material realization information in the EDR where applicable.

Tolerance SHALL NOT authorize Engineering to change upstream governed
intent or another cross-system commitment outside Engineering authority.

## 17. Reassessment Triggers

A Reassessment Trigger identifies a condition requiring governed
reconsideration of the current Engineering basis.

Triggers MAY include:

-   tolerance exceedance;
-   material scope consequence;
-   material architecture change;
-   material security or compliance concern;
-   material cost or effort change;
-   material schedule consequence;
-   material dependency change;
-   invalidated assumption;
-   material validation failure;
-   material evidence insufficiency;
-   external licensing or supplier change;
-   inability to satisfy an Authorization Condition;
-   Slice termination with material Epic consequence;
-   material upstream intent conflict; or
-   another condition established by the governed basis.

Triggers MAY be explicit or arise from material execution learning.

A trigger SHALL NOT predetermine the reassessment outcome.

## 18. Materiality

Materiality determines whether Engineering learning, change, variance,
failure, or external consequence requires additional governance.

Materiality SHALL be assessed by consequence to governed commitments
rather than by the size or novelty of the technical change alone.

A matter SHOULD be treated as material where it materially affects one
or more of:

-   Approved Investment Baseline;
-   Execution Baseline;
-   governed Epic intent;
-   architecture basis;
-   Engineering risk;
-   security or compliance obligations;
-   cost, effort, or timing commitments;
-   dependencies;
-   implementation obligations;
-   validation obligations;
-   Engineering Evidence obligations;
-   applicable acceptance obligations;
-   Authorization Conditions;
-   Delivery Tolerances;
-   Reassessment Triggers;
-   ability to establish Slice Complete;
-   ability to establish Epic Engineering Completion; or
-   another governed commitment.

Where materiality is uncertain and the consequence could reasonably be
material, the applicable governance path SHOULD be used rather than
silently assuming non-materiality.

## 19. Non-material Adaptation

Non-material adaptation MAY occur during Engineering Orchestration
without establishing a new governed baseline where:

-   the adaptation remains within applicable authority;
-   the adaptation remains within applicable Delivery Tolerances;
-   no Reassessment Trigger requires governance;
-   no upstream or cross-system intent is materially changed;
-   applicable obligations remain satisfiable; and
-   required traceability is preserved.

Non-material adaptation MAY still be recorded in the EDR where it is
useful to explain actual realization.

Routine implementation choice SHALL NOT require governance merely
because it differs from an earlier low-level expectation that was not
part of the governed basis.

## 20. Governed Reassessment

Governed reassessment determines how Engineering proceeds when the
current governed basis is materially challenged.

Reassessment SHALL preserve:

-   original governed basis;
-   material learning, trigger, or concern;
-   materiality basis;
-   applicable authority;
-   decision or disposition;
-   affected objects and obligations;
-   resulting governed basis; and
-   required follow-up.

Reassessment MAY result in:

-   continuation on the existing basis;
-   authorized adaptation;
-   revised Engineering Delivery Plan;
-   revised Execution Baseline;
-   new or revised Architecture Decision Record;
-   changed conditions or obligations;
-   changed Slice structure;
-   return to Engineering Delivery Planning;
-   upstream boundary escalation;
-   Slice termination;
-   replacement realization; or
-   another governed disposition.

Reassessment SHALL NOT rewrite the prior governed basis.

## 21. Revised Execution Basis

Where reassessment changes the future authorized execution basis, the
resulting basis SHALL be explicitly governed.

A revised Engineering Delivery Plan MAY be required where the change
materially affects planned execution.

A revised Execution Baseline SHALL be established through an applicable
governed reassessment decision carrying sufficient authority to
authorize the changed execution basis.

A reassessment event, materiality determination, recommendation, Plan
revision, or implementation change SHALL NOT by itself establish a
revised Execution Baseline.

The governing relationship is:

    material execution learning
            ↓
    governed reassessment
            ↓
    authority sufficiency determination
       ↙                         ↘
    sufficient                insufficient
       ↓                         ↓
    reassessment decision     return or escalate to
       ↓                      applicable governance boundary
    revised Execution            ↓
    Baseline                  required governed decision

Where the change exceeds the authority available through reassessment,
Engineering SHALL return or escalate to the applicable earlier
governance boundary.

That boundary MAY include:

-   Execution Readiness governance where the changed execution basis
    requires renewed execution authorization;
-   Investment governance where the Approved Investment Baseline is
    materially challenged; or
-   an applicable cross-system governance boundary where the matter
    exceeds Engineering authority.

The applicable authority SHALL determine the resulting future governed
basis before realization dependent upon that changed authority proceeds.

A revised Execution Baseline SHALL remain traceable to:

-   the prior Execution Baseline;
-   reassessment trigger or material learning;
-   reassessment decision;
-   authority establishing the revised basis;
-   applicable revised Plan;
-   changed obligations, conditions, tolerances, or triggers; and
-   effective future realization.

Prior realization SHALL remain interpreted against the governed basis
applicable when that realization occurred unless a specific governed
disposition establishes otherwise.

## 22. Engineering Slice Governance

Engineering Slices are the canonical governed units of Engineering
realization.

A Slice SHALL remain traceable to:

-   governing Engineering Delivery Plan;
-   applicable Execution Baseline;
-   applicable architecture basis;
-   applicable obligations;
-   dependencies;
-   realization responsibility;
-   validation;
-   Engineering Evidence; and
-   terminal outcome.

The canonical Slice lifecycle is:

    Authorized
        ↓
    Realizing
       ↙  ↘

Complete Terminated

Governance SHALL preserve the distinction between Slice lifecycle state
and orthogonal realization conditions.

## 23. Slice Authorization

A Slice is Authorized when it forms part of the applicable Execution
Baseline or is subsequently introduced through governed reassessment.

Authorization establishes permission for the Slice to enter governed
realization when applicable readiness and progression conditions permit.

Slice authorization SHALL NOT itself establish:

-   readiness to begin;
-   implementation completion;
-   validation success;
-   evidence sufficiency;
-   acceptance satisfaction; or
-   Slice Complete.

## 24. Slice Readiness Governance

Slice Readiness determines whether the prerequisites necessary for
governed realization of a Slice are sufficiently established.

Readiness MAY consider:

-   dependencies;
-   required inputs;
-   architecture basis;
-   environment availability;
-   implementation obligations;
-   validation obligations;
-   evidence obligations;
-   applicable acceptance obligations;
-   authorization conditions;
-   capability or resource needs; and
-   known blockers.

Readiness SHALL remain distinct from Slice lifecycle state.

An Authorized Slice MAY remain not ready without becoming a different
lifecycle state.

## 25. Pause, Resume, and Blocked Progression

Pause, Resume, and Blocked are progression semantics, not canonical
Slice lifecycle states.

A Realizing Slice MAY be Paused where realization is intentionally
suspended.

A Realizing Slice MAY be Blocked where realization cannot materially
progress because of an unresolved dependency, condition, decision,
issue, or external constraint.

A Paused or Blocked Slice remains Realizing unless a governed terminal
outcome is established.

Resume permits realization to continue when the applicable progression
condition is resolved.

Material Pause or Blocked conditions SHOULD preserve:

-   reason;
-   start or recognition point;
-   affected obligations or dependencies;
-   responsible actor;
-   required resolution or decision;
-   material consequences; and
-   resolution or resulting disposition.

Where Pause or Blocked progression materially affects the governed
basis, applicable reassessment SHALL occur.

## 26. Slice Completion Governance

Slice Complete is a terminal Slice lifecycle outcome.

A Slice SHALL reach Complete only when its applicable governed
completion basis is satisfied.

At minimum:

-   authorized realization has been implemented;
-   applicable technical validation has succeeded;
-   sufficient Engineering Evidence supports the completion claim; and
-   any additional governed completion prerequisite has been satisfied
    or received an applicable governed disposition.

Where acceptance obligations apply, their required state SHALL be
satisfied according to the governing basis before Slice Complete where
they are established as completion prerequisites.

Operational signals such as code merge, ticket closure, deployment,
agent completion, or workflow state SHALL NOT independently establish
Slice Complete.

## 27. Slice Termination Governance

Slice Terminated is a terminal Slice lifecycle outcome.

Termination SHALL be governed where realization ends without Slice
completion.

Termination SHALL preserve or reference, as applicable:

-   Slice identity;
-   reason;
-   authority or decision;
-   realization already performed;
-   Engineering Evidence already produced;
-   remaining obligations;
-   dependency consequences;
-   Epic consequences;
-   Execution Baseline consequences;
-   replacement or superseding realization; and
-   resulting disposition.

A Terminated Slice SHALL NOT be deleted or rewritten as though it never
existed.

Termination MAY require reassessment where the consequence is material.

## 28. Replacement and Superseding Realization

Where terminated, invalidated, or otherwise changed realization is
replaced, the replacement SHALL receive its own governed identity.

Replacement realization SHALL preserve traceability to the realization
it replaces or supersedes.

Replacement SHALL NOT overwrite historical Slice identity or outcome.

A Terminated Slice does not automatically prevent Epic Engineering
Completion where required realization has been governably replaced,
superseded, rendered no longer applicable, or otherwise dispositioned
and no required Engineering outcome remains materially unaccounted for.

## 29. Architecture Governance

Architecture governance is continuous across the Engineering lifecycle.

Material architecture decisions MAY arise during:

-   Engineering Delivery Proposal development;
-   Engineering Delivery Planning;
-   Engineering Orchestration; or
-   governed reassessment.

A material architecture decision requiring durable reasoning history
SHOULD be preserved through an Architecture Decision Record according to
the Architecture Decision specification.

Architecture governance SHALL consider proportionality.

Not every implementation choice requires an ADR.

Architecture significance SHALL be determined by consequence to the
governed Engineering basis, future Engineering constraints, system
qualities, dependencies, interoperability, security, operations, or
other material architecture concerns.

Architecture decisions SHALL remain historically traceable when
superseded.

## 30. Architecture Change During Realization

Where execution learning materially challenges the current architecture
basis:

    execution learning
            ↓
    materiality assessment
            ↓
    governed reassessment
            ↓
    architecture decision
            ↓
    new or revised ADR where applicable
            ↓
    revised governed future realization

A material architecture change SHALL NOT be silently introduced merely
because implementation is technically capable of proceeding.

The EDR SHOULD reference material architecture decisions that affected
actual realization.

The ADR remains authoritative for the architecture decision itself.

## 31. Technical Validation Governance

Technical validation establishes whether applicable Engineering claims
have been demonstrated sufficiently for their governed purpose.

Validation SHALL be proportionate to:

-   Engineering significance;
-   risk;
-   architecture consequence;
-   security consequence;
-   operational consequence;
-   uncertainty; and
-   applicable governed obligations.

Validation MAY occur incrementally throughout realization.

Validation SHALL remain distinct from implementation, evidence, and
acceptance.

A validation claim SHALL be supported by sufficient Engineering
Evidence.

## 32. Engineering Evidence Governance

Engineering Evidence supports specific Engineering claims.

Evidence governance SHALL ensure that material evidence is:

-   attributable;
-   traceable to the claim it supports;
-   sufficiently trustworthy;
-   sufficiently durable;
-   accessible according to applicable governance; and
-   proportionate to Engineering significance.

Evidence MAY remain in its authoritative source.

The Engineering System SHOULD reference evidence rather than duplicate
it where stable authoritative references are sufficient.

Evidence sufficiency SHALL be assessed against the claim being made.

The existence of evidence SHALL NOT independently establish that the
supported claim has been accepted or that an Engineering outcome has
been authorized.

## 33. Acceptance Governance

Acceptance is an applicable governed obligation, not a universal
mandatory lifecycle stage.

Acceptance obligations MAY be established by:

-   upstream governed agreements;
-   Engineering Delivery Plan;
-   Execution Baseline;
-   Authorization Conditions;
-   reassessment; or
-   another applicable governed basis.

Where acceptance applies, the governing basis SHALL make sufficiently
clear:

-   what is being accepted;
-   acceptance criteria or obligation;
-   applicable authority;
-   required evidence;
-   timing or lifecycle dependency; and
-   consequence of non-satisfaction.

Acceptance SHALL remain distinct from technical validation.

Technical validation demonstrates Engineering claims.

Acceptance establishes satisfaction of an applicable governed acceptance
obligation by the appropriate authority.

The Engineering System SHALL NOT invent acceptance authority where none
has been established.

## 34. Acceptance Outcomes

Where an acceptance obligation is represented during realization,
canonical domain-level acceptance status MAY include:

-   Not Applicable;
-   Pending; or
-   Satisfied.

Additional exception or failure semantics MAY be represented through the
applicable governed disposition rather than by expanding the canonical
Slice lifecycle.

Acceptance status SHALL NOT be confused with checklist conformance
results or Slice lifecycle state.

## 35. Exceptions

An exception is an explicitly governed departure from an otherwise
applicable Engineering obligation, condition, standard, or expectation.

An exception SHALL preserve or reference:

-   affected obligation;
-   reason;
-   scope;
-   authority;
-   supporting basis;
-   risk or consequence;
-   compensating control where applicable;
-   duration or expiry where applicable;
-   required follow-up; and
-   resulting disposition.

An exception SHALL NOT be inferred from non-compliance, omission, or
silence.

Approved exceptions MAY permit progression or conclusion only to the
extent explicitly authorized.

## 36. Residual Conditions

A residual condition is a material condition intentionally remaining at
Engineering conclusion or another governed boundary.

Residual conditions MAY include:

-   known technical limitation;
-   deferred technical obligation;
-   accepted Engineering risk;
-   unresolved non-blocking dependency;
-   operational prerequisite;
-   downstream Release consideration; or
-   another explicitly governed remaining condition.

Residual conditions SHALL be:

-   explicit;
-   traceable to applicable authority or disposition;
-   sufficiently described for downstream interpretation; and
-   preserved in the EDR where material to the Engineering conclusion.

A residual condition SHALL NOT be used to conceal an unmet prerequisite
required for the claimed Engineering conclusion.

## 37. Engineering Conclusion Governance

A governed Engineering realization SHALL conclude with exactly one
canonical Engineering conclusion:

-   Epic Engineering Completion; or
-   Non-Completion Engineering Conclusion.

The Engineering conclusion SHALL be established through applicable
Engineering authority and supported by sufficient governed basis and
Engineering Evidence.

The conclusion SHALL remain distinct from EDR finalization.

The Engineering conclusion establishes the governed Engineering outcome.

EDR finalization establishes the concluded historical Engineering record
preserving that outcome.

## 38. Epic Engineering Completion Governance

Epic Engineering Completion is the successful Engineering conclusion.

It SHALL be established only where required Engineering realization has
been implemented and technically validated to the extent required by the
governed Engineering basis.

The completion determination SHOULD consider, as applicable:

-   required Slice outcomes;
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
-   terminated or superseded realization;
-   residual conditions; and
-   unresolved governed issues.

Epic Engineering Completion SHALL NOT be inferred from a simple count of
Complete Slices.

No required Engineering realization may remain materially unaccounted
for.

Epic Engineering Completion SHALL NOT establish authority belonging to
Product, Collaboration, Release, deployment, operations, or commercial
governance.

## 39. Non-Completion Engineering Conclusion Governance

Where governed Engineering realization concludes without Epic
Engineering Completion, the canonical outcome SHALL be Non-Completion
Engineering Conclusion.

The conclusion SHALL preserve or reference:

-   specific governed reason;
-   applicable authority or decision;
-   supporting basis;
-   resulting disposition; and
-   sufficient traceability explaining why Epic Engineering Completion
    was not established.

The reason SHALL NOT become a separate canonical Engineering conclusion
state.

Non-Completion Engineering Conclusion SHALL NOT be represented as
successful Engineering completion.

## 40. Engineering Delivery Record Governance

The Engineering Delivery Record SHALL be instantiated when Engineering
Orchestration begins and progressively maintained through realization.

The EDR SHALL preserve material governed history sufficient to explain:

-   what basis was authorized;
-   what was actually realized;
-   what material changes occurred;
-   how those changes were governed;
-   what material decisions and architecture decisions applied;
-   what validation and evidence support material claims;
-   what Slice outcomes occurred;
-   what exceptions or residual conditions remain; and
-   what Engineering conclusion was established.

The EDR SHALL remain Active while governed realization or required
conclusion recording remains in progress.

The EDR SHALL become Finalized only when applicable finalization
requirements are satisfied.

Finalization SHALL NOT rewrite prior realization history.

## 41. Engineering System Conclusion Governance

Establishment of the Engineering conclusion and finalization of the EDR
are distinct lifecycle events.

The Engineering System lifecycle concludes only when:

-   the governed Engineering realization has reached its applicable
    Engineering conclusion;
-   the EDR sufficiently preserves that conclusion and its supporting
    governed basis; and
-   the EDR is Finalized according to applicable Engineering governance.

The lifecycle sequence is:

    Engineering Conclusion established
            ↓
    EDR preserves conclusion
    and satisfies finalization requirements
            ↓
    Engineering Delivery Record → Finalized
            ↓
    Engineering System lifecycle concluded

## 42. Cross-system Escalation

Engineering SHALL escalate through the applicable cross-system boundary
where a material matter exceeds Engineering authority.

Examples MAY include:

-   material change to Product intent;
-   material conflict with upstream acceptance agreements;
-   material commercial consequence;
-   material scope change outside Engineering interpretation authority;
-   Release policy or promotion authority;
-   organizational investment authority outside Engineering;
-   regulatory or legal authority outside Engineering; or
-   another governed external decision.

Engineering MAY provide analysis, evidence, options, and
recommendations.

Engineering SHALL NOT silently resolve an external authority question by
encoding a different assumption into an Engineering artifact or
implementation.

## 43. Engineering-to-Release Boundary

A Finalized Engineering Delivery Record MAY provide the Engineering
basis for an applicable downstream cross-system Release Admission
decision.

Neither Epic Engineering Completion nor EDR finalization establishes:

-   Release Admission;
-   Release Authorization;
-   Release Readiness;
-   QA promotion authority;
-   Pre-Production promotion authority;
-   Production promotion authority; or
-   commercial launch authority.

Those authorities belong to the applicable downstream Release System or
other governed system.

A downstream Release record MAY reference the Finalized EDR.

The EDR does not require a reverse reference to a subsequently
established Release decision.

## 44. Human, AI, and Automated Governance

Engineering governance MAY involve:

-   humans;
-   AI agents;
-   automated Engineering systems;
-   mixed human and AI teams; or
-   other authorized actors.

Actor type SHALL NOT change canonical governance semantics.

AI systems MAY assist with:

-   governance analysis;
-   conformance checking;
-   materiality assessment;
-   risk identification;
-   recommendation generation;
-   evidence collection;
-   traceability;
-   ADR drafting;
-   EDR maintenance;
-   detection of tolerance exceedance;
-   detection of Reassessment Triggers; and
-   preparation of governed decisions.

AI systems SHALL NOT:

-   invent authority;
-   invent decisions;
-   invent evidence;
-   silently approve their own recommendations;
-   silently redefine upstream intent;
-   treat tool permission as governance authority; or
-   establish a governed outcome without applicable authority.

Where an AI or automated mechanism is explicitly delegated decision
authority, the delegation SHALL remain governed and traceable.

## 45. Tool and Workflow Independence

Engineering governance SHALL remain independent of specific tools.

External systems MAY represent governance using:

-   workflow states;
-   approvals;
-   permissions;
-   pull-request reviews;
-   issue transitions;
-   CI gates;
-   policy engines;
-   agent workflows; or
-   other mechanisms.

Such mechanisms MAY implement canonical governance.

They SHALL NOT redefine it.

For example:

-   issue `Approved` SHALL NOT establish an Investment Decision unless
    configured and authorized to represent that canonical decision;
-   pull-request approval SHALL NOT automatically establish Slice
    Complete;
-   successful CI SHALL NOT independently establish Engineering
    conclusion;
-   deployment approval SHALL NOT automatically establish Release
    authority; and
-   agent workflow completion SHALL NOT establish governance authority.

## 46. Governance Traceability

Engineering governance SHALL support reconstruction of material governed
decisions and changes.

It SHOULD be possible to determine, as applicable:

-   what governed basis existed;
-   what decision established it;
-   who or what held authority;
-   what conditions applied;
-   what material learning or trigger arose;
-   how materiality was assessed;
-   what reassessment occurred;
-   what decision or disposition resulted;
-   what future basis changed;
-   what evidence supported material claims;
-   what exceptions were approved;
-   what residual conditions remained;
-   what Engineering conclusion was established; and
-   what Finalized EDR preserves the resulting history.

Traceability SHALL rely on stable governed identities and relationships
rather than tool workflow history alone.

## 47. Governance Conformance

An Engineering realization conforms to this governance model when,
proportionate to its significance:

-   required decisions are explicit;
-   applicable authority is determinable;
-   required baselines are established;
-   realization remains within authorized basis or is governably
    reassessed;
-   material changes are not silently absorbed;
-   architecture decisions are governed where material;
-   Slice terminal outcomes are supported;
-   validation and Engineering Evidence are sufficient for material
    claims;
-   applicable acceptance obligations are dispositioned;
-   exceptions are explicit and authorized;
-   residual conditions are explicit where material;
-   the Engineering conclusion is governed;
-   EDR finalization is distinct from conclusion establishment;
-   historical integrity is preserved; and
-   cross-system authority boundaries are respected.

Conformance SHALL be evaluated against canonical Engineering semantics
rather than superficial compliance with a particular tool workflow.

## 48. Proportional Governance

Governance SHALL be proportionate to Engineering significance.

A small, familiar, low-risk realization MAY require:

-   concise decision rationale;
-   lightweight baselines represented by references;
-   broad tolerances;
-   few explicit reassessment events;
-   minimal architecture governance;
-   lightweight evidence; and
-   a concise EDR.

A large, uncertain, architecturally significant, security-sensitive,
operationally sensitive, financially significant, or dependency-heavy
realization MAY require:

-   richer decision records;
-   explicit authority boundaries;
-   narrower tolerances;
-   explicit Reassessment Triggers;
-   multiple ADRs;
-   substantial validation and evidence;
-   explicit exception governance;
-   detailed reassessment history; and
-   a richer EDR.

Proportionality SHALL reduce unnecessary ceremony without removing
governance necessary for a defensible Engineering outcome.

## 49. Governance Summary

The Engineering Governance model can be summarized as:

    Engineering Delivery Proposal
            ↓
    Investment Decision
            ↓
    Approved Investment Baseline
            ↓
    Engineering Delivery Planning
            ↓
    Engineering Delivery Plan
            ↓
    Execution Readiness Decision
            ↓
    Execution Baseline
            ↓
    Engineering Orchestration
       ├── realization within authority and tolerances
       ├── continuous architecture governance
       ├── validation and Engineering Evidence
       ├── applicable acceptance governance
       ├── materiality assessment
       ├── reassessment when required
       ├── Slice Complete / Terminated
       ├── exception and residual-condition governance
       └── progressive EDR maintenance
            ↓
    Engineering Conclusion
       ├── Epic Engineering Completion
       └── Non-Completion Engineering Conclusion
            ↓
    EDR Finalized
            ↓
    Engineering System lifecycle concluded

The governing rule is:

> Engineering may adapt freely within its authorized envelope, but
> anything that materially changes a governed commitment, basis,
> authority boundary, or conclusion must itself be governed.

Engineering governance therefore enables adaptive realization without
sacrificing authority, evidence, traceability, historical integrity, or
cross-system boundaries.
