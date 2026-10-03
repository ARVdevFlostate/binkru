# Engineering Delivery Proposal Checklist

## Checklist Purpose

This checklist validates whether an Engineering Delivery Proposal is
sufficiently complete, coherent, traceable, and credible to support a
defensible Investment Decision.

The checklist validates decision sufficiency rather than mechanical
completion of the Engineering Delivery Proposal Template.

A populated section does not by itself satisfy a checklist item.

Validation SHALL consider whether the information provided is meaningful,
internally consistent, appropriately evidenced, and sufficient for the
decision being requested.

The checklist SHALL be applied proportionately according to the
significance, complexity, uncertainty, architectural impact, operational
impact, and risk of the proposed Engineering realization.


# Engineering Delivery Proposal Validation Checklist

# Pre-Decision Validation

The following checks apply before an Engineering Delivery Proposal is
submitted for Investment Decision.

## 1. Proposal Identity and Governance

- [ ] The Proposal has a stable identifier.
- [ ] The Proposal identifies the project to which it belongs.
- [ ] The governing Engineering-ready Epic is explicitly identified.
- [ ] The Proposal revision is identifiable.
- [ ] The current Proposal state is identifiable.
- [ ] A governed Proposal Owner is identified.
- [ ] Proposal contributors are identifiable where required.
- [ ] Proposal ownership is not conflated with authorship or contribution.
- [ ] Proposal ownership or authorship is not treated as implicit
      Investment Decision authority.
- [ ] Material revision history is preserved where applicable.


## 2. Governed Engineering Intent

- [ ] The intended capability is derived from the Engineering-ready Epic.
- [ ] The relevant acceptance basis is understood or referenced.
- [ ] Material quality expectations are identified.
- [ ] Material upstream constraints are identified.
- [ ] Relevant Product and Collaboration traceability is preserved.
- [ ] Engineering interpretation preserves the governed meaning of the
      Engineering-ready Epic.
- [ ] The Proposal does not silently introduce, remove, or redefine
      upstream Product or Collaboration intent.
- [ ] Any material upstream deficiency or conflict requiring
      reconsideration is explicitly identified for governed escalation.


## 3. Engineering Proposition

- [ ] The Proposal clearly states what Engineering proposes to realize.
- [ ] The overall technical direction is understandable.
- [ ] The proposed realization is described at sufficient depth for an
      Investment Decision.
- [ ] The proposition is consistent with the governed Engineering intent.
- [ ] The Proposal explains why the proposed realization approach is
      credible.
- [ ] Major affected Engineering areas are identified where material.
- [ ] Significant technical implications are visible where material.
- [ ] Relevant existing capability reuse, extension, replacement, or
      impact is identified.
- [ ] Candidate realization areas, if present, improve investment
      understanding rather than prematurely performing detailed
      Engineering Slice decomposition.


## 4. Executive Decision Sufficiency

- [ ] The Executive Engineering Proposition accurately represents the
      detailed Proposal.
- [ ] Technical feasibility is summarized.
- [ ] Indicative effort is summarized.
- [ ] Indicative cost is summarized where relevant.
- [ ] Indicative delivery range is summarized where relevant.
- [ ] Engineering confidence is communicated.
- [ ] The Engineering recommendation is explicit.
- [ ] Material decision considerations are visible without requiring the
      Investment Decision authority to reconstruct them from technical
      detail.
- [ ] The executive summary does not conceal material uncertainty,
      assumptions, dependencies, risks, constraints, or conditions.


## 5. Technical Feasibility

- [ ] Technical feasibility has been explicitly assessed.
- [ ] The feasibility conclusion is supported by sufficient Engineering
      reasoning.
- [ ] Material feasibility conditions are explicit.
- [ ] Material technical unknowns are identified.
- [ ] Evidence supporting feasibility is referenced where material.
- [ ] Feasibility is not represented with greater certainty than the
      available Engineering understanding supports.
- [ ] Where feasibility remains conditional or materially uncertain, the
      consequence for the Investment Decision is understood.


## 6. Engineering Discovery

- [ ] Bounded Engineering discovery has been performed where necessary to
      establish proposal credibility.
- [ ] Discovery performed is relevant to decision-significant
      uncertainty.
- [ ] Material discovery findings are reflected in the Proposal.
- [ ] Material discovery outputs are preserved or referenced where
      appropriate.
- [ ] Remaining discovery is identified where material.
- [ ] The Proposal explains whether remaining discovery must occur before
      the Investment Decision or may responsibly be carried forward.
- [ ] Proposal-stage discovery has remained bounded to establishing
      decision-relevant knowledge.
- [ ] Discovery activity has not been used to bypass authorization for
      production realization.
- [ ] Any discovery output proposed for later production use remains
      subject to applicable implementation, validation, architecture,
      security, operational, evidence, and acceptance obligations.


## 7. Alternatives and Trade-offs

- [ ] Materially credible alternatives have been considered where they
      could significantly affect the investment proposition.
- [ ] Artificial alternatives have not been introduced merely to satisfy
      documentation structure.
- [ ] Material trade-offs between relevant alternatives are understood.
- [ ] The preferred realization approach is justified.
- [ ] Material uncertainty affecting alternative comparison is explicit.
- [ ] Alternative analysis is proportionate to the significance and
      reversibility of the decision.


## 8. Architecture

- [ ] Applicable Accepted Architecture Decision Records are identified.
- [ ] The proposed realization is assessed against applicable
      architectural decisions.
- [ ] Material new architectural decisions are identified where required.
- [ ] Material architectural decisions resolved during Proposal are
      governed through Architecture Decision Records.
- [ ] A preferred technical approach in the Proposal is not treated as an
      implicit architectural decision.
- [ ] Material unresolved architectural decisions are explicitly
      identified.
- [ ] The reason for carrying each material unresolved architectural
      decision forward is understood.
- [ ] The potential consequence of unresolved architectural decisions is
      understood sufficiently for the Investment Decision.
- [ ] Expected resolution points or conditions are identified where
      practical.
- [ ] Known or anticipated architecture exceptions are identified where
      applicable.


## 9. Dependencies and Constraints

- [ ] Material Engineering dependencies are identified.
- [ ] Material constraints are identified.
- [ ] The source or nature of material constraints is understood.
- [ ] Engineering consequences of material dependencies and constraints
      are understood.
- [ ] Known dependencies are distinguishable from assumptions about
      dependencies where material.
- [ ] Required dependency resolution points or triggers are identified
      where practical.
- [ ] External dependencies that could materially affect investment
      credibility are visible.


## 10. Engineering Capability and Resources

- [ ] Material Engineering capabilities required for realization are
      identified.
- [ ] Capability availability is understood sufficiently for investment
      assessment.
- [ ] Significant capability gaps are identified.
- [ ] Specialist or external sourcing requirements are identified where
      material.
- [ ] Material resource constraints are visible.
- [ ] Resource analysis is sufficient to assess investment feasibility.
- [ ] The Proposal does not imply detailed resource allocation that
      properly belongs to Engineering Delivery Planning.


## 11. Effort Assessment

- [ ] Indicative Engineering effort is assessed.
- [ ] The effort representation is appropriate to Proposal maturity.
- [ ] The effort assessment has an identifiable basis.
- [ ] Material assumptions affecting effort are explicit or referenced.
- [ ] Confidence in the effort assessment is communicated.
- [ ] The effort assessment does not imply precision unsupported by
      available Engineering analysis.
- [ ] Material uncertainty affecting effort is visible.


## 12. Cost Assessment

Where cost is relevant to the Investment Decision:

- [ ] Indicative Engineering cost is assessed.
- [ ] Material cost areas are included or explicitly excluded as
      appropriate.
- [ ] The cost assessment has an identifiable basis.
- [ ] Material assumptions affecting cost are explicit or referenced.
- [ ] Confidence in the cost assessment is communicated.
- [ ] The cost assessment communicates uncertainty appropriately.
- [ ] Material cost exposure not represented in the headline assessment
      is explicitly visible.

Where cost is not relevant:

- [ ] The Proposal explicitly identifies the cost assessment as not
      applicable rather than silently omitting it.


## 13. Delivery Range

Where delivery timing is relevant to the Investment Decision:

- [ ] An indicative delivery range is provided.
- [ ] The delivery range has an identifiable Engineering basis.
- [ ] Material assumptions affecting the range are explicit or
      referenced.
- [ ] Confidence in the delivery range is communicated.
- [ ] Material timing uncertainty is visible.
- [ ] The delivery range accounts for significant known dependencies,
      architectural work, validation, operational work, migration, and
      other material factors where applicable.
- [ ] The Proposal does not represent the indicative delivery range as a
      committed execution schedule.

Where delivery timing is not relevant:

- [ ] The Proposal explicitly identifies the delivery range as not
      applicable rather than silently omitting it.


## 14. Basis of Estimate

- [ ] Material effort, cost, and delivery assessments have an explainable
      basis.
- [ ] Estimation methods are appropriate to the available information.
- [ ] Relevant Engineering discovery or evidence is incorporated where
      it materially affects estimates.
- [ ] Historical or analogous information is used responsibly where
      applicable.
- [ ] Estimates can be traced to the assumptions and information on which
      they depend.
- [ ] Estimate precision does not exceed the maturity of Engineering
      understanding.
- [ ] The Proposal enables an Investment Decision authority to understand
      why Engineering believes the stated ranges are credible.


## 15. Material Assumptions

- [ ] Material assumptions are explicitly identified.
- [ ] Assumptions are not represented as established facts.
- [ ] The basis or evidence for material assumptions is identified where
      practical.
- [ ] The consequence of invalidating each material assumption is
      understood.
- [ ] Validation approaches are identified where appropriate.
- [ ] Required resolution points or conditions are identified where
      practical.
- [ ] Assumptions affecting feasibility, architecture, effort, cost,
      delivery range, risk, dependencies, or investment viability are not
      silently embedded in narrative text.


## 16. Material Uncertainty

- [ ] Material Engineering uncertainty is explicitly identified.
- [ ] The potential consequence of material uncertainty is understood
      sufficiently for the Investment Decision.
- [ ] The Proposal distinguishes unresolved uncertainty from assumptions,
      risks, issues, and blockers.
- [ ] Uncertainty is not concealed to make the investment proposition
      appear more certain.
- [ ] Material uncertainty proposed for carry-forward is explicitly
      identified.
- [ ] The rationale for carrying material uncertainty forward is
      defensible.
- [ ] Applicable risk associated with carried-forward uncertainty is
      within the authority of the Investment Decision.
- [ ] Required resolution points or conditions are identified where
      practical.
- [ ] Any uncertainty preventing a defensible Investment Decision has
      resulted in additional discovery or an appropriate recommendation
      rather than being silently carried forward.


## 17. Engineering Risks

- [ ] Material Engineering risks relevant to the Investment Decision are
      identified.
- [ ] Potential consequences are understood.
- [ ] Mitigation or uncertainty-reduction approaches are identified where
      appropriate.
- [ ] Decision significance is understood.
- [ ] Residual concern is visible where known.
- [ ] Risks are not confused with assumptions, known issues, blockers, or
      unresolved uncertainty.
- [ ] The Proposal focuses on investment-significant Engineering risks
      rather than attempting to become a comprehensive execution risk
      register.


## 18. Issues and Blockers

- [ ] Material current Engineering issues are explicitly identified.
- [ ] Material blockers are explicitly identified.
- [ ] Issues and blockers are distinguishable from risks and assumptions.
- [ ] Required responses are identified.
- [ ] A blocker preventing responsible progression is not concealed by an
      optimistic Engineering recommendation.
- [ ] Where a blocker requires upstream clarification, additional
      discovery, dependency resolution, Return, Defer, Reject, or other
      governance action, that requirement is visible.


## 19. External Obligations

- [ ] Material external obligations affecting the Engineering proposition
      are identified.
- [ ] Relevant security obligations are represented where applicable.
- [ ] Relevant compliance obligations are represented where applicable.
- [ ] Relevant contractual, vendor, platform, or operational obligations
      are represented where applicable.
- [ ] Engineering consequences of material external obligations are
      understood.
- [ ] External obligations are reflected in feasibility, estimates,
      uncertainty, risks, or planning obligations where they materially
      affect those areas.


## 20. Supporting Engineering Evidence

- [ ] Material Engineering claims are supported by evidence where
      evidence is necessary for proposal credibility.
- [ ] Supporting Engineering Evidence is identifiable and traceable.
- [ ] Discovery evidence is preserved where it materially affects the
      proposition.
- [ ] Evidence is referenced rather than unnecessarily duplicated.
- [ ] The Proposal does not create evidence merely to satisfy governance
      ceremony.
- [ ] Evidence quality is proportionate to the significance of the claim
      being supported.


## 21. Traceability

- [ ] The Proposal is traceable to the governing Engineering-ready Epic.
- [ ] Material Product and Collaboration artifacts are traceable where
      required.
- [ ] Applicable Product Decision Records are referenced where material.
- [ ] Applicable Architecture Decision Records are referenced.
- [ ] Supporting Engineering Artifacts are referenced where material.
- [ ] Engineering Evidence is referenced where material.
- [ ] Material external obligations are traceable where applicable.
- [ ] Traceability is sufficient to explain the basis of the Engineering
      proposition and subsequent Investment Decision.


## 22. Carried-forward Conditions and Obligations

- [ ] Material conditions that must survive Proposal approval are
      explicitly identified.
- [ ] Material assumptions requiring later validation are carried forward
      where applicable.
- [ ] Material unresolved uncertainty accepted for later resolution is
      carried forward.
- [ ] Material unresolved architectural decisions are carried forward
      where applicable.
- [ ] Material dependencies requiring later action are carried forward.
- [ ] External or governance obligations requiring later action are
      carried forward.
- [ ] Each material carried-forward item has a reason for being carried
      forward.
- [ ] Required resolution points, conditions, or triggers are identified
      where practical.
- [ ] The carried-forward set provides a usable handoff into Engineering
      Delivery Planning rather than requiring Planning to rediscover
      material Proposal obligations.


## 23. Engineering Recommendation

- [ ] An explicit Engineering recommendation is provided.
- [ ] The recommendation is supported by the Proposal analysis.
- [ ] The recommendation is consistent with the stated feasibility,
      uncertainty, assumptions, risks, dependencies, estimates, and
      evidence.
- [ ] Recommended conditions are explicit where progression is
      conditional.
- [ ] Engineering does not recommend unconditional progression where
      unresolved conditions materially prevent a defensible investment.
- [ ] The Engineering recommendation is represented as advisory.
- [ ] The recommendation is not represented as the Investment Decision
      unless the actor independently holds and explicitly exercises the
      applicable governed authority.


## 24. Proposal Readiness

- [ ] The Proposal contains sufficient Engineering understanding for the
      applicable authority to make a defensible Investment Decision.
- [ ] The realization approach is credible.
- [ ] Technical feasibility has been assessed sufficiently.
- [ ] Material architectural implications are understood sufficiently.
- [ ] Material dependencies and constraints are visible.
- [ ] Engineering capability needs are understood sufficiently.
- [ ] Indicative effort is available.
- [ ] Indicative cost is available where relevant.
- [ ] Indicative delivery range is available where relevant.
- [ ] Material assumptions are explicit.
- [ ] Material risks are explicit.
- [ ] Material uncertainty is explicit.
- [ ] Material carried-forward uncertainty is defensible.
- [ ] Relevant supporting evidence is available where material.
- [ ] An Engineering recommendation has been established.
- [ ] Remaining unknowns do not prevent a defensible Investment Decision.
- [ ] The depth of Proposal analysis is proportionate to the significance
      and uncertainty of the proposed investment.


## 25. Proposal-versus-Plan Boundary

- [ ] The Proposal establishes a credible Engineering investment
      proposition rather than an execution plan.
- [ ] Detailed Engineering Slice decomposition has not been performed
      prematurely.
- [ ] Detailed execution sequencing has not been treated as a Proposal
      requirement.
- [ ] Detailed resource allocation has not been treated as a Proposal
      requirement.
- [ ] Proposal-stage delivery ranges are not represented as committed
      execution schedules.
- [ ] The Proposal contains sufficient realization detail to support the
      Investment Decision without requiring execution-level certainty.
- [ ] Information properly belonging to Engineering Delivery Planning has
      not been introduced merely to make the Proposal appear more
      complete.


## 26. Internal Consistency

- [ ] The Executive Engineering Proposition is consistent with the
      detailed analysis.
- [ ] The feasibility assessment is consistent with the recommendation.
- [ ] Effort, cost, and delivery assessments are consistent with the
      identified realization approach.
- [ ] Estimates are consistent with material dependencies and capability
      constraints.
- [ ] Material assumptions are reflected where they affect estimates or
      feasibility.
- [ ] Material uncertainty is reflected in confidence and recommendation.
- [ ] Material risks are reflected in the decision considerations where
      appropriate.
- [ ] Carried-forward obligations are consistent with the Proposal's
      detailed analysis.
- [ ] No section materially contradicts another without the discrepancy
      being explicitly explained.


## 27. Proportionality

- [ ] Proposal depth is proportionate to investment significance.
- [ ] Proposal depth is proportionate to Engineering complexity.
- [ ] Proposal depth is proportionate to architectural significance.
- [ ] Proposal depth is proportionate to material uncertainty.
- [ ] Proposal depth is proportionate to operational impact and delivery
      risk.
- [ ] Analysis has not been omitted where it is necessary for a
      defensible decision.
- [ ] Unnecessary analysis has not been introduced solely to satisfy
      process ceremony.


## 28. Human, AI, and Mixed-team Integrity

Where AI systems or agents contributed to Proposal development:

- [ ] AI-generated analysis has been evaluated according to its
      Engineering significance.
- [ ] Material AI-generated claims are supported by appropriate evidence
      or Engineering reasoning.
- [ ] AI assistance has not silently redefined Product or Collaboration
      intent.
- [ ] AI-assisted discovery has respected the discovery-versus-realization
      boundary.
- [ ] AI generation of Proposal content has not been interpreted as
      conferring Proposal ownership or Investment Decision authority.
- [ ] Any authority exercised by an AI system is explicitly permitted by
      applicable Engineering governance.

For all team compositions:

- [ ] Responsibility and authority are determined by governance rather
      than inferred solely from whether an actor is human or automated.


## 29. Investment Decision Readiness

Before submitting the Proposal for Investment Decision:

- [ ] The Proposal has completed applicable validation.
- [ ] Material validation failures have been resolved or explicitly
      represented.
- [ ] The Proposal Owner considers the artifact ready for governed
      decision.
- [ ] The applicable Investment Decision authority is identifiable.
- [ ] The decision being requested is clear.
- [ ] Any recommended conditions are explicit.
- [ ] Material carried-forward uncertainty is visible.
- [ ] Material planning obligations that would arise from approval are
      visible.
- [ ] The authority can reasonably choose among Approve, Return, Defer,
      and Reject using the information provided.


# Post-Decision Validation

The following checks apply after an Investment Decision has been recorded.


## 30. Investment Decision Record

- [ ] The governed outcome is recorded as Approve, Return, Defer, or
      Reject.
- [ ] The applicable Decision Authority is recorded.
- [ ] The Decision Date is recorded.
- [ ] Decision rationale is preserved.
- [ ] Decision conditions are recorded where applicable.
- [ ] The recorded decision is distinguishable from the Engineering
      recommendation.


## 31. Approve Outcome

Where the outcome is Approve:

- [ ] The approved Proposal revision is identifiable.
- [ ] The approval date is identifiable.
- [ ] The Investment Decision reference is preserved.
- [ ] The Approved Basis is explicit.
- [ ] Approved Conditions are explicit or recorded as None.
- [ ] Material Carried-forward Uncertainty is explicit or recorded as
      None.
- [ ] Planning Obligations are explicit.
- [ ] The approved Proposal revision establishes the governed investment
      baseline.
- [ ] Approval is not interpreted as Execution Readiness.
- [ ] Approval is not interpreted as authorization for Engineering
      Orchestration.
- [ ] Approval is not interpreted as eliminating all Engineering
      uncertainty.
- [ ] Approval is not interpreted as freezing implementation detail that
      properly belongs to Delivery Planning.


## 32. Return Outcome

Where the outcome is Return:

- [ ] The reason for Return is explicit.
- [ ] Required follow-up work is explicit.
- [ ] The Proposal can be revised without losing the governed Return
      history.
- [ ] Resubmission does not silently erase the prior decision.


## 33. Defer Outcome

Where the outcome is Defer:

- [ ] The basis for deferral is explicit.
- [ ] A meaningful reconsideration trigger is identified where practical.
- [ ] Deferral is not interpreted as authorization to begin Engineering
      Delivery Planning or Engineering Orchestration unless separately
      authorized.


## 34. Reject Outcome

Where the outcome is Reject:

- [ ] The rejected Proposal is preserved.
- [ ] Rejection rationale is preserved.
- [ ] Decision authority is preserved.
- [ ] Material supporting evidence remains traceable.
- [ ] Rejection does not erase Engineering analysis or governance
      history.
- [ ] Any materially different future proposition will enter applicable
      Engineering governance rather than silently replacing the rejected
      basis.


## 35. Approved Investment Baseline Integrity

Where the Proposal is Approved:

- [ ] The exact approved Proposal revision remains identifiable.
- [ ] The historical basis of the Investment Decision is preserved.
- [ ] Subsequent Engineering learning does not rewrite the approved
      Proposal history.
- [ ] Refinement within the approved investment basis is distinguishable
      from material change to that basis.
- [ ] Material learning that invalidates or changes the approved basis
      triggers applicable reassessment.
- [ ] Where reassessment establishes a changed basis, both the original
      approved baseline and the subsequently authorized basis remain
      traceable.


## 36. Transition to Engineering Delivery Planning

Where the Proposal is Approved:

- [ ] The Approved Engineering Delivery Proposal is available as a
      governed input to Engineering Delivery Planning.
- [ ] The Approved Investment Baseline is identifiable.
- [ ] Approved Conditions are visible to Delivery Planning.
- [ ] Material Carried-forward Uncertainty is visible to Delivery
      Planning.
- [ ] Planning Obligations are visible to Delivery Planning.
- [ ] Required resolution points or triggers are preserved.
- [ ] Delivery Planning can elaborate the approved proposition without
      reconstructing the Investment Decision basis from unrelated
      artifacts.
- [ ] Any known condition requiring reassessment before or during Planning
      is explicit.


# Validation Outcome

## 37. Validation Result

**Checklist Result:**  
[Pass / Pass with Conditions / Fail]

**Validated Proposal Revision:**  
[Revision]

**Validated By:**  
[Actor or governed validation mechanism]

**Validation Date:**  
[Date]

### Validation Findings

[Summarize material findings.]

### Conditions

[Identify conditions associated with a Pass with Conditions result.

Use None where not applicable.]

### Required Corrections

[Identify corrections required for a Fail result.

Use None where not applicable.]


## 38. Validation Interpretation

### Pass

Pass indicates that the Engineering Delivery Proposal is sufficiently
complete, coherent, traceable, and credible to proceed to the applicable
Investment Decision.

Pass does not constitute the Investment Decision.


### Pass with Conditions

Pass with Conditions indicates that the Proposal is sufficiently credible
to proceed to Investment Decision while identified validation conditions
remain explicit.

A validation condition SHALL NOT be used to conceal a deficiency that
prevents a defensible Investment Decision.

The Investment Decision authority remains responsible for determining
whether the Proposal should be Approved, Returned, Deferred, or Rejected.


### Fail

Fail indicates that the Proposal contains one or more material
deficiencies that prevent responsible progression to Investment Decision.

Failure SHOULD identify the deficient areas and required correction.

A failed validation does not erase the Proposal or its revision history.


## 39. Checklist Summary

An Engineering Delivery Proposal is validation-ready when it demonstrates
that:

    governed Engineering intent is understood
                ↓
    a credible realization approach exists
                ↓
    technical feasibility is sufficiently established
                ↓
    material architecture implications are understood
                ↓
    dependencies and constraints are visible
                ↓
    capability needs are understood
                ↓
    effort / cost / delivery ranges have defensible bases
                ↓
    assumptions are explicit
                ↓
    uncertainty is explicit
                ↓
    risks, issues, and blockers are distinguished
                ↓
    supporting evidence is available where material
                ↓
    carried-forward obligations are explicit
                ↓
    Engineering recommendation is defensible
                ↓
    Proposal is internally coherent
                ↓
    Investment Decision can be made responsibly

The checklist validates the quality and decision sufficiency of the
Engineering Delivery Proposal.

It does not require every Engineering unknown to be eliminated.

It does not convert indicative Proposal estimates into Delivery Plan
commitments.

It does not authorize Engineering Orchestration.

It does not replace the Investment Decision.

Where the Proposal is Approved, post-decision validation confirms that the
approved Proposal revision, decision conditions, carried-forward
uncertainty, and Planning obligations establish a preserved and usable
governed investment baseline for Engineering Delivery Planning.