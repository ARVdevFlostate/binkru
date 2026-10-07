# Evaluating Implementation Conformance

> **Non-normative guidance**
>
> This guide explains how implementation conformance can be evaluated against the Engineering Operating Model. It does not establish new conformance requirements, applicability rules, architectural obligations, evidence requirements, certification mechanisms, or implementation constraints. The canonical Engineering Platform specifications remain authoritative.

## Purpose

binkru defines an Engineering Operating Model without prescribing a particular software topology, technology stack, deployment platform, AI provider, or implementation framework.

That flexibility does not mean that every implementation is conforming merely because it describes itself using binkru terminology.

Implementation conformance concerns whether the applicable Engineering Platform architecture is actually realized while its required semantics, boundaries, state characteristics, conditions, and invariants are preserved.

A useful way to approach that question is:

```text
What implementation is being evaluated?
              │
              ▼
What canonical obligations apply?
              │
              ▼
Where and how are they realized?
              │
              ▼
What must remain preserved?
              │
              ▼
What must not be silently changed,
collapsed, inferred, or established?
              │
              ▼
What evidence demonstrates the
applicable conformance claims?
```

These questions are an explanatory way to reason about implementation conformance. They are not canonical conformance stages and do not prescribe an evaluation workflow.

## What conformance means

The Engineering Platform architecture defines a derivation from Engineering Capabilities toward concrete implementation:

```text
Engineering Capabilities
        ↓
Realization Mechanisms
        ↓
Platform Technical Responsibilities
        ↓
Logical Components
        ↓
Implementation Constructs
```

Implementation conformance is evaluated in the opposite direction:

```text
Engineering Capabilities
        ↑
Realization Mechanisms
        ↑
Platform Technical Responsibilities
        ↑
Logical Components
        ↑
Implementation Constructs
```

A concrete implementation should therefore be traceable upward to the Engineering responsibilities it realizes, while required architectural responsibilities should be traceable downward to something that actually realizes them.

This does not require one implementation construct for each logical component. A responsibility may be distributed across several constructs, and one construct may realize responsibilities associated with several logical components.

The important question is not whether the implementation resembles the architecture diagram physically.

The important question is whether the implementation satisfies the applicable architectural responsibilities and preserves the semantics and boundaries those responsibilities require.

For that reason, conformance is behavioral and semantic rather than nominal.

## Start with the evaluation scope

Before evaluating conformance, identify what implementation construct or implementation boundary the evaluation is actually about.

Depending on the implementation, the subject might be:

- a complete Engineering Platform realization;
- a collection of implementation components;
- an integration with an external Engineering information source;
- an execution-control realization;
- an execution runtime;
- a derived discovery facility; or
- another concrete realization of applicable Platform responsibilities.

The evaluation scope identifies the subject of the conformance claim. It does not create a conformance level or make canonical obligations optional.

```text
Evaluation scope
       +
applicable canonical architecture
       ↓
conformance claims that need
to be demonstrated
```

An implementation does not become conforming merely by narrowing its declared scope until an applicable responsibility disappears from the evaluation.

Whether a responsibility, contract, boundary, or invariant applies follows from the canonical Engineering architecture and the Engineering responsibilities being realized.

Where applicability itself is unresolved, that uncertainty should remain visible rather than being silently converted into applicability or non-applicability.

## Five concerns for evaluating conformance

The following five concerns provide an explanatory way to organize a conformance evaluation:

```text
Evaluation scope
      │
      ▼
 Applicability
      │
      ▼
  Realization
      │
      ▼
 Preservation
      │
      ▼
Non-violation
      │
      ▼
   Evidence
```

They are not mandatory stages, and an evaluation may move between them as understanding develops.

Evidence may expose a previously unrecognized implementation boundary. A realization mapping may reveal that a responsibility is externally delegated. An invariant may show that an apparently reasonable implementation choice changes an Engineering semantic.

The concerns therefore support reasoning rather than prescribing a sequence.

### Applicability

Ask:

> **Which canonical responsibilities, contracts, boundaries, requirements, and invariants apply to the implementation scope being evaluated?**

Applicability prevents two opposite errors.

The first is assuming that every possible implementation concern must appear identically in every realization.

The second is treating canonical obligations as elective because an implementation does not currently realize them or finds them inconvenient.

A conforming implementation may combine, distribute, delegate, specialize, or externally realize responsibilities where the canonical architecture permits it. Those implementation choices do not remove the obligation to satisfy the applicable Engineering semantics.

Applicability therefore depends on the Engineering responsibilities and semantics relevant to the evaluated realization, not merely on which requirements an implementation chooses to inspect.

### Realization

Ask:

> **Where and how are the applicable architectural responsibilities actually realized?**

The purpose of realization mapping is not to prove that implementation names resemble architectural names.

For example:

```text
Weak reasoning

"We have a service named after
the logical component."
              │
              ▼
       therefore conforming
```

A name does not demonstrate that the responsibility is actually performed or that its semantics are preserved.

A more useful line of reasoning is:

```text
Applicable Engineering Capability
              │
              ▼
Applicable Realization Mechanism
              │
              ▼
Applicable Technical Responsibility
              │
              ▼
Logical implementation responsibility
              │
              ▼
Concrete software / integration /
runtime / external realization
```

The mapping should work in both directions.

From the architecture downward:

> What actually realizes this required responsibility?

From the implementation upward:

> What architectural responsibility does this implementation behavior realize?

A missing implementation for an applicable responsibility is not repaired by naming another construct after it.

Likewise, an implementation construct must not silently acquire Engineering responsibilities or authority merely because it is technically capable of performing related operations.

### Preservation

Ask:

> **Does the implementation preserve the Engineering semantics required by the applicable architecture?**

Realizing a responsibility is not sufficient if its required meaning changes during implementation.

Depending on the applicable responsibility, preservation may include questions such as:

- Is the required responsibility actually performed?
- Are its Engineering semantics preserved?
- Are its architectural boundaries preserved?
- Can materially unresolved, conflicting, partial, stale, unavailable, or uncertain conditions remain distinguishable?
- Are applicable authority, durability, derivation, identity, scope, applicability, uncertainty, or provenance characteristics preserved across implementation boundaries?
- Are dependencies satisfied without creating circular establishment or hidden semantic ownership?
- Where responsibility is delegated, does the resulting realization actually satisfy the applicable contract?

For example, moving an Engineering representation between processes, services, databases, or external systems must not silently change its authority merely because its technical location changed.

Similarly:

```text
persisted
    ≠
authoritative

technically executable
    ≠
authorized to execute

execution success
    ≠
Engineering success

physical separation
    ≠
semantic boundary preservation
```

Implementation choices may change physical realization. They must not silently redefine applicable Engineering meaning.

For a focused explanation of preserving unresolved, conflicting, partial, stale, unavailable, and uncertain conditions, see [When Engineering Does Not Resolve Cleanly](failure_and_uncertainty.md).

### Non-violation

Ask:

> **What must the implementation not silently change, collapse, infer, or establish?**

Conformance is not demonstrated only by showing that required functionality exists.

An implementation may perform the expected technical operation while still violating an Engineering boundary.

For example:

```text
Authenticated participant
        │
        ✕
governed-work responsibility
```

Authentication can establish technical identity or access without establishing governed Engineering responsibility.

Similarly:

```text
Successful AI execution
        │
        ✕
Engineering completion
```

An AI participant may successfully generate or modify code, execute permitted tools, inspect results, or assemble evidence without execution success itself establishing the applicable Engineering outcome.

And:

```text
Cached authoritative representation
        │
source version changes
        ▼
must not silently remain "current"
```

Negative evaluation therefore asks whether the implementation prevents semantic shortcuts that would be architecturally invalid even when they appear technically convenient.

This is especially important for highly capable human, AI, and automation participants. Technical capability may improve what a participant can do; it does not manufacture authority, applicability, evidence sufficiency, or governed outcomes.

### Evidence

Ask:

> **What evidence demonstrates each material applicable conformance claim?**

A conformance assertion is not demonstrated merely because the implementation exists or because its architecture diagram uses binkru terminology.

Evidence should be associated with the claim being made.

Depending on the claim and implementation, useful evidence may include:

- architecture mappings;
- implementation specifications;
- tests;
- contract tests;
- integration tests;
- state-model tests;
- Architecture Decision Records;
- source-adapter tests;
- execution-boundary tests;
- provenance checks;
- continuity or reconstruction tests; or
- runtime observations.

No single evidence type is universally required.

Different claims may require different forms of evidence, and the same artifact may support more than one kind of reasoning.

For example, a test result may serve as Engineering evidence when it supports reasoning about a realized Engineering outcome.

The same test result may also serve as conformance evidence when it demonstrates that an implementation preserves a particular architectural responsibility or boundary.

```text
                Test result
                     │
             ┌───────┴───────┐
             ▼               ▼
   Engineering evidence   Conformance evidence

   supports reasoning     demonstrates an
   about an Engineering   applicable architectural
   outcome                conformance claim
```

The distinction is therefore not necessarily the artifact itself. It is the claim the evidence supports.

Evidence should follow the conformance claim rather than the existence of evidence being treated as proof of unspecified conformance.

## Conformance is semantic, not nominal

Implementation topology does not itself prove or disprove conformance.

For example, none of the following is sufficient by itself:

```text
seven logical components
        =
seven services

component name
        =
responsibility satisfied

separate processes
        =
semantic boundary preserved

shared database
        =
semantic responsibilities collapsed

external service
        =
applicable responsibility delegated correctly
```

A conforming implementation may use a compact process, several services, distributed infrastructure, external systems, replaceable runtimes, or other technical structures where the applicable contracts and architectural boundaries remain satisfied.

The reverse is equally important.

An implementation can reproduce canonical component names, diagrams, or repository structures and still fail to preserve the Engineering semantics those constructs represent.

Consider:

```text
Implementation A

C-01 service
C-02 service
C-03 service
C-04 service
C-05 service
C-06 service
C-07 service

        ≠ automatically conforming
```

and:

```text
Implementation B

one compact runtime
+
external integrations
+
replaceable execution runtime

        ≠ automatically non-conforming
```

The evaluation concerns what those implementations actually realize and preserve.

## A small worked evaluation

Suppose an implementation maintains a cache of an Engineering artifact obtained from an authoritative source.

The cache improves retrieval performance, but the source remains the applicable authoritative mechanism.

This small example can be evaluated using the five concerns.

### Applicability

The implementation is handling a representation whose source identity, authority, version, and currency may matter to Engineering reasoning.

For this example, the relevant architectural concerns include resolving Engineering information while preserving applicable source and state characteristics.

### Realization

The cache is part of the concrete implementation machinery used to make the Engineering artifact available.

Its presence does not make the cache itself authoritative.

The realization must retain the relationship between the cached representation and the authoritative source from which it was resolved.

### Preservation

Persisting the artifact in the cache must not silently change its authority characteristic.

```text
authoritative source
        │
        ▼
resolved representation
        │
        ▼
cached representation

persistence
    ≠
authority transfer
```

Relevant source identity, version, derivation, currency, and other applicable characteristics need to remain distinguishable where required by the canonical architecture.

### Non-violation

Suppose the authoritative source changes after the representation has been cached.

The cached representation must not silently continue to be treated as current merely because it remains technically available.

```text
cached representation
        │
source version changes
        ▼
still available
        │
        ✕
automatically current
```

The implementation must preserve the actual condition rather than converting technical availability into semantic currency.

### Evidence

Depending on the implementation and claim, supporting conformance evidence might include:

- an architecture mapping showing the authoritative source and cache relationship;
- implementation specifications describing source/version preservation;
- source-adapter or cache-invalidation tests;
- state-model tests demonstrating that persistence does not transfer authority; or
- runtime observations showing that a changed source version prevents the cached representation from silently remaining current.

The guide does not require these particular artifacts. They illustrate possible evidence for the claims in this example.

The relevant question is whether the applicable conformance claims can be demonstrated.

## What conformance does not imply

Implementation conformance does not inherently require:

- a particular programming language;
- a particular framework;
- a particular database;
- a particular AI model or provider;
- a particular agent framework;
- one service per logical component;
- seven deployable services;
- a particular repository structure;
- a particular network topology;
- a particular cloud platform;
- organizational teams that mirror Engineering Systems or logical components; or
- identical evidence across different implementations.

Conformance also does not, by itself, establish:

- an official binkru certification;
- a conformance score;
- a conformance percentage;
- a maturity level;
- a universal assessment status model;
- a mandatory audit procedure; or
- a special conformance category for human, AI, or automation realization.

Human, AI, and automation participation remain governed by the same applicable Engineering semantics.

An implementation technology may affect what evidence is useful. It does not create separate conformance semantics.

## Related guidance and examples

For a short introduction to the Engineering Operating Model, see [`ORIENTATION.md`](../ORIENTATION.md).

For guidance on preserving unresolved, conflicting, partial, stale, unavailable, and uncertain Engineering conditions, see [When Engineering Does Not Resolve Cleanly](failure_and_uncertainty.md).

For non-normative examples showing the same Engineering semantics operating across different organizational contexts, see the [Contextual Examples](../examples/contextual/).

These examples illustrate contextual realization. They are not conformance test suites or certification profiles.

## Canonical references

This guide is explanatory. The canonical Engineering Platform remains authoritative.

The primary canonical references for implementation conformance are:

- [Engineering Capability Model](../engineering_platform/specifications/capability_model_specification.md) — defines the Engineering Capabilities whose responsibilities the Platform must make operable.
- [Engineering Platform Realization Model](../engineering_platform/specifications/realization_model_specification.md) — defines the realization mechanisms, contracts, technical responsibilities, state characteristics, and invariants that implementation must preserve.
- [Engineering Platform Implementation Architecture](../engineering_platform/specifications/implementation_architecture_specification.md) — defines logical implementation responsibilities, implementation boundaries, deployment semantics, and the canonical conformance relationship from implementation constructs through the higher architecture.

Where a conformance question involves semantics owned by a particular Engineering System or another canonical specification, that owning specification remains authoritative for those semantics.
