# When Engineering Does Not Resolve Cleanly

> **Non-normative guidance**
>
> This guide explains how failure, conflict, uncertainty, and related conditions can be understood when applying the Engineering Operating Model. It does not establish new Engineering states, authority, lifecycle transitions, recovery procedures, or conformance requirements. The canonical Engineering Platform specifications remain authoritative.

## Purpose

Engineering does not always produce an immediately clean positive or negative outcome.

Relevant information may be incomplete. Evidence may conflict. An authoritative source or execution mechanism may be unavailable. Previously resolved context may become stale. Applicable authority or the applicability of particular Engineering semantics may remain unresolved.

These conditions do not need to be silently converted into stronger outcomes merely to allow the Engineering narrative to appear complete.

The important distinction is:

```text
Observed condition
        │
        ▼
Preserve what is known,
what is not known,
and the condition relating the two
        │
        ▼
Determine what the condition
actually affects
        │
        ▼
Do not infer a stronger or
unrelated Engineering outcome
```

This guide illustrates that distinction. The applicable canonical semantics govern what may subsequently be determined or established.

## Preserve the condition that exists

A condition should retain its Engineering meaning rather than being translated into a different condition for convenience.

For example:

```text
What happened                     What must not be inferred

source unavailable       ──────▶  source rejected the request

execution failed         ──────▶  Engineering failed

evidence incomplete      ──────▶  Engineering outcome failed

authority unresolved     ──────▶  authority was granted or denied

context stale            ──────▶  context remains current
```

The condition and its consequence are related, but they are not interchangeable.

A technical failure may prevent evidence from being produced. Missing evidence may leave a determination unresolved. Unresolved authority may prevent an authoritative action from being established.

None of those relationships permits one condition to be silently replaced by another.

The same principle applies whether the participant encountering the condition is human, AI, or automation.

## Common situations

### Information is stale

Consider an AI-assisted Engineering activity using Claude.

Claude resolves applicable Engineering context and uses that context while analyzing and realizing a change.

```text
Claude resolves applicable context
        │
        ▼
Engineering activity proceeds
        │
        ▼
authoritative source changes
        │
        ▼
Claude still retains
the earlier context
```

The earlier context may have been current when it was resolved. Its continued presence does not establish that it remains current after the authoritative source changes.

```text
previously current
        ≠
currently current
```

The earlier context should therefore not silently continue to represent current authoritative state.

This does not mean that stale context is necessarily false, rejected, unauthorized, or permanently unusable. It means that its currency relative to the applicable authoritative state can no longer be assumed.

Where current context is required for the Engineering activity, that concern remains unresolved until sufficiently current applicable context can legitimately support it.

### Something required is unavailable

Suppose an Engineering activity requires information from an authoritative source, but that source cannot currently be reached.

```text
Engineering activity
        │
        ▼
authoritative information required
        │
        ▼
source unavailable
        │
        ✕
source rejected the activity
```

Unavailability establishes that the required information cannot currently be obtained through that source. It does not by itself establish what the source would have returned.

Similarly:

```text
runtime unavailable
        ≠
Engineering failure

state mechanism unavailable
        ≠
loss of authority

provenance mechanism unavailable
        ≠
underlying Engineering activity did not occur
```

The practical consequence depends on what the unavailable source, mechanism, or capability is required to support.

A determination that materially depends on unavailable information must not be manufactured merely to permit progression. At the same time, unavailability does not universally invalidate unrelated Engineering state or require all Engineering activity to stop.

How the unavailable dependency is restored, substituted, retried, escalated, or otherwise handled depends on the applicable Engineering context and owning semantics. This guide does not prescribe a universal recovery procedure.

### Evidence does not agree

Engineering evidence may support different conclusions at different scopes or may materially conflict.

For example:

```text
Evidence A supports the expected behavior
                    +
Evidence B exposes an unsatisfied behavior
                    │
                    ▼
            conflict remains visible
```

The existence of conflict does not justify silently selecting whichever evidence supports the preferred outcome.

It also does not imply that every conflicting item has identical scope, authority, relevance, or evidential weight.

The applicable Engineering concern determines what the evidence needs to demonstrate. Until the material conflict is legitimately resolved, the conflict remains part of the Engineering condition.

The [Startup Team contextual example](../examples/contextual/startup_team.md) demonstrates this distinction through validation at different scopes.

### The available evidence is incomplete

Evidence may be valid without being sufficient for every Engineering concern.

```text
applicable evidence exists
            ≠
applicable claim demonstrated
```

A passing component test, successful execution, generated implementation, or successful AI activity may provide useful evidence about the concern it actually exercises.

That evidence does not automatically establish a broader Engineering outcome.

For example:

```text
component validation succeeds
        │
        ▼
evidence about component behavior
        │
        ✕
integrated behavior automatically established
```

Existing evidence need not become false merely because additional evidence is required. Its scope and what it legitimately supports remain important.

The affected concern remains unresolved where the available evidence is insufficient to support the applicable determination.

### Authority or applicability is unresolved

A participant may be technically capable of performing an action while the applicable authority for establishing that action remains unresolved.

```text
technical capability
        ≠
authority
```

If authority cannot currently be resolved:

```text
authority unresolved
        ≠
authority granted

authority unresolved
        ≠
authority denied
```

Access, authentication, responsibility, seniority, automation capability, or AI capability does not manufacture the missing authority.

Applicability follows the same preservation discipline.

```text
applicability unresolved
        ≠
applicable

applicability unresolved
        ≠
not applicable
```

Available information may help resolve authority or applicability. It does not permit uncertainty to be silently converted into the answer required for progression.

Unknown is not a disguised yes or a disguised no.

## What failure does not establish

A technical failure can be materially relevant to Engineering without automatically establishing a governed Engineering, Product, Collaboration, or Release outcome.

```text
A technical failure does not by itself establish:

├── an Engineering outcome
├── Capability non-acceptance
├── a Release Admission determination
└── a Release progression outcome
```

For example, an execution failure may mean that expected validation evidence was not produced.

That failure may therefore affect whether an Engineering concern can currently be demonstrated as satisfied.

It does not, merely by occurring, establish every subsequent determination that might depend on that evidence.

Likewise, a later Release-side failure does not by itself rewrite an Engineering outcome that was legitimately established earlier.

Each condition remains governed by the semantics applicable to that condition.

## Resolution without semantic rewriting

Preserving uncertainty, conflict, staleness, or unavailability does not mean that the condition must remain unresolved indefinitely.

Conditions change as Engineering progresses.

For example:

```text
10:00  authoritative source unavailable
          │
          ▼
10:05  source becomes available
```

The later availability does not make the earlier unavailability fictional. Both conditions can accurately describe different points in the Engineering history.

Staleness provides another example:

```text
source version A
        │
        ▼
context resolved and current
        │
        ▼
source changes to version B
        │
        ▼
earlier context becomes stale
        │
        ▼
context resolved against version B
        │
        ▼
new context current
```

Resolution therefore establishes a subsequent condition without requiring the earlier condition to be silently rewritten.

This distinction matters for continuity and provenance because changes in relevant context, evidence, determinations, and conditions may themselves form part of the Engineering history.

A later discovery may still require an earlier outcome to be reconsidered where the applicable Engineering semantics require it.

The rule is not that earlier outcomes can never change.

The rule is that a later condition does not silently rewrite what was legitimately known or established earlier. Its effect on previous outcomes remains governed by the applicable Engineering semantics.

## Related guidance and examples

For a short introduction to the Engineering Operating Model, see [`ORIENTATION.md`](../ORIENTATION.md).

The contextual examples show these distinctions inside complete Engineering narratives.

- [Startup Team](../examples/contextual/startup_team.md) demonstrates validation at different scopes and how successful evidence at one scope does not automatically establish sufficiency at another.
- [Enterprise IT Team](../examples/contextual/enterprise_it_team.md) demonstrates how Engineering context, applicability, evidence, and continuity can evolve when a change crosses organizational and domain boundaries.

These examples are non-normative. Their participants, tools, evidence, workflows, and organizational arrangements illustrate possible realizations rather than universal requirements.

## Canonical references

This guide is explanatory. Canonical definitions and requirements remain owned by the Engineering Platform specifications.

For the concepts discussed here, begin with:

- [Engineering Capability Model](../engineering_platform/specifications/capability_model_specification.md) — Engineering capabilities including Context Resolution & Composition, Execution Enablement, Governance & Validation Integration, and Continuity & Provenance.
- [Engineering Platform Realization Model](../engineering_platform/specifications/realization_model_specification.md) — realization contracts, boundaries, state characteristics, requirements, and invariants.
- [Engineering Platform Implementation Architecture](../engineering_platform/specifications/implementation_architecture_specification.md) — implementation responsibilities, failure and uncertainty preservation, execution boundaries, continuity, provenance, and implementation conformance.

Where a condition involves Product, Collaboration, Engineering, or Release semantics, the applicable owning System specification remains authoritative.
