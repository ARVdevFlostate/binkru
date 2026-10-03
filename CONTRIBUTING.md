# Contributing to binkru

Thank you for your interest in contributing to binkru.

binkru is an open Engineering Operating Model for governed human, AI and automation participation. Contributions that improve the model, its clarity, its usability, or supporting material are welcome.

This document describes the expectations for contributing to the project.

## Before contributing

Start with the repository [`README.md`](README.md) for an overview of binkru.

For changes to the Engineering Operating Model, also review:

- [`engineering_platform/README.md`](engineering_platform/README.md)
- [`engineering_platform/principles/engineering_platform_principles.md`](engineering_platform/principles/engineering_platform_principles.md)
- [`engineering_platform/glossary/engineering_platform_glossary.md`](engineering_platform/glossary/engineering_platform_glossary.md)

Changes affecting a particular Engineering System, Engineering Capability, realization contract, or implementation boundary should also consider the applicable specifications.

You do not need to understand every part of binkru before proposing an improvement. You should, however, understand the semantics directly affected by the proposed change.

## Ways to contribute

Useful contributions may include:

- identifying ambiguity, inconsistency, or missing semantics;
- improving explanations or navigation;
- correcting errors;
- proposing changes to Engineering concepts or contracts;
- improving examples and adoption guidance;
- identifying implementation or realization concerns;
- contributing supporting tools or automation where such components exist; and
- reporting practical experience applying the model.

A contribution does not need to be large to be useful.

## Architectural contributions

The Engineering Operating Model is intentionally governed as a coherent architecture.

Changes to one area may affect semantics established elsewhere. A proposed change should therefore preserve applicable:

- Engineering System boundaries;
- Engineering Capability boundaries;
- semantic ownership;
- responsibility and authority distinctions;
- lifecycle and state semantics;
- governance and validation obligations;
- continuity and provenance requirements;
- realization contracts; and
- implementation boundaries.

Where a contribution intentionally changes one or more of these, the change should identify the affected semantics and update all applicable authoritative material coherently.

Implementation convenience alone is not sufficient reason to change an architectural contract.

## Authority and contributions

Submitting, reviewing, discussing, implementing, or technically enabling a contribution does not by itself establish Engineering authority or make the proposed semantics authoritative.

A contribution becomes part of binkru only when it is accepted and incorporated through the project's governance process.

This distinction allows proposals to be explored openly without confusing participation with authority.

## Proposing changes

Keep each contribution focused on one coherent concern where practical.

For substantive changes, explain:

- the problem being addressed;
- the current behavior or semantics;
- the proposed change;
- why the change is needed;
- the architectural areas affected; and
- any compatibility, migration, or conformance implications that are known.

If a proposal intentionally changes an existing architectural contract, state that explicitly.

Do not hide architectural changes inside terminology cleanup, formatting changes, examples, or implementation work.

## Terminology

Use terminology defined by the Engineering Operating Model consistently.

The canonical glossary is:

[`engineering_platform/glossary/engineering_platform_glossary.md`](engineering_platform/glossary/engineering_platform_glossary.md)

When introducing a new term, first determine whether an existing concept already expresses the intended semantics.

New terminology that introduces a distinct Engineering concept should be defined clearly and used consistently across affected material.

Project identity and architectural terminology are intentionally separate. Use `binkru` for the project and model identity where appropriate; do not unnecessarily prefix established architectural concepts such as Engineering Platform, Product System, Engineering System, or Engineering Capability Model with `binkru`.

## Documentation changes

Documentation changes should preserve semantic precision.

Editorial improvements are welcome, but wording changes to normative or architectural material should be treated as semantic changes when they alter meaning, obligation, authority, ownership, lifecycle, scope, or conformance.

Examples and explanatory material must not contradict the canonical model.

## Tooling and implementation contributions

Supporting software, automation, examples, or other implementation artifacts must not silently redefine canonical Engineering semantics.

Implementation artifacts may realize, project, validate, navigate, or automate the model, but implementation behavior does not become authoritative merely because it is executable.

Where implementation constraints reveal a genuine architectural issue, raise the architectural concern explicitly rather than resolving it only in implementation.

## Pull requests

Before submitting a pull request:

- keep the change scoped and internally coherent;
- review affected terminology and cross-references;
- update related specifications when the semantics require it;
- avoid unrelated cleanup;
- ensure relative links introduced or changed by the contribution resolve correctly; and
- explain any intentional architectural change in the pull request description.

Large architectural changes are easier to evaluate when the problem and intended semantic change have been discussed before substantial implementation work begins.

## Contributions and licensing

binkru is licensed under the Apache License, Version 2.0.

Unless explicitly stated otherwise, contributions intentionally submitted for inclusion in binkru are submitted under the terms of the Apache License, Version 2.0, consistent with Section 5 of the license.

By contributing, you represent that you have the right to submit the contribution under those terms.

See [`LICENSE`](LICENSE) for the full license terms and [`NOTICE`](NOTICE) for attribution information.

## Conduct

Participation in the binkru project is subject to [`CODE_OF_CONDUCT.md`](CODE_OF_CONDUCT.md).

## Security

Do not use a public contribution to disclose a security vulnerability that should be handled privately.

See [`SECURITY.md`](SECURITY.md) for security reporting guidance.
