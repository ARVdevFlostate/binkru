# Context Resolution & Composition Specification

## 1. Purpose

Context Resolution & Composition determines what authoritative Engineering context applies to a participant's current Engineering activity and composes an effective, traceable, and appropriately scoped projection of that context.

The capability enables an Engineer to receive the Engineering context necessary for safe and correct participation without requiring the participant to independently discover, assemble, interpret, or maintain all applicable Engineering state.

Context Resolution & Composition does not create a competing source of Engineering truth.

Authoritative Engineering sources remain authoritative.

---

## 2. Scope

This specification defines the required semantics and realization requirements for the Context Resolution & Composition capability of the Engineering Platform.

Context Resolution & Composition includes:

- resolution of authoritative Engineering context applicable to a participant's Engineering activity;
- determination of context applicability through authoritative Engineering relationships and state;
- composition of Effective Engineering Context;
- activity-specific context;
- context relevance and material completeness;
- layered Engineering context;
- participant-appropriate context projection;
- preservation of normative semantics;
- context provenance and reproducibility;
- context currency and material-change awareness;
- context challenge and affected-scope resolution;
- resumption context;
- independent-review context.

Context Resolution & Composition does not independently:

- create or modify authoritative Engineering source state;
- establish participant identity;
- establish project participation or governed-work responsibility;
- establish Engineering relationships owned by another capability or Engineering System;
- determine governed permissibility;
- determine validation outcomes;
- replace Discovery & Navigation for exploratory Engineering discovery;
- manufacture authoritative Engineering context where applicable authoritative state is missing or ambiguous.

Where context resolution depends upon state or determinations owned elsewhere, Context Resolution & Composition composes with the applicable Engineering Platform capability, Engineering System, authoritative source, or governed mechanism.

---

## 3. Context Model

### 3.1 Resolution and Composition

Context Resolution and Context Composition are distinct operations.

**Context Resolution** determines what authoritative Engineering context applies to a participant's current Engineering activity.

**Context Composition** determines how that applicable context is represented as Effective Engineering Context for the participant and Engineering activity.

Composition must operate upon resolved context without independently changing authoritative applicability.

### 3.2 Authoritative Context

Authoritative Engineering context originates from authoritative Engineering state and relationships.

Context Resolution & Composition does not become authoritative for source Engineering state merely because that state is resolved or included in Effective Engineering Context.

Where authoritative source state changes, the source remains authoritative over any previously composed context representation.

### 3.3 Effective Engineering Context

Effective Engineering Context is the derived, activity-specific projection of authoritative Engineering context resolved as applicable to a participant's current Engineering activity.

Effective Engineering Context may organize, structure, summarize, prioritize, or otherwise project applicable Engineering context for effective participation.

Effective Engineering Context is not an independent source of Engineering truth.

It must remain sufficiently attributable to the authoritative Engineering sources and relationships from which it is derived.

### 3.4 Context Applicability

Context applicability describes whether authoritative Engineering context applies to a participant's current Engineering activity.

Applicability must be resolved from authoritative Engineering state and relationships wherever those relationships permit deterministic resolution.

Discoverability, visibility, semantic similarity, textual proximity, repository proximity, participant memory, conversational context, or AI inference must not independently establish authoritative contextual applicability.

### 3.5 Context Relevance

Context may be treated conceptually as:

- required;
- relevant;
- discoverable.

**Required context** is context that must be resolved where necessary for safe and correct Engineering participation.

**Relevant context** is context that may materially assist the Engineering activity without necessarily being required for participation.

**Discoverable context** is visible Engineering context that may be navigated or considered as Engineering needs emerge but is not thereby established as applicable.

These conceptual treatments must not be interpreted as independently establishing authoritative contextual applicability.

### 3.6 Material Completeness

Context completeness means material completeness rather than maximal information volume.

Effective Engineering Context must include the required context necessary for the applicable Engineering activity.

Completeness does not require inclusion of every discoverable Engineering artifact, relationship, historical state, or potentially relevant item.

The omission of non-required information does not make Effective Engineering Context incomplete solely because that information is discoverable.

### 3.7 Activity and Participant Basis

Effective Engineering Context is specific to the Engineering activity and applicable participant state, including participant responsibility where such responsibility exists.

The same governed work may therefore produce different Effective Engineering Context for different Engineering activities or participant responsibilities.

Context Resolution & Composition must not assume that one context projection is universally applicable to every participant or activity involving the same governed work.

### 3.8 Context and Engineering Truth

Resolution and composition must preserve materially significant distinctions in authoritative Engineering state.

Effective Engineering Context must not convert:

- inference into authority;
- discoverability into applicability;
- historical applicability into current applicability;
- recommendation into requirement;
- permitted discretion into obligation;
- unresolved ambiguity into resolved Engineering truth;
- absence of prohibition into affirmative permission.

Where authoritative Engineering context is missing, conflicting, ambiguous, or unresolved, that condition must remain materially visible in Effective Engineering Context where it affects the Engineering activity.

---

## 4. Context Resolution

### 4.1 Purpose

Context Resolution determines what authoritative Engineering context applies to a participant's current Engineering activity.

Resolution operates over authoritative Engineering state and relationships.

It does not create authoritative Engineering context merely because information is discoverable, relevant, semantically related, or available to the participant.

### 4.2 Resolution Basis

Context Resolution must use authoritative Engineering relationships wherever those relationships permit deterministic applicability resolution.

The resolution basis may include relationships to:

- governed work;
- Execution Baselines;
- upstream intent;
- project context;
- Technology Profiles;
- Development Standards;
- architecture decisions;
- dependencies;
- related governed work;
- validation expectations;
- evidence;
- findings;
- current Engineering conditions;
- applicable participant state.

The presence of an authoritative relationship does not automatically mean every state reachable through that relationship is applicable.

Applicability must follow the semantics established by the authoritative Engineering model.

### 4.3 Deterministic Resolution

Mandatory context applicability must be deterministically resolvable wherever authoritative Engineering relationships permit it.

A realization must not substitute semantic inference for deterministic authoritative resolution merely because inference is easier, faster, or more convenient.

Where deterministic resolution cannot establish applicability, the unresolved condition must remain distinguishable from authoritative applicability.

### 4.4 Assisted Resolution

Semantic, AI-assisted, textual, structural, or other inferential mechanisms may assist discovery of potentially applicable or relevant Engineering context.

Such mechanisms may identify candidate context, relationships, ambiguities, or resolution paths.

They must not independently establish authoritative contextual applicability.

Candidate context identified through assisted resolution must remain distinguishable from context whose applicability has been authoritatively resolved.

### 4.5 Resolution Inputs

Context Resolution may depend upon authoritative state owned by multiple Engineering Platform capabilities, Engineering Systems, authoritative sources, or governed mechanisms.

Resolution must preserve the authority and semantics of those inputs.

The capability must not reinterpret an input merely to make context resolution possible where the authoritative Engineering model does not establish the required semantic relationship.

### 4.6 Resolution Result

A resolution result must preserve sufficient information to determine:

- the Engineering activity for which context was resolved;
- the participant basis relevant to that activity;
- the authoritative context established as applicable;
- the authoritative relationships or state establishing material applicability;
- materially unresolved, ambiguous, or missing context conditions.

A resolution result is derived state.

It does not become authoritative over the source state or relationships from which applicability was determined.

---

## 5. Context Applicability

### 5.1 Applicability Semantics

Context applicability is specific to the participant's Engineering activity and applicable participant state, including participant responsibility where such responsibility exists.

Engineering state may be authoritative without being applicable to a particular Engineering activity.

Engineering state may also be visible, discoverable, or relevant without being authoritatively applicable.

### 5.2 Direct and Transitive Applicability

Applicable context may be established directly or through authoritative relationship traversal where the Engineering model establishes transitive applicability semantics.

The existence of a relationship chain alone does not establish transitive applicability.

Context Resolution must not infer that all Engineering state transitively reachable from governed work, project state, a decision, dependency, standard, or other Engineering entity applies to the current activity.

### 5.3 Conditional Applicability

Applicability may depend upon authoritative Engineering conditions.

Where applicability is conditional, Context Resolution must resolve or consume the applicable authoritative condition or determination through the mechanism that owns it rather than treat the related context as unconditionally applicable.

Where the condition cannot be sufficiently resolved, the resulting applicability must remain unresolved or conditional rather than being silently promoted to applicable context.

### 5.4 Applicability Changes

Context applicability may change when authoritative Engineering state, relationships, participant state, activity, or applicable Engineering conditions change.

A context item previously established as applicable must not be assumed to remain applicable solely because it was included in an earlier Effective Engineering Context.

Current applicability must be resolvable from sufficiently current authoritative Engineering state where reliance upon the context materially affects Engineering activity.

### 5.5 Missing and Ambiguous Applicability

Where authoritative Engineering state required to determine applicability is missing, conflicting, ambiguous, or unresolved, Context Resolution must preserve that condition.

It must not manufacture applicability to produce a complete-looking context projection.

An Engineer may reason about, discover, or propose resolution of the condition, but authoritative applicability must be established through the applicable Engineering state or governed mechanism.

---

## 6. Context Composition

### 6.1 Purpose

Context Composition transforms resolved applicable Engineering context into Effective Engineering Context appropriate to the participant and Engineering activity.

Composition may alter representation, organization, structure, emphasis, ordering, summarization, or delivery mechanism.

Composition must not alter authoritative applicability, Engineering meaning, normative force, or source authority.

### 6.2 Composition Basis

Composition must operate upon the result of Context Resolution and any materially relevant unresolved context conditions that must remain visible to the participant.

Composition must not independently add Engineering state as authoritatively applicable merely because the state appears useful, relevant, related, or semantically similar.

Additional visible Engineering information may remain discoverable through Discovery & Navigation without being incorporated as authoritative applicable context.

### 6.3 Material Completeness

Composition must produce Effective Engineering Context that is materially complete for the applicable Engineering activity.

Material completeness requires inclusion of required context necessary for safe and correct participation.

Composition may include additional context whose applicability has been authoritatively resolved where doing so materially assists the Engineering activity without obscuring required context or materially significant distinctions.

Maximal information volume is not a composition objective.

### 6.4 Progressive Composition

Effective Engineering Context may be progressively elaborated as Engineering needs emerge.

Progressive composition may expose additional resolved context, detail, provenance, explanation, or related Engineering state without requiring maximal context presentation at the start of an activity.

Progressive composition must not silently change authoritative applicability.

Where newly resolved authoritative state changes applicability, that change must be treated as a new or updated resolution rather than merely a presentation expansion.

### 6.5 Composition Failure

Where materially required context cannot be resolved or safely composed, the resulting condition must remain visible.

Composition must not conceal missing, conflicting, ambiguous, stale, or unresolved context merely to produce a coherent participant-facing representation.

Whether Engineering activity may proceed in the presence of such a condition is determined by the applicable Engineering model or governed mechanism rather than by Context Composition itself.

---

## 7. Context Layers

### 7.1 Layered Context Model

Effective Engineering Context may compose context from distinct Engineering layers, including:

- Engineering Environment Context;
- Project Context;
- Work and Activity Context.

Context layers organize Engineering context according to scope and stability.

They do not create separate sources of Engineering truth.

### 7.2 Engineering Environment Context

Engineering Environment Context represents applicable Engineering context whose scope extends beyond an individual project or governed-work activity.

It may include applicable Engineering principles, Platform semantics, Development Standards, operating constraints, or other environment-level Engineering state.

Environment-level context must not be included solely because it exists globally.

Its applicability must follow the authoritative Engineering model.

### 7.3 Project Context

Project Context represents applicable Engineering state specific to the project in which the Engineering activity occurs.

It may include project intent, architecture state, Technology Profiles, project decisions, project-specific Development Standards or constraints, and other authoritative project state.

Project participation or project proximity does not make every item of project state applicable to every Engineering activity.

### 7.4 Work and Activity Context

Work and Activity Context represents applicable Engineering state specific to the governed work and Engineering activity being performed.

It may include:

- upstream intent;
- Execution Baselines;
- dependencies;
- applicable decisions;
- realization constraints;
- validation expectations;
- evidence or findings;
- activity-specific participant state;
- current Engineering conditions.

Work and Activity Context may depend upon Environment and Project Context without duplicating their authoritative source state.

### 7.5 Layer Composition

Context layers may be composed into a coherent Effective Engineering Context appropriate to the Engineering activity.

Composition must preserve the scope, authority, and semantics of context originating from different layers.

Where context from different layers conflicts, overlaps, qualifies, or supersedes other context, Composition must preserve the authoritative Engineering semantics governing that relationship rather than resolve the relationship through presentation preference.

---

## 8. Activity-Specific Context

### 8.1 Activity Basis

Effective Engineering Context must be resolved and composed for the Engineering activity being performed.

Different activities involving the same governed work may require materially different context.

Applicable activities may include:

- realization preparation;
- realization;
- peer review;
- validation;
- resumption;
- other Engineering activities established by the Engineering model.

### 8.2 Realization Preparation Context

Context for realization preparation must provide the authoritative Engineering context required to understand the governed work sufficiently to prepare for realization.

Preparation context may include applicable upstream intent, Execution Baselines, architecture decisions, Technology Profiles, Development Standards, dependencies, conditions, and validation expectations.

Preparation context does not itself establish that realization may begin.

### 8.3 Realization Context

Realization context must provide the applicable Engineering context required for safe and correct realization of governed work.

Where realization context materially changes during active realization, Context Resolution & Composition must support identification and projection of the affected change according to the applicable context-currency semantics.

### 8.4 Peer Review Context

Peer-review context must be resolved for the reviewer's participation responsibility and review activity.

It must not simply inherit the realization participant's Effective Engineering Context or working interpretation.

Peer-review context must be independently reproducible from current authoritative Engineering state and the reviewer's applicable participant state.

### 8.5 Validation Context

Validation context must be resolved for the applicable validation activity and participant responsibility.

It may include validation expectations, relevant Execution Baselines, evidence, findings, applicable Development Standards, decisions, conditions, and other authoritative state required for validation.

Context Resolution & Composition does not determine the validation outcome.

### 8.6 Activity Transition

Transition from one Engineering activity to another may require context to be resolved and composed again.

A context projection created for one activity must not be assumed to remain materially complete or applicable for another activity solely because both activities concern the same governed work.

---

## 9. Normative Semantics

### 9.1 Normative Preservation

Effective Engineering Context must preserve materially significant normative distinctions present in authoritative Engineering state.

Composition must distinguish, where applicable, between:

- requirements;
- prohibitions;
- permissions;
- permitted discretion;
- recommendations or guidance;
- unresolved ambiguity;
- matters requiring authority or governed determination.

These distinctions must not be flattened into equivalent participant guidance.

### 9.2 Normative Source Authority

The normative force of Engineering context derives from its authoritative source and the applicable Engineering model.

Context Resolution & Composition does not strengthen, weaken, create, or remove normative force through inclusion, omission, summarization, ordering, emphasis, or participant projection.

### 9.3 Conflicting Normative Context

Where applicable authoritative context contains materially conflicting normative statements, Context Composition must preserve the conflict unless the authoritative Engineering model establishes how the conflict is resolved.

Composition must not resolve normative conflict through semantic similarity, source ordering, presentation priority, AI judgment, or participant preference.

Where another Engineering Platform capability or governed mechanism owns conflict resolution, that determination must remain authoritative.

### 9.4 Normative Summarization

Normative Engineering context may be summarized or transformed for participant-appropriate representation where the materially significant normative meaning is preserved.

A summary must not:

- convert a recommendation into a requirement;
- convert permitted discretion into obligation;
- convert absence of prohibition into permission;
- omit a material prohibition or condition;
- conceal unresolved ambiguity;
- present inferred interpretation as authoritative normative meaning.

Where summarization cannot preserve the materially significant normative semantics, the authoritative source or a sufficiently faithful representation must remain available to the participant.

### 9.5 Normative Provenance

Effective Engineering Context must preserve sufficient provenance for materially significant normative context to be attributable to its authoritative source.

Where multiple authoritative sources contribute to a normative determination or constraint, their contribution must remain sufficiently traceable for Engineering inspection.

---

## 10. Context Provenance & Derived State

### 10.1 Derived Context

Effective Engineering Context is derived Engineering state.

It is produced from authoritative Engineering sources, relationships, participant state, applicable determinations, and other authoritative state used during Context Resolution & Composition.

Effective Engineering Context does not become an independent source of Engineering truth merely because it is persisted, cached, presented to a participant, or used during Engineering activity.

### 10.2 Reproducibility

Effective Engineering Context must be sufficiently reproducible from the authoritative Engineering state and relationships from which it was derived.

Reproducibility does not require preservation of an identical participant-facing representation where representation mechanisms may legitimately change.

It requires sufficient derivation information to explain materially significant context applicability, source authority, and composition.

### 10.3 Provenance

Effective Engineering Context must preserve sufficient provenance to identify or navigate toward the authoritative Engineering sources and relationships contributing materially significant context.

Provenance must be sufficient to explain, where applicable:

- why context was established as applicable;
- which authoritative state contributed to the context;
- which participant and Engineering activity formed the resolution basis;
- which materially significant conditions or determinations affected applicability;
- which source establishes materially significant normative meaning.

Provenance is explanatory and traceability state.

It does not independently establish source authority or contextual applicability.

### 10.4 Derived Representations

Effective Engineering Context may be represented through summaries, structured projections, machine-consumable forms, human-readable forms, conversational representations, or other participant-appropriate mechanisms.

A derived representation must preserve materially significant Engineering meaning, applicability, normative semantics, unresolved conditions, and provenance required by this specification.

Transformation of representation must not create a new authoritative context source.

### 10.5 Persisted Effective Context

A realization may persist Effective Engineering Context or intermediate resolution and composition state where useful for continuity, performance, traceability, or other Engineering purposes.

Persistence does not make derived context authoritative over its source state.

Persisted Effective Engineering Context remains subject to context-currency semantics when authoritative Engineering state changes.

---

## 11. Context Currency & Change

### 11.1 Context Currency

The currency of Effective Engineering Context depends upon the authoritative Engineering state and relationships materially affecting its applicability or meaning.

Context currency does not require every change in the Engineering environment to invalidate existing Effective Engineering Context.

Only changes capable of materially affecting the participant's applicable Engineering context require context-impact consideration.

### 11.2 Material Change

A material context change is a change to authoritative Engineering state, relationships, participant state, conditions, or determinations that may alter:

- contextual applicability;
- required context;
- materially significant Engineering meaning;
- normative force;
- participant responsibility relevant to the activity;
- validation expectations or other activity-relevant conditions;
- material completeness of Effective Engineering Context.

A change unrelated to the participant's Engineering activity does not inherently make Effective Engineering Context stale.

### 11.3 Change Detection

Context Resolution & Composition must support identification of material authoritative changes capable of affecting active Effective Engineering Context.

The realization need not treat all Engineering changes as context changes.

Where impact cannot be determined immediately, the potentially affected context must remain distinguishable from context known to be current where that distinction materially affects Engineering activity.

### 11.4 Context Impact

When a material authoritative change is identified, Context Resolution & Composition must support determination of which active or durable Effective Engineering Context may be affected.

Affected context may require applicability to be resolved again, composition to be updated, or the participant to be made aware of the material change.

Context impact does not itself determine whether the underlying Engineering activity may continue.

That determination remains with the applicable Engineering model or governed mechanism.

### 11.5 Relevant-State Awareness

Where a material change affects active Engineering context, the affected participant may need to be made aware of the change.

Notifications, alerts, messages, or equivalent awareness mechanisms communicate context change.

They do not become authoritative Engineering state merely because they inform the participant of that change.

The authoritative source state and resulting current applicability remain authoritative.

### 11.6 Stale Context

Effective Engineering Context is stale where material authoritative changes have caused its applicability, meaning, or material completeness to no longer reflect sufficiently current Engineering state.

Stale context must not be represented as current where reliance upon it may materially affect Engineering activity.

A stale context representation may remain available for historical or provenance purposes where it is clearly distinguishable from current Effective Engineering Context.

---

## 12. Context Challenge & Affected Scope

### 12.1 Context Challenge

An Engineer must be able to challenge Effective Engineering Context believed to be incorrect, incomplete, ambiguous, or stale.

A Context Challenge may concern:

- incorrect authoritative source state;
- missing authoritative source state;
- incorrect applicability resolution;
- missing applicable context;
- composition defects;
- provenance defects;
- stale context;
- unresolved or incorrectly represented ambiguity.

A challenge does not itself modify authoritative Engineering state or Effective Engineering Context.

### 12.2 Challenge Classification

Context Resolution & Composition must support distinguishing, sufficiently for resolution, between defects originating in:

- authoritative Engineering source state;
- authoritative Engineering relationships;
- participant state or another capability-owned input;
- applicability-resolution logic or mechanism;
- composition logic or representation;
- context currency or change detection;
- provenance or traceability.

The capability need not own correction of every identified defect.

The defect must be routed or exposed to the mechanism that owns the affected authoritative state or Platform behavior.

### 12.3 Correction

Corrections must occur at the appropriate authoritative source, Engineering Platform capability, governed mechanism, resolution mechanism, or composition mechanism.

Derived Effective Engineering Context must not be manually altered as a substitute for correcting the authoritative state or derivation mechanism responsible for the defect.

After correction, affected context must be capable of being resolved and composed again from the applicable authoritative Engineering state using the corrected source state or Platform mechanism.

### 12.4 Affected-Scope Resolution

Where a context-resolution, composition, provenance, or currency defect is discovered, Context Resolution & Composition must support identification of potentially affected Engineering work, activities, participants, or Effective Engineering Context.

Affected-scope identification must be based upon authoritative relationships and derivation information wherever those relationships permit deterministic impact resolution.

Inferential mechanisms may assist identification of additional potentially affected scope but must not silently present inferred impact as authoritative impact.

### 12.5 Response to Affected Scope

Identification of affected scope does not independently determine the required Engineering response.

The applicable Engineering model, governance capability, or governed mechanism determines whether affected Engineering activity must stop, resume with updated context, be reviewed again, be revalidated, or undergo another governed response.

Context Resolution & Composition provides the applicable context-impact information without assuming ownership of that determination.

---

## 13. Resumption Context

### 13.1 Purpose

Resumption Context enables Effective Engineering Context to be reconstructed when Engineering activity resumes after interruption, handover, participant transfer, or execution-instance replacement.

Resumption must not depend upon participant memory, previous conversational context, or ephemeral execution state as authoritative context.

### 13.2 Resumption Basis

Resumption Context must be resolved from sufficiently current authoritative and durable Engineering state applicable to the resumed Engineering activity.

Where relevant, the resolution basis may include:

- current governed-work state;
- current participant state;
- applicable Execution Baselines;
- current authoritative decisions and standards;
- dependencies;
- validation expectations;
- evidence and findings;
- durable Engineering history;
- material changes since previous Engineering activity;
- other currently applicable Engineering conditions.

Previously composed Effective Engineering Context may assist continuity but must not substitute for current authoritative resolution where material state may have changed.

### 13.3 Material Changes Since Previous Activity

Where Engineering state has materially changed since the participant's previous activity, Resumption Context must support identification and projection of those changes where they affect the resumed activity.

The participant need not be presented with every Engineering change that occurred during the interruption.

Materiality remains specific to the resumed Engineering activity and participant responsibility.

### 13.4 Participant Transfer

Where Engineering activity resumes under a different responsible participant, context must be resolved for the succeeding participant's current authoritative participation state and Engineering activity.

The succeeding participant must not simply inherit the prior participant's Effective Engineering Context, working interpretation, conversational history, or participant-specific projection.

Durable Engineering state produced by prior activity may remain applicable where established by current authoritative resolution.

### 13.5 AI Execution-Instance Replacement

Where an AI execution instance is replaced while the authoritative AI Engineer identity and responsibility remain unchanged, the succeeding execution instance must reconstruct Effective Engineering Context from current authoritative and durable Engineering state.

Prior conversational context or model memory may assist interaction where available but must not be treated as authoritative Resumption Context.

Execution-instance replacement must not itself change contextual applicability.

---

## 14. Independent Review Context

### 14.1 Independent Resolution

Context for an independent Engineering review must be resolved from current authoritative Engineering state and the reviewer's applicable participant responsibility.

It must not be derived merely by copying or inheriting the realization participant's Effective Engineering Context.

### 14.2 Independence of Interpretation

The realization participant's working interpretation, reasoning, conversational history, summaries, or participant-specific context projection must not become authoritative review context merely because they were used during realization.

Where such state is itself authoritative Engineering evidence or durable Engineering state under the Engineering model, it may be resolved for review according to its authoritative semantics.

### 14.3 Shared Authoritative Context

Independent context resolution does not require reviewers and realization participants to receive entirely different Engineering information.

Where the same authoritative context applies to both activities, it may legitimately appear in both Effective Engineering Context projections.

Independence requires separate resolution from authoritative state and participant responsibility, not artificial information divergence.

### 14.4 Review-Specific Context

Review context may include authoritative Engineering state specifically relevant to the review activity, including:

- applicable review expectations;
- Execution Baselines;
- upstream intent;
- Development Standards;
- architecture decisions;
- evidence;
- findings;
- dependencies;
- relevant governed-work state;
- other review-relevant Engineering conditions.

The applicable Engineering model determines what review context is required.

### 14.5 Review Context Currency

Independent review context must reflect sufficiently current authoritative Engineering state for the review activity.

A review must not rely upon a realization-time context snapshot as current merely because that snapshot was valid when realization occurred.

Context Resolution & Composition does not determine the review outcome or whether a review must be repeated after material context change.

---

## 15. Human and AI Engineer Projection

### 15.1 Common Context Semantics

Human Engineers and AI Engineers must receive Effective Engineering Context derived from the same authoritative Engineering semantics for their applicable participant state and Engineering activity, including participant responsibility where such responsibility exists, within applicable visibility and operating constraints.

Participant type must not create separate meanings for contextual applicability, source authority, normative force, material completeness, provenance, or context currency.

### 15.2 Participant-Appropriate Projection

Effective Engineering Context may be projected differently for Human Engineers and AI Engineers.

Participant-specific projection may alter:

- representation;
- structure;
- ordering;
- emphasis;
- level of summarization;
- interaction mechanism;
- delivery mechanism;
- machine-readable or human-readable form.

Such differences must not alter authoritative Engineering meaning, applicability, normative force, unresolved conditions, or source authority.

### 15.3 Human Engineer Projection

Human Engineer context may use representations optimized for human comprehension, navigation, progressive disclosure, explanation, or Engineering decision-making.

Human-readable simplification must not remove materially significant Engineering semantics merely to improve readability.

Authoritative sources and provenance must remain sufficiently available where required for Engineering inspection.

### 15.4 AI Engineer Projection

AI Engineer context may use structured, machine-consumable, compressed, prioritized, or otherwise execution-appropriate representations.

AI-oriented projection must preserve materially significant Engineering semantics and must not rely upon model inference to reconstruct authoritative meaning omitted from the projection.

Where context is required for safe and correct AI Engineering participation, the authoritative meaning necessary for that participation must be explicitly represented or reliably resolvable from the projection and its provenance.

### 15.5 Conversational Context

Conversational context may assist Human or AI interaction with Effective Engineering Context.

Conversation does not become an authoritative Engineering context source merely because it contains prior Engineering information, interpretations, decisions, or summaries.

Where conversational information materially affects Engineering truth, applicability, participation, governance, or another authoritative Engineering concern, that information must be established through the applicable authoritative Engineering mechanism before being relied upon as such.

### 15.6 Projection Equivalence

Different participant projections of the same resolved applicable Engineering context need not be textually, structurally, or representationally identical.

They must remain materially equivalent with respect to the authoritative Engineering semantics necessary for the applicable participant and Engineering activity.

Projection equivalence concerns preservation of Engineering meaning rather than identical presentation.

---

## 16. Capability Integrations

### 16.1 Discovery & Navigation

Context Resolution & Composition may use Discovery & Navigation to locate, traverse, and inspect visible Engineering identities, state, relationships, authoritative sources, and durable history relevant to context resolution.

Discovery & Navigation does not establish contextual applicability.

Information being visible, discoverable, navigable, semantically relevant, or related does not independently make that information applicable Engineering context.

Where Effective Engineering Context exposes provenance or additional discoverable Engineering state, Discovery & Navigation may provide navigation toward the applicable authoritative sources and relationships.

### 16.2 Participation & Scope

Context Resolution & Composition consumes authoritative participant-relative state from Participation & Scope where contextual applicability depends upon the participant's relationship to the project, governed work, or Engineering activity.

Such state may include:

- project participation;
- governed-work responsibility;
- activity-specific participation scope;
- other participant relationships relevant to context resolution.

Participation & Scope establishes the participant relationships it owns.

Context Resolution & Composition determines how those relationships affect contextual applicability for the current Engineering activity.

### 16.3 Governance & Validation Integration

Context Resolution & Composition may consume authoritative governed determinations, validation expectations, evidence, findings, conditions, and other governed state where they affect contextual applicability or Effective Engineering Context.

Governance & Validation Integration or the applicable governed mechanism remains responsible for the governed and validation determinations it owns.

Context Resolution & Composition does not independently determine whether an Engineering action may proceed, whether a governed transition is permitted, or whether validation has succeeded.

Where a governed determination materially changes applicable context, Context Resolution & Composition must be capable of resolving and composing the resulting current context.

### 16.4 Continuity & Provenance

Context Resolution & Composition consumes durable Engineering history and provenance from Continuity & Provenance where required for context resolution, resumption, change analysis, affected-scope resolution, or explanation.

Context Resolution & Composition may contribute derivation and context-provenance information required to explain how Effective Engineering Context was produced.

Continuity & Provenance remains responsible for the durable Engineering history and provenance it owns.

Persisted Effective Engineering Context does not replace authoritative source state or durable Engineering provenance.

### 16.5 Execution Enablement

Context Resolution & Composition provides Effective Engineering Context and other applicable resolved context required by Execution Enablement for Engineering execution.

Execution Enablement may transform applicable resolved context into participant-specific execution projections or AI Execution Composition according to its capability semantics.

Such execution-specific transformation must preserve materially significant Engineering meaning, authority, applicability, normative force, uncertainty, and provenance.

Execution Enablement does not independently determine contextual applicability, and an execution-specific representation does not become an independent source of authoritative Engineering context.

Where materially significant Engineering state changes during execution, Execution Enablement may require sufficiently current context to be resolved or composed again according to the applicable Engineering semantics.

### 16.6 Engineering Systems

Context Resolution & Composition may resolve applicable context from authoritative Engineering state owned by multiple Engineering Systems.

Engineering Systems retain ownership of the Engineering semantics and authoritative state they establish.

Context Resolution & Composition must preserve that authority when resolving and composing context across System boundaries.

### 16.7 Cross-Capability Composition

Context Resolution & Composition may compose with multiple Engineering Platform capabilities, Engineering Systems, authoritative sources, and governed mechanisms where contextual applicability depends upon state or determinations owned across those boundaries.

Such composition does not transfer authoritative ownership.

The capability must preserve the authority, semantics, provenance, and materially significant unresolved conditions of state or determinations obtained from other sources.

---

## 17. Capability Boundaries

Context Resolution & Composition is responsible for determining authoritative contextual applicability and composing Effective Engineering Context for a participant's Engineering activity.

Context Resolution & Composition does not independently:

- create or modify authoritative Engineering source state;
- establish authoritative participant identity;
- establish project participation or governed-work responsibility;
- establish authoritative Engineering relationships owned elsewhere;
- establish access or visibility policy;
- replace Discovery & Navigation for exploratory Engineering discovery;
- treat visibility, discoverability, semantic relevance, textual proximity, repository proximity, participant memory, conversational context, or AI inference as authoritative contextual applicability;
- determine governed permissibility;
- determine validation outcomes;
- resolve normative conflict unless the authoritative Engineering model establishes that resolution within this capability;
- manufacture authoritative context where source state or applicability is missing, conflicting, ambiguous, or unresolved;
- manually modify derived Effective Engineering Context as a substitute for correcting authoritative source state or derivation mechanisms;
- treat persisted, cached, historical, conversational, or previously composed context as currently applicable solely because it was previously valid;
- treat participant-specific projection as a separate source of Engineering truth;
- use participant memory, model memory, or conversational continuity as authoritative Resumption Context.

Where contextual applicability depends upon state or a determination owned elsewhere, Context Resolution & Composition must consume or resolve that state through the applicable authoritative capability, Engineering System, source, or governed mechanism while preserving its ownership.

---

## 18. Realization Requirements

A realization of Context Resolution & Composition must satisfy the following requirements.

### CRC-R01 — Activity-Specific Resolution

The realization must resolve authoritative contextual applicability for the participant's current Engineering activity and applicable participant state, including participant responsibility where such responsibility exists, rather than assume that one applicability determination or context projection applies universally to all activities or participants involving the same governed work.

### CRC-R02 — Authoritative Resolution Basis

The realization must resolve mandatory contextual applicability deterministically from authoritative Engineering state and relationships wherever those relationships permit such resolution.

Semantic, textual, structural, AI-assisted, or other inferential mechanisms must not substitute for deterministic authoritative resolution where authoritative resolution is available.

### CRC-R03 — Applicability Preservation

The realization must preserve the distinction between authoritative contextual applicability and visibility, discoverability, relevance, semantic similarity, relationship proximity, historical applicability, or inferred applicability.

### CRC-R04 — Relationship Semantics

The realization must follow authoritative Engineering relationship semantics when resolving context.

The existence of a direct or transitive relationship must not independently establish contextual applicability unless the Engineering model establishes that applicability semantic.

### CRC-R05 — Conditional Applicability

Where contextual applicability depends upon an authoritative condition or determination, the realization must resolve or consume that condition through the mechanism that owns it.

Unresolved or conditional applicability must not be silently promoted to authoritative applicability.

### CRC-R06 — Materially Complete Composition

The realization must compose Effective Engineering Context that includes the required context necessary for safe and correct participation in the applicable Engineering activity.

Material completeness must not require maximal inclusion of discoverable Engineering information.

### CRC-R07 — Composition Fidelity

Composition may alter representation, structure, ordering, emphasis, summarization, or delivery mechanism but must preserve authoritative applicability, materially significant Engineering meaning, normative force, unresolved conditions, and source authority.

### CRC-R08 — Progressive Composition

The realization may progressively elaborate Effective Engineering Context without treating presentation expansion as a change in authoritative applicability.

Where authoritative applicability changes, the realization must treat that change as an updated context resolution.

### CRC-R09 — Context Layering

The realization must support composition of applicable Engineering Environment Context, Project Context, and Work and Activity Context where those layers are relevant to the Engineering activity.

The realization must preserve the scope, authority, and semantics of context originating from different layers.

### CRC-R10 — Normative Preservation

The realization must preserve materially significant distinctions among requirements, prohibitions, permissions, permitted discretion, recommendations or guidance, unresolved ambiguity, and matters requiring authority or governed determination.

Summarization or projection must not alter materially significant normative force.

### CRC-R11 — Provenance and Reproducibility

The realization must preserve sufficient provenance and derivation information for Effective Engineering Context to be attributable to authoritative Engineering sources and sufficiently reproducible with respect to materially significant applicability, authority, and composition.

Reproducibility does not require identical participant-facing representation.

### CRC-R12 — Context Currency

The realization must support identification of material authoritative changes capable of affecting active Effective Engineering Context.

Changes unrelated to the applicable Engineering activity must not inherently invalidate context solely because they occurred within the Engineering environment.

### CRC-R13 — Context Impact

Where a material authoritative change or context defect is identified, the realization must support determination of potentially affected Effective Engineering Context, Engineering work, activities, or participants using authoritative relationships and derivation information wherever deterministic impact resolution is possible.

Inferentially identified impact must remain distinguishable from authoritative impact.

### CRC-R14 — Stale Context

The realization must preserve the distinction between sufficiently current and stale Effective Engineering Context where that distinction materially affects Engineering activity.

Stale context must not be represented as current merely because it was previously valid or has been persisted.

### CRC-R15 — Context Challenge

The realization must provide a means for an Engineer to challenge Effective Engineering Context believed to be incorrect, incomplete, ambiguous, or stale.

The challenge mechanism must support resolution through correction of the applicable authoritative source state or Platform mechanism rather than manual modification of derived context as a substitute for correction.

### CRC-R16 — Missing and Ambiguous Context

Where authoritative context or applicability is missing, conflicting, ambiguous, conditional, or unresolved, the realization must preserve that condition rather than manufacture authoritative Engineering context to produce a complete-looking projection.

### CRC-R17 — Resumption Context

The realization must reconstruct Effective Engineering Context for resumed Engineering activity from sufficiently current authoritative and durable Engineering state.

Participant memory, conversational continuity, model memory, or previous Effective Engineering Context must not substitute for current authoritative resolution where material state may have changed.

### CRC-R18 — Independent Review Context

The realization must independently resolve peer-review context from current authoritative Engineering state and the reviewer's applicable participant responsibility.

Review context must not simply inherit the realization participant's Effective Engineering Context or working interpretation.

### CRC-R19 — Participant-Appropriate Projection

The realization may provide different context representations for Human Engineers and AI Engineers while preserving common authoritative Engineering semantics.

Participant-specific projection must not create participant-specific Engineering truth.

### CRC-R20 — AI Context Fidelity

AI Engineer projection must explicitly represent, or provide reliable resolution of, the authoritative meaning required for safe and correct AI Engineering participation.

The realization must not rely upon model inference to reconstruct materially significant authoritative meaning omitted from the projection.

### CRC-R21 — Execution-Instance Independence

Replacement or restart of an AI execution instance must not make prior conversational context or model memory authoritative.

A succeeding execution instance must be able to reconstruct applicable Effective Engineering Context from authoritative and durable Engineering state.

### CRC-R22 — Capability Ownership

Where contextual applicability depends upon state or determinations owned by another Engineering Platform capability, Engineering System, authoritative source, or governed mechanism, the realization must consume that state while preserving its authoritative ownership and semantics.

---

## 19. Invariants

The following invariants must hold for every conforming realization of Context Resolution & Composition.

1. **Discoverability does not establish applicability.**  
   Visibility, discovery, navigation, semantic relevance, textual proximity, repository proximity, or inferential association does not independently establish authoritative contextual applicability.

2. **Resolution and composition remain distinct.**  
   Context Resolution determines what applies; Context Composition determines how applicable context is projected. Composition does not independently change applicability.

3. **Effective Engineering Context is derived state.**  
   Effective Engineering Context does not become an independent source of Engineering truth through composition, persistence, caching, presentation, or use.

4. **Authoritative relationships govern applicability.**  
   Context applicability follows authoritative Engineering state and relationship semantics rather than mere relationship reachability or inferential association.

5. **Material completeness is not maximal context.**  
   Effective Engineering Context contains what is materially required for the Engineering activity without requiring inclusion of all discoverable Engineering information.

6. **Normative meaning survives composition.**  
   Requirements, prohibitions, permissions, discretion, recommendations, ambiguity, and matters requiring authority remain materially distinguishable through summarization, transformation, and participant projection.

7. **Missing context remains missing.**  
   Missing, conflicting, ambiguous, conditional, or unresolved authoritative context must not be silently converted into resolved Engineering truth.

8. **Derived context remains attributable.**  
   Materially significant Effective Engineering Context remains sufficiently traceable to the authoritative Engineering sources, relationships, participant basis, and determinations from which it was derived.

9. **Historical context does not establish current context.**  
   Context being previously applicable or current does not establish that its applicability, meaning, or material completeness remains current after material authoritative Engineering state changes.

10. **Context change is materially scoped.**  
    An Engineering change does not inherently invalidate Effective Engineering Context unless the change is capable of materially affecting that context's applicability, meaning, or completeness.

11. **Context correction occurs at the source or derivation mechanism.**  
    Derived Effective Engineering Context is not manually rewritten as a substitute for correcting authoritative Engineering state or the Platform mechanism responsible for its derivation.

12. **Resumption reconstructs context from Engineering state.**  
    Participant memory, conversational continuity, model memory, or ephemeral execution state does not constitute authoritative Resumption Context.

13. **Independent review requires independent resolution.**  
    Peer-review context is resolved from current authoritative Engineering state and reviewer responsibility rather than inherited from the realization participant's context or interpretation.

14. **Participant projection does not alter Engineering truth.**  
    Human Engineer and AI Engineer projections may differ in representation but preserve the authoritative Engineering semantics necessary for their applicable activity and responsibility.

15. **Capability composition does not transfer authority.**  
    Context Resolution & Composition may consume state and determinations owned elsewhere, but authoritative ownership remains with the Engineering capability, System, source, or governed mechanism that establishes them.
