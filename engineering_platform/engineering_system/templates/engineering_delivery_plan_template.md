# Engineering Delivery Plan Template

> Use this template to create the governed Engineering Delivery Plan for
> an Approved Engineering Delivery Proposal.
>
> The Plan establishes the executable Engineering basis submitted for
> Execution Readiness Decision.
>
> Apply the template proportionately. Sections that are not applicable
> MAY be marked `Not Applicable` with a brief rationale rather than
> populated artificially.
>
> The Plan SHALL elaborate the Approved Investment Baseline without
> silently changing it.

---

# 1. Plan Identity

**Project:**  
[Project name]

**Engineering Delivery Plan ID:**  
[Stable artifact identifier]

**Plan Revision:**  
[Revision identifier]

**Plan Status:**  
[Draft / In Review / Ready for Execution Readiness / Authorized /
Returned / Deferred / Rejected / Superseded]

**Plan Owner:**  
[Responsible Engineering owner]

**Created:**  
[Date]

**Last Updated:**  
[Date]

**Governing Engineering-ready Epic:**  
[Artifact identifier / reference]

**Approved Engineering Delivery Proposal:**  
[Artifact identifier / approved revision]

**Investment Decision:**  
[Decision identifier / reference]

**Approved Investment Baseline:**  
[Artifact identifier / reference where separately represented]

---

# 2. Planning Context

## 2.1 Approved Realization

Summarize the Engineering realization approved through the Investment
Decision.

This summary SHALL remain consistent with the Approved Investment
Baseline.

[Approved realization summary]


## 2.2 Intended Engineering Outcome

Describe the Engineering outcome that this Plan is intended to realize.

[Engineering outcome]


## 2.3 Planning Interpretation

Summarize how Engineering interprets the approved proposition for
execution.

Include material:

- realization boundaries;
- quality expectations;
- constraints;
- external obligations;
- execution assumptions; and
- other context necessary to understand the Plan.

[Planning interpretation]


## 2.4 Approved Conditions

List conditions attached to the Approve Investment Decision.

| Condition | Planning Disposition | Owner | Resolution Point / Evidence |
|---|---|---|---|
| [Condition] | [Satisfied / Allocated / Deferred / Escalated / Other] | [Owner] | [Reference] |

If none:

`None.`


## 2.5 Planning Obligations

List Planning Obligations inherited from the Approved Investment
Baseline.

| Obligation | Disposition | Owner | Slice / Resolution Point |
|---|---|---|---|
| [Obligation] | [Disposition] | [Owner] | [Reference] |

If none:

`None.`


## 2.6 Carried-forward Uncertainty

Identify material uncertainty inherited from the Approved Investment
Baseline.

| Uncertainty | Potential Consequence | Current Disposition | Resolution Point / Trigger |
|---|---|---|---|
| [Uncertainty] | [Consequence] | [Disposition] | [Point / trigger] |

If none:

`None.`

---

# 3. Realization Strategy

Describe the overall Engineering strategy for realizing the approved
proposition.

The strategy SHOULD explain:

- major realization boundaries;
- incremental realization approach where applicable;
- significant integration strategy;
- major technical or operational considerations;
- sequencing rationale;
- significant risk-reduction strategy; and
- how the proposed realization structure supports credible execution.

[Realization strategy]

---

# 4. Engineering Slice Structure

## 4.1 Slice Structure Rationale

Explain the selected Engineering Slice structure.

Where the realization is represented by a single Engineering Slice,
explain briefly why further decomposition would not meaningfully improve
execution governance, traceability, validation, acceptance, evidence,
risk management, or delivery adaptability.

Where multiple Slices are used, explain the principal decomposition
logic.

[Slice structure rationale]


## 4.2 Slice Summary

| Slice ID | Slice Name | Realization Objective | Dependencies | Planned Sequence / Window | Owner |
|---|---|---|---|---|---|
| [ID] | [Name] | [Objective] | [Dependencies] | [Sequence / window] | [Owner] |

Add rows as required.

---

# 5. Engineering Slice Detail

Repeat this section for each Engineering Slice.

## Slice [ID] — [Slice Name]

### 5.1 Realization Objective

Describe the meaningful Engineering outcome produced by this Slice.

[Objective]


### 5.2 Governing Traceability

**Engineering-ready Epic:**  
[Reference]

**Approved Delivery Proposal / Investment Basis:**  
[Reference]

**Relevant Acceptance Expectations:**  
[Reference]

**Relevant ADRs:**  
[Reference / None]

**Relevant Planning Obligations:**  
[Reference / None]

**Relevant External Obligations:**  
[Reference / None]

**Other Material Traceability:**  
[Reference / None]


### 5.3 Included Engineering Work

[Included work]


### 5.4 Material Exclusions

[Excluded work / None]


### 5.5 Affected Systems or Components

[Affected systems / components]


### 5.6 Inputs and Prerequisites

[Inputs / prerequisites]


### 5.7 Expected Outputs or Resulting Capability

[Outputs / capability]


### 5.8 Dependencies

| Dependency | Type | Required State / Availability | Owner | Consequence if Unavailable |
|---|---|---|---|---|
| [Dependency] | [Type] | [Required state] | [Owner] | [Consequence] |

If none:

`None.`


### 5.9 Implementation Obligations

Identify material obligations that must be satisfied during realization.

[Implementation obligations]


### 5.10 Validation Obligations

Describe how realization of this Slice will be technically validated.

[Validation obligations]


### 5.11 Acceptance Expectations

Describe the governed acceptance expectations applicable to this Slice.

[Acceptance expectations]


### 5.12 Engineering Evidence

Identify material Engineering Evidence expected from realization of this
Slice.

[Evidence requirements]


### 5.13 Slice-specific Risks and Uncertainty

| Risk / Uncertainty | Potential Consequence | Mitigation / Treatment | Trigger / Resolution Point |
|---|---|---|---|
| [Item] | [Consequence] | [Treatment] | [Trigger / point] |

If none:

`None.`


### 5.14 Slice Notes

[Additional execution-relevant information / None]

---

# 6. Dependency Model

Describe material dependencies affecting realization across the Plan.

Dependencies MAY include:

- Slice dependencies;
- architecture dependencies;
- platform or infrastructure dependencies;
- environment dependencies;
- data dependencies;
- security dependencies;
- external service or vendor dependencies;
- Product dependencies;
- organizational dependencies;
- cross-Epic dependencies; and
- other execution-significant dependencies.

| Dependency | Affected Slice(s) | Owner | Required By | Current State | Consequence | Mitigation / Contingency | Escalation Condition |
|---|---|---|---|---|---|---|---|
| [Dependency] | [Slice(s)] | [Owner] | [Point] | [State] | [Consequence] | [Treatment] | [Condition] |

If no material dependencies:

`None.`

---

# 7. Realization Sequencing

Describe how Engineering Slices are expected to progress.

Identify, where material:

- mandatory predecessor relationships;
- concurrency opportunities;
- synchronization points;
- integration points;
- decision points;
- validation points;
- acceptance points; and
- sequencing constraints.

[Sequencing description]


## 7.1 Sequence Representation

Provide an appropriate representation of the realization sequence.

Example:

    Slice 01
        ↓
    Slice 02
        ├────────→ Slice 03
        │
        └────────→ Slice 04
                       ↓
                   Slice 05

[Sequence representation]

The representation MAY instead reference an authoritative external
planning representation where permitted by Engineering governance.

---

# 8. Architecture Plan

## 8.1 Applicable Architecture Decisions

| ADR | Status | Affected Slice(s) | Planning Consequence |
|---|---|---|---|
| [ADR reference] | [Status] | [Slice(s)] | [Consequence] |

If none:

`None.`


## 8.2 Required Architecture Decisions

Identify architectural decisions that must still be made.

| Decision Required | Required By | Affected Slice(s) | Owner | Current State |
|---|---|---|---|---|
| [Decision] | [Resolution point] | [Slice(s)] | [Owner] | [State] |

If none:

`None.`


## 8.3 Architectural Constraints and Obligations

[Constraints / obligations]


## 8.4 Unresolved Architectural Obligations

Identify architectural matters intentionally carried into Engineering
Orchestration.

For each material item, explain why carrying it forward does not prevent
credible execution authorization.

| Obligation / Decision | Reason for Carry-forward | Resolution Point | Affected Slice(s) |
|---|---|---|---|
| [Item] | [Reason] | [Point] | [Slice(s)] |

If none:

`None.`

---

# 9. Cross-cutting Implementation Obligations

Identify implementation obligations applying across multiple or all
Engineering Slices.

These MAY include:

- security controls;
- observability;
- infrastructure;
- configuration;
- data management;
- migration;
- documentation;
- deployment preparation;
- operational readiness; and
- other cross-cutting realization requirements.

[Cross-cutting implementation obligations]

---

# 10. Validation Strategy

Describe the overall Engineering validation strategy.

The strategy SHOULD identify the validation mechanisms necessary to
establish credible evidence that the realization satisfies its
Engineering obligations.

Applicable validation MAY include:

- automated testing;
- unit testing;
- integration testing;
- system testing;
- performance validation;
- security validation;
- reliability validation;
- migration validation;
- infrastructure validation;
- operational validation;
- compatibility validation; and
- manual technical validation.

[Validation strategy]


## 10.1 Cross-Slice / Aggregate Validation

Identify validation that cannot be meaningfully performed within a single
Slice.

[Aggregate validation / None]

---

# 11. Acceptance Strategy

Describe how Engineering will establish that realization satisfies the
governed acceptance basis.

Identify, where applicable:

- Slice-level acceptance;
- aggregate or integration acceptance;
- required acceptance evidence;
- responsible acceptance authority;
- conditions preventing acceptance; and
- escalation where acceptance cannot be established.

[Acceptance strategy]


## 11.1 Acceptance Authority

| Acceptance Area | Authority | Required Evidence | Decision Point |
|---|---|---|---|
| [Area] | [Authority] | [Evidence] | [Point] |

---

# 12. Engineering Evidence Strategy

Describe the material Engineering Evidence expected during realization.

Evidence SHOULD support material Engineering claims rather than exist
solely for governance ceremony.

| Evidence | Claim Supported | Producing Slice / Activity | Expected Point | Repository / Reference |
|---|---|---|---|---|
| [Evidence] | [Claim] | [Source] | [Point] | [Reference] |

---

# 13. Capability and Resource Plan

## 13.1 Required Engineering Capabilities

| Capability | Required For | Availability | Constraint / Gap |
|---|---|---|---|
| [Capability] | [Slice / concern] | [Availability] | [Constraint] |


## 13.2 Slice Responsibility

| Slice | Execution Owner / Responsible Actor | Supporting Capability / Actors |
|---|---|---|
| [Slice] | [Owner] | [Support] |


## 13.3 Shared or Constrained Resources

Identify material shared resources, specialist constraints,
infrastructure capacity, environments, or other resource contention.

[Resource constraints / None]


## 13.4 External Sourcing

[External sourcing requirements / None]

---

# 14. Refined Delivery Estimate

Record the refined Engineering estimate derived through Delivery
Planning.

The estimate SHALL retain an explainable basis and SHALL NOT imply
unsupported precision.


## 14.1 Effort

**Refined Effort Estimate:**  
[Estimate / range]

**Basis:**  
[Explain basis]


## 14.2 Cost

**Refined Cost Estimate:**  
[Estimate / range]

**Basis:**  
[Explain basis]


## 14.3 Delivery Timing

**Refined Delivery Estimate:**  
[Estimate / range]

**Basis:**  
[Explain basis]


## 14.4 Other Material Estimate Dimensions

[Infrastructure / external services / specialist requirements / other]


## 14.5 Relationship to Proposal Estimate

**Proposal Estimate:**  
[Reference / summary]

**Material Difference:**  
[Yes / No]

**Explanation:**  
[Explain refinement]

**Within Approved Investment Basis and Applicable Tolerances:**  
[Yes / No]

If `No`, identify the required governed reassessment:

[Reassessment reference / required action]

The Approved Proposal SHALL NOT be rewritten merely to align it with the
refined Plan estimate.

---

# 15. Delivery Timeline

Describe the credible delivery timeline.

The timeline MAY use:

- target windows;
- milestones;
- Slice sequence;
- dependency dates;
- decision points;
- integration points;
- validation points;
- acceptance points;
- release points; or
- another suitable representation.

[Timeline]


## 15.1 Timeline Assumptions

[Timing assumptions]


## 15.2 Timeline Uncertainty

[Timing uncertainty / None]


## 15.3 External Schedule Representation

**External Tool / Representation:**  
[Reference / None]

**Authoritative Operational Information, if any:**  
[Describe explicitly / None]

---

# 16. Milestones

| Milestone | Engineering State / Outcome | Target | Dependency / Condition |
|---|---|---|---|
| [Milestone] | [State / outcome] | [Target] | [Dependency] |

If milestones are unnecessary:

`Not Applicable — [brief rationale].`

---

# 17. Execution Risks

| Risk | Affected Slice(s) / Area | Potential Consequence | Mitigation | Contingency | Trigger / Indicator | Escalation Condition | Residual Concern |
|---|---|---|---|---|---|---|---|
| [Risk] | [Area] | [Consequence] | [Mitigation] | [Contingency] | [Trigger] | [Escalation] | [Residual concern] |

If no material execution risks:

`None identified.`

---

# 18. Issues and Blockers

## 18.1 Issues

| Issue | Affected Area | Consequence | Owner | Required Action |
|---|---|---|---|---|
| [Issue] | [Area] | [Consequence] | [Owner] | [Action] |

If none:

`None.`


## 18.2 Blockers

| Blocker | Affected Area | Required Resolution | Owner | Resolution State |
|---|---|---|---|---|
| [Blocker] | [Area] | [Resolution] | [Owner] | [State] |

If none:

`None.`

A blocker preventing a credible executable basis SHALL prevent Execution
Readiness unless resolved or explicitly governed by an applicable
authority.

---

# 19. Assumptions

## 19.1 Inherited Assumptions

| Assumption | Proposal / Baseline Reference | Current State | Consequence if Invalid |
|---|---|---|---|
| [Assumption] | [Reference] | [Validated / Refined / Retained / Invalidated / Other] | [Consequence] |


## 19.2 Planning Assumptions

| Assumption | Basis | Validation / Resolution Point | Consequence if Invalid |
|---|---|---|---|
| [Assumption] | [Basis] | [Point] | [Consequence] |

If none:

`None.`


## 19.3 Invalidated Assumptions

Identify whether any assumption invalidates or materially changes the
Approved Investment Baseline.

[Assessment / None]

Where the Approved Investment Baseline is materially affected, identify
the required reassessment.

[Reassessment reference / None]

---

# 20. Execution Uncertainty

Identify material uncertainty remaining at the point of Execution
Readiness.

| Uncertainty | Potential Consequence | Why Execution Remains Credible | Resolution Point / Condition | Applicable Authority / Tolerance |
|---|---|---|---|---|
| [Uncertainty] | [Consequence] | [Rationale] | [Point] | [Authority / tolerance] |

If none:

`None.`

Uncertainty SHALL NOT be hidden merely to obtain Execution Readiness.

---

# 21. Delivery Tolerances

Identify the tolerances within which Engineering Orchestration may adapt
without requiring governed reassessment.

| Dimension | Applicable Tolerance | Authority / Source | Escalation Point |
|---|---|---|---|
| [Effort / Cost / Timing / Scope / Dependency / Architecture / Risk / Other] | [Tolerance] | [Authority] | [Point] |

If no project-specific tolerances apply:

[Reference applicable Engineering Platform / organizational governance.]

The Plan SHALL NOT establish tolerances exceeding authority delegated to
the project.

---

# 22. Reassessment Triggers

Identify conditions that require governed reassessment during Engineering
Orchestration.

| Trigger | Affected Basis | Required Governance Action |
|---|---|---|
| [Trigger] | [Investment / Execution / Architecture / Acceptance / Other] | [Action] |

Triggers MAY include:

- material scope change;
- invalidated investment assumption;
- material estimate movement;
- critical dependency failure;
- architectural change;
- unacceptable risk increase;
- inability to satisfy acceptance;
- material resource loss;
- operational constraint change; and
- material external obligation change.

---

# 23. External Obligations

Identify external obligations material to execution.

These MAY include:

- regulatory obligations;
- compliance obligations;
- contractual commitments;
- vendor constraints;
- licensing obligations;
- security obligations;
- operational commitments; and
- other externally imposed requirements.

| Obligation | Source | Affected Slice(s) / Area | Required Treatment | Evidence / Resolution |
|---|---|---|---|---|
| [Obligation] | [Source] | [Area] | [Treatment] | [Evidence] |

If none:

`None.`

---

# 24. Supporting Engineering Artifacts

List material artifacts supporting the Engineering Delivery Plan.

| Artifact | Type | Purpose | Reference |
|---|---|---|---|
| [Artifact] | [ADR / Evidence / Discovery / Dependency Model / Estimate / Other] | [Purpose] | [Reference] |

---

# 25. Planning Traceability

Confirm traceability to the governed Engineering context.

| Governed Element | Reference |
|---|---|
| Engineering-ready Epic | [Reference] |
| Approved Engineering Delivery Proposal | [Reference] |
| Investment Decision | [Reference] |
| Approved Investment Baseline | [Reference] |
| Applicable Product artifacts | [Reference / None] |
| Applicable Collaboration artifacts | [Reference / None] |
| Architecture Decision Records | [Reference / None] |
| Engineering Slices | [Reference / embedded] |
| Approved Conditions | [Reference / embedded] |
| Planning Obligations | [Reference / embedded] |
| Material assumptions | [Reference / embedded] |
| Material uncertainty | [Reference / embedded] |
| Dependencies | [Reference / embedded] |
| Engineering Evidence | [Reference / planned] |
| External obligations | [Reference / embedded] |
| Other Supporting Engineering Artifacts | [Reference / None] |

---

# 26. Planning Completeness Assessment

## 26.1 Executable Basis

Explain why the Plan establishes a credible executable Engineering basis.

[Assessment]


## 26.2 Remaining Planning Gaps

Identify any remaining gaps.

[Remaining gaps / None]


## 26.3 Material Blockers to Execution Readiness

[Blockers / None]


## 26.4 Approved Investment Baseline Integrity

**Does this Plan remain consistent with the Approved Investment
Baseline?**

[Yes / No]

**Assessment:**  
[Explain]

If `No`, the Plan SHALL NOT silently proceed to authorization. Identify
the required reassessment.

[Required governance action]

---

# 27. Engineering Readiness Recommendation

**Engineering Recommendation:**

[Ready for Engineering Orchestration /  
Ready subject to explicit conditions /  
Further Planning required /  
Defer pending identified condition /  
Not executable on current approved basis]

**Rationale:**  
[Recommendation rationale]

**Recommended Conditions, if any:**  
[Conditions / None]

This recommendation is advisory and does not itself constitute the
Execution Readiness Decision unless the recommending authority
independently possesses and explicitly exercises the applicable decision
authority.

---

# Execution Readiness Record

> Complete this section when the Engineering Delivery Plan is submitted
> for, or receives, an Execution Readiness Decision.

# 28. Execution Readiness Submission

**Plan Revision Submitted:**  
[Revision]

**Submitted By:**  
[Actor]

**Submission Date:**  
[Date]

**Execution Readiness Authority:**  
[Authority]

**Supporting Decision Material:**  
[References / None]

---

# 29. Execution Readiness Decision

**Decision:**

[Authorize / Return / Defer / Reject]

**Decision Authority:**  
[Authority]

**Decision Date:**  
[Date]

**Decision Rationale:**  
[Rationale]

**Decision Record Reference:**  
[Reference]


## 29.1 Authorize

If `Authorize`:

**Authorized Engineering Delivery Plan Revision:**  
[Revision]

**Authorization Conditions:**  
[Conditions / None]

**Authorization Effective From:**  
[Date / condition]

Engineering Orchestration may begin within the governed Execution
Baseline and applicable authority.


## 29.2 Return

If `Return`:

**Required Planning Corrections:**  
[Corrections]

**Required Reassessment / Resubmission:**  
[Requirements]


## 29.3 Defer

If `Defer`:

**Reason for Deferral:**  
[Reason]

**Required Condition / Trigger for Reconsideration:**  
[Condition / trigger]


## 29.4 Reject

If `Reject`:

**Reason for Rejection:**  
[Reason]

**Governance Consequence / Required Next Action:**  
[Consequence / action]

Decision history SHALL be preserved.

---

# 30. Execution Baseline

> Complete this section when the Execution Readiness Decision is
> `Authorize`.

**Execution Baseline ID:**  
[Stable identifier where applicable]

**Authorized Engineering Delivery Plan Revision:**  
[Revision]

**Execution Readiness Decision:**  
[Decision reference]

**Approved Investment Baseline:**  
[Reference]

**Authorization Conditions:**  
[Conditions / None]


## 30.1 Authorized Engineering Slice Structure

| Slice ID | Slice Name | Authorized State / Reference | Slice-specific Authorization Conditions |
|---|---|---|---|
| [ID] | [Name] | [Reference] | [Conditions / None] |

Slice-specific Authorization Conditions SHALL identify conditions
attached to realization of a particular Engineering Slice.

A Slice-specific condition does not establish a separate Execution
Readiness Decision for that Slice.

The Engineering Delivery Plan remains governed by the Plan-level
Execution Readiness Decision.

Where a Slice-specific Authorization Condition prevents realization of
the affected Slice until a condition is satisfied, Engineering
Orchestration SHALL preserve and enforce that condition.


## 30.2 Applicable Delivery Tolerances

[Reference Section 21 / external governed source]


## 30.3 Carried-forward Execution Uncertainty

[Reference Section 20 / None]


## 30.4 Unresolved Architectural Obligations

[Reference Section 8.4 / None]


## 30.5 Carried-forward Planning Obligations

Identify Planning Obligations intentionally carried into Engineering
Orchestration.

| Planning Obligation | Affected Slice(s) / Area | Required Resolution Point | Owner |
|---|---|---|---|
| [Obligation] | [Slice(s) / area] | [Point] | [Owner] |

If none:

`None.`

Carried-forward Planning Obligations SHALL remain governed execution
obligations until they are satisfied, superseded, rendered immaterial,
escalated, or otherwise dispositioned through applicable Engineering
governance.


## 30.6 Reassessment Triggers

[Reference Section 22]


## 30.7 Other Material Execution Obligations

[Obligations / None]


## 30.8 Execution Baseline Statement

The Execution Baseline preserves the approved investment basis and the
executable realization basis authorized through Execution Readiness.

The Execution Baseline includes, as applicable:

- the authorized Engineering Delivery Plan revision;
- Execution Readiness Decision;
- Plan-level Authorization Conditions;
- Slice-specific Authorization Conditions;
- Approved Investment Baseline;
- authorized Engineering Slice structure;
- applicable Delivery Tolerances;
- carried-forward execution uncertainty;
- unresolved architectural obligations;
- carried-forward Planning Obligations;
- reassessment triggers; and
- other material execution obligations.

Engineering Orchestration may progressively elaborate low-level
execution detail within this baseline and applicable tolerances.

Engineering Orchestration SHALL preserve applicable Plan-level and
Slice-specific Authorization Conditions.

Carried-forward Planning Obligations SHALL remain visible until
explicitly satisfied, superseded, rendered immaterial, escalated, or
otherwise governed.

Material execution learning that invalidates this baseline SHALL trigger
governed reassessment rather than silent rewriting of the historical
authorization basis.

---

# 31. Revision History

| Revision | Date | Author / Actor | Material Change | Governance Consequence |
|---|---|---|---|---|
| [Revision] | [Date] | [Actor] | [Change] | [None / Revalidation / Reassessment / Other] |

Material revision history SHOULD be preserved according to the
Engineering Artifact Model Specification.

Once an Engineering Delivery Plan revision has been authorized, later
revision SHALL NOT rewrite or obscure the historical Plan revision on
which Execution Readiness was established.

---

# 32. Template Guidance

This template represents the governed Engineering Delivery Plan.

It SHALL be applied proportionately.

A small, familiar, low-risk realization may require:

- one Engineering Slice;
- concise Slice detail;
- simple sequencing;
- lightweight dependency representation;
- concise validation and acceptance strategies;
- limited evidence requirements;
- straightforward resource planning;
- a simple delivery timeline; and
- few material risks or uncertainties.

A large, uncertain, architecturally significant, operationally sensitive,
or dependency-heavy realization may require substantially greater detail.

The template SHALL NOT be expanded merely to create an appearance of
planning completeness.

The Plan SHALL contain enough information to support a defensible
Execution Readiness Decision.

The Plan is not a task backlog.

The Plan is not a sprint plan.

The Plan is not a substitute for source-control, issue-tracking,
scheduling, testing, CI/CD, observability, or other operational systems.

Those systems MAY operationalize the Plan.

Their representations SHALL NOT silently redefine governed Engineering
semantics.

Engineering Delivery Planning establishes the executable basis.

An `Authorize` Execution Readiness Decision establishes the governed
Execution Baseline.

Engineering Orchestration subsequently realizes that basis.