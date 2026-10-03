# Project Prompt Readiness Checklist

## 1. Purpose

This checklist verifies whether a project provides the common project-level prerequisites necessary for Engineering Automation Prompt Governance and Prompt Generation to operate reliably.

Project Prompt Readiness does not require activity-specific Product, Collaboration, Engineering, or Release information to exist before that information becomes applicable under the governing lifecycle.

Project Prompt Readiness does not establish:

- prompt conformance;
- execution readiness;
- Product, Collaboration, Engineering, or Release lifecycle readiness;
- participant authority;
- completeness of project artifacts;
- completeness of Development Standards; or
- readiness for any particular governed activity.

Activity-specific requirements remain subject to participant, activity, context, authority, and Generation Basis resolution and validation at generation time.

---

## 2. Use

Apply this checklist to determine whether a project provides the common conditions required for governed Prompt Generation.

The checklist evaluates project-level **resolvability and support**, not whether all possible prompt inputs already exist.

A checklist item is satisfied where the project provides a conforming means to resolve, preserve, distinguish, or evaluate the stated concern when it becomes applicable.

An item SHALL NOT be considered unsatisfied merely because an artifact, decision, standard, implementation detail, or lifecycle state that is not yet applicable has not been established.

Where an item is not applicable to the project, that condition SHOULD be recorded rather than forcing an artificial project structure or configuration solely to satisfy this checklist.

Checklist completion SHALL NOT substitute for generation-time resolution or Prompt Validation.

---

## 3. Project Identification and Governing Basis

- [ ] Project identity is unambiguous.

- [ ] Applicable Engineering Platform principles and specifications can be resolved.

- [ ] Applicable Product, Collaboration, Engineering, and Release System semantics can be resolved where those systems participate in the project.

- [ ] Project-specific governing sources can be distinguished from Platform-level and Engineering System governing sources.

- [ ] The project does not establish a project-local interpretation of the Engineering Operating Model that overrides or replaces its authoritative governing sources.

### Review Notes

_Record observations, unresolved matters, or project-specific considerations here._

---

## 4. Participant Resolution

- [ ] Governed project participants can be identified where participant-specific execution is required.

- [ ] Applicable participant capacity and scope can be resolved.

- [ ] Applicable authority bindings can be resolved to their governing basis rather than inferred solely from participant type, capacity, responsibility, repository access, technical permission, or execution capability.

- [ ] Human, AI, and automation participants can be distinguished where the distinction is material to the governed activity.

- [ ] Unresolved participant authority can remain unresolved rather than being inferred or broadened to permit execution.

- [ ] AI or automation acting independently under persistent scope, responsibility, or delegated authority can be distinguished from transient execution assistance.

### Review Notes

_Record observations, unresolved matters, or project-specific considerations here._

---

## 5. Governed Activity Resolution

- [ ] Governed activities can be resolved to their applicable Engineering System or governed cross-system interaction.

- [ ] Activity resolution can identify the applicable lifecycle context.

- [ ] Activity resolution can identify the governing semantic sources applicable to the resolved activity.

- [ ] Activity resolution does not rely solely on free-form prompt wording to establish governed semantics.

- [ ] An unresolved or materially ambiguous activity can remain unresolved rather than being silently mapped to a guessed governed activity.

- [ ] Activity-specific context requirements can be determined without requiring downstream information before the governing lifecycle makes that information applicable.

### Review Notes

_Record observations, unresolved matters, or project-specific considerations here._

---

## 6. Authoritative Project Source Resolution

- [ ] Authoritative project artifacts and governed state can be located when applicable to a resolved activity.

- [ ] Source resolution preserves source identity, semantic ownership, and authority.

- [ ] Project-owned authoritative sources can be distinguished from derived Engineering Automation representations.

- [ ] Missing authoritative sources can be surfaced explicitly.

- [ ] Material conflicts among authoritative sources can be surfaced rather than silently resolved through arbitrary source ordering.

- [ ] Source availability or retrieval capability is not treated as semantic ownership or authority.

### Review Notes

_Record observations, unresolved matters, or project-specific considerations here._

---

## 7. Project Specialization and Development Standards Resolution

- [ ] Project-specific terminology, conventions, architecture, decisions, and other governed specialization can be resolved where applicable.

- [ ] Project or subsystem specialization can be distinguished from the higher Engineering Platform and Engineering System semantics it specializes.

- [ ] Project specialization cannot override, weaken, broaden, or replace applicable Engineering Platform or Engineering System semantics.

- [ ] Applicable Development Standards can be discovered where a governed activity depends upon established technologies, practices, constraints, conventions, or expectations.

- [ ] Development Standards can be resolved according to activity applicability rather than universally injected into Prompt Generation.

- [ ] Absence of downstream implementation information is not treated as a Project Prompt Readiness failure before the governing lifecycle requires that information to have been established.

- [ ] Legitimately unresolved project or implementation decisions can remain unresolved until an applicable governed activity establishes them.

### Review Notes

_Record observations, unresolved matters, or project-specific considerations here._

---

## 8. Provenance, Failure, Uncertainty, and Validation Support

- [ ] Material Generation Basis provenance can be preserved sufficiently to identify the basis from which generated execution instructions were derived.

- [ ] Required context can be distinguished from applicable, unresolved, not-applicable, and missing-required context.

- [ ] Missing required context can be surfaced rather than inferred, fabricated, or silently omitted.

- [ ] Material uncertainty can be preserved without being converted into apparent certainty through generated instructions.

- [ ] Prompt Governance or Prompt Generation failures can be distinguished from Product, Collaboration, Engineering, or Release failures.

- [ ] Material source conflicts can be represented without arbitrary resolution where existing governance does not establish the resolution.

- [ ] Generated prompts can be evaluated for applicable Resolution Validity, Structural Validity, Semantic Conformance, and Basis Validity.

- [ ] Persisted or reused prompts can be reassessed against their Generation Basis where material governing context changes.

### Review Notes

_Record observations, unresolved matters, or project-specific considerations here._

---

## 9. Activity-Specific Readiness Boundary

Project Prompt Readiness SHALL NOT be interpreted as establishing readiness for an individual Prompt Generation activity.

For each governed Prompt Generation activity, Engineering Automation SHALL still resolve the applicable:

- participant;
- capacity;
- scope;
- authority;
- Engineering System or governed cross-system interaction;
- governed activity;
- lifecycle context;
- authoritative context;
- project or subsystem specialization;
- Development Standards;
- unresolved matters;
- Generation Basis; and
- execution-relevant constraints.

The resulting context SHALL be evaluated according to the activity-scoped applicability semantics established by the Prompt Governance Specification.

Information that is not applicable to the current activity SHOULD NOT be required merely because it exists elsewhere in the project.

Information that is legitimately unresolved SHALL NOT be treated as missing required context unless the governing activity requires that information to have been established at the current lifecycle point.

---

## 10. Non-Requirements

Project Prompt Readiness does not universally require any particular Product, Collaboration, Engineering, or Release artifact to exist.

In particular, this checklist does not universally require:

- Product Vision;
- Product Decision Records;
- Product Roadmap;
- Milestone Plans;
- Release Plans;
- Draft Epics;
- Engineering-ready Epics;
- Engineering Delivery Proposals;
- Engineering Delivery Plans;
- Engineering Slices;
- Architecture Decision Records;
- source code;
- a programming language selection;
- a database selection;
- a framework selection;
- particular Development Standards;
- Release Candidates;
- Release Evidence;
- Release Readiness;
- Release Authorization;
- deployment configuration; or
- any other downstream artifact, decision, technology, or lifecycle state merely because it may become relevant later.

Any such information MAY become required for a particular governed activity where the applicable lifecycle and governing semantics require it to have been established.

That requirement is determined through activity-specific resolution and context applicability, not through Project Prompt Readiness.

---

## 11. Readiness Assessment

A project may be considered **Project Prompt Ready** where the applicable checklist items are satisfied and no unresolved checklist condition prevents Engineering Automation from reliably performing the common resolution, projection, provenance, failure-preservation, and validation functions required by Prompt Governance.

Project Prompt Ready means only that the project provides sufficient common prerequisites for governed Prompt Generation to operate.

It SHALL NOT be interpreted as meaning that:

- every governed activity is ready to execute;
- every required project artifact exists;
- every participant possesses authority;
- every future prompt can be generated;
- a particular generated prompt is conforming;
- a generated prompt remains current;
- Engineering realization is ready;
- Release governance is ready; or
- any Product, Collaboration, Engineering, or Release determination has been established.

Where Project Prompt Readiness cannot be established, the assessment SHOULD identify the unresolved project-level prerequisite rather than substituting activity-specific or downstream lifecycle requirements.

---

## 12. Checklist Governance

This checklist is a reusable Engineering Automation review aid subordinate to the Prompt Governance Specification.

It does not establish independent Engineering Platform semantics, project lifecycle states, participant authority, or Prompt Governance requirements.

Where this checklist and the Prompt Governance Specification appear to conflict, the Prompt Governance Specification governs.

Projects SHOULD apply the canonical checklist rather than maintain project-local copies that may diverge from Prompt Governance.

Project-specific observations or assessment results MAY be retained where useful, but such retained results SHALL NOT be treated as permanently valid where material project or governing conditions have changed.

Checklist completion does not eliminate generation-time Prompt Validation.
