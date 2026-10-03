# Context Resolution Specification

## 1. Purpose

This specification defines Context Resolution for Engineering Automation within the Engineering Platform.

Context Resolution enables Engineering Automation to identify, resolve, classify, and prepare the authoritative and applicable context required for a governed Engineering Platform activity while preserving semantic ownership, source authority, scope, lifecycle boundaries, uncertainty, provenance, and applicable source-precedence relationships.

Context Resolution exists so that human, AI, automation, and mixed-participant execution can operate using context appropriate to the governed activity without requiring all available project information to be accumulated or treated as equally applicable.

Context Resolution does not establish authoritative Product, Collaboration, Engineering, Release, or project state. It resolves and prepares derived execution-oriented context from applicable governing and supporting sources.

---

## 2. Scope

This specification governs:

- activity-specific context applicability;
- authoritative context resolution;
- supporting-context resolution;
- context-source resolution;
- lifecycle-sensitive context resolution;
- participant-sensitive context resolution where applicable;
- context scope;
- context applicability classification;
- unresolved and missing-required context;
- source authority and precedence preservation;
- material context conflicts;
- derived context representations;
- context filtering, projection, summarization, transformation, and compression;
- context provenance;
- persisted or cached resolved context;
- context-resolution failure and uncertainty;
- the relationship between Context Resolution and other Engineering Automation mechanisms; and
- the boundary between Context Resolution and Engineering Composition.

This specification does not define:

- Product, Collaboration, Engineering, or Release semantics;
- Engineering Platform lifecycle semantics;
- participant authority;
- Governed Activity semantics;
- Engineering Composition semantics;
- Development Standards;
- authoritative project artifacts;
- source-control semantics;
- runtime execution capability;
- execution-specific runtime composition;
- a universal project-context model;
- a universal context catalog;
- a project context truth store; or
- a universal context-completeness state.

---

## 3. Normative Language

The key words **SHALL**, **SHALL NOT**, **SHOULD**, **SHOULD NOT**, **MAY**, and **MAY NOT** are to be interpreted as normative requirements within this specification.

---

## 4. Semantic and Authority Boundary

Context Resolution is an Engineering Automation mechanism subordinate to the authoritative Engineering Platform, Engineering Systems, governed cross-system interactions, applicable project-governed sources, and other sources whose governing role establishes their applicability.

Context Resolution SHALL NOT independently define, establish, broaden, narrow, transfer, aggregate, replace, or manufacture governed semantics, authority, lifecycle state, or project state.

Context Resolution SHALL preserve the semantic ownership, authority, scope, uncertainty, and provenance of resolved source material.

The ability to discover, retrieve, read, transform, summarize, index, cache, embed, or otherwise process a source SHALL NOT itself establish:

- source authority;
- context applicability;
- semantic ownership;
- evidentiary weight;
- governing precedence;
- participant authority; or
- governed state.

Context Resolution resolves applicable context rather than creating the authoritative meaning of that context.

---

## 5. Core Concepts

### 5.1 Context Source

A **Context Source** is a governed, authoritative, supporting, external, operational, implementation, or derived source from which information may be considered for a governed activity.

The existence or accessibility of a Context Source SHALL NOT itself make that source applicable to a particular activity.

### 5.2 Context Requirement

A **Context Requirement** identifies context whose applicability is determined by the resolved Governed Activity, lifecycle position, scope, participant context, governance, or other applicable semantic basis.

Context Requirements SHALL be derived from governing semantics rather than from the set of sources that happen to be available.

### 5.3 Context Applicability

**Context Applicability** identifies the relationship between a potential context item and the needs of a particular governed activity at its applicable lifecycle position and scope.

Context Applicability is activity-relative.

Context that is applicable to one activity SHALL NOT automatically be treated as applicable to another activity.

### 5.4 Context Resolution

**Context Resolution** is the Engineering Automation process of identifying applicable context requirements, resolving corresponding Context Sources, classifying their applicability and resolution state, and preparing a bounded execution-oriented context representation.

### 5.5 Resolved Context

**Resolved Context** is the derived execution-oriented representation produced by Context Resolution for use by downstream Engineering Automation mechanisms.

Resolved Context MAY contain or reference authoritative source material, supporting source material, derived projections, applicability classifications, unresolved matters, missing-required context, material conflicts, and provenance.

Resolved Context is a derived representation.

It SHALL NOT acquire independent semantic authority merely because it contains, references, summarizes, or transforms authoritative information.

---

## 6. Context Resolution Contract

Context Resolution SHALL determine context applicability from the requirements of the resolved Governed Activity and applicable lifecycle, scope, participant, governance, and authority semantics.

Context Resolution SHALL resolve applicable context from authoritative and supporting sources according to their governing role.

Context Resolution SHALL preserve:

- semantic ownership;
- source authority;
- applicable precedence;
- activity scope;
- participant-sensitive constraints where applicable;
- lifecycle boundaries;
- material uncertainty;
- material conflicts;
- context applicability;
- provenance; and
- derived-representation status.

Context Resolution SHALL NOT treat source availability, retrievability, technical accessibility, repository proximity, recency, implementation convenience, or model preference as independent evidence of context applicability or authority.

Where required context cannot be resolved, Context Resolution SHALL preserve the applicable missing or unresolved condition rather than manufacture a complete context representation.

---

## 7. Context Applicability Model

Context Resolution SHALL classify material context requirements according to their relationship to the governed activity and applicable lifecycle position.

The standard applicability classifications are:

### 7.1 Required

**Required** context is context that the governing activity requires to be established and available for the applicable use at the current lifecycle point.

Failure to resolve Required context SHALL be represented according to the Missing Required classification where the context is expected to have been established.

### 7.2 Applicable

**Applicable** context is context that is relevant to the governed activity when established and available, but is not required by the governing activity to have been established at the current lifecycle point.

Applicable context SHALL NOT be converted into Required context merely because it would improve execution convenience, completeness, or AI performance.

### 7.3 Unresolved

**Unresolved** context is materially relevant context whose value, decision, state, or authoritative source is legitimately not yet established at the current lifecycle point.

Unresolved context SHALL remain unresolved.

Context Resolution SHALL NOT infer, predict, select, or manufacture a value merely to make downstream execution appear complete.

### 7.4 Not Applicable

**Not Applicable** context is context outside the semantic needs of the governed activity at the applicable lifecycle position and scope.

Availability of Not Applicable context SHALL NOT cause it to be included merely because it may be useful elsewhere in the project or later in the lifecycle.

### 7.5 Missing Required

**Missing Required** context is context that the governed activity requires and that is expected to have been established at the current lifecycle point, but which cannot be resolved sufficiently for the applicable use.

Missing Required context SHALL be surfaced distinctly from legitimately Unresolved context.

Context Resolution SHALL NOT convert Missing Required context into Unresolved context merely to permit downstream execution.

---

## 8. Progressive and Lifecycle-Sensitive Context

Context Resolution SHALL be progressive and lifecycle-sensitive.

Context requirements SHALL reflect what the applicable governed activity requires or permits at its current lifecycle position rather than what may eventually become known elsewhere in the Engineering Platform lifecycle.

Context Resolution SHALL NOT require downstream Product, Collaboration, Engineering, or Release information before applicable governance requires that information to have been established.

Context that becomes applicable later in the lifecycle SHALL NOT automatically be projected backward into an earlier activity merely because it already exists in the project.

For example, existing implementation technologies, source code, Development Standards, deployment configuration, or Release state SHALL NOT automatically become applicable Product context solely because those sources are available.

The governing principle is:

> **applicability, not accumulation.**

---

## 9. Context Scope

Context Resolution SHALL preserve the scope applicable to the resolved Governed Activity.

Context scope MAY include, where established by governing semantics:

- project;
- Engineering System;
- governed cross-system interaction;
- subsystem;
- governed artifact;
- Product Capability;
- Engineering Slice;
- Release;
- Release Candidate;
- execution target; or
- another applicable governed boundary.

Context Resolution SHALL NOT broaden context scope merely because broader information is technically available.

Where context scope is materially unresolved, Context Resolution SHALL preserve the unresolved boundary rather than assume project-wide scope.

Context scope SHALL remain distinguishable from participant authority scope and technical-access scope.

---

## 10. Context Sources and Governing Role

Context Resolution MAY resolve context from sources including, where applicable:

- Engineering Platform principles;
- Engineering Platform specifications;
- Product System artifacts and governed state;
- Collaboration System artifacts, interactions, and governed outcomes;
- Engineering System artifacts and governed state;
- Release System artifacts and governed state;
- project-specific governance;
- Participant Declarations and Resolved Participant Context;
- Resolved Activity Context;
- Development Standards;
- Architecture Decision Records;
- implementation artifacts;
- source code;
- source-control state;
- test and validation results;
- runtime or operational information;
- external standards;
- vendor or dependency documentation;
- other authoritative external references;
- derived indexes or representations; and
- other sources applicable to the governed activity.

This list does not establish that every source class is applicable to every activity.

Context Resolution SHALL preserve the governing role of each source.

Inclusion of multiple sources within Resolved Context SHALL NOT equalize their:

- authority;
- semantic ownership;
- precedence;
- evidentiary weight;
- lifecycle meaning; or
- governing effect.

---

## 11. Source Availability, Applicability, Accessibility, and Authority

Context Resolution SHALL preserve the distinctions among:

- whether a source exists;
- whether a source is applicable;
- whether a source is technically accessible;
- whether a source is authoritative for a particular concern; and
- whether a source is sufficiently current for the applicable use.

These properties SHALL NOT be treated as interchangeable.

A technically accessible source SHALL NOT be assumed applicable.

An applicable source that cannot be technically accessed SHALL NOT be treated as nonexistent.

A retrievable source SHALL NOT be assumed authoritative.

An authoritative source SHALL NOT be assumed applicable to every governed activity.

Technical access to a source SHALL NOT establish participant authority over that source or the governed semantics represented by it.

---

## 12. Authoritative and Supporting Context

Context Resolution SHALL preserve distinctions between authoritative context and supporting context where material.

Authoritative context derives its governing role from applicable Engineering Platform, Engineering System, cross-system, project-governed, or other established authority.

Supporting context MAY inform understanding, execution, evaluation, diagnosis, or evidence without independently establishing the governed semantics or state for which another source is authoritative.

Examples of supporting context MAY include:

- operational logs;
- source-control history;
- external technical documentation;
- derived summaries;
- indexes;
- diagnostic information; or
- other non-authoritative material.

Classification as supporting context SHALL NOT imply that the information is unimportant.

Classification as authoritative context SHALL remain concern-specific where applicable.

A source authoritative for one concern SHALL NOT automatically be treated as authoritative for another concern.

---

## 13. Context Resolution and Source Retrieval

Source retrieval is a technical mechanism and SHALL remain distinct from Context Resolution.

Context Resolution SHOULD determine applicable context requirements before broad source accumulation wherever practical.

The conceptual relationship is:

**Resolved Activity Context + applicable participant and governed context → Context Requirements → source discovery and retrieval → applicability and authority evaluation → Resolved Context**

Implementations MAY optimize, parallelize, index, prefetch, cache, or otherwise alter the technical ordering of these operations provided the semantic distinction between source availability and context applicability is preserved.

Retrieval of a source SHALL NOT itself establish that the source belongs in Resolved Context.

Failure to retrieve a source SHALL be classified according to the source's applicable role rather than automatically treated as absence of context.

---

## 14. Context Conflict and Source Precedence

Context Resolution SHALL preserve existing authority and precedence relationships among applicable sources.

Context Resolution SHALL NOT resolve material source conflicts solely through:

- file order;
- repository path;
- modification timestamp;
- retrieval order;
- majority agreement;
- model preference;
- parsing convenience;
- implementation convenience; or
- arbitrary source ranking.

Where governing semantics establish precedence or conflict resolution, Context Resolution SHALL preserve and apply that relationship.

Where material applicable sources conflict and governing semantics do not establish their resolution, Context Resolution SHALL surface the conflict as unresolved.

A derived context representation SHALL NOT hide a material source conflict through summarization or normalization.

---

## 15. Missing Context and Uncertainty

Context Resolution SHALL preserve failure fidelity and material uncertainty.

Context Resolution SHALL NOT:

- invent missing governed information;
- infer unavailable authoritative state solely from weaker sources;
- convert legitimate uncertainty into apparent certainty;
- convert Missing Required context into a guessed value;
- treat absence of retrieval as proof of nonexistence;
- silently substitute a supporting source for a required authoritative source; or
- broaden context scope to compensate for missing information.

Where uncertainty is material to downstream execution, it SHALL remain represented in Resolved Context.

Downstream Engineering Automation SHALL treat unresolved or missing context according to the requirements of the governed activity rather than manufacture completeness.

---

## 16. Derived Context and Transformation

Context Resolution MAY derive execution-oriented representations from applicable source material.

Permitted derivation MAY include:

- selection;
- filtering;
- referencing;
- indexing;
- extraction;
- projection;
- summarization;
- normalization;
- transformation;
- compression;
- packaging; or
- another conforming representation technique.

Derived context SHALL remain subordinate to its governing sources.

Transformation SHALL preserve material:

- semantics;
- semantic ownership;
- authority;
- scope;
- source distinctions;
- uncertainty;
- material conflicts; and
- provenance.

Context Resolution SHALL NOT use summarization, compression, transformation, or context-window constraints as justification for removing material governance, authority, scope, uncertainty, or conflict information required for conforming execution.

Where transformation materially reduces source detail, sufficient provenance SHOULD be preserved to support retrieval or reconstruction of the relevant source basis where required.

---

## 17. Context Sufficiency

Context sufficiency is relative to a particular Governed Activity, participant context, lifecycle position, scope, and intended downstream use.

This specification does not establish a universal state of complete project context.

A project MAY have context sufficient for one Governed Activity while lacking context required for another.

Context Resolution SHALL NOT infer global project readiness from activity-specific context sufficiency.

Where Required context is resolved and no Missing Required condition remains, that fact SHALL NOT independently establish:

- participant authority;
- lifecycle readiness;
- execution readiness;
- approval;
- authorization;
- acceptance;
- admission;
- Release readiness; or
- any other governed state.

Context sufficiency remains an input to downstream governed execution rather than an independent governed outcome.

---

## 18. Development Standards

Development Standards SHALL be resolved only where applicable to the governed activity.

Context Resolution SHALL NOT inject Development Standards merely because standards exist for the project.

Where a governed Engineering activity relies upon an established technology, practice, or constraint for which an applicable Development Standard is required, Context Resolution SHALL resolve that standard according to the governing activity and lifecycle requirements.

Where a technology or practice is legitimately not yet established, Context Resolution SHALL NOT require its Development Standard prematurely.

Development Standards SHALL remain authoritative according to their Engineering System governance and SHALL NOT become owned by Context Resolution merely because they are included in Resolved Context.

---

## 19. External Context

Context Resolution MAY include external information where applicable to a governed activity.

External information MAY include:

- standards;
- vendor documentation;
- dependency documentation;
- regulatory or contractual references;
- technical references;
- external system state; or
- other applicable sources.

External information SHALL retain the authority, provenance, currency, and governing role established for that source.

Inclusion of external information SHALL NOT automatically make that information authoritative Engineering Platform, Engineering System, or project-governed state.

Where external information is authoritative for a particular concern under applicable governance, Context Resolution SHALL preserve that role without broadening it to unrelated concerns.

---

## 20. Relationship to Participant Resolution

Participant Resolution and Context Resolution are distinct Engineering Automation mechanisms.

Participant Resolution resolves applicable participant identity, capacity, responsibility, scope, authority, constraints, status, and provenance.

Context Resolution MAY use Resolved Participant Context to determine participant-sensitive context requirements, visibility constraints, authority-sensitive context, or other applicable context boundaries.

Context Resolution SHALL NOT independently infer participant authority from raw source access, identity, role-like labels, or technical capability.

Resolved Context SHALL preserve applicable participant-related constraints where those constraints materially affect downstream execution.

Context Resolution SHALL NOT broaden participant authority merely because additional context is available.

---

## 21. Relationship to Activity Resolution

Activity Resolution and Context Resolution are distinct Engineering Automation mechanisms.

Activity Resolution resolves the applicable Governed Activity and its material semantic context.

Context Resolution uses Resolved Activity Context to determine which project and governing information is required, applicable, legitimately unresolved, not applicable, or missing required for that activity.

Resolved Activity Context SHALL identify and preserve the semantic applicability boundaries that Context Resolution operationalizes.

Context Resolution SHALL NOT independently redefine the Governed Activity in order to make available context appear applicable.

Where the activity remains materially unresolved, Context Resolution SHALL NOT manufacture a complete activity-specific context as though resolution had succeeded.

---

## 22. Relationship to Engineering Composition

Context Resolution SHALL remain distinct from Engineering Composition.

Context Resolution determines what authoritative and supporting context applies to a governed activity and prepares a bounded execution-oriented view of that context.

Engineering Composition governs controlled derivation where Engineering System semantics establish composition obligations for Engineering artifacts or Engineering context.

An implementation MAY use common source-resolution, transformation, validation, provenance, or composition libraries for both mechanisms.

Shared implementation machinery SHALL NOT collapse their semantic distinction.

Context Resolution SHALL NOT redefine Engineering Composition semantics, composition authority, governed artifact semantics, or Composition Report semantics.

Where Engineering Composition produces an authoritative or governed derived result, Context Resolution MAY resolve that result according to its governing role without acquiring ownership of the composition semantics that established it.

---

## 23. Relationship to Prompt Governance and Prompt Generation

Prompt Governance and Prompt Generation MAY consume Resolved Context when deriving conforming AI execution instructions.

Prompt Generation SHALL NOT independently broaden context applicability merely because additional project information can be retrieved or would improve prompt detail.

Resolved Context informs the activity-specific authoritative and supporting basis available to Prompt Generation.

Prompt Generation MAY further transform or express resolved context as permitted by Prompt Governance, provided applicable semantic ownership, authority, scope, uncertainty, and provenance remain preserved.

Context Resolution SHALL remain responsible for context applicability; Prompt Generation SHALL remain responsible for deriving conforming AI execution instructions from its applicable generation basis.

---

## 24. Relationship to Execution Composition

Context Resolution and Execution Composition are distinct Engineering Automation mechanisms.

Context Resolution determines and prepares applicable governed context.

Execution Composition determines how Resolved Participant Context, Resolved Activity Context, Resolved Context, applicable execution instructions, runtime constraints, and available execution capabilities are combined for a specific execution.

Context Resolution SHALL NOT require a particular model context format, workspace layout, CLI argument representation, runtime environment, agent protocol, or tool-access mechanism.

Execution Composition SHALL NOT broaden context applicability merely to satisfy runtime convenience.

Where runtime limitations prevent all applicable context from being represented directly, execution preparation MAY use references, retrieval mechanisms, staged context, transformations, or other conforming mechanisms provided material governing semantics and context requirements remain preserved.

---

## 25. Persistence, Caching, and Freshness

Resolved Context MAY be persisted, cached, indexed, or otherwise retained where useful.

Persisted or cached Resolved Context SHALL remain derived context.

Availability of persisted context SHALL NOT establish that it remains current or applicable.

Context Resolution SHALL reassess persisted context before reuse where material changes to any of the following may affect the intended activity:

- governing Platform semantics;
- Engineering System or cross-system semantics;
- Resolved Activity Context;
- Resolved Participant Context;
- project-governed state;
- Development Standards;
- source state;
- lifecycle position;
- activity scope;
- authority or visibility constraints;
- external authoritative references; or
- other material applicability basis.

This specification does not require a particular cache invalidation, indexing, storage, or freshness mechanism.

---

## 26. Provenance and Continuity

Context Resolution SHALL preserve sufficient provenance to identify the material basis from which Resolved Context was produced where required for conformance, reconstruction, validation, continuity, or governed execution.

Relevant provenance MAY include:

- Context Source identity;
- source semantic owner;
- source governing role;
- source version or applicable state;
- applicability classification;
- activity and scope basis;
- participant-sensitive basis where material;
- transformations or projections applied;
- material exclusions;
- unresolved context;
- Missing Required context;
- material source conflicts;
- external reference basis; and
- resolution mechanism or version where useful.

Provenance SHALL remain sufficient to avoid representing derived context as independent authoritative source material where that distinction is material.

---

## 27. Resolution Failure and Failure Fidelity

Context Resolution SHALL preserve failure fidelity.

Examples include:

- failure to discover a required source SHALL NOT be treated as proof that the source does not exist;
- failure to access an applicable source SHALL remain distinguishable from source nonexistence;
- failure to resolve a required source SHALL be represented as Missing Required where the source is expected to have been established;
- legitimately unestablished context SHALL remain Unresolved rather than Missing Required;
- material source conflict SHALL remain unresolved where governance does not establish its resolution;
- transformation failure SHALL be treated as an automation failure rather than failure of the source's governing Engineering System;
- indexing or cache failure SHALL NOT alter source authority;
- context-window limitation SHALL NOT justify silent removal of material governance or uncertainty; and
- unavailable supporting context SHALL NOT automatically establish failure of the governed activity.

Context Resolution failure SHALL NOT itself establish Product failure, Collaboration failure, Engineering failure, Release failure, lifecycle failure, or another governed conclusion unless applicable governing semantics independently establish such a conclusion.

---

## 28. Validation

Context Resolution SHALL support validation of all applicable concerns including:

- context-requirement resolution;
- applicability classification;
- source identity;
- source authority and governing role;
- source accessibility where required;
- source currency where material;
- activity-scope consistency;
- participant-sensitive constraints where applicable;
- source-precedence relationships;
- material source conflicts;
- Required versus Unresolved versus Missing Required classification;
- derived-context transformation integrity;
- provenance sufficiency; and
- persisted-context basis validity where reused.

Successful technical validation of Resolved Context SHALL NOT establish participant authority, lifecycle readiness, execution readiness, or another governed outcome.

Validation execution SHALL NOT manufacture context authority, applicability, governed state, or missing information.

---

## 29. Implementation Neutrality

This specification does not require:

- a universal context catalog;
- a context registry;
- a project context directory;
- a context manifest;
- a universal context schema;
- a context database;
- a centralized context service;
- a universal context identifier namespace;
- a universal source taxonomy;
- a universal context-completeness state;
- a particular retrieval engine;
- a particular search engine;
- a particular vector database;
- embeddings;
- Retrieval-Augmented Generation;
- a knowledge graph;
- a particular indexing strategy;
- a particular cache;
- a particular summarization mechanism;
- a particular AI model;
- a particular context-window strategy;
- a particular source-control system;
- a particular external documentation provider;
- a particular programming language;
- a particular storage mechanism; or
- a particular Engineering Automation implementation.

Implementations MAY introduce such mechanisms where required provided they remain subordinate to authoritative Engineering Platform, Engineering System, cross-system, and project-governed semantics and conform to this specification.

---

## 30. Evolution and Conformance

Context Resolution implementations MAY evolve as Engineering Automation implementation experience reveals improved mechanisms for applicability determination, source discovery, retrieval, filtering, projection, summarization, transformation, conflict handling, validation, provenance, caching, freshness, continuity, or downstream integration.

Implementation detail does not constitute missing Engineering Platform architecture.

Changes to Context Resolution or its implementation SHALL conform to the closed Engineering Platform architecture and applicable Product, Collaboration, Engineering, and Release System semantics.

A proposed change requires architectural reconsideration only where it materially alters an established architectural obligation under the applicable Engineering Platform architecture-reopening criteria.

Context Resolution SHALL remain an Engineering Automation mechanism and SHALL NOT evolve into an independent source of Product, Collaboration, Engineering, Release, project, lifecycle, authority, Development Standard, or Engineering Composition semantics.

The governing objective remains:

> **resolve the smallest sufficient applicable context without becoming the source of its meaning.**
