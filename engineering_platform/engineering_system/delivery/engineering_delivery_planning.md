# Engineering Delivery Planning

## 1. Purpose

The Engineering Delivery Planning process establishes a credible,
executable Engineering basis for realizing an Approved Engineering
Delivery Proposal.

The process transforms the approved Engineering investment proposition
into an Engineering Delivery Plan that explains:

- how the approved realization will be decomposed;
- what Engineering realization units will be delivered;
- how those units relate to the governing Epic;
- how realization will be sequenced;
- how dependencies will be managed;
- what architectural work must occur;
- how implementation will be validated;
- how Engineering acceptance will be established;
- what evidence must be produced;
- what engineering capabilities and resources are required;
- what delivery timeline is credible;
- what execution risks and uncertainties remain;
- how approved conditions and carried-forward obligations will be
  satisfied; and
- whether Engineering has established a sufficiently credible basis to
  request Execution Readiness.

Engineering Delivery Planning is not Engineering Orchestration.

Planning establishes the governed executable basis.

Engineering Orchestration subsequently realizes that basis.


## 2. Process Position

Engineering Delivery Planning begins after an Engineering Delivery
Proposal receives an Approve Investment Decision.

The lifecycle position is:

    Product System
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
    Engineering Orchestration

The Approved Engineering Delivery Proposal establishes the governed
investment basis.

Engineering Delivery Planning elaborates that approved basis into a
credible executable Engineering basis.

The Engineering Delivery Plan becomes the governed basis submitted for
Execution Readiness Decision.


## 3. Process Objective

The objective of Engineering Delivery Planning is to reduce sufficient
execution uncertainty to determine whether Engineering is ready to begin
governed realization.

The process SHALL establish enough understanding to answer:

- What Engineering realization must occur?
- Into what coherent Engineering units should realization be decomposed?
- How does each realization unit contribute to the governing Epic?
- In what sequence can or should realization occur?
- Which realization units may proceed independently or concurrently?
- What dependencies constrain execution?
- What architectural decisions or obligations must be resolved?
- What implementation, validation, evidence, and acceptance obligations
  apply?
- What engineering capabilities and resources are required?
- What delivery timeline is credible?
- What execution risks remain?
- What approved assumptions, conditions, uncertainties, and obligations
  must be preserved or resolved?
- What tolerances govern execution?
- What changes would require reassessment?
- Is the resulting Engineering Delivery Plan sufficiently credible to
  authorize Engineering Orchestration?

Planning SHALL establish executable credibility without pretending that
execution itself is completely predictable.


## 4. Governed Inputs

The primary governed inputs are:

- Approved Engineering Delivery Proposal;
- Approved Investment Baseline; and
- governing Engineering-ready Epic.

The Approved Investment Baseline SHOULD provide or reference:

- Approved Basis;
- Approved Conditions;
- material assumptions;
- Carried-forward Uncertainty;
- Planning Obligations; and
- applicable resolution points or triggers.

Additional inputs MAY include:

- Architecture Decision Records;
- Engineering Evidence;
- Supporting Engineering Artifacts;
- Product artifacts;
- Collaboration artifacts;
- Product Decision Records;
- existing project architecture;
- applicable Development Standards;
- platform constraints;
- operational requirements;
- security or compliance obligations;
- resource and capability information;
- external dependencies;
- historical delivery information;
- applicable organizational constraints; and
- other information necessary to establish the executable basis.

Supporting inputs SHALL NOT silently override the Approved Investment
Baseline or governed intent of the Engineering-ready Epic.


## 5. Preconditions

Engineering Delivery Planning SHOULD begin when:

- the Engineering Delivery Proposal has received an Approve Investment
  Decision;
- the approved Proposal revision is identifiable;
- the Approved Investment Baseline is identifiable;
- Approved Conditions are visible;
- material Carried-forward Uncertainty is visible;
- Planning Obligations are visible;
- applicable resolution points or triggers are available;
- the governing Engineering-ready Epic remains traceable; and
- Engineering has authority to perform Delivery Planning.

Planning MAY begin with unresolved Engineering uncertainty.

Uncertainty that was intentionally accepted by the Investment Decision
does not itself prevent Planning.

Where a condition required before Planning has not been satisfied,
Engineering SHALL use the applicable governance mechanism rather than
silently proceeding.


## 6. Planning Principle

Engineering Delivery Planning SHALL elaborate the approved proposition
rather than redesign the investment proposition without governance.

Planning SHOULD progressively reduce execution-relevant uncertainty.

The depth of Planning SHALL be sufficient to establish a credible
executable basis while remaining proportionate to:

- realization complexity;
- architectural significance;
- uncertainty;
- dependency complexity;
- delivery risk;
- operational impact;
- security significance;
- reversibility;
- resource constraints;
- external obligations; and
- cost of additional planning.

Planning SHALL NOT require every implementation detail to be known before
Engineering Orchestration begins.

Detail MAY be progressively elaborated during governed realization where
the remaining uncertainty falls within applicable authority and
tolerances.


## 7. Preservation of the Approved Investment Basis

Engineering Delivery Planning SHALL preserve the Approved Investment
Baseline.

Planning MAY refine:

- realization detail;
- decomposition;
- sequencing;
- dependencies;
- estimates;
- resource allocation;
- validation strategy;
- acceptance approach;
- architecture work;
- delivery timeline;
- execution risks; and
- implementation detail.

Such refinement does not itself change the approved investment basis.

Planning SHALL NOT silently change:

- governed Epic intent;
- approved realization basis;
- material investment scope;
- Approved Conditions;
- accepted material assumptions;
- accepted material uncertainty;
- material external obligations; or
- another element whose change materially affects the Investment
  Decision.

Where Planning discovers information that materially invalidates or
changes the Approved Investment Baseline, reassessment SHALL occur
according to the Engineering Governance Specification.

The historical approved basis SHALL remain preserved.


## 8. Planning Interpretation

Engineering SHALL establish its Planning interpretation of the approved
proposition.

Planning interpretation SHOULD identify:

- approved realization scope;
- intended Engineering outcome;
- applicable acceptance expectations;
- material quality expectations;
- Approved Conditions;
- carried-forward assumptions;
- carried-forward uncertainty;
- Planning Obligations;
- applicable architectural decisions;
- dependencies;
- external obligations;
- execution constraints; and
- required resolution points or triggers.

Planning interpretation SHALL remain traceable to the Approved Investment
Baseline and governing Engineering-ready Epic.


## 9. Engineering Slice

Engineering Delivery Planning SHALL establish a coherent Engineering
Slice structure for the approved realization.

The primary governed realization unit is the Engineering Slice.

An Engineering Slice is a bounded, traceable unit of Engineering
realization that can be meaningfully planned, implemented, validated,
evidenced, and accepted within Engineering Orchestration.

An Engineering Slice SHOULD:

- have a clear realization objective;
- contribute meaningfully to the governing Epic;
- have identifiable boundaries;
- have explicit dependencies where material;
- have applicable implementation obligations;
- have applicable validation obligations;
- have applicable acceptance expectations;
- identify required Engineering Evidence where material;
- be sufficiently bounded for execution governance; and
- be traceable to its governing Engineering context.

Where the approved realization is already sufficiently bounded, coherent,
traceable, and governable, it MAY be represented as a single Engineering
Slice.

Decomposition SHALL NOT be performed solely to create multiple Slices.

An Engineering Slice is not inherently:

- a sprint;
- a user story;
- a task;
- a ticket;
- a source-control branch;
- a pull request;
- a technical component;
- a project-management work item; or
- a fixed unit of duration.

External tools MAY represent Engineering Slices using operational work
items, but those representations SHALL NOT redefine Engineering Slice
semantics.


## 10. Slice Decomposition

Where multiple Engineering Slices are appropriate, Slice decomposition
SHALL establish a realization structure appropriate to the approved
Engineering proposition.

Decomposition MAY consider:

- capability boundaries;
- technical cohesion;
- architecture boundaries;
- integration boundaries;
- dependency structure;
- validation boundaries;
- acceptance boundaries;
- operational boundaries;
- risk;
- uncertainty;
- reversibility;
- deployability;
- evidence needs; and
- opportunities for incremental realization.

A Slice SHOULD be large enough to represent meaningful Engineering
realization and small enough to remain governable.

Slice decomposition SHALL NOT be driven solely by arbitrary duration,
team structure, tooling convention, or project-management ceremony.

The appropriate number and granularity of Slices SHALL depend on the
realization being planned.

A single-Slice realization is valid where further decomposition would not
meaningfully improve execution governance, traceability, validation,
acceptance, evidence, risk management, or delivery adaptability.


## 11. Slice Traceability

Every Engineering Slice SHALL be traceable to its governing Engineering
context.

Traceability SHOULD establish relationships to, as applicable:

- Engineering-ready Epic;
- Approved Engineering Delivery Proposal;
- Approved Investment Baseline;
- relevant acceptance expectations;
- Architecture Decision Records;
- dependencies;
- Planning Obligations;
- Engineering Evidence;
- external obligations; and
- other Supporting Engineering Artifacts.

Slice traceability SHALL be sufficient to explain why the Slice exists
and what governed realization it contributes to.


## 12. Slice Boundaries

Planning SHALL establish sufficiently clear boundaries for each
Engineering Slice.

Slice boundaries SHOULD identify:

- realization objective;
- included Engineering work;
- material exclusions where necessary;
- affected systems or components;
- inputs or prerequisites;
- outputs or resulting capability;
- dependencies;
- implementation obligations;
- validation obligations;
- acceptance expectations;
- evidence obligations; and
- applicable constraints.

Boundaries SHOULD reduce ambiguity without requiring task-level
decomposition where such decomposition is unnecessary for Execution
Readiness.


## 13. Slice Independence and Coupling

Engineering SHOULD seek Slice boundaries that minimize unnecessary
coupling.

A Slice MAY depend on one or more other Slices.

A Slice MAY be independently realizable where the Engineering context
permits.

Planning SHOULD identify:

- mandatory predecessor relationships;
- optional sequencing preferences;
- shared dependencies;
- integration points;
- concurrency opportunities;
- coordination requirements; and
- coupling that creates material delivery risk.

Slice independence is desirable where practical but SHALL NOT be forced
where artificial separation would reduce technical coherence or increase
risk.


## 14. Sequencing

Engineering Delivery Planning SHALL establish a credible realization
sequence.

Sequencing MAY be:

- linear;
- parallel;
- dependency-driven;
- risk-driven;
- architecture-driven;
- capability-driven;
- evidence-driven;
- operationally constrained; or
- a combination of these.

Planning SHOULD identify:

- required ordering;
- concurrency opportunities;
- critical dependencies;
- integration points;
- decision points;
- validation points;
- acceptance points; and
- significant synchronization needs.

The Engineering Delivery Plan SHALL represent sequencing sufficiently for
Engineering Orchestration without requiring a particular project-
management methodology.


## 15. Incremental Realization

Engineering Delivery Planning SHOULD enable incremental realization where
doing so improves:

- feedback;
- risk reduction;
- evidence generation;
- validation;
- reversibility;
- integration confidence;
- operational confidence; or
- delivery adaptability.

Incremental realization does not require a specific Agile, Scrum,
waterfall, spiral, or other delivery methodology.

Engineering Orchestration MAY realize Slices iteratively, sequentially,
concurrently, or through another governed execution pattern consistent
with the Engineering Delivery Plan.

The Engineering System governs realization semantics rather than
prescribing a universal project-management methodology.


## 16. Architecture Planning

Planning SHALL identify architectural work necessary for credible
execution.

Architecture planning SHOULD determine:

- applicable Accepted ADRs;
- unresolved architectural decisions;
- architectural decisions required before specific Slices;
- architectural constraints;
- architecture exceptions;
- architecture dependencies; and
- architecture validation needs.

Material architectural decisions SHALL continue to be governed according
to the Architecture Decision Specification.

Planning SHALL NOT silently establish architecture decisions merely by
including technical choices in the Engineering Delivery Plan.


## 17. Architectural Decision Timing

Planning SHOULD resolve architectural decisions where their resolution is
necessary to establish Execution Readiness.

An architectural decision MAY remain unresolved where:

- its resolution is not necessary for credible execution authorization;
- the latest responsible decision point occurs during Orchestration;
- its potential consequences are understood;
- associated risk remains within applicable tolerances; and
- the required resolution point or condition is explicit.

An unresolved architectural decision SHALL NOT be carried into execution
where doing so would make the executable basis materially non-credible.


## 18. Dependency Planning

Planning SHALL refine dependencies to execution-relevant depth.

Dependencies MAY include:

- Slice dependencies;
- architecture dependencies;
- internal Engineering dependencies;
- platform dependencies;
- infrastructure dependencies;
- environment dependencies;
- data dependencies;
- security dependencies;
- external service dependencies;
- vendor dependencies;
- organizational dependencies;
- Product dependencies;
- cross-Epic dependencies; and
- other execution-significant dependencies.

Material dependencies SHOULD identify:

- dependency owner where applicable;
- current state;
- affected Slice or Slices;
- required availability point;
- consequence of delay or failure;
- mitigation or contingency where appropriate; and
- escalation condition where material.


## 19. Implementation Obligations

Planning SHALL establish implementation obligations necessary for
governed realization.

Implementation obligations MAY include:

- coding expectations;
- configuration requirements;
- infrastructure changes;
- data changes;
- integration work;
- migration work;
- documentation;
- security controls;
- observability;
- operational readiness work;
- deployment preparation; and
- other realization requirements.

Implementation obligations SHOULD be attached to the relevant Slice or
cross-cutting planning element.

Planning SHALL establish what must be realized without unnecessarily
prescribing every low-level implementation action.


## 20. Validation Planning

Engineering Delivery Planning SHALL establish how realized Engineering
work will be validated.

Validation planning MAY include:

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
- compatibility validation;
- manual technical validation; and
- other applicable verification mechanisms.

Validation obligations SHOULD be associated with the relevant Engineering
Slice or cross-cutting delivery concern.

Validation SHALL be sufficient to produce credible evidence that
realization satisfies its Engineering obligations.


## 21. Acceptance Planning

Planning SHALL establish how Engineering realization will be determined to
have satisfied its governed acceptance basis.

Acceptance planning SHOULD identify:

- applicable acceptance expectations;
- acceptance evidence;
- responsible acceptance authority where applicable;
- Slice-level acceptance where useful;
- integration or aggregate acceptance;
- conditions preventing acceptance; and
- required escalation where acceptance cannot be established.

Engineering acceptance SHALL remain traceable to the applicable governed
acceptance basis.

Planning SHALL NOT silently redefine upstream acceptance expectations.


## 22. Engineering Evidence Planning

Planning SHALL identify Engineering Evidence required to support material
realization claims.

Evidence MAY support:

- implementation completion;
- validation;
- architecture conformance;
- security;
- performance;
- reliability;
- operational readiness;
- migration;
- integration;
- acceptance;
- exception handling; and
- other governed Engineering claims.

Evidence requirements SHOULD be proportionate to the significance of the
claim being established.

Planning SHALL avoid evidence production whose sole purpose is governance
ceremony.


## 23. Capability and Resource Planning

Engineering Delivery Planning SHALL refine the capability and resource
needs established during Proposal.

Planning SHOULD identify, where material:

- required Engineering capabilities;
- capability availability;
- Slice ownership or execution responsibility;
- specialist involvement;
- shared capability constraints;
- external sourcing;
- environment or infrastructure capacity;
- resource dependencies; and
- material resource contention.

Resource planning SHALL be sufficient to establish executable
credibility.

The Engineering System need not prescribe a particular staffing,
capacity-planning, or project-management mechanism.


## 24. Estimate Refinement

Planning SHALL refine Proposal-stage estimates using the increased
execution understanding produced by decomposition and planning.

Refinement MAY apply to:

- effort;
- cost;
- delivery timing;
- infrastructure;
- external services;
- specialist requirements; and
- other material delivery dimensions.

Refined estimates SHOULD consider:

- Slice structure;
- sequencing;
- dependencies;
- architecture work;
- validation;
- acceptance;
- evidence;
- operational work;
- migration;
- capability availability;
- resource constraints;
- uncertainty; and
- execution risk.

Planning estimates SHALL retain an explainable basis.

Refinement SHALL NOT create unsupported precision.


## 25. Relationship to Proposal Estimates

Planning estimates MAY differ from Proposal estimates because Planning
operates with greater execution detail.

Difference alone does not imply that the Approved Investment Baseline has
changed.

Engineering SHALL assess whether estimate refinement remains within the
approved investment basis and applicable tolerances.

Where refined effort, cost, delivery timing, or another material dimension
invalidates the basis on which investment was approved, reassessment SHALL
occur according to Engineering Governance.

The Proposal estimate SHALL NOT be rewritten merely to match the refined
Plan estimate.


## 26. Delivery Timeline

The Engineering Delivery Plan SHALL establish a credible delivery
timeline where timing is relevant.

The timeline MAY represent:

- Slice sequence;
- target windows;
- milestones;
- dependency dates;
- decision points;
- validation points;
- integration points;
- acceptance points;
- release points; or
- other meaningful delivery events.

The timeline SHOULD communicate:

- ordering;
- concurrency;
- significant dependencies;
- material timing assumptions;
- uncertainty;
- and relevant constraints.

The Engineering System SHALL NOT require a particular scheduling
representation.

External planning tools MAY operationalize the timeline.


## 27. Milestones

Planning MAY establish milestones where they improve execution governance.

Milestones SHOULD represent meaningful Engineering states or events rather
than arbitrary reporting dates.

Examples MAY include:

- architecture resolution;
- environment availability;
- integration readiness;
- completion of a significant Slice group;
- migration readiness;
- validation completion;
- operational readiness;
- readiness for applicable downstream acceptance activity; or
- readiness for downstream Release consideration.

Milestones SHALL NOT replace Slice-level realization governance where
Slice governance is required.


## 28. Execution Risk Planning

Planning SHALL refine Engineering risks to execution-relevant depth.

Execution risks MAY concern:

- Slice realization;
- architecture;
- integration;
- dependencies;
- capability;
- resources;
- infrastructure;
- security;
- validation;
- acceptance;
- migration;
- operations;
- cost;
- delivery timing;
- external systems; or
- other material execution concerns.

Material execution risks SHOULD identify:

- potential consequence;
- affected Slices or delivery areas;
- mitigation;
- contingency where appropriate;
- trigger or indicator where practical;
- escalation condition; and
- residual concern.

Execution risk planning SHOULD remain proportionate.


## 29. Issues and Blockers

Known Planning-stage issues and blockers SHALL be explicit.

Planning SHOULD distinguish:

- risks;
- issues;
- blockers;
- assumptions;
- unresolved uncertainty; and
- dependencies.

A blocker preventing a credible executable basis SHALL prevent Execution
Readiness unless resolved or explicitly governed through an applicable
authority.


## 30. Assumption Refinement

Planning SHALL review material assumptions inherited from the Approved
Investment Baseline.

An assumption MAY be:

- validated;
- refined;
- superseded through governed evidence;
- retained for later validation; or
- invalidated.

Where an assumption is invalidated, Engineering SHALL assess whether the
Approved Investment Baseline remains valid.

Material Planning assumptions introduced after Proposal SHALL be explicit.

Assumptions SHALL NOT silently become facts through repetition.


## 31. Uncertainty Management

Planning SHALL identify material execution uncertainty.

Uncertainty inherited from Proposal SHALL remain visible until it is:

- resolved;
- superseded;
- accepted for later resolution;
- rendered immaterial; or
- otherwise governed.

New material uncertainty discovered during Planning SHALL be recorded.

Material uncertainty MAY be carried into Engineering Orchestration where:

- its potential consequence is sufficiently understood;
- execution remains credible;
- associated risk falls within applicable authority and tolerances;
- the required resolution point or condition is explicit where practical;
  and
- carrying the uncertainty forward does not invalidate the Approved
  Investment Baseline.

Planning SHALL NOT create artificial certainty merely to obtain Execution
Readiness.


## 32. Approved Conditions and Planning Obligations

Planning SHALL explicitly account for all Approved Conditions and Planning
Obligations inherited from the Approved Investment Baseline.

Each material item SHOULD be:

- satisfied during Planning;
- allocated to one or more Engineering Slices;
- associated with a later resolution point;
- escalated for governance; or
- otherwise explicitly dispositioned.

No material Approved Condition or Planning Obligation SHALL disappear
merely because detailed Planning has begun.


## 33. Planning Discovery

Engineering MAY perform additional bounded discovery during Delivery
Planning where required to establish executable credibility.

Planning discovery MAY include:

- implementation investigation;
- architecture investigation;
- codebase analysis;
- dependency investigation;
- integration exploration;
- prototype refinement;
- performance investigation;
- security investigation;
- operational investigation; or
- other bounded Engineering analysis.

Planning discovery SHALL establish knowledge necessary for Planning.

It SHALL NOT be used to bypass Execution Readiness and begin unauthorized
Engineering Orchestration.

Outputs MAY subsequently contribute to realization where governed
appropriately.


## 34. Delivery Tolerances

The Engineering Delivery Plan SHOULD identify applicable execution
tolerances where they are necessary to distinguish ordinary execution
variation from material change requiring governance.

Tolerances MAY concern:

- effort;
- cost;
- delivery timing;
- scope interpretation;
- dependencies;
- architecture;
- operational characteristics;
- risk;
- resource availability; or
- other material delivery dimensions.

Engineering Platform governance MAY define reusable tolerance semantics.

Projects MAY specialize tolerances where permitted.

The Delivery Plan SHALL NOT invent tolerance thresholds that exceed the
authority delegated to the project.


## 35. Change and Reassessment Triggers

Planning SHALL identify known conditions that would require reassessment
during Engineering Orchestration.

Triggers MAY include:

- material scope change;
- invalidated investment assumption;
- material estimate movement;
- critical dependency failure;
- architectural change;
- external obligation change;
- unacceptable risk increase;
- inability to satisfy acceptance;
- material resource loss;
- operational constraint change; or
- another condition defined by Engineering Governance.

Triggers SHOULD distinguish normal execution adaptation from changes that
require governed reassessment.


## 36. External Tool Representation

External tools MAY operationalize the Engineering Delivery Plan.

Examples include:

- project-management systems;
- issue trackers;
- source-control platforms;
- CI/CD systems;
- architecture tools;
- documentation platforms;
- observability systems;
- testing systems; and
- AI engineering environments.

External tools MAY represent:

- Engineering Slices;
- tasks;
- dependencies;
- schedules;
- assignments;
- milestones;
- validation activity;
- evidence links; and
- execution status.

External tools SHALL NOT silently redefine:

- Engineering Slice identity;
- governed Delivery Plan content;
- approved investment basis;
- Execution Readiness;
- decision authority;
- acceptance;
- evidence semantics; or
- change governance.

Where an external representation is authoritative for specific operational
information, that authority SHALL be explicitly established through
applicable integration governance.


## 37. Planning Traceability

The Engineering Delivery Plan SHALL preserve traceability to:

- governing Engineering-ready Epic;
- Approved Engineering Delivery Proposal;
- Approved Investment Baseline;
- Investment Decision;
- applicable Product and Collaboration artifacts;
- Architecture Decision Records;
- Engineering Slices;
- Approved Conditions;
- Planning Obligations;
- material assumptions;
- material uncertainty;
- dependencies;
- Engineering Evidence;
- external obligations; and
- other material Supporting Engineering Artifacts.

Traceability SHALL be sufficient to explain how the executable basis was
derived from the approved investment proposition.


## 38. Engineering Delivery Plan

The primary artifact produced by Engineering Delivery Planning is the
Engineering Delivery Plan.

The Engineering Delivery Plan SHOULD establish:

- Delivery Plan identity and ownership;
- governing Proposal and Epic;
- Approved Investment Baseline;
- realization strategy;
- Engineering Slice structure;
- Slice dependencies;
- realization sequencing;
- architectural obligations;
- implementation obligations;
- validation strategy;
- acceptance strategy;
- Engineering Evidence requirements;
- capability and resource allocation;
- refined estimates;
- delivery timeline;
- milestones where applicable;
- execution risks;
- assumptions;
- unresolved uncertainty;
- Approved Conditions;
- Planning Obligations;
- delivery tolerances;
- reassessment triggers;
- external obligations; and
- supporting traceability.

The Plan SHALL contain sufficient information to support an Execution
Readiness Decision without requiring every low-level execution task to be
predefined.


## 39. Plan Evolution

The Engineering Delivery Plan MAY evolve while Delivery Planning is in
progress.

Revision MAY occur because of:

- Planning discovery;
- Slice decomposition or refinement;
- architecture decisions;
- dependency refinement;
- estimate refinement;
- resource information;
- validation planning;
- risk analysis;
- assumption validation;
- uncertainty reduction; or
- other material Planning learning.

Material revision history SHOULD be preserved according to the
Engineering Artifact Model Specification.

Before Execution Readiness authorization, Planning revisions MAY continue
within applicable governance.

Once an Engineering Delivery Plan receives an Authorize Execution
Readiness Decision, the authorized Plan revision SHALL contribute to the
governed Execution Baseline.

Subsequent execution learning SHALL NOT rewrite the historical basis on
which Execution Readiness was established.


## 40. Plan Readiness

An Engineering Delivery Plan is ready for Execution Readiness Decision
when it establishes a sufficiently credible executable basis.

Readiness SHOULD include:

- preserved Approved Investment Baseline;
- a coherent Engineering Slice structure, including a single Slice where
  further decomposition is unnecessary;
- sufficient Slice boundaries;
- actionable dependencies;
- credible sequencing;
- applicable architecture obligations;
- implementation obligations;
- validation strategy;
- acceptance strategy;
- evidence requirements;
- sufficient capability and resource planning;
- refined estimates;
- credible delivery timeline where relevant;
- material execution risks;
- explicit assumptions;
- explicit unresolved uncertainty;
- disposition of Approved Conditions and Planning Obligations;
- applicable delivery tolerances;
- reassessment triggers; and
- sufficient traceability.

Plan readiness does not require elimination of every execution unknown.

It requires sufficient understanding to determine that governed
Engineering Orchestration can begin responsibly.


## 41. Engineering Readiness Recommendation

Engineering SHOULD provide a recommendation concerning Execution
Readiness.

The recommendation MAY indicate that the Plan is:

- ready for Engineering Orchestration;
- ready subject to explicit conditions;
- not yet sufficiently established and requiring further Planning;
- better deferred until an identified dependency or uncertainty is
  resolved; or
- not executable on the current approved basis.

The Engineering recommendation is advisory.

It SHALL NOT itself constitute the Execution Readiness Decision unless the
recommending authority independently possesses and explicitly exercises
the applicable decision authority.


## 42. Execution Readiness Decision

A Plan that is ready for decision SHALL be submitted to the applicable
Execution Readiness authority.

Execution Readiness governance SHALL follow the Engineering Governance
Specification.

The governed outcomes are:

- Authorize;
- Return;
- Defer; or
- Reject.

Authorize establishes that Engineering may begin Engineering
Orchestration subject to:

- the authorized Engineering Delivery Plan;
- Approved Investment Baseline;
- applicable authorization conditions;
- delivery tolerances;
- reassessment triggers;
- architectural governance;
- acceptance obligations; and
- other applicable Engineering governance.

Execution Readiness does not eliminate execution uncertainty.

Authorize does not imply that every implementation detail is fixed.

Authorize establishes permission to begin governed realization within the
authorized execution basis.


## 43. Return, Defer, and Reject

Where the Execution Readiness Decision results in Return, Defer, or
Reject, the applicable Engineering Governance Specification SHALL govern
the outcome.

Return MAY require:

- further decomposition;
- dependency resolution;
- architecture work;
- estimate refinement;
- resource clarification;
- validation planning;
- acceptance clarification;
- risk reduction;
- uncertainty reduction; or
- another specified Planning correction.

Defer MAY apply where the Plan remains potentially executable but a
material condition prevents responsible authorization at the present
time.

Reject MAY apply where the executable basis is not acceptable on its
current governed basis.

Decision history SHALL be preserved.


## 44. Execution Baseline and Transition to Engineering Orchestration

An Engineering Delivery Plan receiving an Authorize Execution Readiness
Decision establishes the governed basis for transition to Engineering
Orchestration.

The governed Execution Baseline SHOULD identify or preserve:

- authorized Engineering Delivery Plan revision;
- Execution Readiness Decision;
- applicable authorization conditions;
- Approved Investment Baseline;
- Engineering Slice structure;
- delivery tolerances;
- unresolved uncertainty intentionally carried into Orchestration;
- unresolved architectural obligations;
- reassessment triggers; and
- other execution obligations material to governed realization.

The Execution Baseline therefore preserves both the approved investment
basis and the executable realization basis authorized through Execution
Readiness.

Engineering Orchestration MAY progressively elaborate low-level execution
detail within the Execution Baseline and applicable tolerances.

Orchestration SHALL preserve:

- governed Epic intent;
- Approved Investment Baseline;
- authorized Plan basis;
- Engineering Slice traceability;
- architecture decisions;
- validation obligations;
- acceptance obligations;
- evidence obligations;
- authorization conditions;
- tolerances;
- reassessment triggers;
- carried-forward execution obligations; and
- applicable external obligations.

Material execution learning that invalidates the Execution Baseline SHALL
trigger reassessment rather than silent plan rewriting.

The historical basis on which execution was authorized SHALL remain
preserved.


## 45. AI-assisted Delivery Planning

AI systems MAY assist Engineering Delivery Planning by:

- analyzing the Approved Engineering Delivery Proposal;
- analyzing the Approved Investment Baseline;
- inspecting project artifacts and codebases;
- proposing Engineering Slice decomposition;
- analyzing Slice boundaries;
- identifying dependencies;
- proposing sequencing;
- identifying concurrency opportunities;
- analyzing architecture obligations;
- supporting Planning discovery;
- proposing validation approaches;
- proposing acceptance approaches;
- identifying evidence requirements;
- supporting resource analysis;
- refining estimates;
- identifying risks;
- identifying assumptions;
- analyzing uncertainty;
- identifying reassessment triggers;
- checking traceability;
- checking Plan consistency; and
- drafting or revising Engineering Delivery Plan content.

AI-generated Planning analysis SHALL be evaluated according to its
Engineering significance.

AI assistance SHALL NOT silently change the Approved Investment Baseline.

AI-generated Slice decomposition does not itself authorize realization.

AI-assisted Planning discovery does not constitute authorization for
Engineering Orchestration.

AI generation of an Engineering Delivery Plan does not confer Execution
Readiness authority.

AI systems MAY exercise governed authority only where explicitly
permitted under the Engineering Governance Specification.


## 46. Human, AI, and Mixed-team Operation

Engineering Delivery Planning SHALL support:

- human-led Engineering teams;
- AI-assisted human teams;
- mixed human and AI-agent teams; and
- AI-led Planning where applicable governance explicitly permits it.

Planning semantics SHALL remain consistent regardless of who or what
performs the work.

Responsibility, ownership, and decision authority SHALL be determined by
applicable Engineering governance rather than inferred solely from whether
an actor is human or automated.


## 47. Proportional Application

Not every Approved Engineering Delivery Proposal requires the same
Planning depth.

A small, familiar, low-risk realization MAY require:

- a single or small number of Engineering Slices;
- simple sequencing;
- lightweight dependency representation;
- concise validation planning;
- limited evidence requirements; and
- a simple delivery timeline.

A large, uncertain, architecturally significant, operationally sensitive,
or dependency-heavy realization MAY require:

- extensive Slice decomposition;
- complex dependency modeling;
- substantial architecture work;
- detailed validation planning;
- explicit evidence strategy;
- refined resource planning;
- sophisticated scheduling;
- extensive risk analysis; and
- stronger execution controls.

Proportionality SHALL NOT remove information necessary for a defensible
Execution Readiness Decision.


## 48. Process Output

The primary output is:

- Engineering Delivery Plan.

Supporting outputs MAY include:

- Engineering Slice artifacts or representations;
- Architecture Decision Records;
- Engineering Evidence;
- Planning discovery artifacts;
- dependency models;
- estimate artifacts;
- delivery timeline representations;
- validation plans;
- resource analysis;
- risk analysis; and
- other Supporting Engineering Artifacts.

The governance output is:

- Execution Readiness Decision.

An Authorize Execution Readiness Decision establishes the governed
Execution Baseline and permits transition to Engineering Orchestration.


## 49. Process Summary

Engineering Delivery Planning can be summarized as:

    Approved Engineering Delivery Proposal
                +
       Approved Investment Baseline
                +
       Engineering-ready Epic
                ↓
    Establish Planning interpretation
                ↓
    Preserve approved investment basis
                ↓
    Establish Engineering Slice structure
                ↓
    Single Slice or decomposed Slices
                ↓
    Establish Slice boundaries
                ↓
    Identify dependencies
                ↓
    Establish sequencing
                ↓
    Plan architecture obligations
                ↓
    Plan implementation obligations
                ↓
    Plan validation
                ↓
    Plan acceptance
                ↓
    Plan Engineering Evidence
                ↓
    Refine capabilities and resources
                ↓
    Refine effort / cost / delivery
                ↓
    Establish delivery timeline
                ↓
    Refine risks and uncertainty
                ↓
    Disposition Approved Conditions
       and Planning Obligations
                ↓
    Establish tolerances and
       reassessment triggers
                ↓
    Engineering Delivery Plan
                ↓
    Plan readiness
                ↓
    Execution Readiness Decision
                ↓
    Authorize / Return / Defer / Reject
                ↓
           [Authorize]
                ↓
    Governed Execution Baseline
                ↓
    Engineering Orchestration

Engineering Delivery Planning transforms an approved Engineering
investment proposition into a credible executable basis.

The process preserves the Approved Investment Baseline while refining the
realization detail necessary for governed execution.

The approved realization is represented through a coherent Engineering
Slice structure.

An Engineering Slice is a bounded, traceable unit of realization that can
be meaningfully planned, implemented, validated, evidenced, and accepted.

Where the approved realization is already sufficiently bounded, coherent,
traceable, and governable, it may constitute a single Engineering Slice.

Further decomposition is performed only where it meaningfully improves
the executable realization structure.

Engineering Slices are governed realization units rather than aliases for
sprints, stories, tickets, tasks, branches, pull requests, or technical
components.

Planning establishes Slice boundaries, dependencies, sequencing,
architecture obligations, implementation obligations, validation,
acceptance, evidence, capabilities, resources, refined estimates,
delivery timing, risks, assumptions, and uncertainty.

Planning may support incremental, iterative, sequential, concurrent, or
other governed realization patterns without prescribing a universal
project-management methodology.

Proposal-stage estimates are refined rather than rewritten.

Where Planning learning materially invalidates the Approved Investment
Baseline, governed reassessment is required.

Approved Conditions, carried-forward uncertainty, and Planning
Obligations remain visible until explicitly satisfied, resolved,
superseded, or otherwise governed.

Planning may carry bounded uncertainty into Engineering Orchestration
where execution remains credible and the uncertainty falls within
applicable authority and tolerances.

The Engineering Delivery Plan establishes sufficient executable
understanding to support an Execution Readiness Decision.

Execution Readiness produces one of four governed outcomes:

- Authorize;
- Return;
- Defer; or
- Reject.

Authorize permits Engineering Orchestration to begin within the governed
execution basis.

The Execution Baseline preserves the authorized Engineering Delivery Plan
revision, Execution Readiness Decision, authorization conditions,
Approved Investment Baseline, Engineering Slice structure, delivery
tolerances, carried-forward execution uncertainty, unresolved
architectural obligations, reassessment triggers, and other material
execution obligations.

Authorization does not eliminate execution uncertainty or freeze every
implementation detail.

Engineering Orchestration may progressively elaborate execution within
the Execution Baseline and applicable tolerances.

Material execution learning that invalidates that baseline triggers
governed reassessment rather than silent rewriting of Engineering
history.