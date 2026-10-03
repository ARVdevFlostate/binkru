# Engineering Delivery Proposal Template

## Template Purpose

This template defines the standard structure for an Engineering Delivery
Proposal.

An Engineering Delivery Proposal establishes the Engineering investment
proposition for realizing an Engineering-ready Epic.

The completed proposal should provide sufficient Engineering understanding
for the applicable authority to make a defensible Investment Decision
without requiring execution-level detail that belongs to Engineering
Delivery Planning.

The template should be applied proportionately.

Sections that are not applicable MAY be marked accordingly rather than
populated with artificial content.


# Engineering Delivery Proposal

## 1. Proposal Identity

**Proposal ID:**  
[Stable identifier]

**Proposal Title:**  
[Concise descriptive title]

**Project:**  
[Project identifier or name]

**Engineering-ready Epic:**  
[Stable identifier and reference]

**Proposal Revision:**  
[Revision identifier]

**Proposal State:**  
[Current governed state]

**Proposal Owner:**  
[Governed owner responsible for maintaining the Proposal]

**Prepared By:**  
[Actor or actors contributing to proposal development]

**Prepared Date:**  
[Date]

**Last Revised:**  
[Date]


## 2. Executive Engineering Proposition

### Engineering Proposition

[Summarize the Engineering proposition for realizing the
Engineering-ready Epic.

State what Engineering proposes to realize and the overall technical
direction at a level appropriate to an Investment Decision.]

### Investment Summary

**Technical Feasibility:**  
[Established / Conditional / Further Investigation Required /
Materially Uncertain / Not Established]

**Indicative Effort:**  
[Range, order-of-magnitude assessment, bounded estimate, or other
appropriate representation]

**Indicative Cost:**  
[Cost range or Not Applicable]

**Indicative Delivery Range:**  
[Delivery range or Not Applicable]

**Engineering Confidence:**  
[Applicable confidence representation]

**Engineering Recommendation:**  
[Proceed / Proceed Subject to Conditions / Further Work Required /
Reconsider Later / Do Not Proceed]

### Material Decision Considerations

[Summarize the most significant matters the Investment Decision authority
should understand.

Include only considerations material to the investment proposition, such
as major uncertainty, architectural implications, dependencies,
assumptions, risks, capability constraints, or external obligations.]


## 3. Governed Engineering Intent

### Intended Capability

[Summarize the capability Engineering is expected to realize based on the
Engineering-ready Epic.]

### Acceptance Basis

[Summarize or reference the governed acceptance expectations relevant to
Engineering realization.]

### Quality Expectations

[Identify material quality expectations relevant to the proposition.]

### Governing Constraints

[Identify material constraints inherited from the Engineering-ready Epic
or other governed upstream artifacts.]

### Upstream Traceability

[Reference material Product and Collaboration artifacts necessary to
understand the governed intent.]

Engineering interpretation in this section SHALL preserve the governed
meaning of the Engineering-ready Epic rather than redefine upstream
intent.


## 4. Proposed Realization

### Realization Approach

[Describe the proposed Engineering realization approach.

Explain the overall technical direction and why the approach is considered
credible.]

### Affected Engineering Areas

[Identify major systems, subsystems, components, services, infrastructure,
data areas, integration surfaces, operational areas, or other Engineering
areas expected to be affected.]

### Significant Technical Implications

[Describe material technical implications, which may include:

- integration;
- data or state;
- infrastructure;
- deployment;
- migration;
- security;
- operations;
- performance;
- reliability;
- scalability; or
- maintainability.]

### Existing Capability Reuse

[Identify significant existing capabilities expected to be reused,
extended, replaced, or otherwise affected.]

### Candidate Realization Areas

[Optional.

Identify likely realization areas or candidate increments only where they
materially improve understanding of the investment proposition.

Do not perform detailed Engineering Slice decomposition here.]


## 5. Technical Feasibility

### Feasibility Assessment

[Explain whether and why the proposed realization appears technically
feasible within known constraints.]

### Feasibility Conditions

[Identify conditions on which feasibility depends.

Use Not Applicable where feasibility is not conditional.]

### Material Technical Unknowns

[Identify technical unknowns that materially affect feasibility or
investment confidence.]

### Feasibility Evidence

[Reference Engineering Evidence, discovery outputs, existing system
evidence, prior implementations, or other information supporting the
assessment.]


## 6. Engineering Discovery

### Discovery Performed

[Describe bounded Engineering discovery performed to establish
decision-relevant knowledge.

Examples may include:

- codebase analysis;
- technical investigation;
- architecture exploration;
- dependency analysis;
- integration investigation;
- technology evaluation;
- prototype;
- proof of concept;
- spike;
- performance exploration;
- security investigation; or
- operational investigation.]

### Material Findings

[Summarize findings that materially affect the Engineering proposition.]

### Discovery Outputs

[Reference material Supporting Engineering Artifacts or Engineering
Evidence produced during discovery.]

### Remaining Discovery

[Identify additional discovery required before or after the Investment
Decision and explain why it can or cannot be carried forward.]

Proposal-stage discovery establishes knowledge.

It does not authorize production realization.


## 7. Alternatives and Trade-offs

### Alternatives Considered

[Describe materially credible alternative realization approaches.

Use Not Applicable where no meaningful alternative exists.]

### Material Trade-offs

[For each material alternative, summarize significant advantages,
disadvantages, risks, costs, reversibility, operational implications, or
other relevant trade-offs.]

### Preferred Approach

[Explain why the proposed realization approach is preferred.]

### Alternative Uncertainty

[Identify uncertainty that materially affects comparison between
alternatives.]


## 8. Architecture

### Applicable Architecture Decisions

[Reference existing Accepted Architecture Decision Records that govern or
materially affect the proposed realization.]

### New Architecture Decisions

[Reference new Architecture Decision Records created or resolved during
Proposal.]

### Unresolved Architecture Decisions

[Identify material architectural decisions intentionally remaining
unresolved.]

For each material unresolved decision, identify:

- why resolution is not presently required;
- potential consequence;
- effect on investment confidence; and
- expected resolution point or condition.

### Architecture Exceptions

[Identify any known or anticipated architectural exception requiring
governance.

Use Not Applicable where none exists.]

A preferred technical approach described in this Proposal does not itself
constitute an Architecture Decision Record.


## 9. Dependencies and Constraints

### Material Dependencies

| Dependency | Type | Current State | Engineering Impact | Required By / Trigger |
|---|---|---|---|---|
| [Dependency] | [Internal / External / Platform / Vendor / Data / etc.] | [State] | [Impact] | [Point or condition] |

### Material Constraints

| Constraint | Source | Engineering Consequence |
|---|---|---|
| [Constraint] | [Source] | [Consequence] |

### Dependency Assumptions

[Identify assumptions being made about dependencies where those
assumptions materially affect the proposition.]


## 10. Engineering Capability and Resource Needs

### Required Capabilities

[Identify material Engineering capabilities required to realize the
Epic.]

### Capability Availability

[Describe known availability of required capabilities.]

### Capability Gaps

[Identify significant capability gaps, specialist needs, or external
sourcing requirements.]

### Resource Constraints

[Identify material resource constraints relevant to investment
feasibility.]

Detailed resource allocation belongs to Engineering Delivery Planning.


## 11. Effort, Cost, and Delivery Assessment

### Indicative Effort

**Assessment:**  
[Range / order-of-magnitude / bounded estimate / other representation]

**Basis:**  
[Explain the basis of the assessment.]

**Material Assumptions:**  
[Reference applicable assumptions.]

**Confidence:**  
[Applicable confidence representation]


### Indicative Cost

**Assessment:**  
[Cost range or Not Applicable]

**Included Cost Areas:**  
[Engineering labor, infrastructure, tooling, external services, hardware,
specialist expertise, migration, or other material cost areas.]

**Basis:**  
[Explain the basis of the assessment.]

**Material Assumptions:**  
[Reference applicable assumptions.]

**Confidence:**  
[Applicable confidence representation]


### Indicative Delivery Range

**Assessment:**  
[Delivery range or Not Applicable]

**Basis:**  
[Explain the basis of the assessment.]

**Material Assumptions:**  
[Reference applicable assumptions.]

**Confidence:**  
[Applicable confidence representation]

Proposal-stage assessments SHALL communicate uncertainty honestly and
SHALL NOT imply execution-level precision unsupported by the available
Engineering analysis.


## 12. Material Assumptions

| ID | Assumption | Basis / Evidence | Consequence if Invalid | Validation Approach | Required Resolution Point / Condition |
|---|---|---|---|---|---|
| A-01 | [Assumption] | [Basis] | [Consequence] | [Approach] | [Point / condition] |

Assumptions SHALL NOT be represented as established facts.


## 13. Material Uncertainty

| ID | Uncertainty | Potential Consequence | Current Understanding | Carry Forward? | Required Resolution Point / Condition |
|---|---|---|---|---|---|
| U-01 | [Uncertainty] | [Consequence] | [Understanding] | [Yes / No] | [Point / condition] |

### Uncertainty Assessment

[Explain why any material unresolved uncertainty being carried forward
does not prevent a defensible Investment Decision.]

Known unresolved uncertainty may be carried forward where its consequence
is sufficiently understood and applicable risk remains acceptable to the
Investment Decision authority.


## 14. Engineering Risks

| ID | Engineering Risk | Potential Consequence | Mitigation / Reduction Approach | Decision Significance | Residual Concern |
|---|---|---|---|---|---|
| R-01 | [Risk] | [Consequence] | [Approach] | [Significance] | [Residual concern] |

### Overall Risk Assessment

[Summarize the Engineering risk profile relevant to the Investment
Decision.

Do not turn the Proposal into a comprehensive execution risk register.]


## 15. Issues and Blockers

### Current Issues

[Identify material Engineering issues that currently exist.

Use None where no material issues exist.]

### Current Blockers

[Identify conditions that prevent required progression.

Use None where no material blockers exist.]

### Required Response

[Identify additional discovery, upstream clarification, dependency
resolution, governance action, or other response required for material
issues or blockers.]


## 16. External Obligations

[Identify material external obligations affecting the Engineering
proposition.

These may include:

- security obligations;
- compliance obligations;
- contractual obligations;
- vendor constraints;
- platform constraints;
- operational obligations; or
- other externally imposed Engineering conditions.

Use Not Applicable where no material external obligation affects the
proposal.]


## 17. Supporting Engineering Evidence

| Evidence / Artifact | Purpose | Reference |
|---|---|---|
| [Evidence or artifact] | [What proposition or assessment it supports] | [Stable reference] |

Supporting evidence SHOULD be referenced rather than unnecessarily
duplicated in the Proposal.


## 18. Proposal Traceability

### Governing Artifact

**Engineering-ready Epic:**  
[Stable identifier and reference]

### Related Product and Collaboration Artifacts

[Stable references]

### Product Decision Records

[Stable references or None]

### Architecture Decision Records

[Stable references or None]

### Supporting Engineering Artifacts

[Stable references or None]

### Engineering Evidence

[Stable references or None]

### External Obligations

[Stable references or None]


## 19. Carried-forward Conditions and Obligations

[Identify material conditions, assumptions, uncertainties, decisions,
dependencies, or obligations that must remain visible if the Proposal is
Approved and progresses into Engineering Delivery Planning.]

| ID / Reference | Condition or Obligation | Why Carried Forward | Required Resolution Point / Trigger |
|---|---|---|---|
| [Reference] | [Condition] | [Reason] | [Point / trigger] |

Use None where no material condition or obligation must be carried
forward.


## 20. Engineering Recommendation

### Recommendation

[Select and explain one of the following:

- Proceed into Engineering Delivery Planning;
- Proceed subject to identified conditions;
- Further Engineering work is required before Investment Decision;
- Reconsider after identified dependency or uncertainty is resolved; or
- Do not proceed on the current Engineering basis.]

### Recommendation Rationale

[Explain the Engineering basis for the recommendation.

Relate the recommendation to feasibility, realization approach,
architecture, effort, cost, delivery range, assumptions, uncertainty,
dependencies, capability needs, risks, and supporting evidence as
applicable.]

### Recommended Conditions

[Identify conditions Engineering recommends attaching to progression.

Use None where unconditional progression is recommended.]

The Engineering recommendation is advisory and does not itself constitute
the Investment Decision.


## 21. Proposal Readiness

### Readiness Assessment

**Ready for Investment Decision:**  
[Yes / No]

### Readiness Basis

[Explain why sufficient Engineering understanding exists—or does not yet
exist—for a defensible Investment Decision.]

Confirm that material:

- feasibility has been assessed;
- realization approach is credible;
- architectural implications are understood sufficiently;
- dependencies and constraints are visible;
- capability needs are understood sufficiently;
- effort is assessed;
- cost is assessed where relevant;
- delivery range is assessed where relevant;
- assumptions are explicit;
- risks are explicit;
- uncertainty is explicit;
- carried-forward uncertainty is defensible;
- supporting evidence is available where material; and
- an Engineering recommendation has been established.

Proposal readiness does not require elimination of every Engineering
unknown.


## 22. Investment Decision

This section records the governed Investment Decision.

It SHALL be completed only by, or under the authority of, the applicable
Investment Decision authority.

### Decision

**Outcome:**  
[Approve / Return / Defer / Reject]

**Decision Authority:**  
[Governed authority]

**Decision Date:**  
[Date]

### Decision Rationale

[Record the basis of the Investment Decision.]

### Decision Conditions

[Record conditions attached to an Approve outcome.

Use None where no conditions apply.]

### Return Requirements

[For Return, identify required proposal work before resubmission.

Use Not Applicable for other outcomes.]

### Deferral Trigger

[For Defer, identify the meaningful reconsideration trigger where
practical.

Use Not Applicable for other outcomes.]

### Rejection Basis

[For Reject, record the material basis of rejection.

Use Not Applicable for other outcomes.]


## 23. Approved Investment Baseline

Complete this section when the Investment Decision outcome is Approve.

**Approved Proposal Revision:**  
[Revision]

**Approval Date:**  
[Date]

**Investment Decision Reference:**  
[Stable reference]

### Approved Basis

[Summarize or reference the Engineering proposition, indicative
investment basis, and material assumptions approved by the Investment
Decision.]

### Approved Conditions

[Reference or record conditions attached to the Approve Investment
Decision.

Use None where approval is unconditional.]

### Carried-forward Uncertainty

[Reference material unresolved uncertainty explicitly accepted as part of
the approved investment basis.

Use None where no material uncertainty is intentionally carried forward.]

### Planning Obligations

[Identify conditions, uncertainties, assumptions, dependencies, or other
obligations that Engineering Delivery Planning must preserve or resolve.]

The Approved Proposal revision establishes the governed investment
baseline.

Subsequent Engineering learning SHALL NOT rewrite the historical basis on
which the Investment Decision was made.

Material learning that invalidates or changes this basis requires
reassessment through applicable Engineering governance.


## 24. Revision History

| Revision | Date | Actor | Change Summary | Governance Significance |
|---|---|---|---|---|
| [Revision] | [Date] | [Actor] | [Summary] | [Significance] |

Material revision history SHALL preserve the evolution of the Proposal.

Once Approved, the approved Proposal revision SHALL remain identifiable as
the governed investment baseline even where later governed reassessment
establishes a changed basis.