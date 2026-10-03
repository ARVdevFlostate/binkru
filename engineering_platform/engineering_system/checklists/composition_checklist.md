# Engineering Composition Checklist

## 1. Purpose

Use this checklist to independently validate an Engineering Composition
operation or implementation against the Engineering Composition
Specification.

This checklist validates, proportionate to the significance of the
Composition Target:

-   Composition Request semantics;
-   target semantics and target contract;
-   source identity, authority, state, scope, and provenance;
-   Development Standards resolution;
-   project-owned knowledge and factual grounding;
-   conflict and precedence handling;
-   specialization boundaries;
-   Derived Engineering Artifact authority;
-   deterministic and AI-assisted composition;
-   validation and failure behaviour;
-   output handling and replacement protection;
-   composition provenance and Composition Reports;
-   governed-record protection;
-   historical integrity;
-   human, AI, automated, and mixed-team participation;
-   tool independence; and
-   implementation conformance.

The Engineering Composition Specification remains authoritative for
canonical composition semantics.

This checklist is a validation instrument. It does not grant Engineering
governance authority or alter the authority, lifecycle, state, or
meaning of any source or target artifact.

## 2. Validation Outcome

Use one of the following outcomes:

-   **Pass** --- applicable composition requirements are satisfied.
-   **Pass with Observations** --- the operation or implementation is
    conformant, but non-blocking observations should be recorded.
-   **Rework Required** --- one or more material requirements are
    incomplete, inconsistent, unsafe, ambiguous, or non-conformant.

A checklist result SHALL NOT independently:

-   approve or accept a governed artifact;
-   establish an Architecture Decision;
-   establish an Execution Baseline;
-   establish an Engineering Conclusion;
-   finalize an Engineering Delivery Record;
-   authorize Release; or
-   create another governance outcome.

## 3. Validation Context

Record the composition context being validated.

  ----------------------------------------------------------------------------------------------
  Field                               Value
  ----------------------------------- ----------------------------------------------------------
  Composition Identity                `<identity or reference>`

  Composition Target                  `<target artifact / target type>`

  Composition Request                 `<request reference or description>`

  Composer                            `<human / AI / automation / mixed / tool>`

  Composer Version                    `<version or N/A>`

  Execution Mode                      `<deterministic / AI-assisted / mixed>`

  Validation Purpose                  `<operation / implementation / target-specific / other>`

  Validation Date / Reference         `<date/time or governed reference>`
  ----------------------------------------------------------------------------------------------

The Composition Request is an operational invocation concept. It SHALL
NOT be treated as a canonical governed Engineering record unless another
applicable specification explicitly establishes it as such.

## 4. Composition Applicability

-   [ ] The activity is a controlled derivation of an Engineering
    artifact from governed or explicitly permitted inputs.
-   [ ] Composition is appropriate for the requested target.
-   [ ] Composition is not being used as unrestricted content
    generation.
-   [ ] Composition is not being used to bypass canonical creation,
    decision, approval, acceptance, authorization, conclusion, or
    finalization semantics.
-   [ ] The applicable Engineering Composition Specification is
    identifiable.
-   [ ] Target-specific specifications, templates, checklists, lifecycle
    rules, or authority models are identifiable where applicable.

### Applicability Observations

`<observations>`

## 5. Composition Request

-   [ ] An explicit Composition Request exists.
-   [ ] The requested target artifact type is identifiable.
-   [ ] Required inputs are identifiable.
-   [ ] Optional inputs are identifiable where relevant.
-   [ ] Intended consumer is identifiable where material.
-   [ ] Permitted configuration is explicit where applicable.
-   [ ] Requested output destination is explicit where applicable.
-   [ ] Replacement or overwrite intent is explicit where applicable.
-   [ ] Validation profile is identifiable where applicable.
-   [ ] Provenance requirements are identifiable where applicable.
-   [ ] The request does not redefine mandatory Engineering governance.
-   [ ] The request does not grant authority the requester does not
    possess.

### Request Observations

`<observations>`

## 6. Composition Target

-   [ ] The target has a known semantic type or explicit target
    contract.
-   [ ] Required target structure and behaviour are identifiable.
-   [ ] Mandatory target responsibilities are identifiable.
-   [ ] Target authority semantics are understood.
-   [ ] Target lifecycle/state semantics are understood where
    applicable.
-   [ ] Target-specific validation requirements are identifiable.
-   [ ] Composition will not cause the target to acquire authority
    merely because it was generated.
-   [ ] Where the target is a governed record, composition is limited to
    the state permitted by applicable governance.

### Target Observations

`<observations>`

## 7. Input Resolution

-   [ ] Required inputs are present and accessible.
-   [ ] Optional inputs are handled explicitly.
-   [ ] Input types/formats are valid where applicable.
-   [ ] Input identities are sufficient for traceability where material.
-   [ ] Input revisions/effective points are identifiable where
    material.
-   [ ] Input provenance is sufficient where material.
-   [ ] Prior composition outputs are used only where explicitly
    permitted.
-   [ ] Missing required inputs cause failure or explicit non-success
    rather than silent substitution.

### Input Resolution Observations

`<observations>`

## 8. Source Authority, State, and Scope

For each material source:

-   [ ] Source authority is understood for the concern being composed.
-   [ ] Source lifecycle state is interpreted correctly.
-   [ ] Source scope is interpreted correctly.
-   [ ] Effective point is considered where material.
-   [ ] Authoritative sources are distinguishable from advisory sources.
-   [ ] Reusable assets are not assumed to be authoritative merely
    because they are reusable.
-   [ ] Generated/derived sources are identifiable as such.
-   [ ] Inferred/defaulted inputs are distinguishable from authoritative
    facts.
-   [ ] One artifact's authority is not generalized beyond its governed
    concern.
-   [ ] A more recent source is not automatically treated as higher
    authority.
-   [ ] Draft, Deferred, Rejected, Superseded, or otherwise historical
    records are interpreted according to their canonical semantics.

### Authority / State / Scope Observations

`<observations>`

## 9. Governed Engineering Records

Where governed Engineering records are composition inputs:

-   [ ] Engineering Delivery Proposals are interpreted according to
    their canonical state and authority.
-   [ ] Approved Investment Baselines are treated according to their
    governed scope.
-   [ ] Engineering Delivery Plans are interpreted according to their
    canonical state and authority.
-   [ ] Execution Baselines are not silently revised by composition.
-   [ ] Engineering Slices are interpreted according to applicable
    lifecycle semantics.
-   [ ] Draft ADRs are not treated as authoritative architecture.
-   [ ] Accepted ADRs are authoritative only for their governed
    architecture scope.
-   [ ] Rejected ADRs are retained as historical knowledge but not
    treated as current architecture.
-   [ ] Superseded ADRs are interpreted according to their effective
    historical context.
-   [ ] Engineering Evidence supports claims but is not treated as
    making governance decisions.
-   [ ] EDRs provide material realization history but do not replace ADR
    reasoning or other governed authority.
-   [ ] Future governed records are interpreted according to their own
    canonical specifications.

### Governed Record Observations

`<observations>`

## 10. Development Standards Resolution

Where reusable Development Standards apply:

-   [ ] Relevant technologies are derived from explicit project
    declarations or equivalent project-owned representations.
-   [ ] Standards are resolved through an explicit or deterministic
    governed mapping mechanism.
-   [ ] Applicable reusable standards are identifiable.
-   [ ] Project-specific standards are applied where valid.
-   [ ] Approved scoped exceptions are applied only within their
    authority.
-   [ ] Unapproved weakening of an Engineering standard is rejected.
-   [ ] Absence of a reusable standard is recorded rather than treated
    automatically as project invalidity.
-   [ ] Composition fails only where the target requires a standard that
    cannot be supplied.
-   [ ] Standards resolution is traceable.

### Standards Observations

`<observations>`

## 11. Project-owned Knowledge and Factual Grounding

-   [ ] Project-specific facts come from project-owned or otherwise
    authoritative sources.
-   [ ] Project purpose and scope are grounded where used.
-   [ ] Repository/module structure is grounded where used.
-   [ ] Technology declarations are grounded where used.
-   [ ] Architecture boundaries are grounded where used.
-   [ ] Project-specific standards are grounded where used.
-   [ ] Delivery context is grounded where used.
-   [ ] Missing material project facts are not invented.
-   [ ] Assumptions are distinguishable from established facts.
-   [ ] Material unavailable facts remain explicitly unresolved where
    permitted.
-   [ ] Composition fails where safe composition requires a fact that is
    unavailable.

### Factual Grounding Observations

`<observations>`

## 12. Precedence and Conflict Resolution

Where multiple sources address the same concern:

-   [ ] The concern in conflict is explicit.
-   [ ] Applicable authority domain is identified.
-   [ ] Source authority is evaluated.
-   [ ] Source scope is evaluated.
-   [ ] Source lifecycle state is evaluated.
-   [ ] Effective point is evaluated where material.
-   [ ] Applicable law, regulation, contract, explicit governance,
    exception, or supersession is considered where relevant.
-   [ ] Lower-authority content does not silently override
    higher-authority content for the same governed concern.
-   [ ] Recency alone is not used as precedence.
-   [ ] Determinable conflicts are resolved according to applicable
    authority.
-   [ ] Unresolved material conflicts cause failure or an explicit
    unresolved-conflict result.
-   [ ] The Composer does not invent a conflict resolution.

### Conflict Observations

`<observations>`

## 13. Mandatory Behaviour

-   [ ] Composition Request is identified.
-   [ ] Target type/contract is validated.
-   [ ] Required inputs are resolved.
-   [ ] Input identity and authority are established where material.
-   [ ] Applicable Engineering System semantics are applied.
-   [ ] Applicable Development Standards are resolved.
-   [ ] Authoritative content is distinguishable from generated
    specialization.
-   [ ] Mandatory target behaviour is preserved.
-   [ ] Project facts, Engineering Evidence, authority, decisions, and
    lifecycle state are not invented.
-   [ ] Material conflicts are detected.
-   [ ] Material uncertainty is preserved where unresolved.
-   [ ] Composed output is validated.
-   [ ] Sufficient provenance is produced.
-   [ ] Unauthorized replacement/override is prevented.
-   [ ] Unsafe composition fails clearly.

### Mandatory Behaviour Observations

`<observations>`

## 14. Non-configurable Behaviour

Confirm that configuration cannot disable:

-   [ ] applicable governance;

-   [ ] required-input validation;

-   [ ] authority evaluation;

-   [ ] material conflict detection;

-   [ ] mandatory target-contract preservation;

-   [ ] provenance;

-   [ ] output validation;

-   [ ] protection against unsupported project facts;

-   [ ] protection against invented Engineering Evidence;

-   [ ] protection against invented authority or decision outcomes;

-   [ ] protection against unauthorized overrides; or

-   [ ] failure on unresolved critical errors.

-   [ ] Invalid attempts to disable mandatory behaviour are rejected.

### Non-configurable Behaviour Observations

`<observations>`

## 15. Permitted Configuration

Where configuration is supported:

-   [ ] Configuration affects only permitted operational or presentation
    concerns.
-   [ ] Output destination configuration remains within applicable
    authority.
-   [ ] Optional input selection does not remove mandatory inputs.
-   [ ] Replacement policy does not bypass governed record protection.
-   [ ] Formatting/verbosity options do not alter canonical semantics.
-   [ ] Optional target sections are omitted only where the target
    contract permits.
-   [ ] Deterministic/AI-assisted execution preferences do not weaken
    mandatory validation.
-   [ ] Target-specific options remain within the target contract and
    applicable authority.

### Configuration Observations

`<observations>`

## 16. Specialization

The Composer MAY specialize permitted content. Validate that
specialization:

-   [ ] resolves placeholders only from grounded or permitted sources;
-   [ ] inserts grounded project facts;
-   [ ] applies project constraints;
-   [ ] inserts applicable Development Standards;
-   [ ] references governed Engineering records correctly;
-   [ ] omits only explicitly optional and irrelevant sections;
-   [ ] expands generic instructions without weakening mandatory
    responsibilities;
-   [ ] generates target-specific structure within the target contract;
-   [ ] adds provenance where appropriate; and
-   [ ] produces derived views without changing source authority.

Confirm that specialization does NOT:

-   [ ] remove mandatory responsibilities;
-   [ ] weaken required validation;
-   [ ] alter canonical lifecycle semantics;
-   [ ] alter canonical artifact semantics;
-   [ ] change approved scope without authority;
-   [ ] contradict authoritative sources;
-   [ ] convert assumptions into facts;
-   [ ] introduce unsupported technologies as project facts;
-   [ ] invent paths, interfaces, dependencies, evidence, authority,
    approvals, decisions, or state;
-   [ ] silently resolve material conflicts;
-   [ ] rewrite historical records; or
-   [ ] turn a generated derivative into a new source of governance
    merely because it was composed.

### Specialization Observations

`<observations>`

## 17. Derived Artifact Authority

-   [ ] The composed artifact is treated as a Derived Engineering
    Artifact unless its canonical target specification establishes
    another semantic class.
-   [ ] Composition does not independently make the artifact approved.
-   [ ] Composition does not independently make the artifact accepted.
-   [ ] Composition does not independently make the artifact authorized.
-   [ ] Composition does not independently make the artifact
    authoritative.
-   [ ] Composition does not independently establish an Engineering
    Conclusion.
-   [ ] Composition does not independently establish an Architecture
    Decision.
-   [ ] Composition does not independently establish an Execution
    Baseline.
-   [ ] Composition does not independently finalize an EDR.
-   [ ] Composition does not independently authorize Release.
-   [ ] Where the target is governed, composition creates/populates it
    only to the state permitted by governance.
-   [ ] Artifact creation and governance authority are not collapsed
    unless explicit delegated authority and the canonical artifact model
    permit it.

### Derived Authority Observations

`<observations>`

## 18. Deterministic Composition

Use where deterministic composition is claimed.

-   [ ] Transformation can be sufficiently specified to support
    deterministic execution.
-   [ ] Materially equivalent inputs produce materially equivalent
    outputs.
-   [ ] Composer implementation/version is identifiable.
-   [ ] Composition Request is identifiable.
-   [ ] Source artifacts/revisions are identifiable.
-   [ ] Project inputs/revisions are identifiable.
-   [ ] Applicable standards are identifiable.
-   [ ] Governed records used are identifiable.
-   [ ] Configuration is identifiable.
-   [ ] Relevant execution environment is identifiable where material.
-   [ ] Ordering, formatting, mapping, and reference resolution use
    stable rules where practical.
-   [ ] Determinism is not claimed where material interpretation depends
    on non-deterministic AI reasoning.

### Determinism Observations

`<observations>`

## 19. AI-assisted Composition

Use where AI participates materially.

-   [ ] AI-assisted mode is identifiable in provenance where material.
-   [ ] AI preserves source authority.
-   [ ] AI distinguishes inference from fact.
-   [ ] AI does not invent project facts.
-   [ ] AI does not invent Engineering Evidence.
-   [ ] AI does not invent authority.
-   [ ] AI does not invent approval, acceptance, decision, or lifecycle
    state.
-   [ ] AI preserves material uncertainty.
-   [ ] AI-generated specialization remains within the target contract.
-   [ ] AI-generated conflict analysis does not silently become
    governance authority.
-   [ ] AI-assisted output undergoes validation proportionate to target
    and risk.
-   [ ] AI capability is not treated as Engineering governance
    authority.

### AI-assisted Composition Observations

`<observations>`

## 20. Request Validation

-   [ ] Request structure is valid.
-   [ ] Target type is supported.
-   [ ] Configuration is permitted.
-   [ ] Required references are present.
-   [ ] Overwrite/replacement intent is valid.
-   [ ] Unsupported options are rejected or explicitly surfaced.

### Request Validation Observations

`<observations>`

## 21. Input Validation

-   [ ] Required inputs are present and accessible.
-   [ ] Expected input type/format is valid.
-   [ ] Schema conformance is verified where applicable.
-   [ ] Stable identity is present where required.
-   [ ] Lifecycle state is valid where applicable.
-   [ ] Authority/approval status is verified where material.
-   [ ] Revision/effective point is verified where material.
-   [ ] Internal consistency is sufficient.

### Input Validation Observations

`<observations>`

## 22. Semantic Validation

-   [ ] Source and target semantics agree.
-   [ ] Required project information is available.
-   [ ] Applicable standards are resolved.
-   [ ] Mandatory target behaviour is preserved.
-   [ ] Prohibited overrides did not occur.
-   [ ] Unresolved placeholders are absent or explicitly permitted.
-   [ ] Project facts are grounded.
-   [ ] Governed records are interpreted according to state and scope.
-   [ ] Authority has not been invented or broadened.
-   [ ] Material conflicts are resolved or explicitly surfaced.
-   [ ] Output is fit for its declared consumer.

### Semantic Validation Observations

`<observations>`

## 23. Output Validation

-   [ ] Output conforms to the target schema/contract.
-   [ ] Output conforms to applicable Engineering System semantics.
-   [ ] Output respects project constraints.
-   [ ] Required structural elements are present.
-   [ ] Provenance requirements are satisfied.
-   [ ] Applicable target-specific checklist or conformance rules are
    satisfied.
-   [ ] Validation result is preserved in provenance or reporting where
    required.

### Output Validation Observations

`<observations>`

## 24. Failure Behaviour

Where composition fails or cannot safely complete:

-   [ ] Failure/non-success is explicit.
-   [ ] Failed stage is identifiable.
-   [ ] Specific issue is identifiable.
-   [ ] Affected source/target is identifiable.
-   [ ] Materiality is identifiable where relevant.
-   [ ] Partial output status is explicit where any partial output
    exists.
-   [ ] Remediation is identified where known.
-   [ ] Machine-readable failure status is available where implemented
    programmatically.
-   [ ] Partial output cannot reasonably be mistaken for a valid
    composed artifact.
-   [ ] Invalid requests do not produce apparently valid output.
-   [ ] Missing required inputs do not cause silent substitution.
-   [ ] Unresolved material conflicts do not produce
    authoritative-looking output.
-   [ ] Output validation failure prevents valid-success status.

### Failure Observations

`<observations>`

## 25. Output Handling

### 25.1 Generated / Composed Status

-   [ ] Derived status is identifiable where material to the consumer.

### 25.2 Manual Editing

Where manual editing is permitted:

-   [ ] Regeneration behaviour is defined.
-   [ ] Preserve/merge/reject/supersede semantics are explicit.
-   [ ] Manual content is not silently lost.
-   [ ] Manual editing does not silently change governed authority.

### 25.3 Atomicity

For programmatic implementations:

-   [ ] Outputs are written atomically where practical.
-   [ ] Failed writes do not leave apparently valid partial artifacts.

### 25.4 Replacement Protection

-   [ ] Existing output is replaced only when explicitly permitted.
-   [ ] Replacement appropriateness can be determined safely.
-   [ ] Governed records are not overwritten merely because the request
    names the same destination.

### Output Handling Observations

`<observations>`

## 26. Composition Provenance

For a successful composition, validate provenance proportionate to
significance.

-   [ ] Composition identity is recorded where applicable.
-   [ ] Target artifact type is recorded.
-   [ ] Composer name/type and version are recorded where material.
-   [ ] Composition Request identity/revision is recorded where
    applicable.
-   [ ] Source artifacts/revisions are recorded.
-   [ ] Project inputs/revisions are recorded where material.
-   [ ] Governed Engineering records and states are recorded where
    material.
-   [ ] Resolved Development Standards are recorded.
-   [ ] Approved exceptions are recorded where applied.
-   [ ] Composition timestamp/effective point is recorded where
    material.
-   [ ] Deterministic or AI-assisted mode is recorded.
-   [ ] Validation result is recorded.
-   [ ] Output identity/location is recorded where applicable.
-   [ ] Provenance avoids unnecessary secrets, credentials, or sensitive
    environment details.

### Provenance Observations

`<observations>`

## 27. Composition Report

Where a Composition Report is produced:

-   [ ] The report describes the composition operation rather than
    redefining the target artifact.
-   [ ] Requested target is identifiable.
-   [ ] Inputs loaded are identifiable.
-   [ ] Unavailable sources are visible where material.
-   [ ] Standards resolved are identifiable.
-   [ ] Optional inputs omitted are identifiable where material.
-   [ ] Specializations applied are identifiable where material.
-   [ ] Conflicts and their dispositions are visible.
-   [ ] Warnings are visible.
-   [ ] Validation performed is visible.
-   [ ] Output produced is identifiable.
-   [ ] Provenance is included or referenced.
-   [ ] The Composition Report is treated as operational provenance.
-   [ ] The Composition Report is not treated as Engineering Evidence.
-   [ ] The Composition Report does not independently establish a
    governed Engineering fact, decision, authority, state, or
    conclusion.
-   [ ] The Composition Report does not supersede the composed artifact
    or authoritative sources.
-   [ ] The Composition Report is not treated as a canonical governed
    Engineering record unless another applicable specification
    explicitly establishes it as such.

### Composition Report Observations

`<observations>`

## 28. Prompt Composition

Use where the Composition Target is a project-specific Engineering
prompt.

-   [ ] Source prompt objective is preserved where applicable.
-   [ ] Required responsibilities are preserved.
-   [ ] Applicable Engineering lifecycle semantics are preserved.
-   [ ] Mandatory Engineering behaviour is preserved.
-   [ ] Validation obligations are preserved.
-   [ ] Completion criteria are preserved.
-   [ ] Authority boundaries are preserved.
-   [ ] Expected output contract is preserved.
-   [ ] Added project purpose/scope is grounded.
-   [ ] Added repository/module context is grounded.
-   [ ] Added technology-specific instructions are grounded.
-   [ ] Applicable Development Standards are correctly
    inserted/referenced.
-   [ ] Governed architecture references are interpreted correctly.
-   [ ] Current authorized execution context is interpreted correctly.
-   [ ] Project-specific constraints are grounded.
-   [ ] Result remains a Derived Engineering Artifact.
-   [ ] Composed prompt is not treated as a new source of Engineering
    governance merely because it contains governed instructions.

### Prompt Composition Observations

`<observations>`

## 29. Composition of Governed Records

Use where the target is a governed Engineering record.

-   [ ] The target's canonical specification is identifiable.
-   [ ] Applicable template is used where required.
-   [ ] Applicable checklist is used where required.
-   [ ] Target lifecycle semantics are preserved.
-   [ ] Target authority semantics are preserved.
-   [ ] Composition creates/populates only the state permitted by
    governance.
-   [ ] Composing a Proposal is not treated as Investment Approval.
-   [ ] Composing a Delivery Plan is not treated as establishment of an
    Execution Baseline.
-   [ ] Composing an ADR is not treated as Architecture Decision
    Approve.
-   [ ] Composing an EDR is not treated as establishment of its
    Engineering Conclusion or finalization.
-   [ ] Any separate governance authority exercised by the Composer is
    explicit rather than inferred from composition capability.

### Governed Record Composition Observations

`<observations>`

## 30. Historical Integrity

-   [ ] Historical records are not rewritten to appear consistent with
    later decisions.
-   [ ] Superseded ADRs retain their historical authoritative context.
-   [ ] Rejected ADRs are not treated as current architecture.
-   [ ] Realization history is not rewritten based on current desired
    state.
-   [ ] Historical evidence is not replaced by later interpretation.
-   [ ] Materially distinct revisions or governed identities are not
    collapsed.
-   [ ] Current derived views distinguish historical and current
    effective context where material.

### Historical Integrity Observations

`<observations>`

## 31. Human, AI, Automated, and Mixed-team Participation

-   [ ] Composer type is identifiable where material.
-   [ ] The same canonical composition rules apply regardless of actor.
-   [ ] Operational permission to compose is not treated as governance
    authority.
-   [ ] Where the Composer holds separate governance authority, that
    authority is explicit.
-   [ ] Separate governance authority is exercised according to the
    target artifact's canonical governance.
-   [ ] Governance authority is not inferred from composition
    capability, tool ownership, technical expertise, or automation
    capability.

### Participation Observations

`<observations>`

## 32. Tool Independence

-   [ ] Tool workflow state does not redefine canonical Engineering
    semantics.
-   [ ] CLI success does not independently establish governance
    authority.
-   [ ] CI/CD completion does not independently establish governance
    authority.
-   [ ] Issue/workflow completion does not independently establish
    governance authority.
-   [ ] Agent completion does not independently establish governance
    authority.
-   [ ] Document generation does not independently establish governance
    authority.
-   [ ] A tool automates canonical transitions only where applicable
    authority and target semantics permit.
-   [ ] Implementation-specific mechanics remain
    implementation details rather than canonical Engineering semantics.

### Tool Independence Observations

`<observations>`

## 33. Machine-readable Representation

Where composition is implemented programmatically:

-   [ ] Composition identity can be represented.
-   [ ] Target type can be represented.
-   [ ] Request identity can be represented.
-   [ ] Source identities/revisions can be represented.
-   [ ] Source authority/state can be represented where material.
-   [ ] Project inputs can be represented.
-   [ ] Standards resolution can be represented.
-   [ ] Exceptions can be represented.
-   [ ] Specialization operations can be represented where required.
-   [ ] Conflicts/dispositions can be represented.
-   [ ] Execution mode can be represented.
-   [ ] Validation result can be represented.
-   [ ] Output identity can be represented.
-   [ ] Provenance can be represented.
-   [ ] Composition Report can be represented where produced.
-   [ ] Implementation does not require one universal manifest/storage
    schema to satisfy canonical semantics.

### Machine-readable Representation Observations

`<observations>`

## 34. Extensibility

Where a new Composition Target type is introduced:

-   [ ] Target semantic type/contract is defined.
-   [ ] Required inputs are defined.
-   [ ] Optional inputs are defined.
-   [ ] Reusable source/template contract is defined where applicable.
-   [ ] Specialization rules are defined.
-   [ ] Authority constraints are defined.
-   [ ] Output validation rules are defined.
-   [ ] Target-specific checklist requirements are defined where
    applicable.
-   [ ] Provenance requirements are defined.
-   [ ] Extension does not weaken mandatory composition rules.

### Extensibility Observations

`<observations>`

## 35. Proportionality Review

-   [ ] Validation depth is proportionate to target significance and
    consequence.
-   [ ] Low-risk derived prompts/views are not burdened with unnecessary
    ceremony.
-   [ ] Architecture-sensitive composition receives stronger validation
    where warranted.
-   [ ] Execution-guidance composition receives stronger validation
    where warranted.
-   [ ] Security-sensitive or regulated composition receives stronger
    validation where warranted.
-   [ ] Governed-record composition receives stronger validation where
    warranted.
-   [ ] Reduced ceremony does not bypass material Engineering
    governance.
-   [ ] Additional ceremony does not obscure the actual composition
    risks or authority boundaries.

### Proportionality Observations

`<observations>`

## 36. Final Conformance Review

Before issuing the checklist result, confirm:

-   [ ] Composition is appropriate for the target.
-   [ ] Composition Request is explicit and operational rather than
    inherently governed.
-   [ ] Target semantics are known.
-   [ ] Required inputs are resolved.
-   [ ] Source authority, state, scope, and effective context are
    respected.
-   [ ] Project facts are grounded.
-   [ ] Development Standards are resolved appropriately.
-   [ ] Material conflicts are not silently resolved.
-   [ ] Mandatory target behaviour is preserved.
-   [ ] Specialization remains within permitted boundaries.
-   [ ] Derived artifacts do not acquire invented authority.
-   [ ] Governed target records retain their own lifecycle and authority
    semantics.
-   [ ] Deterministic/AI-assisted execution mode is represented
    accurately.
-   [ ] Validation is complete proportionate to significance.
-   [ ] Failure behaviour is explicit and safe.
-   [ ] Output handling prevents unsafe replacement or partial-valid
    artifacts.
-   [ ] Provenance is sufficient.
-   [ ] Composition Reports remain operational provenance rather than
    Engineering Evidence.
-   [ ] Historical integrity is preserved.
-   [ ] Human/AI/automation participation remains within explicit
    authority.
-   [ ] Tool behaviour does not redefine canonical Engineering
    semantics.

## 37. Checklist Result

### Result

`Pass / Pass with Observations / Rework Required`

### Blocking Findings

-   `<finding or None>`

### Non-blocking Observations

-   `<observation or None>`

### Required Rework

-   `<required rework or None>`

### Validator

`<human / AI / automated validator / mixed mechanism>`

### Validation Date / Reference

`<date/time or governed reference>`

## 38. Interpretation of Result

### Pass

`Pass` means the composition operation or implementation satisfies
applicable checklist requirements for the validation purpose performed.

It does not establish governance authority for the composed artifact.

### Pass with Observations

`Pass with Observations` means the composition operation or
implementation is conformant for the validation purpose performed, but
non-blocking observations remain worth preserving.

Observations SHALL NOT conceal a material deficiency that should result
in `Rework Required`.

### Rework Required

`Rework Required` means one or more material composition requirements
are incomplete, inconsistent, unsafe, ambiguous, or non-conformant.

The composition operation or implementation SHOULD return to the
applicable correction activity.

A checklist result of `Rework Required` SHALL NOT be interpreted as a
canonical governance outcome for the Composition Target.

## 39. Canonical Validation Rule

The checklist validates Composition.

It does not govern the composed subject matter.

The governing separation is:

    Engineering Composition Specification
        = defines canonical
          composition semantics

    Composition Request
        = operational invocation

    Composer
        = performs composition

    Composition Checklist
        = independently validates
          composition conformance

    Target governance
        = establishes applicable
          authority, state, decision,
          acceptance, authorization,
          conclusion, or finalization

Therefore:

    Composition Checklist Pass
        ≠ target approval / acceptance /
          authorization / decision

and:

    Composition Checklist Rework Required
        ≠ target governance Return /
          rejection / other disposition

unless the applicable target governance separately establishes that
outcome.
