# Participant Resolution Specification

## 1. Purpose

This specification defines Participant Resolution for Engineering Automation within the Engineering Platform.

Participant Resolution enables Engineering Automation to determine the applicable participant context for a governed Engineering Platform activity while preserving the semantic ownership, authority, scope, and provenance established by governing sources.

Participant Resolution exists so that human, AI, automation, and mixed-participant execution can operate consistently without inferring governed authority from identity, role-like labels, technical access, execution capability, or automation configuration.

Participant Resolution does not establish participant authority. It resolves and applies authority and participation context whose meaning and validity are established elsewhere.

---

## 2. Scope

This specification governs:

- participant identification for governed Engineering Platform activities;
- participant type resolution;
- participant capacity resolution;
- participant responsibility resolution where applicable;
- participant scope resolution;
- participant authority resolution;
- participant constraint resolution;
- participant participation-status resolution;
- project-owned Participant Declarations;
- authority-binding resolution;
- delegation resolution where applicable;
- participant provenance;
- initiating, executing, and authorizing participant distinctions where material;
- AI and automation participation;
- cross-system participant resolution;
- participant-resolution failure and uncertainty;
- the relationship between Participant Resolution and downstream Engineering Automation mechanisms.

This specification does not define:

- Product, Collaboration, Engineering, or Release authority semantics;
- organizational authority;
- participant authority assignments;
- authentication;
- identity management;
- access-control policy;
- runtime tool permissions;
- execution capability;
- Engineering Platform lifecycle states; or
- a universal participant-management system.

---

## 3. Normative Language

The key words **SHALL**, **SHALL NOT**, **SHOULD**, **SHOULD NOT**, **MAY**, and **MAY NOT** are to be interpreted as normative requirements within this specification.

---

## 4. Semantic and Authority Boundary

Participant Resolution is an Engineering Automation mechanism subordinate to the authoritative Engineering Platform, Engineering System, cross-system governance, and applicable project-governed sources from which participation and authority semantics are resolved.

Participant Resolution SHALL NOT define, grant, broaden, transfer, aggregate, manufacture, or independently exercise governed authority.

Participant Resolution SHALL preserve the distinction between:

- responsibility and authority;
- capacity and authority;
- participant type and authority;
- technical permission and authority;
- execution capability and authority; and
- ability to determine a result and authority to establish the corresponding governed state.

Technical ability to identify a participant, retrieve a declaration, modify project configuration, invoke a tool, execute an operation, or produce a result SHALL NOT itself establish governed authority.

Participant Resolution SHALL resolve existing authority relationships rather than create them.

---

## 5. Core Concepts

### 5.1 Participant

A **Participant** is a human, AI, or automation entity that participates in a governed Engineering Platform activity.

A Participant may participate directly, assist another participant, execute an authorized action, or operate under explicitly established delegated authority.

Participant identity alone does not establish capacity, responsibility, scope, or authority.

### 5.2 Participant Declaration

A **Participant Declaration** is project-owned governed configuration that identifies a persistent project participant and records applicable participation context required for resolution.

A Participant Declaration MAY record:

- participant identity;
- participant type;
- capacities;
- responsibilities;
- scope;
- authority bindings;
- constraints;
- participation status;
- identity bindings;
- effective conditions;
- delegation information;
- basis or provenance; and
- descriptive information.

A Participant Declaration records project-applicable participation and authority bindings whose meaning and validity remain governed by their authoritative basis.

A Participant Declaration SHALL NOT independently define the meaning of an authority.

### 5.3 Participant Resolution

**Participant Resolution** is the Engineering Automation process of resolving applicable participant identity, type, capacity, responsibility, scope, authority, constraints, status, and provenance for a governed activity.

### 5.4 Resolved Participant Context

**Resolved Participant Context** is the derived execution-oriented representation produced by Participant Resolution for use by downstream Engineering Automation mechanisms.

Resolved Participant Context is a derived representation.

It SHALL NOT acquire independent semantic authority merely because it contains authoritative participation or authority information.

### 5.5 Capacity

A **Capacity** identifies the governed context in which a participant participates.

A participant MAY hold multiple capacities.

Capacity SHALL NOT itself establish authority.

### 5.6 Responsibility

A **Responsibility** identifies an activity, concern, or obligation with which a participant is associated.

Responsibility MAY support participant discovery, activity routing, coordination, or identification of missing participation.

Responsibility SHALL NOT itself establish authority.

### 5.7 Scope

**Scope** identifies the boundary within which a participant's participation, responsibility, constraint, or authority applies.

Scope MAY be expressed in terms appropriate to the governing context, including project, Engineering System, cross-system interaction, subsystem, artifact, or governed activity.

Scope semantics SHALL remain subordinate to their governing basis.

### 5.8 Authority Binding

An **Authority Binding** records an applicable relationship between a participant and authority established under a governing basis.

An Authority Binding references or resolves governing authority semantics. It does not define those semantics.

### 5.9 Participation Status

**Participation Status** identifies whether a persistent Participant Declaration is currently applicable for participant resolution.

The standard participant representation SHOULD support at least:

- active; and
- inactive.

Additional status semantics SHALL NOT be assumed unless established by applicable governance or implementation requirements.

---

## 6. Participant Resolution Contract

Participant Resolution SHALL determine applicable participant context using authoritative and project-governed sources.

Participant Resolution SHALL preserve the governing meaning, scope, authority, constraints, and provenance of resolved information.

Authority SHALL be positively established through an applicable authority binding and governing basis.

Authority SHALL NOT be inferred solely from:

- participant type;
- capacity;
- responsibility;
- repository access;
- technical permission;
- tool availability;
- runtime credentials;
- execution capability;
- configuration ownership;
- artifact authorship;
- prompt wording;
- team membership; or
- absence of an explicit prohibition.

Where applicable authority cannot be established, Participant Resolution SHALL preserve that authority as unresolved.

Engineering Automation SHALL NOT broaden unresolved authority merely to permit an activity to proceed.

---

## 7. Participant Identity

Persistent governed participants SHALL have a stable project participant identity sufficient for attributable participant resolution.

Participant identity SHALL be established by declaration content or another conforming authoritative representation rather than solely by a filename, repository path, runtime username, tool identity, or display label.

External identity bindings MAY associate a project participant with identities from source-control systems, identity providers, communication systems, runtime environments, or other external systems.

External identity binding SHALL NOT by itself establish governed authority.

Where multiple external identities correspond to one governed project participant, implementations MAY resolve them to the same stable participant identity where the governing basis supports that relationship.

---

## 8. Participant Types

The standard participant model recognizes the broad participant types:

- human;
- AI; and
- automation.

Participant type describes the general nature of the participant and SHALL NOT establish authority.

Execution forms such as agent, bot, service account, workflow, CLI user, model invocation, or process SHALL NOT require independent semantic participant types merely because they differ technically.

Implementations MAY retain additional technical classification where useful without treating those classifications as governed authority semantics.

---

## 9. Capacity and Responsibility Resolution

Participant Resolution MAY resolve one or more applicable capacities for a participant.

Capacity resolution SHALL be sensitive to the governed activity and its applicable Engineering System or cross-system interaction.

A participant's capacity in one Engineering System SHALL NOT automatically apply to another Engineering System.

A participant's authority in one capacity SHALL NOT leak into another capacity merely because the same participant identity is involved.

Responsibilities MAY be resolved where useful for:

- activity discovery;
- participant discovery;
- routing;
- coordination;
- missing-participant detection; or
- execution preparation.

Responsibility SHALL remain distinct from authority.

Participant Resolution SHALL NOT infer authority merely because a participant is responsible for, commonly performs, owns operational work for, or is associated with an activity.

---

## 10. Scope Resolution

Participant Resolution SHALL preserve the applicable scope of resolved participation and authority.

A resolved authority SHALL NOT be applied outside the scope established by its governing assignment, delegation, or other authoritative basis.

Where scope is narrower than the project as a whole, Participant Resolution SHALL preserve that narrower boundary.

Where applicable scope is unresolved and materially required for the governed activity, Participant Resolution SHALL surface the unresolved condition rather than assume project-wide scope.

Technical access extending beyond governed scope SHALL NOT broaden that governed scope.

---

## 11. Authority Resolution

Participant Resolution SHALL resolve authority only from applicable governing sources.

An Authority Binding SHALL remain traceable to an applicable governing basis where necessary to establish its validity, scope, or constraints.

The existence of an Authority Binding representation SHALL NOT by itself prove that the represented authority is valid.

Participant Resolution SHALL distinguish, where material, between authority to:

- participate;
- draft;
- recommend;
- evaluate;
- perform;
- validate;
- record;
- establish;
- authorize;
- conclude; or
- perform another governed effect established by applicable governance.

This specification does not establish a universal authority vocabulary.

Authority meaning remains governed by the applicable Engineering Platform, Engineering System, cross-system, or project-governed semantic source.

---

## 12. Project Participant Declarations

Projects use:

`<project>_home/participants/`

as the standard project-owned location for persistent Participant Declarations where such declarations are required.

The standard participant representation SHOULD maintain one persistent participant per declaration.

The standard project representation SHOULD use YAML for machine-resolved Participant Declarations.

The declaration filename SHALL NOT establish participant identity, authority, capacity, or status.

A minimal Participant Declaration SHALL be capable of representing:

- stable participant identity;
- participant type;
- applicable capacity;
- applicable scope;
- zero or more authority bindings; and
- participation status.

A declaration MAY additionally represent:

- responsibilities;
- constraints;
- external identity bindings;
- effective periods or conditions;
- delegation information;
- governing basis or provenance; and
- descriptive information.

This specification defines the semantic obligations of Participant Declarations but does not require a particular YAML schema.

---

## 13. Participant Declaration Ownership

Participant Declarations are project-owned governed configuration.

Engineering Automation consumes and resolves Participant Declarations but SHALL NOT become the semantic owner of the project participation or authority represented by them.

A Participant Declaration SHALL preserve the distinction among:

1. governing semantics that define an authority;
2. project governance or other authoritative basis that establishes an assignment or delegation;
3. the Participant Declaration that records the applicable project binding; and
4. Participant Resolution that derives applicable participant context for execution.

The intended relationship is:

**governing authority semantics → applicable project assignment or delegation → Participant Declaration → Participant Resolution → Resolved Participant Context**

No downstream stage in this relationship SHALL retroactively manufacture authority for an upstream stage.

---

## 14. Authority-Binding Validity and Self-Modification

Modification of a Participant Declaration SHALL NOT itself establish the validity of an authority binding contained within that modification.

Authority changes SHALL remain dependent upon an applicable governing basis independent of the participant's technical ability to modify the declaration representation.

Repository write access, configuration write access, source-control authorship, automation credentials, or technical ownership of a declaration SHALL NOT establish authority to grant or broaden governed authority.

Where a participant modifies its own declaration, Participant Resolution SHALL evaluate material authority claims against their governing basis in the same manner as authority claims introduced by another participant.

A participant SHALL NOT acquire governed authority merely by asserting that authority in its own declaration.

---

## 15. Delegated Authority

Participant Declarations MAY record delegated authority where such delegation is established by applicable governance.

Delegated authority SHALL remain:

- scoped;
- governed;
- traceable;
- constrained by its governing basis; and
- non-self-expanding.

Participant Resolution SHALL NOT infer broader delegation from the existence of narrower delegated authority.

Delegated authority SHALL NOT survive beyond applicable scope, conditions, or effective limits established by its governing basis.

This specification does not require a particular delegation representation or approval workflow.

---

## 16. Participation Status and Historical Resolution

Persistent Participant Declarations SHOULD support active and inactive participation status.

An inactive participant SHALL NOT be treated as currently applicable merely because its declaration remains present.

Inactive Participant Declarations MAY remain discoverable for historical reconstruction, provenance, audit, or continuity.

Status alone SHALL NOT establish or revoke the underlying meaning of historical authority.

Where effective periods or other temporal conditions exist, Participant Resolution MAY use them to determine current applicability.

This specification does not establish a richer participant lifecycle.

---

## 17. AI and Automation Participation

AI or automation does not require an independent Participant Declaration merely because it is technically involved in an activity.

Transient AI or automation assistance MAY operate as an execution mechanism supporting another governed participant where it does not independently hold persistent responsibility, scope, attributable governed participation, or delegated authority.

AI or automation SHOULD be represented as an independent Participant Declaration where it acts under one or more of the following:

- persistent project identity;
- assigned governed responsibility;
- persistent governed scope;
- independent execution of governed activities;
- attributable governed work; or
- delegated authority.

Where AI or automation acts independently as a governed participant, Participant Resolution SHALL preserve its own participant identity, scope, constraints, and authority rather than treating it as the human or system that initiated its execution.

AI or automation SHALL NOT acquire authority merely because it can technically perform an action.

---

## 18. Initiating, Executing, and Authorizing Participants

A governed activity MAY involve multiple materially distinct participant relationships.

Where applicable, Engineering Automation MAY distinguish:

- the participant initiating an activity;
- the participant executing an activity; and
- the participant authorizing a governed effect.

These relationships MAY refer to the same participant or to different participants.

Execution by one participant SHALL NOT imply that the executing participant holds authority belonging to an authorizing participant.

Initiation of an activity SHALL NOT imply authority to establish the governed outcome of that activity.

Participant Resolution SHALL preserve these distinctions where they are material to authority, provenance, governance, or execution.

This specification does not require every activity to contain all three participant relationships.

---

## 19. Cross-System Collaboration

Participant Resolution for governed cross-system collaboration SHALL preserve the capacities, scopes, responsibilities, and authorities originating from participating Engineering Systems.

Participant Resolution SHALL NOT manufacture a generic Collaboration authority by aggregating Product, Engineering, Release, or other participating authorities.

A participant's Product authority SHALL remain Product authority while participating in a Product–Engineering Collaboration activity.

A participant's Engineering authority SHALL remain Engineering authority while participating in a cross-system interaction.

Where Collaboration governance establishes a genuinely Collaboration-owned authority or collaborative determination, Participant Resolution MAY resolve that authority according to its governing basis.

Cross-system participation SHALL NOT itself transfer semantic ownership or authority between participating systems.

---

## 20. Runtime Capability Boundary

Participant Resolution does not establish or represent the complete set of runtime execution capabilities available to a participant.

Actual runtime capabilities MAY be discovered or established by execution environments, tools, integrations, credentials, agents, CLIs, CI systems, or other implementation mechanisms.

Participant Declarations MAY record governed constraints on allowable execution capabilities where applicable.

Participant Resolution SHALL preserve the distinction between:

- governed authority and scope; and
- actual technical capability.

Downstream execution preparation MAY combine:

- Resolved Participant Context;
- Resolved Activity Context;
- applicable automation constraints; and
- available runtime capabilities

to determine whether a particular action can be conformingly executed.

Technical capability SHALL NOT compensate for missing governed authority.

Governed authority SHALL NOT imply that a required technical capability is available.

---

## 21. Downstream Engineering Automation Use

Resolved Participant Context MAY be consumed by Engineering Automation mechanisms including:

- Activity Resolution;
- Context Resolution;
- Prompt Governance and Prompt Generation;
- AI Execution Composition;
- governance and validation assistance;
- execution preparation;
- execution mechanisms; and
- continuity and provenance mechanisms.

Downstream consumers SHALL preserve the authority, scope, constraints, uncertainty, and provenance of Resolved Participant Context.

A downstream representation SHALL NOT broaden participant authority merely because participant information has been transformed, summarized, composed, cached, or embedded into another execution representation.

Prompt Generation SHALL consume resolved participant context rather than independently infer participant authority from raw Participant Declarations.

---

## 22. Resolution Failure and Uncertainty

Participant Resolution SHALL preserve failure fidelity and material uncertainty.

Examples include:

- unresolved participant identity SHALL remain unresolved;
- unresolved capacity SHALL NOT be guessed where materially required;
- unresolved scope SHALL NOT be broadened to project-wide scope;
- unresolved authority SHALL NOT be inferred;
- missing governing basis for a material authority binding SHALL be surfaced;
- conflicting material authority sources SHALL be surfaced where existing governance does not establish their resolution;
- inactive participation SHALL NOT silently become active;
- failure to retrieve a Participant Declaration SHALL NOT be interpreted as evidence that the participant possesses no restrictions or broad authority.

Where required participant context cannot be resolved, downstream Engineering Automation SHALL treat the condition according to the requirements of the governed activity rather than manufacture a complete Resolved Participant Context.

---

## 23. Provenance and Continuity

Participant Resolution SHALL preserve sufficient provenance to identify the material basis for resolved participant scope and authority where required for conformance, reconstruction, validation, continuity, or governed execution.

Relevant provenance MAY include:

- participant identity basis;
- Participant Declaration identity;
- authority-binding basis;
- delegation basis;
- applicable scope;
- effective conditions;
- material governing sources; and
- resolution mechanism or version where useful.

Resolved Participant Context MAY be persisted or cached where useful.

Persisted participant context SHALL NOT be assumed current solely because it remains available.

Where material participant declarations, authority bindings, delegation, governing semantics, scope, status, or other relevant basis changes, cached or persisted participant context SHALL be reassessed before reuse where the change may affect the intended activity.

---

## 24. Validation

Participant Resolution SHALL support validation of all applicable concerns including:

- participant identity resolvability;
- declaration structural validity;
- participant type validity;
- scope resolvability;
- authority-binding basis;
- delegation constraints;
- participation status;
- material source conflicts; and
- provenance sufficiency.

Successful technical validation of a Participant Declaration SHALL NOT itself establish the validity of an authority assignment where that validity depends upon an external governing basis.

Validation execution SHALL NOT manufacture participant authority.

---

## 25. Project Representation and Portability

`<project>_home/participants/` is the standard project representation for persistent Participant Declarations.

Participant Declarations SHOULD remain project-owned and portable with the governed project context where practical.

The Platform-level Participant Resolution contract remains conceptually independent of a particular storage engine, identity provider, source-control system, or runtime environment.

An implementation MAY internally transform Participant Declarations into indexes, caches, databases, compiled representations, or other derived forms.

Such derived representations SHALL remain subordinate to the applicable project-owned declarations and governing authority sources.

---

## 26. Implementation Neutrality

This specification does not require:

- an Identity and Access Management system;
- authentication middleware;
- authorization middleware;
- Role-Based Access Control;
- Attribute-Based Access Control;
- Single Sign-On;
- an external identity provider;
- cryptographic signatures;
- participant groups;
- team inheritance;
- role inheritance;
- nested delegation;
- a participant approval workflow;
- Git branch protection;
- a participant database;
- a centralized participant service;
- a universal authority identifier namespace;
- a universal capacity vocabulary;
- a particular YAML schema;
- a particular CLI or API;
- a particular programming language;
- a particular source-resolution mechanism; or
- a particular Engineering Automation implementation.

Implementations MAY introduce such mechanisms where required provided they conform to this specification and do not redefine the governing Engineering Platform semantics.

---

## 27. Evolution and Conformance

Participant Resolution implementations MAY evolve as Engineering Automation implementation experience reveals improved mechanisms for participant representation, identity binding, authority resolution, delegation, scope resolution, validation, provenance, continuity, or runtime integration.

Implementation detail does not constitute missing Engineering Platform architecture.

Changes to Participant Resolution or its implementation SHALL conform to the closed Engineering Platform architecture and applicable Product, Collaboration, Engineering, and Release System semantics.

A proposed change requires architectural reconsideration only where it materially alters an established architectural obligation under the applicable Engineering Platform architecture-reopening criteria.

Participant Resolution SHALL remain an Engineering Automation mechanism and SHALL NOT evolve into an independent source of participant, organizational, Product, Collaboration, Engineering, or Release authority.

The governing objective remains:

> **resolve applicable participation and authority faithfully without manufacturing either.**
