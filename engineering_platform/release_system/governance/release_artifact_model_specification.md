# Release Artifact Model Specification

## 1. Purpose

The Release Artifact Model defines the canonical semantic objects, decisions, evidence, identities, conditions, contexts, outcomes, states, and records governed by the Release System.

The model establishes the semantic structure required to govern the progression of concluded Engineering outcomes toward applicable Release exposures and released Product states.

The Release Artifact Model SHALL preserve the authority and semantic ownership of originating systems while establishing Release-owned semantics required for Release governance.

The model is representation-neutral. A canonical Release semantic object does not imply a mandatory standalone document, file, schema, database entity, or user-interface representation.

---

## 2. Scope

This specification governs the semantic model for:

- Release;
- Release Identity;
- Release Codename;
- Product Version references where applicable;
- Release Candidate;
- Release Candidate Identity;
- Release Fingerprint;
- Release Admission determination;
- Release Readiness Decision;
- Release Authorization Decision;
- Release Evidence;
- Candidate Integrity;
- Release Exposure Context;
- Release Outcome;
- Released State;
- Release Conclusion; and
- Release Record.

This specification also classifies Release Candidate Formation, Release Validation, Release Promotion, and Release Recovery as governed Release processes associated with these semantic objects.

This specification does not define:

- Product intent;
- Product Capability semantics;
- Engineering readiness;
- Engineering realization;
- Engineering Conclusion;
- Engineering Evidence;
- Engineering Delivery Record semantics;
- Capability Acceptance semantics;
- organizational roles;
- deployment technologies;
- environment topology;
- CI/CD implementation;
- fingerprint algorithms;
- artifact packaging formats; or
- project-specific Release policies.

Those semantics remain governed by their applicable authoritative systems or downstream implementation and project governance.

---

## 3. Release System Semantic Boundary

The Release System consumes authoritative inputs from Product, Collaboration, Engineering, and other applicable governance domains without acquiring ownership of their underlying semantics.

Engineering establishes what has been realized.

The Release System governs whether, how, and under what conditions concluded Engineering outcomes progress through Release consideration, candidate formation, validation, readiness, authorization, exposure, promotion, recovery, and released Product states.

Release governance SHALL NOT redefine Product truth, Engineering truth, or authoritative collaborative outcomes.

The ability to reference, compose, evaluate, validate, transform, deploy, or record an upstream authoritative object SHALL NOT grant Release authority over that object's originating semantics.

---

## 4. Canonical Semantic Classification

The Release Artifact Model classifies canonical Release semantics as follows.

### 4.1 Governed Entity

- Release

### 4.2 Governed Realization Object

- Release Candidate

### 4.3 Identity and Reference Semantics

- Release Identity
- Release Codename
- Product Version reference
- Release Candidate Identity
- Release Fingerprint

### 4.4 Governed Decisions

- Release Readiness Decision
- Release Authorization Decision

Release Admission is a governed cross-system determination established through the Engineering–Release Collaboration domain and consumed by the Release System. Its representation in this model does not make it a Release System-owned decision.

### 4.5 Governed Evidence

- Release Evidence

### 4.6 Governed Conditions and Context

- Candidate Integrity
- Release Exposure Context

### 4.7 Governed Processes

- Release Candidate Formation
- Release Validation
- Release Promotion
- Release Recovery

### 4.8 Governed Outcome, State, and Conclusion

- Release Outcome
- Released State
- Release Conclusion

### 4.9 Authoritative Record

- Release Record

These classifications establish semantic responsibility. They SHALL NOT be interpreted as requiring one physical artifact for each canonical concept.

---

## 5. Release

A **Release** is the governed Release System entity representing a defined progression of realized Engineering outcomes toward one or more intended Release exposures or released Product states.

A Release provides the governing identity and continuity within which applicable Release decisions, candidates, evidence, progression, outcomes, and conclusion are established and preserved.

A Release SHALL have:

- determinable Release Identity;
- determinable governing purpose or basis;
- determinable position within applicable Release governance and lifecycle;
- traceable relationships to applicable authoritative upstream inputs;
- traceable Release Candidate history where candidates exist; and
- an associated Release Record.

A Release MAY:

- contain one or more concluded Engineering outcomes;
- progress through multiple Release Candidates;
- progress through one or more Release Exposure Contexts;
- reference applicable Product release intent;
- reference an applicable Product Version;
- have a Release Codename;
- undergo Release Recovery;
- return identified Engineering needs to Engineering governance; and
- conclude without establishing a Released State.

A Release SHALL remain semantically distinct from a Product Release Plan.

A Product Release Plan may provide authoritative Product context for a Release but SHALL NOT itself establish Release Admission, Release Candidate composition, Release Readiness, Release Authorization, Release Promotion, Released State, or Release Conclusion.

---

## 6. Release Identity

**Release Identity** is the canonical governed identity of a Release.

Every Release SHALL have a determinable Release Identity.

Release Identity SHALL remain sufficiently stable to support authoritative Release traceability throughout the Release lifecycle and after Release Conclusion.

The physical representation, naming convention, or generation mechanism for Release Identity is implementation-specific unless constrained by applicable project governance.

Release Identity SHALL remain semantically distinct from:

- Release Codename;
- Product Version;
- Release Candidate Identity; and
- Release Fingerprint.

---

## 7. Release Codename

A **Release Codename** is an optional human-friendly alias associated with a Release for internal communication.

A Release MAY have a Release Codename.

A Release Codename:

- MAY be used in human conversation, dashboards, reports, or other non-authoritative communication;
- SHALL resolve to the applicable Release where used in governed Release context;
- SHALL NOT substitute for Release Identity where authoritative identification is required; and
- SHALL NOT substitute for Release Fingerprint where exact realization identity is required.

Release Codename is an alias and does not independently establish Release identity or authority.

---

## 8. Product Version Reference

A Release MAY reference an applicable **Product Version** or equivalent Product-owned release identifier where such identity is established by applicable Product governance.

A Product Version reference SHALL preserve the authority and semantics of its originating governance.

The Release System SHALL NOT infer Product authority merely because a version identifier is technically required for packaging, deployment, distribution, or presentation.

Product Version SHALL remain semantically distinct from Release Identity, Release Candidate Identity, and Release Fingerprint.

---

## 9. Release Candidate

A **Release Candidate** is an identified, integrity-controlled composition of realized Engineering outcomes and applicable Release material evaluated for a defined Release progression.

A Release Candidate SHALL:

- belong to a determinable Release;
- have determinable Release Candidate Identity;
- have determinable composition;
- have a determinable Release Fingerprint;
- have determinable intended Release progression or evaluation context;
- preserve traceability to applicable admitted Engineering outcomes and Release material; and
- satisfy applicable Candidate Integrity requirements.

A Release MAY have multiple Release Candidates.

A Release Candidate MAY participate in multiple Release progression or exposure contexts where applicable governance permits.

Formation of a Release Candidate SHALL NOT redefine the authoritative semantics of included Engineering outcomes or other authoritative inputs.

A Release Candidate is a governed semantic realization object. It SHALL NOT be equated with any specific physical representation such as a source branch, binary, container image, package, deployment manifest, repository tag, or build record.

Such representations MAY realize or identify all or part of a Release Candidate.

---

## 10. Release Candidate Identity

**Release Candidate Identity** is the governed identity distinguishing a Release Candidate within applicable Release governance.

Every Release Candidate SHALL have determinable Release Candidate Identity.

Release Candidate Identity SHALL remain distinguishable from:

- Release Identity;
- Product Version; and
- Release Fingerprint.

Release Candidate Identity answers which governed candidate is under consideration.

Release Fingerprint answers which exact governed realization or composition that candidate represents.

Replacement of a Release Candidate SHALL preserve the identity and history of the superseded or replaced candidate.

---

## 11. Release Fingerprint

A **Release Fingerprint** is an immutable, deterministically resolvable identity associated with an identified Release Candidate or released realization, enabling the exact governed Release realization and its composition to be distinguished and traced.

Every Release Candidate SHALL have a determinable Release Fingerprint sufficient to distinguish its governed realization and composition.

A released realization SHALL have a determinable Release Fingerprint.

Release Fingerprint MAY be realized using one or more implementation mechanisms including cryptographic digests, signed manifests, artifact identities, build provenance, component digests, source identities, or other mechanisms capable of satisfying the required semantic contract.

This specification does not prescribe a fingerprint algorithm or representation.

Release Fingerprint SHALL remain semantically distinct from:

- Product Version;
- Release Identity; and
- Release Candidate Identity.

Release Evidence, Release Readiness Decisions, Release Authorization Decisions, Release Promotion, Release Outcomes, and applicable downstream provenance SHALL remain traceable to the relevant Release Fingerprint.

A material change to a Release Candidate's governed realization or composition SHALL result in a distinguishable Release Fingerprint.

Such material change SHALL trigger reassessment of affected Release Evidence, Release Readiness, Release Authorization, and other Release decisions whose validity depends upon the prior realization.

Where Release progression materially transforms a realization, the resulting realization SHALL have a distinguishable Release Fingerprint and SHALL preserve traceable provenance to its governing predecessor.

A shared Product Version SHALL NOT be interpreted as proof of identical Release Fingerprint.

---

## 12. Candidate Integrity

**Candidate Integrity** is the governed condition that an identified Release Candidate remains sufficiently stable and distinguishable for applicable Release Evidence and decisions to remain valid for that candidate.

Candidate Integrity SHALL preserve the relationship between:

- Release Candidate Identity;
- Release Fingerprint;
- candidate composition;
- Release Evidence;
- Release Readiness;
- Release Authorization; and
- Release Outcome.

Candidate Integrity SHALL NOT require a universal code-freeze mechanism.

Projects MAY realize Candidate Integrity through immutable artifacts, digests, signatures, controlled builds, governed candidate replacement, code freeze, or other applicable mechanisms.

A material candidate change SHALL NOT silently retain prior Release Candidate Identity, Release Fingerprint, evidence, readiness, or authorization where the change affects their validity.

---

## 13. Release Admission Determination

A **Release Admission determination** is the governed cross-system determination that one or more concluded Engineering outcomes are eligible to enter Release governance for a defined Release purpose.

Release Admission is an Engineering–Release collaborative interaction established through the Collaboration System's Engineering–Release collaboration domain.

The Release System consumes the resulting Release Admission determination as authoritative Release lifecycle input but SHALL NOT establish, redefine, broaden, narrow, or substitute that determination.

A Release Admission determination SHALL preserve:

- the applicable Release;
- identified Engineering outcome or outcomes;
- applicable Engineering Conclusion;
- applicable Finalized Engineering Delivery Record or Records;
- applicable conditions or limitations;
- governing Release purpose;
- determination;
- authority or participating authorities;
- rationale or basis; and
- provenance.

Release Admission SHALL NOT itself establish:

- Engineering Completion;
- Capability Acceptance;
- Release Candidate;
- Release Readiness;
- Release Authorization; or
- Released State.

The authoritative establishment contract for Release Admission is governed by the applicable Engineering–Release Collaboration semantics.

---

## 14. Release Evidence

**Release Evidence** is governed evidence produced, collected, referenced, or preserved to support Release determinations, progression, validation, authorization, promotion, recovery, or outcome establishment.

Release Evidence MAY include evidence concerning:

- Candidate Integrity;
- packaging;
- deployment;
- compatibility;
- security;
- operational readiness;
- environment readiness;
- Release validation;
- exposure;
- promotion;
- recovery;
- downstream observation; or
- other applicable Release conditions.

Release Evidence SHALL have determinable provenance.

Where Release governance consumes Engineering Evidence or other externally owned evidence, the originating authority and semantics SHALL be preserved.

Referencing upstream evidence as part of Release governance SHALL NOT convert that evidence into Release-owned truth.

Release Evidence SHALL remain traceable to the applicable Release Candidate, Release Fingerprint, progression context, or Release outcome where relevant.

---

## 15. Release Readiness Decision

A **Release Readiness Decision** is the governed determination of whether an identified Release Candidate satisfies applicable conditions for a defined Release progression.

A Release Readiness Decision SHALL identify or resolve:

- the applicable Release;
- Release Candidate;
- Release Fingerprint;
- intended progression or exposure context;
- applicable readiness conditions;
- applicable evidence;
- exceptions or deviations where relevant;
- determination;
- governing authority or authorities;
- basis; and
- provenance.

Release Readiness is contextual.

A Release Candidate MAY be ready for one Release progression or exposure context while not being ready for another.

Release Readiness SHALL NOT be represented semantically as a universal candidate-wide Boolean where multiple progression contexts are possible.

Release Readiness SHALL NOT itself establish Release Authorization.

Successful Release Validation SHALL NOT by itself establish Release Readiness.

---

## 16. Release Authorization Decision

A **Release Authorization Decision** is the governed decision permitting an identified Release Candidate to undergo a defined Release progression or exposure action.

A Release Authorization Decision SHALL identify or resolve:

- the applicable Release;
- Release Candidate;
- Release Fingerprint;
- authorized progression or exposure action;
- applicable Release Readiness basis;
- applicable conditions;
- required participating authorities;
- authorization determination;
- basis;
- validity or constraints where applicable; and
- provenance.

Release Authorization semantics are governed by the Release System.

The authority required to establish a particular Release Authorization SHALL be resolved from applicable governance and MAY involve multiple authority domains.

Release Readiness SHALL NOT itself establish Release Authorization.

Technical permission, deployment capability, administrative access, or automation capability SHALL NOT itself constitute Release Authorization.

---

## 17. Release Exposure Context

A **Release Exposure Context** identifies the governed context in which a Release Candidate is intended to be evaluated, exposed, promoted, or used.

Exposure contexts are project-specific.

Examples MAY include internal exposure, developer preview, private beta, public beta, Production, or other project-defined contexts.

These examples are non-normative and SHALL NOT be interpreted as a required or universal Release progression sequence.

Release Exposure Context SHALL remain distinct from Release lifecycle state.

Public accessibility SHALL NOT itself establish Released State for a Production or other final Release Exposure Context.

A Release progression involving exposure SHALL identify the applicable exposure context sufficiently for Release Evidence, Release Readiness, Release Authorization, and Release Outcome to be interpreted correctly.

---

## 18. Release Candidate Formation

**Release Candidate Formation** is the governed Release process by which admitted Engineering outcomes and applicable Release material are composed into an identified Release Candidate.

Candidate Formation SHALL establish or resolve:

- Release Candidate Identity;
- candidate composition;
- Release Fingerprint;
- applicable provenance;
- intended progression or evaluation context; and
- applicable Candidate Integrity basis.

Candidate Formation SHALL preserve the semantic ownership of its constituent authoritative inputs.

Composition of an Engineering outcome into a Release Candidate SHALL NOT redefine the Engineering outcome.

---

## 19. Release Validation

**Release Validation** is the governed Release process of evaluating an identified Release Candidate against applicable Release conditions and producing, collecting, or resolving Release Evidence.

Release Validation MAY be performed or assisted by humans, automation, AI, testing systems, security systems, operational systems, or other applicable mechanisms.

Performance of Release Validation SHALL NOT itself grant authority to establish Release Readiness.

Validation results SHALL remain traceable to the applicable Release Candidate and Release Fingerprint where candidate-specific validity is required.

---

## 20. Release Promotion

**Release Promotion** is the governed Release process of progressing an identified and authorized Release Candidate through a defined Release progression or exposure action.

Release Promotion SHALL require applicable Release Authorization.

Release Promotion SHALL preserve traceability to:

- Release Identity;
- Release Candidate Identity;
- Release Fingerprint;
- applicable Release Readiness;
- applicable Release Authorization;
- progression or exposure context;
- execution evidence; and
- resulting Release Outcome.

Technical execution of Release Promotion SHALL NOT manufacture missing Release Authorization.

Successful technical deployment SHALL NOT by itself establish Released State.

---

## 21. Release Recovery

**Release Recovery** is the governed Release process for responding to an unsuccessful, degraded, unsafe, or otherwise unacceptable Release progression or outcome.

Release Recovery MAY include:

- rollback;
- roll-forward;
- traffic restoration;
- candidate replacement;
- feature disablement;
- environment recovery;
- progression termination; or
- other applicable recovery mechanisms.

Release Recovery SHALL preserve the Release context, evidence, decisions, actions, and outcomes associated with the recovery.

Where Release Recovery requires additional Engineering realization, that realization SHALL return to applicable Engineering governance.

Release Recovery SHALL NOT silently become Engineering realization.

---

## 22. Release Outcome

A **Release Outcome** is the governed result of an attempted or completed Release progression.

A Release Outcome SHALL be determinable for applicable governed Release progression.

Release Outcome SHALL preserve or resolve:

- applicable Release;
- Release Candidate;
- Release Fingerprint;
- progression or exposure context;
- authorization basis;
- execution evidence;
- resulting state;
- recovery where applicable; and
- provenance.

Successful execution of a technical action SHALL NOT by itself establish a successful governed Release Outcome.

Projects MAY define applicable Release Outcome classifications.

This specification does not prescribe a universal Release Outcome enumeration.

---

## 23. Released State

**Released State** is a governed Release state established when an applicable authorized Release progression has successfully achieved the intended released Product context and the required Release outcome has been established.

Released State SHALL NOT be established solely by:

- Engineering Completion;
- Release Admission;
- Candidate Formation;
- Release Readiness;
- Release Authorization;
- technical deployment success; or
- public accessibility.

A Release MAY establish multiple applicable progression outcomes without establishing Released State.

Released State SHALL remain traceable to the applicable Release Candidate and Release Fingerprint.

---

## 24. Release Conclusion

**Release Conclusion** is the governed determination establishing the terminal Release outcome and its basis.

A Release MAY conclude:

- after successfully achieving its intended Release progression;
- without establishing Released State;
- after cancellation;
- after supersession;
- after inability to proceed;
- following unsuccessful progression or recovery; or
- under another governed terminal condition.

These examples are non-normative and do not prescribe a universal Release Conclusion status model.

Release Conclusion SHALL preserve:

- the applicable Release;
- terminal outcome;
- governing basis;
- applicable Release Candidate and fingerprint relationships;
- significant Release Outcomes;
- unresolved conditions where applicable;
- recovery state where applicable;
- authority;
- rationale; and
- provenance.

Release Conclusion SHALL be established before the Release Record is finalized.

---

## 25. Release Record

The **Release Record** is the authoritative governed record preserving the progression, basis, decisions, evidence, provenance, and outcome of a Release.

Every Release SHALL have an associated Release Record.

The Release Record SHALL be progressive.

It MAY be initialized when the Release is established and progressively preserve:

- Release Identity;
- Release Codename where applicable;
- Product Version references where applicable;
- governing Release purpose and basis;
- Release Admission determinations;
- admitted Engineering outcomes;
- Release Candidate identities;
- candidate compositions;
- Release Fingerprints;
- Candidate Integrity basis;
- Release Evidence;
- Release Readiness Decisions;
- Release Authorization Decisions;
- Release Exposure Contexts;
- Release Promotion;
- Release Outcomes;
- exceptions and deviations;
- Release Recovery;
- Release Conclusion; and
- applicable provenance.

The Release Record preserves governed Release truth.

The act of writing, appending, generating, or modifying information in the Release Record SHALL NOT itself grant authority to establish the governed decision, state, or outcome represented by that information.

Release Record finalization SHALL preserve an already established Release Conclusion.

Finalization SHALL NOT itself manufacture Release Conclusion.

---

## 26. Candidate Replacement and Evidence Continuity

A Release MAY replace or supersede a Release Candidate during its lifecycle.

Candidate replacement SHALL:

- preserve the identity and history of the prior candidate;
- establish or resolve the replacement Candidate Identity;
- establish the replacement Release Fingerprint;
- preserve provenance between applicable candidates;
- reassess the continued applicability of prior Release Evidence;
- reassess affected Release Readiness Decisions;
- reassess affected Release Authorization Decisions; and
- preserve superseded decisions and evidence where required for continuity and provenance.

Prior evidence MAY remain applicable where its continued validity is explicitly established.

Prior evidence SHALL NOT be silently inherited by a materially different candidate.

---

## 27. Cross-System Traceability

The Release Artifact Model SHALL support traceability across applicable authoritative systems.

Where applicable, Release governance SHALL be capable of tracing:

Release purpose and Product intent  
→ admitted Engineering outcomes  
→ Engineering Conclusions and Finalized Engineering Delivery Records  
→ Release Admission  
→ Release Candidate  
→ Release Fingerprint  
→ Release Evidence  
→ Release Readiness  
→ Release Authorization  
→ Release Promotion  
→ Release Outcome  
→ Released State where applicable  
→ Release Conclusion  
→ Finalized Release Record.

Cross-system traceability SHALL preserve originating semantic ownership.

Traceability SHALL NOT imply authority transfer.

---

## 28. Downstream Provenance

A released realization SHALL expose or otherwise preserve sufficient Release identity and fingerprint provenance for downstream observations, incidents, defects, operational evidence, or other governed findings to be resolvable to the applicable released realization.

The mechanism by which Release Identity or Release Fingerprint is exposed, embedded, recorded, surfaced, or resolved downstream is implementation-specific.

Downstream observability or operational systems MAY surface Release identity and fingerprint information but SHALL NOT thereby become authoritative owners of Release semantics.

---

## 29. Exceptions and Deviations

Release artifacts and decisions MAY be subject to governed exceptions or deviations where permitted by applicable Release governance.

Exceptions and deviations SHALL be explicit and traceable.

A Release exception SHALL NOT silently redefine:

- Product authority;
- Engineering authority;
- Release authority;
- Candidate Identity;
- Release Fingerprint; or
- other authoritative cross-system semantics.

Emergency or expedited Release progression SHALL remain subject to applicable Release identity, candidate identity, fingerprint, authority, provenance, and outcome requirements.

---

## 30. Human, AI, and Automation Participation

Humans, AI systems, and automation MAY assist in creating, composing, evaluating, validating, maintaining, or presenting Release semantic objects and records.

AI and automation MAY assist with:

- Release context composition;
- candidate formation;
- fingerprint generation or resolution;
- validation;
- evidence collection;
- readiness evaluation;
- authorization preparation;
- promotion execution;
- recovery;
- Release Record maintenance; and
- provenance resolution.

Authorship, execution, evaluation, generation, technical access, or automation capability SHALL NOT itself grant Release authority.

Applicable governed decisions, states, and conclusions SHALL be established only under applicable authority.

---

## 31. Representation Neutrality

The Release Artifact Model does not prescribe physical representation.

Release semantics MAY be represented using:

- Markdown;
- YAML;
- JSON;
- databases;
- manifests;
- signed metadata;
- CI/CD records;
- deployment systems;
- release management systems;
- generated views;
- user interfaces; or
- combinations of these mechanisms.

Where multiple representations exist, their authoritative relationship SHALL be determinable.

Physical storage location SHALL NOT by itself establish semantic authority.

---

## 32. Conformance Requirements

A conforming Release System realization SHALL:

1. maintain determinable Release Identity for every governed Release;
2. preserve Release as semantically distinct from Product Release Plan;
3. preserve Release Identity, Product Version, Release Candidate Identity, Release Codename, and Release Fingerprint as distinct semantics where applicable;
4. treat Release Codename as optional and non-authoritative;
5. maintain determinable Release Candidate Identity and composition for every Release Candidate;
6. maintain a determinable Release Fingerprint for every Release Candidate;
7. maintain a determinable Release Fingerprint for every released realization;
8. preserve provenance between materially transformed Release realizations;
9. reassess affected evidence and decisions following material candidate change;
10. preserve Candidate Integrity sufficient for applicable evidence and decisions to remain candidate-specific;
11. preserve the cross-system nature of Release Admission;
12. prevent Release Admission from redefining Engineering Conclusion;
13. preserve Release Evidence provenance and originating authority;
14. establish Release Readiness only for a defined candidate and progression context;
15. preserve Release Readiness as distinct from Release Authorization;
16. require applicable authority for Release Authorization;
17. prevent technical permission or execution capability from constituting Release Authorization;
18. require applicable Release Authorization before governed Release Promotion;
19. preserve promotion and outcome traceability to applicable Candidate Identity and Release Fingerprint;
20. prevent successful technical deployment from automatically establishing Released State;
21. preserve Release Exposure Context as distinct from Release lifecycle state;
22. support governed Release Recovery without silently converting Release activity into Engineering realization;
23. return additional Engineering realization to applicable Engineering governance;
24. establish explicit Release Outcome for applicable governed progression;
25. establish Released State only through applicable governed Release semantics;
26. permit Release Conclusion without requiring Released State;
27. establish Release Conclusion before Release Record finalization;
28. maintain an authoritative progressive Release Record for every Release;
29. prevent Release Record mutation or finalization from manufacturing authority;
30. preserve superseded candidates, evidence, and decisions as required for continuity and provenance;
31. support cross-system traceability without transferring semantic ownership;
32. preserve downstream resolvability from released realization to applicable Release identity and fingerprint;
33. keep exceptions, deviations, and emergency progression explicit and traceable;
34. preserve human accountability and applicable authority when AI or automation participates; and
35. remain representation-neutral unless constrained by applicable downstream governance.

A realization that cannot satisfy these requirements is not conformant with the Release Artifact Model.
