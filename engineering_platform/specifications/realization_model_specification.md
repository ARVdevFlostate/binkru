# Engineering Platform Realization Model Specification

## 1. Purpose

The Engineering Platform Realization Model defines the minimum architectural mechanisms required to realize the Engineering Capability Model while preserving the semantic ownership, authority boundaries, governance, traceability, and continuity established by the Engineering Platform architecture.

The Realization Model bridges the Engineering Capability Model and subsequent implementation-oriented architecture.

The Engineering Capability Model defines **what Engineering capabilities the Platform must provide**. The Realization Model defines **what architectural mechanisms must exist for those capabilities to be realizable**.

The Realization Model does not prescribe how those mechanisms must be implemented.

Its purpose is to ensure that different Platform realizations can vary in technology, topology, deployment model, participant interface, and execution environment without changing the authoritative Engineering semantics established by the Engineering Platform.

The Realization Model therefore establishes:

- the foundational Realization Mechanisms required by the Engineering Platform;
- the responsibilities and semantic boundaries of those mechanisms;
- the principles governing interaction between Realization Mechanisms;
- the relationship between Realization Mechanisms and Engineering Capabilities;
- the distinction between authoritative, durable, derived, and ephemeral characteristics of Engineering state;
- the architectural boundaries that Platform realizations must preserve.

The Realization Model applies equally to Engineering activity performed by Human Engineers and AI Engineers.

Human and AI Engineers may interact with different representations, execution capabilities, execution environments, or participant-specific controls. These differences must not create different underlying Engineering semantics, authority models, governance models, or sources of Engineering truth.

---

## 2. Scope

This specification governs the architectural realization of the Engineering Platform capabilities defined by the Engineering Capability Model:

1. Discovery & Navigation
2. Participation & Scope
3. Context Resolution & Composition
4. Execution Enablement
5. Governance & Validation Integration
6. Continuity & Provenance

It defines the shared architectural mechanisms through which those capabilities may be realized while preserving the ownership boundaries defined by the capability architecture.

This specification governs:

- resolution of Engineer identity;
- resolution of authoritative Engineering state;
- resolution of participant-relative Engineering state;
- discovery of Engineering information;
- resolution of applicable Engineering authority;
- resolution of technical execution capabilities;
- Engineering determinations;
- composition of Engineering information;
- projection of Engineering information for participants and uses;
- establishment of authoritative Engineering state;
- establishment of durable Engineering state;
- enforcement of execution-relevant constraints;
- invocation of execution mechanisms;
- preservation and resolution of Engineering provenance;
- composition and interaction of these mechanisms across Engineering capabilities.

This specification does not define:

- Product System semantics;
- Collaboration System semantics;
- Release System semantics;
- the internal domain semantics owned by individual Engineering Systems;
- Development Standards themselves;
- specific governance or validation policies;
- specific Human or AI user experiences;
- specific AI models, agents, prompts, skills, or reasoning mechanisms;
- specific execution tools or environments;
- specific persistence, indexing, messaging, workflow, search, policy, or integration technologies;
- deployment topology;
- service boundaries;
- API design;
- repository structure;
- physical data models;
- infrastructure architecture.

These concerns may be defined by downstream Platform specifications or implementation architecture, provided they conform to the semantic responsibilities and boundaries established by this specification.

The Realization Model does not replace the Engineering Capability Model or the specifications governing individual Engineering capabilities.

Where this specification describes a Realization Mechanism used by an Engineering capability, ownership of the underlying Engineering semantics remains with the capability, Engineering System, Engineering Standard, governance mechanism, validation mechanism, authoritative source, or other mechanism that defines those semantics.

---

## 3. Realization Model

### 3.1 Realization Mechanism

A **Realization Mechanism** is a foundational architectural responsibility required to make one or more Engineering Platform capabilities realizable.

A Realization Mechanism defines:

- the Engineering responsibility it performs;
- the categories of Engineering information or state it may consume;
- the information, state, determination, representation, or operational result it may produce;
- the authority characteristics of its result;
- the Engineering semantics it must preserve;
- the Engineering meaning or authority it must not independently establish;
- its permitted relationships with other Realization Mechanisms.

A Realization Mechanism defines an architectural contract.

It does not define a required implementation unit.

Therefore:

> **Realization Mechanism ≠ component ≠ service ≠ process ≠ API ≠ repository ≠ agent ≠ execution runtime.**

A single implementation component may realize multiple Realization Mechanisms.

A single Realization Mechanism may be realized through multiple components or systems.

A Realization Mechanism may also be delegated wholly or partially to an existing Engineering System, authoritative mechanism, or external execution mechanism where the applicable realization contract remains satisfied.

The mapping between Realization Mechanisms and implementation components is a downstream architectural concern.

### 3.2 Relationship to Engineering Capabilities

Engineering Capabilities and Realization Mechanisms describe different architectural dimensions.

An **Engineering Capability** defines a semantic responsibility of the Engineering Platform.

A **Realization Mechanism** defines an architectural mechanism required to make such semantic responsibilities operable.

Therefore:

> **Engineering Capability ≠ Realization Mechanism.**

A capability may depend upon multiple Realization Mechanisms.

A Realization Mechanism may support multiple capabilities.

The six Engineering Capabilities do not imply six independent runtimes, services, repositories, or implementation components.

Instead, the Engineering Platform is realized through shared mechanisms operating under capability-owned semantics and authority boundaries.

Where a Realization Mechanism evaluates, resolves, composes, represents, enforces, or acts upon semantics owned by an Engineering capability or other authoritative mechanism, use of the Realization Mechanism does not transfer ownership of those semantics.

### 3.3 Semantic Ownership

The Realization Model does not introduce a new universal owner of Engineering truth.

Authoritative Engineering semantics remain owned by the Engineering System, Engineering Standard, governance mechanism, validation mechanism, authoritative source, or other Engineering mechanism responsible for those semantics.

Realization Mechanisms may resolve, discover, determine, compose, project, persist, execute against, or preserve provenance about Engineering information without becoming the authoritative owner of that information.

In particular:

- resolution does not transfer ownership;
- discovery does not establish authority or applicability;
- determination does not inherently establish authoritative Engineering state;
- composition does not create aggregate authority;
- projection does not change Engineering meaning;
- persistence does not establish authority;
- execution does not establish Engineering authority or Engineering completion;
- provenance does not replace authoritative Engineering state or authoritative history.

Where authoritative Engineering state is created or changed, that state must be established according to the semantics and authority of the mechanism owning that state.

### 3.4 Shared Realization

Realization Mechanisms provide shared architectural responsibilities rather than requiring capability-specific duplicate realization mechanisms.

The same foundational mechanism may participate in different Engineering interactions while operating under different capability-owned semantics.

For example, Engineering Determination may support determination of:

- Participation Eligibility;
- applicability;
- materiality;
- currency;
- evidence sufficiency;
- Execution Availability;
- Governed Determinations;
- Validation Determinations.

These are distinct Engineering determinations because their meaning, authority requirements, permissible outcomes, evidence requirements, and consequences are defined by their owning Engineering semantics.

They do not require separate foundational determination mechanisms.

Similarly, Engineering Composition may support Human-oriented Engineering context, AI-oriented execution context, handover, resumption, or other Engineering interactions without those interactions becoming separate foundational Realization Mechanisms.

Shared realization therefore means reuse of architectural responsibilities, not centralization of Engineering meaning or implementation.

### 3.5 Mechanism Composition

Realization Mechanisms may be composed to support Engineering interactions.

For example, an interaction may resolve Engineering state, perform an Engineering Determination, compose relevant information, project that information for a participant, invoke execution, establish state, or preserve provenance.

Such compositions describe cooperation between Realization Mechanisms.

They do not establish a universal Realization Mechanism sequence.

Therefore:

> **Realization Mechanism composition does not define a new Engineering lifecycle.**

Different Engineering interactions may use different subsets of Realization Mechanisms and may compose them differently according to the applicable Engineering semantics.

Dependencies between Realization Mechanisms similarly do not imply implementation coupling, deployment coupling, or mandatory global sequencing.

Reciprocal dependencies may legitimately exist where mechanisms operate over different Engineering questions or state. A realization must not, however, use reciprocal dependency to create circular semantic justification in which a result depends upon the authority, determination, or state that the same interaction is attempting to establish.

### 3.6 Realization Patterns

Some recurring Engineering interactions require coordinated use of multiple Realization Mechanisms but do not constitute additional foundational mechanisms.

Examples include:

- Engineering Entry;
- Engineering Reconstruction;
- handover;
- resumption;
- context re-resolution;
- context challenge;
- Controlled Execution;
- Engineering Automation;
- AI Execution Composition.

These are **Realization Patterns**.

A Realization Pattern describes a valid composition of foundational Realization Mechanisms for a recurring Engineering interaction.

Realization Patterns may be defined or refined by downstream specifications without expanding the foundational Realization Mechanism model unless a genuinely new architectural responsibility is identified.

### 3.7 Implementation Neutrality

The Realization Model is technology-neutral.

Conformance with this specification does not require any particular:

- application architecture;
- service architecture;
- persistence technology;
- event architecture;
- workflow engine;
- policy engine;
- search technology;
- index;
- knowledge graph;
- vector store;
- AI runtime;
- agent framework;
- integration protocol;
- container runtime;
- execution sandbox;
- API style;
- user interface.

An implementation may employ any of these technologies where appropriate.

Technology choices must not alter the semantic responsibilities, authority characteristics, ownership boundaries, or invariants established by the Realization Model.

Implementation optimization may combine multiple Realization Mechanisms into a single technical operation where their individual architectural contracts remain satisfied.

Conversely, a Realization Mechanism may be distributed across multiple technical operations or components.

Implementation structure must not redefine architectural meaning.

---

## 4. Realization Principles

The following principles govern all Realization Mechanisms and their composition.

These principles apply independently of implementation architecture, deployment topology, participant type, execution environment, or technology choice.

Where a Realization Mechanism is delegated to or realized by another Engineering System, authoritative mechanism, external system, or execution mechanism, the applicable principles remain in force.

### 4.1 Dependency Independence

A dependency between Realization Mechanisms identifies an architectural relationship in which the result of one mechanism may be required by another for a particular Engineering interaction.

A dependency does not imply:

- implementation coupling;
- deployment coupling;
- shared persistence;
- synchronous interaction;
- mandatory global sequencing;
- common ownership.

Implementations may realize dependencies through any architecture that preserves the applicable realization contracts and Engineering semantics.

### 4.2 Compositional Dependency

Realization Mechanisms may participate in reciprocal interactions where they operate over different Engineering questions, state, or points in an Engineering interaction.

Reciprocal dependency must not create circular semantic justification.

A Realization Mechanism must not depend upon authority, determination, or state that the same interaction is attempting to establish unless independently established Engineering state provides the required semantic anchor.

Therefore, composition of Realization Mechanisms may be cyclic at the interaction level without permitting circular establishment of Engineering meaning or authority.

### 4.3 Explicit Uncertainty

Where a Realization Mechanism cannot produce a sufficiently grounded result from applicable Engineering state and semantics, it must preserve the applicable unresolved condition rather than fabricate resolution.

Such conditions may include:

- unresolved;
- ambiguous;
- incomplete;
- unavailable;
- inaccessible;
- stale;
- uncertain;
- conflicting;
- unsupported;
- partial.

The applicable condition must retain the meaning required by the owning Engineering semantics.

Absence of a conclusive result must not be silently converted into a positive, negative, default, or assumed Engineering conclusion.

### 4.4 Derived Aggregation

Combining information from authoritative sources does not create a new authoritative source.

Participant State, Engineering Composition, Engineering Projection, discovery results, execution-supporting context, and other derived representations may aggregate information from multiple authoritative sources while remaining derived Engineering state.

Authoritative constituents retain their:

- identity;
- ownership;
- authority characteristic;
- normative force;
- scope;
- provenance.

Aggregation, persistence, indexing, caching, or reuse of such information must not elevate the resulting representation into authoritative Engineering state.

### 4.5 Semantic Preservation

A Realization Mechanism that selects, resolves, assembles, transforms, summarizes, filters, or represents Engineering information must preserve all materially relevant Engineering meaning required for the applicable use.

This includes, as applicable:

- identity;
- source ownership;
- authority characteristic;
- normative force;
- scope;
- applicability;
- lifecycle or state semantics;
- relationships;
- constraints and prohibitions;
- discretion;
- evidence relationships;
- governance and validation meaning;
- uncertainty, ambiguity, incompleteness, and conflict;
- currency;
- provenance.

Semantic preservation does not require textual or structural identity with the source.

Information may be summarized, filtered, compressed, restructured, or transformed where doing so does not materially alter its Engineering meaning.

### 4.6 Representation Independence

Different participants, interfaces, activities, and execution mechanisms may receive different representations of the same underlying Engineering information.

Human-oriented and AI-oriented representations may differ in structure, detail, syntax, interaction model, or machine readability.

Such differences must not create different underlying Engineering semantics.

Representation must not alter:

- normative force;
- authority;
- applicability;
- constraints;
- governance or validation meaning;
- material uncertainty;
- Engineering responsibility.

Representation differences are therefore permitted; semantic divergence is not.

### 4.7 Authority by Ownership

Engineering state becomes authoritative only according to the semantics and authority of the mechanism owning that state.

Neither Engineering authority nor the authoritative characteristic of Engineering state is established merely by:

- storage location;
- persistence;
- discovery;
- aggregation;
- composition;
- projection;
- synchronization;
- publication;
- technical execution;
- successful transmission;
- provenance capture.

Where authoritative Engineering state is created or changed, the applicable authoritative owner must retain control of the semantics by which that state becomes authoritative.

Physical hosting of authoritative state within Platform infrastructure does not by itself make the Platform the semantic owner of that state.

### 4.8 Durability Independence

The durability characteristic of Engineering state is independent of its authority characteristic.

Making Engineering state durable must not elevate its authority.

Therefore:

> **Durable ≠ authoritative.**

Authoritative Engineering state may be durable.

Derived or execution-related Engineering state may also be durable where its preservation is materially required for continuity, reconstruction, governance, validation, or subsequent Engineering activity.

Persistence duration does not increase authority.

Durable representations of authoritative Engineering state must remain distinguishable from the authoritative source they represent unless the representation is itself established as authoritative by the applicable owning mechanism.

### 4.9 Provenance Sufficiency

Engineering Provenance must preserve sufficient materially relevant relationships to support applicable Engineering traceability, explanation, governance, validation, continuity, reconstruction, and accountability.

Provenance need not exhaustively capture every underlying:

- technical operation;
- infrastructure event;
- implementation detail;
- participant interaction;
- Human cognitive process;
- AI internal reasoning process.

The required provenance is determined by Engineering materiality and applicable Engineering semantics.

Technical telemetry, logs, or audit records may contribute to Engineering Provenance but do not inherently constitute sufficient Engineering Provenance.

### 4.10 Provenance Non-Substitution

Engineering Provenance preserves traceability among Engineering state, activity, evidence, determinations, responsibility, authority, execution, and establishment.

It does not replace them.

In particular:

- provenance does not replace authoritative Engineering state;
- provenance does not replace authoritative history where another mechanism owns that history;
- provenance does not replace Engineering Evidence;
- provenance does not establish responsibility;
- provenance does not establish authority;
- provenance does not establish an Engineering Determination.

Traceability to authoritative information does not make the provenance representation itself authoritative over that information.

### 4.11 Provenance Materiality

Materiality may determine which Engineering Provenance must be retained durably.

Where materiality itself cannot be determined without provenance, sufficient provenance must remain available until the applicable materiality determination can be made.

A realization must not discard information required to determine whether that information or its associated Engineering activity is materially significant.

This requirement does not mandate permanent or exhaustive retention of all technical activity.

### 4.12 Technical Possibility

Technical availability of an Execution Capability does not establish that the capability is available for use in the applicable Engineering context.

Therefore:

> **Technical Availability ≠ Execution Availability.**

Technical capability does not independently establish:

- Engineering authority;
- Participation Eligibility;
- governed-work responsibility;
- applicability;
- execution permission.

A technically available capability may remain unavailable for use according to applicable Engineering state, determinations, authority, or constraints.

Likewise, a capability must not be classified as technically unavailable solely because its use is prohibited for a particular participant or Engineering activity.

### 4.13 Controlled Execution

Where the Platform controls an execution surface, applicable execution-relevant constraints that require technical enforcement must remain effective on that surface.

Where the Platform does not control an execution surface, it must not claim technical enforcement that it cannot provide.

A realization must distinguish between constraints that it can:

- technically enforce;
- communicate or expose;
- identify another mechanism as responsible for enforcing.

Knowledge, communication, or display of a constraint does not constitute technical enforcement.

Where required enforcement cannot be achieved, that condition must remain explicit and be available to the applicable Engineering Determination where the owning semantics make enforcement relevant to Execution Availability or another Engineering consequence.

### 4.14 Execution Non-Authority

Execution Invocation and Execution Outcome do not independently establish authoritative Engineering meaning.

In particular:

> **Execution success ≠ Engineering success.**

> **Execution completion ≠ Engineering completion.**

> **Execution Outcome ≠ Governed Determination.**

> **Execution Outcome ≠ Validation Determination.**

Technical execution must not independently establish:

- Engineering authority;
- governed-work responsibility;
- authoritative Engineering state;
- governance or validation outcomes;
- Engineering completion;
- Product acceptance;
- Release Admission;
- deployment or commercial launch.

Where execution results contribute to any such Engineering conclusion, the applicable Engineering semantics, determinations, authority, and authoritative state-establishment requirements remain applicable.

### 4.15 Pattern Non-Lifecycle

Composition of Realization Mechanisms into a recurring Realization Pattern does not create a new canonical Engineering lifecycle.

A pattern may describe a useful or expected interaction among mechanisms without requiring that:

- every Engineering interaction use that pattern;
- every mechanism participate in that pattern;
- mechanisms execute in a universal sequence;
- pattern progression become authoritative Engineering state;
- pattern stages become Engineering lifecycle states.

Engineering lifecycle semantics remain owned by the Engineering mechanisms that define them.

Realization Patterns describe architectural cooperation, not lifecycle authority.

---

## 5. Realization Mechanism Model

The Engineering Platform is realized through fourteen foundational Realization Mechanisms organized into six mechanism families.

The mechanism families provide a conceptual organization of related architectural responsibilities.

They are not additional Realization Mechanisms and do not prescribe:

- implementation components;
- service boundaries;
- deployment units;
- ownership boundaries;
- execution order;
- persistence boundaries.

The classification of a Realization Mechanism into a family reflects its primary architectural responsibility. A mechanism may support Engineering interactions involving responsibilities represented by other families.

### 5.1 Resolution Mechanisms

Resolution Mechanisms resolve Engineering identity, state, authority, discovery needs, and technical execution capability without independently establishing the Engineering state or authority they resolve.

The Resolution family consists of:

1. **Engineer Identity Resolution** — resolves the durable Engineer Identity corresponding to a participant where Engineer identity is required.

2. **Authoritative Engineering State Resolution** — resolves current or historical authoritative Engineering state from its owning mechanism while preserving source identity, ownership, semantics, relationships, temporal characteristics, and provenance.

3. **Participant State Resolution** — resolves participant-relative Engineering state applicable to an Engineer within a defined scope or Engineering concern.

4. **Discovery Resolution** — resolves an Engineering discovery need into candidate Engineering information, identities, relationships, source references, or navigation targets.

5. **Authority Resolution** — resolves the applicable Engineering authority entitled to establish a specific authoritative determination or Engineering state within a defined scope.

6. **Execution Capability Resolution** — resolves technically available Execution Capabilities and the candidate Execution Mechanisms through which those capabilities may be realized.

Resolution describes what can be resolved from applicable Engineering information and mechanisms.

Resolution does not by itself establish applicability, authority, responsibility, permission, authoritative state, or Engineering conclusion.

### 5.2 Determination Mechanism

The Determination family consists of one foundational Realization Mechanism:

1. **Engineering Determination** — evaluates an Engineering question using resolved Engineering state, applicable Engineering semantics, and relevant evidence or conditions to produce an explicit Engineering Determination.

In general:

> **Resolved Engineering State + Applicable Semantics + Relevant Evidence/Conditions → Engineering Determination**

Engineering Determination provides shared realization machinery for Engineering conclusions whose specific meaning remains owned by the applicable Engineering semantics.

Examples include:

- Participation Eligibility;
- applicability;
- materiality;
- currency;
- evidence sufficiency;
- Execution Availability;
- Governed Determinations;
- Validation Determinations.

These uses do not constitute separate foundational Realization Mechanisms.

Engineering Determination does not inherently establish Engineering authority or authoritative Engineering state.

Where a determination carries authoritative Engineering effect, that effect must satisfy the Authoritative Engineering State Establishment contract, including where determination and establishment are realized atomically by the same owning mechanism.

### 5.3 Composition Mechanisms

Composition Mechanisms assemble and represent Engineering information for a defined Engineering activity, concern, participant, interface, or execution use.

The Composition family consists of:

1. **Engineering Composition** — assembles Engineering information required for a defined activity, concern, or use while preserving the semantics, authority characteristics, relationships, uncertainty, and provenance of its constituents.

2. **Engineering Projection** — represents Engineering information for a defined participant, activity, interface, or execution use while preserving materially relevant Engineering meaning.

Engineering Composition determines **what information is assembled**.

Engineering Projection determines **how that information is represented**.

Therefore:

> **Composition ≠ Projection.**

A correct Engineering Composition may be projected incorrectly.

A correct Engineering Projection cannot compensate for materially required Engineering information that was absent from the composition or other information being projected.

Composition and Projection produce derived Engineering state and do not independently establish authoritative Engineering state.

### 5.4 Establishment Mechanisms

Establishment Mechanisms govern the realization of authoritative Engineering state and materially significant durable Engineering state.

The Establishment family consists of:

1. **Authoritative Engineering State Establishment** — establishes or transitions authoritative Engineering state through the mechanism owning that state according to applicable authority, semantics, lifecycle, integrity, and state-transition requirements.

2. **Durable State Establishment** — establishes materially significant Engineering state as durable state where that state must survive ephemeral boundaries without thereby becoming authoritative Engineering state.

These mechanisms establish different characteristics.

Authoritative Engineering State Establishment answers:

> **How does Engineering state become established as authoritative according to its owning semantics and authority?**

Durable State Establishment answers:

> **How does materially significant Engineering state survive ephemeral boundaries?**

Therefore:

> **Authoritative establishment ≠ durable establishment.**

Durability does not establish authority.

Authoritative Engineering state may also be durable, but the authority and durability characteristics remain conceptually distinct.

### 5.5 Execution Mechanisms

Execution Mechanisms make Engineering technical action possible under applicable Engineering state and execution conditions.

The Execution family consists of:

1. **Constraint Enforcement** — technically enforces applicable execution-relevant constraints on execution surfaces controlled by the Platform according to their established meaning, applicability, and enforcement requirements.

2. **Execution Invocation** — invokes an applicable Execution Mechanism to perform an Engineering execution operation using a resolved Execution Capability under the applicable execution conditions.

Execution mechanisms operate while preserving the distinction between technical capability and Engineering availability.

In particular:

> **Technical Availability ≠ Execution Availability.**

Constraint Enforcement does not define the meaning or applicability of the constraints it enforces.

Execution Invocation does not independently establish Engineering authority, authoritative Engineering state, governance or validation outcomes, or Engineering completion.

Execution Outcome remains distinct from Engineering Determination and authoritative Engineering state establishment.

### 5.6 Provenance Mechanism

The Provenance family consists of one foundational Realization Mechanism:

1. **Engineering Provenance** — preserves and resolves sufficient provenance for materially significant Engineering state, determinations, evidence, compositions, projections, execution, and state establishments so that their relevant origins, derivations, relationships, and transformations remain traceable.

Engineering Provenance is cross-cutting.

It may receive provenance-relevant information from any foundational Realization Mechanism and may be resolved by other mechanisms where traceability, explanation, governance, validation, continuity, reconstruction, or accountability requires it.

Engineering Provenance does not become the authoritative owner of the Engineering state or history it describes.

Where sufficient provenance already exists in an authoritative or otherwise adequate durable source, the Platform need not duplicate that provenance solely to establish a Platform-owned provenance record.

Provenance preservation therefore requires durable resolvability where materially necessary, not universal duplication of Engineering history.

### 5.7 Canonical Realization Mechanism Set

The foundational Realization Mechanism set is:

| Family | Realization Mechanism |
|---|---|
| Resolution | Engineer Identity Resolution |
| Resolution | Authoritative Engineering State Resolution |
| Resolution | Participant State Resolution |
| Resolution | Discovery Resolution |
| Resolution | Authority Resolution |
| Resolution | Execution Capability Resolution |
| Determination | Engineering Determination |
| Composition | Engineering Composition |
| Composition | Engineering Projection |
| Establishment | Authoritative Engineering State Establishment |
| Establishment | Durable State Establishment |
| Execution | Constraint Enforcement |
| Execution | Execution Invocation |
| Provenance | Engineering Provenance |

This set is foundational to the Engineering Platform Realization Model.

A Platform realization may introduce additional components, services, adapters, indexes, repositories, workflows, agents, runtimes, or other technical constructs as required.

Such constructs do not become additional foundational Realization Mechanisms merely because they are required by a particular implementation.

Similarly, recurring interactions such as Engineering Entry, Engineering Reconstruction, handover, resumption, Controlled Execution, Engineering Automation, or AI Execution Composition remain Realization Patterns unless they introduce an architectural responsibility not expressible through the foundational Realization Mechanisms.

The foundational set should be expanded only where a genuinely new architectural responsibility cannot be expressed through the responsibilities and composition of the existing Realization Mechanisms without violating their semantic or authority boundaries.

---

## 6. Resolution Mechanisms

Resolution Mechanisms resolve Engineering information required by other Realization Mechanisms and Engineering interactions.

Resolution operates against applicable sources, state, semantics, and mechanisms without independently creating the Engineering meaning, authority, responsibility, permission, or authoritative state being resolved.

A successful resolution means that the requested information has been resolved according to the applicable mechanism contract.

It does not mean that the resolved information is necessarily:

- applicable to the current Engineering activity;
- sufficient for a subsequent Engineering Determination;
- current beyond the temporal characteristics established by its source;
- independently authoritative merely because it has been resolved or represented;
- permitted for use merely because it is technically accessible.

Where resolution cannot produce a sufficiently grounded result, the unresolved, ambiguous, incomplete, unavailable, inaccessible, stale, uncertain, or conflicting condition must remain explicit according to the applicable Engineering semantics.

Resolution Mechanisms may use discovery, indexes, caches, derived representations, references, or other implementation facilities. Such facilities do not replace the authoritative sources or mechanisms against which authoritative resolution is required.

### 6.1 Engineer Identity Resolution

#### Responsibility

Engineer Identity Resolution resolves the durable Engineer Identity corresponding to a participant where Engineering activity requires Engineer identity.

It preserves the distinction between durable Engineer Identity and transient mechanisms through which an Engineer authenticates, participates, interacts, or executes Engineering activity.

Therefore:

> **Engineer Identity ≠ credential ≠ session ≠ Execution Instance ≠ project participation ≠ governed-work responsibility ≠ Engineering authority.**

#### Consumes

Engineer Identity Resolution may consume:

- participant-identifying information;
- authentication or session context;
- identity references associated with Engineering state;
- authoritative identity information;
- durable Engineering state containing identity relationships;
- provenance required to resolve or disambiguate identity.

Authentication information may contribute to identity resolution but does not itself define Engineer Identity.

#### Produces

Engineer Identity Resolution produces:

- a resolved Engineer Identity;
- sufficient identity references required by subsequent Engineering interactions;
- applicable identity provenance;
- an explicit unresolved, ambiguous, unavailable, inaccessible, or conflicting condition where Engineer Identity cannot be sufficiently resolved.

The resolved identity must remain distinguishable from the credential, session, interface, participant mechanism, or Execution Instance through which the Engineer is currently interacting.

#### Authority Characteristic

Engineer Identity Resolution is resolutive.

It does not create Engineer Identity merely by resolving it.

Where the authoritative identity mechanism establishes or changes Engineer Identity, that establishment remains governed by the semantics and authority of the mechanism owning Engineer Identity.

#### Must Preserve

Engineer Identity Resolution must preserve, as applicable:

- durable Engineer identity;
- identity continuity across sessions, interfaces, execution environments, and Execution Instances;
- authoritative identity source;
- identity scope;
- identity relationships;
- relevant temporal characteristics;
- provenance;
- ambiguity or conflict between candidate identities.

Replacement of an Execution Instance, session, credential, tool, interface, or AI runtime must not by itself create a new Engineer Identity.

#### Must Not Establish

Engineer Identity Resolution must not independently establish:

- project participation;
- governed-work responsibility;
- Participation Eligibility;
- Engineering authority;
- Execution Availability;
- execution permission;
- applicable Engineering context;
- Governed Determinations;
- Validation Determinations;
- authoritative Engineering lifecycle state.

Successful authentication or identity resolution must not be interpreted as establishing any of these.

#### Dependencies

Engineer Identity Resolution may depend upon:

- Authoritative Engineering State Resolution, where Engineer Identity or identity relationships are owned by an authoritative Engineering mechanism;
- Engineering Provenance, where provenance is required to resolve identity continuity or disambiguate identity.

Engineer Identity Resolution must not require Participant State Resolution as a prerequisite for establishing which Engineer Identity the participant represents.

---

### 6.2 Authoritative Engineering State Resolution

#### Responsibility

Authoritative Engineering State Resolution resolves current or historical authoritative Engineering state from the mechanism owning that state.

It provides access to authoritative Engineering information while preserving the source identity, ownership, semantics, relationships, temporal characteristics, and provenance that make the state meaningful.

It must not create a competing source of Engineering truth.

#### Consumes

Authoritative Engineering State Resolution may consume:

- authoritative Engineering entity references;
- source-system or owning-mechanism references;
- Engineering scope;
- temporal or version requirements;
- relationship requirements;
- directly supplied authoritative references;
- discovery results identifying candidate authoritative sources or entities;
- provenance required to locate, relate, or disambiguate authoritative state.

#### Produces

Authoritative Engineering State Resolution produces:

- resolved current or historical authoritative Engineering state;
- authoritative source and ownership information;
- applicable entity identity and relationships;
- temporal, version, or currency-relevant source characteristics;
- applicable provenance;
- explicit unresolved, unavailable, inaccessible, incomplete, stale, uncertain, or conflicting conditions.

Where multiple authoritative sources contribute distinct Engineering state, their respective ownership and authority boundaries must remain distinguishable.

#### Authority Characteristic

The state being resolved may be authoritative.

The act of resolution does not make a representation authoritative.

Authority remains anchored in the owning mechanism and its applicable Engineering semantics.

A cache, index, replica, projection, local copy, or other representation of authoritative Engineering state is not independently authoritative merely because it represents authoritative state.

#### Must Preserve

Authoritative Engineering State Resolution must preserve, as applicable:

- authoritative source identity;
- Engineering entity identity;
- semantic ownership;
- authority characteristic;
- lifecycle and state semantics;
- normative force;
- Engineering relationships;
- scope;
- temporal characteristics;
- version or revision characteristics;
- uncertainty, incompleteness, ambiguity, and conflict;
- provenance.

Where authoritative state is represented outside its owning mechanism, sufficient source and temporal information must remain available to distinguish the representation from the authoritative source and support later currency assessment where required.

#### Must Not Establish

Authoritative Engineering State Resolution must not independently:

- create or modify authoritative Engineering state;
- establish new authoritative Engineering relationships;
- infer authoritative relationships merely from correlation or co-occurrence;
- establish applicability merely because information was resolved;
- establish Engineering authority merely because a source is authoritative;
- establish responsibility or participation;
- invent missing authoritative meaning;
- elevate cached, indexed, discovered, composed, projected, replicated, or otherwise derived state into independently authoritative Engineering state.

#### Dependencies

Authoritative Engineering State Resolution may depend upon:

- Engineer Identity Resolution, where source access or participant-relative resolution requires a resolved Engineer Identity;
- Discovery Resolution, where the authoritative source or entity must first be discovered;
- Engineering Provenance, where provenance is required to locate, relate, reconstruct, or disambiguate authoritative state.

Authoritative Engineering State Resolution must remain possible without Discovery Resolution where the caller already possesses a valid authoritative reference.

---

### 6.3 Participant State Resolution

#### Responsibility

Participant State Resolution resolves participant-relative Engineering state applicable to a resolved Engineer within a defined Engineering scope or concern.

Participant State may bring together authoritative facts and applicable determinations concerning how an Engineer currently relates to Engineering activity.

The resulting Participant State is derived Engineering state.

It does not become a new authoritative owner of its constituent facts.

#### Consumes

Participant State Resolution may consume:

- resolved Engineer Identity;
- authoritative Engineering state concerning participation or responsibility;
- applicable Engineering scope;
- participation relationships;
- governed-work responsibility relationships;
- Participant Operating Constraints and any independently established applicability determinations concerning them;
- applicable Engineering Determinations;
- temporal or currency information;
- provenance relevant to participant-relative state.

#### Produces

Participant State Resolution produces:

- resolved participant-relative Engineering state;
- applicable participation relationships;
- applicable governed-work responsibility relationships, where present;
- participant-relative constraints together with their established or unresolved applicability, as applicable;
- applicable participant-relative determinations;
- relevant scope and currency information;
- provenance;
- explicit unresolved, ambiguous, incomplete, unavailable, stale, uncertain, or conflicting participant-state conditions.

Participant State may exist where no governed-work responsibility has been established.

#### Authority Characteristic

Participant State is derived Engineering state.

Authoritative facts represented within Participant State retain their original authoritative owners and authority characteristics.

Resolution of Participant State does not aggregate those facts into a new participant-state authority.

#### Must Preserve

Participant State Resolution must preserve the distinctions among:

- Engineer Identity;
- project participation;
- governed-work responsibility;
- Participation Eligibility;
- Engineering authority;
- execution capability;
- Execution Availability;
- execution activity.

It must also preserve:

- identity of constituent authoritative state;
- source ownership;
- scope;
- currency;
- Participant Operating Constraints and their normative force;
- applicable determination meaning;
- provenance;
- uncertainty, incompleteness, ambiguity, and conflict.

In particular:

> **Participation ≠ responsibility ≠ authority ≠ execution.**

And:

> **Assignment ≠ Self-Assumption ≠ Begin Realization.**

#### Must Not Establish

Participant State Resolution must not independently establish:

- Engineer Identity;
- project participation;
- governed-work responsibility;
- Participation Eligibility;
- Engineering authority;
- Participant Operating Constraints;
- applicability of a constraint where applicability requires an Engineering Determination;
- Execution Availability;
- execution permission;
- authoritative Engineering lifecycle state.

The existence of Participant State must not imply that the Engineer has governed-work responsibility.

#### Dependencies

Participant State Resolution depends upon:

- Engineer Identity Resolution, where participant-relative state is being resolved for a specific Engineer.

It may additionally depend upon:

- Authoritative Engineering State Resolution;
- Engineering Determination;
- Engineering Provenance;
- Authority Resolution, where authority information forms part of the participant-relative state being represented.

Reciprocal interaction with Engineering Determination is permitted where different participant-relative questions are being resolved and no circular semantic justification is introduced.

---

### 6.4 Discovery Resolution

#### Responsibility

Discovery Resolution resolves an Engineering discovery need into candidate Engineering information, identities, relationships, source references, or navigation targets.

In general:

> **Engineering Discovery Need → Candidate Engineering Information**

Discovery enables an Engineer or another Realization Mechanism to locate potentially relevant Engineering information without asserting that the discovered information is authoritative, applicable, sufficient, or permitted for use.

#### Consumes

Discovery Resolution may consume:

- an Engineering discovery need;
- search, navigation, or exploration criteria;
- Engineering scope;
- participant-relative information where discovery is participant-sensitive;
- known Engineering entity or source references;
- Engineering relationships;
- indexes or discovery-oriented representations;
- provenance useful for navigation or relationship discovery.

#### Produces

Discovery Resolution produces:

- candidate Engineering entities;
- candidate Engineering information;
- candidate relationships;
- candidate authoritative-source references;
- navigation targets;
- discovery metadata;
- relevant provenance;
- explicit unresolved, unavailable, inaccessible, incomplete, or ambiguous discovery conditions.

Discovery results are candidates for subsequent Engineering interaction.

#### Authority Characteristic

Discovery Resolution is fundamentally non-authoritative.

Discovery may identify information originating from an authoritative source, but the discovery result does not itself constitute authoritative resolution of that information.

Therefore:

> **Discovery of authoritative state ≠ Authoritative Engineering State Resolution.**

#### Must Preserve

Discovery Resolution must preserve, as applicable:

- identity of discovered candidates;
- known source references;
- known authority characteristics;
- relationship status;
- discovery scope;
- provenance;
- uncertainty or ambiguity concerning candidate identity, relationship, or relevance.

Discovery ranking, filtering, similarity, recommendation, or inferred relationship must remain distinguishable from authoritative Engineering meaning.

#### Must Not Establish

Discovery Resolution must not independently establish:

- authority;
- authoritative Engineering state;
- authoritative Engineering relationships;
- applicability;
- normative force;
- materiality;
- Engineering priority;
- Participation Eligibility;
- governed-work responsibility;
- Execution Availability;
- governance or validation outcomes.

In particular:

> **Relevance ≠ applicability.**

> **Ranking ≠ priority ≠ authority ≠ normative force ≠ materiality.**

> **Inferred relationship ≠ established relationship.**

#### Dependencies

Discovery Resolution may depend upon:

- Engineer Identity Resolution, where discovery is participant-relative;
- Participant State Resolution, where participant-relative scope or constraints affect discovery;
- Authoritative Engineering State Resolution, where authoritative information is needed to support discovery relationships or navigation;
- Engineering Provenance, where provenance supports discovery or traversal.

Discovery Resolution is not a mandatory gateway to Authoritative Engineering State Resolution or any other Realization Mechanism.

---

### 6.5 Authority Resolution

#### Responsibility

Authority Resolution resolves the applicable Engineering authority entitled to establish a specific authoritative Engineering determination or Engineering state within a defined scope.

Authority Resolution answers who or what possesses the applicable authority for the Engineering question being considered.

It resolves authority.

It does not exercise that authority.

#### Consumes

Authority Resolution may consume:

- the Engineering question, determination, state, or transition for which authority must be resolved;
- applicable Engineering scope;
- authoritative Engineering state defining authority;
- governance or validation semantics;
- delegation relationships;
- role or responsibility information where relevant to authority semantics;
- temporal conditions;
- applicable Engineering Determinations;
- provenance relevant to the origin, establishment, or delegation of authority.

#### Produces

Authority Resolution produces:

- resolved applicable Engineering authority;
- authority identity;
- authority source;
- authority scope;
- applicable conditions or limitations;
- delegation boundaries, where applicable;
- temporal validity information;
- provenance;
- explicit unresolved, ambiguous, unavailable, stale, uncertain, or conflicting authority conditions.

#### Authority Characteristic

Authority Resolution is resolutive.

It does not grant, exercise, broaden, transfer, aggregate, or manufacture Engineering authority.

Resolved authority remains defined by the Engineering mechanism and semantics that establish that authority.

#### Must Preserve

Authority Resolution must preserve:

- authority identity;
- authority source;
- authority scope;
- applicable conditions;
- delegation boundaries;
- temporal validity;
- non-transitivity;
- provenance;
- unresolved, ambiguous, incomplete, or conflicting authority conditions.

Where multiple authorities exist, their scopes and relationships must remain distinct unless the applicable Engineering semantics explicitly define otherwise.

#### Must Not Establish

Authority Resolution must not independently:

- grant Engineering authority;
- broaden authority;
- aggregate multiple authorities into greater authority;
- delegate or transfer authority;
- exercise resolved authority;
- establish the target Engineering Determination or authoritative Engineering state;
- infer authority merely from project participation;
- infer authority merely from governed-work responsibility;
- infer authority merely from technical capability;
- infer authority merely from tool or system access;
- infer authority merely from successful execution;
- infer authority merely from the ability to evaluate or produce a determination.

Therefore:

> **Responsibility ≠ authority.**

> **Technical capability ≠ authority.**

> **Ability to determine ≠ authority to establish.**

#### Dependencies

Authority Resolution may depend upon:

- Engineer Identity Resolution;
- Authoritative Engineering State Resolution;
- Participant State Resolution, where participant-relative facts are relevant to authority;
- Engineering Determination, where applicable authority depends upon an independently established Engineering condition;
- Engineering Provenance, where authority or delegation must be traced.

Reciprocal interaction with Engineering Determination is permitted only where the determination used to resolve authority is semantically independent of the determination whose authority is currently being resolved.

---

### 6.6 Execution Capability Resolution

#### Responsibility

Execution Capability Resolution resolves the Execution Capabilities that are technically available for an Engineering activity and the candidate Execution Mechanisms through which those capabilities may be realized.

It answers:

> **What can technically be done, and through what mechanism?**

It does not answer:

> **May this participant use that capability for this Engineering activity?**

That second question is governed by Execution Availability and other applicable Engineering semantics.

#### Consumes

Execution Capability Resolution may consume:

- the Engineering activity or technical operation being considered;
- available Execution Environments;
- available Execution Mechanisms;
- Engineering Tools;
- Engineering Automation;
- environment or mechanism capabilities;
- technical compatibility information;
- participant-relative technical characteristics where they genuinely affect capability or mechanism exposure;
- relevant technical state;
- provenance required to establish capability origin or characteristics.

#### Produces

Execution Capability Resolution produces:

- technically available Execution Capabilities;
- candidate Execution Mechanisms;
- relevant Execution Environment relationships;
- technical capability characteristics and limitations;
- relevant technical compatibility information;
- provenance;
- explicit unavailable, inaccessible, incomplete, uncertain, or conflicting technical-capability conditions.

The result may subsequently contribute to determination of Execution Availability.

#### Authority Characteristic

Execution Capability Resolution is technical and resolutive.

It does not establish Engineering authority, Execution Availability, execution permission, or applicability merely because a technical capability or mechanism exists.

Therefore:

> **Execution Capability ≠ Execution Availability.**

> **Technical Availability ≠ Engineering authority.**

> **Mechanism access ≠ execution permission.**

> **Can execute ≠ may execute.**

#### Must Preserve

Execution Capability Resolution must preserve:

- identity of Execution Capabilities;
- identity of candidate Execution Mechanisms;
- Execution Environment relationships;
- technical limitations and compatibility;
- participant-relative technical differences where genuine;
- relevant temporal or technical-availability characteristics;
- provenance;
- uncertainty, incompleteness, or conflict.

Participant-relative capability resolution must distinguish genuine technical differences in capability or mechanism exposure from restrictions arising from Engineering authority, Execution Availability, or applicable constraints.

A technically available capability must not be reclassified as technically unavailable solely because its use is prohibited for the current participant or Engineering activity.

The following conditions must remain distinct:

> **Technically unavailable**

> **≠ Technically available but not available for use**

> **≠ Technically available and available for use.**

#### Must Not Establish

Execution Capability Resolution must not independently establish:

- Engineering authority;
- Participation Eligibility;
- governed-work responsibility;
- Execution Availability;
- execution permission;
- applicability of Participant Operating Constraints;
- governance or validation outcomes;
- authoritative Engineering state;
- Engineering completion.

Technical access to an Execution Mechanism must not be interpreted as any of these.

#### Dependencies

Execution Capability Resolution may depend upon:

- Engineer Identity Resolution, where technical capability genuinely differs by participant identity;
- Participant State Resolution, where participant-relative technical characteristics affect capability exposure;
- Authoritative Engineering State Resolution, where execution capability or environment information is authoritatively governed;
- Discovery Resolution, where Execution Capabilities or candidate Execution Mechanisms must be discovered;
- Engineering Provenance, where provenance is required to establish capability, environment, or mechanism characteristics.

Execution Capability Resolution must remain semantically independent of Execution Availability.

Execution Availability may consume the result of Execution Capability Resolution through Engineering Determination, but prohibition of use must not be used to redefine technical capability as technical unavailability.

---

## 7. Engineering Determination

Engineering Determination evaluates an Engineering question using resolved Engineering state, applicable Engineering semantics, and relevant evidence or conditions to produce an explicit Engineering Determination.

In general:

> **Resolved Engineering State + Applicable Semantics + Relevant Evidence/Conditions → Engineering Determination**

Engineering Determination is a shared Realization Mechanism.

It does not define a universal determination model, outcome taxonomy, governance model, validation model, or policy language.

The Engineering semantics owning a determination define, as applicable:

- the Engineering question being determined;
- the information, evidence, and conditions relevant to that question;
- the permissible determination outcomes;
- the authority required for the determination;
- the scope of the determination;
- the determination lifecycle or currency semantics;
- the Engineering consequences of the determination;
- the conditions under which reassessment is required.

Engineering Determination realizes those semantics without becoming their owner.

Examples of Engineering Determination include:

- Participation Eligibility;
- applicability;
- materiality;
- currency;
- evidence sufficiency;
- Execution Availability;
- Governed Determinations;
- Validation Determinations.

These examples are uses of the foundational Engineering Determination mechanism rather than additional foundational Realization Mechanisms.

### 7.1 Responsibility

Engineering Determination evaluates a defined Engineering question according to its owning Engineering semantics using sufficiently resolved Engineering state, evidence, conditions, and other applicable inputs.

The mechanism must preserve the distinction between producing a determination result and establishing any authoritative Engineering effect associated with that result.

A determination may be intended by its owning Engineering semantics to carry authoritative Engineering effect, or it may be used as a Derived Determination without authoritative Engineering effect.

This distinction concerns the intended Engineering effect of the determination.

It does not create separate foundational Realization Mechanisms or imply that intended authoritative effect has already been established.

### 7.2 Consumes

Engineering Determination may consume:

- the Engineering question to be determined;
- applicable Engineering semantics;
- resolved authoritative Engineering state;
- resolved Participant State;
- resolved Engineering authority;
- Engineering Evidence;
- prior Engineering Determinations;
- applicable constraints or conditions;
- Engineering scope;
- temporal or currency information;
- execution capability or Execution Outcome information where relevant;
- Engineering Provenance;
- other derived Engineering state where permitted by the owning semantics.

Inputs to a determination retain their respective identity, ownership, authority characteristic, normative force, uncertainty, and provenance.

The presence of an input does not imply that the input is applicable, sufficient, current, or authoritative for the determination unless the applicable Engineering semantics establish that characteristic.

### 7.3 Produces

Engineering Determination produces:

- an explicit determination result;
- the Engineering question determined;
- the applicable determination type or semantics;
- the scope of the determination;
- the applicable outcome defined by the owning Engineering semantics;
- the relevant basis, evidence, or conditions required to support the determination;
- the intended or established authority characteristic of the determination, as applicable;
- applicable temporal, lifecycle, or currency characteristics;
- relevant provenance;
- an explicit unresolved, ambiguous, incomplete, unsupported, unavailable, stale, uncertain, or conflicting condition where a sufficiently grounded determination cannot be produced.

The mechanism must not invent a conclusive outcome where the applicable Engineering semantics do not support one.

A determination outcome must remain within the outcome semantics defined by its owner.

The Realization Model does not require all Engineering Determinations to use a common outcome vocabulary.

### 7.4 Authority Characteristic

An Engineering Determination may be intended to carry authoritative Engineering effect where the owning Engineering semantics define it accordingly.

Producing the determination result does not by itself establish that authoritative effect.

Where a determination creates or changes authoritative Engineering state, that authoritative effect must satisfy the Authoritative Engineering State Establishment contract.

This requirement applies even where Engineering Determination and Authoritative Engineering State Establishment are realized atomically by the same owning mechanism.

Therefore:

> **Producing a determination intended to carry authoritative Engineering effect ≠ establishing that authoritative effect.**

The authority required to establish the authoritative Engineering effect of a determination must remain distinguishable from the technical ability to evaluate or produce the determination.

Therefore:

> **Ability to determine ≠ authority to establish.**

A Derived Determination has no authoritative Engineering effect merely because it was produced using authoritative Engineering state, authoritative evidence, or the same technical machinery used for a determination intended to carry authoritative Engineering effect.

### 7.5 Must Preserve

Engineering Determination must preserve, as applicable:

- the identity of the Engineering question being determined;
- the owning Engineering semantics;
- the identity and ownership of relevant input state;
- the authority characteristics of inputs;
- the authority required for authoritative effect;
- Engineering scope;
- normative force;
- evidence relationships;
- applicable constraints and conditions;
- permissible outcome semantics;
- temporal, lifecycle, and currency semantics;
- uncertainty, ambiguity, incompleteness, and conflict;
- provenance.

Where prior determinations contribute to a subsequent determination, their identity, scope, authority characteristic, currency, and provenance must remain distinguishable.

Where a determination depends upon Engineering Evidence, the relationship between evidence and determination must remain explicit.

In particular:

> **Evidence supports a determination; evidence does not itself constitute the determination.**

Where Execution Outcomes contribute to a determination:

> **Execution Outcome ≠ Engineering Determination.**

Technical success, failure, partial completion, interruption, or generated technical state must retain its technical meaning until the applicable Engineering semantics determine its Engineering consequence.

### 7.6 Must Not Establish

Engineering Determination must not independently:

- define the Engineering semantics it evaluates;
- create a universal determination outcome taxonomy;
- manufacture or broaden Engineering authority;
- infer authority merely from the ability to evaluate a determination;
- aggregate authority from multiple inputs or participants;
- convert authoritative input state into an authoritative determination merely because the input is authoritative;
- convert Engineering Evidence into an authoritative conclusion merely because the evidence exists;
- treat technical execution success or failure as an Engineering conclusion without the applicable Engineering semantics;
- silently convert unresolved, ambiguous, incomplete, unsupported, stale, uncertain, or conflicting conditions into conclusive outcomes;
- establish authoritative Engineering state except through conformance with the Authoritative Engineering State Establishment contract;
- redefine governance, validation, participation, responsibility, execution, or lifecycle semantics owned elsewhere.

Engineering Determination must not treat the absence of contrary evidence as sufficient evidence for a positive determination unless the owning Engineering semantics explicitly define that rule.

### 7.7 Dependencies

Engineering Determination may depend upon:

- Engineer Identity Resolution, where the determination is participant-relative;
- Authoritative Engineering State Resolution;
- Participant State Resolution;
- Authority Resolution, where authoritative effect requires applicable Engineering authority;
- Execution Capability Resolution, where technical capability is relevant to the Engineering question;
- Engineering Provenance;
- other Engineering Determinations where permitted by the owning semantics.

Engineering Determination may also consume Engineering Composition or Engineering Projection where the determination is performed against a composed or projected representation.

Use of a composition or projection must not weaken the semantic, authority, evidence, uncertainty, currency, or provenance requirements of the determination.

Reciprocal interaction between Engineering Determination and another Realization Mechanism is permitted where the mechanisms operate over different Engineering questions or independently established state.

A determination must not depend upon the authority, determination, applicability, or state that the same determination is attempting to establish unless independently established Engineering state provides the required semantic anchor.

### 7.8 Specialized Determinations

Specialized Engineering Determinations remain governed by the Engineering semantics that define them.

For example:

**Participation Eligibility** determines whether applicable Engineering semantics permit an Engineer to participate or to acquire a governed-work responsibility within the relevant scope. It does not itself establish participation or responsibility unless the applicable authoritative state is established through its owning mechanism.

**Applicability** determines whether Engineering information, semantics, constraints, standards, or other Engineering concerns apply within a defined Engineering context. Availability or discovery of information does not establish applicability.

**Materiality** determines whether Engineering information, activity, change, evidence, provenance, or state is materially significant according to applicable Engineering semantics. Materiality must not require prior loss of information needed to make the materiality determination.

**Currency** determines whether Engineering information or state remains sufficiently current for the applicable Engineering use. Persistence, successful resolution, or prior applicability does not establish current applicability.

**Evidence Sufficiency** determines whether the available Engineering Evidence satisfies the evidence requirements for a defined Engineering claim or determination. Evidence existence does not establish evidence sufficiency.

**Execution Availability** determines whether a technically available Execution Capability is available for use in the applicable Engineering context.

Therefore:

> **Technical Availability ≠ Execution Availability.**

A negative Execution Availability determination must not redefine a technically available capability as technically unavailable.

**Governed Determinations** retain the authority, permissible outcomes, scope, evidence requirements, lifecycle, and consequences defined by the applicable governance semantics.

**Validation Determinations** retain the validation meaning, permissible outcomes, evidence requirements, scope, authority, and consequences defined by the applicable validation semantics.

A Validation Determination must not be reduced to technical execution success or failure.

These specialized determinations may compose with one another where permitted by their owning Engineering semantics.

Such composition must not aggregate authority, erase uncertainty, or create circular semantic justification.

---

## 8. Composition Mechanisms

Composition Mechanisms assemble and represent Engineering information for a defined Engineering activity, concern, participant, interface, or execution use.

The Composition family consists of:

1. **Engineering Composition** — determines what Engineering information belongs in an assembly for a defined Engineering use.
2. **Engineering Projection** — determines how Engineering information is represented for a defined participant, activity, interface, or execution use.

Therefore:

> **Composition ≠ Projection.**

Engineering Composition addresses information selection, inclusion, relationship, and assembly.

Engineering Projection addresses representation, structure, transformation, and presentation.

Both mechanisms operate over Engineering information whose underlying semantics and authority remain owned by their applicable sources and Engineering mechanisms.

Composition and Projection produce derived Engineering state.

Neither mechanism creates aggregate authority or independently establishes authoritative Engineering state.

A composition or projection may become durable where materially required without thereby becoming authoritative.

### 8.1 Engineering Composition

#### Responsibility

Engineering Composition assembles Engineering information required for a defined Engineering activity, concern, participant, or use while preserving the materially relevant meaning and relationships of its constituents.

In general:

> **Resolved Engineering Information + Relevant Determinations/Conditions + Activity/Concern → Engineering Composition**

Engineering Composition determines what information belongs in the assembly.

It does not determine how that information must ultimately be represented to a Human Engineer, AI Engineer, interface, execution mechanism, or other consumer.

Engineering Composition may support, among other uses:

- Effective Engineering Context;
- Engineering Entry;
- handover;
- resumption;
- context re-resolution;
- Engineering Reconstruction;
- Controlled Execution;
- Engineering Automation;
- AI Execution Composition.

These uses do not constitute additional foundational Realization Mechanisms.

#### Consumes

Engineering Composition may consume:

- resolved authoritative Engineering state;
- resolved Participant State;
- Engineering Determinations;
- Engineering Evidence;
- applicable Engineering scope;
- applicable constraints and prohibitions;
- Engineering relationships;
- Engineering Provenance;
- durable Engineering state;
- derived Engineering state where permitted for the applicable use;
- Execution Capability information where relevant;
- Execution Outcomes or other execution-related state where relevant;
- the Engineering activity, concern, participant, or use for which composition is required.

Inputs retain their respective identity, ownership, authority characteristic, normative force, applicability, uncertainty, currency, and provenance.

The presence of information among available inputs does not by itself establish that the information belongs in the resulting composition.

#### Produces

Engineering Composition produces:

- a derived assembly of Engineering information for the defined activity, concern, participant, or use;
- the identities and relationships of materially relevant constituent information;
- applicable scope;
- relevant Engineering Determinations together with their applicable scope, currency, and established or unresolved applicability, as applicable;
- relevant constraints and prohibitions;
- relevant evidence relationships;
- relevant governance and validation information;
- relevant uncertainty, ambiguity, incompleteness, or conflict;
- relevant currency information;
- provenance sufficient to relate the composition to its constituent Engineering information;
- explicit unresolved composition conditions where materially required information cannot be sufficiently resolved or its applicability cannot be sufficiently determined.

The composition may identify information as included, excluded, unresolved, unavailable, or otherwise qualified according to the applicable Engineering semantics.

Composition must not silently treat absence from the resulting assembly as proof that the omitted information is inapplicable.

Therefore:

> **Included ≠ applicable.**

> **Omitted ≠ inapplicable.**

#### Authority Characteristic

Engineering Composition is derived Engineering state.

The authority characteristics of authoritative constituents remain anchored in their respective owning mechanisms.

Combining authoritative information does not create aggregate authority over the resulting composition.

Therefore:

> **Authoritative constituents ≠ authoritative composition.**

A composition may be persisted or otherwise made durable where materially required.

Durability does not change its derived authority characteristic.

#### Must Preserve

Engineering Composition must preserve, as applicable:

- constituent Engineering identity;
- source ownership;
- authority characteristic;
- normative force;
- applicability and its basis;
- Engineering scope;
- lifecycle or state semantics;
- Engineering relationships;
- constraints and prohibitions;
- participant discretion;
- evidence relationships;
- governance and validation meaning;
- uncertainty, ambiguity, incompleteness, and conflict;
- currency;
- provenance.

Where information from multiple authoritative sources is composed, their respective ownership and authority boundaries must remain distinguishable.

Where determinations contribute to composition, their identity, scope, outcome semantics, authority effect, currency, and provenance must remain distinguishable.

Where composition requires selection or omission, the selection process must not materially alter the Engineering meaning of the resulting assembly.

#### Must Not Establish

Engineering Composition must not independently:

- create authoritative Engineering state;
- create aggregate Engineering authority;
- change the authority characteristic of constituent information;
- establish applicability merely by including information;
- establish inapplicability merely by excluding information;
- establish currency merely because information was successfully resolved;
- establish Engineering priority merely through ordering or prominence;
- establish governed-work responsibility;
- establish Execution Availability;
- establish governance or validation outcomes;
- resolve uncertainty by omission;
- invent missing Engineering information;
- redefine lifecycle, governance, validation, responsibility, or execution semantics owned elsewhere.

Composition must not treat information from one authoritative source as overriding another authoritative source unless the applicable Engineering semantics establish that relationship.

#### Dependencies

Engineering Composition may depend upon:

- Engineer Identity Resolution;
- Authoritative Engineering State Resolution;
- Participant State Resolution;
- Discovery Resolution;
- Authority Resolution;
- Engineering Determination;
- Execution Capability Resolution;
- Engineering Provenance;
- Durable State Establishment, where previously established durable Engineering state contributes to the composition.

Engineering Composition may consume prior compositions where permitted by the applicable Engineering use.

Composition of compositions must preserve the identity, authority boundaries, derivation, uncertainty, currency, and provenance of materially relevant underlying Engineering information.

Engineering Composition does not require Engineering Projection.

A composition may exist independently of any particular representation.

### 8.2 Engineering Projection

#### Responsibility

Engineering Projection represents Engineering information for a defined participant, activity, interface, execution mechanism, or other Engineering use while preserving materially relevant Engineering meaning.

In general:

> **Engineering Information + Consumer/Use Requirements → Engineering Projection**

Engineering Projection determines how Engineering information is represented.

It may transform structure, syntax, level of detail, organization, encoding, or presentation without changing the underlying Engineering semantics.

A projection may be Human-oriented, AI-oriented, interface-oriented, execution-oriented, or otherwise specialized for the applicable use.

Different projections of the same Engineering information may legitimately differ.

Such differences must not create different underlying Engineering truth.

#### Consumes

Engineering Projection may consume:

- an Engineering Composition;
- resolved authoritative Engineering state;
- resolved Participant State;
- Engineering Determinations;
- Engineering Evidence;
- Engineering Provenance;
- durable or derived Engineering state;
- applicable participant or consumer requirements;
- interface requirements;
- execution-mechanism requirements;
- representation constraints;
- the Engineering activity or use for which projection is required.

Engineering Projection need not require a prior Engineering Composition where the information to be projected is otherwise sufficiently defined.

#### Produces

Engineering Projection produces:

- a derived representation of Engineering information for the defined consumer or use;
- materially relevant Engineering identity and source references;
- materially relevant authority and normative-force information;
- materially relevant applicability and scope;
- materially relevant constraints and prohibitions;
- materially relevant evidence relationships;
- materially relevant governance and validation meaning;
- materially relevant uncertainty, ambiguity, incompleteness, and conflict;
- materially relevant currency information;
- relevant provenance;
- explicit projection limitations or loss conditions where the required representation cannot preserve materially necessary Engineering meaning.

A projection may omit information that is not materially required for its defined use.

Such omission must not cause the represented information to acquire materially different Engineering meaning.

#### Authority Characteristic

Engineering Projection is derived Engineering state.

Representation of authoritative Engineering state does not make the projection independently authoritative.

Therefore:

> **Representation of authority ≠ authority of representation.**

A projection may be durable where materially required.

Persistence, reuse, transmission, synchronization, or publication of a projection does not elevate its authority.

#### Must Preserve

Engineering Projection must preserve all Engineering meaning materially relevant to its defined use, including, as applicable:

- Engineering identity;
- source ownership;
- authority characteristic;
- normative force;
- scope;
- applicability;
- lifecycle or state semantics;
- Engineering relationships;
- constraints and prohibitions;
- discretion;
- evidence relationships;
- governance and validation meaning;
- uncertainty, ambiguity, incompleteness, and conflict;
- currency;
- provenance.

Projection fidelity is measured by preservation of materially relevant Engineering semantics, not by textual or structural similarity to the source.

Therefore:

> **Semantic fidelity ≠ textual identity.**

A projection need not be exhaustive to be semantically faithful.

Where information is summarized, filtered, compressed, restructured, translated, encoded, or transformed, materially relevant Engineering meaning must remain intact.

#### Must Not Establish

Engineering Projection must not independently:

- create authoritative Engineering state;
- create or aggregate Engineering authority;
- change normative force;
- establish or change applicability;
- establish or change Engineering responsibility;
- establish or change Participant Operating Constraints;
- establish Execution Availability;
- establish governance or validation outcomes;
- remove material uncertainty through simplification;
- convert recommendations or inferred relationships into authoritative Engineering meaning;
- reinterpret omission as inapplicability;
- redefine Engineering semantics to suit the target representation.

In particular:

> **Representation must not become reinterpretation.**

A more concise, structured, machine-readable, persuasive, prominent, or technically convenient representation must not acquire greater Engineering authority than the information it represents.

#### Dependencies

Engineering Projection may depend upon:

- Engineering Composition;
- Engineer Identity Resolution, where representation is participant-relative;
- Participant State Resolution, where participant-relative state affects representation requirements;
- Authoritative Engineering State Resolution;
- Engineering Determination;
- Engineering Provenance;
- Durable State Establishment, where durable Engineering state is being projected.

Engineering Projection may operate directly on sufficiently resolved Engineering information without requiring Engineering Composition where no additional assembly responsibility is required.

Projection requirements may influence what information an Engineering Composition must make available for a particular use.

Such reciprocal interaction must not allow representation requirements to redefine the underlying Engineering semantics or improperly exclude materially required information.

### 8.3 Composition and Projection Relationship

Engineering Composition and Engineering Projection are complementary but independent Realization Mechanisms.

A typical interaction may use:

> **Engineering Information → Engineering Composition → Engineering Projection**

This is a valid Realization Pattern, not a mandatory sequence.

Other interactions may project directly from sufficiently resolved Engineering information.

Likewise, a composition may be established without immediately producing a projection.

The correctness of the two mechanisms must remain independently assessable.

A semantically correct composition may be represented incorrectly.

A semantically correct projection cannot compensate for materially required Engineering information that was absent from the information available for projection.

Therefore:

> **Composition completeness and Projection fidelity are distinct concerns.**

Consumer or representation requirements may legitimately influence composition where those requirements affect what information is materially necessary for the intended Engineering use.

They must not cause materially relevant Engineering information to be excluded merely because that information is inconvenient for the target representation.

### 8.4 Effective Engineering Context

Effective Engineering Context is a use of Engineering Composition.

It represents Engineering information composed for a defined Engineering activity, concern, participant, or point of interaction according to applicable Engineering semantics and determinations.

Effective Engineering Context is derived Engineering state.

It is not a new authoritative source of Engineering truth.

Authoritative information represented within Effective Engineering Context retains its original identity, ownership, authority characteristic, normative force, scope, currency, and provenance.

Effective Engineering Context may differ between Engineering activities or participants where applicable Engineering state, responsibility, constraints, determinations, or activity requirements legitimately differ.

Such variation must not create different underlying Engineering semantics.

Effective Engineering Context may be projected differently for Human Engineers and AI Engineers while preserving the same applicable Engineering meaning.

Where underlying Engineering state, applicability, currency, responsibility, constraints, or other materially relevant conditions change, previously composed Effective Engineering Context must not be assumed to remain current merely because it persists.

Context currency and applicability remain subject to the applicable Engineering semantics and determinations.

### 8.5 AI Execution Composition

AI Execution Composition is a Realization Pattern using foundational Realization Mechanisms to provide AI-oriented Engineering information for an Engineering execution use.

Conceptually:

> **Relevant Engineering Information + Applicable Engineering Semantics/Determinations → Engineering Composition → AI-oriented Engineering Projection**

Additional Engineering information may participate where required by the applicable activity and Engineering semantics.

AI Execution Composition is derived execution-supporting Engineering state.

It does not constitute a separate source of Engineering truth, Engineering authority, responsibility, governance, validation, or execution permission.

AI-oriented representation may restructure, summarize, encode, organize, or otherwise transform Engineering information for machine use.

Such transformation must preserve materially relevant:

- requirements;
- prohibitions;
- normative force;
- discretion;
- authority;
- applicability;
- governance and validation meaning;
- uncertainty and ambiguity;
- unresolved conditions;
- currency;
- provenance.

AI Execution Composition must not aggregate authority from multiple sources or participants.

It must not convert ambiguity, uncertainty, incomplete information, conflicting information, or unresolved Engineering conditions into invented certainty for the convenience of AI execution.

Where AI Execution Composition becomes materially significant to continuity, governance, validation, reconstruction, or subsequent Engineering activity, it may become durable through Durable State Establishment.

Durability does not make the AI Execution Composition authoritative.

An AI Engineer may resume Engineering activity through a different Execution Instance or AI runtime.

Resumption must therefore re-resolve materially relevant Engineering state and must not assume that a prior AI Execution Composition remains current merely because it is available.

> **Resumption requires re-resolution, not replay.**

---

## 9. Establishment Mechanisms

Establishment Mechanisms govern the realization of authoritative Engineering state and materially significant durable Engineering state.

The Establishment family consists of:

1. **Authoritative Engineering State Establishment** — establishes or transitions authoritative Engineering state through the mechanism owning that state according to applicable Engineering authority and semantics.
2. **Durable State Establishment** — establishes materially significant Engineering state as durable where that state must survive ephemeral boundaries.

The two mechanisms establish different Engineering characteristics.

Authoritative Engineering State Establishment concerns whether Engineering state has authoritative effect according to its owning Engineering semantics.

Durable State Establishment concerns whether Engineering state must survive loss or replacement of an ephemeral execution, participant, session, process, runtime, or representation boundary.

Therefore:

> **Authoritative establishment ≠ durable establishment.**

Authority and durability are orthogonal characteristics.

Authoritative Engineering state may be durable.

Derived Engineering state may be durable.

Execution-related Engineering state may be durable where materially required.

Making state durable does not make it authoritative, and establishing authoritative Engineering state does not by itself define how or where that state must be persisted.

The same implementation operation may realize both establishment responsibilities where both contracts are independently satisfied.

### 9.1 Authoritative Engineering State Establishment

#### Responsibility

Authoritative Engineering State Establishment establishes or transitions authoritative Engineering state through the mechanism owning that state according to applicable Engineering authority, semantics, lifecycle, integrity, and state-transition requirements.

In general:

> **Proposed State/Transition + Applicable Authority + Applicable Conditions + Owning Mechanism → Authoritative Engineering State**

The mechanism provides the architectural responsibility through which authoritative Engineering effect is established according to the semantics and authority of the mechanism owning that state.

It does not define a universal Platform-owned state-transition model.

The meaning of the authoritative state, its permissible transitions, applicable authority, required conditions, and consequences remain defined by the Engineering mechanism owning that state.

Establishment through the owning mechanism is a semantic requirement.

It does not require the owner to expose a particular API, service, repository, protocol, or remote state-transition interface.

#### Consumes

Authoritative Engineering State Establishment may consume:

- proposed Engineering state or a proposed state transition;
- the identity of the authoritative Engineering state being established or transitioned;
- applicable Engineering authority;
- applicable Engineering Determinations;
- applicable Engineering semantics;
- current authoritative Engineering state;
- lifecycle or state-transition requirements;
- Engineering Evidence where required;
- applicable constraints, preconditions, or integrity requirements;
- concurrency or version information;
- durable or derived Engineering state used as input or proposal;
- Execution Outcomes where relevant to the proposed establishment;
- Engineering Provenance;
- the authoritative mechanism responsible for owning the resulting state.

Inputs used to propose or support authoritative establishment do not acquire authoritative effect merely because they participate in the establishment interaction.

#### Produces

Authoritative Engineering State Establishment produces:

- authoritative Engineering state established or transitioned according to its owning semantics;
- the authoritative identity of the resulting state;
- the resulting lifecycle or state condition where applicable;
- the authoritative source or owning mechanism;
- applicable version, revision, or concurrency characteristics;
- the authority under which establishment occurred;
- applicable evidence and determination relationships;
- relevant temporal characteristics;
- relevant provenance;
- an explicit rejected, conflicted, unavailable, unsupported, invalid, stale, unauthorized, or otherwise unresolved establishment condition where authoritative establishment cannot validly occur.

A failed or unresolved establishment attempt must not be represented as successful authoritative state establishment.

#### Authority Characteristic

Authoritative Engineering State Establishment produces authoritative Engineering effect only through the semantics and authority of the mechanism owning the resulting state.

The Realization Mechanism does not manufacture authority.

It exercises or enables the exercise of already applicable authority through the owning mechanism.

Therefore:

> **Ability to write ≠ authority to establish.**

> **Successful persistence ≠ authoritative establishment.**

> **Successful transmission ≠ authoritative establishment.**

> **Synchronization ≠ authoritative establishment.**

> **Publication ≠ authoritative establishment.**

Physical storage location does not determine authoritative ownership.

An authoritative state owner may be realized inside or outside Platform infrastructure.

Where Engineering Determination and Authoritative Engineering State Establishment are realized atomically, the determination semantics, applicable authority, and authoritative establishment responsibilities must remain independently satisfied.

#### Must Preserve

Authoritative Engineering State Establishment must preserve, as applicable:

- authoritative Engineering entity identity;
- authoritative source and semantic ownership;
- applicable Engineering authority;
- authority scope and conditions;
- lifecycle and state semantics;
- valid state-transition semantics;
- required preconditions;
- normative force;
- Engineering relationships;
- evidence relationships;
- governance and validation meaning;
- concurrency requirements;
- version or revision semantics;
- idempotency requirements;
- conflict semantics;
- temporal characteristics;
- provenance.

Where establishment changes an existing authoritative state, the relationship between the prior and resulting authoritative state must remain consistent with the lifecycle, history, and transition semantics of the owning mechanism.

Where multiple authoritative mechanisms participate in an Engineering interaction, establishment in one mechanism must not silently establish corresponding authoritative state in another mechanism unless that second establishment independently satisfies its owning semantics and authority requirements.

#### Must Not Establish

Authoritative Engineering State Establishment must not independently:

- define the Engineering semantics of the state it establishes;
- manufacture, broaden, aggregate, or infer Engineering authority;
- infer authority merely from technical write access;
- bypass the owning mechanism's lifecycle or transition semantics;
- treat persistence as sufficient evidence of authoritative effect;
- treat synchronization or replication as authoritative establishment;
- convert derived Engineering state into authoritative Engineering state merely by changing its storage location or metadata;
- treat an Execution Outcome as authoritative Engineering state without the applicable Engineering semantics and establishment requirements;
- silently resolve concurrency or state conflicts in a manner not permitted by the owning semantics;
- establish authoritative state in another owning mechanism merely because related state was established successfully elsewhere;
- redefine governance, validation, responsibility, participation, execution, or lifecycle semantics owned elsewhere.

Derived or durable Engineering state may contribute to a proposed authoritative state or transition.

Where corresponding authoritative Engineering state is required, that state must be established through its owning mechanism rather than by promoting the authority characteristic of the derived or durable state.

#### Dependencies

Authoritative Engineering State Establishment may depend upon:

- Engineer Identity Resolution;
- Authoritative Engineering State Resolution;
- Participant State Resolution;
- Authority Resolution;
- Engineering Determination;
- Engineering Provenance;
- Durable State Establishment, where durable Engineering state contributes to the proposed establishment;
- Execution Invocation or Execution Outcomes, where technical execution contributes to the proposed authoritative state or transition.

Dependencies on execution do not allow execution to acquire authoritative Engineering effect independently.

Authoritative Engineering State Establishment may occur atomically with Engineering Determination or with persistence used for durability where the respective contracts remain independently satisfied.

### 9.2 Durable State Establishment

#### Responsibility

Durable State Establishment preserves materially significant Engineering state across ephemeral boundaries where loss of that state would materially impair Engineering continuity, reconstruction, governance, validation, provenance, or subsequent Engineering activity.

In general:

> **Materially Significant State + Durability Requirement → Durable Engineering State**

Durable State Establishment concerns survival of Engineering state.

It does not determine the authoritative meaning of that state.

Ephemeral Engineering state is permitted where its loss would not be materially significant according to applicable Engineering semantics.

#### Consumes

Durable State Establishment may consume:

- materially significant Engineering state;
- applicable materiality determinations;
- durability or continuity requirements;
- authoritative Engineering state requiring a durable representation;
- derived Engineering state;
- Engineering Compositions;
- Engineering Projections;
- Engineering Determinations;
- Engineering Evidence;
- material execution state;
- Execution Outcomes;
- Engineering Provenance;
- temporal, version, or source-reference information required for later interpretation or currency assessment.

Materiality may already be established or may require Engineering Determination.

Where materiality cannot yet be determined without preserving the state or associated provenance, sufficient information must remain available until the applicable materiality determination can be made.

#### Produces

Durable State Establishment produces:

- durable Engineering state capable of surviving the applicable ephemeral boundary;
- preserved identity or source references;
- preserved authority characteristic;
- preserved derivation characteristics;
- relevant temporal and version characteristics;
- relevant uncertainty, incompleteness, ambiguity, or conflict;
- relevant provenance;
- sufficient information to support later currency, applicability, reconstruction, or materiality determination where required;
- an explicit durability failure or unresolved condition where materially required state cannot be preserved sufficiently.

Durable establishment must preserve enough information to prevent later use from confusing a durable representation with a current or independently authoritative source.

#### Authority Characteristic

Durable State Establishment does not establish Engineering authority or authoritative Engineering state.

Therefore:

> **Persisted ≠ authoritative.**

> **Persisted ≠ current.**

> **Recoverable ≠ applicable.**

> **Retention duration ≠ authority.**

A durable representation of authoritative Engineering state remains a representation of that authoritative state unless the owning mechanism itself establishes the durable representation as authoritative according to its semantics.

A durable Derived Determination, Engineering Composition, Engineering Projection, Execution Outcome, or other derived state remains non-authoritative merely by becoming durable.

Authority and durability must therefore remain independently representable.

#### Must Preserve

Durable State Establishment must preserve, as applicable:

- Engineering identity;
- authoritative source identity or reference;
- authority characteristic;
- durability characteristic;
- derivation characteristic;
- source relationships;
- Engineering scope;
- normative force where represented;
- lifecycle or state semantics where represented;
- temporal characteristics;
- version or revision information;
- currency-relevant information;
- evidence relationships;
- governance and validation meaning;
- uncertainty, incompleteness, ambiguity, and conflict;
- provenance.

Where authoritative Engineering state is represented durably outside its owning mechanism, sufficient source identity, version, and temporal information must remain available to support later resolution and currency assessment.

Where derived state is made durable, its derivation from underlying Engineering information must remain traceable where materially required.

#### Must Not Establish

Durable State Establishment must not independently:

- create authoritative Engineering state;
- change the authority characteristic of Engineering state;
- establish Engineering authority;
- establish applicability;
- establish currency;
- establish governed-work responsibility;
- establish Execution Availability;
- establish governance or validation outcomes;
- establish Engineering completion;
- treat recoverability as evidence of current validity;
- treat retention duration as increased authority;
- treat a durable copy of authoritative state as an independently authoritative source;
- silently replace an authoritative source with a durable representation;
- convert derived or execution-related state into authoritative Engineering state through persistence, replication, synchronization, publication, or retention.

Durable State Establishment does not require all Engineering activity or execution state to become durable.

Engineering state whose preservation is materially required by applicable Engineering semantics must satisfy the applicable durability requirement. Other state may be persisted for implementation or operational purposes without thereby becoming materially required Durable Engineering State.

#### Dependencies

Durable State Establishment may depend upon:

- Engineering Determination, including materiality or durability-relevant determinations;
- Authoritative Engineering State Resolution;
- Engineering Composition;
- Engineering Projection;
- Engineering Provenance;
- Execution Invocation or Execution Outcomes where material execution state must survive ephemeral execution boundaries;
- Authoritative Engineering State Establishment where the state being preserved is itself authoritative.

Durable State Establishment must not require a prior conclusive materiality determination where loss of the state would prevent that determination from subsequently being made.

Where sufficient durable state already exists in an authoritative or otherwise adequate durable source, Durable State Establishment need not create a duplicate Platform-owned representation merely to satisfy durability.

### 9.3 Authority, Durability, and Derivation

Authority, durability, and derivation describe distinct characteristics of Engineering state.

They must not be collapsed into a single mutually exclusive state classification.

Conceptually, Engineering state may be described along at least the following independent dimensions:

- **Authority characteristic** — whether the state carries authoritative Engineering effect according to its owning semantics;
- **Durability characteristic** — whether the state survives the applicable ephemeral boundary;
- **Derivation characteristic** — whether the represented state is source state established or maintained by its applicable owning mechanism, or is derived from other Engineering information.

For example:

- authoritative Engineering state may be durable;
- a durable representation of authoritative Engineering state may remain derived and non-authoritative in its own right;
- Engineering Composition may be derived and ephemeral;
- Engineering Composition may be derived and durable;
- an Execution Outcome may be non-authoritative and ephemeral;
- materially significant execution state may be non-authoritative and durable.

Therefore, downstream information models must not assume:

> **authoritative | durable | derived | ephemeral**

to be one mutually exclusive classification.

The characteristics describe different architectural questions.

Persistence answers whether state survives.

Derivation answers how state relates to other Engineering information.

Authority answers whether state carries authoritative Engineering effect according to applicable Engineering semantics.

### 9.4 Establishment and State Transition

Establishment does not imply that every Engineering state change follows a universal Platform state-transition protocol.

Authoritative state transitions remain governed by the lifecycle and transition semantics of their owning mechanisms.

Durable State Establishment likewise does not create a Platform lifecycle for durable state.

A realization may use transactions, events, commands, synchronization, replication, workflows, append-only records, mutable records, content-addressed state, or other implementation approaches.

No such implementation approach independently determines authoritative Engineering meaning.

Where an interaction affects multiple authoritative mechanisms, each authoritative state establishment must remain valid according to the semantics and authority of its respective owner.

Technical atomicity across multiple mechanisms is not required by this Realization Model unless required by applicable Engineering semantics.

Where technical atomicity is unavailable, partial establishment, conflict, or failure must remain explicit where materially relevant and must not be represented as complete authoritative establishment.

### 9.5 Establishment and Correction

Correction, reversal, supersession, replacement, or rollback of Engineering state must preserve the distinction between technical state manipulation and authoritative Engineering change.

A technical rollback may reverse technical effects.

It does not by itself reverse authoritative Engineering state.

Therefore:

> **Technical rollback ≠ authoritative Engineering reversal.**

Where authoritative Engineering state must be corrected, reversed, superseded, or otherwise changed, the resulting authoritative state must satisfy the applicable owning semantics, authority, lifecycle, and Authoritative Engineering State Establishment requirements.

Where durable derived or execution-related state contains information that is later found to be incorrect, stale, superseded, or otherwise unsuitable for continued use, correction must preserve materially required provenance and must not silently rewrite authoritative history owned elsewhere.

Correction mechanisms may vary by implementation and owning semantics.

This Realization Model requires preservation of Engineering meaning and traceability, not a universal correction protocol.

---

## 10. Execution Mechanisms

Execution Mechanisms enable technical Engineering action while preserving the distinction between technical capability and Engineering availability.

The Execution family consists of:

1. **Constraint Enforcement** — technically enforces applicable execution-relevant constraints on execution surfaces controlled by the Platform.
2. **Execution Invocation** — invokes a selected Execution Mechanism to perform a technically available Engineering action.

Execution Mechanisms operate within Engineering semantics established elsewhere.

They do not independently establish:

- Engineer Identity;
- project participation;
- governed-work responsibility;
- Engineering authority;
- applicability of Engineering semantics or constraints;
- Execution Availability;
- governance or validation outcomes;
- authoritative Engineering state;
- Engineering completion.

Therefore:

> **Technical capability ≠ Engineering authority.**

> **Technical action ≠ authoritative Engineering effect.**

> **Execution success ≠ Engineering success.**

Constraint Enforcement and Execution Invocation may participate in a Controlled Execution pattern together with Resolution, Determination, Composition, Establishment, and Provenance mechanisms.

Such composition does not establish a mandatory universal execution sequence or a new Engineering lifecycle.

### 10.1 Constraint Enforcement

#### Responsibility

Constraint Enforcement makes applicable execution-relevant constraints technically effective on execution surfaces controlled by the Platform.

In general:

> **Applicable Constraint + Controlled Execution Surface → Enforced Execution Boundary**

Constraint Enforcement operates on constraints whose meaning, normative force, scope, applicability, and enforcement requirements have been established by their applicable Engineering semantics and mechanisms.

It enforces those constraints where technical enforcement is required and possible.

It does not determine what the constraint means or whether the constraint applies.

The architectural responsibility of Constraint Enforcement is limited to execution surfaces over which the Platform has sufficient technical control to enforce the applicable constraint.

#### Consumes

Constraint Enforcement may consume:

- applicable Participant Operating Constraints;
- other applicable execution-relevant constraints;
- independently established constraint-applicability determinations;
- enforcement requirements defined by applicable Engineering semantics;
- resolved Engineer Identity;
- resolved Participant State;
- Execution Capability information;
- selected or candidate Execution Mechanisms;
- Execution Environment information;
- the Engineering activity or technical operation being controlled;
- relevant Engineering Determinations;
- relevant durable Engineering state;
- Engineering Provenance.

Where constraint applicability remains unresolved, Constraint Enforcement must not silently infer applicability merely in order to enforce or ignore the constraint.

#### Produces

Constraint Enforcement produces, as applicable:

- an enforced execution boundary;
- technical restrictions on available execution operations;
- technical restrictions on Execution Capability use or Execution Mechanism exposure;
- enforcement status;
- enforcement evidence or other technically observable enforcement information;
- relevant provenance;
- an explicit unenforceable, partially enforceable, unavailable, unsupported, failed, uncertain, or unresolved enforcement condition where required enforcement cannot be sufficiently achieved.

An enforcement result describes the technical enforcement condition.

It does not independently determine the Engineering consequence of that condition.

#### Authority Characteristic

Constraint Enforcement is technical and non-authoritative with respect to the Engineering semantics of the constraint.

The source of a constraint and the mechanism enforcing that constraint remain distinct.

Therefore:

> **Constraint source ≠ constraint enforcer.**

> **Constraint applicability ≠ constraint enforcement.**

> **Knowing a constraint ≠ enforcing a constraint.**

> **Displaying a constraint ≠ enforcing a constraint.**

Technical enforcement does not increase, reduce, reinterpret, or otherwise alter the normative force of the constraint being enforced.

#### Must Preserve

Constraint Enforcement must preserve, as applicable:

- constraint identity;
- authoritative source or semantic owner;
- normative force;
- established applicability;
- Engineering scope;
- participant-relative scope;
- enforcement requirements;
- controlled execution surface;
- enforcement status;
- uncertainty or unresolved conditions;
- relevant provenance.

Constraint Enforcement must distinguish among constraints that are:

- technically enforceable on a Platform-controlled surface;
- communicable or exposable but not technically enforceable by the Platform;
- enforced by another mechanism or environment;
- not technically enforceable on the relevant execution surface.

The Platform must not claim technical enforcement where it does not control the relevant execution surface sufficiently to enforce the constraint.

#### Must Not Establish

Constraint Enforcement must not independently:

- define or modify Participant Operating Constraints;
- define or modify other Engineering constraints;
- establish constraint applicability;
- establish normative force;
- establish Engineering authority;
- establish governed-work responsibility;
- establish Participation Eligibility;
- establish Execution Availability;
- establish governance or validation outcomes;
- establish authoritative Engineering state;
- establish Engineering completion;
- determine the Engineering consequence of enforcement success or failure.

Constraint Enforcement must not reinterpret inability to enforce a constraint as permission to proceed.

Likewise, successful technical enforcement must not be interpreted as sufficient evidence that execution is otherwise available, authorized, governed, or valid.

#### Dependencies

Constraint Enforcement may depend upon:

- Engineer Identity Resolution;
- Authoritative Engineering State Resolution;
- Participant State Resolution;
- Engineering Determination, including constraint applicability or Execution Availability where relevant;
- Execution Capability Resolution;
- Engineering Provenance;
- Engineering Composition or Engineering Projection where applicable constraint information is supplied through a derived representation.

Where required enforcement cannot be achieved, the enforcement condition must remain explicit and must be available to the applicable Engineering Determination before execution proceeds where the owning Engineering semantics make enforcement relevant to Execution Availability.

Constraint Enforcement must not independently decide the Engineering consequence of its own enforcement failure.

### 10.2 Execution Invocation

#### Responsibility

Execution Invocation performs technical Engineering action by invoking a selected Execution Mechanism using an Execution Capability available for the applicable Engineering use.

In general:

> **Available Execution Capability + Selected Execution Mechanism + Applicable Inputs → Execution Invocation → Execution Outcome**

Execution Invocation is the Realization Mechanism through which technical action occurs.

It may invoke Human-operated tools, Engineering Automation, AI-oriented execution mechanisms, execution environments, or other technical mechanisms capable of performing the applicable Engineering action.

The executing mechanism is not thereby the Engineer responsible for the Engineering activity.

Therefore:

> **Execution Mechanism ≠ Engineer.**

> **Execution Instance ≠ Engineer Identity.**

> **Responsible Engineer ≠ executing mechanism.**

#### Consumes

Execution Invocation may consume:

- a technically available Execution Capability;
- a selected Execution Mechanism;
- an applicable Execution Availability determination, where required by the applicable Engineering semantics;
- applicable Engineering inputs;
- applicable constraints and enforcement conditions;
- resolved Engineer Identity;
- resolved Participant State;
- Engineering Composition;
- Engineering Projection;
- AI Execution Composition;
- Engineering Evidence where required as execution input;
- Execution Environment information;
- durable Engineering state;
- prior Execution Outcomes where relevant;
- technical configuration or invocation parameters;
- Engineering Provenance.

The presence of a technically available Execution Capability or accessible Execution Mechanism does not by itself establish that invocation is available for use.

Where the applicable Engineering semantics require Execution Availability or constraint enforcement before invocation, those conditions must be satisfied according to their owning semantics.

#### Produces

Execution Invocation produces an Execution Outcome.

An Execution Outcome may include:

- technical success;
- technical failure;
- partial technical outcome;
- interrupted execution;
- generated technical artifacts;
- modified technical state;
- diagnostics;
- execution evidence;
- materially significant execution state;
- Execution Instance relationships;
- relevant temporal information;
- relevant provenance.

Where execution cannot begin or continue, Execution Invocation must preserve an explicit unavailable, blocked, failed, interrupted, partial, uncertain, or otherwise unresolved technical condition as applicable.

An Execution Outcome remains a technical result until applicable Engineering semantics determine any broader Engineering consequence.

#### Authority Characteristic

Execution Invocation is technical.

Invocation does not independently establish authoritative Engineering effect.

Therefore:

> **Execution invocation ≠ authoritative Engineering state establishment.**

> **Execution Outcome ≠ Engineering Determination.**

> **Execution success ≠ Engineering success.**

> **Execution completion ≠ Engineering completion.**

> **Execution failure ≠ governance denial.**

> **Execution failure ≠ Validation Determination.**

A technically successful Execution Outcome may subsequently contribute to Engineering Evidence, Engineering Determination, or a proposed authoritative Engineering state transition.

Those subsequent Engineering effects require their respective mechanisms and applicable semantics.

#### Must Preserve

Execution Invocation must preserve, as applicable:

- identity of the invoked Execution Capability;
- identity of the selected Execution Mechanism;
- identity of the Execution Environment;
- Execution Instance identity;
- resolved Engineer Identity where participant attribution is relevant;
- responsible Engineer relationships where independently established;
- applicable Engineering inputs;
- applicable constraint and enforcement conditions;
- technical invocation parameters materially relevant to Engineering meaning or reconstruction;
- technical outcome semantics;
- partial, interrupted, failed, or uncertain execution conditions;
- generated or modified technical state;
- materially significant execution state;
- relevant evidence relationships;
- temporal characteristics;
- provenance.

Execution provenance must preserve the distinction between the Engineer responsible for Engineering work and the technical mechanism or Execution Instance that performed an action.

Where Human Engineers, AI Engineers, Engineering Automation, or other execution mechanisms participate in the same Engineering realization, actor and mechanism relationships must remain distinguishable.

#### Must Not Establish

Execution Invocation must not independently:

- create Engineer Identity;
- establish project participation;
- establish or transfer governed-work responsibility;
- establish Participation Eligibility;
- establish Engineering authority;
- establish Execution Availability;
- establish constraint applicability;
- establish governance or validation outcomes;
- establish authoritative Engineering state;
- establish Engineering completion;
- treat technical success as evidence sufficiency unless applicable Engineering semantics determine it;
- treat technical failure as governance denial, validation failure, or Engineering failure;
- convert generated technical artifacts into authoritative Engineering artifacts merely because execution produced them;
- infer responsibility from the mechanism or Execution Instance that performed the action.

Execution Invocation must not bypass applicable Engineering Determinations or required Constraint Enforcement merely because the selected Execution Mechanism is technically capable of performing the action.

### 10.3 Execution Outcome

Execution Outcome represents the technical result of Execution Invocation.

It is execution-related Engineering information rather than an Engineering Determination.

An Execution Outcome may be ephemeral or durable depending upon its material significance and applicable continuity requirements.

Where an Execution Outcome or associated execution state becomes materially significant to Engineering continuity, governance, validation, evidence, reconstruction, or subsequent Engineering activity, the applicable state may become durable through Durable State Establishment.

Durability does not make the Execution Outcome authoritative.

An Execution Outcome may contribute to:

- Engineering Evidence;
- Engineering Determination;
- subsequent Engineering Composition or Projection;
- subsequent Execution Invocation;
- proposed authoritative Engineering state establishment;
- Engineering Provenance.

Such use does not change the original technical meaning of the Execution Outcome.

A partial Execution Outcome must remain distinguishable from a complete Execution Outcome.

Therefore:

> **Partial outcome ≠ complete outcome.**

Where applicable Engineering semantics require a determination concerning the Engineering significance of an Execution Outcome, that determination belongs to Engineering Determination rather than Execution Invocation.

### 10.4 Execution Instance

An Execution Instance is a particular runtime occurrence through which an Execution Mechanism participates in Engineering execution.

An Execution Instance may correspond to, for example, a Human-operated tool session, automation run, AI runtime instance, isolated execution environment, or other runtime occurrence.

Execution Instance identity is distinct from Engineer Identity.

An Engineer may act through multiple Execution Instances.

An AI Engineer may resume Engineering activity through an Execution Instance different from the one previously used.

Replacement, termination, failure, or loss of an Execution Instance must not by itself alter:

- Engineer Identity;
- project participation;
- governed-work responsibility;
- Engineering authority;
- authoritative Engineering state.

Material execution state required beyond the lifetime of an Execution Instance must be capable of transition to durable Engineering state through Durable State Establishment.

Ephemeral execution state may remain local to an Execution Instance where its loss is not materially significant.

Execution Instance replacement does not justify reconstruction from hidden reasoning, participant memory, conversational trajectory, or undocumented runtime state.

Where Engineering activity resumes after Execution Instance replacement, materially relevant Engineering state must be re-resolved from authoritative sources and durable Engineering state as applicable.

Therefore:

> **Resumption requires re-resolution, not replay.**

### 10.5 Controlled Execution

Controlled Execution is a Realization Pattern in which applicable Realization Mechanisms cooperate to enable technical Engineering action while preserving Engineering authority, availability, constraints, evidence, and provenance.

A Controlled Execution interaction may involve:

- Engineer Identity Resolution;
- Authoritative Engineering State Resolution;
- Participant State Resolution;
- Authority Resolution;
- Execution Capability Resolution;
- Engineering Determination, including Execution Availability;
- Engineering Composition or Projection;
- Constraint Enforcement;
- Execution Invocation;
- Durable State Establishment;
- Authoritative Engineering State Establishment;
- Engineering Provenance.

A commonly useful interaction shape is:

> **Resolve Technical Capability → Determine Execution Availability → Enforce Applicable Constraints → Invoke Execution → Evaluate Outcome → Establish Required Engineering State**

This is an illustrative Realization Pattern.

It is not a mandatory universal sequence.

Individual interactions may omit, combine, reorder, repeat, or atomically realize mechanisms where the applicable Engineering semantics and individual Realization Contracts remain satisfied.

In particular:

- technical capability may be resolved without determining Execution Availability;
- Execution Availability may require information beyond technical capability;
- constraint applicability may be determined independently of execution;
- enforcement may occur within an Execution Environment or Execution Mechanism rather than as a separate technical operation;
- invocation and technical outcome production may be atomic;
- an Execution Outcome need not cause authoritative Engineering state establishment;
- authoritative Engineering state establishment may require additional governance, validation, evidence, or authority beyond successful execution.

Controlled Execution does not create a new Engineering lifecycle.

### 10.6 Automation and AI Execution

Engineering Automation and AI-oriented execution use the same foundational Execution Mechanisms as Human-operated execution.

Automation or AI participation does not create an alternate Engineering authority model.

Therefore:

> **Automation does not create responsibility or authority.**

> **AI execution does not create responsibility or authority.**

An AI Engineer, Human Engineer, Engineering Automation, Execution Mechanism, and Execution Instance must remain semantically distinguishable according to their respective Engineering roles.

AI Execution Composition may provide an AI-oriented Engineering Projection for Execution Invocation.

The projection does not itself grant Execution Availability or authority to act.

An AI runtime may technically possess capabilities whose use is unavailable for the current Engineering activity.

Those capabilities must remain technically distinguishable from the applicable Engineering permission or availability to use them.

Where AI or automation execution generates materially significant Engineering state, evidence, outcomes, or provenance, the same durability, determination, governance, validation, and authoritative-establishment requirements apply as for Human-operated execution.

No participant type receives authoritative Engineering effect merely because its execution mechanism can perform an action.

---

## 11. Engineering Provenance

Engineering Provenance preserves and resolves sufficient provenance for materially significant Engineering state, activity, determinations, evidence, compositions, projections, execution, and state establishments so that their relevant origins, derivations, relationships, and transformations remain traceable.

In general:

> **Materially Significant Engineering Activity/State + Relevant Relationships → Traceable Engineering Provenance**

Engineering Provenance is a cross-cutting Realization Mechanism.

It may participate in interactions involving any other foundational Realization Mechanism where provenance is materially required for:

- traceability;
- explanation;
- governance;
- validation;
- continuity;
- reconstruction;
- handover;
- resumption;
- accountability;
- subsequent Engineering activity.

Engineering Provenance does not create a universal Platform-owned history of Engineering.

Where sufficient provenance already exists in an authoritative or otherwise adequate durable source, the Platform may preserve the ability to resolve that provenance rather than duplicating it.

Therefore:

> **Provenance preservation requires sufficient traceability, not universal duplication.**

Engineering Provenance records or resolves materially relevant Engineering relationships.

It does not replace the Engineering state, evidence, responsibility, authority, determination, execution, or authoritative history to which those relationships refer.

### 11.1 Responsibility

Engineering Provenance preserves and resolves materially relevant information about the origin, derivation, transformation, participation, execution, determination, establishment, and relationships of Engineering information and activity.

Its responsibility is to make materially significant Engineering relationships traceable across:

- authoritative and derived Engineering state;
- durable and ephemeral boundaries;
- Human and AI participation;
- Execution Instances;
- Engineering Compositions and Projections;
- Engineering Determinations;
- Engineering Evidence;
- technical execution;
- authoritative state establishment;
- handover, reconstruction, and resumption.

Engineering Provenance must preserve distinctions among different kinds of Engineering relationships.

In particular:

> **Responsible Engineer ≠ executing mechanism.**

> **Execution Instance ≠ Engineer Identity.**

> **Evidence source ≠ determination authority.**

> **Derived from ≠ approved by.**

> **Produced by ≠ authoritative owner.**

> **Recorded by ≠ performed by.**

> **Performed by ≠ responsible for.**

> **Responsible for ≠ authorized to determine.**

A realization must not collapse these relationships into a generic actor, owner, author, creator, or provenance relationship where doing so would materially alter Engineering meaning.

### 11.2 Consumes

Engineering Provenance may consume provenance-relevant information concerning:

- Engineer Identity;
- project participation;
- governed-work responsibility;
- Engineering authority;
- authoritative Engineering state;
- derived Engineering state;
- durable Engineering state;
- Engineering Determinations;
- Engineering Evidence;
- Engineering Compositions;
- Engineering Projections;
- Execution Capabilities;
- Execution Mechanisms;
- Execution Environments;
- Execution Instances;
- Execution Outcomes;
- Constraint Enforcement;
- authoritative Engineering state establishment;
- durable state establishment;
- Engineering relationships;
- temporal, version, revision, or transition information;
- source references;
- derivation and transformation relationships;
- other provenance required by applicable Engineering semantics.

Engineering Provenance may consume technical telemetry, logs, audit records, runtime metadata, version-control information, execution traces, or other implementation information where those sources contribute materially relevant Engineering provenance.

Such technical information does not automatically constitute Engineering Provenance merely because it exists.

Provenance relevance must be established according to applicable Engineering semantics and materiality rather than treating all technically observable activity as equally significant Engineering provenance.

### 11.3 Produces

Engineering Provenance produces or makes resolvable, as applicable:

- provenance relationships among Engineering state and activity;
- source and origin relationships;
- derivation relationships;
- transformation relationships;
- Engineer participation relationships where independently established;
- governed-work responsibility relationships where independently established;
- authority relationships where independently established;
- evidence-source relationships;
- determination relationships;
- execution relationships;
- Execution Instance relationships;
- state-establishment relationships;
- temporal relationships;
- version or revision relationships;
- relevant handover, reconstruction, or resumption relationships;
- sufficient references to authoritative or durable provenance maintained elsewhere;
- explicit missing, incomplete, unavailable, inaccessible, uncertain, ambiguous, conflicting, or corrupted provenance conditions.

Engineering Provenance may be represented as directly preserved provenance information, references to provenance maintained elsewhere, or a composition of both.

Where provenance is distributed across multiple sources, the realization must preserve the ownership and meaning of the relevant constituent relationships.

A provenance representation must not become a competing authoritative source for Engineering state merely because it relates multiple authoritative sources.

### 11.4 Authority Characteristic

Engineering Provenance is non-substitutive.

It preserves or resolves relationships concerning Engineering authority and authoritative state without independently becoming the authority it describes.

Therefore:

> **Traceability to authority ≠ authority.**

> **Traceability to authoritative state ≠ authoritative state.**

> **Recorded responsibility ≠ established responsibility.**

> **Recorded authority ≠ established authority.**

> **Recorded determination ≠ Engineering Determination.**

> **Recorded execution ≠ Engineering completion.**

A provenance relationship may refer to an authoritative Engineering fact.

The authoritative characteristic of that fact remains anchored in its owning mechanism.

Where an authoritative mechanism itself owns authoritative provenance or history, Engineering Provenance may resolve or reference that information without assuming ownership of it.

### 11.5 Must Preserve

Engineering Provenance must preserve, as applicable:

- identity of materially relevant Engineering entities;
- identity of Engineer participants;
- identity of Execution Mechanisms;
- identity of Execution Instances;
- source identity;
- semantic ownership;
- authority characteristics;
- responsibility relationships;
- authority relationships;
- evidence relationships;
- determination relationships;
- derivation relationships;
- transformation relationships;
- execution relationships;
- state-establishment relationships;
- temporal ordering or characteristics where materially relevant;
- version or revision relationships;
- scope;
- applicable uncertainty, ambiguity, incompleteness, and conflict;
- provenance of provenance where required to establish the basis of a provenance relationship.

Provenance must preserve relationship semantics sufficiently to distinguish materially different Engineering meanings.

For example, a realization must preserve whether an Engineer:

- proposed a change;
- performed an action;
- was responsible for the governed work;
- supplied evidence;
- made a determination;
- exercised applicable authority;
- approved or validated an Engineering conclusion;

where those distinctions are materially relevant.

Likewise, where an AI Engineer acts through an AI runtime or other Execution Instance, provenance must preserve the distinction between:

- the durable Engineer Identity;
- the Execution Instance;
- the Execution Mechanism;
- the Engineering activity performed;
- the governed-work responsibility, where established;
- the authority exercised, where applicable.

Replacement of an Execution Instance must not break materially required provenance continuity.

### 11.6 Must Not Establish

Engineering Provenance must not independently:

- create Engineer Identity;
- establish project participation;
- establish governed-work responsibility;
- establish Participation Eligibility;
- establish Engineering authority;
- establish applicability;
- establish materiality;
- establish currency;
- establish Execution Availability;
- establish constraint applicability;
- establish governance or validation outcomes;
- establish Engineering Determinations;
- establish authoritative Engineering state;
- establish Engineering completion;
- establish Product acceptance;
- establish Release Admission;
- infer responsibility merely from technical execution;
- infer authority merely from recorded activity;
- infer approval merely from derivation or production;
- infer authoritative ownership merely from storage or provenance capture;
- replace Engineering Evidence;
- replace authoritative Engineering history owned elsewhere;
- fabricate missing provenance.

Engineering Provenance must not infer a stronger Engineering relationship merely because a weaker technical or Engineering relationship is observable.

For example:

> **Performed action ≠ accepted responsibility.**

> **Generated artifact ≠ owns artifact semantics.**

> **Observed state ≠ established state.**

> **Recorded event ≠ authoritative transition.**

Where a provenance relationship cannot be sufficiently established, the unresolved condition must remain explicit.

### 11.7 Provenance and Engineering Evidence

Engineering Provenance and Engineering Evidence are related but distinct.

Engineering Evidence is:

> **traceable information supporting a specific Engineering claim.**

Engineering Provenance describes materially relevant origins, derivations, relationships, transformations, and participation associated with Engineering information or activity.

Therefore:

> **Evidence ≠ provenance.**

> **Provenance ≠ evidence sufficiency.**

Provenance may support the credibility, traceability, interpretation, or admissibility of Engineering Evidence.

Engineering Evidence may itself carry provenance describing:

- where it originated;
- how it was produced;
- what Engineering activity produced it;
- which Execution Mechanism or Execution Instance was involved;
- which Engineer relationships are applicable;
- whether it was transformed;
- which Engineering state or determination it relates to.

The existence of provenance does not establish that information constitutes sufficient Engineering Evidence.

Evidence Sufficiency remains an Engineering Determination governed by the applicable Engineering semantics.

Likewise, information may constitute Engineering Evidence without requiring all underlying technical provenance to be retained where that technical detail is not materially required.

### 11.8 Provenance and Authoritative History

Engineering Provenance does not require the Platform to duplicate authoritative history maintained by another Engineering mechanism.

Where an authoritative source maintains sufficient history concerning:

- authoritative state;
- authoritative transitions;
- authority exercised;
- governed determinations;
- validation determinations;
- other authoritative Engineering relationships;

Engineering Provenance may preserve a durable relationship or resolvable reference to that history where sufficient for the applicable Engineering requirements.

Therefore:

> **Provenance resolvability ≠ provenance duplication.**

A Platform-owned provenance representation must not silently become a substitute authoritative history when the applicable history remains owned elsewhere.

Where authoritative history is unavailable, inaccessible, incomplete, or no longer resolvable, that condition must remain explicit.

Engineering Provenance must not reconstruct missing authoritative history by inference and represent that reconstruction as authoritative fact.

Derived reconstruction may be possible where useful, but its derived and uncertain characteristics must remain explicit.

### 11.9 Provenance Materiality and Durability

Not every technical operation, participant interaction, runtime event, or intermediate state requires durable Engineering Provenance.

Applicable Engineering semantics and materiality determine which provenance must remain durably resolvable.

Where materiality cannot be determined without provenance, sufficient provenance must remain available until the applicable materiality determination can be made.

Therefore:

> **Materiality may govern provenance retention, but provenance required to determine materiality must not be discarded first.**

Where provenance is materially required beyond an ephemeral boundary, it must remain durably resolvable through Durable State Establishment or through an authoritative or otherwise adequate durable source that already satisfies the applicable durability requirement.

Durable provenance may be achieved through:

- Durable State Establishment;
- an authoritative source that already preserves sufficient provenance;
- another adequate durable source;
- durable references to sufficient provenance maintained elsewhere;
- a composition of these approaches.

Durability does not make provenance authoritative over the Engineering information it describes.

Retention duration must be sufficient for applicable Engineering continuity and provenance requirements but does not itself increase provenance authority or significance.

### 11.10 Provenance Across Execution and Resumption

Engineering Provenance must support continuity across replacement, interruption, termination, or loss of Execution Instances where the associated Engineering activity is materially significant.

Execution provenance may include, as applicable:

- the Execution Capability used;
- the Execution Mechanism invoked;
- the Execution Environment;
- Execution Instance identity;
- resolved Engineer Identity;
- responsible Engineer relationships where independently established;
- applicable constraints and enforcement conditions;
- materially relevant inputs;
- materially relevant technical configuration;
- Execution Outcomes;
- generated or modified technical state;
- Engineering Evidence relationships;
- relevant temporal information.

Execution provenance must not infer responsibility or authority from execution.

Where Engineering activity resumes through another Execution Instance, the new instance may use materially relevant provenance together with authoritative sources and durable Engineering state to reconstruct the applicable Engineering situation.

Provenance may support reconstruction.

It does not replace re-resolution of authoritative Engineering state, Participant State, applicable determinations, constraints, currency, or other Engineering information whose current condition matters.

Therefore:

> **Provenance supports resumption; provenance does not freeze context.**

And:

> **Resumption requires re-resolution, not replay.**

Loss of an Execution Instance must not require preservation of hidden AI reasoning, Human recollection, conversational trajectory, or undocumented runtime state as Engineering Provenance.

Materially significant externally relevant Engineering state and relationships must instead be preserved through the applicable Engineering mechanisms.

### 11.11 Human and AI Provenance

Human Engineers and AI Engineers participate under the same Engineering provenance semantics.

Different execution mechanisms may produce different technical provenance.

Those differences do not create different standards for Engineering responsibility, authority, evidence, determination, or traceability.

A Human Engineer's cognitive process is not required to become Engineering Provenance.

An AI Engineer's hidden reasoning process is likewise not required to become Engineering Provenance.

The Platform requires provenance concerning materially significant Engineering state, actions, relationships, determinations, evidence, execution, and authoritative effects rather than private cognitive process.

Therefore:

> **Engineering Provenance concerns externally relevant Engineering relationships, not private reasoning traces.**

Human and AI participation may require different technical mechanisms for capturing provenance.

Those implementation differences must preserve the same underlying Engineering semantics.

---

## 12. Mechanism Composition

Realization Mechanisms cooperate through composition to support Engineering interactions that require multiple architectural responsibilities.

A **Mechanism Composition** is an interaction in which two or more foundational Realization Mechanisms contribute their respective responsibilities toward an Engineering purpose while retaining their individual contracts, authority characteristics, semantic boundaries, and ownership relationships.

Mechanism Composition does not create an additional foundational Realization Mechanism.

It does not create a new owner of Engineering semantics.

It does not create a universal execution sequence or Engineering lifecycle.

Therefore:

> **Composition of mechanisms ≠ composition of authority.**

And:

> **Mechanism cooperation ≠ semantic ownership transfer.**

A Mechanism Composition is valid only where each participating mechanism continues to satisfy its own Realization Contract and the interaction preserves the applicable Engineering semantics.

### 12.1 Composition Model

A Mechanism Composition may involve any valid combination of foundational Realization Mechanisms required by the applicable Engineering interaction.

Conceptually:

> **Engineering Need + Applicable Engineering Semantics + Required Realization Responsibilities → Mechanism Composition → Engineering Interaction Result**

The Engineering interaction determines which realization responsibilities are required.

The Realization Model does not prescribe a universal mechanism sequence from which all interactions must be constructed.

A composition may:

- use only a subset of foundational Realization Mechanisms;
- invoke a mechanism more than once;
- operate mechanisms concurrently;
- operate mechanisms conditionally;
- use previously established mechanism results where they remain sufficiently current and applicable for the Engineering interaction;
- revisit previously resolved or determined information;
- combine multiple mechanism responsibilities within one technical operation;
- distribute one mechanism responsibility across multiple technical operations;
- delegate mechanism responsibilities to existing Engineering Systems or authoritative mechanisms;
- terminate or remain unresolved without invoking every potentially available mechanism.

The validity of a composition depends upon preservation of the participating mechanism contracts rather than conformity to a common technical workflow.

### 12.2 Composition Independence

Each Realization Mechanism participating in a composition retains its architectural responsibility.

Participation in a composition must not broaden the meaning, authority, or responsibility of a mechanism beyond its Realization Contract.

For example:

- Discovery Resolution does not become Authoritative Engineering State Resolution because its result is immediately consumed by that mechanism;
- Participant State Resolution does not establish responsibility because its result contributes to Execution Availability;
- Engineering Determination does not acquire authority merely because Authority Resolution participates in the same interaction;
- Engineering Composition does not become authoritative because it contains authoritative Engineering state;
- Engineering Projection does not acquire the authority of the information it represents;
- Durable State Establishment does not establish authority because it occurs atomically with authoritative persistence;
- Constraint Enforcement does not establish constraint applicability because it consumes an applicability determination;
- Execution Invocation does not establish Engineering completion because its outcome contributes to a Validation Determination;
- Engineering Provenance does not establish responsibility, authority, or state because it records relationships concerning them.

Therefore:

> **Composition must preserve mechanism identity and responsibility.**

Implementation optimization may collapse multiple mechanism interactions into a single technical operation.

Such collapse must not erase the architectural distinctions necessary to determine whether each participating Realization Contract has been satisfied.

### 12.3 Dependency in Composition

A Realization Mechanism dependency identifies another mechanism whose result may be required for a particular Engineering interaction.

It does not establish mandatory global sequencing.

A dependency may be satisfied through:

- a result produced earlier in the same interaction;
- independently established Engineering state;
- a previously produced result that remains sufficiently current and applicable;
- an authoritative source;
- sufficiently durable Engineering state;
- another valid realization that satisfies the required mechanism contract.

A dependency must not be treated as satisfied merely because technically similar information is available.

The information satisfying the dependency must retain the semantic characteristics required by the consuming mechanism.

For example, a need for resolved authoritative Engineering state is not satisfied merely by the presence of a discovery result, cached representation, Engineering Composition, or Engineering Projection unless the applicable Authoritative Engineering State Resolution requirements are independently satisfied.

Likewise, a need for applicable Engineering authority is not satisfied merely because responsibility, participation, technical access, or execution capability is known.

### 12.4 Reciprocal Composition

Realization Mechanisms may participate in reciprocal interactions where they operate over different Engineering questions, state, or points in an Engineering interaction.

For example:

- Participant State Resolution may consume an independently established Engineering Determination, while another Engineering Determination may subsequently consume resolved Participant State;
- Authority Resolution may consume an independently established Engineering Determination concerning an authority condition, while another determination may require resolved authority before authoritative effect can be established;
- Engineering Composition may consume Engineering Determinations, while a determination may operate over information supplied through an Engineering Composition;
- Engineering Projection requirements may influence the information required in an Engineering Composition, while Projection may subsequently consume that Composition;
- Engineering Provenance may consume relationships produced by other mechanisms while those mechanisms may subsequently resolve provenance relevant to their own operation.

Such reciprocal composition is valid where each interaction has an independently grounded semantic basis.

It must not create circular semantic justification.

Therefore:

> **Reciprocal interaction ≠ circular establishment.**

A mechanism must not depend transitively upon the authority, determination, applicability, responsibility, state, or other Engineering meaning that the same interaction is attempting to establish unless independently established Engineering state provides the required semantic anchor.

Where such an anchor cannot be established, the applicable unresolved condition must remain explicit.

### 12.5 Atomic Composition

Multiple Realization Mechanisms may be realized atomically through the same technical operation or implementation mechanism.

Atomic realization does not merge their architectural responsibilities.

Examples may include:

- Engineering Determination and Authoritative Engineering State Establishment;
- Authoritative Engineering State Establishment and Durable State Establishment;
- Constraint Enforcement and Execution Invocation;
- Execution Invocation and production of materially significant execution provenance;
- Engineering Composition and Engineering Projection.

Where mechanisms are realized atomically:

- each applicable Realization Contract must remain satisfied;
- authority requirements must remain independently valid;
- authoritative and derived characteristics must remain distinguishable;
- durability must not be confused with authority;
- technical success must not substitute for an Engineering Determination;
- provenance must preserve materially relevant relationships;
- failure or partial completion must remain explicit where materially relevant.

Therefore:

> **Atomic realization ≠ semantic collapse.**

An implementation need not expose the internal boundaries among atomically realized mechanisms where those boundaries are not externally required.

It must nevertheless preserve sufficient architectural meaning to demonstrate conformance with the applicable Realization Contracts.

### 12.6 Distributed Composition

A Mechanism Composition may span multiple:

- Engineering Systems;
- authoritative mechanisms;
- execution environments;
- services;
- repositories;
- processes;
- tools;
- Human interactions;
- AI runtimes;
- external systems.

Distribution does not create a new semantic owner for the interaction as a whole.

Each authoritative Engineering concern remains owned by its applicable mechanism.

Where information crosses implementation, system, or execution boundaries, the composition must preserve materially relevant:

- identity;
- source ownership;
- authority characteristic;
- derivation characteristic;
- normative force;
- scope;
- applicability;
- constraints;
- evidence relationships;
- determination relationships;
- uncertainty;
- currency;
- provenance.

Technical transfer, synchronization, messaging, replication, caching, or publication between participants in a distributed composition does not independently establish authoritative Engineering effect.

Where part of a distributed composition is unavailable, inaccessible, stale, conflicted, or otherwise unresolved, the composition must preserve that condition where it materially affects the Engineering interaction.

### 12.7 Composition and State

Mechanism Composition may operate over Engineering state with different authority, durability, and derivation characteristics.

Participation of state in a composition does not change its architectural characteristics merely because another mechanism consumes it.

In particular:

> **Consumption ≠ authority transfer.**

> **Composition ≠ authoritative promotion.**

> **Persistence during composition ≠ authoritative establishment.**

> **Execution during composition ≠ Engineering determination.**

A composition may produce multiple kinds of state or results.

For example, the same Engineering interaction may produce:

- an Execution Outcome;
- Engineering Evidence;
- a Derived Determination;
- durable Engineering state;
- Engineering Provenance;
- proposed authoritative Engineering state;
- established authoritative Engineering state.

These results remain distinct according to the Realization Mechanisms and Engineering semantics responsible for them.

A realization must not collapse them into a generic interaction status such as `success`, `complete`, `approved`, or `done` where doing so would erase materially different Engineering meanings.

### 12.8 Composition Failure and Partial Results

A Mechanism Composition need not produce a single binary success or failure result.

Individual participating mechanisms may produce:

- successful results;
- partial results;
- unresolved conditions;
- unavailable or inaccessible conditions;
- stale or uncertain information;
- conflicting information;
- rejected establishment;
- failed execution;
- unenforceable constraints;
- other outcomes defined by their applicable contracts.

A failure or unresolved condition in one mechanism does not automatically define the Engineering meaning of the overall interaction.

The applicable Engineering semantics determine whether:

- the interaction may continue;
- another mechanism may be used;
- reassessment is required;
- additional evidence is required;
- execution remains unavailable;
- authoritative establishment is prohibited;
- a partial result may be retained;
- another Engineering consequence applies.

Therefore:

> **Mechanism failure ≠ universal Engineering failure.**

Likewise:

> **Mechanism success ≠ universal Engineering success.**

Where partial results are materially significant, their identity, status, uncertainty, durability requirements, and provenance must remain explicit.

### 12.9 Realization Patterns

A **Realization Pattern** is a reusable description of Mechanism Composition for a recurring Engineering interaction.

A Realization Pattern may identify:

- the Engineering concern being addressed;
- the foundational Realization Mechanisms that may participate;
- relevant dependencies among those mechanisms;
- applicable Engineering state;
- significant interaction conditions;
- expected categories of result;
- unresolved or failure conditions that must remain explicit;
- provenance or durability requirements.

A Realization Pattern does not establish new foundational architectural responsibility merely by naming a recurring composition.

Examples include:

- Engineering Entry;
- Engineering Reconstruction;
- handover;
- resumption;
- context re-resolution;
- context challenge;
- Controlled Execution;
- Engineering Automation;
- AI Execution Composition.

Realization Patterns may be specialized for particular Engineering Systems, Development Standards, participant types, or Engineering activities.

Such specialization must preserve the underlying Realization Contracts and applicable Engineering semantics.

### 12.10 Pattern Non-Lifecycle

A Realization Pattern may describe an expected or useful interaction shape.

It does not establish a canonical Engineering lifecycle.

A pattern must not imply that:

- every Engineering interaction begins at the same mechanism;
- every mechanism must participate;
- mechanisms execute exactly once;
- mechanisms execute in a fixed universal order;
- progression through the pattern creates authoritative lifecycle state;
- completion of the pattern establishes Engineering completion;
- technical progression establishes governance or validation outcomes.

Therefore:

> **Realization Pattern ≠ Engineering lifecycle.**

An Engineering lifecycle may use Realization Patterns.

A Realization Pattern may operate within one or more Engineering lifecycle states.

Neither relationship transfers ownership of lifecycle semantics to the Realization Model.

### 12.11 Human and AI Composition

Mechanism Composition applies equally to Engineering interactions involving Human Engineers and AI Engineers.

Human and AI participation may use different:

- Engineering Projections;
- Execution Mechanisms;
- Execution Environments;
- participant interfaces;
- technical constraint-enforcement mechanisms;
- provenance-capture mechanisms.

These differences must not create different underlying rules for:

- Engineer Identity;
- project participation;
- governed-work responsibility;
- Engineering authority;
- applicability;
- Engineering Determination;
- authoritative Engineering state;
- governance;
- validation;
- durability;
- provenance.

An AI-oriented composition may automate or combine multiple mechanism interactions.

Automation does not exempt the composition from satisfying the applicable Realization Contracts.

Likewise, a Human-oriented workflow may leave some mechanism boundaries implicit in the participant experience.

Implicit presentation does not eliminate the underlying architectural responsibilities.

Therefore:

> **Participant experience may differ; Engineering semantics must not.**

### 12.12 Composition Conformance

A Mechanism Composition conforms to the Realization Model where:

1. each required foundational Realization Mechanism satisfies its applicable Realization Contract;
2. the composition does not create semantic ownership not established elsewhere;
3. authoritative Engineering state is established only according to its owning semantics and applicable authority;
4. derived state does not acquire aggregate authority through composition;
5. durability does not establish authority;
6. technical capability or execution does not establish Engineering permission, determination, or completion;
7. reciprocal dependencies do not create circular semantic justification;
8. materially relevant uncertainty, partial results, conflicts, and failure conditions remain explicit;
9. materially relevant provenance remains sufficiently resolvable;
10. Human and AI participation preserve the same underlying Engineering semantics.

Conformance concerns architectural meaning rather than technical topology.

Two implementations may use substantially different technical architectures while conforming to the same Mechanism Composition requirements.

---

## 13. State Characteristics

The Engineering Platform Realization Model operates over Engineering state with characteristics that determine how that state may be interpreted, preserved, resolved, composed, projected, established, executed against, and traced.

These characteristics describe architectural properties of Engineering state.

They do not define a universal Engineering state model, lifecycle, storage model, or physical data schema.

Different Engineering Systems and authoritative mechanisms may define different:

- Engineering entities;
- lifecycle states;
- state-transition models;
- authority models;
- persistence models;
- versioning models;
- temporal semantics;
- information structures.

The Realization Model requires Platform realizations to preserve the materially relevant characteristics of that state without replacing the semantics owned by those mechanisms.

At minimum, the Realization Model distinguishes three independent state-characteristic dimensions:

1. **Authority Characteristic**
2. **Durability Characteristic**
3. **Derivation Characteristic**

These dimensions are independent.

Therefore:

> **Authority ≠ durability ≠ derivation.**

A realization must not collapse them into one mutually exclusive classification.

### 13.1 Authority Characteristic

The **Authority Characteristic** describes whether Engineering state carries authoritative Engineering effect according to the semantics and authority of its owning mechanism.

Engineering state is authoritative only where its applicable owning mechanism establishes that state as authoritative according to its Engineering semantics.

Authoritative Engineering state retains, as applicable:

- authoritative identity;
- semantic ownership;
- authoritative source;
- applicable authority;
- normative force;
- scope;
- lifecycle or state semantics;
- relationships;
- temporal characteristics;
- version or revision characteristics;
- provenance.

A representation of authoritative Engineering state does not automatically carry the authority of the state it represents.

Therefore:

> **Authoritative source state ≠ authoritative representation.**

Examples of representations that may refer to or contain authoritative Engineering state without independently becoming authoritative include:

- discovery results;
- cached representations;
- indexes;
- Participant State;
- Engineering Compositions;
- Engineering Projections;
- durable copies;
- execution-supporting context;
- provenance representations.

Such representations must preserve the authority characteristic of the underlying information while remaining distinguishable from the authoritative source or state they represent.

Authority characteristic is established according to Engineering ownership and applicable semantics.

It is not established by:

- persistence;
- physical storage location;
- technical write access;
- replication;
- synchronization;
- publication;
- discovery;
- composition;
- projection;
- execution;
- provenance capture.

Where authoritative Engineering state is created or changed, the Authoritative Engineering State Establishment contract applies.

### 13.2 Durability Characteristic

The **Durability Characteristic** describes whether Engineering state survives the applicable ephemeral boundary.

A state is durable where it remains sufficiently available beyond the lifetime of the execution, session, participant interaction, process, runtime, representation, or other ephemeral boundary for which preservation is materially required.

Durability concerns preservation.

It does not establish:

- authority;
- applicability;
- currency;
- normative force;
- responsibility;
- governance or validation outcome;
- Engineering completion.

Therefore:

> **Durable ≠ authoritative.**

And:

> **Persisted ≠ current.**

Engineering state may be durable because:

- its owning authoritative mechanism already preserves it durably;
- Durable State Establishment preserves it;
- another adequate durable source preserves it;
- a durable reference permits sufficient resolution of the required state or provenance.

Durability does not require Platform-local duplication.

Where materially required Engineering state is already sufficiently durable and resolvable from another source, a Platform realization need not create another durable copy merely to satisfy the durability characteristic.

Durability requirements are determined by applicable Engineering semantics, materiality, continuity requirements, and the ephemeral boundary that must be survived.

A realization may persist information for technical or operational reasons without that information thereby becoming materially required Durable Engineering State.

### 13.3 Derivation Characteristic

The **Derivation Characteristic** describes how represented Engineering state relates to source Engineering information.

At minimum, a realization must be capable of distinguishing between:

- **source state** — Engineering state established or maintained by its applicable owning mechanism;
- **derived state** — Engineering state assembled, calculated, transformed, summarized, selected, aggregated, projected, reconstructed, or otherwise produced from other Engineering information.

Derivation does not itself determine authority.

Source state may be authoritative where its owning semantics establish authoritative effect.

Derived state does not acquire aggregate authority merely because it is derived from authoritative Engineering state.

Therefore:

> **Derived from authoritative state ≠ independently authoritative state.**

Derived Engineering state may include, for example:

- Participant State;
- discovery results;
- Engineering Compositions;
- Engineering Projections;
- Derived Determinations;
- reconstructed Engineering views;
- execution-supporting context;
- AI Execution Composition;
- provenance compositions or representations.

Derived state must preserve materially relevant relationships to the Engineering information from which it was derived.

This may include, as applicable:

- source identity;
- semantic ownership;
- authority characteristic;
- normative force;
- scope;
- applicability;
- temporal or version characteristics;
- uncertainty;
- derivation relationships;
- provenance.

Transformation of Engineering information must not silently change its authority characteristic or Engineering meaning.

### 13.4 Independence of State Characteristics

Authority, durability, and derivation answer different architectural questions.

**Authority Characteristic** asks:

> Does this state carry authoritative Engineering effect according to its owning semantics?

**Durability Characteristic** asks:

> Must or does this state survive the applicable ephemeral boundary?

**Derivation Characteristic** asks:

> Is this represented state source state maintained by its applicable owner, or is it derived from other Engineering information?

These questions must remain independently answerable.

Valid combinations may therefore include:

| Authority | Durability | Derivation | Example |
|---|---|---|---|
| Authoritative | Durable | Source | authoritative Engineering state durably maintained by its owning mechanism |
| Non-authoritative | Durable | Derived | durable Engineering Composition retained for continuity |
| Non-authoritative | Ephemeral | Derived | transient Engineering Projection |
| Non-authoritative | Durable | Derived | durable representation of authoritative Engineering state maintained outside its owning mechanism |
| Non-authoritative | Ephemeral | Source | source state of a non-authoritative technical mechanism whose preservation is not materially required |

Source state in the derivation dimension does not imply authoritative state. It identifies state established or maintained by its applicable owning mechanism rather than state derived from other Engineering information.

The table illustrates possible combinations.

It does not define a closed state taxonomy.

Other combinations may be valid where supported by applicable Engineering semantics.

In particular, a realization must not model Engineering state as one mutually exclusive enumeration such as:

> `authoritative | durable | derived | ephemeral`

Such a representation would collapse independent architectural characteristics and permit invalid semantic inference.

### 13.5 Temporal and Currency Characteristics

Engineering state may possess temporal characteristics relevant to its interpretation or use.

These may include, as applicable:

- creation or establishment time;
- effective time;
- observation time;
- resolution time;
- modification time;
- version or revision;
- validity period;
- supersession;
- expiration;
- last-known source condition;
- other temporal characteristics defined by the owning Engineering semantics.

Temporal characteristics do not independently establish currency.

Currency is an Engineering Determination where applicable Engineering semantics require determination of whether Engineering information remains sufficiently current for a defined Engineering use.

Therefore:

> **Persisted ≠ current.**

> **Recently resolved ≠ necessarily current for every Engineering use.**

> **Previously applicable ≠ currently applicable.**

A durable representation of authoritative Engineering state must retain sufficient source, temporal, version, and provenance information to support later currency assessment where required.

Where current authoritative state matters, a realization must not treat the continued availability of an older durable or derived representation as proof of currency.

### 13.6 Applicability and State

Applicability is not an inherent consequence of Engineering state being:

- authoritative;
- resolved;
- durable;
- discovered;
- included in an Engineering Composition;
- represented in an Engineering Projection;
- available to an execution mechanism.

Applicability is governed by the applicable Engineering semantics and may require Engineering Determination.

Therefore:

> **Available state ≠ applicable state.**

And:

> **Authoritative state ≠ universally applicable state.**

A realization must preserve established applicability, inapplicability, unresolved applicability, scope, and the basis for those characteristics where materially relevant.

Derived state must not silently establish applicability by inclusion or inapplicability by omission.

Where applicability changes, persisted Engineering Compositions, Projections, Participant State, execution-supporting context, or other derived state must not be assumed to remain applicable merely because they remain available.

### 13.7 Uncertainty and State

Engineering state may carry materially relevant uncertainty, ambiguity, incompleteness, conflict, unsupported conditions, or unresolved characteristics.

Such conditions are part of the Engineering meaning of the state where materially relevant.

They must not be discarded merely to make the state easier to:

- persist;
- compose;
- project;
- execute against;
- summarize;
- transmit;
- index;
- reconstruct;
- consume by an AI Engineer.

Therefore:

> **Representation of state must preserve material uncertainty.**

A derived representation must not present greater certainty than is supported by its underlying Engineering information and applicable Engineering Determinations.

Where conflicting authoritative sources exist, aggregation or composition must not silently manufacture a single authoritative resolution unless the applicable Engineering semantics provide a mechanism for resolving that conflict.

Where state cannot be sufficiently resolved, the applicable unresolved condition must remain explicit.

### 13.8 State Identity and Relationships

Engineering state must retain sufficient identity and relationship information to preserve its Engineering meaning across Realization Mechanisms.

Depending upon the applicable Engineering semantics, this may include:

- Engineering entity identity;
- authoritative source identity;
- semantic owner;
- participant identity;
- scope;
- lifecycle relationship;
- version or revision relationship;
- derivation relationship;
- evidence relationship;
- determination relationship;
- responsibility relationship;
- authority relationship;
- execution relationship;
- provenance relationship.

A representation must not infer a stronger Engineering relationship from a weaker one.

For example:

> **Reference to state ≠ ownership of state.**

> **Derivation from state ≠ approval of state.**

> **Execution against state ≠ responsibility for state.**

> **Persistence of state ≠ authority over state.**

State identity must remain sufficiently stable to support traceability where the same Engineering concern is resolved, represented, persisted, or acted upon through different Realization Mechanisms.

### 13.9 State Across Realization Boundaries

Engineering state may cross:

- capability boundaries;
- Engineering System boundaries;
- implementation-component boundaries;
- service boundaries;
- persistence boundaries;
- execution-environment boundaries;
- Human/AI participant boundaries;
- ephemeral/durable boundaries.

Crossing a boundary must not by itself silently alter the state's:

- identity;
- semantic ownership;
- authority characteristic;
- derivation characteristic;
- normative force;
- scope;
- applicability;
- lifecycle or state semantics;
- uncertainty;
- temporal characteristics;
- provenance.

A boundary crossing may change the durability characteristic where the applicable durability requirement is satisfied through Durable State Establishment or another adequate durable source. Such a change must remain distinguishable from changes in authority, derivation, or Engineering meaning.

A receiving mechanism may create a new derived representation of the state.

Where it does, the relationship between the representation and its source must remain sufficiently traceable.

Transfer, synchronization, replication, caching, indexing, serialization, transformation, or projection must not independently establish authoritative Engineering effect.

### 13.10 State and Reconstruction

Reconstruction uses authoritative sources and durable Engineering state to recover a sufficiently grounded Engineering situation after interruption, handover, execution-instance replacement, or other continuity boundary.

Reconstruction may use:

- authoritative Engineering state;
- durable derived state;
- Engineering Provenance;
- prior Engineering Determinations;
- Engineering Evidence;
- Execution Outcomes;
- durable Engineering Compositions or Projections;
- other materially relevant durable Engineering state.

Reconstruction does not make historical state current merely by recovering it.

It does not establish that prior:

- applicability;
- Participant State;
- Engineering authority;
- Execution Availability;
- applicable constraints and their applicability;
- determinations;
- context;

remain current.

Where those characteristics matter to resumed Engineering activity, they must be re-resolved or re-determined according to applicable Engineering semantics.

Therefore:

> **Reconstruction ≠ current-state resolution.**

And:

> **Resumption requires re-resolution, not replay.**

Reconstruction must not depend upon hidden AI reasoning, Human recollection, conversational trajectory, or undocumented runtime state as authoritative Engineering state.

### 13.11 State Representation Requirements

A Platform realization need not represent every state characteristic using a dedicated physical field or common schema.

It must, however, be capable of preserving and resolving the materially relevant characteristics required by the applicable Realization Contracts and Engineering semantics.

Depending upon the Engineering information concerned, this may require representation of:

- identity;
- source;
- semantic ownership;
- authority characteristic;
- durability characteristic;
- derivation characteristic;
- normative force;
- scope;
- applicability;
- lifecycle or state semantics;
- temporal and version characteristics;
- currency;
- uncertainty and conflict;
- evidence relationships;
- determination relationships;
- responsibility relationships;
- authority relationships;
- execution relationships;
- provenance.

These characteristics may be represented:

- directly;
- by reference;
- through relationships;
- through authoritative source resolution;
- through durable Engineering state;
- through other implementation structures that preserve the required Engineering meaning.

The Realization Model does not require one canonical Platform-wide state object containing all characteristics.

Therefore:

> **Common semantics ≠ common physical schema.**

A downstream Engineering Platform Information Model may define common information structures, identifiers, relationships, or representation conventions where useful.

Such structures must preserve the independence and ownership boundaries established by this specification.

### 13.12 Human and AI State Semantics

Human Engineers and AI Engineers operate over the same underlying Engineering state semantics.

Different participant types may receive different Engineering Projections or use different execution-supporting representations.

Those differences must not create different authority, durability, derivation, applicability, currency, or provenance semantics for the same underlying Engineering information.

An AI-oriented representation may be optimized for machine interpretation.

A Human-oriented representation may be optimized for comprehension and interaction.

Neither representation may silently:

- strengthen authority;
- weaken normative force;
- remove material constraints;
- manufacture applicability;
- erase material uncertainty;
- convert derived state into source state;
- treat historical state as current;
- alter responsibility or authority relationships.

Therefore:

> **Participant-specific representation ≠ participant-specific Engineering truth.**

---

## 14. Capability Realization Mapping

The foundational Realization Mechanisms collectively provide the architectural responsibilities required to realize the six Engineering Capabilities defined by the Engineering Capability Model.

Capability realization is many-to-many.

An Engineering Capability may require multiple Realization Mechanisms.

A Realization Mechanism may contribute to multiple Engineering Capabilities.

Therefore:

> **Capability realization ≠ capability-to-mechanism assignment.**

The mapping defined in this section identifies which foundational Realization Mechanisms may provide architectural responsibilities required by each Engineering Capability.

It does not transfer semantic ownership from the capability to the Realization Mechanism.

It does not require a dedicated implementation component for either the capability or the mechanism.

It does not establish a mandatory runtime interaction among the mapped mechanisms.

The applicable capability specification remains authoritative for the semantic responsibilities, boundaries, and invariants of that capability.

### 14.1 Mapping Semantics

A Realization Mechanism is mapped to an Engineering Capability where the mechanism provides a foundational architectural responsibility required to make one or more responsibilities of that capability realizable.

A mapping means:

> **This capability may require this realization responsibility.**

A mapping does not mean:

> **This mechanism owns this capability or its Engineering semantics.**

Nor does a mapping imply that the mechanism must participate in every interaction involving the capability.

The mechanisms actually required for an Engineering interaction depend upon:

- the Engineering concern being addressed;
- applicable Engineering semantics;
- available authoritative and durable Engineering state;
- participant-relative requirements;
- applicable determinations;
- execution requirements;
- provenance requirements;
- other materially relevant conditions.

The absence of a mechanism from a particular interaction does not indicate that the corresponding capability is absent where the capability's required semantics are otherwise satisfied.

Likewise, the presence of a mechanism does not imply that every capability mapped to that mechanism is participating in the interaction.

A mechanism may also consume semantics owned by one capability while providing its realization responsibility to another capability; such consumption does not by itself establish a realization mapping to the semantic-owning capability.

### 14.2 Discovery & Navigation

The **Discovery & Navigation** capability enables Engineering participants and mechanisms to locate, navigate, relate, and inspect Engineering information without converting discovery into authority, applicability, or authoritative ownership.

Its realization may use:

- **Discovery Resolution** — to resolve Engineering discovery needs into candidate Engineering information, identities, relationships, source references, and navigation targets;
- **Authoritative Engineering State Resolution** — to resolve authoritative Engineering state once an authoritative entity or source is known or identified;
- **Engineer Identity Resolution** — where discovery or navigation is participant-relative;
- **Participant State Resolution** — where participant-relative scope or state legitimately affects discovery or navigation;
- **Engineering Determination** — where relevance, applicability, currency, materiality, or another Engineering question requires determination rather than discovery;
- **Engineering Composition** — where discovered or resolved Engineering information must be assembled for navigation, inspection, or an Engineering concern;
- **Engineering Projection** — where Engineering information must be represented for a Human Engineer, AI Engineer, interface, or other consumer;
- **Engineering Provenance** — where origin, relationship, history, or traceability supports discovery and navigation.

Discovery & Navigation retains ownership of its capability semantics.

In particular:

> **Discovery ≠ authoritative resolution.**

> **Relevance ≠ applicability.**

> **Navigation relationship ≠ authoritative Engineering relationship.**

Execution, authoritative state establishment, and durable state establishment may participate in broader Engineering interactions reached through discovery, but they are not implied merely by discovery or navigation.

### 14.3 Participation & Scope

The **Participation & Scope** capability governs how Engineer identity, project participation, governed-work responsibility, participation eligibility, participant-relative constraints, and related Engineering scope are understood while preserving their semantic distinctions.

Its realization may use:

- **Engineer Identity Resolution** — to resolve the durable Engineer Identity participating in Engineering;
- **Authoritative Engineering State Resolution** — to resolve authoritative participation, responsibility, scope, constraint, or related Engineering state;
- **Participant State Resolution** — to resolve participant-relative Engineering state for a defined Engineering scope or concern;
- **Authority Resolution** — where applicable Engineering authority concerning participation, responsibility, or related state must be resolved;
- **Engineering Determination** — for Participation Eligibility, constraint applicability, or other participation-related Engineering determinations;
- **Engineering Composition** — to assemble participant-relative Engineering information for an activity or concern;
- **Engineering Projection** — to represent participant-relative Engineering information appropriately for the participant or consuming mechanism;
- **Authoritative Engineering State Establishment** — where participation, governed-work responsibility, transfer, release, or another authoritative participation-related state is established or changed;
- **Durable State Establishment** — where materially significant participant-related derived state must survive an ephemeral boundary;
- **Engineering Provenance** — to preserve materially relevant participation, responsibility, authority, transfer, and related provenance.

Where participation-related constraints require technical enforcement during execution, **Constraint Enforcement** may enforce them on Platform-controlled execution surfaces after their meaning and applicability have been established.

Participation & Scope retains ownership of participation semantics.

In particular:

> **Engineer Identity ≠ project participation.**

> **Participation ≠ governed-work responsibility.**

> **Responsibility ≠ authority.**

> **Responsibility ≠ execution.**

> **Constraint applicability ≠ constraint enforcement.**

Technical execution must not create participation or governed-work responsibility merely because an Engineer or Execution Mechanism performs an action.

### 14.4 Context Resolution & Composition

The **Context Resolution & Composition** capability governs resolution and composition of Engineering information required to establish sufficiently grounded Engineering context for an activity, concern, participant, or point of interaction.

Its realization may use:

- **Engineer Identity Resolution** — where context is participant-relative;
- **Authoritative Engineering State Resolution** — to resolve authoritative Engineering information contributing to context;
- **Participant State Resolution** — to resolve participant-relative state contributing to context;
- **Discovery Resolution** — to locate candidate Engineering information or sources relevant to context construction;
- **Authority Resolution** — where authority information is materially relevant to the context;
- **Execution Capability Resolution** — where technical capability information is materially relevant to the Engineering activity;
- **Engineering Determination** — for applicability, currency, materiality, or other context-relevant determinations;
- **Engineering Composition** — to assemble Engineering information into Effective Engineering Context or another context-oriented composition;
- **Engineering Projection** — to represent the composed context for Human Engineers, AI Engineers, interfaces, or execution uses;
- **Durable State Establishment** — where materially significant context-related derived state must survive ephemeral boundaries;
- **Engineering Provenance** — to preserve the origin, derivation, relationships, and currency-relevant basis of composed context.

Context Resolution & Composition retains ownership of context semantics.

In particular:

> **Available information ≠ applicable context.**

> **Included ≠ applicable.**

> **Omitted ≠ inapplicable.**

> **Persisted context ≠ current context.**

Effective Engineering Context remains derived Engineering state.

Its composition or projection does not create a new authoritative source of Engineering truth.

### 14.5 Execution Enablement

The **Execution Enablement** capability governs how Engineering technical action becomes possible while preserving the distinctions among technical capability, Engineering availability, participant constraints, execution, authoritative Engineering state, and Engineering outcomes.

Its realization may use:

- **Engineer Identity Resolution** — where execution is associated with a resolved Engineer;
- **Authoritative Engineering State Resolution** — to resolve Engineering state required for execution;
- **Participant State Resolution** — to resolve participant-relative Engineering state relevant to execution;
- **Authority Resolution** — where applicable authority is relevant to the Engineering action or subsequent authoritative effect;
- **Execution Capability Resolution** — to resolve technically available capabilities and candidate Execution Mechanisms;
- **Engineering Determination** — particularly for Execution Availability, constraint applicability, materiality, or Engineering consequences of execution;
- **Engineering Composition** — to assemble Engineering information required for execution;
- **Engineering Projection** — to represent Engineering information for a Human-operated tool, AI runtime, automation mechanism, or other execution use;
- **Constraint Enforcement** — to technically enforce applicable execution-relevant constraints on Platform-controlled execution surfaces;
- **Execution Invocation** — to perform technical Engineering action through a selected Execution Mechanism;
- **Durable State Establishment** — where material execution state or Execution Outcomes must survive ephemeral execution boundaries;
- **Authoritative Engineering State Establishment** — where execution contributes to a proposed authoritative Engineering state change that satisfies the applicable owning semantics and authority;
- **Engineering Provenance** — to preserve materially relevant execution, actor, mechanism, instance, outcome, and state-establishment relationships.

Execution Enablement retains ownership of execution-enablement semantics.

In particular:

> **Execution Capability ≠ Execution Availability.**

> **Can execute ≠ may execute.**

> **Execution Mechanism ≠ Engineer.**

> **Execution Instance ≠ Engineer Identity.**

> **Execution Outcome ≠ Engineering Determination.**

> **Execution success ≠ Engineering success.**

> **Execution completion ≠ Engineering completion.**

Execution Enablement may compose these mechanisms through Controlled Execution, Engineering Automation, AI Execution Composition, or other Realization Patterns without those patterns becoming a new Engineering lifecycle.

### 14.6 Governance & Validation Integration

The **Governance & Validation Integration** capability governs integration of Engineering governance, validation, evidence, authority, and determinations while preserving the semantics and authority of their applicable owning mechanisms.

Its realization may use:

- **Engineer Identity Resolution** — where a governance or validation interaction requires Engineer identity;
- **Authoritative Engineering State Resolution** — to resolve authoritative Engineering state relevant to governance or validation;
- **Participant State Resolution** — where participant-relative state is relevant to governance or validation;
- **Authority Resolution** — to resolve the authority applicable to a Governed Determination, Validation Determination, or resulting authoritative state;
- **Engineering Determination** — to realize Governed Determinations, Validation Determinations, Evidence Sufficiency, materiality, applicability, or other governance- and validation-related Engineering determinations;
- **Engineering Composition** — to assemble Engineering state, evidence, determinations, constraints, and other relevant information for governance or validation;
- **Engineering Projection** — to represent governance- or validation-relevant Engineering information for Human or AI participants and mechanisms;
- **Authoritative Engineering State Establishment** — where a governed or validation determination creates or changes authoritative Engineering state;
- **Durable State Establishment** — where materially significant evidence, derived determinations, compositions, projections, or other governance- or validation-relevant state must remain durable;
- **Engineering Provenance** — to preserve materially relevant relationships among evidence, determinations, authority, participants, execution, and authoritative state.

Execution-related mechanisms may contribute technical results or enforcement information where relevant to governance or validation.

Such contribution does not transfer governance or validation semantics to execution.

Therefore:

> **Execution Outcome ≠ Validation Determination.**

> **Execution Outcome ≠ Governed Determination.**

> **Evidence ≠ determination.**

> **Evidence existence ≠ Evidence Sufficiency.**

> **Ability to determine ≠ authority to establish.**

Governance & Validation Integration retains ownership of the integration semantics required to preserve governance and validation boundaries.

The specific governance or validation mechanism retains ownership of its permissible outcomes, authority requirements, evidence requirements, lifecycle, and consequences.

### 14.7 Continuity & Provenance

The **Continuity & Provenance** capability governs preservation of materially significant Engineering state and provenance so Engineering activity can remain traceable and can be reconstructed, handed over, or resumed across ephemeral boundaries.

Its realization may use:

- **Engineer Identity Resolution** — to preserve Engineer identity continuity across sessions, interfaces, and Execution Instances;
- **Authoritative Engineering State Resolution** — to re-resolve authoritative Engineering state required for reconstruction or resumption;
- **Participant State Resolution** — to re-resolve current participant-relative Engineering state;
- **Discovery Resolution** — where authoritative or durable Engineering information required for reconstruction must be located;
- **Authority Resolution** — where current Engineering authority must be re-resolved;
- **Execution Capability Resolution** — where available technical capability must be re-resolved following environment or Execution Instance change;
- **Engineering Determination** — for current applicability, currency, materiality, Execution Availability, or other conditions required during reconstruction or resumption;
- **Engineering Composition** — to assemble materially relevant Engineering information for reconstruction, handover, or resumed activity;
- **Engineering Projection** — to represent reconstructed Engineering information for the current Human or AI participant or execution use;
- **Durable State Establishment** — to preserve materially significant Engineering state across ephemeral boundaries;
- **Engineering Provenance** — to preserve and resolve materially relevant origins, derivations, transformations, participation, execution, determination, and establishment relationships.

Execution Invocation may participate where resumed Engineering activity proceeds to technical execution, but execution is not required merely to reconstruct Engineering state.

Continuity & Provenance retains ownership of continuity semantics.

In particular:

> **Durability ≠ authority.**

> **Reconstruction ≠ current-state resolution.**

> **Provenance supports resumption; provenance does not freeze context.**

> **Resumption requires re-resolution, not replay.**

Continuity must be reconstructed from authoritative sources and durable Engineering state.

It must not depend upon hidden AI reasoning, Human recollection, conversational trajectory, or undocumented runtime state as authoritative Engineering state.

### 14.8 Capability-to-Mechanism Summary

The following matrix summarizes the principal Realization Mechanisms that may contribute to each Engineering Capability.

A marked relationship indicates architectural relevance.

It does not imply that the mechanism is mandatory for every interaction involving the capability.

| Realization Mechanism | Discovery & Navigation | Participation & Scope | Context Resolution & Composition | Execution Enablement | Governance & Validation Integration | Continuity & Provenance |
|---|:---:|:---:|:---:|:---:|:---:|:---:|
| Engineer Identity Resolution | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ |
| Authoritative Engineering State Resolution | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ |
| Participant State Resolution | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ |
| Discovery Resolution | ✓ |  | ✓ |  |  | ✓ |
| Authority Resolution |  | ✓ | ✓ | ✓ | ✓ | ✓ |
| Execution Capability Resolution |  |  | ✓ | ✓ |  | ✓ |
| Engineering Determination | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ |
| Engineering Composition | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ |
| Engineering Projection | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ |
| Authoritative Engineering State Establishment |  | ✓ |  | ✓ | ✓ |  |
| Durable State Establishment |  | ✓ | ✓ | ✓ | ✓ | ✓ |
| Constraint Enforcement |  |  |  | ✓ |  |  |
| Execution Invocation |  |  |  | ✓ |  | ✓ |
| Engineering Provenance | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ |

The density of this matrix is intentional.

Foundational Realization Mechanisms are shared architectural responsibilities.

Their reuse across capabilities avoids capability-specific duplication without centralizing semantic ownership.

The matrix must not be interpreted as an implementation topology.

In particular, it does not imply:

- one implementation component per Realization Mechanism;
- one implementation component per Engineering Capability;
- a central service implementing all commonly used mechanisms;
- a common persistence model;
- a universal orchestration path;
- mandatory invocation of every marked mechanism;
- ownership of capability semantics by frequently reused mechanisms.

### 14.9 Coverage of the Engineering Capability Model

The mapping demonstrates that the fourteen foundational Realization Mechanisms collectively provide architectural responsibilities for all six Engineering Capabilities.

No additional foundational Realization Mechanism is required solely because a capability uses a specialized Engineering interaction.

Capability-specific interactions may instead be realized through:

- capability-owned Engineering semantics;
- the foundational Realization Mechanisms;
- valid Mechanism Composition;
- Realization Patterns;
- authoritative mechanisms and Engineering Systems;
- downstream implementation constructs.

The mapping also demonstrates why the six Engineering Capabilities must not automatically become six independent implementation systems.

Capabilities define semantic responsibilities.

Realization Mechanisms define reusable architectural responsibilities.

Implementation architecture determines how those responsibilities are technically realized.

Therefore:

> **Capability architecture ≠ realization architecture ≠ implementation topology.**

A downstream realization may combine, distribute, delegate, or specialize implementation responsibilities while preserving this separation.

### 14.10 Mapping Boundaries

Capability realization mapping must not be used to infer Engineering meaning that is not established by the applicable capability or Realization Contract.

In particular:

- mapping a mechanism to a capability does not make every result of that mechanism applicable to that capability;
- mapping Authoritative Engineering State Resolution to a capability does not make all resolved authoritative state relevant or applicable;
- mapping Engineering Determination to a capability does not create a common determination authority or outcome taxonomy;
- mapping Engineering Composition or Projection to multiple capabilities does not create a common authoritative context;
- mapping Durable State Establishment to a capability does not make its state authoritative;
- mapping Execution mechanisms to a capability does not grant execution permission or Engineering authority;
- mapping Engineering Provenance to every capability does not require exhaustive or centralized provenance capture.

The applicable Engineering semantics determine the meaning of each use.

Where the correct capability-to-mechanism relationship is conditional, contextual, or unresolved for a particular Engineering interaction, the realization must preserve that condition rather than infer a stronger relationship from this mapping.

### 14.11 Human and AI Capability Realization

The capability-to-mechanism mapping applies equally to Human Engineers and AI Engineers.

A capability does not require a separate set of foundational Realization Mechanisms merely because an AI Engineer participates.

Human and AI participation may require different:

- Engineering Projections;
- Execution Mechanisms;
- Execution Environments;
- participant interfaces;
- technical enforcement mechanisms;
- provenance-capture mechanisms.

Those differences occur within the same capability and Realization Mechanism architecture.

Therefore:

> **Human/AI realization differences ≠ Human/AI Engineering semantics.**

A Platform realization must not create an alternate AI-specific authority, responsibility, governance, validation, state, or provenance model merely to support AI execution.

AI-specific technical constructs may be introduced downstream where useful, provided they conform to the same foundational Realization Contracts.

---

## 15. Realization Boundaries

The Engineering Platform Realization Model defines architectural responsibilities required to realize Engineering capabilities.

It does not transfer ownership of Engineering semantics to the Platform realization.

A conforming realization may introduce implementation components, services, repositories, indexes, caches, workflow engines, policy engines, agents, runtimes, execution environments, integration mechanisms, or other technical constructs.

Such constructs must operate within the semantic and authority boundaries established by the Engineering Capability Model, applicable Engineering Systems, Development Standards, authoritative mechanisms, and this Realization Model.

Implementation convenience must not redefine Engineering meaning.

Therefore:

> **Technical ownership ≠ semantic ownership.**

And:

> **Implementation control ≠ Engineering authority.**

The following boundaries apply to all Platform realizations.

### 15.1 Semantic Ownership Boundary

A Platform realization must not become the universal owner of Engineering semantics merely because it resolves, stores, indexes, composes, projects, evaluates, executes against, synchronizes, or traces Engineering information.

Engineering semantics remain owned by the applicable:

- Engineering System;
- Engineering Standard;
- governance mechanism;
- validation mechanism;
- authoritative source;
- other Engineering mechanism responsible for those semantics.

A Realization Mechanism may operate over those semantics without acquiring ownership of them.

In particular:

- Engineering Determination does not own the meaning of specialized determinations;
- Engineering Composition does not own the semantics of its constituents;
- Engineering Projection does not own the semantics it represents;
- Constraint Enforcement does not own the constraints it enforces;
- Execution Invocation does not own the Engineering meaning of its outcomes;
- Engineering Provenance does not own the Engineering state or relationships it traces.

Therefore:

> **Realization of semantics ≠ ownership of semantics.**

A downstream implementation must not introduce Platform-defined semantics that override, weaken, broaden, or silently reinterpret semantics owned elsewhere.

### 15.2 Authoritative State Boundary

The Platform realization must not create a competing source of authoritative Engineering truth.

Authoritative Engineering state remains authoritative according to the semantics and authority of its applicable owning mechanism.

Platform facilities such as:

- caches;
- indexes;
- replicas;
- search stores;
- knowledge graphs;
- local copies;
- composed views;
- projections;
- durable representations;
- synchronization stores;
- provenance stores;

must not become independently authoritative merely because they contain or represent authoritative Engineering information.

Therefore:

> **Representation of authoritative state ≠ authoritative state.**

Where authoritative Engineering state must be created or changed, the Authoritative Engineering State Establishment contract applies.

A Platform realization must not bypass the owning mechanism by treating technical persistence, synchronization, replication, publication, or mutation of a representation as authoritative establishment.

### 15.3 Authority Boundary

The Platform realization must preserve the distinction between Engineering authority and technical ability.

Technical capability to:

- read;
- write;
- invoke;
- modify;
- execute;
- approve through an interface;
- call an API;
- operate a tool;
- access a repository;
- satisfy a technical policy;

does not independently establish Engineering authority.

Therefore:

> **Technical permission ≠ Engineering authority.**

Likewise:

> **Implementation control ≠ authority to determine or establish.**

Applicable Engineering authority must remain grounded in the Engineering semantics and authoritative mechanisms that establish that authority.

A Platform realization must not manufacture, broaden, aggregate, infer, or transfer Engineering authority merely to make an Engineering interaction technically executable.

### 15.4 Responsibility and Participation Boundary

The Platform realization must preserve the distinctions among:

- Engineer Identity;
- project participation;
- governed-work responsibility;
- Participation Eligibility;
- Engineering authority;
- execution capability;
- Execution Availability;
- execution activity.

Technical activity must not create participant or responsibility semantics.

In particular:

> **Authentication ≠ participation.**

> **Participation ≠ responsibility.**

> **Responsibility ≠ authority.**

> **Execution ≠ responsibility.**

> **Execution Instance ≠ Engineer Identity.**

An Engineer, agent, automation mechanism, tool, or runtime performing technical activity must not be inferred to hold governed-work responsibility merely because it performed that activity.

Where participation or governed-work responsibility is established, transferred, released, or otherwise changed, the applicable authoritative Engineering semantics and state-establishment requirements remain in force.

### 15.5 Derived State Boundary

Derived Engineering state must remain distinguishable from the Engineering information from which it was derived.

This applies to, among other things:

- Participant State;
- discovery results;
- Derived Determinations;
- Engineering Compositions;
- Engineering Projections;
- Effective Engineering Context;
- AI Execution Composition;
- reconstructed Engineering views;
- provenance compositions;
- execution-supporting representations.

Derived state may aggregate authoritative Engineering information.

Such aggregation does not create aggregate authority.

Therefore:

> **Derived from authority ≠ derived authority.**

A Platform realization must preserve materially relevant:

- source identity;
- semantic ownership;
- authority characteristic;
- derivation characteristic;
- normative force;
- scope;
- applicability;
- uncertainty;
- temporal and currency-relevant characteristics;
- provenance.

Transformation, summarization, compression, indexing, embedding, ranking, machine encoding, or other technical representation must not silently elevate derived state into source or authoritative state.

### 15.6 Durability Boundary

The durability characteristic of Engineering state must remain independent of its authority characteristic, applicability, currency, and Engineering validity.

The Platform may make Engineering state durable where required for:

- continuity;
- reconstruction;
- governance;
- validation;
- evidence;
- provenance;
- subsequent Engineering activity.

Such durability does not independently establish Engineering meaning.

Therefore:

> **Persisted ≠ authoritative.**

> **Persisted ≠ current.**

> **Recoverable ≠ applicable.**

A Platform realization must not treat persistence duration, replication count, storage location, availability, or recoverability as increased Engineering authority or validity.

Where materially required Engineering state is already sufficiently durable and resolvable from an authoritative or otherwise adequate durable source, the Platform need not duplicate that state merely to create Platform-local durability.

### 15.7 Discovery and Resolution Boundary

Discovery facilities must remain distinct from authoritative resolution and Engineering determination.

Search, indexing, ranking, similarity, recommendation, navigation, graph traversal, semantic retrieval, or other discovery mechanisms may identify candidate Engineering information.

They must not independently establish:

- authoritative state;
- authoritative relationships;
- applicability;
- priority;
- normative force;
- materiality;
- responsibility;
- authority;
- governance or validation outcomes.

Therefore:

> **Discovery ≠ resolution ≠ determination.**

Discovery may lead to Authoritative Engineering State Resolution.

Resolution may provide input to Engineering Determination.

These relationships do not permit one responsibility to substitute for another.

A technically convenient discovery representation must not become a hidden authoritative source.

### 15.8 Determination Boundary

A Platform realization may provide common technical machinery for Engineering Determination.

Common machinery must not create a common semantic owner, authority model, or universal outcome taxonomy for Engineering determinations.

Participation Eligibility, applicability, materiality, currency, Evidence Sufficiency, Execution Availability, Governed Determinations, Validation Determinations, and other determinations retain the semantics defined by their applicable owners.

Therefore:

> **Common determination machinery ≠ common determination semantics.**

The ability to evaluate or technically produce a determination does not establish authority to give that determination authoritative Engineering effect.

Where authoritative effect is required, applicable authority and Authoritative Engineering State Establishment remain independently required.

### 15.9 Execution Boundary

Execution mechanisms operate within Engineering semantics established elsewhere.

A Platform realization must not infer Engineering permission, authority, validity, governance, validation, or completion from technical executability or technical outcome.

Therefore:

> **Can execute ≠ may execute.**

> **Execution Outcome ≠ Engineering Determination.**

> **Execution success ≠ Engineering success.**

> **Execution completion ≠ Engineering completion.**

Execution mechanisms may produce artifacts, state, diagnostics, evidence, and other technical results.

Those results do not become authoritative Engineering state merely because they were successfully produced.

Where execution contributes to a broader Engineering conclusion, the applicable determination, governance, validation, evidence, authority, and state-establishment semantics remain required.

### 15.10 Constraint Enforcement Boundary

Constraint Enforcement must remain distinct from constraint definition and constraint applicability.

The Platform may technically enforce an applicable constraint on an execution surface it controls.

It must not infer that technical control gives it authority to define, broaden, weaken, remove, or reinterpret the constraint.

Therefore:

> **Constraint source ≠ constraint enforcer.**

> **Constraint applicability ≠ constraint enforcement.**

Where the Platform cannot technically enforce a required constraint, it must preserve that condition explicitly.

It must not represent communication, display, warning, policy description, or enforcement performed elsewhere as Platform technical enforcement.

Likewise, inability to enforce must not be silently interpreted as permission to proceed.

### 15.11 Governance and Validation Boundary

The Platform realization may integrate governance and validation mechanisms without absorbing their semantics or authority.

Governance and validation remain distinct from technical execution and from one another according to their applicable Engineering semantics.

A Platform realization must not reduce governance or validation to generic technical states such as:

- passed;
- failed;
- approved;
- rejected;
- successful;
- complete;

unless those terms are explicitly defined with that Engineering meaning by the applicable owning semantics.

In particular:

> **Execution success ≠ validation.**

> **Evidence existence ≠ Evidence Sufficiency.**

> **Validation Determination ≠ Governed Determination.**

The permissible outcomes, authority requirements, evidence requirements, lifecycle, scope, and consequences of governance and validation remain owned by their applicable mechanisms.

### 15.12 Provenance Boundary

Engineering Provenance must support traceability without becoming a substitute source of Engineering truth.

A Platform realization must not infer stronger Engineering meaning merely because an activity, relationship, or event has been recorded.

Therefore:

> **Recorded ≠ established.**

> **Performed by ≠ responsible for.**

> **Responsible for ≠ authorized to determine.**

> **Derived from ≠ approved by.**

> **Produced by ≠ authoritative owner.**

Where authoritative history is owned elsewhere, Platform provenance may reference or resolve that history rather than duplicate and assume ownership of it.

Technical telemetry, logs, audit records, traces, or runtime metadata do not automatically become sufficient Engineering Provenance merely because they are available.

Provenance must preserve materially relevant Engineering relationships rather than technical observability alone.

### 15.13 Continuity Boundary

Engineering continuity must depend upon authoritative sources and materially required durable Engineering state.

It must not depend upon preservation of a particular:

- session;
- process;
- Execution Instance;
- AI runtime;
- agent context window;
- conversational trajectory;
- Human recollection;
- hidden AI reasoning;
- undocumented runtime state.

Therefore:

> **Continuity ≠ runtime persistence.**

And:

> **Resumption ≠ replay.**

Replacement of a Human-facing interface, execution mechanism, Execution Instance, AI runtime, or other technical implementation construct must not by itself change Engineer Identity, responsibility, authority, or authoritative Engineering state.

Where Engineering activity resumes, materially relevant current Engineering state must be re-resolved or re-determined where required.

Durable historical context may support reconstruction.

It must not be assumed to remain current merely because it survived.

### 15.14 Human and AI Boundary

The Platform may provide participant-specific technical mechanisms for Human Engineers and AI Engineers.

These may differ in:

- representation;
- interaction model;
- execution mechanism;
- execution environment;
- constraint enforcement;
- provenance capture;
- technical continuity mechanisms.

Such differences must not create separate Engineering truth, authority, responsibility, governance, validation, or lifecycle semantics.

Therefore:

> **Participant-specific mechanism ≠ participant-specific Engineering model.**

AI-specific infrastructure must not create:

- AI-specific authority;
- implicit AI responsibility;
- weaker validation semantics;
- alternate authoritative state;
- hidden AI-only Engineering context;
- authority derived from model capability;
- continuity dependent upon private model state.

Likewise, Human participation must not receive implicit Engineering authority merely because a Human performs an action manually.

Human and AI participation remain subject to the same underlying Engineering semantics.

### 15.15 Platform Boundary

The Engineering Platform Realization Model does not require a conforming implementation to internalize every system or mechanism that participates in Engineering.

A Realization Mechanism may be satisfied through:

- an Engineering System;
- an authoritative source;
- a governance mechanism;
- a validation mechanism;
- an identity mechanism;
- an execution environment;
- an external Engineering tool;
- another system capable of satisfying the applicable Realization Contract.

Therefore:

> **Platform realization ≠ Platform internalization.**

A mechanism being architecturally required does not mean a conforming implementation must itself implement, host, persist, or operate that mechanism.

Where responsibility is delegated or externally realized, a conforming implementation must preserve sufficient integration semantics to ensure that the applicable Realization Contract remains satisfied.

The Platform boundary may therefore vary among implementations without changing the Engineering Capability Model or Realization Model.

### 15.16 Implementation Boundary

The foundational Realization Mechanisms do not prescribe implementation topology.

A downstream implementation may:

- combine multiple mechanisms within one component;
- distribute one mechanism across multiple components;
- delegate mechanisms to existing systems;
- use synchronous or asynchronous interaction;
- use centralized or distributed persistence;
- use event-driven, request-driven, workflow-driven, agent-driven, or other execution approaches;
- introduce implementation-specific supporting constructs.

Such choices must not alter the architectural meaning of the foundational mechanisms.

In particular, implementation architecture must not infer:

> **Realization Mechanism = service.**

> **Engineering Capability = application.**

> **Authoritative source = database.**

> **Engineering Determination = policy engine.**

> **Engineering Composition = context store.**

> **Engineering Provenance = event log.**

> **Execution Enablement = agent runtime.**

Any of these technologies may participate in realizing the corresponding architectural responsibility.

None defines that responsibility by itself.

### 15.17 Boundary Preservation

A Platform realization preserves the Realization Model boundaries where implementation choices do not:

1. transfer semantic ownership to technical infrastructure;
2. create competing authoritative Engineering state;
3. infer Engineering authority from technical access or control;
4. infer participation or responsibility from execution;
5. elevate derived state through aggregation or representation;
6. elevate durable state through persistence;
7. substitute discovery for authoritative resolution or determination;
8. centralize determination semantics merely because determination machinery is shared;
9. convert execution outcomes into Engineering conclusions without applicable Engineering semantics;
10. redefine constraint meaning through enforcement;
11. collapse governance, validation, evidence, and execution into generic technical status;
12. substitute provenance for authoritative Engineering state or authoritative history;
13. make Engineering continuity dependent upon a particular runtime or participant memory;
14. create different Engineering semantics for Human and AI Engineers;
15. require Platform internalization of mechanisms that may validly remain externally owned or realized;
16. derive architectural meaning from implementation topology.

These boundaries constrain implementation architecture without prescribing it.

A downstream implementation may vary substantially while remaining conformant where these boundaries and the applicable Realization Contracts are preserved.

---

## 16. Realization Requirements

A conforming Engineering Platform realization must realize the Engineering Capability Model through architectural mechanisms that satisfy the responsibilities, boundaries, state characteristics, and composition rules established by this specification.

Conformance is determined by preservation of Engineering meaning and architectural responsibility rather than by implementation topology or technology choice.

A realization may combine, distribute, delegate, specialize, or otherwise implement the foundational Realization Mechanisms differently provided that the applicable Realization Contracts remain satisfied.

Therefore:

> **Conformance requires preservation of architectural semantics, not structural similarity between implementations.**

The following requirements apply to every conforming Engineering Platform realization.

### 16.1 Capability Realization

A conforming realization must provide sufficient architectural realization for all six Engineering Capabilities:

1. Discovery & Navigation;
2. Participation & Scope;
3. Context Resolution & Composition;
4. Execution Enablement;
5. Governance & Validation Integration;
6. Continuity & Provenance.

Capability realization may be distributed across Platform components, Engineering Systems, authoritative mechanisms, external systems, execution environments, or other implementation constructs.

The realization must not require each Engineering Capability to correspond to a dedicated:

- application;
- service;
- runtime;
- repository;
- workflow;
- agent;
- deployment unit.

Capability coverage must instead be demonstrable through satisfaction of the applicable Realization Mechanism responsibilities and capability-owned Engineering semantics.

A realization must not omit an architectural responsibility merely because another implementation construct provides technically similar functionality.

### 16.2 Foundational Mechanism Coverage

A conforming realization must provide or validly delegate the responsibilities represented by the fourteen foundational Realization Mechanisms:

1. Engineer Identity Resolution;
2. Authoritative Engineering State Resolution;
3. Participant State Resolution;
4. Discovery Resolution;
5. Authority Resolution;
6. Execution Capability Resolution;
7. Engineering Determination;
8. Engineering Composition;
9. Engineering Projection;
10. Authoritative Engineering State Establishment;
11. Durable State Establishment;
12. Constraint Enforcement;
13. Execution Invocation;
14. Engineering Provenance.

The realization need not implement each mechanism as a separate technical construct.

For every mechanism required by an Engineering interaction, the realization must be capable of demonstrating that the applicable Realization Contract is satisfied.

Where a mechanism is delegated wholly or partially to another system or authoritative mechanism, the realization must preserve sufficient integration semantics to satisfy the applicable contract.

Technical availability of equivalent-looking information or behavior must not be treated as mechanism coverage where the required Engineering semantics are not preserved.

### 16.3 Semantic Ownership Preservation

A conforming realization must preserve the semantic ownership of Engineering information, determinations, constraints, lifecycle state, governance, validation, responsibility, authority, and other Engineering concerns.

Realization infrastructure must not acquire semantic ownership merely because it:

- stores;
- resolves;
- indexes;
- searches;
- evaluates;
- composes;
- projects;
- executes against;
- synchronizes;
- transmits;
- persists;
- traces;

Engineering information.

Where Engineering semantics are owned by another Engineering System, Engineering Standard, governance mechanism, validation mechanism, authoritative source, or other Engineering mechanism, the realization must preserve that ownership.

The realization must not introduce Platform-defined semantics that silently override, weaken, broaden, or reinterpret semantics owned elsewhere.

### 16.4 Authoritative State Preservation

A conforming realization must preserve the identity and ownership of authoritative Engineering state.

Where authoritative Engineering state is resolved, represented, cached, indexed, replicated, composed, projected, persisted, synchronized, or otherwise processed outside its owning mechanism, the realization must preserve sufficient information to distinguish that representation from the authoritative source.

The realization must not create a competing authoritative source merely through technical representation or persistence.

Where authoritative Engineering state is created or changed, the realization must satisfy the Authoritative Engineering State Establishment contract.

The realization must preserve, as applicable:

- Engineering entity identity;
- semantic ownership;
- authoritative source;
- applicable authority;
- lifecycle and state semantics;
- normative force;
- scope;
- relationships;
- temporal characteristics;
- version or revision semantics;
- conflict and concurrency semantics;
- provenance.

### 16.5 Authority Preservation

A conforming realization must preserve Engineering authority independently from technical access, implementation control, participation, responsibility, and execution capability.

Where Engineering authority is required, the realization must be capable of resolving the applicable authority according to the Engineering semantics that establish it.

The realization must not infer Engineering authority merely from:

- authentication;
- identity;
- project participation;
- governed-work responsibility;
- role labels;
- technical permissions;
- tool access;
- repository access;
- execution capability;
- execution success;
- ability to evaluate a determination;
- implementation ownership.

Where authoritative Engineering effect is required, applicable authority must remain valid for the Engineering scope and action concerned.

Authority must not be silently broadened, aggregated, transferred, delegated, or manufactured by implementation machinery.

### 16.6 Participant and Responsibility Preservation

A conforming realization must preserve the distinctions among:

- Engineer Identity;
- project participation;
- governed-work responsibility;
- Participation Eligibility;
- Engineering authority;
- Execution Capability;
- Execution Availability;
- Execution Instance;
- execution activity.

The realization must not establish or infer governed-work responsibility merely because an Engineer, agent, automation mechanism, tool, or Execution Instance performs technical activity.

Where participation or governed-work responsibility is established, transferred, released, or otherwise changed, the applicable authoritative Engineering semantics and state-establishment requirements must be satisfied.

Replacement of a credential, session, interface, Execution Instance, execution mechanism, or AI runtime must not by itself alter durable Engineer Identity or independently established responsibility.

### 16.7 Determination Preservation

A conforming realization must support Engineering Determinations without centralizing ownership of their Engineering semantics.

The realization must preserve, as applicable:

- the Engineering question being determined;
- owning Engineering semantics;
- permissible outcome semantics;
- relevant Engineering state;
- applicable evidence and conditions;
- scope;
- required authority;
- authority characteristic of the result;
- temporal or currency characteristics;
- uncertainty and unresolved conditions;
- provenance.

The realization must not require all Engineering Determinations to use a universal outcome taxonomy.

Where a determination is intended to carry authoritative Engineering effect, production of the determination result must remain distinguishable from establishment of that authoritative effect.

Any authoritative Engineering state created or changed as a consequence of a determination must satisfy the Authoritative Engineering State Establishment contract.

Where a sufficiently grounded determination cannot be produced, the realization must preserve the applicable unresolved condition rather than fabricate a conclusive result.

### 16.8 Derived State Preservation

A conforming realization must preserve derived Engineering state as distinguishable from the Engineering information from which it was derived.

Where Engineering information is:

- aggregated;
- composed;
- projected;
- summarized;
- transformed;
- reconstructed;
- ranked;
- indexed;
- embedded;
- machine encoded;
- otherwise derived;

the realization must preserve materially relevant source identity, semantic ownership, authority characteristic, derivation characteristic, normative force, scope, applicability, uncertainty, temporal characteristics, and provenance.

Derived state must not acquire aggregate authority merely because its constituents include authoritative Engineering state.

The realization must not silently manufacture certainty, applicability, priority, authority, approval, or other Engineering meaning through derivation.

### 16.9 State Characteristic Preservation

A conforming realization must preserve authority, durability, and derivation as independent characteristics of Engineering state.

The realization must be capable of distinguishing, where materially relevant:

- authoritative from non-authoritative state;
- durable from ephemeral state;
- source from derived state.

A realization must not use a state model that requires these characteristics to be interpreted as one mutually exclusive classification.

Persistence must not establish authority.

Derivation from authoritative state must not establish independent authority.

Source state must not be assumed authoritative merely because it is source state.

Where state crosses a capability, system, implementation, persistence, execution, participant, or other realization boundary, the crossing must not by itself alter Engineering meaning.

Any legitimate change to a state characteristic must remain distinguishable from changes to other state characteristics.

### 16.10 Composition and Projection Preservation

A conforming realization must preserve the distinction between Engineering Composition and Engineering Projection.

Engineering Composition must remain responsible for what Engineering information is assembled for a defined Engineering concern or use.

Engineering Projection must remain responsible for how Engineering information is represented for a defined participant, interface, activity, execution mechanism, or other use.

A realization must not use representation requirements to silently remove materially required Engineering information from a composition.

Likewise, a representation must not change materially relevant Engineering meaning merely to satisfy participant, interface, machine, or execution requirements.

Human-oriented and AI-oriented projections may differ.

Such differences must preserve the same underlying Engineering semantics.

Where a projection cannot preserve materially required Engineering meaning, the limitation or loss condition must remain explicit.

### 16.11 Discovery Preservation

A conforming realization must preserve discovery as distinct from authoritative resolution and Engineering Determination.

Discovery results must remain candidate Engineering information until the applicable Engineering mechanisms establish any stronger Engineering meaning.

Search relevance, ranking, similarity, recommendation, graph relationship, semantic proximity, or technical retrieval must not independently establish:

- authority;
- authoritative Engineering state;
- authoritative relationships;
- applicability;
- normative force;
- materiality;
- Engineering priority;
- responsibility;
- governance or validation outcomes.

Where authoritative Engineering state is required, the applicable Authoritative Engineering State Resolution responsibility must be satisfied.

Where applicability or another Engineering conclusion is required, the applicable Engineering Determination responsibility must be satisfied.

### 16.12 Execution Preservation

A conforming realization must preserve technical execution as distinct from Engineering authority, Engineering Determination, authoritative Engineering state, governance, validation, and Engineering completion.

The realization must distinguish:

- technical capability from Execution Availability;
- Execution Mechanism from Engineer;
- Execution Instance from Engineer Identity;
- Execution Outcome from Engineering Determination;
- technical success from Engineering success;
- execution completion from Engineering completion.

Where applicable Engineering semantics require Execution Availability, constraint enforcement, authority, governance, validation, or other conditions before or after execution, the realization must preserve those requirements independently from technical executability.

An Execution Outcome may contribute to Engineering Evidence, Engineering Determination, durable state, provenance, or proposed authoritative Engineering state.

Such contribution must not silently change the technical meaning or authority characteristic of the Execution Outcome.

### 16.13 Constraint Preservation and Enforcement

A conforming realization must preserve the distinction among:

- constraint source;
- constraint meaning and normative force;
- constraint applicability;
- constraint enforcement.

Where an execution-relevant constraint requires technical enforcement on a Platform-controlled execution surface, the realization must enforce that constraint according to its established meaning and applicability.

Where the Platform cannot technically enforce a required constraint, the realization must preserve that condition explicitly.

Where another mechanism or environment is responsible for enforcement, that responsibility must remain distinguishable from Platform enforcement.

The realization must not:

- redefine a constraint through enforcement;
- infer applicability merely because enforcement is technically possible;
- treat communication or display as technical enforcement;
- treat inability to enforce as permission to proceed;
- independently determine the Engineering consequence of enforcement failure.

### 16.14 Governance, Validation, and Evidence Preservation

A conforming realization must preserve governance, validation, and Engineering Evidence as distinct Engineering concerns.

The realization must not reduce Governed Determinations or Validation Determinations to generic technical execution states.

It must preserve the applicable:

- owning semantics;
- permissible outcomes;
- authority requirements;
- evidence requirements;
- scope;
- lifecycle or currency semantics;
- consequences;
- provenance.

Engineering Evidence must remain distinguishable from the Engineering Determination it supports.

Evidence existence must not be treated as Evidence Sufficiency.

Execution Outcome must not be treated as a Governed Determination or Validation Determination.

Where Evidence Sufficiency is required, it must remain an Engineering Determination governed by the applicable Engineering semantics.

### 16.15 Durability and Continuity

A conforming realization must preserve materially significant Engineering state beyond ephemeral boundaries where loss of that state would materially impair:

- continuity;
- reconstruction;
- governance;
- validation;
- provenance;
- evidence;
- subsequent Engineering activity.

The realization must not require all Engineering state or technical activity to become materially required Durable Engineering State.

Where materially required state is already sufficiently durable and resolvable from an authoritative or otherwise adequate durable source, Platform-local duplication is not required.

Where materiality cannot be determined without preserving state or provenance, sufficient information must remain available until the applicable materiality determination can be made.

Durable state must retain sufficient identity, source, authority, derivation, temporal, uncertainty, and provenance characteristics for its later Engineering use.

Durability must not be interpreted as authority, currency, or applicability.

### 16.16 Provenance Preservation

A conforming realization must preserve or make resolvable sufficient Engineering Provenance for materially significant Engineering state, activity, evidence, determinations, compositions, projections, execution, and state establishments.

The realization must preserve materially relevant distinctions among:

- Engineer Identity;
- governed-work responsibility;
- Engineering authority;
- executing mechanism;
- Execution Instance;
- evidence source;
- determination authority;
- derivation;
- production;
- recording;
- authoritative ownership.

Engineering Provenance must not substitute for:

- authoritative Engineering state;
- authoritative history owned elsewhere;
- Engineering Evidence;
- Engineering Determination;
- responsibility;
- authority.

Where sufficient provenance already exists in an authoritative or otherwise adequate durable source, the realization may preserve durable resolvability rather than duplicate the provenance.

The realization must not fabricate missing authoritative provenance or authoritative history.

### 16.17 Reconstruction and Resumption

A conforming realization must support Engineering reconstruction and resumption from authoritative sources and materially required durable Engineering state.

Reconstruction and resumption must not require preservation of:

- a particular Execution Instance;
- a particular AI runtime;
- a particular session;
- Human recollection;
- conversational trajectory;
- hidden AI reasoning;
- undocumented runtime state.

Where resumed Engineering activity depends upon current Engineering state, the realization must re-resolve or re-determine the materially relevant current Engineering conditions required by the applicable Engineering interaction, which may include:

- authoritative Engineering state;
- Participant State;
- applicable authority;
- applicability;
- currency;
- constraints and their applicability;
- Execution Capability;
- Execution Availability;
- other current Engineering conditions.

Historical durability must not be treated as proof of current applicability or currency.

Therefore:

> **Resumption must be realizable through re-resolution rather than replay.**

### 16.18 Human and AI Realization

A conforming realization must apply the same underlying Engineering semantics to Human Engineers and AI Engineers.

Human and AI participation may use different:

- Engineering Projections;
- interaction mechanisms;
- Execution Mechanisms;
- Execution Environments;
- constraint-enforcement mechanisms;
- provenance-capture mechanisms;
- technical continuity mechanisms.

These differences must not create participant-specific:

- Engineering truth;
- authority;
- governed-work responsibility semantics;
- governance semantics;
- validation semantics;
- lifecycle semantics;
- authoritative state semantics;
- provenance standards.

Technical capability of a Human or AI participant must not independently establish authority, responsibility, or permission to act.

Replacement of an AI runtime or Execution Instance must not create a new Engineer Identity where the same durable Engineer Identity continues to participate.

### 16.19 Failure, Conflict, and Uncertainty

A conforming realization must preserve materially relevant failure, conflict, uncertainty, ambiguity, incompleteness, staleness, unavailability, inaccessibility, partial results, and unresolved conditions.

The realization must not silently convert such conditions into:

- success;
- failure;
- approval;
- rejection;
- applicability;
- inapplicability;
- permission;
- prohibition;
- completion;
- authoritative state;

unless the applicable Engineering semantics establish that conclusion.

Failure or success of one Realization Mechanism must not automatically determine the Engineering meaning of a broader Mechanism Composition.

Where an interaction cannot validly continue, the applicable condition must remain explicit and available to the Engineering mechanisms responsible for determining its consequence.

### 16.20 Implementation Independence

A conforming realization may use any implementation architecture capable of satisfying this specification.

The realization may:

- combine multiple Realization Mechanisms within one component;
- distribute one mechanism across multiple components;
- delegate responsibilities to existing systems;
- use centralized or distributed state;
- use synchronous or asynchronous interaction;
- use Human-operated, automated, or AI-oriented mechanisms;
- use workflows, events, commands, agents, services, repositories, indexes, policy engines, or other technical constructs.

Implementation choices must not redefine the architectural responsibilities established by this specification.

In particular:

> **Implementation co-location ≠ semantic collapse.**

And:

> **Physical separation ≠ semantic boundary preservation.**

A realization is conformant because the required Engineering responsibilities and boundaries are preserved, not because its technical architecture resembles another conforming realization.

### 16.21 Conformance Demonstrability

A conforming realization must be capable of demonstrating how the applicable requirements of this specification are satisfied.

Such demonstration must be possible without assuming that implementation topology itself proves conformance.

Where multiple Realization Mechanisms are implemented through the same technical construct or operation, the realization must remain capable of demonstrating that their respective responsibilities and boundaries are independently satisfied.

Where a Realization Mechanism is delegated to another system or mechanism, the realization must remain capable of demonstrating how the delegated responsibility satisfies the applicable Realization Contract.

Where authoritative Engineering semantics or state remain externally owned, conformance demonstration must preserve that external ownership rather than require duplication into Platform-owned state.

Conformance evidence may vary by implementation.

This specification does not prescribe a universal certification process, test framework, evidence format, or conformance tooling.

The architectural requirement is that conformance be demonstrable from preserved Engineering semantics, responsibilities, state characteristics, boundaries, and materially relevant provenance rather than inferred solely from implementation structure.

### 16.22 Realization Requirement Closure

A Platform realization conforms to this specification where it:

1. realizes all six Engineering Capabilities through sufficient architectural responsibilities;
2. provides or validly delegates all required foundational Realization Mechanisms;
3. preserves semantic ownership and authoritative source boundaries;
4. preserves Engineering authority independently from technical capability and implementation control;
5. preserves distinctions among identity, participation, responsibility, authority, and execution;
6. preserves determination semantics and authoritative-effect boundaries;
7. preserves derived state without manufacturing aggregate authority;
8. preserves authority, durability, and derivation as independent state characteristics;
9. preserves Composition and Projection as distinct responsibilities;
10. preserves discovery independently from authoritative resolution and determination;
11. preserves technical execution independently from Engineering conclusions;
12. preserves constraint meaning, applicability, and enforcement as distinct concerns;
13. preserves governance, validation, evidence, and execution distinctions;
14. preserves materially required durable Engineering state and continuity;
15. preserves sufficient materially relevant Engineering Provenance;
16. supports reconstruction and resumption without dependence upon transient participant or runtime memory;
17. applies the same underlying Engineering semantics to Human Engineers and AI Engineers;
18. preserves materially relevant failure, conflict, uncertainty, and unresolved conditions;
19. remains independent of prescribed implementation topology;
20. can demonstrate satisfaction of the applicable Realization Contracts and boundaries.

Conformance with these requirements does not establish conformance with every Engineering System, Engineering Standard, governance mechanism, validation mechanism, or downstream Platform specification.

Those concerns retain their own applicable conformance requirements.

This section defines conformance with the Engineering Platform Realization Model itself.

---

## 17. Invariants

The following invariants define conditions that must remain true across any conforming realization of the Engineering Platform.

They apply independently of implementation topology, technology choice, participant type, execution mechanism, deployment model, persistence model, or interaction pattern.

The invariants consolidate the architectural constraints established by the Realization Model. They do not introduce additional Realization Mechanisms, Engineering lifecycle states, authority models, or semantic ownership.

Violation of an applicable invariant constitutes a violation of the Realization Model even where individual technical operations remain functional.

### 17.1 Semantic Ownership Invariants

Engineering semantics remain owned by the Engineering System, Engineering Standard, governance mechanism, validation mechanism, authoritative source, or other Engineering mechanism responsible for those semantics.

Therefore:

> **Realization of semantics ≠ ownership of semantics.**

> **Technical ownership ≠ semantic ownership.**

> **Implementation control ≠ Engineering authority.**

Shared realization machinery must not become a shared semantic owner merely because multiple Engineering capabilities use it.

### 17.2 Mechanism Invariants

A Realization Mechanism defines a foundational architectural responsibility, not an implementation component.

Therefore:

> **Realization Mechanism ≠ service.**

> **Engineering Capability ≠ application.**

> **Mechanism Composition ≠ universal sequencing.**

> **Atomic realization ≠ semantic collapse.**

> **Reciprocal interaction ≠ circular establishment.**

Multiple Realization Mechanisms may be implemented together, and one Realization Mechanism may be distributed across multiple technical components, provided their responsibilities remain architecturally distinguishable.

### 17.3 Authority Invariants

Engineering authority must arise from the applicable Engineering semantics and authoritative mechanisms, not from technical capability or implementation control.

Therefore:

> **Technical permission ≠ Engineering authority.**

> **Responsibility ≠ authority.**

> **Execution Capability ≠ authority.**

> **Successful execution ≠ authority.**

> **Ability to determine ≠ authority to establish authoritative effect.**

Authority must not be manufactured, broadened, aggregated, transferred, or inferred merely through realization.

### 17.4 Authoritative State Invariants

Authoritative Engineering state remains anchored in the applicable owning mechanism.

Therefore:

> **Representation of authoritative state ≠ authoritative state.**

> **Write ≠ authoritative establishment.**

> **Persistence ≠ authoritative establishment.**

> **Synchronization ≠ authoritative establishment.**

> **Publication ≠ authoritative establishment.**

Any creation or change of authoritative Engineering state must satisfy the Authoritative Engineering State Establishment contract.

### 17.5 State Characteristic Invariants

Authority, durability, and derivation are independent characteristics of Engineering state.

Therefore:

> **Authority ≠ durability ≠ derivation.**

> **Persisted ≠ authoritative.**

> **Persisted ≠ current.**

> **Recoverable ≠ applicable.**

> **Derived from authority ≠ derived authority.**

Persistence duration, replication, availability, recoverability, transformation, aggregation, or representation must not independently alter the authority characteristic of Engineering state.

### 17.6 Discovery, Resolution, and Determination Invariants

Discovery, authoritative resolution, and Engineering Determination remain distinct architectural responsibilities.

Therefore:

> **Discovery ≠ authoritative resolution.**

> **Resolution ≠ determination.**

> **Relevance ≠ applicability.**

> **Ranking ≠ priority, authority, normative force, or materiality.**

> **Inferred relationship ≠ established relationship.**

Common determination machinery must not create common determination semantics:

> **Common determination machinery ≠ common determination semantics.**

Producing a determination intended to carry authoritative Engineering effect does not by itself establish that effect.

### 17.7 Identity, Participation, and Responsibility Invariants

Engineer identity, participation, responsibility, authority, and execution remain distinct.

Therefore:

> **Engineer Identity ≠ credential ≠ session ≠ Execution Instance.**

> **Authentication ≠ participation.**

> **Participation ≠ governed-work responsibility.**

> **Governed-work responsibility ≠ Engineering authority.**

> **Execution ≠ responsibility.**

> **Responsible Engineer ≠ executing mechanism.**

Technical activity must not independently create participation, responsibility, or authority.

### 17.8 Composition and Projection Invariants

Engineering Composition and Engineering Projection operate over Engineering meaning without owning or redefining it.

Therefore:

> **Included ≠ applicable.**

> **Omitted ≠ inapplicable.**

> **Representation must not become reinterpretation.**

Composition and Projection must preserve materially relevant source identity, semantic ownership, authority characteristic, normative force, scope, applicability, uncertainty, currency-relevant characteristics, and provenance.

Human-oriented and AI-oriented representations may differ while preserving the same Engineering semantics.

### 17.9 Execution Invariants

Technical possibility and technical execution remain distinct from Engineering permission and Engineering conclusions.

Therefore:

> **Execution Capability ≠ Execution Availability.**

> **Technical Availability ≠ Execution Availability.**

> **Can execute ≠ may execute.**

> **Execution Outcome ≠ Engineering Determination.**

> **Execution success ≠ Engineering success.**

> **Execution completion ≠ Engineering completion.**

> **Execution invocation ≠ authoritative Engineering state establishment.**

Technical rollback must not silently reverse authoritative Engineering state.

### 17.10 Constraint Invariants

Constraint meaning, applicability, and technical enforcement remain distinct.

Therefore:

> **Constraint source ≠ constraint enforcer.**

> **Constraint applicability ≠ constraint enforcement.**

> **Constraint knowledge or display ≠ constraint enforcement.**

An inability to enforce an applicable constraint must remain explicit and must not independently establish permission to proceed.

Constraint Enforcement must not determine the Engineering consequence of its own enforcement condition.

### 17.11 Governance, Validation, and Evidence Invariants

Governance, validation, evidence, and execution remain semantically distinct.

Therefore:

> **Execution success ≠ validation.**

> **Engineering Evidence ≠ Evidence Sufficiency.**

> **Evidence existence ≠ Evidence Sufficiency.**

> **Validation Determination ≠ Governed Determination.**

> **Technical failure ≠ governance denial.**

Governance or validation meaning must not be reduced to generic technical status unless the applicable owning semantics explicitly define that meaning.

### 17.12 Provenance Invariants

Engineering Provenance establishes traceability, not authority or responsibility by association.

Therefore:

> **Evidence source ≠ determination authority.**

> **Derived from ≠ approved by.**

> **Produced by ≠ authoritative owner.**

> **Recorded by ≠ performed by.**

> **Performed by ≠ responsible for.**

> **Responsible for ≠ authorized to determine.**

> **Recorded ≠ established.**

Technical telemetry, logs, traces, or audit records are not inherently sufficient Engineering Provenance.

### 17.13 Continuity Invariants

Engineering continuity must be reconstructable from authoritative sources and materially required durable Engineering state rather than dependence upon a particular execution instance or participant memory.

Therefore:

> **Continuity ≠ runtime persistence.**

> **Resumption ≠ replay.**

> **Recoverable ≠ current.**

Replacement of a session, process, interface, Execution Instance, Human participant, or AI runtime must not by itself alter Engineering identity, responsibility, authority, or authoritative Engineering state.

Where current Engineering conditions matter, resumption requires applicable re-resolution or re-determination rather than assumption from historical state.

### 17.14 Human and AI Engineering Invariants

Human Engineers and AI Engineers participate under the same authoritative Engineering semantics.

Therefore:

> **Participant-specific mechanism ≠ participant-specific Engineering model.**

Differences in representation, interaction mechanism, execution environment, enforcement, provenance capture, or continuity mechanism must not create separate Engineering truth, authority, responsibility, governance, validation, or lifecycle semantics.

Neither Human action nor AI capability independently establishes Engineering authority.

### 17.15 Platform and Implementation Invariants

Architectural responsibility does not require Platform internalization or prescribe implementation topology.

Therefore:

> **Platform realization ≠ Platform internalization.**

> **Implementation co-location ≠ semantic collapse.**

> **Physical separation ≠ semantic boundary preservation.**

External systems and mechanisms may satisfy Realization Contracts where their integration preserves the required semantics, authority, state characteristics, provenance, and other applicable invariants.

Implementation architecture may vary without changing the Engineering architecture defined by this specification.

### 17.16 Engineering and Release Boundary Invariant

Engineering realization must remain distinct from downstream Release semantics.

Therefore:

> **Engineering completion ≠ Release Admission.**

> **Engineering conclusion ≠ deployment.**

> **Engineering conclusion ≠ commercial launch.**

An Engineering conclusion may provide authoritative Engineering input to downstream Release activity, but it does not by itself establish downstream Release state or authority.

This specification does not define Release System semantics.

### 17.17 Invariant Closure

The Realization Model is conformant only where its applicable invariants remain true across resolution, determination, composition, projection, state establishment, persistence, execution, provenance, reconstruction, resumption, integration, and boundary crossing.

No implementation optimization, participant type, automation mechanism, AI capability, storage strategy, deployment topology, or technical convenience may override these invariants.

Where an implementation choice would make an invariant false, the implementation choice must yield to the Engineering architecture.

The governing principle is:

> **Engineering meaning must survive realization.**
