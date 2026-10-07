# Five-minute orientation

> **About this orientation**
>
> This is an explanatory entry point to binkru. It provides a compact mental model of how the major parts of the Engineering Operating Model relate. It does not replace or redefine the canonical Engineering Operating Model under [`engineering_platform/`](engineering_platform/).

binkru is an Engineering Operating Model for governed human, AI and automation participation in Engineering.

It provides a model for reasoning about Product intent, Engineering work and Release while preserving the semantics, scope, authority, evidence and continuity that govern them.

It does not prescribe a development methodology, organizational structure, toolchain or universal workflow. Different Engineering contexts can realize the model differently while preserving the same governing semantics.

## 1. Start with the model

The easiest way to approach binkru is to separate **what must remain meaningful** from **how a particular organization or project chooses to realize it**.

binkru defines governed Engineering semantics and the relationships between them. A realization may use different people, tools, automation, workflows and physical structures as long as the applicable semantics and authority boundaries are preserved.

This distinction allows the same Engineering Operating Model to support a solo developer, a distributed team, substantial AI participation or a larger organizational environment without defining a separate model for each.

## 2. Two dimensions: Systems and Capabilities

binkru organizes the Engineering Operating Model along two distinct dimensions:

```text
Engineering Systems                 Engineering Capabilities
───────────────────                 ────────────────────────
Product                             Discovery & Navigation
Collaboration                       Participation & Scope
Engineering                         Context Resolution & Composition
Release                             Execution Enablement
                                    Governance & Validation Integration
                                    Continuity & Provenance

governed semantics                  abilities needed to interact
and state                           with governed Engineering state
```

**Engineering Systems** describe where governed semantics and state belong.

The four Systems are:

- **Product System** — governs Product intent and Product-owned state.
- **Collaboration System** — governs concerns that cross System boundaries and require governed collaboration between them.
- **Engineering System** — governs the realization and conclusion of Engineering work.
- **Release System** — governs Release state and progression.

**Engineering Capabilities** describe the logical abilities participants need in order to interact with governed Engineering state.

The six Capabilities are:

- **Discovery & Navigation**
- **Participation & Scope**
- **Context Resolution & Composition**
- **Execution Enablement**
- **Governance & Validation Integration**
- **Continuity & Provenance**

Systems and Capabilities are therefore not ten peer components. They describe different dimensions of the same Engineering Operating Model.

## 3. Keep the concerns distinct

A useful first distinction is:

```text
Product intent
      ≠
Engineering outcome
      ≠
Release progression
```

These concerns are related, but they are not interchangeable.

Product establishes the intended capability and associated Product meaning. Engineering realizes work and governs its Engineering outcomes under applicable Engineering semantics. Release governs established Release state and its progression.

Collaboration governs important relationships across these concerns where determinations cross System boundaries.

Movement between concerns does not silently transfer authority. Performing Engineering work, for example, does not by itself grant authority over Product intent or Release progression.

binkru defines the governed relationships needed to preserve these distinctions. It does not turn them into a mandatory sequence of development steps.

## 4. Participation does not create authority

Humans, AI and automation can all participate in Engineering activities.

Their ability to perform an activity does not by itself determine the authority of the outcome.

```text
               PARTICIPATION

          Human   AI   Automation
             \     |     /
              \    |    /
               ▼   ▼   ▼
             Engineering
              activity

                  │
                  │ does not by itself establish
                  ▼

               AUTHORITY
```

In particular:

```text
technical capability   ≠  authority
responsibility         ≠  authority
access                 ≠  authority
```

Authority follows the applicable Engineering semantics and established authority model, not the type of participant or the sophistication of the tooling involved.

An AI participant may therefore analyze context, propose an approach, generate or modify code, execute permitted tools, inspect failures or assemble evidence without those technical capabilities silently granting authority to establish governed outcomes.

The same principle applies to humans and automation: participant type does not manufacture authority.

## 5. Engineering does not always resolve cleanly

Engineering conditions do not always produce an immediate positive or negative outcome. Relevant information may remain unresolved, conflicting, partial, stale, unavailable, or uncertain.

These conditions should remain distinguishable rather than being silently converted into stronger or unrelated Engineering outcomes.

For a focused explanation, see [When Engineering Does Not Resolve Cleanly](guides/failure_and_uncertainty.md).

## 6. Context changes realization, not the model

The Engineering Operating Model does not require every Engineering environment to look alike.

A solo developer may carry several capacities that are distributed across multiple participants in a startup. An enterprise environment may distribute the same concerns across organizational domains and specialist participants.

```text
                    SAME MODEL

       ┌──────────────┼──────────────┐
       │              │              │
       ▼              ▼              ▼
 Solo developer   Startup team   Enterprise IT
       │              │              │
 concentrated     distributed     distributed
  capacities      participants      domains
                                      and
                                  specialists
       │              │              │
       └──────────────┼──────────────┘
                      ▼
             different realization

                      │
                      ▼
              governing semantics
                 remain common
```

Concentrating several capacities in one person does not collapse the semantic distinctions between them. Distributing those capacities across more people or organizational boundaries does not create a more complete or mature version of binkru.

The required depth of representation, coordination, evidence and governance can depend on the Engineering context and significance of the change.

The principle remains:

> **Context changes how the Engineering Operating Model is realized; it does not create a different model.**

## Where to go next

You do not need to read the repository in a fixed order. Choose the path that matches what you want to understand next.

| If you want to… | Go to… |
| --- | --- |
| Explore the canonical Engineering Operating Model | [`engineering_platform/`](engineering_platform/) |
| Understand the four Engineering Systems | [`engineering_platform/README.md`](engineering_platform/README.md) |
| Understand the Engineering Capability Model | [`engineering_platform/specifications/capability_model_specification.md`](engineering_platform/specifications/capability_model_specification.md) |
| See the model operating in concrete organizational contexts | [`examples/contextual/`](examples/contextual/) |
| Explore the worked-example collection | [`examples/`](examples/) |
| Begin applying binkru to an existing Engineering environment | [`guides/getting_started.md`](guides/getting_started.md) |
| Understand failure, conflict and uncertainty | [`guides/failure_and_uncertainty.md`](guides/failure_and_uncertainty.md) |
| Evaluate implementation conformance | [`guides/conformance.md`](guides/conformance.md) |
| Understand the realization model | [`engineering_platform/specifications/realization_model_specification.md`](engineering_platform/specifications/realization_model_specification.md) |
| Understand the implementation architecture | [`engineering_platform/specifications/implementation_architecture_specification.md`](engineering_platform/specifications/implementation_architecture_specification.md) |
| Explore Engineering Automation | [`engineering_platform/engineering_automation/`](engineering_platform/engineering_automation/) |

The orientation explains the model. The examples illustrate it. The canonical Engineering Platform defines the governing semantics.
