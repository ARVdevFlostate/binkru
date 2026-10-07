# Startup Team

**Example version:** 1.0.0

> **Non-normative example**
>
> This example illustrates one possible realization of the Engineering Operating Model in a startup-team context. It does not establish Engineering semantics or prescribe a required implementation, organizational structure, or division of responsibility. Where this example differs from the canonical Engineering Operating Model, the canonical model governs.

[Explore all Contextual Examples](./README.md)

## About this example

This example follows a customer account-deletion capability from Product intent through Engineering and Release in a small-to-medium startup team where Product and Engineering responsibilities are distributed across multiple human participants and AI and automation also participate in Engineering activity.

The scenario is intentionally the same capability used by the Solo Developer contextual example. The difference is not the Engineering Operating Model being applied, but the organizational and participant context in which it is realized.

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

In this realization, responsibility for the product and its Engineering is distributed across a startup team rather than concentrated in one person. Relevant context, decisions, evidence, and governed outcomes may therefore need to cross participant boundaries as the capability progresses from Product intent through Engineering and Release.

### Scenario assumptions

For this example:

- the product already exists and is operational;
- customers authenticate before using account-specific functionality;
- customer accounts have persisted associated state;
- permanent account deletion is a newly requested Product capability;
- the capability requires Engineering realization before it can become part of the product;
- Product and Engineering responsibilities are distributed across multiple human participants;
- relevant authority is established for the capacities exercised in this realization rather than inferred from organizational titles;
- Claude and Claude Code participate as illustrative AI-assisted Engineering tooling;
- CI/CD automation participates in applicable Engineering and Release activity; and
- AI and automation participation does not alter the applicable authority semantics.

## Participants and authority

This example distributes relevant Product, Engineering, capability-evaluation, Collaboration, and Release capacities across multiple human participants.

The distribution makes coordination and shared context more explicit than in the Solo Developer example. It does not create different Engineering semantics or allow organizational titles, responsibilities, or technical access to manufacture authority.

| Participant | Illustrative participation | Authority relevant to this example |
| --- | --- | --- |
| Product participant | Establishes the intended customer capability and participates in evaluation of the realized capability against Product intent | Carries the applicable Product and capability-evaluation authority established for this realization |
| Engineering participant A | Investigates the existing product, contributes to the Engineering approach, realizes affected application behavior, and contributes Engineering evidence | Participates within the applicable Engineering scope and carries the Engineering authority established for their applicable activity |
| Engineering participant B | Contributes to Engineering planning and realization, investigates affected persisted state and dependent behavior, and contributes Engineering evidence | Participates within the applicable Engineering scope and carries the Engineering authority established for their applicable activity |
| Startup lead | Participates in applicable Engineering evaluation, performs applicable Collaboration determinations, and performs applicable Release activity | Carries the applicable Engineering, Collaboration, and Release authority established for those capacities in this realization |
| Claude / Claude Code | Assists with codebase analysis, Engineering planning, implementation, validation, and investigation of failures | Participates in Engineering activity but does not gain Engineering authority merely from its technical capability, access, or contribution |
| CI/CD automation | Executes applicable automated validation and Release-related automation and preserves resulting evidence | Produces execution results and evidence but does not independently establish governed Engineering or Release determinations merely because execution succeeds |

This participant arrangement is illustrative. A startup could distribute the same capacities differently, combine several capacities in one person, or involve additional participants where its context warrants them.

### Distributed participation, explicit authority

Multiple people participating in the change makes responsibility and authority more visibly separate.

An Engineering participant may be responsible for implementing part of the account-deletion capability without therefore holding every authority relevant to the Engineering outcome.

Likewise, the startup lead's broader involvement does not create authority merely from organizational position. The authority exercised in this example is the authority established for the applicable capacity and scope.

The Product participant may also carry both Product and capability-evaluation capacities. Those capacities remain distinct: establishing the intended capability is not the same determination as evaluating whether the realized capability satisfies that intent.

Similarly, the startup lead may participate in Engineering, Collaboration, and Release capacities without those capacities becoming semantically interchangeable.

The distribution can be represented as:

```text
                         Product participant
                         ┌───────┴────────┐
                         ↓                ↓
                  Product capacity   capability-evaluation
                                           capacity

 Engineering participant A       Engineering participant B
              \                         /
               \                       /
                └── Engineering activity ──┐
                           ↑               │
                      Claude Code          │
                           ↑               │
                    AI participation       │
                                           ↓
                                      Startup lead
                                  Engineering capacity
                                           │
                              ┌────────────┴────────────┐
                              ↓                         ↓
                    Collaboration capacity       Release capacity

                           CI/CD automation
                    automated execution + evidence
```

The diagram shows the distribution used by this example. It does not define reporting relationships, authority delegation, or a required startup-team structure.

### Shared context across participants

Because Engineering activity is distributed, relevant context cannot be assumed to exist equally with every participant.

For example, the Product participant may understand why permanent account deletion is wanted without knowing the implementation dependencies discovered by Engineering. One Engineering participant may understand the customer-facing behavior while another discovers implications for persisted account-associated state.

The team therefore needs sufficient shared representation for applicable participants to understand the context required for their activity.

This does not mean every participant needs every available artifact or every detail known by another participant.

Context remains activity-specific:

```text
available Product + Engineering context
                 ↓
       resolve applicability
                 ↓
    compose relevant context
                 ↓
       applicable participant
                 ↓
       Engineering activity
```

The introduction of more participants therefore increases the importance of explicit context transfer without changing the underlying principle: **applicability, not accumulation**.

### AI-assisted Engineering

This example uses **Claude and Claude Code** as illustrative AI-assisted Engineering tooling.

A paid Claude subscription providing Claude Code access is required to reproduce the example as written. Claude is an implementation choice for this example, not a requirement of the Engineering Operating Model.

Claude may assist either Engineering participant with codebase analysis, planning, implementation, test creation, validation, failure investigation, and evidence assembly.

Its participation may therefore cross work performed by multiple human participants. That makes the context supplied to Claude especially important: access to the repository or previous AI interactions does not guarantee that the context applicable to a particular Engineering activity has been established.

Claude's technical capability, repository access, or ability to perform substantial Engineering work does not independently establish authority.

### Automation participation

CI/CD automation may build the changed product, execute tests and other automated checks, preserve validation results, and perform applicable automated Release activity.

Its results can provide evidence used by multiple participants and across different governed concerns.

Successful automated execution does not independently establish Engineering Conclusion, Capability Acceptance, Release Admission, or Release progression.

Likewise, failed automation remains meaningful evidence. Where it exposes a deficiency, conflict, or unresolved condition, that condition remains visible to the applicable participants rather than being bypassed merely to allow the workflow to continue.

## What applies in this example

The account-deletion capability crosses several governed concerns in the Engineering Operating Model. The following Systems and Engineering Capabilities are relevant to the realization shown in this example.

### Systems

| System | Relevance in this example |
| --- | --- |
| Product System | Owns the intended customer capability that the Engineering change is intended to realize |
| Collaboration System | Supports transitions and determinations across Product, Engineering, and Release concerns, including the applicable Capability Acceptance and Release Admission determinations |
| Engineering System | Governs the distributed Engineering work through realization, evidence, evaluation, and Engineering Conclusion |
| Release System | Governs the established Release and its progression |

All four Systems appear because this particular example follows the capability from Product intent through Engineering and Release. Their presence here does not imply that every Engineering situation must exercise every System.

The distribution of participants does not redistribute semantic ownership between the Systems. For example, involving several Engineering participants does not move Product intent into the Engineering System, and involvement by the startup lead in Release activity does not move Release Admission ownership out of the Collaboration System.

### Engineering Capabilities

| Engineering Capability | How it appears in this example |
| --- | --- |
| Discovery & Navigation | Different participants locate the Product, codebase, Engineering, validation, and Release information relevant to their activity |
| Participation & Scope | Applicable participants, capacities, authority, Engineering scope, and boundaries of participation are established across the distributed team |
| Context Resolution & Composition | Relevant context is resolved and composed for different participants and activities rather than assuming that everyone shares the same knowledge or accumulating all available information |
| Execution Enablement | Human participants, Claude, and automation are prepared to perform applicable Engineering activity using the context and constraints relevant to their respective activity |
| Governance & Validation Integration | Evidence and validation results produced across participants and automation remain connected to the governed evaluations and determinations they inform without execution success becoming authority |
| Continuity & Provenance | Product intent, Engineering decisions, contributions, evidence, and governed outcomes remain sufficiently connected as work and information cross participant boundaries |

These Capabilities describe Engineering abilities exercised by the example. They do not prescribe particular tools, artifacts, services, team structures, communication mechanisms, or implementation components.

The startup context makes some of these Capabilities more visible because applicable Engineering information and activity are distributed. That visibility does not make them more semantically important than they were in the Solo Developer example.

### Governed concerns

As the example progresses, several governed concerns become important:

- the Product-owned intended capability;
- transition of sufficient Product context for the capability to become actionable for Engineering;
- Engineering scope and participation across multiple participants;
- resolution and composition of applicable context for distributed Engineering activity;
- coordinated Engineering realization and supporting evidence;
- Engineering Conclusion;
- evaluation of the realized capability against Product intent;
- Release establishment;
- Release Admission; and
- Release progression.

The Engineering journey introduces these concerns when they become relevant rather than treating them as a mandatory sequence or universal checklist.

Distribution can make some concerns require more explicit representation or coordination. It does not make additional ceremony inherently necessary.

The relevant question remains whether the realization preserves sufficient semantics, authority, context, evidence, continuity, and provenance for the Engineering activity being performed.

## Engineering journey

The following journey shows one possible realization of this Engineering change. The stages provide a chronological narrative for the example; they do not define a mandatory sequential process. Engineering activity may return to an earlier concern when new evidence, uncertainty, or understanding requires it.

Because participation is distributed in this realization, the journey also shows how relevant context and decisions remain sufficiently connected as work moves between or involves multiple participants.

### 1. Establish the intended capability

The Product participant establishes the intended customer capability:

> **A signed-in customer must be able to permanently delete their account.**

At this point, the Product intent establishes what capability is wanted. It does not yet prescribe how account deletion will be implemented.

The Product participant therefore does not turn an assumed technical solution into part of the Product intent. Questions about interfaces, affected account state, implementation structure, validation, and failure behavior remain Engineering concerns to be resolved as the change becomes actionable.

Because the Product participant and Engineering participants are different people in this realization, the intended capability must remain sufficiently represented for Engineering to understand what it is being asked to realize without relying on unshared Product knowledge.

That does not require Product to specify the Engineering solution. It requires the Product-owned intent and applicable context to survive the participant boundary.

### 2. Prepare the change for Engineering

The intended capability is prepared for Engineering by establishing enough applicable Product and Engineering context for the team to begin responsible Engineering activity.

The Engineering participants examine the existing application and relevant Product context to understand:

- how a signed-in customer is identified;
- what persisted state is associated with an account;
- what other product behavior depends on the continued existence of that account;
- what "permanently delete" needs to mean for this product;
- what should be true after successful deletion;
- what could leave the deletion incomplete or unsuccessful; and
- what remains uncertain and requires further investigation.

Different participants may discover or hold different parts of this context.

For example, the Product participant may clarify intended customer behavior while one Engineering participant identifies authentication dependencies and another identifies account-associated persisted state that may be affected by deletion.

The relevant context therefore needs to become sufficiently shared or accessible for the Engineering activity that depends on it.

This can be represented as:

```text
Product intent
     │
     ├──── applicable Product context
     │
     ↓
Engineering preparation
     │
     ├──── existing product behavior
     ├──── Engineering discoveries
     ├──── dependencies
     └──── unresolved conditions
     │
     ↓
sufficient actionable Engineering context
```

The purpose is not to collect everything every participant knows. It is to resolve and preserve the context applicable to the Engineering change.

If required information cannot be established, the team keeps that uncertainty visible rather than filling the gap with an assumption merely to allow implementation to begin.

### 3. Determine the Engineering approach

With the relevant Engineering context established sufficiently to proceed, the Engineering participants determine how the capability can be realized.

Claude Code may assist during this activity by inspecting the existing codebase and other applicable Engineering information. It may help identify account-related components, authentication behavior, persisted account-associated state, dependent functionality, existing validation, and areas likely to be affected by deletion.

Different Engineering participants may use Claude while investigating different parts of the change. The resulting AI-assisted analysis does not become shared Engineering context merely because Claude produced it or because another participant can technically access the same repository.

Material discoveries must remain sufficiently connected to the Engineering work so that participants whose activity depends on them can understand and evaluate them.

The team can explore questions such as:

- where account deletion behavior should enter the existing product;
- which persisted state and dependent behavior are affected;
- what conditions must hold before deletion can proceed;
- how incomplete or failed deletion should be handled;
- how affected Engineering work relates across participants;
- what observable behavior would demonstrate successful realization; and
- what validation would provide useful evidence about the resulting Engineering outcome.

For example, an Engineering participant investigating persisted state may discover a dependency that changes the approach another participant intended to use for the customer-facing deletion flow.

That discovery becomes relevant Engineering context for both activities.

```text
Engineering participant A
        │
        │ discovery affecting shared scope
        ↓
relevant Engineering context
        ↓
Engineering participant B
        │
        ↓
affected Engineering approach
```

The purpose of making the discovery available is not to require every participant to receive every Engineering detail. It is to preserve the information needed where activities materially depend on one another.

Claude may help identify, analyze, or communicate such dependencies, but its participation does not independently establish the resulting Engineering decision.

The Engineering participants evaluate the applicable information within their established scope and authority.

The resulting approach remains implementation-specific to the actual product. The example does not require a particular API design, persistence strategy, application architecture, or deletion mechanism.

Where analysis exposes missing or conflicting information, the applicable part of the Engineering approach remains open until that condition is sufficiently resolved.

### 4. Plan the realization

Once there is sufficient understanding of the intended capability, affected Engineering scope, and proposed approach, the team plans the realization.

The work may be decomposed into manageable Engineering pieces where that helps coordinated execution and evaluation. For this capability, those pieces might concern:

- the customer interaction that initiates deletion;
- authenticated handling of the deletion request;
- treatment of account-associated persisted state;
- behavior of functionality that depends on the deleted account;
- failure and partial-completion behavior; and
- validation of the resulting capability.

These are illustrative planning concerns, not a required decomposition or universal set of Engineering Slices.

Where work is distributed, the plan also preserves enough relationship between the pieces for participants to understand dependencies, relevant decisions, and the Engineering scope within which they are participating.

For example:

```text
customer-facing deletion behavior
               │
               ├──── depends on ──── authentication behavior
               │
               └──── affects ─────── account-associated state
                                            │
                                            ↓
                                  dependent functionality
                                            │
                                            ↓
                                         validation
```

The diagram represents relationships that may matter to coordinated realization. It does not prescribe how the work must be divided between participants.

Claude may assist with planning by identifying dependencies, proposing implementation activities, highlighting affected areas, and suggesting validation. Human participants evaluate and adjust those proposals against the applicable Engineering context.

Planning also makes unresolved conditions visible across the activities they affect. Recording an assumption in a shared plan does not transform that assumption into established Engineering context.

The resulting plan provides sufficient coordination for distributed realization without requiring every participant to possess identical context or requiring every Engineering decision to become a formal artifact.

At this point, the work is sufficiently prepared for realization, while the implementation and plan remain free to evolve as Engineering activity produces new evidence and understanding.

### 5. Realize the capability

The Engineering participants begin realizing the planned change, with Claude Code participating in applicable Engineering activity.

Because the work is distributed, each participant needs the context applicable to the activity they are performing together with sufficient information about dependencies that can affect other parts of the realization.

For example, one Engineering participant may work primarily on the customer-facing and authenticated deletion behavior while another works on treatment of account-associated persisted state and dependent functionality.

This distribution does not make those activities independent merely because different participants perform them.

The context composed for an Engineering participant or Claude interaction may include:

- the intended capability;
- the participant's applicable Engineering scope;
- relevant Engineering decisions;
- affected code and interfaces;
- dependencies on work performed by other participants;
- applicable constraints and validation expectations; and
- unresolved conditions that must remain visible.

The objective remains to provide the context needed for the activity rather than accumulating every available Product and Engineering artifact for every participant.

Claude Code may assist either Engineering participant by:

- inspecting implementation areas relevant to their activity;
- proposing or modifying code;
- creating or updating automated tests;
- identifying dependencies or potential conflicts with other Engineering work;
- executing available development and validation tooling;
- analyzing failures and unexpected behavior; and
- proposing corrections or further investigation.

Material discoveries made during realization remain connected to the activities they affect.

For example, if the participant working on persisted state discovers that deletion must account for an additional dependency used by customer-facing functionality, that discovery becomes relevant context for the participant working on the deletion flow.

```text
Engineering activity A
        │
        │ material discovery
        ↓
applicable shared context
        ↓
Engineering activity B
        │
        ↓
realization adjusted
```

The mechanism used to preserve that connection may be lightweight. The example does not require a particular issue tracker, design document, messaging system, meeting, or other coordination mechanism.

What matters is that a materially relevant discovery does not disappear at the boundary between participants.

Claude may help identify or communicate the dependency, but its ability to do so does not independently establish the resulting Engineering decision.

Similarly, CI/CD automation may execute repeatedly as the implementation develops and produce evidence about individual activities and their integration.

Realization may change the team's Engineering understanding. When new evidence invalidates an assumption, exposes a dependency, or changes the applicable scope, the affected participants return to the relevant Engineering concern rather than continuing against a plan that no longer reflects the Engineering context.

### 6. Validate the Engineering outcome

As the distributed realization develops, the Engineering participants evaluate both their applicable work and the resulting integrated Engineering change using evidence appropriate to the Engineering scope.

Validation may include, where relevant:

- automated tests for successful account deletion;
- validation of authentication and authorization behavior around the deletion operation;
- tests or inspection of account-associated persisted state;
- checks of functionality that previously depended on the account;
- validation of expected failure behavior;
- integration validation across affected Engineering areas;
- static analysis, builds, or other applicable automated checks; and
- direct inspection or execution of the resulting customer behavior.

Evidence produced by one participant or activity may be relevant beyond the scope in which it originated.

For example, suppose the participant working on the customer-facing deletion flow completes the applicable implementation and its focused automated tests pass.

The participant working on account-associated state also completes the planned changes, and the applicable focused tests for that work pass.

When CI executes the broader integration validation, however, a test reveals that a dependent part of the application still attempts to use account-associated state after deletion.

The focused successful checks remain valid evidence about the behavior they evaluated.

They do not override the integration failure.

```text
Engineering activity A ──→ focused validation ──→ pass
                                                   \
                                                    \
                                                     → integrated validation
                                                    /
                                                   /
Engineering activity B ──→ focused validation ──→ pass
                                                     │
                                                     ↓
                                                   failure
                                                     │
                                                     ↓
                                      unresolved integrated condition
```

The failure is meaningful Engineering evidence because the Engineering outcome must be evaluated in relation to the applicable integrated scope, not merely as a collection of individually successful activities.

The failure also creates new applicable context.

The relevant participants investigate the condition. Claude Code may assist by tracing the dependency, identifying affected implementation, analyzing how the independently developed changes interact, and proposing a correction.

The investigation may determine that one participant's implementation needs revision, that several activities need coordinated changes, or that the team's earlier understanding of the dependency was incomplete.

The applicable participants update the realization and perform the relevant validation again.

This produces a distributed feedback loop:

```text
distributed realization
        ↓
local + integrated validation
        ↓
shared Engineering evidence
        ↓
deficiency, conflict or uncertainty?
        │
        ├── yes → resolve applicable context
        │          ↓
        │       coordinate affected activity
        │          ↓
        │       revise realization
        │          ↓
        │       validate again
        │
        └── no  → continue Engineering evaluation
```

Evidence accumulated through the work may therefore originate from different human participants, Claude-assisted activity, CI/CD automation, and the integrated product behavior.

Its origin does not independently determine its sufficiency or authority.

In particular:

**Individual work passes validation ≠ integrated Engineering outcome is sufficient**

**Claude reports completion ≠ Engineering Conclusion**

**CI reports success ≠ Engineering Conclusion**

The applicable evidence must remain sufficiently connected for the Engineering outcome to be evaluated across the scope being concluded.

### 7. Conclude the Engineering work

Once the applicable Engineering scope has been realized and evaluated, the Engineering outcome can be considered for conclusion.

In this distributed realization, no participant establishes Engineering Conclusion merely because the portion of work for which they were responsible is complete.

Likewise, combining several successful local results does not automatically establish a governed Engineering outcome.

The conclusion is informed by the applicable Engineering scope, the coordinated realization, and the relevant evidence accumulated across participants and validation activities:

```text
applicable Engineering scope
        +
coordinated Engineering realization
        +
relevant distributed evidence
        ↓
applicable Engineering evaluation
        ↓
Engineering Conclusion
```

The evidence used for this evaluation need not be physically consolidated into one artifact. It must be sufficiently available and connected for the applicable Engineering evaluation and resulting determination.

In this realization, the startup lead carries the applicable Engineering authority for concluding the integrated Engineering scope and establishes the Engineering Conclusion in an Engineering capacity.

The Engineering participants contribute realization, analysis, decisions, and evidence that materially inform that evaluation. Their contribution does not independently become the Engineering Conclusion.

Similarly, Claude and CI/CD automation may contribute substantial evidence and analysis without acquiring the authority to establish the conclusion.

If material evidence is missing, conflicting, or unresolved, the Engineering Conclusion is not inferred from participant confidence, completion of assigned work, or workflow state. The applicable condition remains visible and the work returns to the Engineering concern needed to resolve it.

When the applicable Engineering evaluation supports conclusion, the Engineering Conclusion establishes the governed Engineering outcome for the applicable scope.

The relationship remains:

```text
distributed contributions
        ↓
Engineering evidence
        ↓
applicable Engineering evaluation
        ↓
authorized determination
        ↓
Engineering Conclusion
```

Distribution therefore changes how evidence and context must reach the applicable evaluation. It does not change what evidence is, convert contribution into authority, or make Engineering Conclusion the automatic result of workflow completion.

The Engineering Conclusion also does not determine whether the realized capability satisfies the Product intent.

That remains a separate governed concern.

Likewise, Engineering Conclusion does not establish a Release, determine Release Admission, or authorize Release progression.

### 8. Evaluate the realized capability

With the Engineering work concluded, the realized capability can be evaluated against the Product intent:

> **A signed-in customer must be able to permanently delete their account.**

In this realization, the Product participant performs the evaluation in the applicable capability-evaluation capacity.

The evaluation considers whether the realized capability satisfies the Product-owned intent. Engineering evidence produced across the distributed realization may inform that evaluation, but the Engineering Conclusion does not automatically establish the result.

The Product participant therefore needs sufficient applicable information about the realized capability to perform the evaluation without needing to reproduce the Engineering evaluation that established Engineering Conclusion.

For example, the evaluation may consider whether a signed-in customer can initiate permanent account deletion and whether the resulting customer-visible behavior is consistent with the intended capability.

Relevant Engineering evidence may help demonstrate that behavior. The capability evaluation remains a distinct determination made against Product-owned intent.

If the realized capability does not satisfy the Product intent, that result remains visible. It does not become an Engineering deficiency merely because Capability Acceptance was not established. The reason for non-acceptance must be understood in its applicable context and may lead to further Product, Collaboration, or Engineering activity.

In this realization, the evaluation determines that the realized capability satisfies the applicable Product intent, establishing Capability Acceptance for that capability.

The Engineering Conclusion and Capability Acceptance were established through different capacities and by different participants in this realization.

That distribution makes their semantic distinction particularly visible, but the distinction does not depend on different people performing the determinations.

### 9. Establish the Release

The concluded Engineering outcome is next considered for inclusion in a Release.

In this example, the startup lead performs the applicable Release activity and establishes the Release for which the account-deletion outcome will be considered.

Release establishment identifies the Release that is to be governed. It does not by itself determine that the Engineering outcome is admitted to that Release or that the Release is authorized to progress.

Relevant Release context must remain sufficiently available for the subsequent governed activity. That context may include information originating from Engineering, Collaboration, and Release concerns without transferring semantic ownership between those Systems.

Keeping Release establishment distinct from subsequent determinations preserves the boundary between the existence of a governed Release and decisions about what may enter or happen to it.

### 10. Determine Release Admission

Once the Release has been established, the concluded Engineering outcome can be considered for Release Admission.

Release Admission is a Collaboration-owned determination about whether the Engineering outcome is admitted to the established Release under the applicable context and governance.

In this realization, the startup lead performs the determination in the applicable Collaboration capacity.

The fact that the startup lead also participated in Engineering evaluation and performs Release activity does not collapse those capacities or transfer Release Admission ownership to the Engineering System or Release System.

The determination may be informed by:

- the Engineering Conclusion;
- relevant Engineering evidence;
- Capability Acceptance where applicable;
- unresolved or materially significant conditions relevant to admission; and
- the context of the established Release.

These inputs may originate through different participants and activities. Their distribution does not require every underlying artifact to be reproduced for the admission determination, but sufficient applicable context must reach the determination for it to be made responsibly.

Capability Acceptance is available in this example and can inform Release Admission. Its presence here does not establish Capability Acceptance as a universal prerequisite for Release Admission.

Likewise, the existence of an Engineering Conclusion does not automatically produce a positive Release Admission determination.

If applicable information is missing, conflicting, or insufficient, Release Admission remains unresolved rather than being inferred from workflow progress, participant expectation, or the existence of the established Release.

For this realization, the applicable information supports admitting the concluded account-deletion outcome to the established Release.

### 11. Progress the Release

With the applicable Engineering outcome admitted, the Release can continue through the Release governance relevant to this realization.

The startup lead performs the applicable Release activity and determines whether the Release can progress according to the governing Release semantics and available evidence.

CI/CD automation may participate substantially in the resulting Release activity. It may prepare or execute applicable automated Release mechanisms, preserve execution results, and expose failures or other conditions relevant to Release governance.

Its ability to execute those mechanisms does not independently authorize Release progression.

Release progression is not established merely because:

- the implementation exists;
- individual or integrated automated checks pass;
- Engineering Conclusion has been established;
- Capability Acceptance has been established;
- Release Admission has been determined; or
- CI/CD automation is technically able to perform the Release activity.

Those outcomes and capabilities can contribute to the applicable Release context, but they do not collapse the distinct Release governance that determines progression.

For example, if an applicable automated Release check fails after Release Admission, that failure remains meaningful evidence:

```text
Release Admission
        ↓
applicable Release activity
        ↓
CI/CD execution
        ↓
Release-relevant failure
        ↓
progression remains unresolved
        ↓
investigate / resolve applicable condition
```

Release Admission is not retroactively converted into a failed Engineering Conclusion merely because a later Release-relevant condition prevents progression.

Likewise, technical ability to retry or bypass the failing automation does not create authority to authorize progression.

In this example, the applicable Release conditions are ultimately satisfied and the Release progresses with the account-deletion capability included.

The customer-facing capability has now travelled from Product intent through distributed Engineering realization and governed Engineering outcome into an established and governed Release.

## Evidence and outcomes

The Engineering journey produced evidence and governed outcomes at different points for different purposes.

Because Engineering activity was distributed across multiple participants, relevant evidence originated in different activities and locations. That distribution did not change the semantics of the evidence or the governed determinations it informed.

Evidence supported evaluation and determination. It did not become a governed determination merely because it existed, was shared across the team, or was produced by a particular participant.

### Evidence that supported the Engineering outcome

Evidence relevant to the Engineering outcome included, where applicable:

- implementation changes produced across the distributed Engineering work;
- Engineering decisions and materially relevant dependencies identified during realization;
- focused validation results for individual Engineering activities;
- integrated validation results across affected Engineering areas;
- observed account-deletion behavior;
- the integration failure that exposed a dependency between otherwise successful Engineering activities;
- the investigation and correction of that condition; and
- subsequent validation after the coordinated correction.

Some evidence originated through individual human activity, some through shared Engineering activity, some through Claude-assisted Engineering, and some through CI/CD automation.

Its origin did not independently determine its sufficiency.

Its scope also mattered.

For example, successful focused validation provided evidence about the Engineering behavior it actually evaluated. It did not establish that the broader integrated Engineering outcome was sufficient.

The integration failure therefore remained meaningful even though the affected Engineering activities had individually produced successful validation results.

```text
focused evidence A ─────┐
                        │
focused evidence B ─────┼──→ applicable Engineering evaluation
                        │
integration evidence ───┤
                        │
failure + correction ───┤
                        │
subsequent evidence ────┘
```

The diagram does not imply that every evidence item has equal significance or that evidence must be physically consolidated before evaluation. It shows that evidence originating across the distributed realization can contribute to evaluation of the applicable Engineering scope.

Preserving the integration failure, the investigation it caused, the resulting Engineering decisions, and the subsequent correction provides continuity that would be lost if the team retained only the final successful validation result.

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

In this realization, different participants or capacities contributed to or established different outcomes. That distribution made some semantic boundaries more externally visible, but it did not create those boundaries.

The System ownership of these governed outcomes can be represented as:

```text
Product System
    └── Product intent

Engineering System
    └── Engineering Conclusion

Collaboration System
    ├── Capability Acceptance
    └── Release Admission determination

Release System
    ├── Release establishment
    └── Release progression
```

These governed outcomes are related through the Engineering journey, but they remain semantically distinct and retain their applicable System ownership. The representation shows ownership, not lifecycle order; it does not imply that every Engineering situation must establish every outcome shown.

Engineering Conclusion did not establish Capability Acceptance. Capability Acceptance did not establish Release Admission. Release Admission did not by itself establish Release progression.

The Release-relevant failure encountered after Release Admission also did not retroactively invalidate the Engineering Conclusion or transform Release Admission into a different determination. It became evidence relevant to the Release concern in which it occurred.

### Continuity from intent to release

The example preserves a connected path from the original Product intent to the resulting Release:

```text
Product intent
    ↓
applicable Product and Engineering context
    ↓
distributed Engineering scope and participation
    ↓
Engineering decisions and coordinated realization
    ↓
local + integrated validation
    ↓
Engineering evidence
    ↓
Engineering Conclusion
    ↓
Capability Acceptance
    ↓
Release establishment
    ↓
Release Admission determination
    ↓
Release activity and evidence
    ↓
Release progression
```

This representation describes the path taken by this example. It does not establish a universal mandatory sequence for every Engineering situation.

In the startup-team context, continuity cannot depend entirely on one participant retaining the history and meaning of the change in personal working memory.

Relevant intent, decisions, dependencies, evidence, unresolved conditions, and governed outcomes therefore need sufficient representation to survive the participant boundaries across which the work progresses.

That does not require every conversation, intermediate result, AI interaction, or implementation detail to become a permanent governed artifact.

The objective is sufficient continuity and provenance for materially significant relationships to remain understandable.

For example:

```text
Product intent
      ↓
Engineering participant A
      │
      ├── material discovery
      ↓
shared applicable context
      ↓
Engineering participant B
      │
      ├── realization + evidence
      ↓
Engineering evaluation
```

If the material discovery disappears when the work crosses the participant boundary, later evidence and decisions can become difficult to understand in relation to the context that produced them.

AI-assisted activity creates another provenance boundary. Claude may contribute analysis, implementation, dependency discovery, investigation, and validation across work performed by different participants.

Those contributions need not be preserved as complete AI transcripts. What matters is that materially significant AI-assisted contributions remain sufficiently connected to the Engineering context, decisions, realization, and evidence they influenced.

The same principle applies to CI/CD automation. Execution results that materially affect Engineering or Release evaluation should remain sufficiently connected to the activity and governed concern they inform.

## What changed — and what did not

The startup-team context affected how the Engineering Operating Model was realized. It did not create a different version of the model.

### What changed in this context

Product, Engineering, capability-evaluation, Collaboration, and Release capacities were distributed across multiple human participants rather than concentrated in one person.

That distribution increased the number of participant boundaries across which applicable context, decisions, evidence, and governed outcomes had to remain understandable.

Coordination therefore became more explicit.

The Product-owned intent needed to reach Engineering without being replaced by an assumed technical solution. Engineering discoveries made by one participant needed to become available where they materially affected another participant's activity. Evidence originating across focused and integrated validation needed to remain sufficiently connected for evaluation of the applicable Engineering scope.

Shared representation also became more important because no individual participant could be assumed to hold the complete working context of the change.

This did not require every participant to possess identical information or every Engineering interaction to produce a formal artifact. The realization used enough shared representation and coordination to preserve the context and relationships required by the applicable activity.

AI participation also crossed participant boundaries. Claude could assist different Engineering participants with analysis, implementation, dependency discovery, validation, and failure investigation. Relevant AI-assisted discoveries therefore needed to survive beyond the individual interaction where they originated when they materially affected other Engineering activity.

CI/CD automation similarly produced evidence relevant across different scopes and governed concerns, including focused Engineering validation, integrated validation, and applicable Release activity.

The principal contextual change can be summarized as:

```text
greater participant distribution
             ↓
more boundaries across which
Engineering meaning must survive
             ↓
more explicit context sharing,
coordination, evidence integration
and provenance where required
```

More explicit does not necessarily mean more formal.

A conversation, lightweight shared record, Engineering artifact, automated result, or other mechanism may be sufficient where it preserves the applicable Engineering meaning. The Engineering Operating Model does not require ceremony merely because several people participate.

### What remained invariant

Distribution did not change the Engineering semantics governing the work.

In particular:

- Product intent remained distinct from Engineering realization;
- responsibility, organizational position, technical capability, access, and authority remained distinct concepts;
- participant distribution did not independently establish or transfer authority;
- AI and automation participation did not independently create Engineering authority;
- applicable context still had to be resolved rather than assumed or accumulated indiscriminately;
- Engineering discoveries that materially affected other activity had to remain sufficiently connected to that activity;
- validation results and other evidence informed governed determinations but did not become those determinations;
- successful focused validation did not establish the sufficiency of a broader integrated Engineering outcome;
- Engineering Conclusion remained distinct from Capability Acceptance;
- Release establishment preceded the Release Admission determination in this realization;
- Release Admission remained a Collaboration-owned determination rather than becoming Engineering-owned or Release-owned;
- Capability Acceptance was not made a universal prerequisite for Release Admission;
- Release Admission remained distinct from Release progression;
- a Release-relevant failure did not automatically rewrite an earlier Engineering Conclusion or Release Admission determination; and
- sufficient continuity and provenance still had to connect intent, context, Engineering activity, evidence, and governed outcomes.

The central distinction can therefore be represented as:

```text
context changes
    ↓
participant distribution,
coordination topology,
shared representation,
tooling and ceremony

context does not silently change
    ↓
semantic ownership,
applicable authority,
governed determinations,
evidence semantics,
continuity, provenance
or conformance obligations
```

A startup team may therefore require more explicit coordination and shared representation than a solo developer because Engineering activity and knowledge cross more participant boundaries.

That increased explicitness is a consequence of the realization's context, not a higher tier of the Engineering Operating Model and not evidence that the startup realization is inherently more mature, rigorous, governed, or conforming.

## What this example does not imply

This example illustrates one possible realization of the Engineering Operating Model. It should not be interpreted as prescribing the particular participants, authority arrangement, team structure, tooling, artifacts, coordination mechanisms, execution mechanisms, evidence, or sequence shown here.

In particular, this example does not imply that:

- a startup requires the participant structure or division of responsibility shown here;
- organizational titles, seniority, responsibility, repository access, or technical capability independently establish authority;
- Engineering authority must be concentrated in a startup lead or any other particular participant;
- distributing work across more participants inherently requires more governance, documentation, approvals, or ceremony;
- every participant must receive or retain all available Product and Engineering context;
- shared context requires a particular issue tracker, documentation system, communication mechanism, meeting structure, or workflow;
- Claude, Claude Code, CI/CD automation, or any particular tooling is required by the Engineering Operating Model;
- AI participation requires separate Engineering semantics or gains authority from technical capability, access, autonomy, or use across multiple participants;
- the particular artifacts, validation activities, evidence, coordination mechanisms, or implementation concerns shown here form a universal required set;
- successful focused validation establishes the sufficiency of a broader integrated Engineering outcome;
- the eleven narrative stages define a mandatory Engineering process or required lifecycle sequence;
- Capability Acceptance is universally required before Release Admission;
- successful validation, Engineering Conclusion, Capability Acceptance, Release Admission, or successful automated execution can substitute for another governed determination; or
- a startup-team realization is inherently more mature, rigorous, governed, or conforming than a solo-developer realization.

Different realizations may distribute participants, responsibilities, authority, context, coordination, tooling, automation, evidence, and governance mechanisms differently where the applicable canonical Engineering semantics are preserved.

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
| Participant scope, capacity, responsibility, and authority across distributed Engineering activity | [Participation & Scope Specification](../../engineering_platform/specifications/participation_scope_specification.md) |
| Resolution and composition of applicable Engineering context across participants and activities | [Context Resolution & Composition Specification](../../engineering_platform/specifications/context_resolution_composition_specification.md) |
| Preparation of participants and automation for applicable Engineering execution | [Execution Enablement Specification](../../engineering_platform/specifications/execution_enablement_specification.md) |
| Relationship between distributed validation, evidence, governed determinations, and authority | [Governance & Validation Integration Specification](../../engineering_platform/specifications/governance_validation_integration_specification.md) |
| Preservation of Engineering continuity, provenance, history, and materially significant relationships across participant boundaries | [Continuity & Provenance Specification](../../engineering_platform/specifications/continuity_provenance_specification.md) |
| Human, AI, and automation participation in execution without technical capability becoming authority | [Engineering Automation](../../engineering_platform/engineering_automation/README.md) |

These references are provided for semantic drill-down. Their inclusion does not imply that they are the only canonical Engineering semantics applicable to every realization, and their absence from another example would not establish an exemption from otherwise applicable canonical obligations.
