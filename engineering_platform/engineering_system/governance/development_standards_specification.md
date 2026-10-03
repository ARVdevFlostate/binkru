# Development Standards Specification

## 1. Purpose

This specification defines the governance model for Development Standards within the Engineering System.

Development Standards establish reusable, governed constraints, conventions, expectations, and practices that guide Engineering realization within a project.

This specification defines:

- what constitutes a Development Standard;
- when Development Standards are required;
- how Development Standards are established and changed;
- the minimum semantic contract of a Development Standard;
- how Development Standards relate to Architecture Decisions and other governed Engineering artifacts;
- how exceptions and deviations are governed;
- how Development Standards are maintained, superseded, and retired;
- how Development Standards are owned and maintained within a project;
- how Development Standards participate in Engineering Composition and Engineering realization;
- how Human Engineers, AI Engineers, and automation may interact with Development Standards;
- how provenance and traceability are preserved.

This specification governs Development Standards as an Engineering concept. It does not prescribe a specific serialization format, authoring tool, repository implementation, or automation mechanism.

---

## 2. Scope

This specification applies to Development Standards used to govern repeatable Engineering realization within a project.

Development Standards MAY address, among other concerns:

- programming languages;
- frameworks and libraries;
- databases and data technologies;
- APIs and integration practices;
- error handling;
- security practices;
- testing and validation;
- observability;
- infrastructure;
- accessibility;
- UI/UX and design implementation;
- source organization;
- dependency management;
- build and packaging practices;
- other recurring Engineering practices requiring governed consistency.

Development Standards SHALL apply only within their explicitly established scope.

This specification does not make a technology, practice, convention, or recommendation applicable merely because it exists.

---

## 3. Definition of a Development Standard

A **Development Standard** is a governed project-specific Engineering artifact that establishes reusable constraints, conventions, expectations, or practices applicable to a defined area of Engineering realization.

A Development Standard expresses how Engineering realization SHALL, SHOULD, or MAY proceed within its applicable scope where consistent repeatability is required.

Development Standards may be technology-specific or practice-specific.

Examples of technology-specific Development Standards include standards governing the project use of:

- Go;
- PostgreSQL;
- React;
- Kubernetes.

Examples of practice-specific Development Standards include standards governing:

- error handling;
- API design;
- accessibility;
- observability;
- UI/UX implementation;
- testing conventions.

Technology-specific Development Standards MAY be described as **Technology Standards** where that distinction is useful. Technology Standards remain Development Standards and are governed by this specification.

---

## 4. Development Standards Boundary

A Development Standard defines governed project Engineering practice.

A Development Standard is not general documentation about a technology or Engineering discipline.

The following SHALL NOT become Development Standards solely by being stored, copied, referenced, or made available within a project:

- vendor documentation;
- programming-language documentation;
- framework documentation;
- API references;
- tutorials;
- installation guides;
- external best-practice articles;
- general technology guidance;
- ungoverned team preferences;
- reference material.

Such material MAY be referenced by a Development Standard where it provides useful context, evidence, rationale, or provenance.

External documentation remains external reference material unless the applicable Engineering authority explicitly establishes project-specific requirements derived from it.

A Development Standard SHALL describe the project's governed use of a technology or Engineering practice rather than reproduce general documentation about that subject.

---

## 5. Governance Principles

Development Standards SHALL conform to the following principles.

### 5.1 Project Specificity

Development Standards SHALL be established within the context of an applicable project.

The existence of a Development Standard within one project SHALL NOT make that standard authoritative for another project.

Reusable knowledge MAY inform standards in multiple projects, but applicability and authority SHALL be established independently for each applicable project.

### 5.2 Explicit Applicability

Every Development Standard SHALL define sufficient applicability information to determine when the standard governs Engineering realization.

Applicability SHALL NOT be inferred solely from file location, file name, technology availability, tool behavior, or automation behavior.

### 5.3 Governed Establishment

A proposed Development Standard SHALL NOT become authoritative merely because it has been authored, generated, committed, discovered, or technically enforced.

A Development Standard becomes governed only when established by the applicable Engineering authority.

### 5.4 Authority Preservation

Technical ability to create, modify, validate, enforce, or apply a Development Standard SHALL NOT itself grant authority to establish or change that standard.

Development Standards SHALL preserve the authority model established by the Engineering System.

### 5.5 Reusable Engineering Guidance

Development Standards SHOULD govern concerns sufficiently recurring or material to justify consistent reuse.

Development Standards SHOULD NOT be created for isolated implementation details that do not require reusable governance.

### 5.6 Traceability

Development Standards SHALL preserve sufficient provenance and traceability to understand their governing basis, applicability, material evolution, and relationship to applicable Engineering decisions.

---

## 6. Development Standard Qualification

Development Standards SHALL be established when an Engineering concern requires reusable governed consistency across applicable Engineering realization.

Applicable Development Standards SHALL be established before governed Engineering realization relies upon the corresponding technology or practice where the required constraints, conventions, or expectations are already known.

A project SHALL NOT intentionally defer known material Development Standards merely to allow realization to begin without them.

Development Standards MAY subsequently be introduced or evolved when Engineering realization, validation, operational experience, Architecture Decisions, or other governed Engineering activity reveals additional reusable constraints, conventions, expectations, or practices.

The absence of complete future knowledge SHALL NOT require speculative Development Standards to be created before Engineering realization begins.

The governing principle is:

> Standardize what must be known before realization; govern what is learned during realization.

A proposed standard SHOULD therefore represent either:

1. a known constraint, convention, expectation, or practice required before applicable realization proceeds; or
2. sufficiently stable Engineering knowledge discovered through realization or experience that now warrants governed reuse.

---

## 7. Required Semantic Contract

Every Development Standard SHALL preserve, either directly or through governed relationships, the following semantic elements.

### 7.1 Identity

The Development Standard SHALL have a stable identity sufficient for traceability and reference.

### 7.2 Subject

The Development Standard SHALL identify the technology, Engineering practice, concern, or combination of concerns that it governs.

### 7.3 Applicability

The Development Standard SHALL establish the scope and conditions under which it applies.

### 7.4 Governance Status

The Development Standard SHALL make its current governance status determinable.

It SHALL be possible to distinguish an established Development Standard from a draft, candidate, superseded, retired, or otherwise non-current standard.

This requirement does not prescribe specific status names.

### 7.5 Governing Basis

The Development Standard SHALL preserve traceability to applicable authoritative Engineering decisions, constraints, evidence, requirements, or other governing basis where such basis exists.

### 7.6 Normative Content

The Development Standard SHALL clearly establish the reusable constraints, conventions, expectations, or practices that constitute the standard.

Normative requirements SHOULD be distinguishable from explanatory material, examples, rationale, and references.

### 7.7 Exception Semantics

The Development Standard SHALL identify how deviations from applicable normative requirements are governed or reference the applicable Engineering exception mechanism.

### 7.8 Provenance

The Development Standard SHALL preserve sufficient provenance to understand why material requirements were established.

### 7.9 Evolution

Where a Development Standard supersedes, replaces, or retires another standard, the relationship SHALL remain traceable.

---

## 8. Applicability

A Development Standard SHALL govern only Engineering realization within its established applicability.

Applicability MAY depend upon factors including:

- project scope;
- technology adoption;
- component type;
- architectural boundary;
- Engineering concern;
- runtime environment;
- delivery context;
- other explicitly governed conditions.

A Development Standard SHALL NOT silently broaden its own applicability.

Where applicability is ambiguous, the ambiguity SHALL be resolved through applicable Engineering governance rather than inferred by an execution mechanism.

Conflicting applicable Development Standards SHALL be surfaced for resolution and SHALL NOT be silently reconciled by Human Engineers, AI Engineers, automation, or composition mechanisms without applicable authority.

---

## 9. Relationship to Engineering Governance

Development Standards operate within the Engineering governance model and SHALL NOT create an independent authority domain.

Applicable Engineering authority governs establishment, material change, exception, supersession, and retirement according to the scope and significance of the Development Standard.

This specification SHALL NOT require a universal organizational role such as a Development Standards Owner.

Responsibility for authoring, maintaining, reviewing, or technically enforcing a Development Standard SHALL NOT be conflated with authority to establish the governed standard.

Development Standards SHALL NOT override higher-authority Engineering decisions or constraints.

Where a conflict exists, applicable Engineering governance SHALL resolve the conflict.

---

## 10. Relationship to Architecture Decisions

Development Standards and Architecture Decisions serve different purposes.

An Architecture Decision establishes a material architectural decision where Architecture Decision governance applies.

A Development Standard establishes reusable Engineering constraints, conventions, expectations, or practices within the architectural and Engineering basis applicable to the project.

A Development Standard MAY derive from or reference one or more Architecture Decisions.

A Development Standard SHALL NOT silently establish or materially alter an Architecture Decision where Engineering governance requires that decision to be governed independently.

Where creation or maintenance of a Development Standard reveals a material architectural question:

1. the architectural question SHALL be governed through the applicable Architecture Decision mechanism;
2. the resulting authoritative decision SHALL be preserved according to Architecture Decision governance; and
3. the Development Standard MAY subsequently be established or updated consistently with that decision.

Not every Development Standard requires a dedicated Architecture Decision.

Where no applicable Architecture Decision exists, the Development Standard SHALL preserve traceability to whatever legitimate Engineering basis establishes its requirements.

---

## 11. Establishment and Change

A Development Standard MAY be authored or proposed by an applicable Human Engineer, AI Engineer, automation mechanism, or combination thereof.

Authorship SHALL NOT establish authority.

Before becoming authoritative, a Development Standard SHALL be subject to the applicable Engineering governance necessary for its scope and materiality.

Once established, a Development Standard becomes part of the governed Engineering context for realization within its applicable scope.

Material changes to an established Development Standard SHALL be governed.

A Development Standard SHOULD evolve when:

- applicable Architecture Decisions change;
- adopted technologies materially change;
- Engineering realization reveals reusable improvements or constraints;
- recurring exceptions indicate that the standard no longer represents appropriate project practice;
- validation or operational evidence exposes deficiencies;
- project requirements materially alter applicability.

Changes SHALL preserve sufficient history and provenance to understand material evolution.

---

## 12. Exceptions and Deviations

Applicability of a Development Standard does not imply that deviation can never occur.

Where Engineering realization requires deviation from an applicable Development Standard, the deviation SHALL be explicit and governed according to the authority appropriate to its scope and materiality.

A governed deviation SHALL preserve sufficient information to determine:

- the applicable Development Standard;
- the requirement being deviated from;
- the affected Engineering scope;
- the rationale;
- the applicable authority or governed basis;
- relevant evidence or consequences where required.

A deviation SHALL NOT silently modify the Development Standard itself.

Recurring or materially significant deviations SHOULD trigger reassessment of the applicable Development Standard.

Human Engineers, AI Engineers, automation mechanisms, and execution tooling SHALL NOT silently ignore applicable Development Standards.

---

## 13. Supersession and Retirement

A Development Standard MAY be superseded when a new governed standard replaces all or part of its applicability.

Supersession SHALL preserve traceability between the superseded standard and its successor.

A Development Standard MAY be retired when its governed requirements are no longer applicable.

Retirement MAY occur because:

- the governed technology is no longer used;
- the governed practice no longer applies;
- project architecture has changed;
- another Development Standard subsumes the requirements;
- the applicable Engineering concern no longer requires governed standardization.

Superseded or retired Development Standards SHALL NOT silently remain applicable to new Engineering realization.

Historical standards MAY remain available where required for provenance, historical interpretation, auditability, or understanding previously realized Engineering outcomes.

---

## 14. Project Ownership and Repository Placement

The Engineering System owns the semantic definition and governance model for Development Standards.

Individual projects own the Development Standard instances applicable to their Engineering realization.

Project-specific Development Standards SHALL therefore be maintained within the applicable project context rather than as universal standards within the reusable Engineering System.

A project MAY maintain Development Standards within a repository area such as:

`<project>_home/development_standards/`

The specific physical repository organization is an implementation concern provided that semantic identity, applicability, governance, provenance, and discoverability are preserved.

Repository placement SHALL NOT itself establish authority.

A Development Standard from one project SHALL NOT automatically become applicable to another project through copying, reuse, import, tooling, or automation.

---

## 15. Reference Implementations, Boilerplates, and Templates

Development Standards MAY reference reusable implementation assets that assist Engineering realization.

Such assets MAY include:

- boilerplate implementations;
- reference implementations;
- templates;
- scaffolding;
- configuration examples;
- validation assets;
- other reusable Engineering implementation material.

A referenced implementation asset SHALL NOT be conflated with the Development Standard itself.

The Development Standard establishes the applicable normative Engineering requirements.

A boilerplate, template, or reference implementation provides one possible mechanism for realizing some or all of those requirements.

A Development Standard MAY require use of a particular governed implementation asset where applicable Engineering authority explicitly establishes that requirement.

Otherwise, conformance to a Development Standard SHALL NOT imply mandatory use of a particular reference implementation merely because that implementation is referenced.

Changes to a boilerplate, template, or reference implementation SHALL NOT silently change the normative meaning of the governing Development Standard.

Similarly, changes to a Development Standard SHALL trigger reassessment of referenced implementation assets where those assets may no longer conform.

---

## 16. Engineering Composition and Consumption

Applicable Development Standards form part of the governed Engineering context available to Engineering Composition and Engineering realization.

Engineering Composition MAY resolve and include applicable Development Standards when preparing execution context.

Composition SHALL preserve:

- Development Standard identity;
- applicability;
- normative requirements;
- relevant governing basis;
- applicable exceptions;
- provenance required for trustworthy use.

Composition SHALL NOT silently:

- alter a Development Standard;
- broaden or narrow its applicability;
- resolve conflicting standards without authority;
- create an exception;
- convert a draft or candidate standard into an established standard;
- establish new normative requirements.

An execution context derived from Development Standards SHALL remain subordinate to the authoritative Development Standards from which it was composed.

---

## 17. Automation and AI Assistance

Human Engineers, AI Engineers, and automation MAY assist with Development Standards.

Assistance MAY include:

- drafting candidate Development Standards;
- identifying recurring Engineering practices suitable for standardization;
- discovering applicable Development Standards;
- resolving standards into Engineering context;
- comparing Engineering realization against normative requirements;
- identifying potential non-conformance;
- identifying conflicting or stale standards;
- collecting supporting evidence;
- proposing updates;
- identifying applicable boilerplates, templates, or reference implementations;
- preserving provenance and traceability.

Technical capability SHALL NOT grant governance authority.

An AI Engineer or automation mechanism SHALL NOT establish, materially change, supersede, retire, or authorize deviation from a Development Standard unless the applicable Engineering governance explicitly grants the corresponding authority through an established mechanism.

Automated validation MAY provide evidence of conformance or non-conformance.

Automated validation SHALL NOT itself establish a governed Engineering decision unless the applicable Engineering governance explicitly defines that validation result as authoritative for the relevant decision.

---

## 18. Representation

Development Standards are defined by their governed semantics rather than their serialization format.

A Development Standard MAY use a representation suitable for its content and intended consumers.

Representations MAY include:

- Markdown;
- YAML;
- another structured format;
- a combination of human-readable and machine-readable representations.

For example, a UI/UX Development Standard may benefit from a primarily explanatory human-readable representation, while a technology-specific or mechanically validated Development Standard may benefit from structured representation.

This specification SHALL NOT prescribe a universal file format for Development Standards.

Regardless of representation, the required semantic contract defined by this specification SHALL remain preservable and determinable.

Where multiple representations describe the same Development Standard, the authoritative relationship between those representations SHALL be explicit so that conflicting representations cannot independently establish competing truth.

---

## 19. Provenance and Traceability

Development Standards SHALL preserve sufficient provenance to support trustworthy Engineering use.

Where applicable, traceability SHOULD allow an Engineer or authorized mechanism to determine:

- why the standard exists;
- what Engineering basis supports it;
- which Architecture Decisions materially influence it;
- when it became applicable;
- what material changes occurred;
- what it superseded;
- whether it has been superseded or retired;
- what exceptions materially affect its application;
- which implementation assets are associated with it.

Traceability SHALL support understanding without requiring Development Standards to duplicate the authoritative content of related Engineering artifacts.

References SHALL preserve semantic boundaries between the Development Standard and the artifacts or evidence it references.

---

## 20. Conformance Requirements

A project conforms to this specification when:

1. Development Standards are project-specific governed Engineering artifacts.
2. Applicable known Development Standards are established before governed realization relies upon the corresponding technology or practice where the necessary requirements are already known.
3. Development Standards may evolve as additional reusable Engineering knowledge emerges.
4. Development Standards preserve the required semantic contract.
5. Applicability is explicit and determinable.
6. Development Standards are established and materially changed through applicable Engineering authority.
7. Development Standards do not silently establish or alter Architecture Decisions.
8. Deviations from applicable Development Standards are explicit and governed.
9. Supersession and retirement preserve traceability.
10. Project-specific standards are maintained within the applicable project context.
11. General technology documentation is not misrepresented as a Development Standard.
12. Boilerplates, templates, and reference implementations remain semantically distinct from the standards they support.
13. Engineering Composition preserves the authority and semantics of applicable Development Standards.
14. Human, AI, and automated assistance does not manufacture governance authority.
15. Representation choices preserve the governed semantic contract.
16. Provenance and traceability remain sufficient to support trustworthy Engineering realization.

Failure to satisfy these requirements SHALL be treated as a Development Standards governance deficiency and resolved through applicable Engineering governance.
