# Participation & Scope Specification

## 1. Purpose

Participation & Scope establishes and exposes authoritative Engineering state describing a participant's relationship to the Engineering environment, projects, governed work, and Engineering activities.

The capability enables Engineering participation, responsibility, and scope to be determined explicitly rather than inferred from visibility, discovery, repository activity, conversational context, participant type, or other incidental signals.

Participation & Scope provides authoritative participant-relative Engineering state without independently determining governed permissibility.

---

## 2. Scope

This specification defines the required semantics and realization requirements for the Participation & Scope capability of the Engineering Platform.

Participation & Scope includes:

- participant-relative Engineering state;
- project participation;
- governed-work responsibility;
- responsibility acquisition, release, and transfer;
- participation topology;
- participation scope applicable to Engineering activity;
- participant-state changes and currency;
- participant-aware composition with other Engineering Platform capabilities.

Participation & Scope does not independently:

- establish access or visibility policy;
- establish authoritative participant identity;
- determine contextual applicability;
- compose Effective Engineering Context;
- determine governed permissibility;
- determine validation outcomes;
- own governed-work lifecycle state;
- infer participation or responsibility solely from observation, discovery, repository activity, conversational activity, or participant type.

Where participation or responsibility depends upon governed conditions or determinations owned elsewhere, Participation & Scope composes with the applicable Engineering Platform capability or governed mechanism.

---

## 3. Participation Model

### 3.1 Participation State

Participation state describes authoritative Engineering relationships between a participant and the Engineering environment, project, governed work, or Engineering activity.

Participation state may include:

- project participation;
- governed-work responsibility;
- eligibility to assume governed-work responsibility;
- participation scope applicable to an Engineering activity;
- other participant relationships established by the Engineering model.

These relationships are distinct and must not be treated as interchangeable merely because they concern the same participant or Engineering state.

### 3.2 Visibility and Participation

Visibility and participation are distinct.

Visibility of Engineering state does not establish participation.

A participant may be able to observe or discover Engineering state without participating in the project or governed work represented by that state.

Participation & Scope does not own the policy or authority establishing participant visibility.

### 3.3 Project Participation and Governed-Work Responsibility

Project participation and governed-work responsibility are distinct Engineering relationships.

Participation in a project does not, by itself, establish responsibility for governed work within that project.

Responsibility for governed work must be established through the applicable authoritative participation state or governed mechanism.

A participant may therefore participate in a project while holding responsibility for no governed work.

### 3.4 Work State and Participant Eligibility

The authoritative state of governed work and the eligibility of a participant to assume responsibility for that work are distinct.

Governed work being unassigned, unclaimed, available, or otherwise open does not, by itself, establish that a particular participant is eligible to assume responsibility for it.

Eligibility must be determined through the applicable authoritative participant state and governed mechanisms, taking into account participation topology, operating constraints, and other Engineering conditions where relevant.

### 3.5 Eligibility and Responsibility

Eligibility to assume governed-work responsibility does not itself establish that responsibility.

Responsibility exists only when it has been authoritatively established through the applicable participation or governed mechanism.

A participant may therefore be eligible for multiple items of governed work while holding responsibility for none, one, or more of them according to the applicable Engineering model.

### 3.6 Responsibility and Authority

Governed-work responsibility and Engineering authority are distinct.

Responsibility for governed work does not independently establish every action the responsible participant may perform upon that work.

Participation & Scope may expose participant relationships relevant to authority, but authoritative governed permissibility remains the responsibility of the applicable governance mechanism.

### 3.7 Participant Type

Participant type does not independently establish participation, responsibility, eligibility, authority, or governed permissibility.

Human Engineers and AI Engineers may operate under different operating constraints, but those constraints must be established through applicable authoritative Engineering state or governed rules rather than inferred solely from participant type.

---

## 4. Participant Identity

### 4.1 Identity Dependency

Participation & Scope requires a sufficiently established participant identity wherever participant-relative Engineering state is created, resolved, modified, or attributed.

Participation & Scope does not independently establish authoritative participant identity.

It consumes participant identity established by the applicable authoritative identity mechanism.

### 4.2 Identity and Participation State

Participation state must be associated with authoritative participant identity rather than inferred from incidental representations of identity.

Repository identity, execution identity, conversational identity, display name, local account, or other implementation identity must not independently establish authoritative Engineering participation unless the Engineering environment establishes that relationship.

### 4.3 Identity Continuity

Participant identity must remain sufficiently stable to preserve authoritative participation relationships across Engineering activity, interruption, resumption, and changes in interaction or execution mechanism.

Replacement of an AI execution instance or termination of a conversational session must not, by itself, create a new Engineering participant or terminate existing authoritative participation state.

Where the authoritative identity of a participant cannot be sufficiently resolved, Participation & Scope must preserve that condition rather than infer participant-relative Engineering state.

---

## 5. Project Participation

### 5.1 Purpose

Project participation establishes an authoritative Engineering relationship between a participant and a project.

Project participation defines participation in the project without, by itself, establishing governed-work responsibility, contextual applicability, authority, or governed permissibility.

### 5.2 Establishment of Project Participation

Project participation must be established through an applicable authoritative participation or governed mechanism.

Observation of a project, discovery of project state, repository access, contribution history, prior interaction, or participant presence within the Engineering environment must not independently establish project participation.

### 5.3 Participation Without Governed-Work Responsibility

A participant may participate in a project without holding responsibility for governed work.

Such participation may support Engineering activities permitted by the applicable participation model and operating constraints without requiring artificial assignment of governed work.

Participation & Scope must therefore represent project participation independently of governed-work responsibility.

### 5.4 Multiple Project Participation

A participant may participate in multiple projects where permitted by the applicable Engineering model.

Participation state for one project must not be silently applied to another project.

Project-relative participation, responsibility, eligibility, and scope must remain distinguishable where their semantics differ between projects.

### 5.5 Project Participation Changes

Project participation may be established, changed, suspended, or ended through the applicable authoritative mechanism.

Changes to project participation must not silently rewrite durable historical participation state.

Where current project participation affects Engineering activity, current authoritative participation state must be distinguishable from historical participation.

---

## 6. Governed-Work Responsibility

### 6.1 Purpose

Governed-work responsibility establishes which participant is authoritatively responsible for realization of governed work where such responsibility is required by the Engineering model.

Responsibility is explicit Engineering state.

It must not be inferred solely from repository activity, implementation changes, conversational activity, prior interaction, visibility, project participation, or apparent work availability.

### 6.2 Responsibility Relationship

Governed-work responsibility must identify, directly or through authoritative relationships:

- the participant holding responsibility;
- the governed work for which responsibility is held;
- the applicable responsibility relationship;
- the current authoritative state of that relationship.

Where the Engineering model permits multiple forms of responsibility, materially different responsibility semantics must remain distinguishable.

### 6.3 Responsibility Cardinality

The number of governed-work responsibilities a participant may hold is determined by the applicable Engineering model, participation topology, operating constraints, and governed mechanisms.

Participation & Scope must not assume that a participant may hold responsibility for only one item of governed work at a time.

It must likewise not assume that eligibility for multiple items of governed work permits simultaneous responsibility for all of them.

### 6.4 Responsibility and Governed-Work Lifecycle

Governed-work responsibility and governed-work lifecycle state are distinct.

A lifecycle transition may affect whether responsibility can be established, retained, released, or transferred, but Participation & Scope does not independently own governed-work lifecycle state.

Similarly, a change in responsibility must not silently imply a governed-work lifecycle transition unless the applicable Engineering model establishes that relationship.

### 6.5 Responsibility and Execution

Execution or realization activity does not independently establish governed-work responsibility.

A participant performing implementation activity associated with governed work must not be treated as its responsible participant unless authoritative participation state establishes that responsibility.

Where the Engineering model requires responsibility before particular Engineering activity may occur, the applicable authoritative responsibility must be resolvable before that activity proceeds.

---

## 7. Responsibility Acquisition

### 7.1 Purpose

Responsibility Acquisition establishes governed-work responsibility for a participant through an applicable authoritative participation or governed mechanism.

Responsibility may be acquired through mechanisms such as assignment, self-assumption, or other forms established by the Engineering model.

The realization mechanism must preserve the same authoritative responsibility semantics regardless of how acquisition is initiated.

### 7.2 Acquisition Preconditions

Governed work being unassigned, unclaimed, available, or otherwise open is not sufficient by itself to establish responsibility.

Responsibility acquisition must occur only where the applicable authoritative participant state, eligibility determination, participation topology, operating constraints, governed-work state, and governed conditions permit the acquisition.

Participation & Scope must not manufacture eligibility or permissibility merely because responsibility acquisition has been requested.

### 7.3 Self-Assumption of Responsibility

Where the applicable Engineering model permits a participant to assume responsibility without assignment by another participant, self-assumption may establish responsibility through the applicable authoritative mechanism.

Self-assumption is not a universal entitlement of either Human Engineers or AI Engineers.

Whether it is permitted depends upon the applicable participant state, participation topology, operating constraints, governed-work state, and governed conditions.

### 7.4 Assignment

Where responsibility is assigned to a participant, the assignment must result in authoritative responsibility state through the applicable participation or governed mechanism.

An instruction, message, conversation, planning statement, or other communication does not independently establish authoritative governed-work responsibility unless the Engineering environment recognizes that mechanism as authoritative.

### 7.5 Acquisition Atomicity

Responsibility acquisition must not produce an authoritative state in which mutually incompatible responsibility relationships are simultaneously established merely because multiple participants attempt to acquire the same governed work.

Where responsibility acquisition is exclusive, the realization must preserve that exclusivity across concurrent acquisition attempts.

An unsuccessful acquisition attempt must not create partial or implied responsibility.

### 7.6 Acquisition Result

Successful responsibility acquisition must produce authoritative participation state that can be resolved by other Engineering Platform capabilities.

The resulting responsibility must not depend upon participant memory, conversational continuity, or ephemeral execution state for its continued authority.

---

## 8. Responsibility Release & Transfer

### 8.1 Responsibility Release

Governed-work responsibility may be released through the applicable authoritative participation or governed mechanism where the Engineering model permits release.

Release ends the applicable current responsibility relationship.

It must not erase durable historical state establishing that the participant previously held responsibility.

### 8.2 Release Preconditions

A participant's desire to stop Engineering activity does not independently release authoritative responsibility.

Where release is subject to governed conditions, those conditions must be satisfied through the applicable governed mechanism.

Interruption, disconnection, inactivity, session termination, or AI execution-instance termination must not silently release responsibility unless the Engineering model explicitly establishes that semantic.

### 8.3 Responsibility Transfer

Where responsibility may move from one participant to another, transfer must preserve an authoritative and durable transition between the prior and succeeding responsibility relationships.

Transfer must not rely upon informal handover alone to establish the succeeding participant's responsibility.

Where applicable, the transfer mechanism must preserve sufficient state to identify the governed work, prior responsible participant, succeeding responsible participant, and authoritative transition.

### 8.4 Transfer and Context

Transfer of governed-work responsibility may affect the Effective Engineering Context required by the succeeding participant.

Participation & Scope establishes the responsibility transition.

Context Resolution & Composition remains responsible for resolving and composing the applicable Effective Engineering Context for the succeeding Engineering activity.

### 8.5 Abandoned or Unavailable Participants

Participant unavailability does not independently determine the disposition of governed-work responsibility.

Where a responsible participant becomes unavailable, the applicable Engineering model or governed mechanism determines whether responsibility is retained, released, transferred, escalated, or otherwise resolved.

Participation & Scope must preserve the authoritative responsibility state until that determination is established.

---

## 9. Participation Topology

### 9.1 Purpose

Participation topology describes the authoritative participant arrangement relevant to a project, governed work, or Engineering activity where that arrangement affects participation, responsibility, eligibility, or responsibility acquisition.

Participation topology allows participation rules to account for the Engineering environment in which participants operate without encoding universal assumptions about team size or participant type.

### 9.2 Topology as Engineering State

Where participation topology materially affects participant-relative determinations, it must be established or deterministically resolvable from authoritative Engineering state.

Participation & Scope must not infer topology solely from currently observed activity, repository contributors, active sessions, conversational participants, or other incidental signals.

### 9.3 Single-Participant Topology

A project or applicable participation scope may have a topology in which one Engineer is the sole participating Engineer relevant to applicable governed work.

Where the Engineering model permits it, such a topology may allow that Engineer to assume responsibility for multiple available items of governed work without coordination with another Engineer.

The existence of a single-participant topology does not itself establish eligibility and does not remove applicable governed conditions, operating constraints, lifecycle requirements, or responsibility semantics.

### 9.4 Multi-Participant Topology

Where multiple participants may hold or acquire governed-work responsibility, the applicable Engineering model may require coordination, allocation, exclusivity, authority, governance, or other conditions that are unnecessary in a single-participant topology.

Participation & Scope must preserve those topology-dependent distinctions.

It must not assume that a responsibility-acquisition rule valid for a single-participant topology remains valid when additional participants are present.

### 9.5 Topology Changes

Participation topology may change over time.

A change in topology may affect future eligibility, responsibility acquisition, participation scope, or applicable governed conditions.

A topology change must not silently invalidate, create, or transfer existing governed-work responsibility unless the applicable Engineering model establishes that consequence.

Where topology-dependent participant state is relied upon for Engineering action, sufficiently current authoritative topology must be resolved.

---

## 10. Participation Scope & Engineering Activity

### 10.1 Participation Scope

Participation scope describes the authoritative participant-relative boundary within which an Engineer participates in an Engineering activity.

Participation scope may be established through relationships to a project, governed work, responsibility, Engineering activity, or other authoritative Engineering state.

Participation scope is distinct from visibility, contextual applicability, authority, and governed permissibility.

### 10.2 Activity-Specific Participation

A participant's Engineering participation may differ across Engineering activities involving the same project or governed work.

Participation & Scope must therefore support participant-relative state appropriate to the Engineering activity rather than assuming that one participation relationship grants undifferentiated participation across all Engineering activities.

Applicable Engineering activities may include realization, peer review, validation, handover, or other activities established by the Engineering model.

### 10.3 Responsibility and Realization

Where the Engineering model requires governed-work responsibility for realization, only a participant holding the applicable authoritative responsibility may proceed as the responsible realization participant.

Other visible or participating Engineers do not acquire realization responsibility merely by observing, assisting, discussing, or inspecting the governed work.

Where collaboration is permitted, collaboration must not obscure which participant holds authoritative governed-work responsibility.

### 10.4 Independent Participation Responsibilities

Engineering activities requiring independence must preserve distinct participant responsibilities where established by the Engineering model.

For example, participation in peer review or validation must not be silently derived from realization responsibility where the applicable Engineering model requires independent participation.

Participation & Scope must preserve materially different activity responsibilities rather than flattening them into generic project participation.

### 10.5 Activity Completion and Participation State

Completion of an Engineering activity does not automatically terminate project participation or other participation relationships.

Similarly, completion or transition of governed work does not automatically erase responsibility history.

Changes to current participation state must occur according to the applicable authoritative participation or governed mechanism.

---

## 11. Human and AI Engineers

### 11.1 Common Participation Semantics

Human Engineers and AI Engineers participate through the same authoritative Participation & Scope semantics.

Participant type must not create separate meanings for project participation, governed-work responsibility, eligibility, responsibility acquisition, release, transfer, or participation scope.

### 11.2 Participant Operating Constraints

Participant Operating Constraints are authoritative constraints governing how a participant may participate in or perform applicable Engineering activity.

Participant Operating Constraints may be established by applicable authoritative Engineering capabilities, Engineering Systems, Development Standards, projects, governance mechanisms, or other authoritative Engineering mechanisms according to the Engineering concern from which the constraint arises.

Participation & Scope does not become the universal authoritative source of Participant Operating Constraints merely because those constraints affect participant-relative Engineering state.

Participation & Scope consumes and applies applicable Participant Operating Constraints where they affect participation eligibility, governed-work responsibility, responsibility acquisition, responsibility release or transfer, activity participation, concurrency, escalation, or other participant-relative Engineering state or determinations owned by this capability.

The authoritative mechanism establishing a Participant Operating Constraint retains responsibility for the meaning and normative force of that constraint.

Human Engineers and AI Engineers may be subject to different Participant Operating Constraints without creating different underlying Engineering truth.

### 11.3 AI Engineer Realization Responsibility

Where an AI Engineer holds responsibility for realization of governed work, the AI Engineer must perform that realization within its applicable operating constraints.

The AI Engineer must not independently delegate or transfer its realization responsibility to another AI Engineer unless the applicable Engineering model explicitly permits such delegation or transfer.

Where required Human Engineer input, authority, clarification, or governed intervention prevents autonomous continuation, the AI Engineer may escalate through the applicable Engineering Platform mechanism without relinquishing responsibility unless an authoritative responsibility change is established.

### 11.4 AI Execution-Instance Replacement

Replacement, restart, or loss of an AI execution instance does not independently create, release, or transfer governed-work responsibility.

A succeeding execution instance acting for the same authoritative AI Engineer must resolve current authoritative participation and responsibility state rather than infer it from prior conversational context.

Where the authoritative AI Engineer identity itself changes, applicable responsibility transfer or acquisition semantics must be followed.

### 11.5 Human Engineer Continuity

Human Engineer participation and responsibility likewise do not depend upon continuous session presence, repository activity, or conversational continuity.

Interruption or inactivity does not independently alter authoritative participation state.

Human Engineers and AI Engineers therefore share the same durable participation semantics even where their execution and interaction models differ.

---

## 12. Participant State Currency

### 12.1 Current and Historical Participant State

Participation & Scope must preserve the distinction between current and historical participant state.

Historical participation, responsibility, eligibility, topology, or activity scope must not be represented as current solely because it is durably preserved.

### 12.2 Participant-State Changes

Changes to participant state must occur through applicable authoritative participation or governed mechanisms.

Material changes may include:

- project participation beginning or ending;
- governed-work responsibility being acquired, released, or transferred;
- eligibility changing;
- participation topology changing;
- activity-specific participation changing;
- participant operating constraints changing.

Participation & Scope must expose sufficiently current authoritative state for participant-relative Engineering determinations.

### 12.3 Stale Participant State

Derived, cached, conversational, or previously resolved participant state may become stale.

Where participant state may materially affect responsibility acquisition, Engineering activity, authority, governance, or another participant-relative determination, the realization must provide a means to resolve sufficiently current authoritative participant state before reliance upon the stale representation.

A prior determination must not preserve participation, responsibility, eligibility, or scope that is no longer authoritative.

### 12.4 Durable Participant State

Authoritative participation and responsibility state required for Engineering continuity must not depend solely upon participant memory, conversational continuity, active sessions, or ephemeral execution state.

Durable historical participant state must remain available to the applicable Continuity & Provenance mechanisms where required by the Engineering model.

### 12.5 Participant-State Conflict

Where participant state is conflicting, ambiguous, or cannot be authoritatively resolved, Participation & Scope must preserve that condition.

It must not select or manufacture participant state merely to allow Engineering activity to continue.

Where resolution requires governance or another authoritative mechanism, the applicable mechanism must establish the resulting state.

---

## 13. Capability Integrations

### 13.1 Discovery & Navigation

Participation & Scope provides authoritative participant-relative Engineering state required by Discovery & Navigation for participant-aware discovery.

Such state may include:

- project participation;
- governed-work responsibility;
- eligibility to assume governed-work responsibility;
- activity-specific participation scope;
- other participant relationships owned by Participation & Scope.

Discovery & Navigation may expose and navigate this state but does not independently establish or modify it.

Visibility and discoverability remain distinct from participation, responsibility, and eligibility.

### 13.2 Context Resolution & Composition

Participation & Scope provides authoritative participant-relative state that may contribute to Context Resolution & Composition.

Project participation, governed-work responsibility, and activity-specific participation may affect which Engineering context must be resolved for a participant's current Engineering activity.

Participation & Scope does not independently determine contextual applicability or compose Effective Engineering Context.

A change in participation or responsibility may require Effective Engineering Context to be resolved again, but Context Resolution & Composition remains responsible for that determination and composition.

### 13.3 Governance & Validation Integration

Participation & Scope may depend upon governed determinations when establishing, changing, releasing, or transferring participant relationships.

Governance & Validation Integration or the applicable governed mechanism remains responsible for governed permissibility and validation determinations it owns.

Participation & Scope must not convert eligibility, responsibility, absence of prohibition, or participant intent into governed permission where the applicable Engineering model requires a separate governed determination.

Where governance establishes a participant-relative determination requiring a change to authoritative participation state, Participation & Scope must establish or modify the resulting participant relationship through the applicable authoritative participation mechanism.

### 13.4 Continuity & Provenance

Participation & Scope provides current authoritative participant state and contributes durable participation-state changes required for Engineering continuity and provenance.

Continuity & Provenance remains responsible for preserving durable Engineering history and provenance.

Historical participation state must remain distinguishable from current authoritative participation state.

Replacement of an execution instance, interruption of Engineering activity, or loss of conversational continuity must not require reconstruction of authoritative participation state from participant memory.

### 13.5 Execution Enablement

Participation & Scope provides authoritative participant, project participation, governed-work responsibility, and other applicable participant-relative Engineering state required by Execution Enablement.

Execution Enablement consumes that state when resolving and enabling applicable Engineering execution but does not independently establish participation, responsibility, eligibility, or participant authority.

Participation & Scope may apply Participant Operating Constraints to participant-relative Engineering state and determinations it owns.

Execution Enablement remains responsible for enforcing applicable Participant Operating Constraints within the execution surfaces it provides or controls, without assuming authoritative ownership of the constraints themselves.

Execution activity, tool access, successful execution, Engineering Automation invocation, Execution Instance existence, or execution resumption does not independently create, transfer, release, or otherwise modify authoritative participation, responsibility, or authority.

### 13.6 Governed-Work Lifecycle

Participation & Scope composes with the authoritative mechanism owning governed-work lifecycle state where participation or responsibility depends upon that state.

Governed-work lifecycle state may constrain responsibility acquisition, retention, release, transfer, or activity-specific participation.

Participation & Scope does not independently create or transition governed-work lifecycle state.

Changes in lifecycle state and changes in participant state must remain semantically distinguishable unless the Engineering model explicitly establishes a relationship between them.

### 13.7 Cross-Capability Composition

Participation & Scope may compose with multiple Engineering Platform capabilities where a participant-relative determination depends upon state or determinations owned across capability boundaries.

Such composition does not transfer authoritative ownership.

Participation & Scope must preserve the authority and semantics of state or determinations obtained from other capabilities or governed mechanisms.

---

## 14. Capability Boundaries

Participation & Scope is responsible for establishing, maintaining, and exposing authoritative participant-relative Engineering state within the boundaries defined by the Engineering model.

Participation & Scope does not independently:

- establish access or visibility policy;
- establish authoritative participant identity;
- create or modify governed-work lifecycle state;
- determine contextual applicability;
- compose Effective Engineering Context;
- determine governed permissibility;
- determine validation outcomes;
- create Engineering authority not established by the applicable Engineering model;
- infer project participation from visibility, discovery, repository access, contribution history, or participant presence;
- infer governed-work responsibility from implementation activity, conversation, prior interaction, project participation, or apparent work availability;
- infer eligibility solely from governed work being unassigned, unclaimed, available, or otherwise open;
- treat participant type as an implicit participation, responsibility, eligibility, authority, or permission model;
- treat session continuity, execution-instance continuity, or participant activity as authoritative participation state;
- erase or rewrite durable historical participation state when current participation state changes.

Where participant-relative state depends upon a determination owned elsewhere, Participation & Scope must obtain or consume that determination through the applicable authoritative capability or governed mechanism rather than assume ownership of it.

---

## 15. Realization Requirements

A realization of Participation & Scope must satisfy the following requirements.

### PS-R01 — Authoritative Participant Identity

The realization must associate participant-relative Engineering state with sufficiently established authoritative participant identity.

Incidental identity representations must not independently establish authoritative participation state unless the Engineering environment explicitly establishes that relationship.

### PS-R02 — Distinct Participation Relationships

The realization must preserve materially distinct semantics for project participation, governed-work responsibility, eligibility to assume responsibility, activity-specific participation scope, and other participant relationships established by the Engineering model.

These relationships must not be silently treated as interchangeable.

### PS-R03 — Project Participation

The realization must support authoritative establishment, resolution, change, suspension, and termination of project participation independently of governed-work responsibility.

Historical project participation must remain distinguishable from current participation.

### PS-R04 — Governed-Work Responsibility

The realization must support authoritative establishment and resolution of governed-work responsibility without inferring responsibility from visibility, project participation, implementation activity, conversational activity, prior interaction, or apparent work availability.

### PS-R05 — Responsibility Acquisition

The realization must support responsibility acquisition through the applicable mechanisms established by the Engineering model, including assignment, self-assumption, or other permitted forms where applicable.

Acquisition must occur only where the applicable authoritative participant state, eligibility determination, participation topology, operating constraints, governed-work state, and governed conditions permit it.

### PS-R06 — Acquisition Exclusivity

Where governed-work responsibility is exclusive, the realization must preserve that exclusivity across concurrent responsibility-acquisition attempts.

An unsuccessful acquisition attempt must not create partial, implied, or competing authoritative responsibility.

### PS-R07 — Responsibility Release

The realization must support authoritative responsibility release where permitted by the Engineering model.

Interruption, inactivity, disconnection, session termination, or execution-instance termination must not independently release responsibility unless the Engineering model explicitly establishes that semantic.

### PS-R08 — Responsibility Transfer

Where responsibility transfer is permitted, the realization must preserve an authoritative transition from the prior responsibility relationship to the succeeding responsibility relationship without relying upon informal handover as the source of authority.

### PS-R09 — Participation Topology

Where participation topology materially affects participant-relative determinations, the realization must establish or deterministically resolve sufficiently current authoritative topology.

Topology must not be inferred solely from observed activity, repository contributors, active sessions, conversational participants, or similar incidental signals.

### PS-R10 — Topology-Dependent Participation

The realization must support participation and responsibility semantics that may vary according to authoritative participation topology without encoding universal assumptions about team size or participant type.

A topology change must not silently create, invalidate, release, or transfer existing governed-work responsibility unless the Engineering model establishes that consequence.

### PS-R11 — Activity-Specific Participation

The realization must support materially distinct participation responsibilities for Engineering activities where required by the Engineering model.

Project participation or governed-work realization responsibility must not silently establish participation responsibility for peer review, validation, or other independent Engineering activities.

### PS-R12 — Human and AI Engineer Semantics

The realization must preserve common authoritative Participation & Scope semantics for Human Engineers and AI Engineers while supporting different authoritative operating constraints where established by the Engineering model.

Participant type alone must not establish participation, responsibility, eligibility, authority, or governed permissibility.

### PS-R13 — AI Engineer Realization Responsibility

Where an AI Engineer holds governed-work realization responsibility, the realization must preserve that responsibility while the AI Engineer performs the realization within its applicable operating constraints.

Responsibility must not be independently delegated or transferred to another AI Engineer unless the applicable Engineering model explicitly permits it.

Escalation for required Human Engineer input, authority, clarification, or governed intervention must not itself transfer or release responsibility.

### PS-R14 — Execution and Session Independence

Authoritative participation and responsibility state must not depend upon continuous participant sessions, conversational continuity, repository activity, or ephemeral execution state.

Replacement or restart of an AI execution instance acting for the same authoritative AI Engineer must not independently create, release, or transfer responsibility.

### PS-R15 — Participant-State Currency

The realization must preserve the distinction between current and historical participant state and provide sufficiently current authoritative state where participant-relative Engineering determinations depend upon it.

Previously resolved, cached, derived, or conversational participant state must not preserve relationships that are no longer authoritative.

### PS-R16 — Participant-State Conflict

Where authoritative participant state is conflicting, ambiguous, or cannot be sufficiently resolved, the realization must preserve that condition rather than manufacture participant state to permit Engineering activity to continue.

### PS-R17 — Durable Participation State

Authoritative participation and responsibility state required for Engineering continuity must be durably representable and resolvable independently of participant memory, conversational continuity, or ephemeral execution state.

Historical participant-state changes must remain available to the applicable Continuity & Provenance mechanisms where required by the Engineering model.

### PS-R18 — Capability Ownership

Where participation or responsibility depends upon state or a determination owned by another Engineering Platform capability or governed mechanism, the realization must consume that authoritative state or determination while preserving its ownership and semantics.

Participation & Scope must not assume authority for the determination merely because it uses the result to establish or expose participant-relative state.

---

## 16. Invariants

The following invariants must hold for every conforming realization of Participation & Scope.

1. **Visibility does not establish participation.**  
   Observation, discovery, access, or visibility of Engineering state does not independently establish project participation or governed-work responsibility.

2. **Participation does not establish responsibility.**  
   Project participation does not independently establish responsibility for governed work within that project.

3. **Work availability does not establish eligibility.**  
   Governed work being unassigned, unclaimed, available, or otherwise open does not independently establish that a particular participant may assume responsibility for it.

4. **Eligibility does not establish responsibility.**  
   Eligibility to assume governed-work responsibility does not itself create that responsibility.

5. **Responsibility does not establish governed permissibility.**  
   Holding governed-work responsibility does not independently authorize every Engineering action upon that work.

6. **Participant type does not establish participant state.**  
   Human Engineer or AI Engineer classification does not independently establish participation, responsibility, eligibility, authority, or governed permissibility.

7. **Participation state is explicit and authoritative.**  
   Authoritative participant relationships are established through applicable Engineering Platform or governed mechanisms rather than inferred from incidental participant behavior or implementation signals.

8. **Participation state survives execution discontinuity.**  
   Interruption, session termination, conversational discontinuity, inactivity, or AI execution-instance replacement does not independently create, release, or transfer authoritative participation or responsibility state.

9. **Responsibility transitions are authoritative.**  
   Acquisition, release, and transfer of governed-work responsibility occur through applicable authoritative mechanisms and preserve materially significant current and historical state.

10. **Activity responsibilities remain distinguishable.**  
    Realization responsibility, peer-review participation, validation participation, and other materially distinct Engineering activity responsibilities must not be silently collapsed into generic project participation.

11. **Topology influences participation without replacing governance.**  
    Participation topology may affect eligibility, responsibility acquisition, or participation scope, but topology alone does not remove applicable operating constraints, governed conditions, or responsibility semantics.

12. **Capability composition does not transfer authority.**  
    Participation & Scope may consume state and determinations owned by other Engineering Platform capabilities or governed mechanisms, but authoritative ownership remains with the capability or mechanism that establishes them.
