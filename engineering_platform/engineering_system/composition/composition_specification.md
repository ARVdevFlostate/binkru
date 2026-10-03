# Engineering Composition Specification

## 1. Purpose

This specification defines the canonical Engineering System semantics
for controlled composition of derived Engineering artifacts from
governed sources, project-owned knowledge, reusable assets, and
applicable context.

It establishes:

-   what Engineering Composition is and is not;
-   the authority boundary between composition and governance;
-   composition inputs and their authority;
-   conflict and precedence handling;
-   specialization rules;
-   deterministic and AI-assisted composition;
-   validation, failure, and output semantics;
-   provenance and Composition Reports;
-   derived-artifact authority;
-   human, AI, automated, and mixed-team participation; and
-   implementation conformance.

This specification governs composition semantics.

It SHALL NOT require a particular composition engine, manifest format,
repository layout, prompt framework, AI model, or implementation
product.

Conforming implementations MAY realize these semantics but are not part of the canonical Engineering System model.

## 2. Core Principle

Engineering Composition is the controlled derivation of a target
Engineering artifact from authoritative and explicitly permitted inputs.

Composition:

    governed sources
        +
    project-owned knowledge
        +
    reusable assets
        +
    applicable context
        ↓
    controlled derivation
        ↓
    validated derived artifact
        +
    composition provenance

Composition is not unrestricted content generation.

Composition SHALL preserve authority boundaries, source provenance,
material constraints, and traceability.

A composed artifact SHALL NOT acquire greater authority than the sources
and governance that permit its creation.

## 3. Canonical Capability and Implementation Boundary

Composition is a canonical Engineering System capability because
Engineering artifacts MAY need to be derived consistently from governed
Engineering knowledge.

The Engineering System owns:

-   composition semantics;
-   authority rules;
-   lifecycle and artifact constraints applicable to composition;
-   validation expectations;
-   provenance expectations; and
-   reusable Development Standards where such standards are governed by
    the Engineering System.

An implementation owns operational mechanics such as:

-   manifest or request parsing;
-   source loading;
-   registry lookup;
-   deterministic transformation;
-   AI-assisted interpretation;
-   schema validation;
-   output generation;
-   atomic writes;
-   reporting; and
-   tool-specific workflow integration.

An implementation SHALL NOT redefine canonical Engineering governance
merely because it performs composition.

## 4. Composition Roles

### 4.1 Engineering System

The Engineering System establishes the canonical governance, lifecycle,
artifact, authority, standards, and composition semantics applicable to
Engineering work.

### 4.2 Project or Governed Engineering Context

The project or applicable governed Engineering context owns
project-specific facts and governed records, which MAY include:

-   purpose and scope;
-   architecture context;
-   repository structure;
-   technology declarations;
-   project-specific standards;
-   approved exceptions;
-   Engineering Delivery Proposals;
-   Engineering Delivery Plans;
-   Engineering Slices;
-   Architecture Decision Records;
-   Engineering Evidence;
-   Engineering Delivery Records; and
-   other applicable governed objects.

### 4.3 Reusable Asset Source

A reusable asset source MAY provide templates, schemas, prompts,
patterns, examples, mappings, or other reusable material.

A reusable asset SHALL NOT be assumed to be authoritative Engineering
governance merely because it is reusable.

### 4.4 Composer

The Composer is the human, AI, automated system, mixed team, or tool
performing the composition operation.

The Composer owns the execution of the composition operation.

The Composer does not inherently own:

-   Engineering governance;
-   project facts;
-   Architecture Decision Authority;
-   investment authority;
-   execution authority;
-   Engineering Conclusion authority;
-   EDR finalization authority; or
-   Release authority.

Capability to compose SHALL NOT imply authority over the composed
subject matter.

## 5. Composition Target

A Composition Target is the Engineering artifact intended to be produced
through composition.

A target SHALL have a known semantic type or explicit target contract.

Targets MAY include:

-   project-specific Engineering prompts;
-   derived instructions;
-   configured templates;
-   generated Engineering views;
-   context packages;
-   validation inputs;
-   implementation guidance;
-   governed summaries where derivation is permitted; or
-   other derived Engineering artifacts.

Composition SHALL NOT be used to bypass the canonical creation,
decision, approval, acceptance, or finalization semantics of a governed
record.

Where an artifact type has its own canonical specification, template,
checklist, lifecycle, or authority model, composition SHALL conform to
that model.

## 6. Composition Request

A composition operation SHALL have an explicit Composition Request.

The request MAY be represented by:

-   a manifest;
-   structured API request;
-   workflow object;
-   command invocation;
-   governed configuration;
-   human instruction; or
-   another unambiguous representation.

The Composition Request SHOULD identify, as applicable:

-   request or composition identity;
-   target artifact type;
-   reusable source or template;
-   required inputs;
-   optional inputs;
-   intended consumer;
-   permitted configuration;
-   requested output location or destination;
-   overwrite policy;
-   validation profile; and
-   provenance requirements.

A Composition Request describes what is to be composed.

A Composition Request is an operational invocation concept, not a
canonical governed Engineering record unless another applicable
specification explicitly establishes its representation as such.

It SHALL NOT redefine mandatory Engineering governance or grant
authority that the requester does not possess.

## 7. Composition Inputs

Composition inputs MAY include:

-   Composition Request;
-   reusable source artifact or template;
-   applicable Engineering System specifications;
-   applicable Development Standards;
-   project-owned context;
-   project-specific standards;
-   technology declarations;
-   governed Engineering records;
-   Engineering Evidence;
-   explicitly permitted workflow or lifecycle state;
-   approved exceptions;
-   prior composition outputs where explicitly allowed; and
-   other authoritative or permitted sources.

Each input SHOULD have sufficient identity, authority, revision, and
provenance information for the composition operation.

The Composer SHALL distinguish authoritative inputs from advisory,
generated, inferred, or defaulted inputs.

## 8. Source Authority

Composition SHALL reason about authority, not merely file presence.

An input MAY be:

-   authoritative for a particular concern;
-   approved but scoped;
-   advisory;
-   reusable but non-authoritative;
-   generated/derived;
-   inferred;
-   defaulted; or
-   unresolved.

Authority SHALL be evaluated for the concern being composed.

For example, an Accepted ADR MAY be authoritative for an architecture
decision within its scope while an Engineering Delivery Plan MAY be
authoritative for an authorized execution basis within its applicable
scope.

One artifact's authority SHALL NOT be generalized beyond its governed
concern.

## 9. Precedence and Conflict Resolution

Composition SHALL NOT rely on one universal hard-coded precedence list
for all Engineering concerns.

Where multiple sources address the same concern, precedence SHALL be
determined by applicable authority, scope, lifecycle state, effective
point, explicit governance, and any applicable law, regulation, or
contractual obligation.

The Composer SHALL:

1.  identify the concern in conflict;
2.  determine the applicable authority domain;
3.  evaluate source scope and state;
4.  determine whether an authorized exception or supersession applies;
5.  apply the authoritative source where precedence is determinable; and
6.  surface the conflict where authority cannot be determined safely.

A lower-authority source SHALL NOT silently override a higher-authority
source for the same governed concern.

A more recent source SHALL NOT automatically override an older
authoritative source unless applicable governance establishes that
effect.

Where a material conflict remains unresolved, composition SHALL fail or
return an explicit unresolved-conflict result rather than invent a
resolution.

## 10. Development Standards Resolution

Where the target requires reusable Development Standards, the Composer
SHALL resolve standards from explicit project declarations and governed
mappings.

A project MAY declare relevant technologies through a Technology Profile
or equivalent project-owned representation.

A standards resolution mechanism MAY use:

-   explicit registry;
-   naming convention;
-   structured mapping;
-   schema relationship;
-   governed capability mapping; or
-   another deterministic mechanism.

A declared technology without a reusable Engineering standard is not
automatically invalid.

Where no reusable standard exists, the Composer SHALL:

-   record that no reusable standard was resolved;
-   apply applicable Engineering governance;
-   apply valid project-specific standards where available; and
-   fail only where the target requires a standard that cannot be
    supplied.

An approved scoped exception MAY override an Engineering standard within
the authority of that exception.

An unapproved weakening SHALL be rejected.

## 11. Project-owned Knowledge

Project-owned knowledge MAY supply facts needed to specialize the
target.

Examples include:

-   project purpose;
-   domain context;
-   repository and module structure;
-   stakeholders;
-   constraints;
-   environments;
-   architecture boundaries;
-   technology declarations;
-   applicable Development Standards;
-   delivery context; and
-   other project facts.

The Composer SHALL NOT invent missing project facts.

Where a material fact is unavailable, the Composer SHALL either:

-   leave the matter explicitly unresolved where the target permits;
-   request or obtain an authoritative source through the applicable
    workflow; or
-   fail composition where safe composition requires the fact.

Assumptions SHALL NOT be silently converted into facts.

## 12. Governed Engineering Records as Inputs

Governed Engineering records MAY be used as composition inputs according
to their state, scope, and authority.

Examples include:

-   Engineering Delivery Proposal;
-   Approved Investment Baseline;
-   Engineering Delivery Plan;
-   Execution Baseline;
-   Engineering Slice;
-   Architecture Decision Record;
-   Engineering Evidence;
-   Engineering Delivery Record; and
-   applicable future Engineering records.

The Composer SHALL interpret each record according to its canonical
semantics.

Examples:

-   a Draft ADR SHALL NOT be treated as authoritative architecture;
-   an Accepted ADR MAY be authoritative only for its governed
    architecture scope;
-   a Rejected ADR MAY provide historical knowledge but SHALL NOT
    constrain current architecture;
-   an EDR MAY provide material realization history but SHALL NOT
    replace the ADR's architecture reasoning; and
-   an Execution Baseline SHALL NOT be silently revised by a composed
    derivative artifact.

## 13. Mandatory Composition Behaviour

A conforming composition operation SHALL, proportionate to target
significance:

1.  identify the Composition Request;
2.  validate the requested target type or contract;
3.  resolve required inputs;
4.  establish input identity and authority where material;
5.  apply applicable Engineering System semantics;
6.  resolve applicable Development Standards;
7.  distinguish authoritative content from generated specialization;
8.  preserve mandatory target behaviour;
9.  avoid inventing project facts, evidence, authority, decisions, or
    lifecycle state;
10. detect material conflicts;
11. preserve unresolved material uncertainty;
12. validate the composed output;
13. produce sufficient composition provenance;
14. prevent unauthorized replacement or override; and
15. fail clearly where safe composition is not possible.

## 14. Non-configurable Behaviour

A Composition Request SHALL NOT disable mandatory behaviour including:

-   applicable governance;
-   required-input validation;
-   authority evaluation;
-   material conflict detection;
-   mandatory target-contract preservation;
-   provenance;
-   output validation;
-   protection against unsupported project facts;
-   protection against invented Engineering Evidence;
-   protection against invented authority or decision outcomes;
-   protection against unauthorized overrides; and
-   failure on unresolved critical errors.

Configuration attempting to disable mandatory behaviour is invalid.

## 15. Permitted Configuration

Composition MAY permit non-governance configuration such as:

-   output destination;
-   optional input inclusion;
-   composition identifier;
-   report destination;
-   replacement policy;
-   reference inclusion;
-   formatting profile;
-   verbosity profile;
-   optional target sections;
-   deterministic or AI-assisted execution preference where supported;
    and
-   other target-specific presentation or execution options.

Permitted configuration SHALL remain within the target contract and
applicable authority.

## 16. Specialization Rules

The Composer MAY, where permitted:

-   resolve placeholders;
-   insert grounded project facts;
-   apply project constraints;
-   insert applicable Development Standards;
-   reference governed Engineering records;
-   omit explicitly optional and irrelevant sections;
-   expand generic instructions into project-specific instructions;
-   generate target-specific structure;
-   add provenance metadata; and
-   produce derived views from authoritative sources.

The Composer SHALL NOT:

-   remove mandatory responsibilities;
-   weaken required validation;
-   alter canonical Engineering lifecycle semantics;
-   alter canonical artifact semantics;
-   change approved scope without applicable authority;
-   contradict authoritative sources;
-   convert assumptions into facts;
-   introduce unsupported technologies as project facts;
-   invent repository paths, interfaces, dependencies, evidence,
    authority, approvals, decisions, or state;
-   silently resolve material conflicts;
-   rewrite historical records to reflect current truth; or
-   treat a generated derivative as a new source of governance merely
    because it was composed.

## 17. Derived Artifact Authority

A composed artifact is a Derived Engineering Artifact unless the
canonical specification for its target type establishes another semantic
class.

Composition SHALL NOT independently make a derivative artifact:

-   approved;
-   accepted;
-   authorized;
-   authoritative;
-   an Engineering Conclusion;
-   an Architecture Decision;
-   an Execution Baseline;
-   a finalized EDR; or
-   a Release authorization.

If the target is a governed record, composition MAY create or populate
the record only to the state permitted by applicable governance.

For example:

    compose ADR content
        ↓
    ADR may become Draft
        ↓
    applicable validation / review / authority
        ↓
    Architecture Decision
        ↓
    Accepted only through Approve

The Composer SHALL NOT collapse artifact creation and governance
authority into one operation unless explicit delegated authority and the
canonical artifact model permit it.

## 18. Determinism

Composition SHOULD be deterministic wherever the transformation can be
fully specified.

A deterministic composition operation SHOULD produce materially
equivalent output when given materially equivalent:

-   Composer implementation and version;
-   Composition Request;
-   source artifacts and revisions;
-   project inputs and revisions;
-   applicable standards;
-   governed Engineering records;
-   configuration; and
-   relevant execution environment.

Ordering, formatting, mapping, and reference resolution SHOULD use
stable rules where practical.

Determinism SHALL NOT be claimed where material interpretation depends
on non-deterministic AI reasoning.

## 19. AI-assisted Composition

AI MAY participate in composition where permitted.

AI-assisted composition MAY:

-   interpret context;
-   select relevant permitted source material;
-   specialize generic content;
-   summarize governed sources;
-   generate derived structure;
-   identify conflicts;
-   propose mappings;
-   assist validation; and
-   generate composition reports.

AI-assisted composition SHALL:

-   preserve source authority;
-   distinguish inference from fact;
-   avoid inventing Engineering Evidence;
-   avoid inventing authority, approval, decision, acceptance, or
    lifecycle state;
-   preserve material uncertainty;
-   disclose AI-assisted mode in provenance where material; and
-   undergo validation proportionate to the target and risk.

AI capability SHALL NOT imply Engineering governance authority.

## 20. Validation

Composition validation SHOULD include the following layers where
applicable.

### 20.1 Request Validation

Validate:

-   request structure;
-   target type;
-   permitted configuration;
-   required references;
-   overwrite/replacement intent; and
-   unsupported options.

### 20.2 Input Validation

Validate:

-   presence and accessibility;
-   expected type or format;
-   schema conformance where applicable;
-   stable identity where required;
-   lifecycle state;
-   authority or approval status where material;
-   revision/effective point where material; and
-   internal consistency.

### 20.3 Semantic Validation

Validate that:

-   source and target semantics agree;
-   required project information is available;
-   applicable standards were resolved;
-   mandatory target behaviour is preserved;
-   prohibited overrides did not occur;
-   unresolved placeholders are permitted or absent;
-   project facts are grounded;
-   governed records are interpreted according to state and scope;
-   authority has not been invented or broadened;
-   material conflicts are resolved or explicitly surfaced; and
-   the output is fit for its declared consumer.

### 20.4 Output Validation

Validate the output against:

-   target schema or contract;
-   applicable Engineering System semantics;
-   project constraints;
-   required structural elements;
-   provenance requirements; and
-   applicable target-specific checklist or conformance rules.

## 21. Failure Behaviour

Composition SHALL fail or return an explicit non-success result when
safe composition is not possible.

Material failure conditions include:

-   invalid Composition Request;
-   unsupported target type;
-   missing required input;
-   unreadable or unparseable required input;
-   indeterminate required authority;
-   unresolved material conflict;
-   mandatory target behaviour would be lost;
-   prohibited override requested;
-   required project fact unavailable;
-   required Engineering standard unavailable;
-   output validation failure; or
-   unauthorized replacement of an existing artifact.

Failure information SHOULD identify:

-   failed stage;
-   specific issue;
-   affected source or target;
-   materiality;
-   whether any non-authoritative partial output was produced;
-   remediation where known; and
-   machine-readable failure status where implemented programmatically.

A failed composition SHALL NOT leave a partial output that can
reasonably be mistaken for a valid composed artifact.

## 22. Output Handling

### 22.1 Generated or Composed Status

A derived artifact SHOULD be identifiable as generated or composed where
that distinction is material to its consumer.

### 22.2 Manual Editing

Generated artifacts SHOULD be treated as read-only by default where
regeneration could overwrite manual changes.

Where manual editing is permitted, the implementation SHALL define how
regeneration:

-   preserves;
-   merges;
-   rejects; or
-   supersedes

manual content.

Manual editing SHALL NOT silently change the governed authority of the
artifact.

### 22.3 Atomicity

Programmatic implementations SHOULD write outputs atomically where
practical.

### 22.4 Replacement Protection

An existing output SHALL NOT be replaced unless:

-   replacement is explicitly permitted; and
-   the implementation can safely determine that replacement is
    appropriate.

A governed record SHALL NOT be overwritten merely because a Composition
Request names the same output location.

## 23. Composition Provenance

Every successful composition SHOULD produce embedded or accompanying
provenance proportionate to target significance.

Provenance SHOULD identify, where applicable:

-   composition identity;
-   target artifact type;
-   Composer name/type and version;
-   Composition Request identity and revision;
-   source artifacts and revisions;
-   project inputs and revisions;
-   governed Engineering records and states;
-   resolved Development Standards;
-   approved exceptions applied;
-   composition timestamp or effective point;
-   deterministic or AI-assisted mode;
-   validation result; and
-   output identity or location.

Provenance SHALL avoid unnecessarily embedding secrets, credentials, or
sensitive environment details.

## 24. Composition Report

A composition operation MAY produce a Composition Report describing what
occurred during composition.

A Composition Report MAY include:

-   requested target;
-   inputs loaded;
-   sources not available;
-   standards resolved;
-   optional inputs omitted;
-   specializations applied;
-   conflicts detected;
-   conflict resolutions;
-   warnings;
-   validation performed;
-   output produced; and
-   provenance.

A Composition Report is operational provenance for the composition
operation.

It is not Engineering Evidence and does not independently establish a
governed Engineering fact, decision, authority, state, or conclusion.

A Composition Report SHALL NOT supersede:

-   the composed artifact;
-   any authoritative source;
-   Engineering Evidence supporting engineering claims;
-   an ADR;
-   an EDR; or
-   another governed Engineering record.

A Composition Report is not a canonical governed Engineering record
unless another applicable specification explicitly establishes it as
such.

## 25. Prompt Composition

A project-specific Engineering prompt MAY be produced through
composition.

Prompt composition SHOULD preserve, where applicable:

-   source prompt objective;
-   required responsibilities;
-   applicable Engineering lifecycle semantics;
-   mandatory Engineering behaviour;
-   validation obligations;
-   completion criteria;
-   authority boundaries; and
-   expected output contract.

Project specialization MAY add:

-   project purpose and scope;
-   repository/module context;
-   technology-specific instructions;
-   applicable Development Standards;
-   governed architecture references;
-   current authorized execution context;
-   project-specific constraints;
-   target output locations; and
-   other grounded project context.

The resulting prompt remains a Derived Engineering Artifact.

A composed prompt SHALL NOT itself become a source of Engineering
governance merely because it contains governed instructions.

## 26. Composition of Governed Records

Composition MAY assist creation of governed Engineering records where
the target's canonical specification permits it.

Examples MAY include:

-   populating an Engineering Delivery Proposal draft from project
    context;
-   constructing an Engineering Delivery Plan draft from approved
    planning inputs;
-   drafting an ADR from architecture context and Engineering Evidence;
    or
-   assembling an EDR representation from governed realization records.

Composition SHALL preserve the target record's canonical lifecycle and
authority semantics.

For example:

-   composing a Proposal does not approve investment;
-   composing a Delivery Plan does not establish an Execution Baseline;
-   composing an ADR does not Approve an Architecture Decision;
-   composing an EDR does not establish its Engineering Conclusion or
    finalization.

The target's own specification, governance, template, and checklist
remain authoritative.

## 27. Historical Integrity

Composition SHALL preserve historical truth.

A Composer SHALL NOT:

-   rewrite an old record to make it appear consistent with a later
    decision;
-   treat a Superseded ADR as though it had never been authoritative;
-   treat a Rejected ADR as current architecture;
-   rewrite realization history based on the current desired state;
-   replace historical evidence with later interpretation; or
-   collapse materially distinct revisions or governed identities.

Where a current derived view combines historical and current sources,
the effective context SHOULD remain distinguishable.

## 28. Human, AI, Automated, and Mixed-team Participation

Composition MAY be performed by:

-   a human;
-   an AI agent;
-   deterministic automation;
-   a mixed human/AI workflow; or
-   another governed mechanism.

The same canonical composition rules apply regardless of actor.

Operational permission to execute composition SHALL NOT imply authority
to change the governed meaning of source or target artifacts.

Where the Composer also holds a separate governance authority, that
authority SHALL remain explicit and shall be exercised according to the
target artifact's canonical governance rather than being inferred from
the composition operation.

## 29. Tool Independence

Composition SHALL remain independent of specific tools.

A conforming implementation MAY use:

-   command-line tools;
-   CI/CD automation;
-   IDE integration;
-   repository workflows;
-   agent systems;
-   document-generation services;
-   structured Engineering repositories;
-   integrated Engineering Platform implementations; or
-   other implementations.

Tool workflow state SHALL NOT redefine canonical Engineering semantics.

A tool MAY automate canonical transitions only where the applicable
authority and target specification permit that transition.

## 30. Machine-readable Representation

Composition SHOULD be machine-readable sufficiently to preserve, where
applicable:

-   composition identity;
-   target type;
-   request identity;
-   source identities and revisions;
-   source authority/state;
-   project inputs;
-   standards resolution;
-   exceptions;
-   specialization operations;
-   conflicts and dispositions;
-   execution mode;
-   validation result;
-   output identity;
-   provenance; and
-   Composition Report where produced.

Machine readability SHALL NOT require one universal manifest or storage
schema.

An implementation MAY maintain structured composition state while
rendering human-readable manifests, reports, or derived artifacts.

## 31. Extensibility

A new composition target type MAY adopt this specification by defining:

-   target semantic type or contract;
-   required and optional inputs;
-   reusable source/template contract where applicable;
-   specialization rules;
-   authority constraints;
-   output validation rules;
-   target-specific checklist requirements where applicable; and
-   provenance requirements.

An extension SHALL NOT weaken mandatory rules in this specification.

## 32. Proportional Application

Composition governance SHALL be proportionate to the significance of the
target and its consequences.

A low-risk derived prompt or view MAY require lightweight provenance and
validation.

A composition operation affecting architecture, execution guidance,
security-sensitive material, regulated concerns, or governed records MAY
require:

-   stronger source validation;
-   explicit authority evaluation;
-   deeper conflict detection;
-   richer provenance;
-   target-specific checklist validation; and
-   human or separately authorized review.

Proportionality SHALL reduce unnecessary ceremony without permitting
composition to bypass material Engineering governance.

## 33. Conformance

A composition implementation conforms to this specification when,
proportionate to target significance:

-   the Composition Request is explicit;
-   target semantics are known;
-   source authority and state are respected;
-   applicable Engineering governance is applied;
-   project facts are grounded;
-   standards resolution is controlled;
-   material conflicts are not silently resolved;
-   mandatory target behaviour is preserved;
-   generated derivatives do not acquire invented authority;
-   governed records retain their own lifecycle and authority semantics;
-   deterministic and AI-assisted modes are represented accurately;
-   output validation is performed;
-   provenance is sufficient;
-   failure is explicit and safe;
-   historical integrity is preserved;
-   AI/automation remains within explicit authority; and
-   tool behaviour does not redefine canonical Engineering semantics.

## 34. Canonical Summary

The canonical composition model is:

    Composition Request
            ↓
    identify target semantics
            ↓
    resolve permitted inputs
            ↓
    determine authority / state / scope
            ↓
    resolve applicable standards
            ↓
    detect conflicts
       ↙                ↘
    unresolved          resolved
    material conflict      ↓
       ↓              specialize
    fail / explicit        ↓
    unresolved result   compose
                           ↓
                       validate
                      ↙        ↘
                   fail        pass
                    ↓            ↓
              no valid       derived
               output        artifact
                               +
                          provenance /
                      Composition Report

For governed target records:

    Composition
        = may create or populate

    Governance
        = establishes authoritative
          state, decision, acceptance,
          authorization, or conclusion

The governing rule is:

> Composition derives Engineering artifacts from governed and permitted
> sources; it does not create authority merely by assembling
> authoritative content.

This separation allows implementations to automate Engineering artifact
construction extensively while keeping Engineering governance, authority,
lifecycle, evidence, and historical integrity explicit and independently
enforceable.
