# Engineering Architecture Decision Specification

## 1. Purpose

This specification defines the canonical model for material architecture
decisions within the Engineering System.

It establishes:

-   what constitutes an Architecture Decision;
-   when an Architecture Decision Record (ADR) is warranted;
-   the distinction between an Architecture Decision and its ADR;
-   ADR lifecycle and Architecture Decision outcomes;
-   architecture decision authority and concurrence;
-   architecture scope;
-   review, approval, return, deferral, rejection, and supersession
    semantics;
-   post-acceptance immutability and correction rules;
-   relationships to Engineering Delivery Proposal, Engineering Delivery
    Planning, Engineering Delivery Plan, governed baselines, Engineering
    Slices, reassessment, Engineering Evidence, and the Engineering
    Delivery Record;
-   traceability and historical-integrity requirements; and
-   expectations for human, AI, automated, and mixed-team participation.

This specification governs material architecture decisions.

It SHALL NOT require an ADR for every design or implementation choice,
prescribe a particular architecture methodology, or assign architecture
authority to a specific organizational job title.

Applicable Engineering Lifecycle, Artifact Model, Governance, Delivery,
Orchestration, and EDR specifications remain authoritative for their
respective concerns.

## 2. Core Principle

Architecture governance is continuous across the Engineering lifecycle.

A material architecture decision MAY arise during Engineering Delivery
Proposal development, Engineering Delivery Planning, Engineering
Orchestration, governed reassessment, or another applicable Engineering
governance activity.

An ADR is not a lifecycle stage.

An ADR is the governed Engineering record that preserves a material
Architecture Decision and its durable reasoning history.

Routine technical choices SHALL remain within normal Engineering
realization where they do not materially affect a governed architecture
concern.

## 3. Architecture Decision and Architecture Decision Record

An Architecture Decision is the governed determination of a material
architecture matter.

An Architecture Decision Record is the durable governed record that
preserves the architecture proposition, decision basis, applicable
review history, Architecture Decision, and subsequent disposition.

The two concepts SHALL remain distinct:

    Architecture Decision
        = governed determination

    Architecture Decision Record
        = governed record preserving
          the determination and its basis

The persistence of an ADR SHALL NOT by itself establish an authoritative
Architecture Decision.

An Architecture Decision becomes authoritative only through the
applicable governed Architecture Decision outcome defined by this
specification.

## 4. One Material Decision per ADR

One ADR SHOULD preserve one coherent material Architecture Decision.

An ADR MAY address multiple tightly related considerations where they
form one indivisible architecture determination.

Materially independent decisions SHOULD use separate ADR identities.

This preserves clear authority, independent disposition, precise
supersession, useful traceability, understandable architecture history,
and reliable machine interpretation.

An ADR SHALL NOT become a general-purpose architecture notebook or
collection of unrelated design choices.

## 5. When an ADR Is Required

An ADR SHOULD be created where an architecture decision is material
enough to require durable governance and reasoning history.

Material architecture consequence MAY include significant effect on:

-   architecture basis;
-   system boundaries;
-   component or service responsibilities;
-   data ownership or persistence strategy;
-   integration or interoperability;
-   public or materially shared interfaces;
-   security or privacy architecture;
-   reliability, availability, resilience, or recoverability;
-   performance or scalability;
-   deployment or operational architecture;
-   technology or platform dependency;
-   material third-party dependency;
-   licensing or supplier constraint;
-   future Engineering constraints;
-   significant reversibility or migration cost;
-   cross-Slice or cross-Epic realization;
-   Approved Investment Baseline;
-   Execution Baseline; or
-   another materially governed Engineering concern.

Materiality SHALL be determined by consequence, not merely by technical
complexity or novelty.

## 6. When an ADR Is Not Required

An ADR is not required merely because Engineering made a technical
choice.

Routine local implementation choices MAY remain ordinary Engineering
decisions where non-material.

A team MAY preserve lightweight technical notes for such choices. Those
notes SHALL NOT automatically acquire canonical ADR semantics.

## 7. Architecture Decision Record Identity

Each ADR SHALL have a stable identity sufficient for durable reference.

ADR identity SHALL remain stable across drafting, review, Return,
Deferral, Acceptance, Rejection, and subsequent Supersession.

Identity SHALL NOT depend solely on filename, mutable title, directory
path, transient issue identifier, agent execution identifier, or
workflow position.

An ADR SHOULD have a concise descriptive title in addition to its stable
identity.

## 8. Architecture Scope

Each ADR SHALL identify the architecture scope to which its decision
applies.

Scope MAY include one Engineering realization, one or more Slices, a
component, service, subsystem, platform capability, integration
boundary, data domain, operational architecture concern, multiple Epics
or Delivery Plans, or another sufficiently bounded architecture domain.

An ADR SHALL NOT be assumed to belong exclusively to the Epic, Plan, or
Slice during which it was created.

An Accepted ADR MAY remain authoritative across subsequent Engineering
realizations until superseded or otherwise dispositioned according to
governance.

## 9. ADR Lifecycle

The canonical ADR lifecycle is:

    Draft
      ↓
    Ready for Review
      ↓
    Architecture Decision
      ├── Approve → Accepted
      ├── Return  → Draft
      ├── Defer   → Deferred
      └── Reject  → Rejected

A Deferred ADR MAY subsequently re-enter Draft or Ready for Review
according to the re-entry semantics defined by this specification.

A Rejected ADR is terminal for the architecture proposition represented
by that ADR.

An Accepted ADR MAY subsequently become Superseded.

The canonical ADR states are:

-   Draft;
-   Ready for Review;
-   Deferred;
-   Accepted;
-   Rejected; and
-   Superseded.

Approve, Return, Defer, and Reject are Architecture Decision outcomes.
They SHALL NOT be treated as ADR states.

## 10. Draft

Draft indicates that the ADR is under development.

Draft content is not authoritative architecture merely because it is
documented.

A Draft ADR MAY be revised freely subject to normal historical and
collaboration practices.

## 11. Ready for Review

Ready for Review indicates that the ADR is sufficiently developed for an
Architecture Decision.

Before entering Ready for Review, the ADR SHOULD contain, proportionate
to significance:

-   decision context and architecture scope;
-   material concern and relevant constraints;
-   viable alternatives and analysis;
-   material trade-offs, risks, and consequences;
-   relevant Engineering Evidence;
-   recommended option;
-   affected governed bases or realization;
-   applicable authorities; and
-   unresolved matters material to the decision.

Ready for Review is not approval.

## 12. Architecture Decision Outcomes

A Ready for Review ADR SHALL be subject to an Architecture Decision by
the applicable Architecture Decision Authority.

Canonical outcomes are Approve, Return, Defer, or Reject.

The outcome SHALL preserve or reference the ADR identity, outcome,
applicable authority, concurrence where required, rationale, effective
point, conditions, affected governed basis, required follow-up, and
resulting ADR state as applicable.

## 13. Approve

Approve establishes the proposed Architecture Decision as authoritative
for its governed scope and transitions the ADR to Accepted.

Approve SHALL NOT by itself authorize Engineering execution, revise a
governed baseline, establish Slice Complete, establish Epic Engineering
Completion, or authorize Release.

Where the approved Architecture Decision materially changes another
governed basis, the applicable reassessment or governance boundary SHALL
establish that changed basis.

## 14. Return

Return indicates that further analysis, clarification, correction,
evidence, or revision is required.

Return transitions the ADR to Draft while preserving stable identity and
applicable review history.

Return does not establish authoritative architecture.

## 15. Defer

Defer indicates that the Architecture Decision will not be established
at the present time and transitions the ADR to Deferred.

A Deferred ADR SHALL preserve the reason for deferral and SHOULD
identify the reconsideration trigger, condition, dependency, or timing
where known.

A Deferred ADR is not authoritative architecture.

A Deferred ADR MAY re-enter Draft when additional analysis, evidence, or
proposition revision is required.

A Deferred ADR MAY re-enter Ready for Review where the deferred
proposition remains materially unchanged and the condition preventing
the Architecture Decision has been resolved.

Re-entry SHALL preserve the prior Defer outcome and its rationale as
governed history.

Re-entry SHALL NOT create a new ADR identity merely because the
previously deferred proposition is being reconsidered.

## 16. Reject

Reject explicitly declines the proposed Architecture Decision and
transitions the ADR to Rejected.

A Rejected ADR SHALL be retained as governed architecture history and
SHOULD preserve sufficient rationale to explain why the proposition was
declined.

A Rejected ADR SHALL NOT constrain current architecture as an
authoritative decision.

Rejected is terminal for the architecture proposition represented by
that ADR.

A Rejected ADR SHALL NOT return to Draft or Ready for Review.

Where changed circumstances, new evidence, changed constraints, or
another material development causes a previously rejected approach to be
considered again, the materially renewed proposition SHALL use a new ADR
identity.

The new ADR SHOULD reference the Rejected ADR where the prior decision
is historically relevant.

## 17. Accepted

Accepted indicates that the Architecture Decision preserved by the ADR
is authoritative for its applicable scope.

An Accepted ADR SHALL preserve the accepted decision, scope, decision
authority, applicable concurrence, material rationale, alternatives
considered, relevant constraints, material consequences, relevant
Engineering Evidence, affected governed bases or realization, conditions
where applicable, and effective point.

Accepted SHALL remain distinguishable from execution authorization.

## 18. Post-Acceptance Immutability

The substantive Architecture Decision of an Accepted ADR SHALL be
immutable.

Materially changing the accepted decision, scope, rationale, or
architectural consequence SHALL require a new ADR and applicable
Architecture Decision.

Controlled non-substantive correction or enrichment MAY include
typographical or formatting correction, administrative metadata
correction, stable reference repair, non-substantive evidence links,
clarification that does not alter decision meaning, and
successor/supersession linkage.

Where correction could materially change interpretation, a new ADR SHALL
be used.

## 19. Supersession

Supersession occurs when a later Accepted ADR establishes a new
authoritative Architecture Decision that replaces all or part of an
earlier Accepted ADR for the applicable scope.

The superseding ADR SHALL identify the ADR or ADRs it supersedes.

The superseded ADR SHOULD identify its successor where the
representation permits governed linkage without rewriting substantive
history.

Supersession means the prior decision is no longer current authoritative
architecture for the superseded scope. It SHALL NOT imply that the prior
decision was necessarily incorrect.

A Superseded ADR SHALL remain durable architecture history.

## 20. Partial Supersession

Where a new Architecture Decision replaces only part of an earlier
decision, the relationship SHALL make the affected scope explicit.

Partial supersession SHALL NOT make it unclear which architecture basis
remains authoritative.

Where partial supersession would create excessive ambiguity, a clearer
replacement decision structure SHOULD be used.

## 21. No Deprecated State

The canonical ADR lifecycle does not require a separate Deprecated
state.

Where an Accepted decision is replaced, Superseded SHALL be used.

A distinct future state SHOULD be introduced only if the Engineering
System establishes a separate semantic need.

## 22. Architecture Decision Authority

Architecture Decision Authority is the explicitly established authority
to make an Architecture Decision for a defined architecture scope and
significance.

The Engineering System SHALL NOT hard-code Architecture Decision
Authority to a particular job title.

Authority MAY vary according to architecture scope, Engineering
significance, security, privacy/data, operational, platform,
interoperability, financial/supplier, organizational, or other governed
consequence.

Architecture Decision Authority SHALL be determinable before an ADR is
established as Accepted.

Authority SHALL remain scoped and non-transitive.

Authority to make one Architecture Decision SHALL NOT imply authority to
make another outside its scope, approve investment, authorize execution,
establish an Engineering conclusion, finalize an EDR, authorize Release,
or exercise another governance authority unless explicitly established.

## 23. Multiple-authority Concurrence

An Architecture Decision MAY require concurrence from multiple
applicable authorities where its material consequences cross governed
authority domains.

Required concurrence SHALL be determinable before the Architecture
Decision is established as Approve.

The specification SHALL NOT require fixed roles such as Security
Approver or Operations Approver.

Applicable governance determines which authorities are required.

Missing required concurrence SHALL prevent the ADR from becoming
Accepted.

## 24. Delegation

Architecture Decision Authority MAY be delegated according to the
Engineering Governance Specification.

Delegation SHALL identify, proportionate to significance, the delegating
authority, delegated actor or mechanism, architecture scope, decision
significance or class, limits and conditions, effective period where
relevant, and escalation path.

An actor's technical expertise or implementation responsibility SHALL
NOT by itself establish Architecture Decision Authority.

## 25. Relationship to Engineering Delivery Proposal

A material Architecture Decision MAY arise during Engineering Delivery
Proposal development.

An ADR MAY preserve a feasibility decision, architectural constraint,
Engineering risk, investment assumption, estimate/dependency
consequence, or architecture basis supporting an Approved Investment
Baseline.

A Proposal MAY reference Draft or Deferred ADRs where unresolved
architecture uncertainty is material.

Only Accepted ADRs SHALL be treated as authoritative architecture
decisions.

## 26. Relationship to Approved Investment Baseline

An Accepted ADR MAY contribute to the architecture basis represented by
an Approved Investment Baseline.

Accepting a new ADR after investment approval SHALL NOT silently rewrite
the Approved Investment Baseline.

Where the new Architecture Decision materially challenges the approved
investment basis, applicable Investment governance or other authorized
reassessment SHALL occur.

## 27. Relationship to Engineering Delivery Planning

Architecture decisions MAY emerge during Engineering Delivery Planning
as execution detail is refined.

Where such a decision is material, an ADR SHOULD be governed before the
affected execution basis is treated as ready for authorization.

Unresolved material architecture decisions SHALL be visible during
Execution Readiness evaluation.

## 28. Relationship to Engineering Delivery Plan

The Engineering Delivery Plan MAY reference applicable ADRs as part of
its architecture basis.

The Plan SHOULD distinguish Accepted ADRs from Deferred or unresolved
ADRs where material.

The Plan SHALL NOT treat a Draft, Ready for Review, Deferred, or
Rejected ADR as authoritative architecture.

## 29. Relationship to Execution Baseline

Accepted ADRs MAY form part of the architecture basis represented by an
Execution Baseline.

The Execution Baseline remains the governed basis authorizing
realization. The ADR remains the governed record of the Architecture
Decision.

The acceptance of an ADR SHALL NOT independently establish or revise the
Execution Baseline.

## 30. Architecture Decision During Orchestration

Engineering Orchestration MAY produce execution learning requiring a new
Architecture Decision.

The canonical reasoning path is:

    execution learning
            ↓
    architecture consequence identified
            ↓
    materiality assessment
       ↙                  ↘
    non-material          material
       ↓                    ↓
    local adaptation      governed reassessment
                            ↓
                      architecture proposition
                            ↓
                           ADR
                            ↓
                    Architecture Decision

Non-material architecture implementation detail MAY remain within the
authorized execution envelope.

Material architecture change SHALL use applicable governance.

## 31. Accepted ADR and Execution Authority

Where an Architecture Decision is Approved during Engineering
Orchestration, the ADR becomes Accepted.

If the decision materially changes the current Execution Baseline,
governed reassessment SHALL determine whether sufficient authority
exists to establish a revised basis or whether the matter must return or
escalate to the applicable governance boundary.

An Accepted ADR establishes architecture authority for its scope. It
does not automatically establish execution authority for a materially
changed basis.

## 32. Relationship to Reassessment

A material architecture concern arising against an existing governed
basis SHALL participate in the applicable Engineering reassessment
model.

Reassessment MAY result in continuation without a new ADR, creation or
revision of an ADR, an Architecture Decision, supersession, revised Plan
or Execution Baseline, changed Slice structure, upstream escalation, or
another governed disposition.

Architecture Decision Authority SHALL NOT silently exercise authority
belonging to Execution Readiness, Investment, Product, Release, or
another governed domain.

## 33. Relationship to Engineering Slices

An ADR MAY apply to one Slice, several Slices, all Slices in a
realization, or architecture beyond the current realization.

A Slice SHOULD reference applicable ADRs where those decisions
materially govern its realization.

A Slice SHALL NOT require an ADR merely because it exists.

Slice lifecycle state and ADR lifecycle state are independent.

Where a pending Architecture Decision materially prevents governed
progression, the applicable Slice MAY be Paused or Blocked according to
Engineering Orchestration governance.

## 34. Relationship to Engineering Evidence

An ADR MAY reference Engineering Evidence supporting its analysis and
recommendation, including benchmarks, prototypes, experiments,
validation, security analysis, performance results, reliability
analysis, compatibility analysis, operational findings, migration
experiments, supplier/licensing information, or other authoritative
sources.

Engineering Evidence supports architecture claims.

Evidence SHALL NOT make the Architecture Decision.

The applicable Architecture Decision Authority evaluates the governed
basis and establishes the decision.

## 35. Relationship to Engineering Delivery Record

The ADR and EDR have distinct responsibilities:

    ADR
      = why a material architecture
        decision was made

    EDR
      = what materially happened during
        Engineering realization

The EDR SHOULD reference ADRs that materially affected actual
realization.

The EDR SHALL NOT duplicate the ADR's full reasoning merely to preserve
delivery history.

The ADR SHALL NOT replace the EDR's realization history.

## 36. Cross-realization Architecture Knowledge

An Accepted ADR MAY remain authoritative beyond the Engineering
realization in which it was created.

Future Proposals, Plans, Execution Baselines, Slices, reassessments, and
EDRs MAY reference the same Accepted ADR where its scope remains
applicable.

A new Epic SHALL NOT require recreation of an existing applicable
Architecture Decision merely to make it visible.

## 37. Rejected and Deferred Knowledge Retention

Rejected and Deferred ADRs SHALL be retained where they constitute
governed architecture history.

They MAY inform future Engineering analysis but SHALL NOT be treated as
current authoritative architecture.

Historical ADRs SHALL be interpreted according to their state and
effective context.

## 38. Decision Context

An ADR SHOULD preserve sufficient context to make the decision
intelligible after the immediate delivery conversation has passed.

Context SHOULD include, proportionate to significance, the problem or
architecture concern, scope, relevant system context, material forces,
constraints, assumptions, dependencies, applicable governed basis,
relevant prior ADRs, and why a governed Architecture Decision is
required.

Context SHALL distinguish fact from assumption where material.

## 39. Alternatives and Trade-offs

A material ADR SHOULD identify viable alternatives sufficiently to
explain the decision.

The ADR SHOULD preserve alternatives seriously considered, relevant
advantages/disadvantages, material risks, reversibility, migration
consequence, operational consequence, future constraint, and why the
recommended or accepted option was preferred.

A single-option ADR MAY be valid where constraints genuinely eliminate
viable alternatives, but the basis SHOULD be explicit.

## 40. Consequences

An Accepted ADR SHOULD preserve material expected consequences of the
Architecture Decision, including benefits, costs, technical debt,
constraints, dependencies, migration obligations, operational/security
implications, validation obligations, future decision constraints, known
risks, and follow-up Engineering work as applicable.

Consequences SHALL NOT be limited to positive effects.

Material uncertainty SHOULD remain visible.

## 41. Conditions and Follow-up

An Architecture Decision MAY be Approved subject to explicit
architecture conditions where governance permits.

Conditions SHALL be identifiable, attributable, sufficiently clear,
traceable to affected realization, and dispositioned where required.

An ADR MAY identify follow-up actions without turning those actions into
canonical Engineering realization units.

Material follow-up realization SHOULD be governed through the applicable
Engineering Delivery Plan and Slice model.

## 42. Architecture Decision Traceability

The Engineering System SHOULD be able to determine, as applicable:

-   what architecture concern existed and why it was material;
-   what ADR represented it and what scope applied;
-   what alternatives and evidence informed it;
-   what recommendation was made;
-   who or what held Architecture Decision Authority;
-   what concurrence was required;
-   what outcome occurred and when it became effective;
-   what governed baselines and Slices were affected;
-   what later learning challenged the decision;
-   what ADR superseded it where applicable; and
-   what EDRs record material realization consequences.

Traceability SHALL rely on stable identities and governed relationships
rather than directory structure alone.

## 43. Human, AI, and Automated Participation

Humans, AI agents, automated systems, and mixed teams MAY participate
according to applicable authority.

AI systems MAY assist with identifying potential material decisions,
drafting ADRs, gathering context, alternatives/trade-off analysis,
architecture modelling, evidence collection, risk identification,
conformance analysis, finding prior ADRs, detecting possible
supersession, preparing recommendations, completeness checking, and
traceability.

AI capability SHALL NOT imply Architecture Decision Authority.

An AI system MAY move an ADR toward Ready for Review where authorized
operationally.

It SHALL NOT establish Approve, Return, Defer, or Reject unless
explicitly delegated sufficient authority.

An AI system SHALL NOT invent architecture facts, Engineering Evidence,
authority, concurrence, decision outcomes, accepted rationale, or
supersession.

## 44. Tool Independence

ADR governance SHALL remain independent of specific tools or file
formats.

An ADR MAY be represented as Markdown, a structured database record,
architecture repository object, issue-linked governed record,
machine-native Engineering object, or another durable governed
representation.

Tool workflow states MAY implement ADR lifecycle states. They SHALL NOT
redefine them.

Merged Markdown, issue status, pull-request approval, or agent workflow
completion SHALL NOT independently establish an authoritative
Architecture Decision unless explicitly configured and governed to
represent the canonical decision.

## 45. Machine-readable Representation

ADR representations SHOULD be machine-readable sufficiently to preserve,
as applicable:

-   ADR identity, title, state, and revision;
-   architecture scope and context;
-   decision proposition, alternatives, and recommendation;
-   evidence references and affected governed objects;
-   Architecture Decision outcome;
-   authority and concurrence;
-   effective point and conditions;
-   supersedes and superseded-by relationships;
-   related ADRs; and
-   EDR or realization references where material.

Machine readability SHALL NOT require one universal storage schema.

A conforming implementation MAY maintain ADR semantics in structured storage while generating Markdown as a human-readable governed view.

## 46. Proportional Application

ADR governance SHALL be proportionate to architecture significance.

A bounded material decision MAY require concise context, few
alternatives, lightweight evidence, one Architecture Decision Authority,
and concise consequence analysis.

A platform-wide, security-sensitive, operationally significant,
expensive, difficult-to-reverse, or cross-system decision MAY require
deeper analysis, prototypes or experiments, substantial Engineering
Evidence, multiple-authority concurrence, migration analysis, detailed
consequences, conditions, and broader traceability.

Proportionality SHALL reduce unnecessary ceremony without weakening
governance necessary for durable architecture decisions.

## 47. Conformance

Architecture decision governance conforms to this specification when,
proportionate to significance:

-   material architecture decisions are identified;
-   ADRs are used where durable governance is warranted;
-   Architecture Decision and ADR remain semantically distinct;
-   ADR identity and scope are stable;
-   Draft and Ready for Review are not treated as authoritative;
-   Architecture Decision outcomes are explicit;
-   applicable authority and required concurrence are determinable;
-   Accepted decisions are substantively immutable;
-   material change uses a new ADR;
-   supersession is explicit and historically preserved;
-   Accepted ADRs do not silently revise governed baselines;
-   material execution changes use reassessment;
-   evidence supports rather than makes decisions;
-   EDR and ADR responsibilities remain distinct;
-   Deferred re-entry preserves the prior Defer decision history;
-   Rejected is terminal for the represented proposition and materially
    renewed propositions use new ADR identities;
-   Rejected and Deferred knowledge is retained;
-   AI participation remains within explicit authority; and
-   tool state does not redefine canonical governance.

## 48. Canonical Summary

The canonical architecture decision model is:

    Material architecture concern
            ↓
    ADR → Draft
            ↓
    analysis / alternatives / evidence
            ↓
    ADR → Ready for Review
            ↓
    Architecture Decision
      ├── Approve → Accepted
      ├── Return  → Draft
      ├── Defer   → Deferred
      └── Reject  → Rejected

    Accepted ADR
            ↓
    authoritative architecture
    for its governed scope
            ↓
    may apply across Plans,
    Slices, and realizations
            ↓
    later material architecture change
            ↓
    new ADR
            ↓
    Architecture Decision → Approve
            ↓
    new ADR → Accepted
            ↓
    prior ADR → Superseded

During active Engineering realization, an Accepted ADR that materially
changes the Execution Baseline SHALL enter governed reassessment.
Sufficient authority may establish a revised basis; insufficient
authority requires return or escalation to the applicable governance
boundary.

The governing rule is:

> An ADR preserves a material Architecture Decision; it does not create
> architecture authority merely by existing, and it does not create
> execution authority merely by being Accepted.

This separation allows architecture governance to remain continuous,
durable, and reusable across Engineering delivery while preserving the
authority, baseline, realization, evidence, and historical-integrity
semantics of the wider Engineering System.
