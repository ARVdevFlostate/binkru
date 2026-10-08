# Enterprise IT Team

**Example version:** 1.0.0

> **Non-normative example**
>
> This example illustrates one possible realization of the Engineering Operating Model in an enterprise IT context. It does not establish Engineering semantics or prescribe a required implementation, organizational structure, department model, division of responsibility, or governance process. Where this example differs from the canonical Engineering Operating Model, the canonical model governs.

[Explore all Contextual Examples](./README.md)

## About this example

This example follows a customer account-deletion capability from Product intent through Engineering and Release in an enterprise IT environment where relevant responsibilities, authority, Engineering activity, specialist knowledge, and Release activity are distributed across organizational boundaries.

The scenario is intentionally the same capability used by the Solo Developer and Startup Team contextual examples. The difference is not the Engineering Operating Model being applied, but the organizational and participant context in which it is realized.

In this realization, a Product organization, an Engineering organization, and a Production Engineering organization participate in different parts of the journey. These organizational structures are illustrative. They provide a realistic setting for showing how Engineering meaning can cross organizational boundaries without making those organizations equivalent to the Product, Engineering, or Release Systems.

## Scenario

### Product intent

> **A signed-in customer must be able to permanently delete their account.**

### Why this capability matters

A customer account represents persistent state associated with a customer and their use of a product. Providing permanent account deletion gives the customer a way to end that continued account existence.

The change is meaningful from an Engineering perspective because deletion is destructive and may be difficult or impossible to reverse. Its realization can affect authentication, persisted account state, dependent data, customer-facing behavior, shared services, failure handling, and the evidence needed to determine whether the intended capability has been realized correctly.

In an enterprise environment, some affected behavior or knowledge may also exist outside the immediate organizational boundary of the team realizing the customer-facing change. This makes the scenario useful for demonstrating how applicable context, specialist knowledge, authority, evidence, continuity, and provenance can remain connected across organizational boundaries.

The scenario does not imply that every product must provide account deletion or that account deletion necessarily requires enterprise-specific governance, specialist participation, or organizational separation. The capability is the Product intent established for this example.

### Engineering context

An existing customer-facing application allows customers to create an account, sign in, and use functionality associated with that account.

The application does not currently provide a way for a signed-in customer to permanently delete their account.

The requested capability therefore requires an Engineering change to the existing product.

In this realization, the product is supported through several organizational structures:

- a **Product organization** carries applicable Product responsibilities and participates in evaluation of the realized capability;
- an **Engineering organization** performs the principal Engineering realization and evaluation;
- a **Production Engineering organization** performs applicable Release activity and operates relevant Release mechanisms; and
- specialist participants contribute applicable knowledge, activity, or evidence where the Engineering context requires it.

These organizational structures are characteristics of this realization. They are not prescribed by the Engineering Operating Model and are not organizational equivalents of the canonical Systems.

For example:

```text
illustrative organization                    canonical concern principally exercised

Product organization          ───────────→   Product concerns

Engineering organization      ───────────→   Engineering concerns

Production Engineering
organization                   ───────────→   Release concerns
```

The arrows indicate principal participation in this realization, not semantic identity or exclusive ownership. A participant within one organization may exercise more than one applicable capacity where the corresponding authority has been established.

Collaboration concerns can therefore be exercised across or within these organizational structures without requiring a separate Collaboration organization. Capability Acceptance and Release Admission remain Collaboration-owned determinations even where the participants performing them belong to the Product, Engineering, or Production Engineering organizations.

The Engineering organization also depends on a shared identity service relevant to customer identity. Knowledge and Engineering responsibility associated with that service are not assumed to reside entirely within the application Engineering participants working on the account-deletion capability.

This creates an organizational and contextual boundary that becomes important during the Engineering journey.

### Scenario assumptions

For this example:

- the product already exists and is operational;
- customers authenticate before using account-specific functionality;
- customer accounts have persisted associated state;
- permanent account deletion is a newly requested Product capability;
- the capability requires Engineering realization before it can become part of the product;
- Product, Engineering, specialist, Collaboration, and Release capacities are distributed across multiple participants and organizational structures;
- the customer-facing application depends on a shared identity service relevant to customer identity;
- relevant knowledge about that shared service is not assumed to be held by every Engineering participant;
- relevant authority is established for the capacities and scope exercised in this realization rather than inferred from organizational membership, job title, seniority, responsibility, or technical access;
- organizational structure does not determine canonical System ownership;
- Claude and Claude Code participate as illustrative AI-assisted Engineering tooling;
- enterprise automation participates in applicable Engineering and Release activity; and
- AI and automation participation does not alter the applicable authority semantics.

## Participants and authority

This realization distributes Engineering activity and applicable authority across several participants and organizational structures.

The organizational location of a participant helps explain how work is coordinated in this example. It does not independently establish what that participant is authorized to determine.

A participant may also exercise more than one capacity. Where that occurs, the capacities remain semantically distinct even when they are carried by the same person or organizational participant.

### Product participant

A participant within the Product organization carries the applicable Product authority for the account-deletion capability.

In this example, the Product participant:

- establishes the Product intent that a signed-in customer must be able to permanently delete their account;
- provides applicable Product context where required during Engineering;
- evaluates the realized capability against the applicable Product intent; and
- carries the applicable authority for the resulting Capability Acceptance determination.

The Product participant does not prescribe the Engineering solution merely by establishing the intended capability.

Its participation in Capability Acceptance is exercised in the applicable Collaboration capacity. The fact that the participant belongs to the Product organization does not transfer Capability Acceptance into Product System ownership.

### Application Engineering participant

An Application Engineering participant works within the Engineering organization and principally contributes to the customer-facing and application behavior required to realize account deletion.

This participant may:

- investigate the existing account-management behavior;
- identify relevant application dependencies;
- contribute to Engineering scope and planning;
- implement customer-facing and application changes;
- use Claude and Claude Code during applicable Engineering activity;
- perform focused validation; and
- contribute evidence relevant to evaluation of the Engineering outcome.

Application Engineering responsibility does not by itself establish authority to conclude the integrated Engineering outcome.

### Identity Engineering participant

An Identity Engineering participant carries relevant Engineering responsibility and knowledge for the shared identity service on which the customer-facing application depends.

The participant may be situated within another team or organizational boundary from the Application Engineering participant.

In this example, the Identity Engineering participant may:

- provide applicable context about the shared identity service;
- identify identity-related dependencies affected by permanent account deletion;
- contribute to determining the Engineering scope;
- realize changes within the shared identity service where required;
- perform applicable validation; and
- contribute evidence about the resulting identity behavior.

Expertise in the shared identity service does not automatically establish authority over the integrated Engineering outcome, Product intent, Capability Acceptance, Release Admission, or Release progression.

### Engineering authority holder

A participant within the Engineering organization carries the applicable Engineering authority for evaluating and concluding the integrated Engineering outcome represented by this example.

The authority is established for the applicable Engineering scope. It is not inferred from a management title, organizational seniority, ownership of a repository, ability to approve a change technically, or position within the enterprise.

The Engineering authority holder may:

- participate in determining applicable Engineering scope and context;
- evaluate Engineering decisions and materially relevant evidence across participating Engineering domains;
- identify when unresolved context, dependencies, validation failures, or conflicting evidence prevent Engineering Conclusion;
- determine whether the applicable Engineering obligations have been satisfied; and
- establish the Engineering Conclusion for the integrated outcome.

The Engineering authority holder may rely on contributions and evidence from Application Engineering, Identity Engineering, AI-assisted Engineering, automation, and other applicable participants.

Those contributions inform the determination. They do not independently become the Engineering Conclusion.

### Specialist participant

Where the Engineering context requires knowledge not held by the principal Engineering participants, an applicable specialist may participate.

For example, a specialist might contribute knowledge concerning platform behavior, operational constraints, security characteristics, data dependencies, or another concern materially relevant to the Engineering change.

Specialist participation is contextual rather than an enterprise requirement.

A specialist may contribute analysis, identify a previously unresolved concern, perform applicable activity, or provide evidence. Specialist expertise, organizational status, or the ability to block a technical mechanism does not by itself establish authority over Product intent, Engineering Conclusion, Capability Acceptance, Release Admission, or Release progression.

If specialist input reveals materially applicable context that was previously unresolved, that context remains visible and is routed to the participant carrying the applicable authority rather than being silently treated as either approval or rejection.

### Production Engineering participant

A participant within the Production Engineering organization carries applicable Release responsibility and, in this realization, exercises distinct Release and Collaboration capacities.

In the applicable Release capacity, the Production Engineering participant may:

- establish the Release for which the concluded Engineering outcome will be considered;
- prepare and operate applicable Release mechanisms;
- perform or coordinate Release activity;
- evaluate applicable Release evidence; and
- establish Release progression where the corresponding Release authority has been established.

In the applicable Collaboration capacity, the same participant carries the authority required to determine Release Admission for the Engineering outcome represented by this example.

These capacities remain distinct:

```text
Production Engineering participant
        │
        ├── Release capacity
        │       ├── Release establishment
        │       ├── Release activity
        │       └── Release progression
        │
        └── Collaboration capacity
                └── Release Admission determination
```

The participant's organizational location within Production Engineering does not make Release Admission Release-owned.

Likewise, technical ability to deploy, promote, roll back, bypass, or otherwise operate Release mechanisms does not independently establish authority to determine Release Admission or Release progression.

### Claude and Claude Code

Claude and Claude Code participate as illustrative AI-assisted Engineering tooling. Claude Code is not required by the Engineering Operating Model; other AI-assisted Engineering tools may participate under the same applicable Engineering semantics, authority, context, governance, and provenance requirements.

Within applicable Engineering scope and available context, Claude and Claude Code may assist participants by:

- analyzing relevant implementation and configuration;
- identifying possible dependencies;
- proposing Engineering approaches;
- generating or modifying code;
- generating or modifying tests;
- interpreting validation results;
- investigating failures;
- comparing evidence across Engineering activity; and
- helping assemble information used by human participants when making governed determinations.

Claude may assist participants working across more than one Engineering domain, but access to repositories, documentation, execution environments, conversation history, or a large context window does not mean that all enterprise context has become applicable or resolved.

```text
technical access
        ≠
applicable context

available information
        ≠
resolved Engineering context

AI capability
        ≠
Engineering authority
```

Claude and Claude Code do not acquire Product, Engineering, Collaboration, or Release authority merely because they can perform technically sophisticated activity or contribute materially useful evidence.

### Enterprise automation

Enterprise automation participates in applicable Engineering and Release activity.

Depending on the realization, automation may perform activities such as building software, running tests, validating integration behavior, preparing artifacts, checking environments, executing deployment mechanisms, observing execution results, or producing evidence.

Automation may therefore operate across organizational and System boundaries represented in this example.

Its technical reach does not cause authority to cross those boundaries with it.

Successful automated execution is evidence about the activity performed. It does not independently establish Engineering Conclusion, Capability Acceptance, Release Admission, or Release progression.

### Participant topology

The resulting participant topology can be represented as:

```text
Product organization
    │
    └── Product participant
            ├── Product capacity
            │       └── Product intent
            │
            └── Collaboration capacity
                    └── Capability Acceptance

Engineering organization
    │
    ├── Application Engineering participant
    │
    ├── Identity Engineering participant
    │
    ├── applicable specialist participation
    │
    └── Engineering authority holder
            └── Engineering capacity
                    └── Engineering Conclusion

Production Engineering organization
    │
    └── Production Engineering participant
            ├── Release capacity
            │       ├── Release establishment
            │       └── Release progression
            │
            └── Collaboration capacity
                    └── Release Admission

Across applicable Engineering and Release activity
    │
    ├── Claude / Claude Code
    └── enterprise automation
```

This topology describes the realization used by this example. It does not prescribe an enterprise organization chart or require these capacities to be distributed among participants in this way.

The important boundary is semantic rather than organizational:

> **Organizational structure may realize or reinforce semantic boundaries; it does not define them.**

Authority remains attached to the applicable governed capacity and scope even where several capacities are carried by one participant or participants collaborate across organizational boundaries.

## What applies in this example

The account-deletion capability exercises concerns across all four Systems and all six Engineering Capabilities represented by the Engineering Operating Model.

Their applicability follows from the Engineering situation represented by the example, not from the organization being an enterprise.

The organizational structures introduced earlier provide one way of realizing the applicable concerns. They do not change their canonical ownership.

### Systems

#### Product System

The Product System governs the Product intent represented by this example.

The relevant Product intent is:

> **A signed-in customer must be able to permanently delete their account.**

The Product organization provides the organizational setting in which the applicable Product participant operates, but the organizational structure does not define Product System semantics.

Engineering may resolve how the capability is realized without silently changing the Product-owned intent.

#### Collaboration System

The Collaboration System governs applicable cross-System determinations and transitions exercised in the example.

Two become particularly visible:

- Capability Acceptance evaluates whether the identified realized capability satisfies the applicable Product-owned intent; and
- Release Admission determines whether a concluded Engineering outcome is admitted to an established Release.

Neither determination requires a separate Collaboration organization.

In this realization, participants situated within the Product and Production Engineering organizations exercise the applicable Collaboration capacities. Their organizational location does not change Collaboration System ownership of those determinations.

#### Engineering System

The Engineering System governs the Engineering realization of the requested capability.

Applicable Engineering concerns include:

- determining the Engineering scope;
- resolving relevant dependencies and context;
- planning the realization;
- performing Engineering activity across affected domains;
- evaluating Engineering decisions and validation evidence;
- responding to materially relevant discoveries or failures; and
- establishing the Engineering Conclusion.

Because relevant Engineering knowledge is distributed across organizational and domain boundaries, the Engineering System concerns represented here cannot be reduced to the activity of the Application Engineering participant alone.

#### Release System

The Release System governs the established Release and its applicable progression.

In this realization, the Production Engineering organization performs much of the associated Release activity.

That organizational responsibility does not make every determination occurring near Release activity Release-owned. In particular, Release Admission remains Collaboration-owned even when performed by a participant situated within Production Engineering.

Release establishment, Release Admission, and Release progression therefore remain distinct governed concerns.

### Engineering Capabilities

All six Engineering Capabilities are exercised in the realization.

#### Discovery & Navigation

Participants need to discover applicable Engineering information across more than one immediate working boundary.

This includes discovering relevant application behavior, the shared identity-service dependency, applicable Engineering context, and the sources needed to understand or validate the change.

Discovery does not establish authority or determine applicability merely because information has been found.

#### Participation & Scope

The realization must establish who is participating, in what capacity, within what applicable scope, and with what authority.

This is particularly important where organizational membership, specialist expertise, repository ownership, technical access, or operational responsibility could otherwise be mistaken for authority.

The Engineering scope may also evolve when materially relevant dependencies become visible.

#### Context Resolution & Composition

Applicable context is assembled from the sources required for the Engineering activity being performed.

In this enterprise realization, no single participant is assumed to begin with all relevant application, identity-service, specialist, Engineering, or Release context.

Context is therefore resolved according to applicability rather than accumulated merely because the enterprise can make more information technically available.

```text
more organizational information
            ≠
more applicable context

cross-organizational access
            ≠
resolved context
```

This applies equally to human, AI, and automated participants.

#### Execution Enablement

Applicable participants and automation require executable Engineering conditions appropriate to the activity being performed.

These may include repository state, dependencies, tools, execution environments, validation mechanisms, configuration, or other execution prerequisites.

In an enterprise environment, those conditions may span more than one Engineering domain or organizational boundary.

Execution availability does not establish authority. The ability to build, modify, validate, deploy, or otherwise execute activity remains distinct from authority to establish governed outcomes.

#### Governance & Validation Integration

Validation evidence is integrated with the applicable governance required to evaluate the Engineering outcome.

Evidence may originate from Application Engineering, Identity Engineering, specialist activity, Claude-assisted Engineering, enterprise automation, or other applicable sources.

Its origin does not determine its sufficiency.

A successful result within one Engineering domain also does not necessarily establish sufficiency for the integrated Engineering outcome when materially applicable dependencies remain unresolved.

Likewise, failed or conflicting evidence remains meaningful rather than being discarded merely because other validation has succeeded.

#### Continuity & Provenance

Engineering meaning must remain sufficiently connected as activity crosses participant, domain, organizational, and lifecycle boundaries.

For this example, relevant continuity includes connections among:

```text
Product intent
      ↓
applicable scope and context
      ↓
Engineering decisions
      ↓
distributed realization
      ↓
validation and evidence
      ↓
Engineering Conclusion
      ↓
Capability Acceptance where applicable
      ↓
Release establishment
      ↓
Release Admission determination
      ↓
Release activity and progression
```

The representation used to preserve those connections may vary.

Continuity does not require every conversation, AI interaction, automated execution result, intermediate artifact, or organizational hand-off to be preserved in full. It requires materially significant Engineering meaning and provenance to remain sufficiently connected for the applicable activity and governed determinations.

### Engineering Automation

Engineering Automation supports applicable activity in the example without becoming an additional System or source of Engineering authority.

Claude and Claude Code provide illustrative AI-assisted Engineering capabilities. Enterprise automation provides applicable execution, validation, and Release mechanisms.

Where used, automation may help resolve participants, activities, context, prompts, or execution conditions. Those mechanisms operate within the applicable Engineering semantics rather than replacing them.

For example:

```text
Claude discovers a dependency
        ↓
dependency becomes relevant input
to Engineering context resolution
        ↓
applicable participant evaluates
its consequence

not

Claude discovers a dependency
        ↓
Claude establishes Engineering scope,
authority, or Engineering Conclusion
```

Similarly:

```text
enterprise automation can deploy
        ≠
Release Admission has been determined

enterprise automation reports success
        ≠
Release progression has been established
```

The mechanisms can make Engineering and Release activity executable and observable. They do not manufacture the authority required for governed determinations.

### Applicability is contextual

The concerns identified in this section are applicable because they are exercised by this particular Engineering situation.

Their presence should not be interpreted as a universal checklist for enterprise Engineering.

An enterprise change with different Engineering significance, dependencies, participant distribution, authority distribution, or Release context could require a different depth of realization while remaining governed by the same Engineering Operating Model.

Conversely, a Solo Developer or Startup Team change could require deeper evidence, context resolution, governance, or continuity than this enterprise example if its Engineering context warranted it.

> **Organizational scale does not determine Engineering significance.**

## Engineering journey

The journey below follows one possible realization of the account-deletion capability through the applicable Product, Collaboration, Engineering, and Release concerns.

The numbered stages provide a narrative structure for this example. They are not mandatory Engineering Operating Model process steps, workflow gates, or a required ordering for every Engineering change.

### 1. Establish the intended capability

The Product participant establishes the Product intent:

> **A signed-in customer must be able to permanently delete their account.**

The intent establishes the capability the product is expected to provide without prescribing its Engineering realization.

At this point, the Product participant does not need to determine which application components, data stores, identity mechanisms, services, deployment mechanisms, or organizational participants must change.

Those are Engineering concerns to be resolved through applicable Engineering activity.

The Product intent therefore crosses into Engineering without becoming an Engineering design:

```text
Product organization

    Product intent
         │
         │  what capability is intended
         ↓

Engineering organization

    determine how that capability
    can be realized
```

The organizational transition does not transfer ownership of the Product intent to Engineering.

If Engineering later discovers that the capability has consequences not initially understood by the Product participant, those consequences may require additional context or Product clarification. Engineering does not silently rewrite the Product intent to fit a preferred implementation.

### 2. Prepare the change for Engineering

The requested capability is prepared for Engineering so that applicable participants can understand what is being asked and begin resolving the Engineering context.

The initial Engineering context establishes that:

- the customer-facing application already supports authenticated customer accounts;
- account-associated state persists beyond an individual authenticated session;
- no permanent account-deletion capability currently exists;
- deletion is expected to affect customer-facing behavior and persisted account state; and
- the application uses a shared identity service relevant to customer identity.

The existence of the shared identity service is known at this point. Its complete significance to permanent account deletion is not yet assumed to be resolved.

This distinction is important:

```text
dependency is known
        ≠
dependency is fully understood

information is available
        ≠
applicability has been resolved
```

The Engineering organization therefore begins with sufficient context to investigate the change without pretending that all affected scope is already known.

Applicable participation is also established.

The Application Engineering participant is expected to investigate the customer-facing application and its directly associated behavior. The Identity Engineering participant can contribute context concerning the shared identity service. Additional specialist participation can be introduced if materially relevant concerns emerge.

Claude and Claude Code may assist with discovery and analysis within the context made available to them.

Their ability to inspect implementation, repository history, interfaces, tests, documentation, or other Engineering material does not establish that all relevant enterprise context has been discovered or resolved.

Preparation for Engineering therefore establishes a usable starting point rather than a claim of complete knowledge.

### 3. Determine the Engineering approach

The Engineering participants investigate how the intended capability interacts with the existing product and its dependencies.

Application Engineering examines the current account lifecycle, authenticated customer experience, account-associated state, relevant service interactions, and existing validation behavior.

Identity Engineering provides applicable context about how the customer-facing application interacts with the shared identity service.

Claude and Claude Code assist with activities such as tracing implementation paths, locating relevant interfaces, identifying possible dependencies, examining existing tests, and comparing candidate approaches.

The resulting analysis indicates that realizing the capability will require coordinated changes rather than only adding a customer-facing deletion control.

The initial Engineering approach includes:

- providing an authenticated customer action for requesting permanent account deletion;
- ensuring the deletion action operates against the intended customer account;
- removing or otherwise resolving applicable persisted account state;
- handling affected application behavior after deletion;
- addressing applicable interaction with the shared identity service; and
- validating the resulting behavior across the affected Engineering scope.

This is an Engineering approach, not a restatement of Product intent.

```text
Product intent
    │
    │ "what must the customer be able to do?"
    ↓
Engineering analysis
    │
    │ "what must change for that capability
    │  to be realized correctly here?"
    ↓
Engineering approach
```

At this stage, the Engineering participants have identified the shared identity service as part of the relevant Engineering landscape, but they have not assumed that every consequence of account deletion across that service has already been discovered.

The applicable Engineering authority holder evaluates the emerging approach within the integrated Engineering scope.

Input from Application Engineering, Identity Engineering, specialists, Claude, and automation can inform that evaluation. None of those inputs independently establishes the Engineering approach merely because its source has technical expertise or access.

Where uncertainty remains material, it remains visible as unresolved Engineering context rather than being converted into an unsupported assumption.

### 4. Plan the realization

The Engineering participants translate the approach into realizable Engineering activity.

The work is distributed according to the affected Engineering concerns rather than merely according to organizational boundaries.

Application Engineering plans the customer-facing and application changes within its applicable scope.

Identity Engineering plans applicable investigation and change associated with the shared identity service.

The Engineering participants also identify where coordinated validation will be needed so that successful work within one domain is not mistaken for sufficiency of the integrated outcome.

A simplified realization view is:

```text
                         account-deletion capability
                                   │
                    ┌──────────────┴──────────────┐
                    ↓                             ↓
          Application Engineering         Identity Engineering
                    │                             │
          customer-facing flow             shared identity
          application behavior             service behavior
          account-state handling           applicable dependency
                    │                             │
                    └──────────────┬──────────────┘
                                   ↓
                         integrated validation
                                   ↓
                         Engineering evidence
```

The diagram represents the Engineering concerns currently identified. It does not establish that the scope is permanently closed.

Planning preserves the possibility that realization or validation may expose additional applicable context.

Claude and Claude Code may assist in decomposing the work, examining dependencies, proposing implementation sequences, generating candidate changes, or identifying validation needs.

Enterprise automation may provide executable conditions for builds, tests, integration validation, or other planned Engineering activity.

Neither AI-generated planning nor automated execution establishes that the plan is complete.

The Engineering authority holder does not establish Engineering Conclusion at this point merely because a plan exists or because the identified work appears sufficient.

The plan provides a coordinated basis for realization while preserving unresolved context and the possibility of feedback:

```text
current context
      ↓
Engineering approach
      ↓
planned activity
      ↓
realization / validation
      │
      └───────────────┐
                      │ materially relevant
                      │ new information
                      ↓
               context resolution
                      ↓
               scope / approach /
               plan adjusted where required
```

This feedback path is particularly important in a distributed environment. An Engineering plan that crosses organizational or domain boundaries must remain able to absorb materially relevant discoveries without treating the original plan as authoritative Engineering truth.

Planning therefore coordinates the realization; it does not freeze the Engineering context.

### 5. Realize the capability

The Engineering participants begin realizing the planned changes within their applicable scopes.

Application Engineering implements the customer-facing deletion flow and the associated application behavior. The work includes ensuring that the action applies to the authenticated customer, handling relevant account-associated state, and updating application behavior so that a deleted account is no longer treated as an active customer account.

Identity Engineering works with the applicable shared identity-service behavior identified during planning.

Claude and Claude Code assist within the context available to the participating engineers. Depending on the activity, this includes generating or modifying implementation, tracing service interactions, proposing tests, investigating existing behavior, and reviewing changes.

Enterprise automation builds the affected components and performs applicable focused validation.

Initial results are encouraging.

Application-focused validation shows that:

- an authenticated customer can initiate account deletion;
- the intended application account is removed;
- applicable directly associated application state is handled as intended; and
- subsequent application behavior no longer treats the deleted account as active.

Identity-focused activity also confirms that the expected account-deletion interaction reaches the shared identity service.

These results provide useful Engineering evidence, but they remain scoped evidence.

```text
Application Engineering
        │
        └── focused validation passes
                    │
                    ├──────────────┐
                    │              │
Identity Engineering               │
        │                          │
        └── expected service       │
            interaction occurs     │
                    │              │
                    └──────┬───────┘
                           ↓
                 useful Engineering evidence

                           ≠

                 Engineering Conclusion
```

During further investigation of the shared identity-service behavior, Identity Engineering identifies a materially relevant condition that was not fully resolved by the initial context.

The deletion interaction removes the application-facing account relationship as expected, but an account-linked identity mapping remains within the shared service.

That mapping can still associate the deleted customer identity with behavior relevant to the product's account lifecycle.

The existence of the shared identity service was already known. What has changed is the Engineering understanding of how its internal behavior affects the intended permanent-deletion capability.

```text
known dependency
      │
      ↓
shared identity service
      │
      │ deeper realization / investigation
      ↓
previously unresolved behavior
      │
      ↓
account-linked identity mapping remains
      │
      ↓
material consequence for the
account-deletion capability
```

The discovery does not mean the earlier Engineering activity was meaningless or that its evidence becomes invalid.

The focused application evidence still describes what occurred within its applicable scope.

What changes is the understanding of the integrated Engineering scope and whether the currently realized outcome is sufficient.

The new information is therefore routed into Engineering context resolution rather than treated as a specialist veto, an automatic failure of all previous work, or an implicit change to Product intent.

Identity Engineering contributes the relevant service context and evidence. If additional specialist knowledge is required to understand the mapping or its dependencies, an applicable specialist participant contributes that knowledge.

Claude and Claude Code may assist with tracing the newly identified behavior and evaluating possible changes, but AI discovery does not itself determine the consequence for Engineering scope.

The applicable Engineering authority holder evaluates the new information and determines that the unresolved identity mapping is materially relevant to the integrated account-deletion outcome.

The Engineering context and scope are updated accordingly.

```text
new evidence
     ↓
applicable context resolution
     ↓
Engineering significance evaluated
     ↓
scope adjusted where required
     ↓
approach / plan updated
     ↓
additional realization
```

Engineering therefore continues rather than proceeding toward Conclusion on the basis of evidence that is locally successful but incomplete for the now-resolved scope.

Identity Engineering realizes the additional change required to address the applicable identity mapping.

Application Engineering evaluates whether the newly resolved behavior requires corresponding application changes.

The participants update coordinated validation where necessary so that the resulting behavior can be evaluated as an integrated Engineering outcome.

This feedback loop demonstrates a consequence of organizational distribution without making organizational distribution itself a failure:

> **Work can be correct within one Engineering boundary while the integrated Engineering outcome remains incomplete because materially applicable context crosses that boundary.**

The same condition could occur in a smaller organization. The enterprise context merely makes the boundary across which the Engineering meaning must survive more visible.

### 6. Validate the Engineering outcome

After the additional Engineering activity, the participants validate the resulting account-deletion behavior across the applicable Engineering scope.

Application Engineering repeats the relevant application-focused validation.

Identity Engineering validates the updated shared identity-service behavior.

Applicable integrated validation exercises the account-deletion capability across the affected interaction between the customer-facing application and the shared identity service.

Enterprise automation performs the applicable executable validation and preserves results used as Engineering evidence.

Claude and Claude Code may assist participants in interpreting results, investigating discrepancies, identifying missing coverage, or comparing observed behavior with the intended Engineering outcome.

The resulting evidence now shows that:

- the authenticated customer can initiate deletion of the intended account;
- the applicable customer-facing and application behavior completes as expected;
- applicable persisted application state is handled as intended;
- the shared identity-service interaction completes as expected;
- the materially relevant account-linked identity mapping identified during realization is resolved; and
- applicable integrated validation no longer exposes the previously unresolved behavior.

The evidence originates from several participants and mechanisms:

```text
Application Engineering evidence ──────┐
                                       │
Identity Engineering evidence ─────────┤
                                       │
specialist evidence, where applicable ─┤
                                       ├──→ integrated Engineering
enterprise automation results ─────────┤    evidence
                                       │
Claude-assisted analysis ──────────────┘
```

The sources differ, but source type does not determine evidentiary sufficiency.

A human observation is not automatically authoritative because it came from a human. An automated result is not automatically sufficient because it is repeatable. Claude-assisted analysis is not automatically insufficient because AI participated in producing it.

Each contribution is evaluated for what it establishes within the applicable Engineering context.

The previously unsuccessful state also remains meaningful.

```text
before scope adjustment
    application-focused evidence       ✓
    expected identity interaction      ✓
    unresolved identity mapping        ✗

after additional realization
    application-focused evidence       ✓
    identity-service behavior          ✓
    integrated behavior                ✓
```

The earlier evidence is not rewritten to make the Engineering journey appear linear. Its relationship to the subsequent scope adjustment and realization remains part of the continuity of the Engineering outcome.

This matters because:

```text
failed or incomplete evidence
        ≠
evidence to erase

successful local validation
        ≠
integrated sufficiency

successful integrated validation
        ≠
Engineering Conclusion
```

The final distinction is essential.

Validation establishes evidence about the realized Engineering outcome. It does not itself perform the governed determination that the applicable Engineering obligations have been satisfied.

Enterprise automation can report that every applicable automated check passed.

Claude can report that the implementation and evidence appear complete.

Application Engineering, Identity Engineering, and applicable specialists can each report successful results within their scopes.

None of those statements independently establishes Engineering Conclusion.

The evidence is instead made available to the participant carrying the applicable Engineering authority for evaluation in the next stage.

### 7. Conclude the Engineering work

The Engineering authority holder evaluates the integrated Engineering outcome using the applicable context, decisions, realization, validation results, and other materially relevant evidence.

The evaluation includes evidence contributed across the Engineering scope, including:

- the realized customer-facing and application behavior;
- the resulting shared identity-service behavior;
- the resolution of the account-linked identity mapping discovered during realization;
- applicable focused and integrated validation;
- materially relevant specialist input, where applicable;
- enterprise automation results; and
- relevant Claude-assisted analysis used during Engineering activity.

The earlier discovery of the unresolved identity mapping remains part of the Engineering history.

The Engineering authority holder can therefore evaluate not only the final successful validation but also how the Engineering context changed, why the scope was adjusted, what additional realization occurred, and what evidence supports the resulting outcome.

```text
initial Engineering context
          ↓
initial scope and approach
          ↓
distributed realization
          ↓
materially relevant discovery
          ↓
context and scope adjustment
          ↓
additional realization
          ↓
integrated validation
          ↓
Engineering evidence
          ↓
Engineering Conclusion
```

The Engineering authority holder determines that the applicable Engineering obligations for the integrated account-deletion outcome have been satisfied and establishes the Engineering Conclusion.

That determination is distinct from the evidence supporting it.

```text
tests pass
        ≠
Engineering Conclusion

enterprise automation succeeds
        ≠
Engineering Conclusion

Claude reports completion
        ≠
Engineering Conclusion

participating engineers report
their work complete
        ≠
Engineering Conclusion
```

Those results may materially support the determination, but they do not replace it.

Likewise, the Engineering authority holder's organizational position does not create the authority to conclude the work. The authority used here is the applicable Engineering authority established for the integrated scope.

The Engineering Conclusion establishes the governed Engineering outcome for that scope.

It does not establish Capability Acceptance, create or establish a Release, determine Release Admission, or establish Release progression.

Those remain distinct concerns governed by their applicable semantics.

### 8. Evaluate the realized capability

With the Engineering outcome concluded, the realized capability can be evaluated against the applicable Product-owned intent.

The Product participant performs that evaluation in the applicable Collaboration capacity.

The Product intent remains:

> **A signed-in customer must be able to permanently delete their account.**

The Product participant evaluates the identified realized capability against that intent using the applicable Engineering outcome and supporting information.

The evaluation is concerned with whether the realized capability satisfies the applicable Product intent. It does not repeat the Engineering Conclusion or require the Product participant to independently reproduce the Engineering evaluation.

```text
Engineering Conclusion
        │
        │ identifies a concluded
        │ Engineering outcome
        ↓
realized capability
        │
        │ evaluated against
        ↓
Product-owned intent
        │
        ↓
Capability Acceptance
```

In this realization, the Product participant determines that the identified realized capability satisfies the applicable Product intent and establishes Capability Acceptance for that capability and scope.

The fact that the Product participant belongs to the Product organization does not make Capability Acceptance Product-owned.

The participant is exercising a Collaboration capacity when making the determination.

```text
Product participant
        │
        ├── Product capacity
        │       └── Product intent
        │
        └── Collaboration capacity
                └── Capability Acceptance
```

This organizational arrangement makes the distinction between Product intent and Capability Acceptance visible, but it does not create that distinction.

Similarly, the organizational separation between the Product participant and the Engineering authority holder makes the distinction between Engineering Conclusion and Capability Acceptance easy to observe, but the determinations would remain semantically distinct even if one person carried both applicable capacities.

```text
Engineering Conclusion
        ≠
Capability Acceptance

Engineering sufficiency
        ≠
Product capability satisfaction
```

Capability Acceptance also does not establish the Release, determine Release Admission, or establish Release progression.

In this example, Capability Acceptance is available as an input to subsequent activity where applicable.

Its occurrence here should not be interpreted as establishing Capability Acceptance as a universal prerequisite for Release establishment or Release Admission.

The next part of the journey moves into the Release context, where the Production Engineering participant exercises distinct Release and Collaboration capacities.

### 9. Establish the Release

The Production Engineering participant establishes the Release for which the concluded account-deletion Engineering outcome will be considered.

This occurs in the participant's applicable Release capacity.

The Release provides the governed Release context within which applicable Engineering outcomes can subsequently be considered for admission and Release activity can progress.

At this point:

- the Engineering outcome has been concluded;
- Capability Acceptance has been established for the identified realized capability in this example;
- the Release has been established; and
- Release Admission for the Engineering outcome has not yet been determined.

The distinction between Release establishment and Release Admission is important.

```text
Engineering Conclusion
        ↓
concluded Engineering outcome

Release establishment
        ↓
established Release

        ≠

Engineering outcome
admitted to Release
```

Establishing the Release does not itself admit the account-deletion outcome to that Release.

The Production Engineering participant may already have the technical ability to prepare artifacts, configure deployment activity, operate environments, or execute other Release mechanisms.

That technical readiness also does not establish Release Admission.

The Release is established first so that the subsequent Release Admission determination has an established Release against which the concluded Engineering outcome can be considered.

The fact that the Production Engineering participant establishes the Release does not give the Release System ownership of the subsequent Release Admission determination.

### 10. Determine Release Admission

The concluded account-deletion Engineering outcome is considered for admission to the established Release.

The Production Engineering participant now exercises the applicable Collaboration capacity rather than the Release capacity used to establish the Release.

The participant evaluates the concluded Engineering outcome against the applicable Release Admission context.

Relevant inputs may include:

- the Engineering Conclusion;
- the identity of the concluded Engineering outcome being considered;
- the established Release;
- applicable Release context;
- Capability Acceptance where relevant to this determination; and
- other applicable evidence or governed information required by the Release Admission context.

Capability Acceptance is available in this example because it was established in Stage 8.

Its availability does not make Capability Acceptance a universal prerequisite for Release Admission.

The Production Engineering participant determines, in the applicable Collaboration capacity, that the concluded account-deletion Engineering outcome is admitted to the established Release.

```text
Production Engineering participant
        │
        ├── Release capacity
        │       └── established Release
        │
        └── Collaboration capacity
                │
                └── Release Admission determination
```

Using the same participant for both capacities does not merge the governed concerns.

```text
Release establishment
        ≠
Release Admission

Release responsibility
        ≠
Release Admission authority

technical deployment capability
        ≠
Release Admission authority
```

Release Admission remains Collaboration-owned even though the participant performing the determination belongs to the Production Engineering organization.

Likewise, the Release Admission determination does not rewrite the Engineering Conclusion or Capability Acceptance. Those governed outcomes retain their own semantic meaning and provenance.

The determination establishes that the concluded Engineering outcome is admitted to this established Release.

It does not itself establish Release progression.

### 11. Progress the Release

With the Engineering outcome admitted, the Production Engineering participant proceeds with the applicable Release activity in the Release capacity.

Enterprise automation performs the applicable technical activity required by this realization.

Depending on the Release mechanisms used by the enterprise, that activity may include preparing deployable artifacts, executing deployment, performing environment checks, observing deployment behavior, running applicable post-deployment validation, or producing other Release evidence.

The specific mechanisms are illustrative rather than requirements of the Engineering Operating Model.

```text
established Release
        ↓
Release Admission determination
        ↓
applicable Release activity
        ↓
Release evidence
        ↓
Release progression
```

Enterprise automation can execute substantial portions of this activity.

Its technical capability does not independently establish Release progression.

For example:

```text
deployment completed
        ≠
Release progression established

automated checks passed
        ≠
Release progression established

Claude reports expected behavior
        ≠
Release progression established
```

Those results may provide evidence relevant to the applicable Release governance.

The Production Engineering participant evaluates the applicable Release state and evidence using the Release authority established for this scope.

In this realization, the applicable Release conditions are satisfied and the Production Engineering participant establishes the corresponding Release progression.

The same organizational participant has therefore participated in three distinct Release-related concerns:

```text
Production Engineering participant
        │
        ├── Release capacity
        │       │
        │       ├── Release establishment
        │       │
        │       └── Release progression
        │
        └── Collaboration capacity
                │
                └── Release Admission
```

The organizational concentration of those capacities does not collapse their semantics.

This is the same principle demonstrated elsewhere in the contextual examples under a different organizational realization: participant distribution determines where applicable capacities happen to reside, not whether the governed distinctions exist.

The resulting journey can now be viewed end to end:

```text
Product intent
      ↓
Engineering preparation
      ↓
Engineering approach
      ↓
Engineering planning
      ↓
distributed realization
      ↓
cross-organizational context discovery
      ↓
scope adjustment and additional realization
      ↓
integrated validation and evidence
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

This sequence describes the narrative followed by this example.

It does not establish a mandatory workflow, universal ordering of every possible governed concern, required enterprise approval chain, or process template for other Engineering changes.

What matters is that the applicable semantic relationships remain preserved: the Engineering outcome is concluded before it is considered for Release Admission, the Release is established before Release Admission is determined, Release Admission remains Collaboration-owned, and Release progression remains distinct from the determination that admitted the Engineering outcome.

## Evidence and outcomes

The Engineering and Release journey produces evidence and governed outcomes across several participants, organizational structures, and execution mechanisms.

The distribution of those sources does not change the distinction between evidence and the governed determinations that evidence may support.

### Evidence that supported the Engineering outcome

Evidence relevant to the Engineering outcome includes:

- observations of the existing customer-account behavior;
- analysis of the customer-facing deletion path;
- analysis of the shared identity-service dependency;
- application implementation and focused validation results;
- identity-service implementation and focused validation results;
- evidence exposing the unresolved account-linked identity mapping;
- applicable specialist analysis where additional context was required;
- evidence from the additional realization that addressed the mapping;
- integrated validation across the affected application and identity-service behavior;
- enterprise automation results;
- materially relevant Claude-assisted analysis; and
- the relationships among the initial scope, subsequent discovery, adjusted scope, realization, and final validation.

The evidence does not need to originate from one participant or one organizational structure.

```text
Product context ─────────────────────┐
                                     │
Application Engineering evidence ────┤
                                     │
Identity Engineering evidence ───────┤
                                     │
specialist contributions ────────────┤
                                     ├──→ applicable governed
Claude-assisted analysis ────────────┤    evaluation
                                     │
enterprise automation evidence ──────┤
                                     │
Release evidence ────────────────────┘
```

Not every item in this diagram supports the same determination.

Product context may help preserve the relationship to intended capability. Engineering evidence supports evaluation of the Engineering outcome. Release evidence supports applicable Release governance. Specialist and AI-assisted contributions have meaning according to their applicable scope and use.

Their common presence in the Engineering journey does not collapse those distinctions.

Evidence also remains scoped.

The successful application-focused validation performed before the identity mapping was fully understood remains valid evidence about the behavior it actually evaluated.

It does not become false merely because additional applicable context was later discovered.

Likewise, the discovery of the unresolved identity mapping does not erase the successful work that preceded it.

Instead, the evidence collectively shows how the Engineering understanding changed:

```text
application behavior validated
            │
            │ valid within evaluated scope
            ↓
identity behavior investigated
            │
            ↓
material unresolved mapping discovered
            │
            ↓
Engineering context and scope adjusted
            │
            ↓
additional realization
            │
            ↓
integrated validation succeeds
```

Preserving this relationship is more useful than retaining only the final successful result.

It allows the Engineering Conclusion to remain connected to the context against which the work was actually evaluated.

The source of evidence also does not determine its authority or sufficiency.

```text
human produced
      ≠
authoritative by default

specialist produced
      ≠
governed determination

AI produced
      ≠
Engineering authority

automation produced
      ≠
governed outcome
```

Evidence becomes useful through its relationship to the applicable concern, scope, context, and governed evaluation.

### Governed outcomes

Several governed outcomes are established during the example.

| Governed outcome | Applicable ownership in the Engineering Operating Model | Realization in this example |
| --- | --- | --- |
| Product intent | Product System | Established by the Product participant |
| Engineering Conclusion | Engineering System | Established by the Engineering authority holder for the applicable integrated scope |
| Capability Acceptance | Collaboration System | Established by the Product participant exercising the applicable Collaboration capacity |
| Release establishment | Release System | Established by the Production Engineering participant exercising the applicable Release capacity |
| Release Admission determination | Collaboration System | Established by the Production Engineering participant exercising the applicable Collaboration capacity |
| Release progression | Release System | Established by the Production Engineering participant exercising the applicable Release capacity |

The organizational distribution can make some of these distinctions easier to see, but it does not create their semantic ownership.

A System-ownership view of the resulting outcomes is:

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

This representation shows semantic ownership. It does not show lifecycle ordering.

In particular, Release establishment occurs before the Release Admission determination in the journey even though the System-ownership view groups both Release-owned outcomes together.

Similarly, the table does not imply that every Engineering change must establish every listed outcome or use the participant distribution shown here.

### Continuity from intent to release

The example depends on Engineering meaning surviving several kinds of boundary:

```text
Product intent
      │
      │ organizational boundary
      ↓
Engineering context and scope
      │
      ├── Application Engineering
      │
      ├── Identity Engineering
      │
      └── applicable specialist participation
      │
      │ domain + participant boundaries
      ↓
Engineering decisions and realization
      │
      │ materially relevant discovery
      ↓
context and scope adjustment
      │
      ↓
additional realization
      │
      ↓
validation and evidence
      │
      ↓
Engineering Conclusion
      │
      │ organizational / capacity boundary
      ↓
Capability Acceptance
      │
      ↓
Release establishment
      │
      │ capacity boundary
      ↓
Release Admission determination
      │
      ↓
Release activity and evidence
      │
      ↓
Release progression
```

Continuity does not require all of this information to reside in one document, repository, workflow system, conversation, or database.

Nor does it require every intermediate interaction to be preserved indefinitely.

What matters is that materially significant Engineering meaning remains sufficiently connected for subsequent activity and governed determinations.

In this example, that includes preserving enough provenance to understand:

- which Product intent the Engineering activity was intended to realize;
- what Engineering scope and context were initially understood;
- which participants contributed within applicable scopes;
- what Engineering approach and decisions shaped the realization;
- what the initial validation established;
- how the unresolved identity mapping was discovered;
- why that discovery was materially relevant;
- how Engineering scope changed in response;
- what additional realization occurred;
- what final evidence supported Engineering Conclusion;
- which realized capability was evaluated through Capability Acceptance;
- which concluded Engineering outcome was considered for Release Admission;
- which established Release it was admitted to; and
- what Release evidence supported subsequent progression.

This provenance is especially useful where organizational boundaries mean that later participants may not share the memory or local context of the participants who performed earlier activity.

```text
organizational hand-off
        ≠
semantic reset
```

The Engineering meaning needed by the next participant must remain recoverable to the degree required by the applicable context.

The same principle applies to AI and automation.

Claude conversations do not need to be retained wholesale merely because Claude participated. Materially significant AI-assisted analysis, decisions, or evidence should remain sufficiently connected where subsequent Engineering activity depends on them.

Likewise, every enterprise automation log does not become a governed artifact merely because automation produced it. Applicable execution results and evidence should remain connected where they materially support Engineering or Release evaluation.

The goal is not maximal retention.

It is sufficient continuity and provenance for the applicable Engineering situation:

```text
preserve everything
        ✗

preserve nothing beyond
the final outcome
        ✗

preserve materially significant
meaning and provenance
        ✓
```

Greater organizational distribution can make this need more visible because context cannot safely depend on one participant remembering the entire journey.

It does not create a different continuity or provenance principle for enterprises.

## What changed — and what did not

The Enterprise IT context changes how the Engineering Operating Model is realized.

It does not create a different Engineering Operating Model.

### What changed in this context

The principal difference in this realization is the distribution of relevant activity, knowledge, responsibility, and authority across organizational and Engineering-domain boundaries.

The Product participant, Application Engineering participant, Identity Engineering participant, Engineering authority holder, applicable specialists, and Production Engineering participant do not all operate within one immediate working context.

That distribution affects how Engineering meaning must move through the realization.

```text
greater organizational distribution
              ↓
more boundaries across which
Engineering meaning must survive
              ↓
more explicit context routing,
authority resolution,
coordination,
continuity and provenance
where required
```

#### Context is more distributed

No participant is assumed to begin with every piece of context relevant to the account-deletion capability.

Application Engineering understands the customer-facing application within its applicable scope.

Identity Engineering contributes context about the shared identity service.

Specialists contribute additional knowledge where materially relevant.

Production Engineering operates within the applicable Release context.

Claude and enterprise automation operate only with the context and execution conditions made available and applicable to their activities.

The enterprise therefore cannot safely treat the existence of information somewhere in the organization as equivalent to resolved Engineering context.

```text
the enterprise knows
        ≠
the participant knows

the participant can access
        ≠
the context is applicable

the information is available
        ≠
the Engineering meaning is resolved
```

This makes Context Resolution & Composition particularly visible, but it does not change its semantics.

#### Engineering scope may cross organizational boundaries

The customer-facing capability initially appears principally within the application domain, but realization exposes a materially relevant consequence within the shared identity service.

The Engineering scope therefore cannot be determined solely from the organizational boundary of the team that received the change.

```text
organizational ownership
        ≠
complete Engineering scope
```

Applicable Engineering scope follows the Engineering situation.

When new materially relevant context becomes visible, the scope can be adjusted without treating the original plan as immutable or the discovery as an organizational failure.

#### Specialist participation becomes more visible

The enterprise context provides a natural setting for specialist knowledge to enter Engineering activity.

A specialist can identify a concern, contribute analysis, provide evidence, or participate in realization where applicable.

That participation does not automatically make the specialist the authority for the integrated Engineering outcome.

```text
specialist expertise
        ≠
Engineering Conclusion authority

specialist concern
        ≠
automatic approval gate
```

The consequence of specialist input is evaluated within the applicable semantic and authority boundaries.

#### Authority may require more explicit resolution

Organizational distribution can make it less safe to infer authority from proximity to the work.

A repository owner, team lead, platform owner, specialist, Production Engineering participant, or person capable of operating deployment mechanisms may each have substantial responsibility or technical capability.

None of those facts independently establishes authority for a governed determination.

The enterprise realization therefore benefits from making applicable capacity, scope, and authority explicit where ambiguity would otherwise exist.

That does not mean enterprises require more approval roles.

It means unresolved authority should not be replaced with organizational inference.

#### Continuity and provenance become more visible

A Solo Developer may be able to retain substantial local context in one person's memory.

In this enterprise realization, Engineering meaning crosses participant and organizational boundaries.

Later participants may not have been present when an earlier decision was made, when a dependency was discovered, or when Engineering scope changed.

Materially significant context therefore needs sufficient continuity and provenance to remain recoverable.

This may lead to more explicit shared representation in this realization, but the Engineering Operating Model does not prescribe a particular document, ticketing system, workflow engine, repository structure, meeting, or record format.

> **More explicit does not necessarily mean more formal.**

The required representation depends on what Engineering meaning must survive the applicable boundary.

#### Automation can span organizational boundaries

Enterprise automation may build, validate, package, deploy, observe, or otherwise support activity across several organizational domains.

This can make the technical execution topology broader than the authority topology.

```text
automation reach
        │
        │ may span
        ↓
multiple organizational boundaries

        without implying

authority reach
```

The ability of an automated mechanism to execute activity across those boundaries does not grant it authority over the governed determinations associated with them.

### What remained invariant

Despite the different organizational realization, the governing semantic relationships remain the same.

Product intent remains Product-owned.

Engineering determines how the intended capability is realized without silently converting Engineering decisions into Product intent.

Responsibility, technical capability, organizational position, access, and authority remain distinct.

Applicable authority must exist for the governed capacity and scope in which a determination is made.

AI and automation participate within the same applicable Engineering semantics as other participants. Their technical capability does not create additional authority.

Context remains governed by applicability rather than accumulation.

Evidence remains distinct from the governed determination it supports.

Successful local validation does not necessarily establish sufficiency for an integrated Engineering outcome.

Materially relevant failed, incomplete, or conflicting evidence remains meaningful.

Engineering Conclusion remains distinct from Capability Acceptance.

Capability Acceptance remains Collaboration-owned and is not made Product-owned merely because a Product participant performs it.

Release establishment remains distinct from Release Admission.

The Release must be established before the Engineering outcome can be admitted to it.

Release Admission remains Collaboration-owned even when the determination is performed by a participant within the Production Engineering organization.

Capability Acceptance is not a universal prerequisite for Release Admission.

Release Admission remains distinct from Release progression.

Technical ability to deploy or operate Release mechanisms does not establish Release Admission or Release progression authority.

Continuity and provenance remain applicable across the journey even though the mechanisms used to preserve them may differ with context.

The Enterprise realization can therefore be summarized as:

```text
what changed
────────────────────────────────
participant distribution
organizational boundaries
domain boundaries
context-routing needs
coordination topology
representation of continuity
execution topology

            │
            │ did not change
            ↓

what remained governed
────────────────────────────────
System ownership
semantic boundaries
applicable authority
evidence semantics
governed determinations
continuity and provenance
conformance obligations
```

The increased visibility of governance in an enterprise setting should not be mistaken for a requirement to maximize governance ceremony.

A significant Solo Developer change may require deeper context resolution, validation, evidence, or governance than a routine Enterprise IT change.

Likewise, a large enterprise does not become more conforming merely by having more participants, organizational structures, approval mechanisms, artifacts, or automated controls.

> **Engineering significance and applicable context determine the required depth of realization; organizational scale does not.**

## What this example does not imply

This example illustrates one possible enterprise realization of the Engineering Operating Model.

It does not imply that:

- enterprises must organize Product, Engineering, and Production Engineering as separate organizations, departments, teams, or functions;
- a Product organization is equivalent to the Product System, an Engineering organization to the Engineering System, or a Production Engineering organization to the Release System;
- Collaboration requires a separate Collaboration organization, participant, department, workflow, or approval body;
- organizational size or structure determines Engineering significance, governance depth, evidence depth, or conformance;
- enterprises inherently require more governance, approvals, artifacts, meetings, hand-offs, or ceremony than smaller Engineering contexts;
- the participant capacities and authority distribution shown here are required for other enterprise realizations;
- job title, seniority, organizational position, responsibility, expertise, repository ownership, system ownership, technical access, or operational capability independently establishes authority;
- an Engineering change must involve separate Application Engineering, Identity Engineering, specialist, or Production Engineering participants;
- specialist participation is universally required, or specialist expertise automatically creates authority over a governed determination;
- Engineering scope is determined by organizational ownership or team boundaries;
- every participant must receive all enterprise information for context to be sufficiently resolved;
- more available information necessarily produces better Engineering context;
- Claude, Claude Code, or any particular AI tooling is required by the Engineering Operating Model;
- AI participation introduces different Engineering semantics or grants AI authority over governed determinations;
- enterprise automation acquires authority because it can execute activity across organizational or technical boundaries;
- successful local, automated, specialist, or AI-assisted validation independently establishes Engineering Conclusion;
- the artifacts, evidence sources, execution mechanisms, organizational hand-offs, or representations shown here form a universal required set;
- the eleven narrative stages form a mandatory workflow, approval sequence, lifecycle implementation, or enterprise process;
- Capability Acceptance is a universal prerequisite for Release establishment or Release Admission;
- Release establishment and Release Admission are the same determination;
- Release Admission becomes Release-owned because it is performed by a participant within the Production Engineering organization;
- technical ability to deploy, promote, roll back, bypass, or otherwise operate Release mechanisms establishes Release Admission or Release progression authority; or
- this Enterprise IT context represents a higher maturity level, stronger form of governance, more complete adoption, or greater degree of conformance than the Solo Developer or Startup Team contexts.

Other enterprise realizations may distribute participants, responsibilities, authority, context, evidence, automation, and organizational structures differently.

They remain valid realizations where the applicable canonical Engineering semantics and obligations are preserved.

## Canonical references

This example applies concepts defined by the canonical Engineering Operating Model.

The references below provide routes to the authoritative semantics most directly exercised by the example. They are not prerequisites for reading the example, and their presence or absence does not establish conformance, exemption, or complete coverage.

| Concept exercised | Canonical source |
| --- | --- |
| Product intent and Product-owned capability semantics | [Product Principles Specification](../../engineering_platform/product_system/governance/product_principles_specification.md) |
| Engineering lifecycle, Engineering realization, and Engineering Conclusion | [Engineering Lifecycle Specification](../../engineering_platform/engineering_system/governance/engineering_lifecycle_specification.md) |
| Capability Acceptance | [Capability Acceptance Specification](../../engineering_platform/collaboration_system/product_engineering/capability_acceptance_specification.md) |
| Release establishment and Release representation | [Release Record Specification](../../engineering_platform/release_system/progression/release_record_specification.md) |
| Release Admission | [Release Admission Specification](../../engineering_platform/collaboration_system/engineering_release/release_admission_specification.md) |
| Release progression | [Release Progression Specification](../../engineering_platform/release_system/progression/release_progression_specification.md) |
| Participant capacity, applicable scope, and authority | [Participation & Scope Specification](../../engineering_platform/specifications/participation_scope_specification.md) |
| Applicable context resolution and composition | [Context Resolution & Composition Specification](../../engineering_platform/specifications/context_resolution_composition_specification.md) |
| Executable Engineering conditions and execution availability | [Execution Enablement Specification](../../engineering_platform/specifications/execution_enablement_specification.md) |
| Validation evidence and governance integration | [Governance & Validation Integration Specification](../../engineering_platform/specifications/governance_validation_integration_specification.md) |
| Continuity and provenance across participants, activity, and governed outcomes | [Continuity & Provenance Specification](../../engineering_platform/specifications/continuity_provenance_specification.md) |
| AI-assisted Engineering and Engineering Automation | [Engineering Automation](../../engineering_platform/engineering_automation/README.md) |

These references define the canonical semantics.

The organizational structures, participant distribution, shared identity-service dependency, specialist participation, Claude and Claude Code usage, enterprise automation, evidence representation, and execution mechanisms shown in this example are illustrative realization choices.

Where an illustrative choice appears to conflict with a canonical semantic, authority boundary, ownership boundary, lifecycle relationship, or other applicable obligation, the canonical Engineering Operating Model governs.
