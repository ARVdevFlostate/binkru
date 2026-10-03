# Activity Resolution Specification

## 1. Purpose

This specification defines Activity Resolution for Engineering Automation within the Engineering Platform.

Activity Resolution enables Engineering Automation to determine the governed Engineering Platform activity applicable to participant intent and current governed context while preserving the semantic ownership, lifecycle boundaries, governance, authority conditions, scope, and provenance established by authoritative sources.

Activity Resolution exists so that human, AI, automation, and mixed-participant interaction can invoke governed Engineering Platform activities without requiring participants to reproduce internal Platform terminology or implementation-specific commands.

Activity Resolution does not define governed activities. It resolves activity meaning from authoritative Engineering Platform, Engineering System, cross-system, and applicable project-governed semantics.

---

## 2. Scope

This specification governs:

- participant-intent interpretation for governed Engineering Platform activities;
- governed activity identification;
- Engineering System resolution;
- governed cross-system interaction resolution;
- lifecycle-context resolution;
- activity semantic-basis resolution;
- activity-instance resolution where applicable;
- applicable activity scope;
- applicable governance and authority-condition resolution;
- expected governed-effect resolution;
- activity discovery;
- activity aliases and implementation mappings;
- ambiguous or unresolved activity handling;
- activity-resolution provenance;
- the relationship between Activity Resolution and downstream Engineering Automation mechanisms.

This specification does not define:

- Product, Collaboration, Engineering, or Release activities;
- Engineering Platform lifecycle semantics;
- participant authority;
- lifecycle readiness;
- execution readiness;
- Release readiness;
- authorization to perform an activity;
- authorization to establish a governed outcome;
- technical operations;
- runtime execution capabilities;
- a universal activity catalog; or
- an independent Engineering Automation lifecycle.

---

## 3. Normative Language

The key words **SHALL**, **SHALL NOT**, **SHOULD**, **SHOULD NOT**, **MAY**, and **MAY NOT** are to be interpreted as normative requirements within this specification.

---

## 4. Semantic and Authority Boundary

Activity Resolution is an Engineering Automation mechanism subordinate to the authoritative Engineering Platform, Engineering Systems, governed cross-system interactions, and applicable project-governed sources from which activity semantics are resolved.

Activity Resolution SHALL NOT independently define, broaden, narrow, aggregate, replace, or manufacture governed Engineering Platform activities.

Activity Resolution SHALL preserve the semantic ownership and authority relationships established by the governing sources of the resolved activity.

Participant intent SHALL NOT itself establish:

- governed activity semantics;
- participant authority;
- lifecycle readiness;
- execution readiness;
- authorization;
- approval;
- completion;
- acceptance;
- admission;
- readiness;
- promotion;
- conclusion; or
- any other governed state or effect.

Technical ability to invoke a command, call an API, execute a workflow, operate a tool, modify an artifact, deploy software, or produce a result SHALL NOT itself establish the governed activity or authority applicable to that operation.

Activity Resolution resolves existing governed activity semantics rather than creating them.

---

## 5. Core Concepts

### 5.1 Participant Intent

**Participant Intent** is an expressed or invoked indication that a participant seeks to perform, assist with, inspect, prepare, evaluate, or otherwise interact with a governed Engineering Platform activity.

Participant Intent MAY be expressed through:

- natural language;
- a CLI command;
- an API request;
- a user-interface action;
- an automation event;
- an agent invocation;
- a workflow transition;
- a structured request; or
- another implementation-specific interaction mechanism.

Participant Intent is an input to Activity Resolution.

Participant Intent SHALL NOT independently define governed activity semantics or establish authority to produce the requested governed effect.

### 5.2 Governed Activity

A **Governed Activity** is an activity whose meaning, lifecycle relationship, governance, authority conditions, inputs, outputs, or governed effects are established by applicable Engineering Platform, Engineering System, cross-system, or project-governed semantics.

Engineering Automation resolves Governed Activities but does not become their semantic owner.

### 5.3 Activity Identity

**Activity Identity** identifies the governed activity semantics applicable to an intended action.

Activity Identity refers to the governed activity itself rather than a particular project occurrence of that activity.

### 5.4 Activity Instance

An **Activity Instance** identifies the application of a Governed Activity to a particular project scope, governed object, lifecycle context, or other concrete execution context.

For example, a governed Engineering Slice realization activity may be applied to a particular Engineering Slice.

Activity Instance SHALL remain subordinate to the semantics of its resolved Activity Identity.

### 5.5 Activity Resolution

**Activity Resolution** is the Engineering Automation process of resolving Participant Intent and applicable governed context to a Governed Activity and its material execution-oriented semantic context.

### 5.6 Resolved Activity Context

**Resolved Activity Context** is the derived execution-oriented representation produced by Activity Resolution for use by downstream Engineering Automation mechanisms.

Resolved Activity Context MAY include:

- Activity Identity;
- Activity Instance;
- applicable Engineering System or governed cross-system interaction;
- lifecycle context;
- semantic basis;
- applicable scope;
- applicable inputs or governed state;
- expected governed effect;
- applicable governance;
- authority conditions;
- material activity boundaries;
- unresolved matters; and
- provenance.

Resolved Activity Context is a derived representation.

It SHALL NOT acquire independent semantic authority merely because it contains authoritative activity information.

---

## 6. Activity Resolution Contract

Activity Resolution SHALL resolve governed activity meaning from authoritative Engineering Platform, Engineering System, governed cross-system, and applicable project-governed sources.

Activity Resolution SHALL preserve the governing:

- activity meaning;
- semantic ownership;
- Engineering System or cross-system boundary;
- lifecycle context;
- scope;
- governance;
- authority conditions;
- expected governed effect;
- material constraints;
- uncertainty; and
- provenance.

Activity Resolution SHALL NOT use free-form Participant Intent, technical operation names, aliases, routing metadata, or execution capability as independent semantic authority for a Governed Activity.

Where the applicable Governed Activity cannot be established reliably, Activity Resolution SHALL preserve the activity as unresolved.

Engineering Automation SHALL NOT silently select a materially different Governed Activity merely to permit downstream execution.

---

## 7. Intent Interpretation

Engineering Automation MAY interpret Participant Intent expressed using terminology that differs from canonical Engineering Platform or Engineering System terminology.

Intent interpretation MAY use:

- natural-language interpretation;
- aliases;
- command mappings;
- structured request fields;
- current project context;
- governed object identity;
- lifecycle context;
- participant context;
- prior interaction context;
- implementation routing metadata; or
- other conforming resolution mechanisms.

Intent interpretation SHALL remain a resolution mechanism rather than a source of governed activity semantics.

Where Participant Intent is incomplete but applicable governed context uniquely resolves the intended Governed Activity, Activity Resolution MAY resolve the activity using that context.

Where materially different Governed Activities remain plausible, Activity Resolution SHALL preserve the ambiguity rather than choose one solely through statistical likelihood, implementation convenience, or technical availability.

---

## 8. Engineering System and Cross-System Resolution

Every resolved Governed Activity SHALL remain associated with its applicable authoritative Engineering System or governed cross-system interaction.

Activity Resolution SHALL preserve distinctions among:

- Product System activities;
- Collaboration System governed interactions;
- Engineering System activities; and
- Release System activities.

An activity SHALL NOT be reassigned to another Engineering System merely because:

- another system originated an artifact involved in the activity;
- another system consumes the resulting artifact or outcome;
- a participant holds capacity in another system;
- an automation mechanism is shared across systems; or
- reassignment would simplify implementation.

Where a Governed Activity belongs to a cross-system Collaboration domain, Activity Resolution SHALL preserve that governed interaction rather than collapse the activity into one participating Engineering System.

For example, Product–Engineering Epic Refinement remains a governed Product–Engineering Collaboration activity even though Product-owned and Engineering-relevant semantics participate in the interaction.

Release Admission remains a governed Engineering–Release Collaboration activity rather than an Engineering or Release activity merely for automation convenience.

---

## 9. Lifecycle Context

Activity Resolution SHALL identify applicable lifecycle context where lifecycle position is material to the meaning or applicability of a Governed Activity.

The same Participant Intent MAY resolve differently where governing lifecycle context materially changes its meaning.

Activity Resolution SHALL NOT manufacture lifecycle state where applicable state cannot be resolved.

Activity Resolution SHALL preserve unresolved lifecycle context where the missing context prevents reliable activity resolution.

Resolution of a Governed Activity SHALL NOT itself establish that:

- lifecycle prerequisites are satisfied;
- the activity is currently ready;
- the activity may currently execute;
- the participant possesses applicable authority; or
- the expected governed effect may be established.

Lifecycle applicability and execution permissibility remain governed by their applicable semantic and authority sources.

---

## 10. Activity Identity and Activity Instance

Activity Resolution SHOULD distinguish Activity Identity from Activity Instance where a concrete governed object, scope, or project occurrence is material.

Activity Identity answers:

> What governed activity is this?

Activity Instance answers:

> To what particular governed object, scope, or project context is this activity being applied?

Resolution of an Activity Identity SHALL NOT require an Activity Instance where the intended interaction is legitimately activity-level, exploratory, or discovery-oriented.

Where an Activity Instance is required for downstream execution but cannot be resolved, Activity Resolution SHALL preserve the activity identity and surface the unresolved instance rather than invent one.

---

## 11. Activity Scope

Activity Resolution SHALL preserve the applicable scope of the Governed Activity.

Activity scope MAY include, where applicable:

- project;
- Engineering System;
- cross-system interaction;
- subsystem;
- governed artifact;
- Engineering Slice;
- Product Capability;
- Release;
- Release Candidate; or
- another scope established by governing semantics.

Activity Resolution SHALL NOT broaden activity scope merely because broader project information or technical access is available.

Where activity scope is materially ambiguous or unresolved, Activity Resolution SHALL preserve that condition rather than assume project-wide scope.

Activity scope SHALL remain distinct from participant authority scope.

Downstream Engineering Automation SHALL evaluate both where applicable.

---

## 12. Semantic Basis

Resolved Activity Context SHALL remain traceable to the material governing sources from which the activity semantics were resolved.

The Semantic Basis MAY include applicable:

- Engineering Platform principles;
- Engineering Platform specifications;
- Product System semantics;
- Collaboration System semantics;
- Engineering System semantics;
- Release System semantics;
- project-governed state;
- project-specific governance; and
- other authoritative sources relevant to the resolved activity.

Activity Resolution SHALL preserve existing authority and precedence relationships among governing sources.

Where material governing sources conflict and existing governance does not establish their resolution, Activity Resolution SHALL surface the conflict rather than resolve it through arbitrary source ordering.

---

## 13. Applicable Inputs and Governed State

Activity Resolution MAY identify authoritative artifacts, governed state, or other inputs materially associated with a resolved Governed Activity.

Identification of an input does not establish that the input exists, is complete, is current, or is sufficient for execution.

Activity Resolution SHALL distinguish, where material, between:

- an input required by the governed activity;
- an input applicable if established;
- an input legitimately unresolved at the current lifecycle point;
- a required input that is expected to have been established but cannot be resolved; and
- information outside the applicable activity context.

Detailed retrieval and composition of activity-specific context MAY be performed by Context Resolution or other downstream Engineering Automation mechanisms.

Activity Resolution SHALL NOT require downstream information merely because that information may become relevant later in the lifecycle.

---

## 14. Governance and Authority Conditions

Activity Resolution SHALL identify applicable governance and authority conditions where those conditions are material to the resolved Governed Activity.

Identification of an authority condition SHALL NOT establish that a participant satisfies that condition.

Participant authority SHALL be resolved through Participant Resolution and applicable governing sources.

Activity Resolution SHALL preserve distinctions among materially different governed effects such as:

- drafting;
- recommending;
- evaluating;
- performing;
- validating;
- recording;
- establishing;
- authorizing;
- concluding; or
- another effect established by applicable governance.

This specification does not establish a universal governed-effect or authority vocabulary.

The meaning of each condition remains governed by the authoritative source of the activity.

---

## 15. Expected Governed Effect

Activity Resolution SHOULD identify the expected governed effect of a resolved activity where that effect is material to downstream preparation or execution.

An expected governed effect describes what the activity may establish, produce, modify, evaluate, preserve, or cause when performed conformingly and under applicable authority.

Identification of an expected governed effect SHALL NOT itself establish that effect.

Technical completion of an operation SHALL NOT automatically establish the corresponding governed effect.

Where the expected governed effect depends upon a separate governed determination or authority, Activity Resolution SHALL preserve that boundary.

---

## 16. Activity Discovery

Engineering Automation MAY support discovery of Governed Activities applicable to current project context.

Activity discovery MAY consider:

- current governed state;
- applicable Engineering System or cross-system interaction;
- lifecycle context;
- governed object;
- Resolved Participant Context;
- participant capacity;
- participant responsibility;
- participant authority;
- unresolved prerequisites; and
- other applicable governed context.

Activity discovery SHALL distinguish activity relevance or applicability from participant authority where the distinction is material.

The presence of an activity in a discovery result SHALL NOT by itself establish that the participant:

- possesses authority to perform it;
- satisfies lifecycle prerequisites;
- may currently execute it; or
- may establish its governed effect.

Where authority has been resolved, implementations MAY communicate authority-sensitive activity availability provided the distinction between activity applicability, authority, and execution capability remains preserved.

Activity discovery SHALL derive governed activity meaning from authoritative sources rather than an independent Engineering Automation activity model.

---

## 17. Activity Aliases, Commands, and Mappings

Engineering Automation implementations MAY maintain aliases, commands, classifiers, routing tables, mappings, model instructions, or other metadata that assist Activity Resolution.

Such mechanisms are derived automation assets.

They SHALL NOT independently define:

- Governed Activity semantics;
- lifecycle position;
- semantic ownership;
- authority requirements;
- governed effects; or
- Engineering System boundaries.

An alias or command MAY map participant terminology to a Governed Activity but SHALL remain subordinate to the authoritative semantic basis of that activity.

Changes to governing activity semantics SHALL NOT be considered incorporated merely because existing automation mappings remain unchanged.

Persisted mappings SHOULD be reassessed where material governing semantics change.

---

## 18. Ambiguity and Unresolved Activity

Activity Resolution SHALL preserve material ambiguity.

A Governed Activity SHALL remain unresolved where:

- Participant Intent materially corresponds to more than one Governed Activity;
- required lifecycle context cannot be resolved;
- the governed object or scope required to distinguish activities cannot be resolved;
- material governing sources conflict without an established resolution;
- no authoritative governed activity corresponding to the requested effect can be established; or
- another material resolution dependency remains unresolved.

An unresolved activity SHALL NOT be converted into a resolved activity solely because:

- one candidate is statistically more likely;
- one candidate is easier to automate;
- one candidate has an available runtime;
- one candidate matches a familiar command;
- one candidate permits the requested outcome; or
- selecting one avoids asking for additional information.

Downstream Engineering Automation SHALL preserve the unresolved condition where it remains material.

---

## 19. Activity Resolution Versus Readiness and Authorization

Activity Resolution answers:

> **What governed activity is applicable?**

It does not independently answer:

> **May this participant perform it now?**

or:

> **Are all prerequisites for execution satisfied?**

or:

> **May the resulting governed effect be established?**

A Governed Activity MAY therefore be correctly resolved while:

- participant authority remains unresolved;
- required context is missing;
- lifecycle prerequisites are unsatisfied;
- validation is incomplete;
- runtime capability is unavailable;
- execution is prohibited; or
- authorization has not been established.

Downstream Engineering Automation SHALL preserve these distinctions.

Activity Resolution SHALL NOT become an implicit execution-authorization mechanism.

---

## 20. Relationship to Participant Resolution

Participant Resolution and Activity Resolution are distinct Engineering Automation mechanisms.

Participant Resolution resolves who is participating, in what capacity and scope, and under what applicable authority or constraints.

Activity Resolution resolves what Governed Activity is applicable and the material semantic context of that activity.

Either mechanism MAY contribute context useful to the other where implementation requires iterative resolution.

Neither mechanism SHALL manufacture the unresolved semantics of the other.

A resolved activity SHALL NOT imply resolved participant authority.

A resolved participant SHALL NOT imply a particular Governed Activity.

Downstream Engineering Automation MAY combine Resolved Participant Context and Resolved Activity Context where required for governed execution preparation.

---

## 21. Relationship to Context Resolution

Activity Resolution determines the semantic requirements and applicability boundaries that inform activity-specific Context Resolution.

Context Resolution MAY retrieve, assemble, project, or otherwise prepare authoritative and applicable project context required for the resolved activity.

Activity Resolution SHALL NOT be required to retrieve or compose all execution context itself.

The relationship is conceptually:

**Participant Intent + applicable governed context → Activity Resolution → Resolved Activity Context → Context Resolution**

where additional Participant Resolution context MAY participate as required.

Context Resolution SHALL remain responsible for determining and preparing the applicable execution context without altering the semantic meaning of the resolved Governed Activity.

---

## 22. Relationship to Prompt Governance and Prompt Generation

Prompt Governance and Prompt Generation SHALL consume Resolved Activity Context rather than independently invent governed activity semantics from prompt wording.

Resolved Activity Context informs the applicable:

- Engineering System or cross-system projection;
- lifecycle semantics;
- semantic basis;
- activity obligations;
- authority conditions;
- boundaries;
- expected governed effect; and
- context applicability

used for conforming Prompt Generation.

Prompt Generation MAY express the resolved activity in execution-oriented language appropriate to AI participation.

Such expression SHALL remain subordinate to the authoritative activity semantics preserved by Activity Resolution.

---

## 23. Relationship to Execution Composition

Execution Composition MAY combine:

- Resolved Participant Context;
- Resolved Activity Context;
- resolved applicable context;
- conforming AI execution instructions where AI participates;
- runtime constraints; and
- available execution capabilities

to prepare an execution-specific representation.

Execution Composition SHALL NOT reinterpret the Governed Activity merely to match available runtime capabilities.

If available execution capabilities cannot conformingly perform the resolved activity, the limitation SHALL remain an execution-preparation or runtime limitation rather than causing Activity Resolution to select a different Governed Activity.

---

## 24. Resolution Failure and Failure Fidelity

Activity Resolution SHALL preserve failure fidelity.

Examples include:

- unrecognized Participant Intent SHALL remain unresolved rather than being forced into a known activity;
- materially ambiguous intent SHALL remain ambiguous;
- missing required lifecycle context SHALL be surfaced;
- unresolved activity scope SHALL remain unresolved;
- missing authoritative semantic basis SHALL be surfaced;
- conflicting governing sources SHALL be surfaced where governance does not establish their resolution;
- inability to retrieve resolution metadata SHALL be treated as an automation-resolution failure rather than a Product, Collaboration, Engineering, or Release failure;
- unavailable runtime capability SHALL NOT be represented as failure of the Governed Activity itself.

Resolution failure SHALL NOT establish lifecycle failure, participant failure, Engineering failure, Release failure, or another governed conclusion unless the applicable governing semantics independently establish such a conclusion.

---

## 25. Provenance and Continuity

Activity Resolution SHALL preserve sufficient provenance to identify the material basis from which a Governed Activity and its material context were resolved where required for conformance, reconstruction, validation, continuity, or governed execution.

Relevant provenance MAY include:

- Participant Intent basis;
- resolved Activity Identity;
- Activity Instance basis;
- applicable Engineering System or cross-system interaction;
- lifecycle-context basis;
- governing semantic sources;
- activity scope;
- material project state;
- automation mappings or aliases materially used in resolution; and
- resolution mechanism or version where useful.

Resolved Activity Context MAY be persisted or cached where useful.

Persisted Resolved Activity Context SHALL NOT be assumed current solely because it remains available.

Where material governing activity semantics, lifecycle context, project state, scope, mappings, or other resolution basis changes, persisted context SHALL be reassessed before reuse where the change may affect the intended activity.

---

## 26. Validation

Activity Resolution SHALL support validation of all applicable concerns including:

- Participant Intent resolvability;
- Activity Identity resolvability;
- Activity Instance resolvability where required;
- Engineering System or cross-system association;
- lifecycle-context validity;
- semantic-basis validity;
- activity-scope validity;
- applicable governance resolution;
- authority-condition resolution;
- expected governed-effect consistency;
- material source conflicts; and
- provenance sufficiency.

Successful technical validation of Resolved Activity Context SHALL NOT establish participant authority, lifecycle readiness, execution readiness, or authorization to produce the governed effect.

Validation execution SHALL NOT manufacture governed activity semantics or authority.

---

## 27. Implementation Neutrality

This specification does not require:

- a universal activity catalog;
- an activity registry;
- activity-definition YAML files;
- an activity database;
- a centralized activity service;
- a universal activity identifier namespace;
- a universal governed-effect vocabulary;
- a universal authority vocabulary;
- a particular natural-language model;
- a particular classifier;
- a particular routing algorithm;
- a particular alias mechanism;
- a particular command structure;
- a particular CLI;
- a particular API;
- a particular user interface;
- a particular workflow engine;
- a particular programming language;
- a particular storage mechanism; or
- a particular Engineering Automation implementation.

Implementations MAY introduce such mechanisms where required provided they remain subordinate to authoritative Engineering Platform and Engineering System semantics and conform to this specification.

---

## 28. Evolution and Conformance

Activity Resolution implementations MAY evolve as Engineering Automation implementation experience reveals improved mechanisms for intent interpretation, activity discovery, semantic-source resolution, lifecycle resolution, routing, mapping, ambiguity handling, validation, provenance, continuity, or downstream integration.

Implementation detail does not constitute missing Engineering Platform architecture.

Changes to Activity Resolution or its implementation SHALL conform to the closed Engineering Platform architecture and applicable Product, Collaboration, Engineering, and Release System semantics.

A proposed change requires architectural reconsideration only where it materially alters an established architectural obligation under the applicable Engineering Platform architecture-reopening criteria.

Activity Resolution SHALL remain an Engineering Automation mechanism and SHALL NOT evolve into an independent source of Product, Collaboration, Engineering, Release, lifecycle, governance, or authority semantics.

The governing objective remains:

> **resolve the governed activity faithfully without becoming the source of the activity's meaning.**
