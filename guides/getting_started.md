# Applying binkru to an Existing Engineering Environment

> **Non-normative adoption guide**
>
> This guide helps readers begin applying the Engineering Operating Model to an existing Engineering environment. It does not establish an adoption process, maturity model, implementation sequence, required organizational structure, or new Engineering semantics. The canonical Engineering Platform specifications remain authoritative.

## What this guide is for

You may understand the Engineering Operating Model and still have a practical question:

> **Where do I begin in my own Engineering environment?**

Most existing environments already have people, repositories, development workflows, review practices, automation, CI/CD, issue tracking, release mechanisms, AI tooling, governance practices, and sources of Engineering information.

Applying binkru does not inherently require replacing them.

The practical starting point is therefore not:

> Which binkru components should we implement?

A more useful question is:

> **Which concrete Engineering concern matters in our current context, what binkru semantics apply to it, and how is that concern represented today?**

This guide provides a way to reason about that question.

It is a reasoning aid, not a required adoption sequence.

---

## Do not begin by implementing the whole model

binkru defines four Engineering Systems and six Engineering Capabilities, together with realization and implementation architecture.

That does not mean adoption begins by creating a project for each System or Capability.

Applying binkru does not inherently mean:

- implementing every Engineering System at once;
- implementing every Engineering Capability at once;
- creating software components named after the model;
- replacing existing Engineering tools;
- copying one of the contextual examples;
- introducing enterprise-style governance ceremony;
- assigning every Engineering concern to a different person;
- creating a document for every canonical concept;
- completing an adoption checklist; or
- progressing through maturity levels.

Different Engineering environments may physically realize the same applicable semantics in very different ways.

Existing mechanisms may already satisfy some applicable responsibilities.

The first task is therefore to understand the Engineering concern and the environment in which it currently exists.

---

## Begin with a concrete Engineering concern

Choose a concern that already matters.

For example:

- AI can modify production code, but it is unclear what Engineering context should be provided to it.
- A deployment pipeline can release software, but technical deployment permission and Release authority are not clearly distinguished.
- Engineering decisions are made during conversations, but the evidence required to understand or resume the work is difficult to recover.
- Several sources describe the same Engineering state and sometimes disagree.
- A team can execute an Engineering activity, but it is unclear whether execution is currently available under the applicable Engineering conditions.
- Responsibility for an Engineering activity is understood informally, but the authority to establish its governed outcome is not.

The concern does not need to span the whole Engineering Operating Model.

A bounded concern is often more useful because applicability can be examined without turning adoption into a complete-model inventory.

> **Begin from an Engineering concern, not from a list of binkru components to implement.**

---

## Understand the current environment

Before proposing a new realization, describe what already exists around the concern.

Depending on the concern, this may include:

- participating humans, AI, and automation;
- repositories and source-control mechanisms;
- issue or work-management systems;
- Engineering documentation;
- CI/CD and execution mechanisms;
- review and approval practices;
- Product or Release governance;
- authoritative information sources;
- derived or cached Engineering information;
- evidence and provenance mechanisms;
- continuity or resumption practices; and
- external systems involved in the activity.

The purpose is not to produce a complete inventory of the organization.

Capture only what is materially relevant to the concern being examined.

At this point, avoid translating every existing mechanism into a binkru component merely because a similar name exists.

First understand what the mechanism actually does.

---

## Identify applicable Engineering semantics

With the concern and current environment understood, determine which canonical binkru semantics are applicable.

This may involve questions such as:

- Which Engineering System owns the relevant semantics?
- Which cross-system concerns are involved?
- Which Engineering Capabilities are needed by the participating actors?
- Which canonical state, lifecycle, authority, governance, validation, continuity, or provenance semantics apply?
- Which Realization Mechanisms or Technical Responsibilities become relevant if the concern is being implemented or evaluated technically?

Applicability is contextual.

Not every System, Capability, mechanism, responsibility, or specification must be involved in every concern.

But contextual adoption does not permit an applicable canonical responsibility to be ignored merely because the current realization does not represent it explicitly.

When applicability is unclear, preserve that uncertainty and consult the relevant canonical material rather than assuming an answer.

---

## Identify participants, responsibilities, and authority

For the concern being examined, identify who or what currently participates.

Participants may include:

- individual humans;
- teams;
- AI;
- automation;
- execution systems; or
- external services.

Then distinguish three questions:

```text
Who or what can participate?
            │
            ▼
What responsibility is being performed?
            │
            ▼
Where does authority to establish the
governed Engineering outcome reside?
```

These questions may produce different answers.

Technical capability, access, responsibility, and authority are not interchangeable.

For example, an AI participant may be technically capable of modifying code. A CI system may be technically capable of deploying it. A human may be technically capable of merging it.

None of those capabilities, by themselves, establish the Engineering or Release authority associated with the resulting governed outcome.

If authority is unresolved, record it as unresolved. Do not assign authority merely to complete the adoption exercise.

---

## Identify required context and information

Ask what information a participant needs for the activity or outcome being examined.

Relevant context may include:

- Product intent;
- Engineering state;
- applicable decisions;
- current work scope;
- authoritative source material;
- participant responsibility;
- applicable authority;
- governance or validation requirements;
- execution availability;
- relevant constraints;
- previous Engineering outcomes; and
- provenance required to understand how the current state arose.

Do not assume that more context is always better.

The objective is applicable Engineering context, not accumulation of every available artifact.

Also distinguish authoritative information from derived, cached, summarized, or otherwise non-authoritative representations.

Persisting, copying, summarizing, or presenting information does not by itself change its authority.

---

## Examine governance, evidence, and continuity

For the concern, ask what must remain demonstrable or recoverable.

Questions may include:

- What governed determination or outcome is being established?
- What validation applies?
- What evidence supports the resulting Engineering claim?
- What provenance is materially required?
- What must survive if a participant, AI session, automation run, or execution environment disappears?
- What information would another legitimate participant need to resume the Engineering activity?
- What unresolved, conflicting, partial, stale, unavailable, or uncertain conditions must remain visible?

Do not manufacture certainty merely because a workflow expects a completed field or binary answer.

The actual Engineering condition should remain distinguishable until applicable semantics legitimately change it.

For focused guidance on these conditions, see [`failure_and_uncertainty.md`](failure_and_uncertainty.md).

---

## Reuse what already works

Once the applicable responsibilities are understood, compare them with the current environment.

An existing mechanism does not need to use binkru terminology to be useful.

For each materially relevant responsibility, ask:

```text
What existing mechanism realizes this today?
                 │
                 ▼
Does it preserve the applicable
Engineering semantics and boundaries?
          ┌──────┼──────┐
          ▼      ▼      ▼
        yes   partly    no
          │      │      │
          ▼      ▼      ▼
       retain  strengthen
                 or      establish
                clarify   what is missing
```

The names of the tools or components do not establish conformance.

Likewise, the absence of a component named after a binkru concept does not establish a gap.

What matters is whether the applicable responsibility and semantic boundary are actually preserved.

---

## Keep gaps and uncertainty visible

The examination may reveal that something is not known or not sufficiently represented.

Examples include:

- authority is unresolved;
- two sources conflict;
- required context cannot currently be resolved;
- evidence is incomplete;
- information is stale;
- an execution capability is unavailable;
- responsibility is only partially represented; or
- the existing mechanism does not preserve a required semantic boundary.

These are useful findings.

Do not convert them into invented facts merely so the environment appears complete.

Instead, identify:

1. what is actually known;
2. what is not known;
3. what the condition affects;
4. what must not be inferred; and
5. which applicable semantics govern legitimate resolution.

The purpose of the adoption exercise is not to make every box green.

It is to make the actual Engineering condition understandable and governable.

---

## Establish only what is materially missing

After examining the concern, the result may be that much of the required realization already exists.

A material gap exists where an applicable Engineering responsibility, semantic distinction, boundary, state characteristic, governance requirement, continuity requirement, or other applicable obligation is not sufficiently represented or preserved.

The response to a gap depends on the gap.

It may involve:

- clarifying an existing responsibility;
- making an authority boundary explicit;
- changing how context is resolved;
- preserving additional evidence or provenance;
- strengthening an existing workflow;
- introducing a validation;
- changing an integration boundary;
- establishing durable state;
- modifying an execution control; or
- introducing a new implementation mechanism where no suitable realization currently exists.

Do not introduce new machinery merely to make the environment resemble the structure of the canonical documentation.

The physical realization should remain appropriate to the Engineering context.

---

## Re-evaluate as the Engineering context changes

A realization that is sufficient for one Engineering context may no longer be sufficient after the context changes.

For example:

- additional participants become involved;
- AI or automation receives broader technical capability;
- responsibility moves between participants;
- authority changes;
- new authoritative information sources are introduced;
- execution moves across a new boundary;
- governance obligations change;
- Release responsibilities become more complex; or
- continuity requirements increase.

Re-evaluation does not mean restarting an adoption process.

Return to the affected Engineering concern, resolve the current applicable semantics, and determine whether the existing realization still preserves them.

---

## A small worked adoption example

Consider a three-person software team.

The team already uses:

- GitHub for source control and pull requests;
- CI for automated validation;
- an existing deployment pipeline; and
- Claude Code for AI-assisted implementation.

The team is comfortable allowing Claude Code to modify application code.

A human reviews the pull request, CI passes, and someone with repository permission merges it.

The practical concern is:

> **What does the existing merge workflow actually establish, and is authority to conclude the Engineering work clear?**

### 1. Examine the existing environment

The team already has:

```text
Claude Code
     │
     ▼
code modification

GitHub pull request
     │
     ▼
human review

CI
     │
     ▼
automated validation

merge permission
     │
     ▼
repository state change
```

There is no immediate reason to replace any of these mechanisms.

### 2. Identify the applicable concern

The concern is not whether Claude Code can generate code or whether GitHub can merge it.

Those technical capabilities already exist.

The concern is whether the participants, responsibilities, validation, evidence, and authority associated with the Engineering outcome are sufficiently represented.

### 3. Separate capability from authority

Claude Code can modify code.

CI can execute validation.

A human can review the change.

A repository permission may allow a participant to merge it.

But:

```text
can modify
    ≠
may establish Engineering outcome

can validate
    ≠
may establish Engineering outcome

can merge
    ≠
may conclude Engineering work
```

The team therefore examines where the applicable authority actually resides rather than inferring it from GitHub permissions.

### 4. Examine what already works

The pull request may already provide useful scope and evidence.

CI may already satisfy part of the applicable validation responsibility.

Repository history may already preserve relevant provenance.

Human review may already realize part of the applicable governance.

These mechanisms should not be replaced simply because they were not designed using binkru terminology.

### 5. Identify the material gap

Suppose the team determines that the technical workflow is adequate but authority to establish the Engineering conclusion has never been made explicit.

That is the material gap.

The adoption response is not:

> Build a binkru Engineering Conclusion service.

It is:

> Establish a realization that preserves the applicable authority and conclusion semantics in this team's context.

That realization might use existing GitHub mechanisms, an existing Engineering record, another established source, or a combination of mechanisms.

The canonical semantics determine what must be preserved.

The implementation determines how it is realized.

### 6. Evaluate the resulting realization

Once the team has established or strengthened the realization, it can evaluate whether the implementation actually satisfies the applicable canonical obligations.

For that question, continue with [`conformance.md`](conformance.md).

---

## Where to go next

For a short introduction to the Engineering Operating Model, see [`../ORIENTATION.md`](../ORIENTATION.md).

To see the model operating across solo-developer, startup-team, and enterprise-IT contexts, explore the [`../examples/contextual/`](../examples/contextual/) examples.

For focused guidance on unresolved, conflicting, partial, stale, unavailable, or uncertain Engineering conditions, see [`failure_and_uncertainty.md`](failure_and_uncertainty.md).

To evaluate whether a concrete implementation satisfies applicable canonical obligations, see [`conformance.md`](conformance.md).

When governing detail is required, consult the canonical Engineering Platform under [`../engineering_platform/`](../engineering_platform/).

## Canonical references

This guide is explanatory. It does not replace the canonical Engineering Operating Model.

The principal canonical sources for the concerns discussed here are:

- [`../engineering_platform/README.md`](../engineering_platform/README.md) — Engineering Platform structure and canonical navigation.
- [`../engineering_platform/specifications/capability_model_specification.md`](../engineering_platform/specifications/capability_model_specification.md) — Engineering Capabilities and their semantic responsibilities.
- [`../engineering_platform/specifications/realization_model_specification.md`](../engineering_platform/specifications/realization_model_specification.md) — realization mechanisms, contracts, state characteristics, failure semantics, and invariants.
- [`../engineering_platform/specifications/implementation_architecture_specification.md`](../engineering_platform/specifications/implementation_architecture_specification.md) — technical responsibilities, logical implementation boundaries, state, execution, continuity, provenance, and conformance relationships.

Where a concern is owned by a specific Engineering System or cross-system specification, that owning canonical material remains authoritative.
