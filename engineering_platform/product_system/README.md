# Product System

The **Product System** is the reusable product governance framework within the Engineering Platform.

It defines the principles, methodology, templates, validation rules and composition specifications required to create consistent, governed product artifacts.

The Product System is **product-agnostic**. It does not contain any project-specific knowledge or decisions. Instead, it provides reusable assets that can be applied to any product.

---

# Purpose

The Product System exists to:

- establish consistent product governance;
- standardize product artifact creation;
- improve quality and consistency;
- enable repeatable product development practices;
- support AI-assisted product development; and
- enable future automated artifact composition.

---

# Scope

The Product System provides reusable assets for creating and governing product artifacts including:

- Vision
- Product Decision Records 
- Roadmaps
- Milestone Plans
- Release Plans
- Epics

Project-specific artifacts are intentionally **not** part of the Product System.

---

# Product Artifact Model

Every reusable product artifact is defined by four complementary assets.

## Methodology

Describes **how a product artifact should be created**.

Examples include:

- developing a Vision;
- writing a Product Decision Record;
- creating a Roadmap; and
- planning Releases.

Methodology guides are intended primarily for humans and AI collaborators.

---

## Template

Defines **the standard structure** of a product artifact.

Templates specify required sections, formatting and expected content.

Templates do not contain project-specific information.

---

## Checklist

Defines **how a completed artifact is validated**.

Checklists promote consistency, completeness and quality before an artifact is approved.

---

## Composition Specification

Defines **how a product artifact is composed from reusable Product System assets and project-owned knowledge**.

Composition Specifications are intended primarily for automated composition mechanisms that assemble Product artifacts from governed Product inputs.

They define:

- required inputs;
- governing assets;
- composition rules;
- validation requirements;
- expected outputs; and
- composition behaviour.

---

# Repository Structure

```text
product_system/
├── governance/
├── methodology/
├── templates/
├── checklists/
└── composition/
```

## governance

Defines the governing specifications for the Product System.

Examples include:

- Product Governance
- Product Principles
- Product Lifecycle
- Product Artifact Model

---

## methodology

Defines recommended approaches for creating product artifacts.

These documents describe product development practices rather than artifact structure.

---

## templates

Defines reusable artifact templates.

Templates describe the structure of an artifact without including project-specific content.

---

## checklists

Defines validation checklists for each supported artifact.

Checklists assist reviewers, product owners and automated tooling.

---

## composition

Defines artifact-specific composition specifications.

These specifications describe how reusable Product System assets and project-owned knowledge are assembled into validated project artifacts.

---

## Terminology

Cross-Platform terminology and semantic distinctions are summarized in the [Engineering Platform Glossary](../glossary/engineering_platform_glossary.md).

Authoritative Product System semantics remain established by the applicable Product System specifications and governance.

---

# Relationship to Projects

The Product System provides reusable assets.

Projects own product-specific artifacts produced using the Product System, including:

- business context;
- Product Vision;
- Product Decision Records;
- Roadmap;
- Milestone Plan;
- Release Plan; and
- draft Epics.

Projects consume the Product System through their Product Workflow.

---

# Relationship to Product Workflow

The Product System defines reusable product governance.

The Product Workflow instantiates that governance for a specific product.

```text
Product System
        │
        ▼
Product Workflow
        │
        ▼
Project Product Artifacts
```

---

# Relationship to Engineering System

The Product System precedes the Engineering System.

Approved Product artifacts become inputs to the Collaboration System, where Product and Engineering collaboratively establish engineering readiness before Engineering execution begins.

```text
Product System
        │
        ▼
Product Workflow
        │
        ▼
Collaboration System
        │
        ▼
Engineering System
```

---

# Future Direction

The Product System is intentionally independent of any implementation technology.

Tools, including AI assistants and automated composition mechanisms, may consume Product System artifacts but MUST preserve the semantics and authority defined by the Product System.

---

# Guiding Principle

> **The Product System defines reusable product knowledge. Projects provide product context. Together they produce governed product artifacts.**
