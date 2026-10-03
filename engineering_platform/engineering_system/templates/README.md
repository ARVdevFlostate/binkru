# Engineering System Templates

## 1. Purpose

This directory contains canonical Engineering System templates used to
create or initialize Engineering artifacts where a canonical document
representation is useful.

Templates provide reusable structure for artifact creation.

They support consistency, completeness, governance, traceability, and
machine-assisted Engineering without making every Engineering concept
document-centric.

Not every Engineering System capability or artifact requires a template.

## 2. Canonical Role of a Template

A template defines a reusable representation structure for an applicable
Engineering artifact.

A template MAY provide:

-   required or recommended sections;
-   canonical fields;
-   placeholders;
-   authoring guidance;
-   embedded preparation checks;
-   relationship/reference structures; and
-   representation conventions.

A template does not independently define the complete semantics of the
artifact.

Where an artifact has an applicable specification, that specification
defines its canonical semantics.

Where an artifact has an applicable checklist, that checklist governs
independent readiness or conformance validation for the purpose defined
by the checklist.

## 3. Template, Specification, and Checklist

The canonical separation is:

    Specification
        = defines canonical semantics

    Template
        = structures artifact creation
          or representation

    Checklist
        = independently validates
          readiness or conformance

A template SHALL NOT override an applicable specification.

Embedded checks in a template are authoring aids unless an applicable
specification explicitly establishes otherwise.

An applicable canonical checklist SHALL NOT be replaced by a template's
embedded checks.

## 4. Templates and Authority

Instantiation of a template does not by itself make the resulting
artifact authoritative.

Authority depends on:

-   the semantic type of the artifact;
-   its canonical lifecycle state;
-   applicable governance;
-   applicable decision, approval, acceptance, authorization, or
    finalization;
-   the scope of the relevant authority; and
-   any required concurrence.

Therefore:

    template instantiation
        ≠ approval

    template completion
        ≠ acceptance

    template validation
        ≠ authorization

    generated document
        ≠ authoritative record

An artifact created from a template MAY become authoritative only
through the governance applicable to that artifact.

Examples include:

-   an Engineering Delivery Proposal does not establish an Approved
    Investment Baseline merely because its template is complete;
-   an Engineering Delivery Plan does not establish an Execution
    Baseline merely because it has been generated or validated;
-   an Architecture Decision Record does not become Accepted merely
    because the ADR template has been completed;
-   an Engineering Delivery Record does not establish its Engineering
    Conclusion or finalization merely because all template sections have
    been populated.

## 5. Applicability

Use a canonical template where the applicable Engineering artifact
benefits from a consistent human-readable representation.

A template is particularly useful where:

-   the artifact is a durable governed record;
-   recurring information must be captured consistently;
-   lifecycle or governance information must remain visible;
-   stable relationships and references are important;
-   human and machine participants benefit from a common representation;
    or
-   omission of material information creates Engineering risk.

A template is not required merely because a canonical Engineering
capability exists.

For example, an operational or continuous capability such as Engineering
Composition or Engineering Orchestration MAY be governed by a
specification and checklist without requiring a canonical record
template.

## 6. Artifact Identity

Where the applicable artifact model requires stable identity, the
instantiated artifact SHALL preserve that identity independently of:

-   filename;
-   directory path;
-   document title;
-   issue identifier;
-   workflow identifier;
-   agent execution identifier; or
-   tool-specific storage location.

Templates SHOULD expose stable identity fields where required by the
applicable artifact semantics.

Representation revision SHALL NOT be used to bypass canonical identity,
immutability, supersession, or governance rules.

## 7. Template Principles

Canonical Engineering System templates SHOULD:

-   reflect the applicable canonical specification;
-   preserve lifecycle and authority boundaries;
-   support proportional application;
-   provide sufficient structure without unnecessary ceremony;
-   distinguish facts, assumptions, evidence, recommendations,
    decisions, and conclusions where material;
-   preserve stable identity and traceability where applicable;
-   support human, AI, automated, and mixed-team use;
-   remain tool-independent;
-   support machine-readable representation where practical; and
-   avoid embedding project-specific facts in the canonical template.

Templates SHOULD evolve only when the change improves the canonical
Engineering System rather than one project's local preference.

## 8. Guidance and Authoring Aids

Templates MAY contain guidance explaining:

-   when the template applies;
-   how sections should be completed;
-   what information is required or optional;
-   relevant lifecycle or authority semantics;
-   common failure modes;
-   proportionality considerations; and
-   relationships to applicable specifications or checklists.

Guidance is an authoring aid.

A template MAY also contain embedded readiness or final-record checks.

Such checks SHALL NOT be interpreted as independent governance authority
unless an applicable specification explicitly establishes that
authority.

## 9. Instantiation

When a canonical template is instantiated:

-   placeholders SHOULD be replaced with grounded artifact-specific
    content;
-   non-applicable optional sections MAY be omitted where the template
    and applicable specification permit;
-   mandatory semantic content SHALL be preserved;
-   canonical lifecycle and authority semantics SHALL be preserved;
-   applicable stable identities and references SHALL be retained;
-   generated or inferred content SHALL remain distinguishable from
    authoritative facts where material; and
-   applicable validation SHALL be performed.

Guidance MAY be removed from the instantiated representation where doing
so does not remove required semantics, context, or governance
information.

There is no universal requirement that all guidance text be removed from
every instantiated artifact.

## 10. Project and Engineering Context

An instantiated artifact SHOULD identify its applicable Engineering
context through stable governed relationships rather than relying only
on a project name or repository location.

Depending on the artifact, relevant context MAY include:

-   Product or initiative;
-   Engineering Delivery Proposal;
-   Approved Investment Baseline;
-   Engineering Delivery Plan;
-   Execution Baseline;
-   Epic;
-   Engineering Slice;
-   Architecture Decision Record;
-   Engineering Evidence;
-   Engineering Delivery Record;
-   Release or other cross-system relationship; and
-   other governed Engineering objects.

An artifact SHALL NOT be assumed to belong to only one project lifetime
where its canonical semantics permit reuse across realizations.

For example, an Accepted ADR MAY remain applicable across future
Engineering realizations while its governed architecture scope remains
valid.

## 11. Composition and Generated Artifacts

A template MAY be instantiated manually or through Engineering
Composition.

Composition MAY:

-   populate template structure;
-   resolve grounded project context;
-   insert applicable Development Standards;
-   reference governed records;
-   specialize permitted content; and
-   produce a Derived Engineering Artifact or governed-record draft
    where permitted.

Composition does not create authority merely by populating a canonical
template.

Where the target is a governed record, the target's own specification,
lifecycle, governance, and checklist remain applicable.

## 12. Human, AI, and Automated Use

Templates MAY be used by:

-   humans;
-   AI agents;
-   deterministic automation;
-   mixed human/AI teams; or
-   other governed mechanisms.

The same canonical artifact semantics apply regardless of actor.

AI or automation MAY assist with template selection, population,
validation, traceability, and composition where permitted.

AI or automation SHALL NOT infer authority merely from the ability to
create or complete a template.

It SHALL NOT invent:

-   project facts;
-   Engineering Evidence;
-   authority;
-   approval;
-   acceptance;
-   Architecture Decisions;
-   Engineering Conclusions;
-   lifecycle state; or
-   other governed outcomes.

## 13. Project-specific Adaptation

Projects MAY adapt an instantiated artifact where the applicable
specification and governance permit it.

Project-specific adaptation SHALL NOT:

-   modify the canonical template in place;
-   weaken mandatory Engineering semantics;
-   remove required governance;
-   redefine canonical lifecycle states;
-   redefine canonical authority;
-   silently alter stable identity;
-   bypass an applicable checklist; or
-   represent a local convention as canonical Engineering System
    behaviour.

Where a recurring project-specific need indicates a generally useful
improvement, the canonical Engineering System template MAY be revised
through the applicable Engineering System governance.

## 14. Canonical Template Ownership

Canonical templates are owned by the Engineering System.

Projects and implementations SHOULD consume canonical templates without
modifying the canonical source for local needs.

Conforming implementations MAY render, compose, validate, or operationalize templates while preserving their canonical semantics.

A tool-specific representation SHALL NOT become the canonical template
merely because a particular implementation uses it.

## 15. Template Evolution

A canonical template SHOULD be reviewed when:

-   its governing specification changes;
-   its applicable checklist changes materially;
-   lifecycle or authority semantics change;
-   the Artifact Model changes;
-   repeated use reveals structural ambiguity;
-   automation requires clearer machine-readable semantics; or
-   a generally applicable improvement is identified.

Template evolution SHALL preserve historical artifact integrity.

Updating a canonical template SHALL NOT retroactively rewrite previously
governed records merely to match the newest template structure.

## 16. Directory Conformance

A canonical template in this directory SHOULD:

-   have a clear artifact purpose;
-   align with an applicable Engineering System specification;
-   use canonical terminology;
-   expose applicable lifecycle/state semantics;
-   expose authority/governance fields where required;
-   preserve stable identity where required;
-   reference applicable checklist semantics where relevant;
-   avoid project-specific content;
-   remain implementation-independent; and
-   avoid claiming authority merely from template completion.

A template that no longer aligns with its governing specification SHOULD
be revised, superseded, or removed from the canonical template set
through the applicable Engineering System governance.

## 17. Canonical Summary

The template model is:

    Engineering System Specification
              ↓
       canonical semantics
              ↓
         Template
              ↓
    structures creation
              ↓
    instantiated artifact
              ↓
    applicable validation
              ↓
    applicable governance
              ↓
    authoritative state
    only where governance
    establishes authority

The governing rule is:

> A template structures an Engineering artifact; it does not grant the
> artifact authority.

Canonical templates therefore support consistent Engineering realization
while preserving the separation between representation, validation,
governance, and authority.
