# Continuity & Provenance Specification

## 1. Purpose

Continuity & Provenance preserves materially significant Engineering state, relationships, history, and attribution required for Engineering activity to remain intelligible, traceable, and resumable across time, participant changes, interruptions, handovers, execution-instance replacement, and changes to authoritative Engineering state.

The capability enables current Engineering state to be understood in relation to its materially significant origin, derivation, prior state, and authoritative relationships without making participant memory, conversational continuity, or ephemeral execution state a prerequisite for Engineering continuity.

Continuity & Provenance preserves the distinction between current authoritative Engineering state, durable Engineering history, and provenance explaining materially significant Engineering state.

It does not make state authoritative merely because that state is persisted, historical, attributable, or available.

---

## 2. Scope

This specification defines the required semantics and realization requirements for the Continuity & Provenance capability of the Engineering Platform.

Continuity & Provenance includes:

- durable representation of materially significant Engineering state;
- preservation of materially significant Engineering history;
- provenance relationships;
- attribution;
- derivation relationships;
- temporal relationships between materially significant Engineering state;
- reconstruction of sufficiently current Engineering state and meaning;
- continuity across interruption and resumption;
- continuity across participant handover or transfer;
- continuity across AI execution-instance replacement;
- inspection and explanation of provenance;
- correction while preserving historical integrity;
- retention and availability semantics required for Engineering continuity.

Continuity & Provenance does not independently:

- establish participant identity, participation, responsibility, or authority;
- determine contextual applicability owned by Context Resolution & Composition;
- establish governed permissibility or validation outcomes;
- make historical state currently authoritative;
- make persisted state authoritative solely because it is durable;
- determine the Engineering meaning of state owned by another capability, Engineering System, authoritative source, or governed mechanism;
- require participant memory, conversational history, model memory, or ephemeral execution state to serve as authoritative Engineering history;
- require a particular persistence, eventing, versioning, database, or storage architecture.

Where continuity or provenance depends upon Engineering state owned elsewhere, Continuity & Provenance preserves the materially significant state, relationships, history, and attribution required by the applicable Engineering semantics while preserving authoritative ownership.

---

## 3. Continuity & Provenance Model

### 3.1 Engineering Continuity

Engineering Continuity is the preservation of materially significant Engineering state and meaning required for Engineering activity to remain intelligible and resumable across discontinuity.

Discontinuity may include:

- interruption;
- participant absence;
- participant handover or transfer;
- execution-instance replacement;
- system restart;
- passage of time;
- material change to authoritative Engineering state;
- other loss of ephemeral participant or execution context.

Engineering Continuity does not require preservation of every transient interaction, reasoning step, implementation detail, or participant memory.

It requires sufficient durable Engineering state to preserve or reconstruct the materially significant Engineering state and meaning necessary for the applicable Engineering activity.

### 3.2 Durable Engineering State

Durable Engineering State is Engineering state preserved beyond the ephemeral interaction or execution context in which it was produced, observed, or used.

Durability does not independently establish:

- authority;
- correctness;
- applicability;
- currency;
- normative force;
- governed permissibility;
- validation success.

The authoritative meaning of durable state remains established by the capability, Engineering System, authoritative source, or governed mechanism that owns that meaning.

### 3.3 Provenance

Provenance describes materially significant relationships explaining the origin, attribution, derivation, basis, or lineage of Engineering state.

Provenance may identify relationships to:

- authoritative sources;
- participants;
- Engineering activities;
- governed work;
- prior Engineering state;
- derived Engineering state;
- evidence;
- findings;
- determinations;
- changes;
- applicable Engineering conditions;
- other materially significant Engineering state.

Provenance must preserve the semantics and authority of the state and relationships it describes.

The existence of provenance does not independently establish that the described Engineering state is correct, current, applicable, or authoritative.

### 3.4 Authoritative and Historical State

Current authoritative Engineering state and historical Engineering state are distinct.

Historical state records Engineering state that previously existed, applied, was authoritative, was observed, or otherwise forms part of materially significant Engineering history according to the applicable Engineering model.

Historical availability does not make historical state currently authoritative.

Where authoritative state changes, Continuity & Provenance must preserve sufficient distinction between prior and current state to prevent historical state from being silently represented as current.

### 3.5 Engineering Change

A materially significant Engineering change is a change to Engineering state or relationships whose preservation is required for continuity, provenance, reconstruction, explanation, or another applicable Engineering concern.

Not every implementation event or state mutation is necessarily a materially significant Engineering change.

The applicable Engineering semantics determine what change must be durably represented.

Continuity & Provenance must not infer Engineering significance solely from implementation-level event volume or technical persistence behavior.

### 3.6 Attribution

Attribution identifies the participant, mechanism, Engineering System, authoritative source, or other origin materially responsible for producing, establishing, modifying, or determining Engineering state.

Attribution must preserve the distinction between:

- performing an Engineering activity;
- producing information or evidence;
- proposing a change;
- authoritatively establishing state;
- approving or validating state;
- recording or persisting state.

A participant or mechanism must not be represented as authoritatively establishing Engineering state merely because it transmitted, stored, displayed, or otherwise handled that state.

### 3.7 Derivation

Derived Engineering state is Engineering state produced from other Engineering state through an applicable derivation mechanism.

Where derived state is materially significant, its provenance must preserve sufficient relationships to explain its authoritative basis and derivation.

Derivation does not transfer authoritative ownership from source state to the derived representation.

Derived state must remain distinguishable from the authoritative source state from which it was produced.

Where source state materially changes, the applicable Engineering semantics determine whether derived state remains current, becomes stale, or requires reconstruction or re-derivation.

### 3.8 Reconstruction

Reconstruction produces a sufficiently current and materially complete representation of Engineering state or meaning from authoritative and durable Engineering state.

Reconstruction must not require participant memory, prior conversational context, model memory, or ephemeral execution state as an authoritative source.

Reconstruction need not reproduce every historical interaction or implementation event.

It must preserve the materially significant Engineering semantics required by the applicable activity.

Where authoritative or durable state is insufficient for reliable reconstruction, that insufficiency must remain explicit rather than being silently filled through inference.

### 3.9 Retention and Availability

Engineering continuity depends upon materially significant Engineering state and provenance remaining available for as long as required by the applicable Engineering semantics.

Retention does not imply indefinite preservation of all Engineering state.

The applicable Engineering model determines what state must remain available, for what purpose, and for what required duration or lifecycle.

Where required durable state or provenance is unavailable, incomplete, corrupted, or otherwise unusable, the resulting continuity or provenance limitation must remain explicit.

Continuity & Provenance must not manufacture missing historical or authoritative state to conceal such loss.

---

## 4. Durable Engineering State

### 4.1 Durability Requirement

Engineering state must be durably represented where its loss would materially impair Engineering continuity, provenance, reconstruction, explanation, governance, validation, resumption, or another applicable Engineering concern.

The applicable Engineering semantics determine what state requires durability.

Technical availability, implementation convenience, storage mechanism, or frequency of access does not independently determine Engineering durability requirements.

### 4.2 Durable-State Scope

Durable Engineering State may include materially significant:

- authoritative Engineering state;
- participant and responsibility state;
- governed-work state;
- Engineering relationships;
- Execution Baselines;
- determinations;
- evidence and findings;
- derived Engineering state;
- Engineering history;
- provenance;
- changes;
- exceptions or waivers;
- other state required for Engineering continuity.

The inclusion of state in durable representation does not change its authoritative semantics.

### 4.3 Authoritative Durable State

Where authoritative Engineering state requires durability, its durable representation must preserve sufficient identity, meaning, authority, scope, and other materially significant semantics for continued Engineering use.

Durability does not create or transfer authority.

The capability, Engineering System, authoritative source, or governed mechanism owning the Engineering state remains authoritative for its meaning.

### 4.4 Derived Durable State

Derived Engineering state may be durably represented where required for continuity, performance, explanation, provenance, historical understanding, or another applicable Engineering concern.

Persistence of derived state does not make it authoritative over its source state.

Where materially significant source state changes, the applicable Engineering semantics determine whether persisted derived state remains current, becomes stale, requires re-derivation, or remains available only as historical state.

### 4.5 Durable Relationships

Materially significant Engineering relationships required for continuity or provenance must be durably representable.

A durable relationship must preserve sufficient relationship semantics to distinguish materially different Engineering relationships.

Durability of a relationship does not independently establish that the relationship remains current.

### 4.6 Durable Identity

Durable Engineering State must preserve sufficient identity to distinguish materially different Engineering entities, states, relationships, determinations, evidence, findings, changes, or other Engineering concerns.

Identity must remain sufficiently stable across applicable Engineering continuity boundaries to support provenance, history, reconstruction, and resumption.

Durable identity does not require any particular identifier format or identity implementation.

### 4.7 Durable State and Ephemeral State

Not all Engineering interaction or execution state requires durability.

Ephemeral state may be discarded where its loss does not materially impair applicable Engineering continuity, provenance, reconstruction, explanation, or authoritative Engineering semantics.

State required to reconstruct materially significant Engineering meaning must not remain exclusively ephemeral.

### 4.8 Durable-State Loss

Where required Durable Engineering State is unavailable, incomplete, corrupted, or otherwise unusable, the resulting limitation must remain explicit.

Continuity & Provenance must not silently reconstruct missing durable state through inference and present the inferred result as preserved Engineering state.

The applicable Engineering model determines what Engineering activity may continue when required durable state is unavailable.

---

## 5. Provenance Relationships

### 5.1 Purpose

Provenance Relationships explain materially significant origin, attribution, derivation, basis, or lineage relationships concerning Engineering state.

Provenance Relationships supplement the Engineering state they describe.

They do not independently change the authority, applicability, currency, or normative meaning of that state.

### 5.2 Provenance Subjects and Sources

A Provenance Relationship must sufficiently identify the Engineering state whose provenance is being described and the materially significant source, participant, activity, mechanism, prior state, or other Engineering concern related to it.

A provenance source may itself have provenance.

Continuity & Provenance must support materially significant provenance chains where Engineering explanation requires relationships across multiple derivation or attribution steps.

### 5.3 Relationship Semantics

Provenance Relationships must preserve the materially significant semantics of the relationship they represent.

Different relationships such as:

- produced by;
- proposed by;
- established by;
- modified by;
- validated by;
- governed by;
- derived from;
- supersedes;
- supported by;
- based upon;
- observed during;

must not be silently represented as semantically equivalent merely because they connect the same Engineering entities.

The applicable Engineering model determines the authoritative semantics of provenance relationships.

### 5.4 Attribution Provenance

Where participant or mechanism attribution is materially significant, provenance must preserve the applicable role of that participant or mechanism in relation to the Engineering state.

Attribution must not collapse materially different participation such as proposing, producing, reviewing, validating, authorizing, establishing, recording, or persisting state into undifferentiated authorship.

### 5.5 Derivation Provenance

Where Engineering state is materially derived from other Engineering state, provenance must preserve sufficient derivation relationships to explain the materially significant basis of the derived state.

Derivation provenance must not imply that every source contributing information has equal authority or normative significance.

Where different sources contribute different semantics, those distinctions must remain representable.

### 5.6 Determination Provenance

Where determinations or Validation Determinations require durable provenance, Continuity & Provenance must preserve sufficient relationships to the materially significant state contributing to those determinations according to the applicable Governance & Validation semantics.

Preserving determination provenance does not transfer authority for the determination to Continuity & Provenance.

### 5.7 Provenance Completeness

Provenance completeness means preservation of the materially significant provenance required for the applicable Engineering concern.

It does not require recording every technical operation, intermediate representation, participant interaction, or implementation detail involved in producing Engineering state.

Where materially required provenance is missing, that limitation must remain explicit.

### 5.8 Provenance Transitivity

The existence of a chain of Provenance Relationships does not imply that every semantic property, authority, applicability condition, or normative meaning of an upstream source transfers transitively to downstream Engineering state.

Transitive provenance traversal may support explanation and lineage analysis.

Authoritative Engineering semantics determine what, if anything, propagates through a provenance chain.

---

## 6. Engineering History

### 6.1 Purpose

Engineering History preserves materially significant Engineering state and change over time.

Engineering History enables prior Engineering state and materially significant transitions between states to remain inspectable and distinguishable from sufficiently current Engineering state.

Engineering History does not make prior state currently authoritative.

### 6.2 Historical State

Historical Engineering State may include materially significant state that:

- was previously authoritative;
- was previously applicable;
- was observed;
- was proposed;
- was rejected;
- was superseded;
- was invalidated;
- resulted from an Engineering activity;
- represented a prior derived state;
- otherwise forms part of materially significant Engineering history.

Historical state must preserve its applicable historical semantics rather than being retrospectively represented as having had a different status.

### 6.3 Historical Change

Where materially significant Engineering state changes, Engineering History must preserve sufficient information to distinguish the prior state, resulting state, and materially significant change relationship.

The historical representation need not reproduce every implementation-level operation through which the change occurred.

It must preserve the Engineering meaning required to understand the materially significant change.

### 6.4 Historical Authority

State that was authoritative at an earlier time must remain distinguishable as historically authoritative where that distinction is materially significant.

A later correction, supersession, revocation, re-evaluation, or replacement must not cause prior authoritative state to be retrospectively represented as though it had never been authoritative.

Historical authority does not imply current authority.

### 6.5 Historical Non-Authority

Engineering History may preserve state that was never authoritative.

Persistence or historical inclusion of a proposal, observation, rejected state, failed attempt, inferred state, or other non-authoritative Engineering state must not cause that state to be represented as historically authoritative.

### 6.6 Correction and Historical Integrity

Where Engineering state is corrected, the correction and resulting authoritative state must remain distinguishable from the state that preceded the correction.

Correction must not rewrite materially significant Engineering history into a representation in which the corrected state appears to have always existed or always been authoritative.

Where the prior state was itself incorrectly recorded rather than historically authoritative, the applicable Engineering semantics determine how the recording defect and its correction are represented.

### 6.7 Supersession

Where Engineering state supersedes prior state, Continuity & Provenance must preserve the materially significant relationship between the superseding and superseded state.

Supersession does not inherently mean that the superseded state was incorrect.

Superseded state may remain valid historical Engineering state while no longer being current or applicable.

### 6.8 Historical Inspection

Historical Engineering State must remain distinguishable from current Engineering state during inspection and reconstruction.

Where historical state is presented without sufficient temporal or status distinction, it must not be represented in a manner likely to cause materially incorrect reliance upon it as current state.

---

## 7. Change & Temporal Semantics

### 7.1 Temporal Meaning

Engineering state may have materially significant temporal semantics concerning when it existed, applied, became authoritative, ceased to apply, was observed, was produced, was determined, or was otherwise relevant to Engineering activity.

Continuity & Provenance must preserve such temporal distinctions where required for continuity, provenance, history, reconstruction, or explanation.

### 7.2 Time and Engineering State

A recorded time value does not independently establish the Engineering semantics of a state change.

Different Engineering concerns may distinguish materially different times, including:

- when an activity occurred;
- when state was produced;
- when state became authoritative;
- when state was observed;
- when state was recorded;
- when state became applicable;
- when state ceased to apply;
- when a determination was established.

These temporal meanings must not be silently collapsed where the distinction is materially significant.

### 7.3 Change Identity

A materially significant Engineering change must be sufficiently identifiable to support applicable history, provenance, reconstruction, affected-scope analysis, or explanation.

Change identity does not require every technical mutation to receive an independent Engineering identity.

Multiple implementation operations may collectively realize one materially significant Engineering change where the applicable Engineering semantics establish that meaning.

### 7.4 Change Attribution

Where attribution of a materially significant Engineering change is required, Continuity & Provenance must preserve the materially significant relationship between the change and the participants, mechanisms, Engineering Systems, or authoritative sources involved.

Change attribution must preserve the distinction between proposing, performing, authorizing, establishing, recording, or otherwise participating in the change where those roles materially differ.

### 7.5 Change Ordering

Where the relative order of materially significant Engineering changes affects Engineering meaning, Continuity & Provenance must preserve sufficient ordering information.

Ordering need not imply that all Engineering changes across the Platform have one universal total order.

The realization must preserve the ordering semantics required by the applicable Engineering relationships and Engineering model.

### 7.6 Concurrent or Independent Change

Materially significant Engineering changes may occur concurrently or without an authoritative ordering relationship between them.

Continuity & Provenance must not manufacture a semantic ordering solely because an implementation mechanism records one change before another.

Where authoritative ordering is absent or unresolved, that condition must remain representable.

### 7.7 Current Authoritative State

Current authoritative Engineering state must be determinable from the applicable authoritative Engineering mechanisms and durable Engineering state according to the applicable Engineering semantics.

Continuity & Provenance must not determine current authoritative state solely by selecting the most recently recorded historical state.

Temporal recency and authoritative currency are distinct.

### 7.8 Temporal Reconstruction

Where Engineering activity requires reconstruction of state as of an earlier Engineering condition or time, Continuity & Provenance must support that reconstruction to the extent required by the applicable Engineering semantics and available durable state.

Historical reconstruction must preserve the distinction between:

- what was authoritative at the reconstructed point;
- what was known or recorded at that point;
- what may have been discovered or corrected later.

Later knowledge must not be silently projected backward as though it had been available or authoritative at the reconstructed point.

### 7.9 Temporal Uncertainty

Where materially significant temporal information is missing, ambiguous, conflicting, or insufficient to establish an authoritative ordering or historical interpretation, that limitation must remain explicit.

Continuity & Provenance must not manufacture temporal precision or ordering merely to produce a complete-looking history.

---

## 8. Reconstruction & Resumption

### 8.1 Reconstruction Purpose

Reconstruction produces a sufficiently current and materially complete representation of Engineering state and meaning required for an applicable Engineering activity.

Reconstruction uses authoritative and durable Engineering state according to the applicable Engineering semantics.

It does not establish new authoritative Engineering state merely by reconstructing a representation.

### 8.2 Reconstruction Basis

Reconstruction may depend upon materially significant Engineering state from authoritative sources and durable Engineering state, including:

- current authoritative Engineering state;
- Engineering relationships;
- Engineering history;
- provenance;
- participant and responsibility state;
- governed-work state;
- applicable determinations;
- evidence and findings;
- derived Engineering state;
- material changes;
- other state required by the applicable Engineering activity.

Each input retains the authority and semantics established by its owning capability, Engineering System, authoritative source, or governed mechanism.

### 8.3 Material Completeness

Reconstruction completeness means material completeness for the applicable Engineering activity.

It does not require reconstruction of every historical interaction, transient participant state, implementation event, reasoning step, or other state that does not materially affect the activity.

Where required Engineering state cannot be reconstructed with material completeness, that limitation must remain explicit.

### 8.4 Reconstruction and Inference

Inference may assist reconstruction by identifying candidate relationships, missing concerns, or potentially relevant Engineering state.

Inference must not silently manufacture missing authoritative or historical Engineering state.

Where reconstructed meaning depends upon inference rather than authoritatively or durably established state, that distinction must remain explicit where materially significant.

### 8.5 Resumption

Resumption is continuation of Engineering activity after a discontinuity.

Resumption must be based upon sufficiently current authoritative and durable Engineering state rather than requiring the participant to reproduce or remember the prior interaction or execution context.

The applicable Engineering activity determines what state must be reconstructed before resumption can proceed correctly.

### 8.6 Resumption After Material Change

Where authoritative Engineering state materially changed during an interruption, resumption must not silently continue from the previously applicable state.

The resuming participant must be able to resolve the sufficiently current Engineering state and materially significant changes required for the applicable activity.

Whether the activity may continue, requires re-evaluation, or requires another governed response is determined by the applicable Engineering semantics.

### 8.7 Resumption Position

A prior participant or execution instance having reached a particular working position does not independently establish that the same position remains valid for resumption.

Resumption position must be derived from sufficiently current authoritative and durable Engineering state.

Ephemeral indicators such as conversational position, local working memory, cached workflow state, or model memory must not independently establish the authoritative resumption position.

### 8.8 Reconstruction Failure

Where required Engineering state or provenance is unavailable, corrupted, ambiguous, conflicting, or otherwise insufficient for reliable reconstruction, that limitation must remain explicit.

Continuity & Provenance must not present a guessed or materially incomplete reconstruction as though Engineering continuity had been reliably preserved.

The applicable Engineering model determines what activity may proceed under the resulting limitation.

---

## 9. Handover & Participant Continuity

### 9.1 Handover

Handover is the continuation or transfer of Engineering activity across a change in participant involvement.

Handover may occur between:

- Human Engineers;
- AI Engineers;
- Human and AI Engineers;
- other participant arrangements established by the Engineering model.

Handover does not itself establish a change in participation, responsibility, or authority.

Such changes must occur through the applicable authoritative mechanism.

### 9.2 Handover State

A participant receiving Engineering activity through handover must be able to reconstruct the materially significant Engineering state required for the receiving participant's applicable activity.

Handover continuity must not depend upon the outgoing participant remaining available to explain undocumented materially significant Engineering state.

Participant communication may assist handover but must not substitute for durable Engineering state where loss of that communication would materially impair continuity.

### 9.3 Participant-Specific State

Not all state useful to one participant must be transferred to another participant.

Handover must preserve or enable reconstruction of the materially significant Engineering state required by the receiving participant's responsibility and activity.

Personal working preferences, transient reasoning, conversational history, or other participant-specific state need not be preserved unless the applicable Engineering semantics make that state materially significant.

### 9.4 Handover and Responsibility

Continuity & Provenance may preserve the history and provenance of responsibility or participation changes.

It does not establish those changes.

The receiving participant must resolve current participation and responsibility through the applicable Participation & Scope semantics rather than inferring responsibility from the existence of handover material.

### 9.5 Handover and Authority

Handover of Engineering information, artifacts, context, evidence, or working state does not transfer authority.

Authority applicable to the receiving participant must be established through the applicable authoritative Engineering mechanism.

### 9.6 Handover History

Where handover is materially significant to Engineering continuity or provenance, sufficient history and attribution must be preserved to explain the transition in participant involvement.

Preserving handover history must not imply that the outgoing and incoming participants held equivalent responsibility, authority, interpretation, or Engineering position.

---

## 10. AI Execution-Instance Continuity

### 10.1 Execution Instance

An AI execution instance is a particular runtime occurrence through which an AI Engineer participates in Engineering activity.

Execution-instance identity is distinct from the durable Engineering identity and participation semantics of the AI Engineer where the Engineering model establishes such continuity.

Creation, replacement, restart, or termination of an execution instance does not independently create, transfer, revoke, or otherwise change Engineering responsibility or authority.

### 10.2 Execution-Instance Replacement

Engineering activity involving an AI Engineer must remain resumable across execution-instance replacement where continuity is required by the applicable Engineering semantics.

A succeeding execution instance must be able to reconstruct the materially significant Engineering state required for the applicable activity from authoritative and durable Engineering state.

The predecessor execution instance must not be required to remain available.

### 10.3 Ephemeral AI State

Model context, hidden reasoning, conversational memory, transient plans, local runtime state, cached inference, and other execution-instance state are not independently authoritative Engineering state.

Such state may assist an execution instance while it exists.

Where information represented only in ephemeral AI state becomes materially significant to Engineering continuity, the applicable materially significant Engineering state must be durably represented through an appropriate Engineering mechanism.

### 10.4 AI Memory

AI memory or prior conversational context may assist interaction but must not be required as the authoritative basis for reconstructing materially significant Engineering state.

A succeeding execution instance must not be required to reproduce the predecessor's internal reasoning in order to continue Engineering activity correctly.

Continuity concerns the preservation of materially significant Engineering state and meaning, not preservation of an AI model's internal cognitive trajectory.

### 10.5 Execution-Instance Attribution

Where execution-instance attribution is materially significant, Continuity & Provenance must preserve sufficient distinction between:

- the AI Engineer;
- the execution instance;
- the Engineering activity;
- the authoritative mechanism establishing resulting Engineering state.

Execution-instance attribution must not cause an execution instance to be represented as possessing authority that belongs to the AI Engineer, another participant, or an authoritative Engineering mechanism.

### 10.6 Replacement and Current State

A succeeding AI execution instance must resolve sufficiently current Engineering state according to the applicable Engineering semantics.

It must not assume that state previously available to its predecessor remains current merely because that state appears in durable history, cached state, conversational records, or other retained material.

### 10.7 Replacement and Incomplete Continuity

Where durable Engineering state is insufficient for a succeeding execution instance to reconstruct materially significant Engineering meaning, that limitation must remain explicit.

The succeeding execution instance may identify or escalate the continuity defect through the applicable Engineering mechanism.

It must not silently substitute inferred predecessor intent, imagined reasoning, or reconstructed conversation for missing authoritative Engineering state.

---

## 11. Provenance Inspection & Explanation

### 11.1 Provenance Inspection

An Engineer must be able to inspect materially significant provenance required to understand Engineering state relevant to the Engineer's applicable activity.

Inspection may include navigation of:

- origin;
- attribution;
- derivation;
- authoritative basis;
- prior state;
- materially significant changes;
- supporting evidence or findings;
- determinations;
- supersession or correction relationships;
- other applicable provenance.

Inspection does not independently change the authority, applicability, or currency of the inspected state.

### 11.2 Provenance Explanation

Continuity & Provenance must support explanation of materially significant Engineering state through available provenance.

An explanation may describe:

- where state originated;
- who or what materially contributed to it;
- what authoritative state it depends upon;
- how derived state was produced;
- what materially significant changes occurred;
- what state preceded or superseded it;
- why historical and current representations differ.

An explanation must preserve uncertainty, missing provenance, conflicting state, and materially significant distinctions in authority or semantics.

### 11.3 Explanation and Authority

A provenance explanation is a representation of available Engineering state and provenance.

It does not become an independent source of Engineering truth.

Where explanation is derived or generated, its authoritative basis must remain distinguishable from the explanatory representation.

### 11.4 AI-Assisted Explanation

AI-assisted mechanisms may summarize, traverse, organize, or explain provenance.

AI-generated explanation must not silently invent missing provenance, causal relationships, authority, temporal ordering, or Engineering meaning.

Where an explanation contains inference beyond authoritative or durable provenance, that distinction must remain explicit where materially significant.

### 11.5 Provenance Depth

The depth of provenance required for inspection or explanation depends upon the applicable Engineering concern.

A participant need not be presented with every available provenance relationship where a materially sufficient explanation can be provided without loss of Engineering meaning.

Additional provenance must remain inspectable where required for deeper Engineering investigation and where available according to the applicable Engineering semantics.

### 11.6 Provenance Challenge

An Engineer must be able to challenge provenance believed to be incorrect, incomplete, ambiguous, misleading, or inconsistent with authoritative Engineering state.

A provenance challenge does not itself modify the challenged provenance or underlying Engineering state.

Correction must occur through the mechanism responsible for the affected provenance or authoritative state.

---

## 12. Integrity & Correction

### 12.1 Integrity

Continuity & Provenance must preserve the materially significant identity, meaning, relationships, history, attribution, and temporal semantics of durable Engineering state.

Integrity does not require that every historical record be immutable.

It requires that materially significant Engineering history and provenance not be silently altered into a misleading representation of what occurred, existed, was authoritative, or was known.

### 12.2 Integrity Defects

An integrity defect may include:

- missing durable Engineering state;
- corrupted state;
- incorrect attribution;
- incorrect provenance relationships;
- incorrect historical status;
- incorrect temporal information;
- improper conflation of current and historical state;
- broken derivation relationships;
- misleading reconstruction;
- other defects materially affecting continuity or provenance.

Integrity defects must remain identifiable where their existence materially affects Engineering activity.

### 12.3 Correction

Where durable Engineering state, history, or provenance is incorrect, the Platform must support correction through the applicable authoritative or provenance mechanism.

Correction must preserve sufficient information to distinguish:

- the defective state or representation;
- the nature of the defect where materially significant;
- the correction;
- the resulting state or provenance;
- applicable attribution and temporal relationships.

Correction must not silently rewrite materially significant Engineering history.

### 12.4 Correction of Authoritative State

Where the defect concerns authoritative Engineering state rather than its historical or provenance representation, correction must occur through the authoritative mechanism owning that Engineering state.

Continuity & Provenance preserves the materially significant history and provenance of the correction.

It does not independently replace authoritative Engineering state merely because a continuity or provenance defect has been identified.

### 12.5 Correction of Historical or Provenance Representation

Where authoritative Engineering state was correctly established but its durable historical or provenance representation is defective, the representation may require correction without changing the underlying authoritative Engineering history.

The correction must remain distinguishable from a change to the Engineering state itself where that distinction is materially significant.

### 12.6 Affected-Scope Identification

Where an integrity or provenance defect is discovered, Continuity & Provenance must support identification of potentially affected Engineering state, history, provenance, reconstruction, or relying Engineering activity.

Authoritatively resolvable impact must remain distinguishable from inferentially identified potential impact.

The applicable Engineering mechanisms determine the required response to identified impact.

### 12.7 Correction Provenance

A materially significant correction must itself have sufficient provenance.

Correction provenance must preserve the applicable attribution, basis, affected state, and temporal relationships required to explain why the historical or current representation differs after correction.

---

## 13. Retention, Availability & Loss

### 13.1 Retention

Materially significant Engineering state, history, and provenance must be retained for as long as required by the applicable Engineering semantics.

Retention requirements may differ according to the type, authority, lifecycle, historical significance, continuity need, governance need, validation need, or other Engineering purpose of the state.

Continuity & Provenance does not require indefinite retention of all Engineering state.

### 13.2 Availability

Retained Engineering state must remain sufficiently available for the Engineering activities that require it.

Availability requirements may differ according to the applicable Engineering concern.

Retention without sufficient availability does not satisfy continuity where the required state cannot be resolved when materially needed.

### 13.3 Loss

Loss occurs where Engineering state, history, or provenance required by applicable Engineering semantics is no longer available or usable with sufficient integrity.

Loss may result from deletion, corruption, incomplete retention, inaccessible state, broken provenance, or another condition preventing reliable Engineering use.

Loss does not authorize Continuity & Provenance to manufacture replacement historical or authoritative state.

### 13.4 Partial Loss

Continuity or provenance may be partially preserved where some required state remains available and other state has been lost.

The remaining state must not be represented as materially complete where the missing state affects continuity, provenance, reconstruction, explanation, or another applicable Engineering concern.

### 13.5 Loss and Engineering Activity

Where loss materially affects an Engineering activity, the limitation must remain explicit to the applicable participant or mechanism.

The applicable Engineering model determines whether activity may continue, requires reconstruction from other authoritative sources, requires challenge or escalation, or requires another governed response.

Continuity & Provenance must not independently convert availability of partial information into permission to continue.

### 13.6 Retention Change

A change to retention behavior must not silently remove Engineering state that remains required by applicable Engineering semantics.

Where materially significant retained state becomes eligible for removal, the applicable Engineering semantics determine whether and how that removal may occur.

Removal from active retention does not imply that the removed state was incorrect, non-authoritative, or historically insignificant.

### 13.7 External Authoritative State

Where authoritative Engineering state is retained by an external Engineering System or authoritative source, Continuity & Provenance need not duplicate that state merely to claim durability.

It must preserve or be able to resolve the materially significant identity, relationships, provenance, and availability required for Engineering continuity according to the applicable Engineering semantics.

Where continued continuity depends upon external availability, that dependency must remain materially representable.

---

## 14. Human and AI Engineer Semantics

### 14.1 Common Continuity Semantics

Human Engineers and AI Engineers are subject to the same Engineering continuity, history, provenance, attribution, and integrity semantics for equivalent Engineering concerns.

Participant type alone must not change what Engineering state is authoritative, historical, derived, current, superseded, corrected, or materially significant.

### 14.2 Participant-Specific Representation

Continuity and provenance may be represented differently for Human Engineers and AI Engineers according to their interaction mechanisms and Engineering activities.

Participant-specific representation may alter structure, summarization, navigation, emphasis, or delivery mechanism.

It must not alter materially significant Engineering meaning, authority, provenance, historical status, uncertainty, or temporal semantics.

### 14.3 Human Engineer Memory

Human Engineer memory, recollection, or undocumented understanding may assist Engineering activity.

They must not be required as the sole authoritative basis for materially significant Engineering continuity where loss of that participant would materially impair the applicable Engineering activity.

Where a Human Engineer identifies materially significant state absent from durable Engineering state, that state must be established or preserved through the applicable Engineering mechanism before it can serve as authoritative durable Engineering state.

### 14.4 AI Engineer State

AI conversational context, model memory, hidden reasoning, transient plans, or execution-instance state may assist Engineering activity.

They do not independently become authoritative Engineering state or durable Engineering history.

Where materially significant Engineering state emerges through AI participation, that state must be established or preserved through the applicable Engineering mechanism according to its Engineering semantics.

### 14.5 Human and AI Handover

Engineering continuity between Human and AI Engineers must be based upon authoritative and durable Engineering state rather than assumptions about equivalent memory, reasoning, or internal representation.

Neither participant type is required to reproduce the other's internal cognitive or execution state.

The receiving participant must be able to reconstruct the materially significant Engineering meaning required for the applicable activity.

### 14.6 Attribution Across Participant Types

Provenance must preserve materially significant attribution for Human Engineers, AI Engineers, execution instances, mechanisms, and Engineering Systems according to their actual Engineering roles.

Attribution must not collapse materially different roles merely to normalize Human and AI participation into a common technical representation.

### 14.7 Participant Replacement

Replacement of a Human Engineer, AI Engineer, or AI execution instance must not independently change authoritative Engineering state, responsibility, authority, determinations, Validation Determinations, or other Engineering semantics.

Any such change must occur through the applicable authoritative Engineering mechanism.

Continuity & Provenance must preserve sufficient durable state and provenance for the succeeding participant to resolve the applicable current Engineering position.

---

## 15. Capability Integrations

### 15.1 Discovery & Navigation

Continuity & Provenance provides materially significant durable Engineering state, history, provenance, change relationships, and temporal semantics that may be discovered or navigated through Discovery & Navigation.

Discovery & Navigation may support inspection of:

- historical Engineering state;
- provenance relationships;
- materially significant changes;
- attribution;
- derivation;
- supersession and correction relationships;
- reconstruction-relevant state;
- other continuity or provenance information.

Discovery & Navigation does not establish the historical status, authority, provenance, temporal meaning, or integrity of the state it exposes.

Continuity & Provenance retains responsibility for the continuity and provenance semantics it owns.

### 15.2 Participation & Scope

Continuity & Provenance consumes authoritative participant, participation, responsibility, and related scope state where required for attribution, history, handover, reconstruction, or participant continuity.

Participation & Scope remains responsible for the participant relationships and responsibility semantics it owns.

Continuity & Provenance may preserve historical participation and responsibility state and the provenance of materially significant changes to that state.

Historical preservation of participation or responsibility does not establish current participation or responsibility.

### 15.3 Context Resolution & Composition

Continuity & Provenance provides durable Engineering state, history, provenance, and materially significant change information that may contribute to Effective Engineering Context and resumption context.

Context Resolution & Composition determines contextual applicability and composition according to its capability semantics.

Continuity & Provenance does not independently establish that preserved or historical Engineering state is applicable to a participant's current Engineering activity.

Where Effective Engineering Context or another derived context requires reconstruction, Continuity & Provenance may provide the durable state, history, provenance, and temporal relationships required for that reconstruction while preserving authoritative ownership and applicability semantics.

### 15.4 Governance & Validation Integration

Continuity & Provenance preserves materially significant durable state, history, provenance, attribution, and temporal relationships required by Governance & Validation Integration.

Such state may include:

- determinations;
- Validation Determinations;
- Validation Expectations;
- evidence;
- findings;
- governance conditions;
- exceptions or waivers;
- determination provenance;
- re-evaluation history;
- materially significant changes affecting governance or validation.

Governance & Validation Integration remains responsible for the governance and validation semantics and authoritative determinations it owns or integrates.

Persistence, historical availability, or provenance of a governed or Validation Determination does not independently establish that the determination remains current or applicable.

### 15.5 Execution Enablement

Continuity & Provenance consumes materially significant Material Execution State, Execution Outcomes, and Execution Provenance produced or preserved through Execution Enablement where required for Engineering continuity.

Execution Enablement must enable materially significant execution state and provenance to cross ephemeral execution boundaries according to applicable continuity semantics.

Continuity & Provenance remains responsible for the broader durability, history, provenance, reconstruction, handover, correction, retention, and continuity semantics it owns.

Execution Enablement may consume authoritative sources and durable Engineering state provided or resolved through applicable continuity mechanisms when supporting execution resumption.

Durability or preservation of execution-related state does not transfer authoritative ownership of that state to either Execution Enablement or Continuity & Provenance where authoritative ownership resides elsewhere.

### 15.6 Engineering Systems

Continuity & Provenance may consume, preserve references to, or preserve materially significant history and provenance concerning Engineering state owned by Engineering Systems.

An Engineering System remains authoritative for the Engineering state and semantics it owns.

Where authoritative Engineering state remains durably available from an Engineering System, Continuity & Provenance need not duplicate that state solely for durability.

Continuity & Provenance must preserve or support resolution of sufficient identity, provenance, relationships, temporal meaning, and availability for the applicable Engineering continuity requirements.

### 15.7 Authoritative Sources and Mechanisms

Continuity & Provenance may depend upon authoritative sources and governed mechanisms outside the capability for current or historical Engineering state.

Preservation, indexing, replication, representation, reconstruction, or explanation of such state does not transfer authoritative ownership to Continuity & Provenance.

Where the authoritative source or mechanism changes state, Continuity & Provenance must preserve materially significant historical and provenance relationships according to the applicable Engineering semantics.

### 15.8 Cross-Capability Continuity

Engineering continuity may depend upon materially significant state owned across multiple Engineering Platform capabilities, Engineering Systems, authoritative sources, and governed mechanisms.

Continuity & Provenance must preserve sufficient identity, relationships, history, provenance, and temporal semantics to support continuity across those ownership boundaries.

Cross-capability continuity does not require Continuity & Provenance to become the authoritative owner or physical persistence owner of all contributing Engineering state.

---

## 16. Capability Boundaries

Continuity & Provenance is responsible for preserving and making reconstructable the materially significant Engineering state, history, provenance, attribution, relationships, and temporal semantics required for Engineering continuity.

Continuity & Provenance does not independently:

- establish participant identity, participation, responsibility, or authority;
- establish governed-work responsibility;
- determine contextual applicability;
- establish governed permissibility;
- establish Validation Determinations or determinations;
- create authoritative Engineering state merely by persisting, reconstructing, indexing, replicating, or explaining it;
- make durable state authoritative solely because it has been preserved;
- make historical state currently authoritative;
- determine current authoritative state solely from temporal recency or recording order;
- treat historical inclusion as evidence that state was historically authoritative;
- treat provenance as proof that the state it describes is correct, current, applicable, or authoritative;
- treat provenance relationships as semantically interchangeable;
- propagate authority, applicability, normative meaning, or other Engineering semantics transitively through provenance unless the applicable Engineering semantics establish such propagation;
- infer responsibility or authority from handover;
- treat execution-instance replacement as a change in AI Engineer identity, responsibility, or authority unless the applicable Engineering model establishes such a change;
- require Human Engineer memory, AI memory, conversational context, hidden reasoning, or ephemeral execution state as the authoritative basis for Engineering continuity;
- reconstruct missing authoritative or historical Engineering state through inference and present the inferred result as preserved state;
- silently rewrite materially significant Engineering history during correction;
- correct authoritative Engineering state through a provenance mechanism where the state is owned by another authoritative mechanism;
- treat retained state as materially complete where required state has been lost;
- manufacture temporal precision, ordering, provenance, causality, or historical meaning where the available Engineering state does not establish it;
- require a particular persistence, storage, eventing, versioning, graph, database, or replication architecture.

Where continuity or provenance depends upon state owned elsewhere, Continuity & Provenance must preserve or resolve the materially significant continuity and provenance information required by the applicable Engineering semantics while preserving authoritative ownership.

---

## 17. Realization Requirements

A realization of Continuity & Provenance must satisfy the following requirements.

### CP-R01 — Material Durability

The realization must durably represent Engineering state where loss of that state would materially impair applicable Engineering continuity, provenance, reconstruction, explanation, governance, validation, resumption, or another applicable Engineering concern.

The realization must not require durability of every transient interaction, implementation event, reasoning step, or ephemeral execution state merely because it occurred during Engineering activity.

### CP-R02 — Durability and Authority Separation

The realization must preserve durability and authority as distinct Engineering semantics.

Persistence, replication, indexing, retention, or availability of Engineering state must not independently establish authority, correctness, applicability, currency, normative force, governed permissibility, or validation success.

### CP-R03 — Authoritative Ownership

Where durable Engineering state is owned by another Engineering Platform capability, Engineering System, authoritative source, or governed mechanism, the realization must preserve that authoritative ownership and materially significant semantics.

Continuity & Provenance must not become authoritative merely because it preserves or represents the state.

### CP-R04 — Durable Identity

The realization must preserve sufficient identity for materially significant Engineering entities, states, relationships, determinations, evidence, findings, changes, and other applicable Engineering concerns across required continuity boundaries.

No particular identifier format or identity implementation is required.

### CP-R05 — Durable Relationships

Materially significant Engineering relationships required for continuity or provenance must be durably representable with sufficient semantics to distinguish materially different relationship types.

Persistence of a relationship must not independently establish that the relationship remains current.

### CP-R06 — Ephemeral-State Boundary

Engineering state required to reconstruct materially significant Engineering meaning must not remain exclusively ephemeral.

Human memory, AI memory, conversational context, hidden reasoning, transient plans, cached inference, local runtime state, or equivalent ephemeral state must not be the sole authoritative basis for required Engineering continuity.

### CP-R07 — Provenance Fidelity

The realization must preserve materially significant provenance concerning origin, attribution, derivation, basis, and lineage where required by the applicable Engineering semantics.

Provenance representation must preserve materially significant differences between provenance relationship types.

### CP-R08 — Attribution Fidelity

Where attribution is materially significant, the realization must distinguish the applicable roles of participants, mechanisms, Engineering Systems, authoritative sources, and execution instances.

Materially different roles such as proposing, producing, reviewing, validating, authorizing, establishing, recording, or persisting state must not be silently collapsed into undifferentiated authorship.

### CP-R09 — Derivation Provenance

Where materially significant Engineering state is derived from other Engineering state, the realization must preserve sufficient derivation provenance to explain its materially significant basis.

Derived state must remain distinguishable from its authoritative source state where that distinction is materially significant.

### CP-R10 — Provenance Non-Transitivity

The realization must not assume that authority, applicability, normative force, currency, or other materially significant Engineering semantics transfer transitively through provenance relationships.

Any semantic propagation through provenance must be established by the applicable Engineering semantics.

### CP-R11 — Provenance Completeness

The realization must preserve materially complete provenance for the applicable Engineering concern.

Material completeness does not require preservation of every technical operation, intermediate representation, or participant interaction.

Where materially required provenance is missing, the limitation must remain explicit.

### CP-R12 — Historical State Distinction

The realization must preserve historical Engineering state as distinguishable from sufficiently current Engineering state.

Historical availability must not independently establish current authority or applicability.

### CP-R13 — Historical Authority Fidelity

Where historically authoritative state is materially significant, the realization must preserve its historical authoritative status.

Later correction, supersession, revocation, re-evaluation, or replacement must not retrospectively represent such state as though it had never been authoritative.

### CP-R14 — Historical Non-Authority Fidelity

State that was proposed, observed, rejected, inferred, attempted, derived, or otherwise historically present without being authoritative must not be represented as historically authoritative merely because it is retained in Engineering History.

### CP-R15 — Historical Change

Where materially significant Engineering state changes, the realization must preserve sufficient information to distinguish the prior state, resulting state, and materially significant change relationship.

The realization need not preserve every implementation-level mutation through which the Engineering change occurred.

### CP-R16 — Supersession

Where Engineering state supersedes prior state, the realization must preserve the materially significant supersession relationship.

Supersession must not independently imply that the superseded state was incorrect.

### CP-R17 — Temporal Fidelity

The realization must preserve materially significant temporal semantics where required by the applicable Engineering concern.

Materially different temporal meanings such as occurrence, production, observation, recording, authority, applicability, cessation, or determination time must not be silently collapsed where the distinction affects Engineering meaning.

### CP-R18 — Change Ordering

Where relative ordering of materially significant Engineering changes affects Engineering meaning, the realization must preserve sufficient authoritative ordering information.

The realization must not require or manufacture a universal total ordering where the applicable Engineering semantics do not establish one.

### CP-R19 — Concurrent and Independent Change

The realization must support materially significant Engineering changes for which no authoritative ordering relationship exists.

Technical recording order must not independently be represented as semantic Engineering ordering.

### CP-R20 — Current Authoritative State

The realization must support determination of sufficiently current authoritative Engineering state from the applicable authoritative Engineering mechanisms and durable Engineering state according to the applicable Engineering semantics.

The most recently recorded historical state must not independently be treated as current authoritative state.

### CP-R21 — Temporal Reconstruction

Where required by the applicable Engineering semantics, the realization must support reconstruction of materially significant Engineering state as of an earlier Engineering condition or time.

Historical reconstruction must preserve the distinction between what was authoritative, what was known or recorded, and what was discovered or corrected later.

### CP-R22 — Temporal Uncertainty

Where materially significant temporal information is missing, ambiguous, conflicting, or insufficient to establish authoritative ordering or historical interpretation, the realization must preserve that limitation.

It must not manufacture temporal precision or ordering merely to produce a complete representation.

### CP-R23 — Reconstruction

The realization must support reconstruction of sufficiently current and materially complete Engineering state and meaning required for applicable Engineering activity from authoritative sources and durable Engineering state.

Reconstruction must not independently establish new authoritative Engineering state.

### CP-R24 — Reconstruction Materiality

Reconstruction completeness must be evaluated according to the materially significant Engineering state required for the applicable activity.

The realization must not require reconstruction of every historical interaction, transient participant state, implementation event, or reasoning step where those are not materially required.

### CP-R25 — Reconstruction and Inference

Inference may assist reconstruction, but the realization must not silently manufacture missing authoritative or historical Engineering state.

Where materially significant reconstructed meaning depends upon inference rather than authoritatively or durably established state, that distinction must remain explicit.

### CP-R26 — Reconstruction Failure

Where required Engineering state or provenance is unavailable, corrupted, ambiguous, conflicting, or otherwise insufficient for reliable reconstruction, the realization must preserve that limitation.

A guessed or materially incomplete reconstruction must not be represented as reliably preserved Engineering continuity.

### CP-R27 — Resumption

The realization must support continuation of Engineering activity after applicable discontinuity from sufficiently current authoritative sources and durable Engineering state according to the applicable Engineering semantics.

Resumption must not require reproduction of prior participant memory, conversational context, hidden reasoning, or ephemeral execution state.

### CP-R28 — Resumption After Material Change

Where authoritative Engineering state materially changes during interruption, the realization must support resolution of the sufficiently current state and materially significant changes required for resumption.

The prior working position must not independently establish the valid current resumption position.

### CP-R29 — Handover Continuity

The realization must support materially sufficient Engineering continuity across participant handover where required by the applicable Engineering semantics.

Handover continuity must not depend upon the outgoing participant remaining available to explain undocumented materially significant Engineering state.

### CP-R30 — Handover Authority Boundary

Handover of Engineering information, artifacts, context, evidence, or working state must not independently transfer participation, responsibility, or authority.

Such changes must remain governed by their applicable authoritative mechanisms.

### CP-R31 — AI Execution-Instance Continuity

Where Engineering continuity is required for an AI Engineer, the realization must support resumption across execution-instance replacement from authoritative and durable Engineering state.

A predecessor execution instance must not be required to remain available.

### CP-R32 — Execution-Instance Independence

Creation, replacement, restart, or termination of an AI execution instance must not independently create, transfer, revoke, or otherwise change Engineering identity, responsibility, authority, determinations, Validation Determinations, or other authoritative Engineering semantics.

### CP-R33 — AI Ephemeral-State Boundary

AI model context, conversational memory, hidden reasoning, transient plans, cached inference, and local runtime state must not independently be treated as authoritative Engineering state or durable Engineering history.

Where materially significant Engineering state emerges through AI participation, that state must be established or preserved through the applicable Engineering mechanism.

### CP-R34 — Provenance Inspection

The realization must support inspection of materially significant provenance required for applicable Engineering understanding, investigation, reconstruction, or explanation.

Inspection must preserve materially significant distinctions in authority, historical status, temporal meaning, and relationship semantics.

### CP-R35 — Provenance Explanation

The realization must support materially sufficient explanation of Engineering state through available provenance.

Generated or derived explanations must remain distinguishable from their authoritative Engineering basis and must preserve materially significant uncertainty, missing provenance, and conflicting state.

### CP-R36 — AI-Assisted Provenance

AI-assisted provenance traversal, summarization, organization, or explanation must not silently invent missing provenance, causal relationships, authority, temporal ordering, or Engineering meaning.

Materially significant inference beyond authoritative or durable provenance must remain distinguishable as inference.

### CP-R37 — Provenance Challenge

The realization must provide a means for an Engineer to challenge materially significant provenance believed to be incorrect, incomplete, ambiguous, misleading, or inconsistent with authoritative Engineering state.

Challenge must not itself modify the challenged provenance or underlying authoritative state.

### CP-R38 — Integrity

The realization must preserve the materially significant identity, meaning, relationships, history, attribution, and temporal semantics of durable Engineering state.

Integrity must not depend upon treating every historical representation as immutable.

### CP-R39 — Correction

The realization must support correction of materially incorrect durable Engineering state, history, or provenance through the applicable authoritative or provenance mechanism.

Correction must preserve sufficient history and provenance to distinguish the defect, correction, resulting representation or state, and materially significant attribution and temporal relationships.

### CP-R40 — Authoritative-State Correction Boundary

Where a defect concerns authoritative Engineering state, correction must occur through the authoritative mechanism owning that state.

Continuity & Provenance must not replace authoritative Engineering state merely because it identifies or records a defect.

### CP-R41 — Historical and Provenance Representation Correction

Where authoritative Engineering state was correctly established but its historical or provenance representation is defective, the realization must support correction of that representation without falsely representing the correction as a change to the underlying authoritative Engineering state.

### CP-R42 — Correction Provenance

Materially significant corrections must themselves preserve sufficient provenance to explain their basis, attribution, affected state, and temporal relationships.

### CP-R43 — Affected-Scope Identification

Where a continuity, integrity, historical, or provenance defect is discovered, the realization must support identification of potentially affected Engineering state, history, provenance, reconstruction, and relying Engineering activity.

Authoritatively resolvable impact must remain distinguishable from inferentially identified potential impact.

### CP-R44 — Retention

The realization must retain materially significant Engineering state, history, and provenance for as long as required by the applicable Engineering semantics.

It must not require indefinite retention of all Engineering state unless such retention is established by those semantics.

### CP-R45 — Availability

Retained Engineering state must remain sufficiently available for the Engineering activities requiring it.

Retention without materially sufficient availability must not be treated as satisfying Engineering continuity.

### CP-R46 — Loss

Where required Engineering state, history, or provenance is lost, corrupted, inaccessible, incomplete, or otherwise unusable, the realization must preserve the resulting continuity or provenance limitation.

It must not manufacture replacement authoritative or historical state to conceal the loss.

### CP-R47 — Partial Loss

Where only part of required Engineering state remains available, the realization must not represent the remaining state as materially complete where the missing state affects continuity, provenance, reconstruction, explanation, or another applicable Engineering concern.

### CP-R48 — External Authoritative State

The realization must support continuity where authoritative Engineering state remains durably owned by an external Engineering System or authoritative source without requiring unnecessary duplication of that state.

It must preserve or support resolution of sufficient identity, provenance, relationships, temporal semantics, and availability for the applicable Engineering continuity requirements.

### CP-R49 — Human and AI Continuity Semantics

The realization must apply common Engineering continuity, history, provenance, attribution, and integrity semantics to Human Engineers and AI Engineers for equivalent Engineering concerns.

Participant type alone must not alter the authority, historical status, derivation, currency, supersession, correction, or material significance of Engineering state.

### CP-R50 — Participant-Specific Representation

The realization may represent continuity and provenance differently for Human Engineers and AI Engineers.

Participant-specific representation must not alter materially significant Engineering meaning, authority, provenance, historical status, uncertainty, or temporal semantics.

### CP-R51 — Participant Replacement

Replacement of a Human Engineer or AI Engineer must not independently change authoritative Engineering state, participation, responsibility, or authority.

Replacement of an AI execution instance must not independently change authoritative Engineering state or the identity, participation, responsibility, or authority of the AI Engineer associated with that execution instance.

The realization must preserve sufficient durable Engineering state and provenance for the succeeding participant or execution instance to resolve the applicable current Engineering position.

### CP-R52 — Capability Ownership

Where continuity or provenance depends upon Engineering state owned by another Engineering Platform capability, Engineering System, authoritative source, or governed mechanism, the realization must preserve the materially significant state and relationships required for continuity without transferring authoritative ownership.

---

## 18. Invariants

The following invariants must hold for every conforming realization of Continuity & Provenance.

1. **Durability does not create authority.**  
   Engineering state does not become authoritative, correct, applicable, current, normative, permitted, or validated merely because it is persisted, retained, replicated, indexed, or available.

2. **Historical state is not current state.**  
   Historical availability does not independently establish current authority or applicability.

3. **Historical inclusion does not imply historical authority.**  
   A proposal, observation, rejected state, inferred state, failed attempt, derived state, or other retained Engineering state must not be represented as historically authoritative merely because it forms part of Engineering History.

4. **Provenance does not create truth.**  
   The existence of provenance does not independently establish that the Engineering state it describes is correct, current, applicable, or authoritative.

5. **Provenance relationships retain their semantics.**  
   Materially different relationships such as proposed by, established by, validated by, derived from, supported by, or persisted by must not be silently treated as equivalent.

6. **Provenance is not semantically transitive by default.**  
   Authority, applicability, normative force, currency, and other Engineering semantics do not automatically propagate through provenance chains.

7. **Attribution is role-sensitive.**  
   Performing, proposing, producing, reviewing, validating, authorizing, establishing, recording, and persisting Engineering state are not interchangeable forms of authorship.

8. **Derived state remains derived.**  
   Persistence, explanation, or repeated use of derived Engineering state does not make it authoritative over its source state.

9. **Technical mutation is not inherently Engineering change.**  
   An implementation event, state mutation, or storage operation does not independently establish a materially significant Engineering change.

10. **Recording order is not semantic order.**  
    One Engineering change being recorded before another does not independently establish an authoritative Engineering ordering relationship.

11. **Recency is not authority.**  
    The most recently recorded Engineering state is not necessarily the current authoritative Engineering state.

12. **Historical reconstruction does not rewrite knowledge backward.**  
    State discovered or corrected later must not be silently represented as though it had been known, recorded, or authoritative at an earlier reconstructed point.

13. **Temporal uncertainty remains uncertainty.**  
    Missing, ambiguous, conflicting, or insufficient temporal information must not be silently converted into precise ordering or historical meaning.

14. **Reconstruction does not create Engineering truth.**  
    A reconstructed representation does not independently establish new authoritative Engineering state.

15. **Inference does not replace missing state.**  
    Inference may assist reconstruction or explanation but must not be presented as preserved authoritative or historical Engineering state where such state is missing.

16. **Material incompleteness remains visible.**  
    A reconstruction, provenance representation, or retained state set must not be represented as materially complete where required Engineering state is unavailable or unusable.

17. **Resumption is based on current Engineering state, not prior working position.**  
    A participant or execution instance having previously reached a working position does not independently establish that the same position remains valid after discontinuity.

18. **Handover does not transfer responsibility or authority.**  
    Transfer of Engineering information, artifacts, context, evidence, or working state does not independently transfer participation, responsibility, or authority.

19. **Participant memory is not Engineering continuity.**  
    Human memory, AI memory, conversational context, hidden reasoning, or other ephemeral participant state must not be the sole authoritative basis for materially significant Engineering continuity.

20. **Execution-instance replacement is not Engineering-state change.**  
    Creation, restart, replacement, or termination of an AI execution instance does not independently change AI Engineer identity, responsibility, authority, determinations, Validation Determinations, or other authoritative Engineering state.

21. **AI internal state is not authoritative Engineering state.**  
    Model context, hidden reasoning, transient plans, cached inference, and local runtime state do not independently establish authoritative Engineering state or durable Engineering history.

22. **Explanation is not authority.**  
    A provenance explanation, including an AI-generated explanation, does not become an independent source of Engineering truth.

23. **Integrity does not require absolute immutability.**  
    Historical or provenance representations may be corrected where necessary, provided materially significant Engineering history and correction provenance remain truthful and distinguishable.

24. **Correction does not rewrite history into fiction.**  
    Correcting Engineering state or its historical representation must not silently make the corrected state appear to have always existed, applied, or been authoritative.

25. **Correction of representation is distinct from correction of Engineering state.**  
    Repairing defective history or provenance does not independently establish a change to correctly established authoritative Engineering state.

26. **Supersession does not imply error.**  
    State may cease to be current or applicable without having been incorrect when it was authoritative or applicable.

27. **Loss does not authorize invention.**  
    Missing, corrupted, inaccessible, or otherwise unusable Engineering state or provenance must not be replaced by manufactured historical or authoritative state.

28. **Retention is not completeness.**  
    The existence of retained Engineering state does not establish that all materially required Engineering state or provenance remains available.

29. **External ownership does not defeat continuity.**  
    Continuity does not require Continuity & Provenance to physically duplicate authoritative Engineering state that remains durably and sufficiently available from its authoritative source.

30. **Participant type does not change Engineering truth.**  
    Human and AI Engineers may use different continuity representations or interaction mechanisms, but participant type alone does not alter authoritative Engineering meaning, history, provenance, or temporal semantics.

31. **Participant replacement does not transfer Engineering semantics.**  
    Replacing a Human Engineer, AI Engineer, or AI execution instance does not independently create, revoke, transfer, or modify authoritative Engineering state, responsibility, or authority.

32. **Capability composition does not transfer ownership.**  
    Continuity & Provenance may preserve, relate, reconstruct, or explain Engineering state owned elsewhere, but authoritative ownership remains with the capability, Engineering System, authoritative source, or governed mechanism that establishes it.
