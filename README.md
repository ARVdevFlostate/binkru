# binkru

**An Engineering Operating Model for governed human, AI and automation
participation.**

binkru is an open Engineering Operating Model for structuring how
Product, Engineering, Release, humans, AI, and automation participate in
software Engineering without allowing technical capability to silently
become Engineering authority.

It is designed around a simple premise:

> AI and automation should be able to participate deeply in Engineering
> without requiring Engineering semantics, governance, authority, or
> accountability to be surrendered to the tools performing the work.

## Why binkru exists

Software Engineering is increasingly performed by mixed participants.

Humans make decisions. AI generates and analyzes Engineering material.
Agents perform increasingly complex development activity. Automation
validates, integrates, builds, deploys, and observes software.

The difficult problem is no longer simply whether these participants can
perform Engineering work.

The difficult problem is determining:

-   what work is being performed;
-   which Engineering context applies;
-   which sources are authoritative;
-   who or what may participate;
-   what responsibilities apply;
-   where authority resides;
-   which governance and validation requirements apply;
-   what evidence must be preserved; and
-   how Engineering activity remains understandable and continuable
    across participants, tools, and time.

binkru provides an Engineering Operating Model for addressing those
concerns.

## What binkru is

binkru defines an Engineering Platform with two complementary
dimensions:

1.  **Engineering Systems** --- authoritative domain semantics, governed
    state, lifecycle, decisions, authority, and outcomes.
2.  **Engineering Capabilities** --- common logical abilities through
    which participants operate within and across those authoritative
    semantics.

The Engineering Platform currently recognizes four Engineering Systems:

-   **Product System**
-   **Collaboration System**
-   **Engineering System**
-   **Release System**

It defines six Engineering Capabilities:

-   **Discovery & Navigation**
-   **Participation & Scope**
-   **Context Resolution & Composition**
-   **Execution Enablement**
-   **Governance & Validation Integration**
-   **Continuity & Provenance**

Together, these provide a common operating architecture for governed
Engineering activity involving human, AI, automation, and mixed
participants.

## What binkru is not

binkru is not a prescribed software architecture, application framework,
development tool, agent framework, CI/CD platform, repository structure,
or mandatory technology stack.

It does not require an existing product or project to replace its
application architecture.

It does not require every organization or project to realize the model
through the same processes, services, repositories, tools, runtimes, or
deployment topology.

And governance does not mean that every Engineering activity must pass
through the same heavyweight process.

The model separates authoritative Engineering semantics from the
mechanisms used to realize them so that implementations can remain
appropriate to their scale, risk, participants, and Engineering
environment.

## Human, AI and automation participation

binkru treats human, AI, automation, and mixed-participant Engineering
as part of the same governed Engineering environment.

The participant performing an activity does not determine the authority
of the outcome.

An AI system may be technically capable of generating code, proposing a
decision, modifying an artifact, executing a workflow, or invoking
another tool. That technical capability does not by itself grant the AI
authority to establish Engineering truth, approve Product intent,
conclude Engineering, admit an outcome to Release, or authorize Release.

The same principle applies to humans and automation:

> **Technical capability, responsibility, access, and authority are
> distinct concepts.**

This allows AI and automation to participate deeply without requiring a
parallel "AI Engineering" lifecycle.

## Existing products and projects

binkru is intended to be realizable around existing Engineering
environments.

Its architectural concepts are not mandatory physical repository,
service, runtime, process, or deployment boundaries.

A conforming implementation may therefore integrate existing tools,
systems, workflows, repositories, and execution mechanisms while
preserving the applicable Engineering semantics, authority boundaries,
governance obligations, continuity, and provenance requirements.

Adoption does not inherently require rewriting the product being
engineered.

## Start small

Using binkru does not require implementing the entire model at once.

A project can begin with the Engineering concerns that matter for its
current context and progressively establish additional capabilities and
governance as required.

The objective is not governance for its own sake.

The objective is to preserve sufficient Engineering semantics,
authority, evidence, and continuity for the work being performed.

This makes the model applicable to contexts ranging from early product
development and small Engineering teams to larger multi-participant
Engineering environments.

## Repository structure

The canonical Engineering Operating Model is maintained under:

``` text
engineering_platform/
```

Its major areas are:

``` text
engineering_platform/
├── principles/
├── glossary/
├── specifications/
├── product_system/
├── collaboration_system/
├── engineering_system/
├── release_system/
└── engineering_automation/
```

The architectural entry point is:

[`engineering_platform/README.md`](engineering_platform/README.md)

## Where to start

If you are new to binkru, begin with the five-minute orientation:

[`ORIENTATION.md`](ORIENTATION.md)

For an architectural overview, begin with:

[`engineering_platform/README.md`](engineering_platform/README.md)

For the foundational principles:

[`engineering_platform/principles/engineering_platform_principles.md`](engineering_platform/principles/engineering_platform_principles.md)

For canonical terminology:

[`engineering_platform/glossary/engineering_platform_glossary.md`](engineering_platform/glossary/engineering_platform_glossary.md)

For the Engineering Capability Model:

[`engineering_platform/specifications/capability_model_specification.md`](engineering_platform/specifications/capability_model_specification.md)

For architecture realization and implementation boundaries:

-   [`engineering_platform/specifications/realization_model_specification.md`](engineering_platform/specifications/realization_model_specification.md)
-   [`engineering_platform/specifications/implementation_architecture_specification.md`](engineering_platform/specifications/implementation_architecture_specification.md)

The Product, Collaboration, Engineering, Release, and Engineering
Automation areas provide their respective detailed specifications and
governed artifacts.

## Status

binkru is being established as an open Engineering Operating Model.

The current repository provides the canonical Engineering Platform
architecture and specifications. Additional adoption guidance, examples,
implementation support, and tooling may evolve independently of the
canonical architectural model.

## About the name

**binkru** is named after Binkie, a British Shorthair cat affectionately known as "Binkru." Binkie has a sister, Eevee. Both have been known to provide occasional supervision of Engineering activities.

## Contributing

Contribution guidance is provided in
[`CONTRIBUTING.md`](CONTRIBUTING.md).

## Security

Security-related guidance and reporting information are provided in
[`SECURITY.md`](SECURITY.md).

## Code of Conduct

Participation in the binkru community is governed by
[`CODE_OF_CONDUCT.md`](CODE_OF_CONDUCT.md).

## License

binkru is made available under the terms provided in
[`LICENSE`](LICENSE).
