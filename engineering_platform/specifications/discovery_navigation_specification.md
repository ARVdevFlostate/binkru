# Discovery & Navigation Specification

## 1. Purpose

Discovery & Navigation enables an Engineer to orient within, discover, and navigate the Engineering environment through authoritative Engineering identities, state, and relationships without requiring prior knowledge of physical repository locations.

The capability supports both intentional discovery, where an Engineer seeks specific Engineering information, and observational discovery, where permitted by applicable participant operating constraints.

Discovery & Navigation provides navigable representations of Engineering state without creating an independent source of Engineering truth.

---

## 2. Scope

This specification defines the required semantics and realization requirements for the Discovery & Navigation capability of the Engineering Platform.

Discovery & Navigation includes:

- Engineering-environment bootstrap and orientation;
- Engineering landscape discovery;
- discovery through Engineering intent;
- navigation across authoritative Engineering identities and relationships;
- temporal navigation of durable Engineering history;
- participant-aware discovery;
- navigation from derived representations toward authoritative Engineering sources.

Discovery & Navigation operates within the Engineering state visible to the participant.

It does not independently:

- establish access or visibility policy;
- establish project or governed-work participation;
- establish responsibility or authority;
- determine authoritative contextual applicability;
- determine governed permissibility;
- own durable Engineering history;
- create or modify authoritative Engineering state;
- manufacture Engineering truth where authoritative information is missing, ambiguous, or unresolved.

Where these concerns are required to satisfy an Engineering discovery need, Discovery & Navigation composes with the applicable Engineering Platform capabilities.

---

## 3. Discovery Model

### 3.1 Engineering Discovery

Engineering discovery is navigation of the Engineering environment through authoritative Engineering identities, state, and relationships.

Discovery is not limited to repository search, filesystem traversal, textual matching, or knowledge of artifact locations.

An Engineer may discover Engineering information through:

- environment orientation;
- project and Engineering landscape exploration;
- Engineering intent;
- known Engineering identity;
- authoritative relationships;
- current Engineering state;
- durable historical state;
- participant-relative Engineering questions.

The realization mechanism may vary, but the Engineering semantics of discovery must remain consistent.

### 3.2 Engineering Identity and Physical Location

An Engineering entity's physical repository location is not its Engineering identity.

Discovery must treat authoritative Engineering identity and relationships as the stable basis for navigation where such identity and relationships exist.

Physical repository locations and representations may be resolved from Engineering identity where required for inspection or interaction.

Moving an Engineering artifact must not, by itself, change the Engineering identity or meaning of the represented Engineering entity.

### 3.3 Authoritative State

Discovery & Navigation does not create authoritative Engineering state.

Authoritative Engineering sources remain authoritative.

Discovery may expose, organize, summarize, or otherwise represent authoritative Engineering state for navigation purposes, but such representations remain derived state.

Where authoritative information within the participant's visible Engineering state is missing, ambiguous, or unresolved, Discovery must preserve that condition rather than manufacture an authoritative answer.

### 3.4 Visibility

Discovery operates within the Engineering state visible to the participant.

Visibility is independent of governed-work responsibility.

An Engineer may therefore be able to discover or navigate Engineering state for which the Engineer holds no governed-work responsibility.

Visibility or discovery does not establish:

- participation;
- responsibility;
- eligibility;
- authority;
- governed permissibility.

Discovery & Navigation does not own the policy or authority that establishes participant visibility.

### 3.5 Discovery and Engineering Intent

An Engineer is not required to know binkru terminology, capability boundaries, artifact types, or physical repository locations before expressing an Engineering discovery need.

Discovery may resolve participant terminology toward applicable binkru Engineering concepts where the relationship is supportable by the Engineering environment.

Such resolution must preserve material semantic distinctions.

Participant terminology must not be treated as equivalent to a binkru Engineering concept where authoritative semantics do not support that equivalence.

Where an Engineering intent materially maps to multiple possible concepts or destinations, the ambiguity must remain visible until sufficiently resolved.

### 3.6 Discovery and Applicability

Discoverability does not establish contextual applicability.

Discovery & Navigation determines what Engineering information, state, and relationships can be found and navigated.

Context Resolution & Composition determines what authoritative Engineering context applies to a participant's Engineering activity.

Discovery must not independently establish authoritative contextual applicability where that determination belongs to Context Resolution & Composition.

### 3.7 Discovery and Governed Action

Discovery of Engineering state does not itself authorize action upon that state.

The existence, visibility, lifecycle state, participation state, or apparent availability of governed work must not independently be interpreted by Discovery as establishing authority or governed permissibility.

Where an Engineering discovery need requires determination of participation, responsibility, eligibility, authority, or governed permissibility, the applicable Engineering Platform capability must provide that determination.

---

## 4. Bootstrap & Orientation

### 4.1 Purpose

Bootstrap & Orientation enables an Engineer to enter the Engineering environment and establish sufficient initial orientation to begin Engineering discovery without requiring prior knowledge of repository structure, physical artifact locations, or binkru-specific navigation conventions.

Bootstrap establishes discoverable entry points into the Engineering environment.

Orientation enables the Engineer to understand the environment sufficiently to navigate toward relevant Engineering capabilities, projects, Systems, governed work, and authoritative sources.

Bootstrap & Orientation does not require the Engineer to load or understand the complete Engineering environment before meaningful Engineering activity can begin.

### 4.2 Bootstrap

The Engineering environment must provide a deterministic bootstrap mechanism through which an Engineer can establish:

- the Engineering environment being entered;
- the available discovery entry points;
- how authoritative Engineering information can be reached;
- how further Engineering discovery can be initiated.

Bootstrap must not depend upon prior knowledge of physical repository locations beyond the entry mechanism through which the Engineer enters the Engineering environment.

Bootstrap information may itself be represented through one or more participant-appropriate mechanisms.

The bootstrap mechanism must navigate toward authoritative Engineering state rather than becoming an independent source of Engineering truth.

### 4.3 Orientation

Orientation provides sufficient understanding of the Engineering environment for an Engineer to determine how to continue discovery.

Orientation may include discoverable information about:

- the Engineering Platform and its capabilities;
- visible projects;
- applicable Engineering Systems;
- Development Standards;
- project entry points;
- governed work;
- other discoverable Engineering resources.

Orientation is progressive.

An Engineer must not be required to consume the complete Engineering environment, project state, or body of Engineering documentation before navigating toward the Engineering information relevant to the current need.

### 4.4 Participant-Aware Bootstrap

Human Engineers and AI Engineers may require different bootstrap and orientation representations or interaction mechanisms.

Such differences may include:

- human-readable navigation surfaces;
- machine-consumable discovery mechanisms;
- different information structures or projections;
- participant-specific operating constraints.

These differences must not create separate Engineering semantics.

Human Engineers and AI Engineers must ultimately navigate the same authoritative Engineering identities, state, and relationships subject to their applicable visibility and operating constraints.

### 4.5 Bootstrap and Participant State

Bootstrap may use participant identity and applicable participant state where required to determine the Engineering environment and discovery entry points available to the Engineer.

Bootstrap & Orientation does not itself establish:

- project or governed-work participation;
- governed-work responsibility;
- responsibility;
- eligibility;
- authority.

Where participant-relative information is required, the applicable Engineering Platform capability must provide that state.

### 4.6 Bootstrap and Effective Context

Bootstrap & Orientation does not require Effective Engineering Context to exist before discovery can begin.

Where an Engineer already has an established Engineering activity or responsibility, bootstrap may enable navigation toward the mechanisms required to resolve the applicable Effective Engineering Context.

Bootstrap must not independently determine contextual applicability or compose Effective Engineering Context.

### 4.7 Bootstrap Continuity

Bootstrap must not depend upon participant memory or previous conversational context as the authoritative means of reconstructing the Engineering environment.

A returning Engineer or replacement AI execution instance must be able to re-enter the Engineering environment without depending upon prior participant memory or ephemeral execution state.

Where prior Engineering activity is relevant to resumption, reacclimatization, or continued discovery, the applicable Continuity & Provenance and Context Resolution mechanisms provide the required durable and effective state.

### 4.8 Bootstrap Representations

Bootstrap and orientation surfaces are derived navigation representations.

They must remain traceable to the authoritative Engineering sources they represent and must not become competing sources of Engineering truth.

A bootstrap representation may provide concise explanatory or navigational information where useful, provided that materially authoritative Engineering semantics remain attributable to their authoritative sources.

---

## 5. Engineering Landscape Discovery

### 5.1 Purpose

Engineering Landscape Discovery enables an Engineer to observe and navigate the visible current state of an Engineering environment or project without requiring a specific governed-work responsibility.

Landscape discovery supports situational awareness, orientation, and acclimatization by making visible Engineering entities, activity, state, and relationships discoverable as an Engineering landscape.

Landscape discovery does not establish participation, responsibility, eligibility, authority, or governed permissibility over the Engineering state being observed.

### 5.2 Landscape Scope

An Engineering landscape may include visible current state relating to:

- projects;
- Engineering capabilities;
- Engineering Systems;
- governed work;
- lifecycle state;
- participation state;
- dependencies and other Engineering relationships;
- architecture decisions;
- Engineering conditions;
- recent Engineering activity;
- other discoverable Engineering state.

The landscape presented to an Engineer must remain within the participant's applicable visibility boundary.

The absence of governed-work responsibility does not, by itself, prevent landscape discovery where the participant's applicable operating constraints permit such observation.

### 5.3 Observational Discovery

Discovery & Navigation must support observational discovery where permitted by applicable participant operating constraints.

Observational discovery does not require the Engineer to begin with a specific Engineering information request.

It may enable an Engineer to understand:

- what Engineering work exists;
- what work is active;
- what work is available or otherwise unclaimed;
- how work is progressing;
- what Engineering decisions or conditions are visible;
- how visible Engineering entities relate to one another.

Observational discovery is informational.

Observation of Engineering state must not independently establish that the Engineer may participate in, claim, modify, transition, review, validate, or otherwise act upon the observed state.

### 5.4 Current-State Representation

Landscape discovery represents current Engineering state as derived navigation state.

A landscape representation must preserve materially significant distinctions present in authoritative Engineering state.

Where represented state may change independently of the representation, the realization must provide a means to resolve or navigate to sufficiently current authoritative state before the representation is relied upon for Engineering action.

Landscape representations must not become independent records of project or governed-work state.

### 5.5 Engineering Activity and State

Landscape discovery may expose Engineering activity through changes or current state that are visible within the Engineering environment.

Activity representations must remain attributable to the authoritative or durable Engineering state from which they are derived.

Repository activity, file modification, execution activity, or other implementation signals must not automatically be treated as equivalent to meaningful Engineering activity unless the Engineering model establishes that relationship.

### 5.6 Landscape Navigation

An Engineer must be able to navigate from a landscape representation toward the discoverable Engineering entities and relationships represented by it.

Where an entity has an authoritative source or physical representation, landscape discovery must support navigation toward that source or representation where permitted.

Landscape navigation must allow progressive exploration without requiring the Engineer to consume the complete Engineering landscape.

### 5.7 Landscape and Work Availability

Landscape discovery may expose governed work whose authoritative state indicates that it is unassigned, unclaimed, available, or otherwise open according to the applicable Engineering model.

Such representation does not independently establish that a particular Engineer is eligible or authorized to assume responsibility for that work.

Where an Engineer asks what governed work the Engineer may assume, Discovery & Navigation must obtain the applicable participation, eligibility, authority, or governance determination from the capability that owns that state.

### 5.8 Landscape and Acclimatization

Landscape discovery may support project or Engineering-environment acclimatization independently of governed-work responsibility.

Acclimatization through observation allows an Engineer to develop situational understanding from visible Engineering state without converting observed state into participant responsibility or authoritative contextual applicability.

Where acclimatization constitutes an Engineering activity requiring Effective Engineering Context, contextual applicability remains the responsibility of Context Resolution & Composition.

### 5.9 Participant-Aware Landscape Discovery

Human Engineers and AI Engineers may interact with Engineering landscapes differently according to their applicable operating constraints.

Participant-specific constraints may limit or shape observational exploration, representation, navigation depth, or the Engineering activities for which landscape discovery is permitted.

Such differences must not alter the authoritative meaning of the Engineering state represented or create participant-specific Engineering truth.

---

## 6. Intent-Based Discovery

### 6.1 Purpose

Intent-Based Discovery enables an Engineer to discover and navigate Engineering information by expressing an Engineering need without requiring prior knowledge of binkru terminology, artifact types, capability boundaries, authoritative source locations, or physical repository structure.

Engineering intent provides a discovery input.

It does not itself establish Engineering meaning, authoritative applicability, participation, responsibility, authority, or governed permissibility.

### 6.2 Engineering Intent

An Engineering intent expresses what the Engineer is attempting to understand, locate, inspect, or navigate.

Intent may be expressed using:

- natural Engineering terminology;
- binkru terminology;
- known Engineering identities;
- descriptions of Engineering concerns or outcomes;
- questions about Engineering state or relationships;
- combinations of these forms.

Discovery must not require an Engineer to translate a legitimate Engineering need into binkru-specific vocabulary before discovery can begin.

### 6.3 Intent Resolution

Discovery may resolve expressed intent toward one or more discoverable binkru Engineering concepts, identities, state, relationships, or authoritative sources.

Intent resolution must be grounded in the visible Engineering environment.

Intent resolution may use semantic or AI-assisted mechanisms, but such mechanisms must not independently create authoritative Engineering meaning or applicability.

Where authoritative Engineering identities, state, or relationships deterministically resolve the discovery need, they take precedence over semantic inference for navigation.

### 6.4 Terminology Mapping

Participant terminology may be mapped toward binkru Engineering terminology where the mapping is sufficiently supported.

Terminology mapping is navigational.

It must not manufacture semantic equivalence where the concepts materially differ.

Where participant terminology corresponds only partially to a binkru Engineering concept, Discovery must preserve the distinction rather than silently replacing the participant's concept with the binkru concept.

Where useful, Discovery may explain the distinction sufficiently to enable further navigation.

### 6.5 Ambiguous Intent

Where expressed Engineering intent materially maps to multiple discoverable interpretations, Discovery must preserve the ambiguity until it is sufficiently resolved.

Discovery may present candidate interpretations or navigation paths where doing so assists resolution.

A candidate interpretation must not be represented as authoritative merely because it is considered likely.

Intent resolution must not silently select among materially different Engineering interpretations where the available Engineering state does not support that selection.

### 6.6 Unsupported or Unresolved Intent

Where Discovery cannot sufficiently resolve an Engineering intent from the visible Engineering environment, that condition must remain visible.

Discovery must distinguish, where the visible Engineering state permits, between conditions such as:

- no discoverable matching Engineering state;
- insufficient information to resolve the intent;
- multiple unresolved interpretations;
- missing authoritative Engineering information;
- unresolved authoritative Engineering state.

Discovery must not manufacture an Engineering entity, relationship, artifact type, or authoritative answer merely to satisfy the expressed intent.

### 6.7 Intent and Authoritative Sources

Where an Engineering intent resolves toward authoritative Engineering state, Discovery must support navigation toward the authoritative sources or representations establishing that state.

A derived answer, summary, explanation, or navigation result must not replace the authoritative source from which its Engineering meaning is derived.

Where multiple authoritative sources materially contribute to the resolved result, the relevant relationships between those sources must remain navigable.

### 6.8 Intent and Capability Composition

An Engineer is not required to know which Engineering Platform capability owns the state or determination required to satisfy an Engineering intent.

Discovery & Navigation may compose with other Engineering Platform capabilities to resolve participant-relative, contextual, historical, governed, or other Engineering questions.

Such composition must preserve capability ownership.

Discovery must not assume authoritative responsibility for a determination merely because the determination is required to satisfy an expressed Engineering intent.

### 6.9 Intent and Engineering Questions

Intent-Based Discovery may support questions such as:

- what Engineering state exists;
- where authoritative Engineering information is represented;
- how Engineering entities relate;
- what changed;
- what authoritative source establishes a visible Engineering statement;
- which capability or governed mechanism owns a required Engineering determination.

Where a question requires determination of contextual applicability, participation, responsibility, eligibility, authority, governed permissibility, or other state owned by another Engineering Platform capability, Discovery must obtain or navigate toward that determination rather than infer it independently.

### 6.10 Progressive Intent Refinement

Intent resolution may proceed progressively.

An Engineer may begin with broad, incomplete, unfamiliar, or partially ambiguous terminology and refine the discovery need through subsequent navigation or interaction.

Progressive refinement must preserve previously unresolved material ambiguity until sufficient Engineering information or participant clarification resolves it.

An Engineer must not be required to formulate a complete or binkru-native query before useful discovery can begin.

---

## 7. Relationship Navigation

### 7.1 Purpose

Relationship Navigation enables an Engineer to navigate between discoverable Engineering entities, state, and authoritative sources through Engineering relationships established by the Engineering environment.

Relationship Navigation allows an Engineer to progressively move through related Engineering state without requiring prior knowledge of where related information is physically represented.

Discovery & Navigation exposes and traverses Engineering relationships.

It does not independently create authoritative Engineering relationships merely to enable navigation.

### 7.2 Authoritative Relationships

Relationship Navigation must use authoritative Engineering relationships where those relationships are established by the Engineering environment.

Such relationships may include relationships between:

- governed work and upstream intent;
- governed work and Execution Baselines;
- governed work and related governed work;
- dependencies and dependents;
- Engineering entities and architecture decisions;
- Engineering entities and Technology Profiles;
- Engineering entities and Development Standards;
- governed work and validation expectations;
- governed work and evidence;
- Engineering state and findings;
- current Engineering state and durable historical state;
- Engineering entities and their authoritative sources or physical representations.

The presence of a navigable relationship does not alter the authority or ownership of the related Engineering state.

### 7.3 Relationship Authority

Discovery & Navigation does not become the authoritative owner of an Engineering relationship by exposing or traversing it.

The capability, System, project state, governed mechanism, or authoritative source that establishes the relationship remains authoritative for that relationship.

Where a relationship is derived for navigation purposes, its derived status must remain distinguishable from an authoritative relationship.

A derived relationship must not be represented as authoritative merely because it is useful, probable, or semantically inferred.

### 7.4 Deterministic and Inferred Relationships

Where an authoritative Engineering relationship is deterministically established, Relationship Navigation must use that relationship as the basis for navigation.

Semantic, AI-assisted, textual, structural, or other inferred relationships may assist discovery of potentially related Engineering state.

An inferred relationship must not independently establish an authoritative Engineering relationship, contextual applicability, participation, responsibility, authority, or governed permissibility.

Where useful, an inferred relationship may be presented as a candidate navigation path provided its non-authoritative status remains materially clear.

### 7.5 Relationship Traversal

An Engineer must be able to navigate progressively across discoverable Engineering relationships without requiring knowledge of the physical locations of related Engineering representations.

Relationship traversal may proceed across multiple related Engineering entities where permitted by the participant's visibility boundary.

Each traversal step must preserve sufficient identity and relationship meaning for the Engineer to understand what Engineering state is being navigated and how it relates to the preceding state.

Relationship traversal must not silently cross the participant's applicable visibility boundary.

### 7.6 Bidirectional Navigation

Where the authoritative Engineering model establishes relationships that are meaningfully navigable in both directions, Discovery must support navigation in both directions.

For example, an Engineer may need to navigate:

- from governed work to its upstream intent and from upstream intent toward governed work that realizes it;
- from a dependency to its dependents and from a dependent to its dependencies;
- from an architecture decision toward affected Engineering state and from affected Engineering state toward the applicable decision;
- from evidence toward the governed work it supports and from governed work toward its evidence.

Bidirectional navigation does not require the underlying authoritative relationship to be stored or represented bidirectionally.

### 7.7 Source and Representation Navigation

Where an Engineering entity or state has an authoritative source or physical representation, Relationship Navigation must support navigation toward that source or representation where permitted.

Physical representations remain locations or representations of Engineering state rather than the semantic identity of that state.

Where an Engineering entity is represented through multiple physical artifacts or sources, Discovery must not arbitrarily present one representation as authoritative unless the Engineering environment establishes that authority.

### 7.8 Explanation Navigation

Relationship Navigation may support explanation-oriented traversal by enabling an Engineer to navigate from visible Engineering state toward the authoritative relationships, decisions, conditions, evidence, or provenance that explain how that state was established.

For example:

- a Technology Profile choice may navigate toward the architecture decision establishing it;
- a governed-work dependency may navigate toward the state establishing that dependency;
- a validation outcome may navigate toward its evidence and applicable validation expectations;
- current Engineering state may navigate toward durable provenance explaining how it changed.

Discovery & Navigation exposes the navigable basis for explanation.

It must not manufacture authoritative rationale where the Engineering environment does not establish one.

### 7.9 Missing, Broken, and Unresolved Relationships

Where an Engineering relationship established or referenced by visible Engineering state cannot be resolved, Discovery must preserve that condition.

Where the Engineering environment permits the distinction, Relationship Navigation must distinguish between conditions such as:

- no authoritative relationship is established;
- a referenced Engineering entity cannot be resolved;
- a relationship target is missing;
- relationship information is ambiguous;
- a derived or inferred relationship exists but is not authoritative.

Discovery must not silently repair, substitute, or invent an authoritative relationship to preserve navigability.

### 7.10 Relationship Navigation and Capability Composition

Relationship traversal may cross Engineering state owned by multiple Engineering Platform capabilities and Engineering Systems.

An Engineer is not required to understand those ownership boundaries before navigating the relationship.

Discovery & Navigation must preserve the authoritative ownership and semantics of each related state while providing a coherent navigation path across those boundaries.

Where traversal requires a determination owned by another Engineering Platform capability, Discovery must obtain or navigate toward that determination rather than infer it independently.

---

## 8. Temporal Navigation

### 8.1 Purpose

Temporal Navigation enables an Engineer to discover and navigate material Engineering state and relationships across time using durable Engineering history.

Temporal Navigation supports Engineering questions concerning what changed, when Engineering state changed, how current state relates to prior state, and what durable Engineering history is available for further navigation.

Discovery & Navigation does not own durable Engineering history.

Continuity & Provenance remains responsible for preserving the durable Engineering state and provenance required for temporal navigation.

### 8.2 Temporal Basis

Temporal discovery requires a sufficiently established temporal basis for the history, period, point in time, or comparison being navigated.

A temporal basis may be established from durable Engineering state where the applicable Engineering model authoritatively provides it.

An Engineer may also explicitly provide a temporal basis, such as a point in time, period of interest, or comparison boundary.

Discovery must not silently manufacture a participant-specific temporal basis from incidental implementation signals where authoritative Engineering semantics do not establish that relationship.

Signals such as repository activity, file access, login activity, conversational activity, or execution-instance activity must not automatically be treated as an Engineer's last meaningful Engineering activity.

### 8.3 Engineering Change

Temporal Navigation must operate over meaningful Engineering state and relationships rather than treating every underlying implementation change as an Engineering change.

Engineering changes may include changes to:

- governed-work state;
- participation state;
- authoritative Engineering relationships;
- architecture decisions;
- Technology Profiles;
- Development Standards;
- Engineering conditions;
- validation state;
- evidence or findings;
- other durable Engineering state.

Repository commits, file modifications, execution events, or other implementation signals may assist temporal discovery where useful, but they must not independently establish meaningful Engineering change unless the Engineering model establishes that relationship.

### 8.4 Change Navigation

Where durable Engineering history permits, an Engineer must be able to navigate:

- from current Engineering state toward relevant prior state;
- from prior Engineering state toward subsequent state;
- between materially different states across a temporal boundary;
- toward durable provenance associated with an Engineering change;
- toward authoritative Engineering entities and relationships affected by the change.

Temporal navigation must preserve sufficient Engineering identity and state meaning to distinguish what changed from how the underlying representation changed.

### 8.5 Current and Historical State

Temporal Navigation must preserve material distinctions between:

- historical Engineering state;
- current Engineering state;
- current authoritative Engineering state;
- current contextual applicability.

Engineering state that was historically authoritative, or whose historical applicability is established by durable Engineering state, must not be represented as currently authoritative or applicable solely because it is preserved in durable history.

Where historical and current state differ, Discovery must preserve that distinction during navigation.

### 8.6 Temporal Landscape Discovery

Landscape discovery may be evaluated relative to a temporal boundary to support questions such as:

- what changed during a period;
- what governed work progressed;
- what Engineering state was created, completed, superseded, abandoned, or otherwise changed;
- what decisions or Engineering conditions changed;
- what visible Engineering relationships changed.

A temporal landscape is a derived navigation representation.

It must remain attributable to the durable and authoritative Engineering state from which it is derived and must not become an independent historical record.

### 8.7 Reacclimatization

Temporal Navigation may support reacclimatization by enabling a returning Engineer to discover material Engineering changes since an established or explicitly supplied temporal boundary.

Reacclimatization does not require an active governed-work responsibility.

Temporal reacclimatization provides navigation of Engineering change.

It does not independently determine which changes are contextually applicable or materially relevant to a particular current Engineering activity.

Where activity-specific relevance is required, Context Resolution & Composition determines the applicable Effective Engineering Context.

### 8.8 Resumption

Temporal discovery may contribute durable change information required for resumption of interrupted Engineering work.

Resumption Context is not a temporal-discovery representation.

Context Resolution & Composition remains responsible for reconstructing Effective Engineering Context for resumed work from current authoritative and durable Engineering state.

Temporal Navigation may enable an Engineer to inspect the historical changes, prior state, and provenance contributing to that Resumption Context.

### 8.9 Explanation Across Time

Temporal Navigation may compose with Relationship Navigation and Continuity & Provenance to enable an Engineer to understand how current Engineering state developed.

Where durable provenance permits, an Engineer may navigate from a current state through relevant changes toward prior state, decisions, evidence, findings, or other Engineering state associated with its evolution.

Temporal Navigation exposes the durable basis for such explanation.

It must not manufacture causal rationale merely because two Engineering changes are temporally related.

### 8.10 Intermediate and Superseded State

Durable Engineering state may remain temporally discoverable even where it is no longer part of current Engineering state.

Where preserved history permits, Temporal Navigation may expose intermediate, superseded, abandoned, reverted, or otherwise historical Engineering state when relevant to the temporal discovery need.

The existence of historical state does not establish its current applicability.

Discovery must preserve its historical status during navigation.

### 8.11 Temporal Visibility

Temporal Navigation operates within the participant's applicable visibility boundary.

The fact that Engineering state existed historically does not independently establish that the state, its prior representation, or its provenance is visible to the participant.

Temporal navigation must not use historical information to bypass current visibility constraints.

### 8.12 Temporal Navigation and Capability Composition

Temporal Navigation depends upon durable Engineering history and provenance supplied by the applicable Continuity & Provenance mechanisms.

Where a temporal question requires determination of contextual applicability, participation, responsibility, authority, governed permissibility, or other state owned by another Engineering Platform capability, Discovery must obtain or navigate toward that determination rather than infer it independently.

Discovery & Navigation must preserve the distinction between navigating Engineering history and determining what that history means for a participant's current Engineering activity.

---

## 9. Participant-Aware Discovery

### 9.1 Purpose

Participant-Aware Discovery enables Discovery & Navigation to account for authoritative participant state where an Engineering discovery need depends upon the participant's relationship to the Engineering environment, project, governed work, or Engineering activity.

Participant-aware discovery allows discovery results and navigation to reflect applicable participant state without making Discovery & Navigation the authority for that state.

### 9.2 Participant-Relative Discovery

Some Engineering discovery needs are independent of participant state.

For example, an Engineer may discover:

- what visible projects exist;
- what governed work is visible;
- what authoritative Engineering state is represented;
- how visible Engineering entities relate;
- what visible Engineering changes occurred.

Other discovery needs require participant-relative determination.

These may include questions concerning:

- the projects in which the Engineer participates;
- governed work for which the Engineer holds responsibility;
- governed work the Engineer may be eligible to assume;
- Engineering activities within the Engineer's participation scope;
- authority applicable to the Engineer;
- governed actions permitted to the Engineer.

Where participant-relative determination is required, Discovery & Navigation must obtain the applicable authoritative participant state or determination from the Engineering Platform capability or governed mechanism that owns it.

### 9.3 Visibility and Participation

Visibility and participation are distinct.

An Engineer may be able to discover Engineering state without participating in the project or governed work represented by that state where the applicable visibility and operating constraints permit it.

Conversely, participation does not require Discovery & Navigation to expose Engineering state beyond the participant's applicable visibility boundary.

Discovery must not infer participation from visibility, navigation, observation, or prior interaction with Engineering state.

### 9.4 Participation and Responsibility

Project participation and governed-work responsibility are distinct Engineering relationships.

Discovery of project participation must not be interpreted as establishing responsibility for governed work within that project.

Discovery of governed-work responsibility must be grounded in the authoritative participation state that establishes that responsibility.

The absence of governed-work responsibility does not, by itself, prevent discovery of visible governed work or other visible project Engineering state.

### 9.5 Eligibility and Work Availability

The authoritative state of governed work and the eligibility of a particular Engineer to assume responsibility for that work are distinct.

Discovery may expose governed work whose authoritative state indicates that it is unassigned, unclaimed, available, or otherwise open.

Discovery must not infer from that state alone that a particular Engineer may assume responsibility for the work.

Where an Engineer seeks governed work that the Engineer may assume, Discovery must obtain the applicable eligibility, participation, authority, or governance determination rather than derive eligibility solely from discovered work state.

### 9.6 Authority and Governed Permissibility

Participant-aware discovery may expose authoritative participant state relevant to Engineering authority or governed permissibility.

Discovery & Navigation does not independently establish that authority or permissibility.

Where an Engineer asks what action the Engineer may perform, Discovery must distinguish navigation of relevant participant and governed state from the authoritative determination that permits the action.

A discovery representation of a permitted action must remain attributable to the authoritative state or governed determination establishing that permission.

### 9.7 Participant State Changes

Participant state may change independently of an existing discovery representation.

Changes to project participation, governed-work responsibility, eligibility, authority, or other participant state may therefore affect participant-relative discovery results.

Where participant-relative discovery is relied upon for Engineering action, the realization must provide a means to resolve sufficiently current authoritative participant state.

A previous discovery result must not itself preserve or extend participant state that is no longer authoritative.

### 9.8 Human and AI Engineers

Participant-aware discovery applies to both Human Engineers and AI Engineers.

Human Engineer and AI Engineer participation may be governed by different operating constraints, responsibility models, or authority rules.

Discovery & Navigation must use the applicable authoritative participant state rather than infer permissions or restrictions solely from participant type.

Participant type may affect how discovery is represented or how permitted discovery activities are performed, but it must not create a separate source of Engineering truth.

### 9.9 Participant Identity

Where a discovery need depends upon participant-relative state, the participant must be sufficiently identifiable for the applicable authoritative state or determination to be resolved.

Discovery & Navigation may use established participant identity for this purpose.

It does not independently establish authoritative participant identity.

Where participant identity cannot be sufficiently resolved, Discovery must preserve that condition rather than infer participant-relative state from conversational identity, execution context, repository activity, or other incidental signals.

### 9.10 Participant-Aware Navigation

Participant-relative determinations may themselves provide navigation into the authoritative Engineering state that establishes them.

For example, an Engineer may navigate from:

- project participation toward the authoritative participation state;
- governed-work responsibility toward the governed work and participation state establishing it;
- an eligibility determination toward the state or governed mechanism establishing that determination;
- an authority or permissibility determination toward its authoritative basis.

Discovery must preserve capability and state ownership throughout such navigation.

Navigability of a participant-relative determination does not transfer authority for that determination to Discovery & Navigation.

---

## 10. Context and Applicability

### 10.1 Discovery and Effective Engineering Context

Discovery & Navigation and Context Resolution & Composition are distinct capabilities.

Discovery & Navigation enables an Engineer to discover and navigate Engineering information, state, and relationships.

Context Resolution & Composition determines what authoritative Engineering context applies to a participant's current Engineering activity and composes the applicable Effective Engineering Context.

Discoverability, visibility, proximity, semantic relevance, or relationship to governed work must not independently establish contextual applicability.

### 10.2 Navigation from Effective Engineering Context

Effective Engineering Context must remain navigable toward the authoritative Engineering sources, identities, state, and relationships from which it is derived.

Discovery & Navigation may enable an Engineer to inspect those sources and navigate toward additional visible Engineering state.

Such navigation does not modify the authoritative applicability established by Context Resolution & Composition.

Additional discovered information does not become part of Effective Engineering Context merely because the Engineer navigates to it.

### 10.3 Context Challenge and Discovery

Where an Engineer believes Effective Engineering Context is incorrect, incomplete, ambiguous, or stale, Discovery & Navigation may support navigation toward the authoritative state and relationships relevant to that concern.

Resolution of a Context Challenge remains the responsibility of the applicable Context Resolution & Composition and governed mechanisms.

Discovery must not repair Effective Engineering Context by independently modifying its derived applicability.

---

## 11. Governance and Explanation Navigation

### 11.1 Governed State Navigation

Discovery & Navigation may expose and navigate governed Engineering state, governing relationships, validation expectations, evidence, findings, conditions, and other visible state relevant to governed Engineering activity.

Navigability of governed state does not establish governed permissibility.

Where a question requires an authoritative determination of whether an Engineering action or transition is permitted, Governance & Validation Integration or the applicable governed mechanism remains responsible for that determination.

### 11.2 Explanation Navigation

Where an authoritative governed determination is available, Discovery & Navigation may enable navigation toward the Engineering state and relationships establishing or supporting that determination.

Explanation navigation may include navigation toward:

- applicable governing conditions;
- validation expectations;
- evidence;
- findings;
- participation or authority state;
- dependencies;
- applicable decisions;
- other authoritative Engineering state contributing to the determination.

Discovery & Navigation exposes the navigable basis of the determination.

It does not independently create, override, or reinterpret the governed determination.

### 11.3 Unresolved Governed Questions

Where the authoritative Engineering environment does not establish a governed determination required by an Engineering question, Discovery must preserve that condition.

Discovery must not convert the absence of a prohibition, validation failure, finding, participant, or other visible condition into affirmative governed permission unless the applicable governance model establishes that semantic.

---

## 12. Participant Interaction

### 12.1 Common Engineering Semantics

Human Engineers and AI Engineers must discover and navigate the same authoritative Engineering identities, state, relationships, and capability semantics subject to their applicable visibility, participation, and operating constraints.

Participant-specific interaction mechanisms must not create separate Engineering truth.

### 12.2 Participant-Appropriate Interaction

Discovery & Navigation may provide different representations, structures, interaction mechanisms, or delivery forms for Human Engineers and AI Engineers.

Such differences may support:

- human-readable exploration;
- machine-consumable navigation;
- structured or conversational discovery;
- participant-appropriate progressive disclosure;
- participant-specific operating constraints.

Participant projection may alter representation, structure, emphasis, or interaction mechanism.

It must not alter authoritative Engineering meaning, normative force, relationship authority, or capability ownership.

### 12.3 AI-Assisted Interaction

AI-assisted interaction may support intent interpretation, terminology mapping, summarization, candidate relationship discovery, explanation-oriented navigation, or progressive refinement.

AI-assisted interaction must remain grounded in visible Engineering state.

Probabilistic confidence, conversational continuity, model memory, or generated explanation must not independently establish authoritative Engineering identity, state, relationship, applicability, participation, responsibility, authority, or governed permissibility.

Where authoritative resolution is required, the applicable Engineering state or Platform capability remains authoritative.

---

## 13. Derived Discovery Representations

### 13.1 Derived State

Discovery results, landscapes, summaries, navigation views, search results, temporal views, explanations, bootstrap surfaces, and other discovery representations are derived Engineering state unless the Engineering environment explicitly establishes otherwise.

A derived discovery representation is not an independent source of Engineering truth.

### 13.2 Provenance and Traceability

Derived discovery representations must preserve sufficient provenance to identify or navigate toward the authoritative or durable Engineering state from which their materially significant Engineering meaning is derived.

Where a representation combines Engineering state from multiple authoritative sources, the contribution of those sources must remain sufficiently traceable for Engineering inspection.

### 13.3 Currency

A derived discovery representation may become stale as authoritative Engineering state changes.

Where the represented state may materially affect Engineering action, the realization must provide a means to resolve or navigate toward sufficiently current authoritative state before reliance upon the derived representation.

A stale representation must not preserve superseded Engineering state as currently authoritative.

### 13.4 Representation Semantics

Derived representations may organize, summarize, rank, filter, translate, or otherwise transform Engineering information for navigation purposes.

Such transformation must preserve materially significant Engineering distinctions.

A representation must not flatten authoritative requirements, prohibitions, permissions, unresolved ambiguity, historical state, inferred relationships, or other materially different Engineering semantics into equivalent guidance.

---

## 14. Missing, Ambiguous, and Unresolved Information

### 14.1 Preservation of Information State

Discovery & Navigation must preserve materially different information conditions where the visible Engineering environment permits those conditions to be distinguished.

Such conditions may include:

- no discoverable matching Engineering state;
- missing authoritative Engineering information;
- unresolved authoritative Engineering state;
- ambiguous Engineering intent;
- ambiguous relationship information;
- unresolved Engineering identity or relationship target;
- derived or inferred information that is not authoritative.

These conditions must not be silently collapsed into a single successful, unsuccessful, or assumed result where doing so would alter Engineering meaning.

### 14.2 No Manufactured Resolution

Discovery must not manufacture authoritative Engineering truth to resolve missing, ambiguous, conflicting, or unresolved information.

Semantic inference, AI-assisted reasoning, participant assumptions, repository structure, naming conventions, or implementation signals may assist navigation or identify candidate interpretations.

They must not independently resolve authoritative ambiguity where an applicable authoritative or governed mechanism is required.

### 14.3 Progressive Resolution

Missing or ambiguous information may be progressively resolved through:

- additional Engineering navigation;
- participant clarification;
- authoritative relationship traversal;
- resolution by another Engineering Platform capability;
- applicable governed mechanisms.

Until sufficiently resolved, materially unresolved conditions must remain visible in the discovery result or navigation path.

---

## 15. Capability Integrations

### 15.1 Participation & Scope

Discovery & Navigation obtains authoritative participant state from Participation & Scope where discovery depends upon project participation, governed-work responsibility, eligibility, or other participant relationships owned by that capability.

Discovery does not independently establish or modify that state.

### 15.2 Context Resolution & Composition

Discovery & Navigation provides navigation across visible Engineering state and relationships that may contribute to context resolution.

Context Resolution & Composition remains responsible for determining authoritative contextual applicability and composing Effective Engineering Context.

Discovery does not independently establish contextual applicability.

### 15.3 Governance & Validation Integration

Discovery & Navigation may expose and navigate governed state, validation expectations, evidence, findings, conditions, and authoritative determinations.

Governance & Validation Integration remains responsible for the applicable governed and validation determinations it owns.

Discovery does not independently establish governed permissibility or validation outcome.

### 15.4 Continuity & Provenance

Discovery & Navigation relies upon Continuity & Provenance for durable Engineering history and provenance required for temporal and explanation-oriented navigation.

Discovery may represent and navigate that history but does not become its authoritative durable record.

### 15.5 Execution Enablement

Discovery & Navigation may expose and navigate Execution Capabilities, Execution Environments, Engineering Tools, Engineering Automation, execution-related Engineering state, and materially significant Execution Provenance where such information is discoverable according to the applicable Engineering semantics.

Execution Enablement may consume Engineering entities, relationships, history, provenance, and other discoverable Engineering state surfaced through Discovery & Navigation where required to support Engineering execution.

Discovery & Navigation does not independently establish that a discovered Execution Capability is available for use, permitted, or applicable to a particular Engineering Activity.

Execution Enablement remains responsible for resolving Execution Availability and enforcing applicable execution constraints within the execution surfaces it provides or controls.

### 15.6 Cross-Capability Composition

Discovery & Navigation may compose with multiple Engineering Platform capabilities where satisfying an Engineering discovery need requires state or determinations owned across capability boundaries.

Discovery does not become authoritative for composed determinations merely because it provides the participant-facing navigation or representation through which those determinations are reached.

### 15.7 Engineering Systems

Discovery & Navigation may traverse Engineering identities, state, relationships, and authoritative sources owned by multiple Engineering Systems.

Engineering Systems retain ownership of the Engineering semantics and authoritative state they establish.

Discovery provides coherent navigation across those boundaries without redefining their semantics.

---

## 16. Capability Boundaries

Discovery & Navigation is responsible for enabling orientation, discovery, and navigation across visible Engineering identities, state, relationships, authoritative sources, and durable history.

Discovery & Navigation does not independently:

- create or modify authoritative Engineering state;
- establish Engineering identity where no authoritative identity exists;
- create authoritative Engineering relationships;
- establish access or visibility policy;
- establish participant identity;
- establish project or governed-work participation;
- establish governed-work responsibility or eligibility;
- establish Engineering authority;
- determine authoritative contextual applicability;
- compose Effective Engineering Context;
- determine governed permissibility;
- determine validation outcomes;
- own durable Engineering history or provenance;
- manufacture authoritative rationale, causality, or semantic equivalence;
- convert inferred, semantic, probabilistic, or generated information into authoritative Engineering truth.

Where discovery requires state or a determination owned elsewhere, Discovery & Navigation must obtain, expose, or navigate toward the applicable authoritative state or capability without assuming ownership of that determination.

---

## 17. Realization Requirements

A realization of Discovery & Navigation must satisfy the following requirements.

### DN-R01 — Deterministic Bootstrap

The realization must provide a deterministic mechanism through which an Engineer can enter the Engineering environment, establish available discovery entry points, and begin navigation without prior knowledge of physical repository structure beyond the entry mechanism itself.

### DN-R02 — Progressive Discovery

The realization must support progressive orientation and discovery without requiring the Engineer to load, inspect, or understand the complete Engineering environment before useful navigation can begin.

### DN-R03 — Engineering Identity Navigation

The realization must navigate authoritative Engineering identities and relationships independently of physical repository location where authoritative identity and relationships exist.

Physical representation may be resolved from Engineering identity but must not substitute for that identity.

### DN-R04 — Landscape Discovery

The realization must support discovery and navigation of visible Engineering landscapes independently of governed-work responsibility where applicable participant operating constraints permit observation.

Landscape discovery must not confer participation, responsibility, eligibility, authority, or governed permissibility.

### DN-R05 — Intent-Based Discovery

The realization must support discovery through Engineering intent without requiring prior knowledge of binkru terminology, artifact types, capability boundaries, authoritative source locations, or physical repository structure.

Material ambiguity or semantic mismatch must remain visible until sufficiently resolved.

### DN-R06 — Authoritative Relationship Navigation

The realization must support progressive traversal of authoritative Engineering relationships and navigation toward their authoritative sources or representations where permitted.

Inferred or derived relationships must remain distinguishable from authoritative relationships.

### DN-R07 — Temporal Navigation

The realization must support navigation of durable Engineering history where such history is available, preserving the distinction between historical state, current state, current authoritative state, and current contextual applicability.

Temporal navigation must not treat incidental implementation activity as meaningful Engineering history unless the Engineering model establishes that relationship.

### DN-R08 — Participant-Aware Discovery

Where a discovery need depends upon participant-relative state, the realization must obtain the applicable authoritative participant state or determination rather than infer participation, responsibility, eligibility, authority, or governed permissibility from visibility, participant type, prior interaction, or discovered work state.

### DN-R09 — Visibility Preservation

All discovery and navigation must remain within the participant's applicable visibility boundary.

Navigation, relationship traversal, temporal history, derived representations, or participant-relative discovery must not provide a mechanism for bypassing that boundary.

### DN-R10 — Authoritative Source Navigation

Derived discovery representations must preserve sufficient provenance and navigability toward the authoritative or durable Engineering sources from which their materially significant Engineering meaning is derived.

### DN-R11 — Current-State Resolution

Where a derived or participant-relative discovery result may materially affect Engineering action, the realization must provide a means to resolve or navigate toward sufficiently current authoritative state before reliance upon that result.

### DN-R12 — Semantic Preservation

The realization must preserve materially significant distinctions among authoritative, derived, inferred, historical, ambiguous, unresolved, permitted, prohibited, and otherwise materially different Engineering state.

Representation, summarization, ranking, filtering, terminology mapping, or AI-assisted interaction must not erase those distinctions.

### DN-R13 — Missing and Ambiguous State

The realization must preserve missing, ambiguous, unresolved, or non-authoritative conditions where the visible Engineering environment permits those conditions to be distinguished.

It must not manufacture authoritative Engineering truth to satisfy a discovery request.

### DN-R14 — Capability Ownership

Where satisfying a discovery need requires a state or determination owned by another Engineering Platform capability or Engineering System, the realization must obtain or navigate toward that authoritative state or determination while preserving its ownership.

Discovery & Navigation must not assume authority for the determination merely because it presents the result.

### DN-R15 — Participant-Appropriate Realization

The realization may provide different interaction mechanisms or representations for Human Engineers and AI Engineers.

Such differences must preserve common authoritative Engineering semantics and must not create participant-specific Engineering truth.

### DN-R16 — Durable Re-entry

The realization must allow a returning Engineer or replacement AI execution instance to re-enter the Engineering environment without depending upon prior participant memory, conversational continuity, or ephemeral execution state as authoritative bootstrap state.

---

## 18. Invariants

The following invariants must hold for every conforming realization of Discovery & Navigation.

1. **Discovery does not create Engineering truth.**  
   Discovery may expose, derive, organize, summarize, infer, or navigate Engineering information, but authoritative Engineering state remains authoritative.

2. **Discovery does not confer participation or authority.**  
   Visibility, discoverability, navigation, observation, or apparent work availability does not establish participation, responsibility, eligibility, authority, or governed permissibility.

3. **Engineering identity is not physical location.**  
   Physical repository paths and representations may locate Engineering state but do not substitute for authoritative Engineering identity where such identity exists.

4. **Derived discovery state remains attributable.**  
   Material Engineering meaning presented through a derived discovery representation remains traceable to the authoritative or durable Engineering state from which it is derived.

5. **Historical state does not imply current applicability.**  
   Preservation or discovery of historical Engineering state does not establish that the state remains currently authoritative or contextually applicable.

6. **Participant projections preserve Engineering semantics.**  
   Human Engineer and AI Engineer representations or interaction mechanisms may differ, but they must preserve the same authoritative Engineering meaning subject to applicable visibility and operating constraints.

7. **Material information distinctions remain visible.**  
   Missing, ambiguous, unresolved, inferred, derived, and authoritative information states must remain materially distinguishable where the distinction affects Engineering meaning.

8. **Capability composition does not transfer authority.**  
   Discovery & Navigation may compose state and determinations from other Engineering Platform capabilities and Engineering Systems for navigation purposes, but authoritative ownership remains with the capability, System, governed mechanism, or source that establishes them.
