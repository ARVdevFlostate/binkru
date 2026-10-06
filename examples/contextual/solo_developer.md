# Solo Developer

**Example version:** 1.0.0

> **Non-normative example**
>
> This example illustrates one possible realization of the Engineering Operating Model in a solo-developer context. It does not establish Engineering semantics or prescribe a required implementation. Where this example differs from the canonical Engineering Operating Model, the canonical model governs.

## About this example

This example follows a customer account-deletion capability from Product intent through Engineering and Release in a solo-developer context with AI and automation participation.

## Scenario

### Product intent

> **A signed-in customer must be able to permanently delete their account.**

### Why this capability matters

A customer account represents persistent state associated with a customer and their use of a product. Providing permanent account deletion gives the customer a way to end that continued account existence.

The change is meaningful from an Engineering perspective because deletion is destructive and may be difficult or impossible to reverse. Its realization can affect authentication, persisted account state, dependent data, customer-facing behavior, failure handling, and the evidence needed to determine whether the intended capability has been realized correctly.

This makes account deletion useful for demonstrating continuity from Product intent through Engineering realization, governed outcomes, and Release without requiring a specialized application domain.

The scenario does not imply that every product must provide account deletion. The capability is the Product intent established for this example.

### Engineering context

An existing customer-facing application allows customers to create an account, sign in, and use functionality associated with that account.

The application does not currently provide a way for a signed-in customer to permanently delete their account.

The requested capability therefore requires an Engineering change to the existing product.

### Scenario assumptions

For this example:

- the product already exists and is operational;
- customers authenticate before using account-specific functionality;
- customer accounts have persisted associated state;
- permanent account deletion is a newly requested Product capability;
- the capability requires Engineering realization before it can become part of the product; and
- AI and automation may participate in Engineering activity but their participation does not alter the applicable authority semantics.

## Participants and authority

This example has one human participant: the solo developer. The same person carries several capacities that might be distributed across different people in another organizational context.

Those capacities remain semantically distinct even though one person performs them.

| Participant | Illustrative participation | Authority relevant to this example |
| --- | --- | --- |
| Solo developer | Establishes Product intent, performs Engineering activity, evaluates the Engineering outcome, evaluates the realized capability against Product intent, performs applicable Collaboration determinations, and performs applicable Release activity | Carries the applicable authority associated with the distinct Product, Engineering, capability-evaluation, Collaboration, and Release capacities established for this realization |
| Claude / Claude Code | Assists with codebase analysis, Engineering planning, implementation, validation, and investigation of failures | Participates in Engineering activity but does not gain Engineering authority merely from its technical capability, access, or contribution |
| CI automation | Executes automated validation and produces results that may contribute Engineering evidence | Produces execution results and evidence but does not independently establish governed Engineering determinations merely because validation succeeds |

### One person, distinct capacities

The solo developer may act in several capacities during the same Engineering change:

- in a **Product capacity**, establishing the intended customer capability;
- in an **Engineering capacity**, determining and realizing the Engineering change and establishing the Engineering Conclusion where applicable authority resides with that capacity;
- in a **capability-evaluation capacity**, determining whether the realized capability satisfies the Product-owned intent;
- in a **Collaboration capacity**, performing applicable cross-system determinations such as Release Admission; and
- in a **Release capacity**, performing applicable Release activity.

Concentrating these capacities in one person reduces the need to coordinate across multiple human participants. It does not merge their semantics.

For example, concluding that the Engineering work has satisfied its applicable Engineering obligations is not the same determination as deciding whether the resulting capability satisfies the Product intent. The same person may perform both determinations while acting in different capacities.

Likewise, technical ability does not determine authority. The solo developer's ability to modify the repository does not by itself establish every authority relevant to the change.

### AI-assisted Engineering

This example uses **Claude and Claude Code** as illustrative AI-assisted Engineering tooling.

A paid Claude subscription providing Claude Code access is required to reproduce the example as written. Claude is an implementation choice for this example, not a requirement of the Engineering Operating Model.

Claude may participate substantially in the Engineering work. For example, it may inspect the codebase, identify affected areas, propose an Engineering approach, modify code, create or modify tests, execute available tooling, analyze failures, and help assemble relevant evidence.

The extent of that participation does not independently change its authority.

A successful Claude Code execution does not by itself establish that:

- the Engineering work is concluded;
- the realized capability satisfies the Product intent;
- the Engineering outcome is admitted to a Release; or
- the Release is authorized to progress.

Those remain governed determinations established through the applicable authority and semantics of the Engineering Operating Model.

### Automation participation

CI automation may build the changed product, execute tests and other automated checks, and preserve their results as Engineering evidence.

Those results can materially inform Engineering evaluation. They do not become an Engineering Conclusion merely because the automated checks report success.

Similarly, failed automated validation is meaningful evidence. It can identify a deficiency or unresolved condition that requires further Engineering activity rather than being discarded simply because it does not support the desired outcome.

## What applies in this example

The account-deletion capability crosses several governed concerns in the Engineering Operating Model. The following Systems and Engineering Capabilities are relevant to the realization shown in this example.

### Systems

| System | Relevance in this example |
| --- | --- |
| Product System | Owns the intended customer capability that the Engineering change is intended to realize |
| Collaboration System | Supports the transition between Product and Engineering concerns and the applicable Capability Acceptance and Release Admission determinations |
| Engineering System | Governs the Engineering work through realization, evidence, evaluation, and Engineering Conclusion |
| Release System | Governs the established Release and its progression |

All four Systems appear because this particular example follows the capability from Product intent through Engineering and Release. Their presence here does not imply that every Engineering situation must exercise every System.

### Engineering Capabilities

| Engineering Capability | How it appears in this example |
| --- | --- |
| Discovery & Navigation | Relevant product, codebase, Engineering, and validation information is located as the change is understood and realized |
| Participation & Scope | The applicable participants, capacities, Engineering scope, and boundaries of participation are established for the work |
| Context Resolution & Composition | Relevant context is resolved and composed for the Engineering activity being performed rather than accumulating all available information |
| Execution Enablement | The solo developer, Claude, and automation are prepared to perform applicable Engineering activity using the context and constraints relevant to that activity |
| Governance & Validation Integration | Engineering evidence, validation results, and governed determinations remain connected without treating successful execution as authority |
| Continuity & Provenance | Product intent, Engineering decisions, realization, evidence, and governed outcomes remain sufficiently connected to preserve the history and meaning of the change |

These Capabilities describe Engineering abilities exercised by the example. They do not prescribe particular tools, artifacts, services, or implementation components.

### Governed concerns

As the example progresses, several governed concerns become important:

- the Product-owned intended capability;
- sufficient context for the capability to become actionable for Engineering;
- Engineering realization and supporting evidence;
- Engineering Conclusion;
- evaluation of the realized capability against Product intent;
- Release establishment;
- Release Admission; and
- Release progression.

The Engineering journey introduces these concerns when they become relevant rather than treating them as a mandatory sequence or universal checklist.

## Engineering journey

The following journey shows one possible realization of this Engineering change. The stages provide a chronological narrative for the example; they do not define a mandatory sequential process. Engineering activity may return to an earlier concern when new evidence, uncertainty, or understanding requires it.

### 1. Establish the intended capability

The solo developer begins in a Product capacity and establishes the intended customer capability:

> **A signed-in customer must be able to permanently delete their account.**

At this point, the Product intent establishes what capability is wanted. It does not yet prescribe how account deletion will be implemented.

The solo developer therefore does not treat an assumed technical solution as part of the Product intent. Questions about interfaces, affected account state, implementation structure, validation, and failure behavior remain Engineering concerns to be resolved as the change becomes actionable.

### 2. Prepare the change for Engineering

The solo developer next considers the capability in an Engineering capacity and determines what must be understood before realization can proceed responsibly.

The existing application and relevant Product context are examined to establish the Engineering scope. This includes understanding:

- how a signed-in customer is identified;
- what persisted state is associated with an account;
- what other product behavior depends on the continued existence of that account;
- what "permanently delete" needs to mean for this product;
- what should be true after successful deletion;
- what could leave the deletion incomplete or unsuccessful; and
- what remains uncertain and requires further investigation.

The purpose is not to accumulate every piece of information available about the product. It is to resolve enough applicable context to make the requested capability actionable for Engineering.

If required information cannot be established, the solo developer keeps that uncertainty visible rather than inventing an answer simply to allow implementation to begin.

### 3. Determine the Engineering approach

With the relevant Engineering context established sufficiently to proceed, the solo developer begins determining how the capability can be realized.

Claude Code participates in this activity by inspecting the existing codebase and other available Engineering information. It may help identify account-related components, authentication behavior, persisted account-associated state, dependent functionality, existing validation, and areas likely to be affected by deletion.

The solo developer evaluates this analysis rather than treating Claude's findings as authoritative merely because they were produced by the AI tooling.

Together, the human and AI-assisted Engineering activity can explore questions such as:

- where account deletion behavior should enter the existing product;
- which persisted state and dependent behavior are affected;
- what conditions must hold before deletion can proceed;
- how incomplete or failed deletion should be handled;
- what observable behavior would demonstrate successful realization; and
- what validation would provide useful evidence about the resulting Engineering outcome.

The resulting Engineering approach is based on the applicable Product and Engineering context discovered for the actual product. The example does not require a particular API design, persistence strategy, application architecture, or deletion mechanism.

Where analysis exposes missing or conflicting information, the Engineering approach remains open until that condition is sufficiently resolved.

### 4. Plan the realization

Once there is sufficient understanding of the intended capability, affected Engineering scope, and proposed approach, the solo developer plans the realization.

The work may be decomposed into manageable Engineering pieces where that helps execution and evaluation. For this capability, those pieces might concern:

- the customer interaction that initiates deletion;
- authenticated handling of the deletion request;
- treatment of account-associated persisted state;
- behavior of functionality that depends on the deleted account;
- failure and partial-completion behavior; and
- validation of the resulting capability.

These are illustrative planning concerns, not a required decomposition or universal set of Engineering Slices.

Claude may assist by proposing a plan, identifying dependencies, highlighting potentially affected areas, and suggesting validation activities. The solo developer evaluates and adjusts that plan against the applicable Engineering context.

Planning also identifies where uncertainty remains. A plan does not turn an unresolved assumption into established Engineering context merely by recording it.

At this point, the work is sufficiently prepared for realization, while the implementation remains free to evolve as Engineering activity produces new evidence and understanding.

### 5. Realize the capability

The solo developer begins realizing the planned change with Claude Code participating as an AI-assisted Engineering participant.

The context provided to Claude is composed for the Engineering activity being performed. It may include the intended capability, relevant Engineering decisions, affected code and interfaces, applicable constraints, validation expectations, and unresolved conditions that must remain visible.

The objective is to provide the context needed for the activity rather than transferring every available Product and Engineering artifact into the AI interaction.

Claude Code may then:

- inspect relevant implementation areas in greater detail;
- propose or modify code;
- create or update automated tests;
- execute available development and validation tooling;
- analyze failures and unexpected behavior; and
- propose corrections or further investigation.

The solo developer evaluates the resulting changes and analysis against the applicable Engineering context. Claude's ability to modify files, execute commands, or produce a technically plausible implementation does not independently establish that the change is correct or complete.

Automation may also participate during realization. Tests, static analysis, builds, or other applicable automated checks can execute repeatedly as the implementation develops and produce evidence about the current state of the work.

Realization may expose information that changes the Engineering understanding of the work. If implementation reveals an incorrect assumption, an unknown dependency, or an unresolved condition, the solo developer returns to the relevant Engineering concern rather than treating the existing plan as fixed.

The plan guides realization; it does not prevent Engineering understanding from evolving.

### 6. Validate the Engineering outcome

As the capability is realized, the solo developer evaluates the resulting Engineering change using evidence appropriate to the applicable Engineering scope.

Validation may include, where relevant:

- automated tests for successful account deletion;
- validation of authentication and authorization behavior around the deletion operation;
- tests or inspection of account-associated persisted state;
- checks of functionality that previously depended on the account;
- validation of expected failure behavior;
- static analysis, builds, or other applicable automated checks; and
- direct inspection or execution of the resulting customer behavior.

Validation is not limited to demonstrating the expected successful path.

For example, suppose Claude implements the primary account-deletion behavior and the existing automated checks pass. During further validation, an integration test added for the change reveals that some account-associated state remains after the account is deleted.

The failed integration test is meaningful Engineering evidence.

The successful checks do not override that evidence, and the unresolved condition is not discarded merely because most of the implementation appears to work. The Engineering work returns to investigation and realization.

Claude Code may inspect the failure, identify the affected implementation, propose a correction, and update relevant tests. The solo developer evaluates the proposed change, and the applicable validation is performed again.

The resulting feedback loop can be represented as:

```text
realization
    ↓
validation
    ↓
evidence
    ↓
deficiency or uncertainty?
    │
    ├── yes → investigate → revise realization → validate again
    │
    └── no  → continue Engineering evaluation
```

Evidence accumulated through this work may include implementation changes, Engineering decisions, automated test results, observed behavior, failure results, corrections, and subsequent validation.

No individual evidence item establishes Engineering completion by itself.

In particular:

**Claude reports completion ≠ Engineering Conclusion**

**Automated checks pass ≠ Engineering Conclusion**

The evidence informs the applicable Engineering evaluation. Its origin in human activity, AI-assisted activity, or automation does not by itself determine either its sufficiency or the authority of the resulting determination.

### 7. Conclude the Engineering work

Once the applicable Engineering scope has been realized and evaluated, the solo developer considers whether the Engineering work can be concluded.

The Engineering Conclusion is not established merely because implementation activity stopped, Claude completed its requested tasks, or the latest automated checks passed.

The conclusion is informed by the applicable Engineering scope, the resulting realization, and the relevant evidence accumulated through implementation and validation. Previously identified deficiencies and unresolved conditions must be considered as part of that evaluation.

The relationship can be represented as:

```text
applicable Engineering scope
        +
Engineering realization
        +
relevant evidence
        ↓
applicable Engineering evaluation
        ↓
Engineering Conclusion
```

In this realization, the solo developer carries the applicable Engineering authority and, acting in an Engineering capacity, establishes the Engineering Conclusion for the applicable scope.

The Engineering Conclusion establishes the governed Engineering outcome. The evidence supports that determination; it is not itself the determination.

This distinction remains important even in a solo-developer context. The same person may have performed the implementation, observed the validation results, evaluated the evidence, and established the Engineering Conclusion, but those activities do not become semantically identical merely because one person performs them.

The Engineering Conclusion also does not determine whether the realized capability satisfies the Product intent.

That evaluation remains a separate governed concern.

Likewise, Engineering Conclusion does not establish a Release, determine Release Admission, or authorize Release progression. Those concerns occur later in the journey.

### 8. Evaluate the realized capability

With the Engineering work concluded, the realized capability can be evaluated against the Product intent:

> **A signed-in customer must be able to permanently delete their account.**

In this example, the solo developer performs this evaluation in a capability-evaluation capacity.

The evaluation considers whether the realized capability satisfies the applicable Product-owned intent. Engineering evidence produced during realization and validation may inform that evaluation, but the Engineering Conclusion does not automatically establish the result.

For example, the evaluation may consider whether a signed-in customer can initiate permanent account deletion and whether the resulting customer-visible behavior is consistent with the intended capability.

If the realized capability does not satisfy the Product intent, that result remains visible. It does not become an Engineering deficiency merely because Capability Acceptance was not established. The reason for non-acceptance must be understood in its applicable context and may lead to further Product, Collaboration, or Engineering activity.

In this realization, the evaluation determines that the realized capability satisfies the applicable Product intent, establishing Capability Acceptance for that capability.

The same person established the Engineering Conclusion and Capability Acceptance, but did so in distinct capacities and through distinct determinations.

### 9. Establish the Release

The concluded Engineering outcome is next considered for inclusion in a Release.

In this example, the solo developer performs the applicable Release activity and establishes the Release for which the account-deletion outcome will be considered.

Release establishment identifies the Release that is to be governed. It does not by itself determine that the Engineering outcome is admitted to that Release or that the Release is authorized to progress.

Keeping Release establishment distinct from subsequent determinations preserves the boundary between the existence of a governed Release and decisions about what may enter or happen to it.

### 10. Determine Release Admission

Once the Release has been established, the concluded Engineering outcome can be considered for Release Admission.

Release Admission is a Collaboration-owned determination about whether the Engineering outcome is admitted to the established Release under the applicable context and governance.

In this solo-developer realization, the same human participant performs the determination in the applicable Collaboration capacity. The concentration of participation does not transfer Release Admission ownership to the Engineering System or Release System.

The determination may be informed by the Engineering Conclusion, relevant evidence, Capability Acceptance where applicable, and the context of the established Release.

Capability Acceptance is available in this example and can inform the determination. Its presence here does not establish Capability Acceptance as a universal prerequisite for Release Admission.

If applicable information were missing, conflicting, or insufficient, Release Admission would remain unresolved rather than being inferred from the existence of an Engineering Conclusion or an established Release.

For this realization, the applicable information supports admitting the concluded account-deletion outcome to the established Release.

### 11. Progress the Release

With the applicable Engineering outcome admitted, the Release can continue through the Release governance relevant to this realization.

The solo developer performs the applicable Release activity and determines whether the Release can progress according to the governing Release semantics and available evidence.

Release progression is not established merely because:

- the implementation exists;
- automated checks pass;
- Engineering Conclusion has been established;
- Capability Acceptance has been established; or
- Release Admission has been determined.

Those outcomes can contribute to the applicable Release context, but they do not collapse the distinct Release governance that determines progression.

In this example, the applicable Release conditions are satisfied and the Release progresses with the account-deletion capability included.

The customer-facing capability has now travelled from Product intent through Engineering realization and governed Engineering outcome into an established and governed Release.

## Evidence and outcomes

The Engineering journey produced evidence and governed outcomes at different points for different purposes.

Evidence supported evaluation and determination. It did not become a governed determination merely because it existed or because it was produced by a particular participant.

### Evidence that supported the Engineering outcome

Evidence relevant to the Engineering outcome included, where applicable:

- the implemented account-deletion changes;
- Engineering decisions made during realization;
- automated test and validation results;
- observed account-deletion behavior;
- the failed integration test that exposed remaining account-associated state;
- the investigation and correction of that deficiency; and
- subsequent validation after the correction.

Some evidence originated through human activity, some through Claude-assisted Engineering activity, and some through automation.

Its origin did not independently determine its sufficiency.

The failed integration test was particularly significant because it changed the Engineering understanding of the realized state. Preserving that failure, the resulting investigation, and the subsequent correction provided stronger continuity than retaining only the final successful validation result.

The applicable evidence informed the Engineering evaluation that supported Engineering Conclusion.

### Governed outcomes

The journey established several distinct governed outcomes:

| Governed outcome | What it established in this example |
| --- | --- |
| Product intent | The customer capability that Engineering was intended to realize |
| Engineering Conclusion | The governed Engineering outcome for the applicable Engineering scope |
| Capability Acceptance | That the realized capability satisfied the applicable Product intent |
| Release establishment | The governed Release into which the Engineering outcome could be considered for admission |
| Release Admission determination | That the concluded Engineering outcome was admitted to the established Release |
| Release progression | That the Release could progress under the applicable Release governance |

These outcomes are related, but they are not interchangeable.

For example, Engineering Conclusion did not establish Capability Acceptance, Capability Acceptance did not establish Release Admission, and Release Admission did not by itself establish Release progression.

The same human participant performed several of these determinations in this solo-developer realization. Their semantic distinction remained intact despite that concentration of responsibility and authority.

### Continuity from intent to release

The example preserves a connected path from the original Product intent to the resulting Release:

```text
Product intent
    ↓
applicable Engineering context and scope
    ↓
Engineering approach and realization
    ↓
validation and evidence
    ↓
Engineering Conclusion
    ↓
Capability Acceptance
    ↓
Release establishment
    ↓
Release Admission determination
    ↓
Release progression
```

This representation describes the path taken by this example. It does not establish a universal mandatory sequence for every Engineering situation.

Continuity means that the resulting governed outcomes can be understood in relation to the intent, context, Engineering activity, decisions, and evidence that preceded them.

It does not require every piece of information produced during Engineering to be retained or placed into a single artifact.

In a solo-developer context, much of the working knowledge may initially exist with one person. The Engineering Operating Model still benefits from preserving sufficient evidence and provenance for the outcome to remain understandable beyond the participant's immediate memory.

AI-assisted activity makes that continuity especially relevant. Claude may contribute analysis, implementation, investigation, and validation, but those contributions should remain connected sufficiently to the Engineering context and resulting governed outcomes to understand how they influenced the realization.

## What changed — and what did not

The solo-developer context affected how the Engineering Operating Model was realized. It did not create a different version of the model.

### What changed in this context

One human participant carried several capacities that could be distributed across multiple people in another context.

This reduced coordination overhead. Product intent, Engineering decisions, capability evaluation, and Release activity did not require handoffs between different human participants merely to move the work forward.

Some context could also remain comparatively lightweight because the same person maintained continuity across much of the Engineering journey. For example, an Engineering decision did not necessarily require a formal handoff artifact simply to communicate that decision to another engineer.

The realization could therefore use relatively lightweight representations for planning, decisions, evidence, and coordination where those representations remained sufficient for the applicable Engineering concerns.

AI and automation increased the number and type of participants without requiring additional human organizational structure. Claude could contribute substantial Engineering activity, while CI automation could repeatedly execute validation and produce evidence.

The resulting participation topology was comparatively simple:

```text
                     Solo developer
                    /      |       \
                   /       |        \
          Product capacity |   Release capacity
                           |
                    Engineering capacity
                           |
                    capability-evaluation
                         capacity
                           |
              +------------+------------+
              |                         |
         Claude Code                CI automation
       AI participation          automated execution
```

The diagram represents the concentrated participation used in this example. It does not imply that authority flows from the solo developer to Claude or CI automation, or that these capacities must be arranged this way in another realization.

### What remained invariant

Concentrating participation did not collapse the semantic distinctions that governed the work.

In particular:

- Product intent remained distinct from Engineering realization;
- responsibility, technical capability, access, and authority remained distinct concepts;
- AI and automation participation did not independently create Engineering authority;
- applicable context still had to be resolved rather than assumed or manufactured;
- validation results and other evidence informed governed determinations but did not become those determinations;
- Engineering Conclusion remained distinct from Capability Acceptance;
- Release establishment preceded the Release Admission determination in this realization;
- Release Admission remained a Collaboration-owned determination rather than becoming Engineering-owned or Release-owned;
- Capability Acceptance was not made a universal prerequisite for Release Admission;
- Release Admission remained distinct from Release progression; and
- sufficient continuity and provenance still had to connect intent, Engineering activity, evidence, and governed outcomes.

The central distinction can therefore be summarized as:

```text
context changes
    ↓
participants, distribution, coordination,
representation, tooling and ceremony

context does not silently change
    ↓
semantic ownership, applicable authority,
governed determinations, evidence semantics,
continuity, provenance or conformance obligations
```

A solo developer can therefore realize the Engineering Operating Model with substantially less coordination machinery than a more distributed organization while preserving the Engineering semantics applicable to the work.

## What this example does not imply

This example illustrates one possible realization of the Engineering Operating Model. It should not be interpreted as prescribing the particular participants, authority arrangement, tooling, artifacts, execution mechanisms, evidence, or sequence shown here.

In particular, this example does not imply that:

- a solo developer automatically holds every authority relevant to Engineering activity;
- one person must perform the Product, Engineering, capability-evaluation, Collaboration, and Release capacities shown here;
- organizational size determines the required depth of Engineering rigor, evidence, governance, or documentation;
- Claude, Claude Code, CI automation, or any particular tooling is required by the Engineering Operating Model;
- AI participation requires a separate set of Engineering semantics or gains authority from technical capability, access, or autonomy;
- the particular artifacts, validation activities, evidence, or implementation concerns shown here form a universal required set;
- the eleven narrative stages define a mandatory Engineering process or required lifecycle sequence;
- Capability Acceptance is universally required before Release Admission;
- successful validation, Engineering Conclusion, Capability Acceptance, or Release Admission can substitute for another governed determination; or
- a more distributed organization is necessarily a more mature, rigorous, or conforming realization.

Different realizations may use different participants, authority distributions, representations, tooling, automation, workflows, and governance mechanisms where the applicable canonical Engineering semantics are preserved.

## Canonical references

This example applies Engineering semantics defined by the canonical Engineering Operating Model. The following references provide the primary authoritative sources for the concepts most materially exercised by the example.

| Concept exercised | Canonical source |
| --- | --- |
| Product intent and the boundary between Product intent and technical implementation | [Product Principles Specification](../../engineering_platform/product_system/governance/product_principles_specification.md) |
| Engineering lifecycle, Engineering Evidence, Engineering Conclusion, and the Engineering-to-Release boundary | [Engineering Lifecycle Specification](../../engineering_platform/engineering_system/governance/engineering_lifecycle_specification.md) |
| Capability Acceptance and evaluation of a realized capability against Product-owned intent | [Capability Acceptance Specification](../../engineering_platform/collaboration_system/product_engineering/capability_acceptance_specification.md) |
| Release establishment and preservation of governed Release state | [Release Record Specification](../../engineering_platform/release_system/progression/release_record_specification.md) |
| Release Admission and the Engineering–Release collaboration boundary | [Release Admission Specification](../../engineering_platform/collaboration_system/engineering_release/release_admission_specification.md) |
| Release progression and its governed decisions, evidence, execution, and outcomes | [Release Progression Specification](../../engineering_platform/release_system/progression/release_progression_specification.md) |
| Participant scope, capacity, responsibility, and authority | [Participation & Scope Specification](../../engineering_platform/specifications/participation_scope_specification.md) |
| Resolution and composition of applicable Engineering context | [Context Resolution & Composition Specification](../../engineering_platform/specifications/context_resolution_composition_specification.md) |
| Relationship between validation, evidence, governed determinations, and authority | [Governance & Validation Integration Specification](../../engineering_platform/specifications/governance_validation_integration_specification.md) |
| Preservation of Engineering continuity, provenance, history, and materially significant relationships | [Continuity & Provenance Specification](../../engineering_platform/specifications/continuity_provenance_specification.md) |
| Human, AI, and automation participation in execution without technical capability becoming authority | [Engineering Automation](../../engineering_platform/engineering_automation/README.md) |

These references are provided for semantic drill-down. Their inclusion does not imply that they are the only canonical Engineering semantics applicable to every realization, and their absence from another example would not establish an exemption from otherwise applicable canonical obligations.
