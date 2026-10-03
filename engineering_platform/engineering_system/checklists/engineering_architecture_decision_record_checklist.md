# Engineering Architecture Decision Record Checklist

## 1. Purpose

Use this checklist to independently validate an Engineering Architecture
Decision Record (ADR) against the canonical Engineering
architecture-decision model.

This checklist validates, proportionate to the significance of the
decision:

-   ADR readiness for Architecture Decision;
-   canonical state and outcome semantics;
-   materiality and architecture scope;
-   decision context, alternatives, analysis, and Engineering Evidence;
-   Architecture Decision Authority and required concurrence;
-   decision integrity;
-   governed baseline and reassessment consequences;
-   Deferred, Rejected, Accepted, and Superseded semantics;
-   historical integrity and traceability; and
-   human, AI, automated, and tool-governance boundaries.

This checklist is the canonical validation instrument for ADR readiness
and conformance where it applies.

The Engineering Architecture Decision Specification remains
authoritative for architecture-decision semantics.

The Engineering Architecture Decision Record Template structures ADR
creation. Its embedded checks are authoring aids and do not replace this
checklist.

## 2. Validation Outcome

Use one of the following outcomes:

-   **Pass** --- the ADR satisfies applicable checklist requirements.
-   **Pass with Observations** --- the ADR is conformant, but
    non-blocking observations should be recorded.
-   **Rework Required** --- one or more material requirements are
    incomplete, inconsistent, ambiguous, or non-conformant.

A checklist result SHALL NOT itself establish an Architecture Decision.

A `Pass` does not mean `Approve`.

Architecture Decision outcomes remain:

-   Approve;
-   Return;
-   Defer; or
-   Reject.

## 3. Applicability

Before validation:

-   [ ] The record represents one coherent material Architecture
    Decision.
-   [ ] Use of an ADR is warranted by material architecture consequence.
-   [ ] The record is not merely a routine implementation choice or
    technical note.
-   [ ] The applicable Engineering Architecture Decision Specification
    is identifiable.
-   [ ] Applicable Engineering Governance and Artifact Model semantics
    are understood.

### Applicability Notes

`<notes>`

## 4. Record Identity and State

-   [ ] ADR ID is present.
-   [ ] ADR ID is stable and does not depend solely on filename, title,
    path, issue ID, agent execution ID, or workflow position.
-   [ ] Title is concise and sufficiently descriptive.
-   [ ] ADR State uses a canonical state only:
    -   Draft;
    -   Ready for Review;
    -   Deferred;
    -   Accepted;
    -   Rejected; or
    -   Superseded.
-   [ ] Architecture Decision outcomes are not represented as ADR
    states.
-   [ ] Revision identifies a representation revision of the same ADR.
-   [ ] Revision is not being used to materially alter an Accepted
    Architecture Decision under the same ADR identity.
-   [ ] Originating context is identifiable where material.
-   [ ] Creation/update metadata is sufficient for governed history.

### Identity / State Observations

`<observations>`

## 5. Architecture Concern and Materiality

-   [ ] The architecture concern requiring a decision is explicit.
-   [ ] The reason the concern is material is explicit.
-   [ ] Materiality is based on consequence rather than novelty or
    technical complexity alone.
-   [ ] Relevant material consequences are identified, where applicable,
    across architecture basis, boundaries, data, integration,
    interfaces, security/privacy, system qualities, operations,
    dependencies, licensing/suppliers, future constraints,
    reversibility/migration, cross-Slice/cross-Epic realization, or
    governed baselines.
-   [ ] Facts and assumptions are distinguishable where that distinction
    is material.
-   [ ] The ADR does not manufacture materiality merely to justify
    documentation.

### Materiality Observations

`<observations>`

## 6. Architecture Scope

-   [ ] Architecture scope is explicit.
-   [ ] Scope is sufficiently bounded to determine where the decision is
    authoritative if Accepted.
-   [ ] Scope is not implicitly limited to the Epic, Plan, or Slice in
    which the ADR originated unless that is the actual governed scope.
-   [ ] Cross-realization applicability is visible where relevant.
-   [ ] Scope does not combine materially independent Architecture
    Decisions into one ADR.
-   [ ] Partial or overlapping scope with related ADRs is
    understandable.

### Scope Observations

`<observations>`

## 7. Governed Basis and Relationships

-   [ ] Relevant Engineering Delivery Proposal is referenced where
    applicable.
-   [ ] Approved Investment Baseline is referenced where applicable.
-   [ ] Engineering Delivery Plan is referenced where applicable.
-   [ ] Execution Baseline is referenced where applicable.
-   [ ] Affected Engineering Slice(s) are referenced where applicable.
-   [ ] Prior, related, or potentially superseded ADRs are referenced
    where applicable.
-   [ ] Other governed Engineering objects materially affected by the
    decision are referenced.
-   [ ] References use stable governed identities where available.
-   [ ] The ADR does not rely on directory structure alone for semantic
    traceability.

### Governed Basis Observations

`<observations>`

## 8. Constraints, Assumptions, and Dependencies

-   [ ] Material constraints are explicit.
-   [ ] Material assumptions are explicit.
-   [ ] Material dependencies are explicit.
-   [ ] Assumptions are not presented as established facts.
-   [ ] Supplier, licensing, platform, interoperability, operational, or
    cross-system dependencies are visible where material.
-   [ ] Material uncertainty remains visible rather than being silently
    resolved.

### Constraint / Assumption / Dependency Observations

`<observations>`

## 9. Architecture Proposition

-   [ ] The architecture proposition is explicit.
-   [ ] The proposition is sufficiently precise to be decided.
-   [ ] The proposition is distinguishable from background context and
    recommendation rationale.
-   [ ] The proposition does not present itself as authoritative before
    an Approve outcome.
-   [ ] The proposition corresponds to the architecture scope being
    governed.

### Proposition Observations

`<observations>`

## 10. Alternatives

-   [ ] Viable alternatives seriously considered are represented
    proportionate to significance.
-   [ ] Alternatives are materially distinct where multiple options
    exist.
-   [ ] Advantages and disadvantages are visible.
-   [ ] Material risks and consequences are visible.
-   [ ] Reversibility and migration considerations are addressed where
    material.
-   [ ] Alternatives are not artificially manufactured where constraints
    genuinely leave one viable option.
-   [ ] Where only one viable option exists, the basis for that
    conclusion is explicit.

### Alternatives Observations

`<observations>`

## 11. Engineering Evidence

-   [ ] Material claims are supported by Engineering Evidence where
    evidence is necessary.
-   [ ] Evidence references point to authoritative sources where
    available.
-   [ ] Evidence relevance to the decision is understandable.
-   [ ] Benchmarks, prototypes, experiments, validation, security
    analysis, performance findings, operational findings,
    supplier/licensing information, or other evidence are included where
    material.
-   [ ] Evidence is distinguished from assumptions and recommendations.
-   [ ] Evidence supports the Architecture Decision but is not treated
    as making the decision.
-   [ ] No evidence appears invented, unverifiable, or attributed
    without basis.

### Evidence Observations

`<observations>`

## 12. Analysis and Trade-offs

-   [ ] Analysis explains the material reasoning across the proposition
    and alternatives.
-   [ ] Material trade-offs are explicit.
-   [ ] Relevant quality attributes are considered.
-   [ ] Security/privacy consequences are considered where material.
-   [ ] Operational consequences are considered where material.
-   [ ] Cost, supplier, or licensing consequences are considered where
    material.
-   [ ] Dependency consequences are considered where material.
-   [ ] Reversibility and migration are considered where material.
-   [ ] Future Engineering constraints are considered where material.
-   [ ] Validation consequences are considered where material.
-   [ ] Residual uncertainty is visible.
-   [ ] Analysis is proportionate rather than ceremonially exhaustive.

### Analysis Observations

`<observations>`

## 13. Recommendation

-   [ ] A recommended option is explicit where the ADR is being prepared
    for review.
-   [ ] Recommendation rationale is understandable.
-   [ ] Material risks or uncertainty associated with the recommendation
    are visible.
-   [ ] Recommendation is clearly distinguishable from the governed
    Architecture Decision.
-   [ ] Recommendation does not imply Architecture Decision Authority.

### Recommendation Observations

`<observations>`

## 14. Affected Engineering Realization

-   [ ] Materially affected Plans, Baselines, Slices, components,
    services, or other Engineering objects are identifiable.
-   [ ] Expected realization consequences are visible.
-   [ ] The ADR assesses whether approval would materially change an
    existing governed baseline.
-   [ ] `Yes`, `No`, or `Not Yet Determinable` baseline consequence is
    supported by sufficient reasoning.
-   [ ] Where a material baseline change may occur, the applicable
    reassessment or governance path is identified.
-   [ ] The ADR does not imply that Architecture Decision Authority can
    silently revise a governed execution basis.

### Realization / Baseline Observations

`<observations>`

## 15. Architecture Decision Authority

-   [ ] Primary Architecture Decision Authority is explicit.
-   [ ] Authority scope is explicit.
-   [ ] Authority basis or delegation is identifiable.
-   [ ] Authority is sufficient for the architecture scope and
    significance of the decision.
-   [ ] Authority is not inferred merely from authorship, technical
    expertise, implementation responsibility, tool ownership, or
    workflow state.
-   [ ] Authority is treated as scoped and non-transitive.
-   [ ] Architecture Decision Authority is not confused with Investment,
    Execution Readiness, Engineering Conclusion, EDR finalization,
    Release, or other governance authority.

### Authority Observations

`<observations>`

## 16. Required Concurrence

-   [ ] Cross-domain material consequences have been assessed for
    concurrence requirements.
-   [ ] Required concurrence is explicit where applicable.
-   [ ] Required authority for each concurrence is identifiable.
-   [ ] Concurrence status is explicit.
-   [ ] Required concurrence is satisfied before an Approve outcome
    establishes Accepted.
-   [ ] `Not Applicable` is used only where concurrence is genuinely
    unnecessary.
-   [ ] Missing concurrence is not bypassed by tool state, workflow
    completion, or recommendation.

### Concurrence Observations

`<observations>`

## 17. Ready for Review Validation

Use this section when validating transition to `Ready for Review`.

-   [ ] Architecture concern is sufficiently clear for decision.
-   [ ] Materiality is established.
-   [ ] Architecture scope is bounded.
-   [ ] Relevant governed basis is referenced.
-   [ ] Constraints, assumptions, and dependencies are visible.
-   [ ] Architecture proposition is explicit.
-   [ ] Alternatives are sufficiently analysed.
-   [ ] Material trade-offs, risks, and consequences are visible.
-   [ ] Relevant Engineering Evidence is referenced.
-   [ ] Recommendation is explicit.
-   [ ] Affected governed realization is identifiable.
-   [ ] Architecture Decision Authority is determinable.
-   [ ] Required concurrence is determinable.
-   [ ] Material unresolved matters are visible and do not prevent
    meaningful review.
-   [ ] No section incorrectly represents the proposition as already
    authoritative.

### Ready for Review Result

`Pass / Pass with Observations / Rework Required`

### Ready for Review Observations

`<observations>`

## 18. Architecture Decision Integrity

Use this section where an Architecture Decision has occurred.

-   [ ] Decision Outcome is one of `Approve / Return / Defer / Reject`.
-   [ ] Decision Authority is recorded.
-   [ ] Decision date or effective point is recorded.
-   [ ] Resulting ADR State corresponds correctly to the outcome:
    -   Approve → Accepted;
    -   Return → Draft;
    -   Defer → Deferred;
    -   Reject → Rejected.
-   [ ] Decision rationale is preserved.
-   [ ] Conditions are explicit where applicable.
-   [ ] Required follow-up is explicit where applicable.
-   [ ] Required concurrence is confirmed.
-   [ ] Decision history is preserved.
-   [ ] Checklist outcome has not been substituted for Architecture
    Decision outcome.

### Decision Integrity Observations

`<observations>`

## 19. Approve → Accepted Validation

Use when Decision Outcome is `Approve`.

-   [ ] Resulting ADR State is Accepted.
-   [ ] Accepted Architecture Decision is stated in concise
    authoritative form.
-   [ ] Applicable architecture scope is explicit.
-   [ ] Architecture Decision Authority was sufficient.
-   [ ] Required concurrence was satisfied.
-   [ ] Material expected consequences are preserved.
-   [ ] Conditions are preserved where applicable.
-   [ ] Baseline/reassessment consequences are explicit.
-   [ ] Acceptance is not treated as automatic execution authorization.
-   [ ] Acceptance is not treated as automatic revision of the Approved
    Investment Baseline or Execution Baseline.
-   [ ] Accepted decision substance is protected from material mutation
    under the same ADR identity.

### Accepted Validation Observations

`<observations>`

## 20. Return → Draft Validation

Use when Decision Outcome is `Return`.

-   [ ] Resulting ADR State is Draft.
-   [ ] Return rationale is explicit.
-   [ ] Required further analysis, clarification, correction, evidence,
    or revision is actionable.
-   [ ] Stable ADR identity is preserved.
-   [ ] Review/Return history is retained proportionate to significance.
-   [ ] Return has not been represented as rejection.
-   [ ] No authoritative Architecture Decision is implied.

### Return Validation Observations

`<observations>`

## 21. Defer → Deferred Validation

Use when Decision Outcome is `Defer`.

-   [ ] Resulting ADR State is Deferred.
-   [ ] Deferral rationale is explicit.
-   [ ] Reconsideration trigger, condition, dependency, or timing is
    recorded where known.
-   [ ] Deferred is not treated as authoritative architecture.
-   [ ] Stable ADR identity is preserved.

For a Deferred ADR that later re-enters:

-   [ ] Re-entry to Draft is used where additional analysis, evidence,
    or proposition revision is required; or
-   [ ] Re-entry to Ready for Review is used only where the proposition
    remains materially unchanged and the condition preventing the
    decision has been resolved.
-   [ ] Prior Defer outcome and rationale remain preserved as governed
    history.
-   [ ] Re-entry does not create a new ADR identity merely because the
    same deferred proposition is reconsidered.

### Deferred Validation Observations

`<observations>`

## 22. Reject → Rejected Validation

Use when Decision Outcome is `Reject`.

-   [ ] Resulting ADR State is Rejected.
-   [ ] Rejection rationale is explicit.
-   [ ] Rejected is treated as terminal for the architecture proposition
    represented by this ADR.
-   [ ] The ADR has not returned to Draft or Ready for Review after
    rejection.
-   [ ] A materially renewed proposition uses a new ADR identity.
-   [ ] The new ADR references the Rejected ADR where historically
    relevant.
-   [ ] The Rejected ADR is retained as architecture history.
-   [ ] Rejected is not treated as current authoritative architecture.

### Rejected Validation Observations

`<observations>`

## 23. Post-Acceptance Immutability

Use for an Accepted or Superseded ADR.

-   [ ] Substantive accepted decision has not been rewritten.
-   [ ] Architecture scope has not been materially changed under the
    same ADR identity.
-   [ ] Accepted rationale has not been materially rewritten.
-   [ ] Material architectural consequences have not been silently
    changed.
-   [ ] Any post-Acceptance revision is limited to permitted
    non-substantive correction or enrichment.
-   [ ] Governed correction history is preserved where applicable.
-   [ ] Material change uses a new ADR identity and applicable
    Architecture Decision.

### Immutability Observations

`<observations>`

## 24. Supersession

Use where an Accepted ADR supersedes another ADR or has itself become
Superseded.

-   [ ] Superseding ADR is Accepted.
-   [ ] Supersedes relationship is explicit.
-   [ ] Superseded-by relationship is recorded where the representation
    permits.
-   [ ] Effective point is identifiable.
-   [ ] Full or partial supersession scope is explicit.
-   [ ] Partial supersession leaves no ambiguity about which
    architecture basis remains authoritative.
-   [ ] Prior ADR remains preserved as durable architecture history.
-   [ ] Supersession is not interpreted as proof that the prior decision
    was incorrect.
-   [ ] A separate Deprecated state has not been invented to represent
    ordinary replacement.

### Supersession Observations

`<observations>`

## 25. EDR and Engineering Evidence Boundary

-   [ ] ADR preserves why the material Architecture Decision was made.
-   [ ] EDR references are used for material realization history where
    applicable.
-   [ ] ADR does not duplicate the EDR's realization history
    unnecessarily.
-   [ ] EDR does not replace the ADR's architecture reasoning.
-   [ ] Engineering Evidence remains in authoritative sources where
    stable references are sufficient.
-   [ ] Evidence is referenced rather than unnecessarily duplicated.
-   [ ] Material realization consequences of the Architecture Decision
    are traceable to applicable EDRs where relevant.

### ADR / EDR / Evidence Observations

`<observations>`

## 26. Cross-realization Integrity

-   [ ] An Accepted ADR remains reusable across future Engineering
    realizations where its scope remains applicable.
-   [ ] Existing applicable Architecture Decisions have not been
    recreated merely because a new Epic or Plan exists.
-   [ ] Future Proposals, Plans, Baselines, Slices, reassessments, or
    EDRs can reference the ADR through stable identity.
-   [ ] Historical ADR state and effective context are sufficient to
    distinguish current authority from historical knowledge.

### Cross-realization Observations

`<observations>`

## 27. Human, AI, and Automated Participation

Where AI or automation participated:

-   [ ] AI/automation participation is distinguishable from Architecture
    Decision Authority.
-   [ ] AI assistance in drafting, analysis, evidence collection,
    recommendation, conformance checking, or traceability remained
    within permitted authority.
-   [ ] Movement toward Ready for Review was operationally authorized
    where performed by automation.
-   [ ] AI/automation did not establish Approve, Return, Defer, or
    Reject without explicit sufficient delegation.
-   [ ] No architecture facts were invented.
-   [ ] No Engineering Evidence was invented.
-   [ ] No authority or concurrence was invented.
-   [ ] No decision outcome, accepted rationale, or supersession was
    invented.
-   [ ] Human and automated contributions remain traceable where
    governance requires.

### AI / Automation Observations

`<observations>`

## 28. Tool Independence

-   [ ] Tool state is not being treated as canonical ADR semantics
    unless explicitly governed to represent them.
-   [ ] Issue `Done` does not independently mean Accepted.
-   [ ] Pull-request approval does not independently mean Architecture
    Decision Approve.
-   [ ] Merged Markdown does not independently establish authoritative
    architecture.
-   [ ] Agent workflow completion does not independently establish
    Architecture Decision Authority.
-   [ ] Tool-specific metadata does not override canonical ADR state,
    decision outcome, authority, or supersession semantics.

### Tooling Observations

`<observations>`

## 29. Traceability and Historical Integrity

-   [ ] The material architecture concern can be traced to the ADR.
-   [ ] The ADR can be traced to its architecture scope.
-   [ ] Alternatives and Engineering Evidence can be traced where
    material.
-   [ ] Recommendation can be distinguished from the governed decision.
-   [ ] Decision authority and concurrence can be traced.
-   [ ] Decision outcome and effective point can be traced.
-   [ ] Affected governed baselines and Slices can be traced where
    applicable.
-   [ ] Reassessment can be traced where a material baseline consequence
    occurred.
-   [ ] Deferred re-entry preserves prior Defer history.
-   [ ] Rejected ADRs remain terminal for their represented
    propositions.
-   [ ] Supersession preserves predecessor/successor history.
-   [ ] EDR references preserve material realization consequences where
    applicable.
-   [ ] Historical records have not been rewritten to reflect current
    architecture as though it had always been true.

### Traceability Observations

`<observations>`

## 30. Proportionality Review

-   [ ] Validation depth is proportionate to architecture significance.
-   [ ] Bounded decisions are not burdened with unnecessary ceremony.
-   [ ] Platform-wide, security-sensitive, operationally significant,
    expensive, difficult-to-reverse, or cross-system decisions receive
    appropriately deeper validation.
-   [ ] Reduced ceremony has not removed material governance.
-   [ ] Additional ceremony has not obscured the actual Architecture
    Decision.

### Proportionality Observations

`<observations>`

## 31. Final Conformance Review

Before issuing the checklist result, confirm:

-   [ ] ADR use is materially warranted.
-   [ ] One coherent Architecture Decision is represented.
-   [ ] Identity, revision, state, and scope are correct.
-   [ ] Materiality and context are sufficient.
-   [ ] Alternatives, evidence, analysis, and recommendation are
    proportionate.
-   [ ] Applicable Architecture Decision Authority is explicit and
    sufficient.
-   [ ] Required concurrence is satisfied where applicable.
-   [ ] State and Architecture Decision outcome semantics are correct.
-   [ ] Accepted decisions are substantively immutable.
-   [ ] Deferred re-entry semantics are preserved.
-   [ ] Rejected terminality is preserved.
-   [ ] Supersession semantics are preserved.
-   [ ] Accepted ADRs do not silently revise governed baselines.
-   [ ] Material baseline consequences use governed reassessment.
-   [ ] ADR, EDR, and Engineering Evidence responsibilities remain
    distinct.
-   [ ] AI/automation remains within explicit authority.
-   [ ] Tool state does not redefine canonical governance.
-   [ ] Traceability and historical integrity are sufficient.

## 32. Checklist Result

### Result

`Pass / Pass with Observations / Rework Required`

### Blocking Findings

-   `<finding or None>`

### Non-blocking Observations

-   `<observation or None>`

### Required Rework

-   `<required rework or None>`

### Validator

`<actor / role / governed mechanism>`

### Validation Date / Reference

`<date/time or governed reference>`

## 33. Interpretation of Result

### Pass

`Pass` means the ADR satisfies applicable checklist requirements for the
validation purpose performed.

It does not establish an Architecture Decision.

Where the validation purpose is readiness, a Pass means the ADR may
proceed to the applicable Architecture Decision process.

### Pass with Observations

`Pass with Observations` means the ADR is conformant for the validation
purpose performed, but non-blocking observations remain worth
preserving.

Observations SHALL NOT be used to conceal a material deficiency that
should result in `Rework Required`.

### Rework Required

`Rework Required` means one or more material checklist requirements are
incomplete, inconsistent, ambiguous, or non-conformant.

The ADR SHOULD return to the applicable preparation or governance
activity.

A checklist result of `Rework Required` is not an Architecture Decision
outcome of `Return` unless the applicable Architecture Decision
Authority separately establishes `Return`.

## 34. Canonical Validation Rule

The checklist validates the ADR.

It does not make the Architecture Decision.

The governing separation is:

    ADR Specification
        = defines canonical semantics

    ADR Template
        = structures record creation

    ADR Checklist
        = independently validates
          readiness and conformance

    Architecture Decision Authority
        = establishes
          Approve / Return / Defer / Reject

Therefore:

    Checklist Pass
        ≠ Architecture Decision Approve

and:

    Checklist Rework Required
        ≠ Architecture Decision Return

unless the applicable governed authority separately establishes that
Architecture Decision outcome.
