# Product Artifact Model Specification

## 1. Purpose

This specification defines the Product Artifact Model for the Product System.

It identifies the authoritative Product artifact types, their purpose, ownership, governance relationships, lifecycle progression and traceability requirements.

The Product Artifact Model establishes a consistent governance framework for Product artifacts that may be instantiated by individual Product Workflows.

This specification defines the Product-owned artifact model. It does not define Collaboration or Engineering artifacts.

---

# 2. Scope

This specification applies to all artifacts governed by the Product System.

It defines:

- supported Product artifact types;
- artifact purpose;
- artifact ownership;
- governance relationships;
- lifecycle progression;
- traceability expectations; and
- artifact hierarchy.

Artifacts governed by the Collaboration System and Engineering System are outside the scope of this specification.

---

# 3. Principles

The Product Artifact Model is governed by the following principles.

- Every Product artifact has a clearly defined purpose.
- Every Product artifact has a single authoritative Product owner.
- Every Product artifact shall preserve approved business intent.
- Every Product artifact shall be traceable to higher-level Product artifacts.
- Product artifacts shall not duplicate responsibilities.
- Product artifacts shall evolve through governed Product lifecycle states.
- Strategic Product decisions remain human-owned.
- AI may assist in creating Product artifacts but does not become their authority.
- Product governance concludes with approved draft Epics.

---

# 4. Supported Artifact Types

The Product System currently defines the following Product artifact types.

## Vision

Defines the long-term purpose, direction and identity of the product.

The Vision represents the highest level of Product intent.

---

## Product Decision Record

Captures significant strategic Product decisions together with their rationale.

Product Decision Records influence long-term Product direction.

---

## Roadmap

Defines the planned evolution of the product.

The Roadmap translates Product Vision and Product Decisions into planned delivery outcomes.

---

## Milestone Plan

Defines significant intermediate objectives required to realise the Product Roadmap.

---

## Release Plan

Defines the scope and objectives of an individual Product release.

---

## Epic

Represents a coherent body of business capability derived from an approved Release Plan.

The Epic is the final Product artifact governed entirely within the Product System.

Approved draft Epics become Product inputs to the Collaboration System.

---

# 5. Artifact Ownership

Every Product artifact has an identified human owner.

The owner is responsible for:

- correctness;
- governance compliance;
- lifecycle progression within the Product System;
- approval; and
- ongoing maintenance.

AI may assist with artifact creation but does not own Product artifacts.

---

# 6. Artifact Authority

Higher-level Product artifacts govern lower-level Product artifacts.

Lower-level artifacts shall not contradict approved higher-level artifacts.

The Product System defines the following governance hierarchy.

```text
Vision
    │
    ▼
Product Decision Records
    │
    ▼
Roadmap
    │
    ▼
Milestone Plans
    │
    ▼
Release Plans
    │
    ▼
Draft Epics
```

Governance responsibility concludes with approved draft Epics.

Subsequent lifecycle progression is governed by the Collaboration System.

---

# 7. Traceability

Every Product artifact shall preserve traceability to one or more governing Product artifacts.

Examples include:

- Product Decision Record → Vision
- Roadmap → Vision
- Roadmap → Product Decision Records
- Milestone Plan → Roadmap
- Release Plan → Milestone Plan
- Epic → Release Plan

Traceability shall remain intact throughout the Product lifecycle.

---

# 8. Product Lifecycle Relationships

Product artifacts evolve through progressively more detailed stages of Product planning.

A typical Product progression is:

```text
Vision
    │
    ▼
Product Decision Records
    │
    ▼
Roadmap
    │
    ▼
Milestone Plans
    │
    ▼
Release Plans
    │
    ▼
Draft Epics
```

Following Product approval, draft Epics enter the Collaboration System for collaborative refinement.

The Product Workflow may revisit earlier Product artifacts as Product understanding evolves.

---

# 9. Human and AI Responsibilities

The Product System supports AI-assisted Product development.

Humans remain responsible for:

- defining Product intent;
- making Product decisions;
- approving Product artifacts;
- accepting Product accountability.

AI may assist by:

- drafting artifacts;
- analysing alternatives;
- recommending improvements;
- validating against Product checklists;
- composing Product artifacts from reusable Product System assets.

AI does not approve Product artifacts.

---

# 10. Relationship to Product Workflow

The Product Artifact Model defines reusable Product artifact types.

The Product Workflow instantiates those artifact types for a specific product.

The Product Workflow owns project-specific Product content.

The Product System owns the reusable Product governance assets.

---

# 11. Relationship to Composition

Each supported Product artifact is defined through four complementary Product assets:

- Methodology
- Template
- Checklist
- Composition Specification

Together these assets define how a Product artifact is created, validated and composed.

---

# 12. Artifact Identity

Each Product artifact represents a unique, authoritative instance of a particular Product artifact type within a Product Workflow.

Product artifacts retain their identity throughout Product governance.

Approved draft Epics subsequently continue their lifecycle within the Collaboration System.

Superseded Product artifacts remain part of Product history and preserve traceability.

---

# 13. Conformance

A Product Workflow conforms to the Product Artifact Model when:

- Product artifacts conform to their defined type;
- governance relationships are preserved;
- Product ownership is maintained;
- higher-level Product authority is respected;
- traceability is preserved;
- Product governance requirements are satisfied; and
- approved draft Epics are ready to enter the Collaboration System.
