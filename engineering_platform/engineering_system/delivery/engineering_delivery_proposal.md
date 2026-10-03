# Engineering Delivery Proposal

## 1. Purpose

The Engineering Delivery Proposal process establishes a defensible
Engineering proposition for realizing an Engineering-ready Epic before
detailed Engineering Delivery Planning begins.

The process determines whether Engineering has sufficient understanding
of the proposed realization to support an Investment Decision.

It transforms an Engineering-ready Epic into an Engineering Delivery
Proposal that explains:

- what Engineering is being asked to realize;
- the proposed realization approach;
- whether the realization appears technically feasible;
- material architectural implications;
- material engineering risks and uncertainties;
- significant dependencies and constraints;
- required engineering capabilities and resources;
- indicative effort, cost, and delivery range;
- material assumptions; and
- the basis on which Engineering recommends proceeding, revising,
  deferring, or not proceeding.

The Engineering Delivery Proposal is an investment-facing Engineering
artifact.

It establishes a credible basis for deciding whether Engineering should
proceed into detailed Delivery Planning.

It is not an Engineering Delivery Plan and SHALL NOT attempt to provide
execution-level certainty before sufficient planning has occurred.


## 2. Process Position

Engineering Delivery Proposal is the first Engineering-native realization
process after an Epic becomes Engineering-ready.

The lifecycle position is:

    Product System
        ↓
    Draft Epic
        ↓
    Collaboration System
        ↓
    Engineering-ready Epic
        ↓
    ─────────────────────────────
          Engineering System
    ─────────────────────────────
        ↓
    Engineering Delivery Proposal
        ↓
    Investment Decision
        ↓
    Engineering Delivery Planning
        ↓
    Engineering Delivery Plan
        ↓
    Execution Readiness Decision
        ↓
    Engineering Orchestration

The Engineering-ready Epic establishes the governed intent that
Engineering is expected to realize.

The Engineering Delivery Proposal establishes whether there is a credible
Engineering proposition for realizing that intent.

The Engineering Delivery Plan subsequently establishes how an approved
Engineering proposition will be executed.


## 3. Process Objective

The objective of Engineering Delivery Proposal is to reduce sufficient
Engineering uncertainty to support a responsible Investment Decision.

The process SHALL establish enough understanding to answer:

- What are we proposing to build from an Engineering perspective?
- Is the Engineering-ready Epic technically realizable?
- What realization approach is proposed?
- What material architectural decisions or investigations are apparent?
- What significant engineering risks exist?
- What assumptions materially affect the proposition?
- What dependencies or constraints could materially affect realization?
- What engineering capabilities and resources appear necessary?
- What indicative effort, cost, and delivery range should the
  investment authority understand?
- How confident is Engineering in those ranges and assumptions?
- What material uncertainty remains?
- Is the proposition sufficiently credible to justify detailed Delivery
  Planning?

The process SHALL NOT create artificial certainty where the available
Engineering information does not support it.


## 4. Inputs

The primary governed input is:

- Engineering-ready Epic.

Additional inputs MAY include:

- Product artifacts traceable through the Engineering-ready Epic;
- Collaboration artifacts and records;
- applicable Product Decision Records;
- applicable Development Standards and other governed organizational Engineering constraints;
- existing Accepted Architecture Decision Records;
- relevant project architecture;
- existing platform or system constraints;
- known technical debt;
- prior Engineering Evidence;
- operational constraints;
- security or compliance obligations;
- external system or vendor constraints;
- known delivery dependencies;
- engineering capability information;
- historical delivery information;
- relevant project context; and
- other information necessary to evaluate the proposed realization.

Supporting inputs SHALL NOT silently override the governed intent of the
Engineering-ready Epic.


## 5. Preconditions

Engineering Delivery Proposal SHOULD begin when:

- an Engineering-ready Epic exists;
- the Epic has completed the applicable Collaboration transition;
- its governed intent and acceptance basis are sufficiently clear for
  Engineering analysis;
- material known constraints are available;
- relevant project context can be accessed; and
- Engineering has authority to perform proposal analysis.

The process MAY begin with unresolved Engineering uncertainty.

The existence of uncertainty is not itself a reason to prevent proposal
work.

Where the Engineering-ready Epic is materially insufficient to support
meaningful proposal analysis, Engineering SHALL identify the deficiency
and use the applicable upstream governance mechanism rather than silently
inventing missing Product or Collaboration intent.


## 6. Proposal Principle

The Engineering Delivery Proposal SHALL describe a credible Engineering
proposition rather than a detailed execution commitment.

Proposal analysis SHOULD seek the minimum sufficient depth required to
support the Investment Decision.

The proposal SHOULD progressively reduce material uncertainty while
avoiding detailed planning work whose value depends on the investment
being approved.

The appropriate depth of proposal analysis SHALL be proportionate to:

- investment significance;
- engineering complexity;
- architectural significance;
- uncertainty;
- delivery risk;
- operational impact;
- reversibility;
- external obligations; and
- cost of further analysis.


## 7. Engineering Interpretation

Engineering SHALL begin by establishing its understanding of the
Engineering-ready Epic.

Engineering interpretation SHOULD identify:

- intended capability;
- governed acceptance expectations;
- relevant quality expectations;
- known constraints;
- integration expectations;
- operational expectations;
- external obligations;
- assumptions inherited from upstream artifacts;
- dependencies visible at Engineering entry; and
- areas requiring Engineering clarification.

Engineering interpretation SHALL preserve the governed meaning of the
Engineering-ready Epic.

Engineering SHALL NOT reinterpret upstream intent merely to simplify the
implementation.


## 8. Realization Framing

Engineering SHALL frame the proposed realization at sufficient depth to
support feasibility, investment, risk, and architectural analysis.

Realization framing MAY identify:

- major technical areas involved;
- affected systems or subsystems;
- new components or capabilities;
- existing components likely to change;
- integration surfaces;
- data implications;
- infrastructure implications;
- deployment implications;
- operational implications;
- migration implications;
- security implications; and
- significant technical dependencies.

Realization framing is not Engineering Slice decomposition.

The proposal MAY identify likely realization areas or candidate
increments where they materially improve understanding, but detailed
Engineering Slice decomposition belongs to Engineering Delivery
Planning.


## 9. Technical Feasibility

Engineering SHALL assess whether the Engineering-ready Epic appears
technically realizable within the known constraints.

Feasibility analysis SHOULD consider, as applicable:

- available technology;
- existing architecture;
- integration feasibility;
- data feasibility;
- infrastructure feasibility;
- operational feasibility;
- security constraints;
- performance expectations;
- reliability expectations;
- scalability expectations;
- maintainability implications;
- deployment constraints;
- migration constraints;
- external dependencies;
- required engineering capabilities; and
- material technical unknowns.

Feasibility MAY be:

- established with sufficient confidence;
- conditional on explicit assumptions;
- dependent on further investigation;
- materially uncertain; or
- not established.

Engineering SHALL represent feasibility uncertainty explicitly.


## 10. Engineering Discovery

Engineering MAY perform bounded discovery where additional information is
necessary to establish proposal credibility.

Discovery MAY include:

- technical investigation;
- architecture exploration;
- codebase analysis;
- dependency analysis;
- integration investigation;
- technology evaluation;
- proof of concept;
- prototype;
- spike;
- performance exploration;
- security investigation;
- operational investigation;
- vendor or platform investigation; or
- other bounded technical analysis.

Discovery SHALL be proportionate to the Investment Decision being
supported.

Proposal discovery SHOULD reduce decision-relevant uncertainty.

Proposal-stage discovery is authorized to establish decision-relevant
knowledge.

It is not authorization to realize production scope.

Discovery SHALL NOT become ungoverned implementation of the
Engineering-ready Epic.

Discovery output MAY subsequently contribute to implementation where its
reuse is explicitly incorporated into the approved Engineering Delivery
Plan and the output satisfies the applicable:

- implementation obligations;
- validation obligations;
- architectural obligations;
- security obligations;
- operational obligations;
- evidence obligations; and
- acceptance obligations.

The technical reusability of discovery output SHALL NOT retroactively
convert proposal-stage discovery into authorized Engineering
Orchestration.

Where discovery activity begins to materially realize production scope
rather than establish proposal knowledge, the activity SHALL stop or be
governed through the applicable Engineering lifecycle and authority.


## 11. Discovery Outputs

Material discovery results SHALL be preserved where they affect:

- feasibility;
- realization approach;
- architectural direction;
- assumptions;
- dependencies;
- risks;
- estimates;
- investment significance; or
- later Engineering Delivery Planning.

Discovery outputs MAY be preserved as Supporting Engineering Artifacts or
Engineering Evidence according to the Engineering Artifact Model
Specification.

The Engineering Delivery Proposal SHOULD reference material discovery
outputs rather than unnecessarily duplicating their full contents.


## 12. Realization Approach

The Engineering Delivery Proposal SHALL describe the proposed realization
approach at a level appropriate to the Investment Decision.

The realization approach SHOULD explain, as applicable:

- the overall technical direction;
- significant affected areas;
- expected integration approach;
- significant data or state implications;
- infrastructure implications;
- deployment or migration approach;
- major implementation constraints;
- relevant reuse or extension of existing capabilities;
- significant new engineering capability; and
- material alternatives considered.

The proposal SHALL explain why the proposed approach is credible.

It SHOULD NOT contain execution-level task decomposition that properly
belongs to the Engineering Delivery Plan.


## 13. Alternatives

Materially credible realization alternatives SHOULD be considered where
they could significantly affect:

- investment;
- architecture;
- risk;
- delivery range;
- operational characteristics;
- reversibility;
- maintainability;
- external dependency; or
- strategic Engineering direction.

Alternative analysis SHALL be proportionate.

The proposal does not require artificial alternatives where there is only
one reasonable realization path.

Where alternatives are materially relevant, the proposal SHOULD identify:

- the alternatives considered;
- significant advantages and disadvantages;
- material trade-offs;
- reasons for the preferred approach; and
- uncertainty affecting the comparison.


## 14. Architecture Analysis

Engineering SHALL identify material architectural implications of the
proposed realization.

Architecture analysis SHOULD determine:

- which existing Accepted ADRs apply;
- whether the proposal conforms to those decisions;
- whether a new material architectural decision appears necessary;
- whether an existing ADR may require reassessment;
- whether an architectural exception may be required; and
- whether architectural uncertainty materially affects the investment
  proposition.

Material architectural decisions SHALL be governed according to the
Architecture Decision Specification.

The Engineering Delivery Proposal SHALL NOT silently establish a material
architectural decision merely by describing a preferred technical
approach.


## 15. Architectural Decision Timing

A material architectural decision MAY be required during Proposal,
Delivery Planning, or Engineering Orchestration depending on when the
decision becomes necessary.

An architectural decision SHOULD be resolved during Proposal where it
materially affects:

- technical feasibility;
- investment viability;
- major cost or effort range;
- delivery range;
- significant risk;
- fundamental realization approach; or
- the credibility of the Investment Decision.

Architectural decisions that do not materially affect the Investment
Decision MAY remain for later lifecycle stages where sufficient
decision-making context exists.

The proposal SHALL identify material unresolved architectural decisions
that remain relevant to the Investment Decision.


## 16. Dependencies and Constraints

Engineering SHALL identify dependencies and constraints that materially
affect the proposed realization.

These MAY include:

- upstream Product dependencies;
- cross-Epic dependencies;
- internal Engineering dependencies;
- shared platform dependencies;
- infrastructure dependencies;
- external service dependencies;
- vendor dependencies;
- organizational dependencies;
- data dependencies;
- environment dependencies;
- security or compliance constraints;
- operational constraints;
- resource constraints;
- contractual constraints; and
- timing constraints.

The proposal SHOULD distinguish known dependencies from assumptions about
dependencies where that distinction affects investment confidence.


## 17. Engineering Capability and Resource Needs

The proposal SHALL identify the engineering capabilities materially
required to realize the Epic.

Capability needs MAY include:

- software engineering disciplines;
- architecture expertise;
- platform expertise;
- infrastructure or operations expertise;
- security expertise;
- data expertise;
- domain expertise;
- quality engineering;
- specialized technical knowledge;
- external vendor capability; and
- other material engineering competencies.

Where relevant, the proposal SHOULD identify:

- capability availability;
- significant capability gaps;
- external sourcing requirements;
- resource constraints; and
- dependencies on scarce or shared expertise.

Proposal-stage resource analysis SHOULD establish investment feasibility.

Detailed resource allocation belongs to Engineering Delivery Planning or
the applicable execution-management mechanism.


## 18. Effort Assessment

The Engineering Delivery Proposal SHALL provide an effort assessment
appropriate to the maturity of proposal understanding.

Effort SHOULD normally be represented as:

- a range;
- an order-of-magnitude assessment;
- a bounded estimate; or
- another representation that communicates uncertainty honestly.

The proposal SHALL identify material assumptions underlying the effort
assessment.

Effort SHALL NOT be represented with precision unsupported by the
available Engineering analysis.


## 19. Cost Assessment

Where cost is relevant to the Investment Decision, the proposal SHALL
provide an indicative Engineering cost basis.

Cost MAY include, as applicable:

- Engineering labor;
- external engineering services;
- infrastructure;
- environments;
- tooling;
- third-party services;
- licenses;
- hardware;
- migration;
- specialist expertise; and
- other material realization costs.

Cost SHOULD be expressed with uncertainty appropriate to proposal
maturity.

Detailed budget control or procurement execution is outside the purpose
of the Engineering Delivery Proposal unless explicitly required by
applicable organizational governance.


## 20. Delivery Range

The Engineering Delivery Proposal SHALL provide an indicative delivery
range where delivery timing is material to the Investment Decision.

The range SHOULD be based on available Engineering understanding,
including:

- realization complexity;
- likely implementation scope;
- dependencies;
- capability availability;
- uncertainty;
- architectural work;
- validation needs;
- operational work;
- migration needs; and
- material risks.

Proposal-stage delivery range SHALL NOT be treated as the committed
Engineering Delivery Plan timeline.

Detailed sequencing, Slice planning, and executable scheduling belong to
Engineering Delivery Planning.


## 21. Basis of Estimate

Material effort, cost, and delivery assessments SHOULD identify their
basis.

The basis MAY include:

- analogous prior work;
- engineering judgment;
- codebase analysis;
- technical discovery;
- historical project information;
- dependency estimates;
- vendor information;
- prototype or proof-of-concept evidence;
- parametric estimation;
- range analysis; or
- another defensible estimation method.

Where multiple estimation methods materially improve confidence,
Engineering MAY use them together.

The purpose of the basis is to make the estimate explainable rather than
to create false mathematical precision.


## 22. Confidence and Uncertainty

The proposal SHALL communicate material uncertainty associated with its
engineering assessments.

Uncertainty MAY concern:

- feasibility;
- architecture;
- implementation complexity;
- dependencies;
- external systems;
- resource availability;
- effort;
- cost;
- delivery timing;
- operational behavior;
- validation; or
- another material factor.

Engineering SHOULD communicate confidence in a manner appropriate to the
organization and project.

The Engineering Platform MAY define reusable confidence semantics.

Projects MAY specialize confidence representations where permitted by
applicable governance.

A proposal SHALL NOT conceal uncertainty merely to make an Investment
Decision easier.

Not all material uncertainty must be resolved before an Investment
Decision.

Known unresolved uncertainty MAY be carried forward where:

- the uncertainty is explicitly identified;
- its potential consequence is sufficiently understood;
- carrying it forward does not prevent a defensible Investment Decision;
- applicable risk remains acceptable to the decision authority; and
- the point or condition by which resolution is required is identified
  where practical.

Where unresolved uncertainty prevents a defensible Investment Decision,
Engineering SHOULD perform additional discovery or the proposal SHOULD
receive an applicable Return, Defer, or Reject outcome.


## 23. Assumptions

Material assumptions SHALL be explicit.

An assumption is material where its invalidation could significantly
change:

- feasibility;
- realization approach;
- architecture;
- effort;
- cost;
- delivery range;
- risk;
- dependency structure; or
- investment viability.

Material assumptions SHOULD identify, where practical:

- the assumption;
- why it is currently necessary;
- evidence supporting it;
- consequence if invalid;
- validation approach; and
- point by which validation is required.

Assumptions SHALL NOT be presented as established facts.


## 24. Engineering Risks

The proposal SHALL identify material Engineering risks relevant to the
Investment Decision.

Risks MAY concern:

- feasibility;
- architecture;
- integration;
- technology;
- data;
- infrastructure;
- security;
- operations;
- performance;
- reliability;
- scalability;
- maintainability;
- migration;
- dependencies;
- resources;
- capability;
- cost;
- delivery timing;
- external services; or
- another material Engineering concern.

Material risks SHOULD identify:

- risk description;
- potential consequence;
- relevant uncertainty;
- proposed mitigation or reduction approach;
- decision significance; and
- residual concern where known.

The proposal SHOULD focus on risks that materially affect the investment
proposition rather than becoming a comprehensive execution risk register.


## 25. Issues and Blockers

Known issues or blockers that materially affect proposal credibility SHALL
be identified.

The proposal SHOULD distinguish:

- a risk that may occur;
- an issue that currently exists;
- a blocker that prevents required progression; and
- an assumption used because information is not yet established.

A material blocker MAY require Return, Defer, Reject, upstream escalation,
additional discovery, or another governed response.


## 26. Product and Collaboration Boundary

Engineering Delivery Proposal SHALL preserve the Product and
Collaboration governance boundaries.

Engineering MAY identify that the Engineering-ready Epic contains a
condition that:

- is technically infeasible;
- creates disproportionate engineering consequences;
- conflicts with an external obligation;
- depends on unavailable capability;
- materially changes the expected investment; or
- requires reconsideration of upstream intent.

Engineering SHALL NOT silently alter the Engineering-ready Epic to resolve
such a condition.

The condition SHALL be escalated through the applicable upstream
governance mechanism with sufficient Engineering evidence to support
reconsideration.


## 27. Proposal Traceability

The Engineering Delivery Proposal SHALL be traceable to its governing
Engineering-ready Epic.

The proposal SHOULD also preserve relationships to material:

- Product artifacts;
- Collaboration artifacts;
- Product Decision Records;
- Architecture Decision Records;
- discovery outputs;
- Engineering Evidence;
- dependencies;
- external obligations; and
- other supporting Engineering artifacts.

Traceability SHALL be sufficient to explain the basis of the proposed
Engineering realization and subsequent Investment Decision.


## 28. Proposal Evolution

The Engineering Delivery Proposal MAY evolve while proposal analysis is
in progress.

Revision MAY occur because of:

- Engineering discovery;
- clarified upstream information;
- architectural decisions;
- changed assumptions;
- dependency information;
- revised estimates;
- risk analysis;
- authority feedback; or
- other material proposal learning.

Material revision history SHOULD be preserved according to the
Engineering Artifact Model Specification.

Proposal evolution before a final Investment Decision does not require a
new artifact identity unless applicable artifact governance requires it.

Once an Engineering Delivery Proposal receives an Approve Investment
Decision, the approved proposal revision SHALL establish the governed
investment baseline.

Subsequent Engineering learning SHALL NOT rewrite the historical basis on
which the Investment Decision was made.

Later information MAY refine Engineering understanding without changing
the approved investment baseline where the refinement remains within
applicable governance tolerances and preserves the approved proposition.

Where subsequent learning materially invalidates or changes the approved
investment basis, reassessment SHALL occur according to the Engineering
Governance Specification.

Where reassessment authorizes a changed investment basis, the changed
basis and resulting governed decision SHALL be preserved according to the
Engineering Artifact Model Specification and Engineering Governance
Specification.


## 29. Proposal Readiness

An Engineering Delivery Proposal is ready for Investment Decision when it
provides sufficient information for the applicable authority to make a
defensible determination.

Readiness SHOULD include:

- traceable Engineering-ready Epic scope;
- credible realization approach;
- sufficient feasibility assessment;
- material architectural implications;
- material unresolved architectural decisions;
- significant dependencies and constraints;
- required engineering capabilities;
- indicative effort;
- indicative cost where relevant;
- indicative delivery range where relevant;
- material assumptions;
- material risks;
- material uncertainty;
- relevant supporting evidence; and
- an Engineering recommendation.

Where material uncertainty remains unresolved, Proposal readiness SHOULD
also establish that:

- the uncertainty is explicitly identified;
- its potential consequence is understood sufficiently for the
  Investment Decision;
- carrying the uncertainty forward does not invalidate the investment
  proposition;
- applicable risk remains within the authority of the Investment
  Decision; and
- the point or condition by which the uncertainty should be resolved is
  identified where practical.

Proposal readiness does not require elimination of every Engineering
unknown.

It requires sufficient understanding of known material uncertainty to
support a defensible Investment Decision.

Proposal readiness SHALL be proportionate to the significance and
uncertainty of the proposed investment.


## 30. Engineering Recommendation

The proposal SHOULD provide an Engineering recommendation to the
Investment Decision authority.

The recommendation MAY indicate that Engineering believes the proposition
is:

- suitable to proceed into Delivery Planning;
- suitable to proceed subject to identified conditions;
- not yet sufficiently established and requiring further work;
- better reconsidered after a dependency or uncertainty is resolved; or
- not technically or economically credible on the current basis.

The Engineering recommendation is advisory.

It SHALL NOT be treated as the Investment Decision unless the
recommending authority independently possesses and explicitly exercises
the applicable Investment Decision authority.


## 31. Investment Decision

A proposal that is ready for decision SHALL be submitted to the applicable
Investment Decision authority.

Investment Decision governance SHALL follow the Engineering Governance
Specification.

The available governed outcomes are:

- Approve;
- Return;
- Defer; and
- Reject.

Engineering ownership or authorship of the proposal SHALL NOT by itself
confer Investment Decision authority.


## 32. Approve Outcome

Approve indicates that the Engineering proposition is authorized to
progress into Engineering Delivery Planning.

Approval MAY include explicit conditions where those conditions do not
invalidate the basis of the investment approval.

Approval of the Engineering Delivery Proposal:

- authorizes detailed Delivery Planning;
- establishes the approved Engineering investment basis;
- establishes the approved proposal revision as the governed investment
  baseline;
- preserves applicable assumptions and conditions;
- preserves material unresolved uncertainty intentionally carried
  forward; and
- provides the governing proposal basis for the Engineering Delivery
  Plan.

Approval does not:

- constitute Execution Readiness;
- authorize Engineering Orchestration;
- authorize production realization through proposal-stage discovery;
- approve every future architectural decision;
- eliminate uncertainty;
- freeze all implementation details; or
- authorize Engineering to exceed applicable governance tolerances.

Subsequent Engineering learning SHALL be evaluated against the approved
investment baseline.

Where learning refines implementation understanding without materially
changing that baseline, Engineering MAY continue according to applicable
governance.

Where learning materially invalidates or changes the baseline,
reassessment SHALL occur rather than rewriting the approved proposal
history.


## 33. Return Outcome

Return indicates that the proposal requires additional work before a
final Investment Decision can be made.

Return MAY require:

- additional Engineering analysis;
- revised realization framing;
- additional discovery;
- stronger feasibility evidence;
- architectural clarification;
- revised estimates;
- additional risk analysis;
- clarification of assumptions;
- upstream clarification; or
- another specified correction.

The Return decision SHALL identify the reason and required follow-up.

The proposal MAY be revised and resubmitted while preserving the governed
Return history.


## 34. Defer Outcome

Defer indicates that the Engineering proposition remains valid for
consideration but the Investment Decision should not presently be made.

Deferral MAY arise because of:

- unresolved dependency;
- unavailable evidence;
- external decision;
- organizational timing;
- resource availability;
- funding timing;
- upstream decision;
- architectural dependency; or
- another material condition.

The Defer decision SHOULD identify a meaningful reconsideration trigger
where practical.

Deferral SHALL NOT be interpreted as approval to begin Delivery Planning
or Engineering Orchestration unless separately authorized by applicable
governance.


## 35. Reject Outcome

Reject indicates that the Engineering proposition is not approved on its
current governed basis.

Rejection SHALL preserve:

- the rejected proposal;
- decision rationale;
- decision authority;
- material supporting evidence; and
- applicable governance history.

Rejection does not erase the Engineering analysis performed.

A materially different future proposition MAY be considered according to
the applicable Engineering Lifecycle and governance.


## 36. Conditional Approval

An Investment Decision MAY Approve a proposal with explicit conditions
where:

- the overall investment basis remains valid;
- the condition does not conceal a material feasibility deficiency;
- the condition can be satisfied within the authorized progression;
- the consequence of non-satisfaction is understood; and
- follow-up responsibility is established.

A proposal SHOULD instead be Returned or Deferred where the unresolved
condition prevents a defensible investment commitment.

Conditions SHALL remain traceable into Engineering Delivery Planning where
they affect the approved delivery basis.


## 37. Transition to Engineering Delivery Planning

An Approved Engineering Delivery Proposal becomes a governed input to
Engineering Delivery Planning.

The approved proposal revision establishes the governed investment
baseline against which subsequent Delivery Planning is performed.

Delivery Planning SHALL elaborate the approved proposition into a credible
executable basis.

Planning MAY refine:

- realization detail;
- Engineering Slice decomposition;
- sequencing;
- dependencies;
- estimates;
- resource allocation;
- validation strategy;
- acceptance approach;
- architectural work;
- delivery tolerances;
- execution risks; and
- other implementation details.

Planning SHALL preserve the approved investment basis unless authorized
change governance permits it to change.

Refinement of planning detail does not itself require revision of the
approved Proposal where the approved investment basis remains valid.

Known unresolved uncertainty intentionally carried forward from Proposal
SHALL remain visible during Delivery Planning until it is resolved,
superseded, or otherwise governed.

Where an uncertainty has a required resolution point or condition,
Delivery Planning SHALL account for that obligation in the executable
basis.

A material planning discovery that invalidates the approved proposal basis
SHALL trigger reassessment according to the Engineering Governance
Specification.

Authorized reassessment SHALL preserve the original approved investment
baseline and the governed decision establishing any changed basis.


## 38. Proposal Versus Delivery Plan

The Engineering Delivery Proposal and Engineering Delivery Plan serve
different governance purposes.

The Proposal answers:

    Should the organization invest in progressing this
    Engineering realization?

The Delivery Plan answers:

    Has Engineering established a credible executable basis
    for delivering the approved realization?

The Proposal therefore focuses on:

- feasibility;
- realization approach;
- architecture implications;
- investment;
- material dependencies;
- capabilities;
- ranges;
- uncertainty;
- assumptions; and
- material risks.

The Delivery Plan focuses on:

- Engineering Slice decomposition;
- execution sequencing;
- actionable dependencies;
- resource allocation;
- refined estimates;
- delivery timeline;
- validation;
- acceptance;
- orchestration readiness; and
- execution governance.

The Proposal SHALL NOT be made artificially detailed merely to resemble a
Delivery Plan.

The Delivery Plan SHALL NOT be used to retroactively bypass the Investment
Decision.


## 39. Proposal and Architecture Decision Records

An Engineering Delivery Proposal MAY reference zero, one, or multiple
Architecture Decision Records.

The existence of a proposal does not imply that all architecture must be
decided before investment approval.

Architecture decisions SHALL be made at the latest responsible point
consistent with:

- decision significance;
- feasibility;
- investment credibility;
- reversibility;
- uncertainty;
- dependency impact; and
- delivery needs.

Where an architectural decision materially determines whether the
proposition is viable, it SHOULD be resolved before the Investment
Decision.


## 40. Proposal and Engineering Evidence

Engineering Evidence MAY support proposal claims concerning:

- feasibility;
- architecture;
- integration;
- performance;
- operational behavior;
- technology suitability;
- dependency behavior;
- estimates;
- risk;
- security;
- migration; or
- other material Engineering concerns.

Evidence SHOULD be created or retained where it materially improves the
credibility or explainability of the Investment Decision.

Evidence SHALL NOT be produced merely to create governance ceremony.


## 41. Proposal and External Tools

External tools MAY support Engineering Delivery Proposal work.

Examples include:

- source-control platforms;
- code analysis tools;
- architecture tools;
- project-management systems;
- estimation tools;
- documentation platforms;
- modeling tools;
- prototyping environments;
- issue trackers; and
- AI engineering tools.

External tools MAY contain operational representations of proposal
information.

They SHALL NOT silently redefine:

- Engineering Delivery Proposal identity;
- governed proposal content;
- Investment Decision outcome;
- decision authority;
- proposal state; or
- traceability.

Where external representations are authoritative for specific operational
information, that authority SHALL be explicitly established by applicable
integration governance.


## 42. AI-assisted Proposal Development

AI systems MAY assist Engineering Delivery Proposal development by:

- analyzing the Engineering-ready Epic;
- inspecting relevant project artifacts;
- analyzing codebases;
- identifying technical implications;
- identifying dependencies;
- proposing realization approaches;
- comparing alternatives;
- identifying architecture concerns;
- supporting technical discovery;
- generating prototypes or proofs of concept;
- analyzing engineering risks;
- supporting estimation;
- identifying assumptions;
- evaluating uncertainty;
- checking traceability;
- identifying missing proposal information; and
- drafting or revising proposal content.

AI-generated analysis SHALL be evaluated according to its engineering
significance and the evidence supporting it.

AI assistance SHALL NOT silently redefine Product or Collaboration intent.

AI generation of an Engineering Delivery Proposal does not confer
Investment Decision authority.

AI-assisted discovery remains subject to the same boundary between
decision-relevant discovery and authorized Engineering realization.

An AI system SHALL NOT treat permission to investigate, prototype, or
produce a proof of concept as implicit authorization to realize
production scope.

An AI system MAY exercise governed authority only where explicitly
permitted under the Engineering Governance Specification.


## 43. Human, AI, and Mixed-team Operation

The Engineering Delivery Proposal process SHALL support:

- human-led Engineering teams;
- AI-assisted human teams;
- mixed human and AI-agent teams; and
- AI-led execution where applicable governance explicitly permits it.

The process semantics SHALL remain the same regardless of who or what
performs proposal analysis.

Responsibility and decision authority SHALL be determined by applicable
Engineering governance rather than inferred solely from whether the actor
is human or automated.


## 44. Proportional Application

Not every Engineering-ready Epic requires the same proposal depth.

A relatively small, familiar, low-risk Epic MAY require a concise
Engineering Delivery Proposal.

A large, uncertain, expensive, architecturally significant, or
operationally sensitive Epic MAY require substantial analysis and
supporting evidence.

Proportional application MAY vary:

- discovery depth;
- alternative analysis;
- estimate sophistication;
- evidence requirements;
- architecture analysis;
- risk analysis;
- cost analysis; and
- decision preparation.

Proportionality SHALL NOT remove information necessary for a defensible
Investment Decision.


## 45. Process Output

The primary output is:

- Engineering Delivery Proposal.

Supporting outputs MAY include:

- Architecture Decision Records;
- Engineering Evidence;
- technical discovery artifacts;
- prototypes;
- proofs of concept;
- estimates;
- analysis artifacts;
- dependency information; and
- other Supporting Engineering Artifacts.

The governance output is:

- Investment Decision.

An Approved Engineering Delivery Proposal becomes the governed input to
Engineering Delivery Planning.

The approved proposal revision establishes the governed investment
baseline for that progression.


## 46. Process Summary

Engineering Delivery Proposal can be summarized as:

    Engineering-ready Epic
            ↓
    Establish Engineering interpretation
            ↓
    Frame proposed realization
            ↓
    Assess technical feasibility
            ↓
    Identify material uncertainty
            ↓
    Bounded Engineering discovery
        where required
            ↓
    Define realization approach
            ↓
    Consider material alternatives
            ↓
    Analyze architectural implications
            ↓
    Identify dependencies and constraints
            ↓
    Identify capability and resource needs
            ↓
    Assess effort / cost / delivery range
            ↓
    Make assumptions explicit
            ↓
    Identify material Engineering risks
            ↓
    Establish confidence and evidence
            ↓
    Engineering Delivery Proposal
            ↓
    Proposal readiness
            ↓
    Investment Decision
       │       │       │       │
       │       │       │       └── Reject
       │       │       │
       │       │       └── Defer
       │       │
       │       └── Return
       │
       └── Approve
              ↓
    Establish governed
      investment baseline
              ↓
    Engineering Delivery Planning

The Engineering Delivery Proposal establishes a defensible Engineering
investment proposition.

It provides sufficient Engineering understanding to determine whether
detailed Delivery Planning is justified without pretending that detailed
planning has already occurred.

Proposal analysis is proportionate to investment significance,
engineering complexity, uncertainty, architectural impact, and risk.

Engineering MAY perform bounded discovery where necessary to reduce
decision-relevant uncertainty.

Proposal-stage discovery is authorized to establish knowledge rather than
to realize production scope.

Discovery output MAY later contribute to implementation, but only through
the governed realization lifecycle and applicable implementation,
validation, architecture, security, operational, evidence, and acceptance
obligations.

Material architectural decisions are governed through Architecture
Decision Records and are resolved during Proposal only where their
resolution is necessary for a credible Investment Decision.

Effort, cost, and delivery timing are represented with uncertainty
appropriate to proposal maturity rather than false precision.

Material uncertainty does not need to be eliminated before investment
approval where it is explicitly understood, its consequence is bounded
sufficiently for the decision, applicable risk is acceptable, and its
required resolution point or condition is identified where practical.

Where uncertainty prevents a defensible Investment Decision, additional
discovery or an applicable Return, Defer, or Reject outcome is required.

The Engineering Delivery Proposal preserves Product and Collaboration
intent and escalates upstream concerns rather than silently redefining
them.

The Engineering recommendation informs but does not replace the
Investment Decision.

Approve authorizes Engineering Delivery Planning.

It does not constitute Execution Readiness or authorize Engineering
Orchestration.

The approved Proposal revision establishes the governed investment
baseline.

Subsequent Engineering learning SHALL NOT rewrite the historical basis on
which that Investment Decision was made.

Planning MAY refine the approved proposition while the investment basis
remains valid.

Material learning that invalidates or changes the approved investment
basis triggers reassessment, with both the original basis and any
subsequently authorized basis preserved through governed history.

The approved Proposal establishes the governed investment basis from
which the Engineering Delivery Plan is subsequently developed.