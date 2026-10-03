# Prompt Governance Specification

## 1. Purpose

This specification defines Prompt Governance for Engineering Automation within the Engineering Platform.

Prompt Governance establishes reusable rules for deriving AI execution instructions that conform to the applicable Engineering Operating Model.

Prompt Generation applies those rules to resolved participant, activity, project, system, and authoritative context to produce a conforming AI execution representation.

Prompt Governance exists to enable consistent AI participation across projects without duplicating, redefining, weakening, or replacing the authoritative semantics of the Engineering Platform or its Engineering Systems.

---

## 2. Scope

This specification governs:

- derivation of AI execution instructions for governed Engineering Platform activities;
- resolution and projection of applicable governing semantics into those instructions;
- participant, scope, and authority projection;
- system and activity specialization;
- project and subsystem specialization;
- context applicability;
- treatment of missing and unresolved information;
- generation basis and provenance;
- prompt validation and conformance;
- prompt persistence, reuse, staleness, and regeneration;
- boundaries between Prompt Generation, AI Execution Composition, and Engineering Composition.

This specification does not establish Product, Collaboration, Engineering, or Release semantics.

It does not define participant authority, Engineering System artifacts, lifecycle states, Development Standards, Release authority, or other governed Engineering Platform semantics.

It does not require a particular AI model, provider, prompt representation, template mechanism, manifest format, persistence strategy, runtime, CLI, API, agent framework, or implementation product.

---

## 3. Normative Language

The key words **SHALL**, **SHALL NOT**, **SHOULD**, **SHOULD NOT**, **MAY**, and **MAY NOT** are to be interpreted as normative requirements within this specification.

---

## 4. Semantic and Authority Boundary

Prompt Governance is an Engineering Automation concern subordinate to the authoritative Engineering Platform and Engineering System semantics from which it derives execution instructions.

For the purposes of this specification, the **binkru Engineering Operating Model** is a collective referent for the applicable authoritative operating semantics established by:

- Engineering Platform principles;
- Engineering Platform specifications;
- Product System semantics and governance;
- Collaboration System semantics and governance;
- Engineering System semantics and governance;
- Release System semantics and governance; and
- applicable authoritative project-governed state.

The Engineering Operating Model is not established by this specification as an additional semantic authority layer or independent canonical artifact.

Prompt Governance SHALL preserve the semantic ownership and authority of its governing sources.

Prompt Governance, Prompt Generation, generated prompts, and execution-specific prompt representations SHALL NOT independently redefine, override, weaken, broaden, transfer, aggregate, manufacture, or exercise authority established elsewhere in the Engineering Platform.

Technical ability to generate, modify, persist, retrieve, or execute a prompt SHALL NOT itself establish authority over the governed activity represented by that prompt.

---

## 5. Core Concepts

### 5.1 Prompt Governance

Prompt Governance defines reusable rules for deriving AI execution instructions from applicable authoritative Engineering Platform and project semantics.

Prompt Governance governs the derivation process. It does not own the underlying semantics being projected.

### 5.2 Prompt Generation

Prompt Generation is the application of Prompt Governance rules to a resolved governed activity and its applicable participant, project, system, lifecycle, and authoritative context.

Prompt Generation produces a derived AI execution representation.

### 5.3 Conforming Prompt

A **Conforming Prompt** is an AI execution instruction representation whose material instructions faithfully preserve the applicable:

- semantic ownership;
- lifecycle boundaries;
- participant scope;
- authority;
- constraints;
- governing obligations;
- material uncertainty; and
- provenance requirements

of the governed activity for which the prompt was generated.

Prompt usefulness, completeness, fluency, or execution quality does not by itself establish prompt conformance.

### 5.4 Generation Basis

The **Generation Basis** is the material set of governing sources, resolved contexts, Prompt Governance rules, and applicable specializations used to derive a generated prompt.

Generation Basis is a provenance concept and does not require a separate canonical Engineering Platform artifact.

### 5.5 Operating Model Projection

**Operating Model Projection** is the derivation of execution-relevant obligations from applicable authoritative Engineering Platform and Engineering System semantics.

Projection SHALL preserve governing meaning while adapting it for execution use.

### 5.6 Activity Projection

**Activity Projection** specializes applicable governing semantics for a particular governed activity.

### 5.7 Project and Subsystem Specialization

Project and subsystem specialization applies project-specific or subsystem-specific context, constraints, conventions, and authoritative state to a generated execution representation without altering higher governing semantics.

---

## 6. Prompt Governance Contract

Prompt Governance SHALL derive execution instructions from authoritative semantics rather than establish independent interpretations of those semantics.

Prompt Governance SHALL favor:

> **projection rather than transcription; applicability rather than accumulation.**

Prompt Governance SHALL NOT require the complete Engineering Platform or complete project state to be transcribed into every generated prompt.

Prompt Governance SHALL identify and project the material execution obligations applicable to the governed activity.

A Prompt Governance rule SHALL NOT redefine, override, weaken, broaden, or manufacture authoritative Engineering Platform semantics, governance, state, scope, or authority.

Where Prompt Governance operationalizes an authoritative obligation, the relationship between the rule and its governing basis SHOULD remain traceable where materially useful.

---

## 7. Governed Prompt Scope

Prompt Governance applies where AI materially participates in a governed Engineering Platform activity or creates, refines, transforms, composes, evaluates, validates, reviews, recommends changes to, or acts upon governed Engineering Platform artifacts, state, decisions, or outcomes.

Prompt Governance need not apply to incidental AI interactions that do not materially participate in governed Engineering Platform activity.

The criterion for Prompt Governance applicability is the governed activity and the effect of AI participation, not merely the use of an AI model.

AI used solely as a transient execution aid does not automatically become an independently governed project participant.

Where AI participates independently under persistent scope, responsibility, or delegated authority, applicable participant governance SHALL be resolved separately from Prompt Governance.

---

## 8. Prompt Generation Inputs

Prompt Generation SHALL operate on resolved semantic context rather than independently manufacture participant, activity, or authority interpretations.

Applicable generation inputs MAY include:

- Resolved Activity Context;
- Resolved Participant Context;
- applicable Engineering Platform semantics;
- applicable Engineering System or Collaboration interaction semantics;
- applicable project-governed state;
- applicable subsystem context;
- applicable Development Standards;
- applicable architectural and decision context;
- applicable authoritative artifacts;
- applicable source or implementation context;
- Prompt Governance rules; and
- execution-relevant constraints.

Not every input class is applicable to every governed activity.

Prompt Generation SHALL resolve and use context according to applicability to the governed activity.

---

## 9. Activity-Scoped Context Applicability

Prompt generation readiness SHALL be activity-scoped and lifecycle-aware.

A context element SHALL NOT be required merely because it exists somewhere in the project or may become relevant during a later lifecycle stage.

For a particular governed activity, context may be treated conceptually as:

### 9.1 Required

Context that must have been established and be resolvable for conforming execution of the activity.

Failure to resolve required context SHALL be surfaced and SHALL NOT be silently replaced, inferred, or fabricated.

### 9.2 Applicable

Context that is relevant to the activity when established and available, but is not required by the governing activity to have been established at the current lifecycle point.

### 9.3 Unresolved

Context materially relevant to the activity that has legitimately not yet been established.

Unresolved context SHALL remain unresolved unless the governed activity has authority to establish it.

### 9.4 Not Applicable

Context outside the semantic needs of the current governed activity.

Not-applicable context SHOULD NOT be injected merely because it is available elsewhere in the project.

### 9.5 Missing Required Context

Where governing semantics require information to have been established at the current lifecycle point and that information cannot be resolved, Prompt Generation SHALL treat the condition as missing required context.

Missing required context SHALL NOT be converted into apparent certainty through generated instructions.

Engineering Automation SHALL NOT demand downstream knowledge merely because that knowledge may eventually exist.

---

## 10. Operating Model Projection

Prompt Generation SHALL project applicable authoritative semantics into execution-relevant instructions.

Projection MAY summarize, transform, structure, reference, retrieve, or otherwise optimize authoritative context for execution efficiency provided that material:

- governing semantics;
- semantic ownership;
- authority;
- scope;
- lifecycle boundaries;
- constraints;
- uncertainty; and
- provenance

are preserved.

Prompt Governance SHALL NOT require one universal static master prompt containing the complete Engineering Operating Model.

An implementation MAY generate broad instruction representations where useful, but such representations remain derived and subordinate to their authoritative basis.

---

## 11. System and Activity Projection

Prompt Generation SHALL preserve the semantic boundaries of the Engineering System or governed cross-system interaction applicable to the resolved activity.

### 11.1 Product Projection

Product-oriented prompt generation SHALL preserve applicable:

- Product intent;
- Product semantic ownership;
- Product artifact contracts;
- Product lifecycle;
- Product authority;
- Product governance; and
- downstream Collaboration, Engineering, and Release boundaries.

Product prompt generation SHALL NOT require downstream Engineering implementation knowledge unless that knowledge is materially applicable to the governed Product activity.

The existence of Engineering implementation choices SHALL NOT by itself make those choices applicable to Product prompt generation.

### 11.2 Collaboration Projection

Collaboration-oriented prompt generation SHALL preserve:

- originating-system semantic ownership;
- participating-system authority;
- governed interaction semantics;
- shared-understanding and collaborative-outcome boundaries; and
- non-transfer of semantic ownership merely through collaboration.

Prompt Generation SHALL NOT manufacture a generic Collaboration authority by aggregating participating authorities.

### 11.3 Engineering Projection

Engineering-oriented prompt generation SHALL preserve applicable:

- Engineering artifact semantics;
- Engineering lifecycle;
- investment and planning boundaries;
- realization boundaries;
- Engineering Slice semantics;
- Development Standards;
- Engineering Evidence;
- Engineering Conclusion; and
- Engineering authority.

The specific Engineering context required SHALL depend on the resolved Engineering activity and lifecycle point.

### 11.4 Release Projection

Release-oriented prompt generation SHALL preserve applicable distinctions among:

- Release Admission;
- admitted Release scope;
- Release Candidate identity and integrity;
- Release Evidence;
- Release Readiness;
- Release Authorization;
- Release Promotion;
- Release outcomes;
- Released State; and
- Release Conclusion.

Technical ability to perform a deployment or promotion action SHALL NOT be projected as Release authority.

### 11.5 Activity Specialization

System projection SHALL be further specialized according to the resolved governed activity.

Different activities within the same Engineering System MAY require materially different governing context and execution instructions.

---

## 12. Participant, Scope, and Authority Projection

Prompt Generation SHALL consume resolved participant context where participant-specific execution instructions are required.

Prompt Generation SHALL preserve distinctions among:

- participant identity;
- participant type;
- capacity;
- responsibility;
- scope;
- authority;
- technical permission; and
- execution capability.

Capacity, responsibility, participant type, technical capability, repository access, or execution permission SHALL NOT by themselves be interpreted as governed authority.

Authority SHALL be projected only where established through the applicable resolved authority basis.

Prompt Generation SHALL NOT broaden participant authority to make an execution easier or more complete.

Where AI assists another participant without independently holding the applicable capacity or authority, generated instructions SHOULD represent the AI as assisting that participant rather than falsely asserting the participant's capacity or authority as the AI's own.

Where AI participates independently under delegated authority, generated instructions SHALL preserve the applicable scope and limits of that delegation.

---

## 13. Project and Subsystem Specialization

Prompt Generation MAY specialize execution instructions using applicable project-specific context, including:

- project terminology;
- project artifact locations;
- project architecture;
- project decisions;
- Development Standards;
- repository conventions;
- approved tooling expectations; and
- other governed project constraints.

Project specialization SHALL NOT:

- remove applicable Platform governance;
- broaden participant authority;
- redefine system-owned artifacts;
- alter lifecycle semantics;
- override applicable Development Standards;
- convert unresolved governed state into established state; or
- otherwise contradict higher governing semantics.

Subsystem specialization MAY be applied where a project has materially distinct subsystem context.

Subsystem specialization SHALL NOT be required merely because a project contains subsystems.

---

## 14. Development Standards

Development Standards SHALL be resolved according to their applicability to the governed activity.

Prompt Generation SHALL NOT inject all available Development Standards into every generated prompt.

Product or Collaboration activities SHALL NOT require implementation-specific Development Standards merely because those standards exist elsewhere in the project.

Where an Engineering realization activity relies upon a technology, practice, or constraint governed by an applicable established Development Standard, that standard SHALL be included or appropriately projected where necessary for conforming execution.

Where an applicable Development Standard is required at the current lifecycle point but cannot be resolved, the condition SHALL be surfaced as missing required context.

Where the relevant technology or practice is legitimately unresolved and the current activity does not require it to have been established, Prompt Generation SHALL preserve that unresolved state.

---

## 15. Generated Prompt Semantics

A generated prompt MAY contain execution-oriented representations of:

- participant and participation context;
- governed activity purpose;
- scope;
- authoritative basis;
- applicable obligations;
- semantic and authority boundaries;
- applicable project context;
- applicable Development Standards;
- uncertainty and unresolved matters;
- expected output or execution result;
- authority effect;
- validation expectations; and
- provenance requirements.

The generated representation SHALL distinguish, where material, between actions such as:

- draft;
- recommend;
- evaluate;
- perform;
- validate;
- record;
- establish;
- authorize; and
- conclude.

Generated instructions SHALL NOT imply that successful technical execution establishes a governed outcome where the applicable governance requires a separate authoritative determination.

---

## 16. Source Authority and Conflict Handling

Prompt Generation SHALL preserve the semantic ownership and authority relationships already established among its governing sources.

Sources SHALL NOT be treated as equally authoritative merely because they are available to the generation mechanism.

Prompt Generation SHALL NOT resolve material source conflicts through arbitrary source ordering where governing authority does not already establish the resolution.

Where authoritative sources materially conflict and the conflict cannot be resolved under existing governance, the conflict SHALL be surfaced.

Runtime user instructions, project customization, generated prompt content, or technical configuration SHALL NOT override applicable governing semantics merely because they are more recent or operationally convenient.

---

## 17. Missing Information and Uncertainty

Prompt Generation SHALL NOT invent missing governed information merely to produce a complete-looking execution representation.

Material uncertainty SHALL be preserved.

Where a decision has not yet been established, Prompt Generation SHALL NOT represent that decision as established unless the current governed activity has authority to establish it and actually does so through the applicable governance.

Where information is:

- not applicable, it SHOULD normally be omitted;
- applicable but unavailable, its absence SHOULD be represented according to its materiality;
- legitimately unresolved, it SHALL remain unresolved;
- required but missing, the condition SHALL be surfaced as an impediment to conforming generation or execution.

---

## 18. Generation Basis and Provenance

Prompt Generation SHALL preserve sufficient Generation Basis provenance to identify the material basis from which generated execution instructions were derived and to support applicable conformance, reconstruction, validation, or reuse.

Generation Basis MAY include:

- Prompt Governance mechanism or rule version;
- applicable Engineering Platform basis;
- applicable Engineering System or interaction basis;
- resolved system and activity;
- project and subsystem basis;
- applicable Development Standards;
- resolved participant and authority basis;
- material authoritative inputs; and
- generation-time validation information.

Generation Basis SHALL NOT itself become an independent semantic authority.

Implementations MAY represent Generation Basis in any conforming form.

---

## 19. Prompt Persistence, Reuse, and Staleness

Generated prompts MAY be:

- generated dynamically for a single execution;
- cached for reuse;
- persisted as derived project automation assets; or
- regenerated from current governing context.

Persistence, version control, review, or reuse SHALL NOT elevate a generated prompt into an authoritative Product, Collaboration, Engineering, or Release artifact.

A persisted or reused prompt SHALL NOT be assumed current solely because it remains available.

Where its governing basis has materially changed, applicability SHALL be reassessed.

Material changes MAY include changes to:

- Engineering Platform semantics;
- Engineering System governance;
- governed activity semantics;
- participant scope or authority;
- Development Standards;
- project governance;
- project architecture; or
- other material generation inputs.

A basis change SHALL NOT automatically require regeneration where the change does not materially affect the intended execution.

---

## 20. Prompt Validation and Conformance

Prompt validation SHALL evaluate all applicable dimensions including:

### 20.1 Resolution Validity

Whether required participant, activity, authority, and context inputs were successfully resolved.

### 20.2 Structural Validity

Whether the generated representation is structurally consumable by its intended execution mechanism.

### 20.3 Semantic Conformance

Whether the generated instructions preserve applicable governing semantics, authority, lifecycle boundaries, scope, constraints, and uncertainty.

### 20.4 Basis Validity

Whether the Generation Basis remains applicable to the intended execution.

A successful validation execution SHALL NOT itself establish a Product, Collaboration, Engineering, or Release determination unless the applicable governance explicitly grants authority for that determination.

Validation status SHALL NOT be represented as established where the required validation has not occurred.

---

## 21. Failure Semantics

Prompt Governance and Prompt Generation SHALL preserve failure fidelity.

Examples include:

- unresolved participant SHALL remain unresolved rather than receiving inferred authority;
- unresolved activity SHALL not be silently mapped to a guessed governed activity;
- missing required authoritative context SHALL be surfaced rather than fabricated;
- material source conflict SHALL be surfaced rather than silently resolved;
- prompt construction failure SHALL be treated as an Engineering Automation failure rather than a governed Engineering System failure;
- execution-runtime limitations SHALL NOT be interpreted as permission to omit material governing constraints.

Where execution context limitations prevent all applicable governing information from being represented directly, the implementation MAY use retrieval, summarization, structured projection, references, or other mechanisms, but SHALL NOT silently discard material governance obligations.

---

## 22. AI Execution Composition Boundary

Prompt Generation and AI Execution Composition are distinct.

Prompt Generation answers:

> **What governed execution instructions apply to this AI participation?**

AI Execution Composition answers:

> **What does this AI execution require now for this specific execution instance?**

AI Execution Composition MAY combine:

- generated instructions;
- current authoritative artifacts;
- current source or implementation context;
- participant and scope context;
- current lifecycle state;
- runtime constraints;
- available tools and execution capabilities; and
- other execution-specific information.

Execution-specific representations remain derived and SHALL NOT acquire semantic authority merely by containing authoritative material.

---

## 23. Engineering Composition Boundary

Prompt Governance does not redefine Engineering Composition.

Engineering Composition remains governed by the Engineering System.

Engineering Automation MAY implement or reuse source resolution, transformation, composition, validation, provenance, or other mechanics across both Engineering Composition and Prompt Generation.

Shared implementation mechanics SHALL NOT merge their semantic ownership or governed purposes.

Engineering Composition governs controlled Engineering derivation.

Prompt Generation governs derivation of AI execution instructions.

AI Execution Composition prepares a specific AI execution using those instructions and current execution context.

---

## 24. Human, AI, and Automation Boundary

Prompt Governance specifically governs AI execution instructions.

A human participant MAY perform governed Engineering Platform activities through Engineering Automation without Prompt Generation where AI execution instructions are unnecessary.

Deterministic automation MAY use applicable participant, activity, authority, context, validation, or provenance mechanisms without becoming prompt-governed merely because those mechanisms are shared.

Where non-AI automation later requires equivalent governed execution projections, implementations MAY reuse compatible Prompt Governance mechanics without treating prompts as the required universal representation.

Participant type SHALL NOT determine authority.

---

## 25. Implementation Neutrality

This specification does not require:

- a universal master prompt;
- a particular prompt format;
- textual prompts;
- prompt templates;
- a prompt schema;
- a prompt manifest;
- a Prompt Conformance Report;
- a particular AI model or provider;
- a particular agent framework;
- a particular context-window strategy;
- prompt persistence;
- a particular programming language;
- a particular CLI or API;
- a particular source-resolution mechanism; or
- a particular Engineering Automation implementation.

Implementations MAY use templates, structured representations, generated instructions, retrieval, compiled rules, declarative configuration, programmatic generation, or other mechanisms provided they conform to this specification.

Tool-specific implementations remain subordinate to this specification and the authoritative Engineering Platform semantics from which it derives.

---

## 26. Evolution and Conformance

Prompt Governance implementations MAY evolve as Engineering Automation implementation experience reveals improved mechanisms for projection, resolution, generation, validation, provenance, execution preparation, or runtime integration.

Implementation detail does not constitute missing Engineering Platform architecture.

Changes to Prompt Governance or its implementation SHALL conform to the closed Engineering Platform architecture and applicable Engineering System semantics.

A proposed change requires architectural reconsideration only where it materially alters an established architectural obligation under the applicable Engineering Platform architecture-reopening criteria.

Prompt Governance SHALL remain an Engineering Automation mechanism and SHALL NOT evolve into an independent source of Engineering Platform semantic authority.

The governing objective remains:

> **derive conforming execution instructions from authoritative Engineering semantics without creating another interpretation of those semantics.**
