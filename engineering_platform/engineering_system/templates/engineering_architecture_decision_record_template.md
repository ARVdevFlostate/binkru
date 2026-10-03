# Engineering Architecture Decision Record Template

## 1. Template Purpose

Use this template to preserve one coherent material Architecture
Decision as an Architecture Decision Record (ADR).

An ADR is a governed Engineering record. It preserves the architecture
proposition, decision basis, applicable review history, Architecture
Decision, and subsequent disposition.

Creating or completing this template does not by itself establish
authoritative architecture.

Canonical ADR states are:

-   Draft
-   Ready for Review
-   Deferred
-   Accepted
-   Rejected
-   Superseded

Canonical Architecture Decision outcomes are:

-   Approve
-   Return
-   Defer
-   Reject

`Approve`, `Return`, `Defer`, and `Reject` are decision outcomes, not
ADR states.

An Accepted ADR is authoritative for its governed architecture scope.
Acceptance of an ADR does not by itself authorize Engineering execution
or revise a governed baseline.

## 2. Record Identity

  -------------------------------------------------------------------------------------------------
  Field                  Value
  ---------------------- --------------------------------------------------------------------------
  ADR ID                 `<stable ADR identity>`

  Title                  `<concise descriptive title>`

  ADR State              `Draft / Ready for Review / Deferred / Accepted / Rejected / Superseded`

  Revision               `<revision identifier>`

  Created                `<date/time or governed reference>`

  Last Updated           `<date/time or governed reference>`

  Architecture Scope     `<bounded architecture scope>`

  Originating Context    `<Proposal / Planning / Orchestration / Reassessment / other>`
  -------------------------------------------------------------------------------------------------

The ADR ID SHALL remain stable across drafting, review, Return,
Deferral, Acceptance, Rejection, and subsequent Supersession.

Revision identifies the representation revision of the same ADR and
SHALL NOT be used to establish a materially different Architecture
Decision under the same ADR identity.

After Acceptance, Revision MAY change only through permitted governed
non-substantive correction or enrichment.

A material change to an Accepted Architecture Decision requires a new
ADR identity and applicable Architecture Decision.

## 3. Architecture Concern

### 3.1 Decision Context

Describe the architecture concern requiring a governed decision.

Include enough context for a future engineer or agent to understand the
decision without relying on the memory of the original participants.

`<context>`

### 3.2 Why This Decision Is Material

Describe the material Engineering consequence that warrants an ADR.

Consider, where applicable:

-   architecture basis;
-   system boundaries;
-   component or service responsibilities;
-   data ownership or persistence;
-   integration or interoperability;
-   public or materially shared interfaces;
-   security or privacy;
-   reliability, availability, resilience, or recoverability;
-   performance or scalability;
-   deployment or operational architecture;
-   technology, platform, supplier, or licensing dependency;
-   future Engineering constraints;
-   reversibility or migration cost;
-   cross-Slice or cross-Epic consequence;
-   Approved Investment Baseline; or
-   Execution Baseline.

`<materiality basis>`

### 3.3 Architecture Scope

Define precisely where the decision applies.

`<scope>`

### 3.4 Applicable Governed Basis

Reference the governed Engineering basis relevant to this decision.

  -----------------------------------------------------------------------
  Governed Object /     Reference                 Relationship
  Basis                                           
  --------------------- ------------------------- -----------------------
  Engineering Delivery  `<reference or N/A>`      `<relationship>`
  Proposal                                        

  Approved Investment   `<reference or N/A>`      `<relationship>`
  Baseline                                        

  Engineering Delivery  `<reference or N/A>`      `<relationship>`
  Plan                                            

  Execution Baseline    `<reference or N/A>`      `<relationship>`

  Engineering Slice(s)  `<reference(s) or N/A>`   `<relationship>`

  Prior / Related       `<reference(s) or N/A>`   `<relationship>`
  ADR(s)                                          

  Other governed object `<reference or N/A>`      `<relationship>`
  -----------------------------------------------------------------------

## 4. Constraints, Assumptions, and Dependencies

### 4.1 Material Constraints

-   `<constraint>`
-   `<constraint>`

### 4.2 Material Assumptions

-   `<assumption>`
-   `<assumption>`

Distinguish assumptions from established facts where material.

### 4.3 Material Dependencies

-   `<dependency>`
-   `<dependency>`

## 5. Architecture Proposition

State the architecture proposition being submitted for decision.

This section describes what is proposed. It is not authoritative until
an Architecture Decision outcome of `Approve` is established by the
applicable authority.

`<architecture proposition>`

## 6. Alternatives Considered

Record the viable alternatives seriously considered.

### Option A --- `<name>`

**Description**

`<description>`

**Advantages**

-   `<advantage>`

**Disadvantages / Risks**

-   `<disadvantage or risk>`

**Material Consequences**

`<consequences>`

**Reversibility / Migration Considerations**

`<considerations>`

------------------------------------------------------------------------

### Option B --- `<name>`

**Description**

`<description>`

**Advantages**

-   `<advantage>`

**Disadvantages / Risks**

-   `<disadvantage or risk>`

**Material Consequences**

`<consequences>`

**Reversibility / Migration Considerations**

`<considerations>`

------------------------------------------------------------------------

Add or remove alternatives proportionate to the decision.

Where constraints genuinely leave only one viable option, explain why
alternatives are not viable rather than manufacturing artificial
choices.

## 7. Engineering Evidence

Reference Engineering Evidence supporting material claims or trade-off
analysis.

  --------------------------------------------------------------------------------------------------------
  Evidence                                                                 Authoritative   Claim /
                                                                           Reference       Decision
                                                                                           Relevance
  ------------------------------------------------------------------------ --------------- ---------------
  `<benchmark / prototype / experiment / validation / analysis / other>`   `<reference>`   `<relevance>`

  `<evidence>`                                                             `<reference>`   `<relevance>`
  --------------------------------------------------------------------------------------------------------

Evidence supports the Architecture Decision. Evidence does not make the
decision.

## 8. Analysis and Trade-offs

Summarize the material reasoning across the proposition and
alternatives.

Address the dimensions that materially affect this decision, such as:

-   structural consequence;
-   quality attributes;
-   security or privacy;
-   operational consequence;
-   implementation complexity;
-   cost or supplier consequence;
-   capability requirements;
-   dependency consequence;
-   reversibility;
-   migration;
-   future Engineering constraint;
-   validation consequence; and
-   residual uncertainty.

`<analysis>`

## 9. Recommendation

### Recommended Option

`<recommended option>`

### Recommendation Rationale

`<why this option is recommended>`

### Material Risks / Uncertainty

-   `<risk or uncertainty>`
-   `<risk or uncertainty>`

A recommendation is not an Architecture Decision and does not establish
architecture authority.

## 10. Affected Engineering Realization

Identify the governed Engineering objects or realization expected to be
affected.

  ---------------------------------------------------------------------------------------------
  Affected Object                                             Reference       Expected
                                                                              Consequence
  ----------------------------------------------------------- --------------- -----------------
  `<Plan / Baseline / Slice / component / service / other>`   `<reference>`   `<consequence>`

  ---------------------------------------------------------------------------------------------

### Baseline Consequence Assessment

Does approval of this proposition materially change an existing governed
baseline?

`Yes / No / Not Yet Determinable`

If `Yes` or `Not Yet Determinable`, describe the required reassessment
or governance path.

`<reassessment / escalation / governance requirement>`

## 11. Architecture Decision Authority

### Primary Architecture Decision Authority

  Field             Value
  ----------------- -----------------------------------------------
  Authority         `<actor / role / governed mechanism>`
  Authority Scope   `<scope>`
  Authority Basis   `<delegation / governance reference / other>`

### Required Concurrence

Use this section where the material consequences cross governed
authority domains.

  ---------------------------------------------------------------------------------------------------------------------------------
  Authority Domain                                         Required        Concurrence Status                       Reference /
                                                           Authority                                                Date
  -------------------------------------------------------- --------------- ---------------------------------------- ---------------
  `<security / privacy / operations / platform / other>`   `<authority>`   `Pending / Concurred / Not Applicable`   `<reference>`

  ---------------------------------------------------------------------------------------------------------------------------------

Missing required concurrence prevents the ADR from becoming Accepted.

## 12. Ready for Review Assessment

Before setting ADR State to `Ready for Review`, confirm that the record
is sufficiently developed for an Architecture Decision.

This assessment is an in-record preparation aid.

Where a canonical Engineering Architecture Decision Record Checklist
applies, that checklist governs formal readiness validation.

-   [ ] Architecture concern is clear.
-   [ ] Materiality basis is explicit.
-   [ ] Architecture scope is bounded.
-   [ ] Relevant governed basis is referenced.
-   [ ] Material constraints, assumptions, and dependencies are visible.
-   [ ] Architecture proposition is explicit.
-   [ ] Viable alternatives are sufficiently analysed.
-   [ ] Material trade-offs, risks, and consequences are visible.
-   [ ] Relevant Engineering Evidence is referenced.
-   [ ] Recommendation is explicit.
-   [ ] Affected governed bases or realization are identifiable.
-   [ ] Architecture Decision Authority is determinable.
-   [ ] Required concurrence is determinable.
-   [ ] Material unresolved matters are visible.

### Review Readiness

`Ready / Not Ready`

### Readiness Notes

`<notes>`

## 13. Architecture Decision

Complete this section when the ADR is subject to the governed
Architecture Decision.

  ---------------------------------------------------------------------------
  Field                          Value
  ------------------------------ --------------------------------------------
  Decision Outcome               `Approve / Return / Defer / Reject`

  Decision Authority             `<authority>`

  Decision Date / Effective      `<date/time or governed reference>`
  Point                          

  Resulting ADR State            `<Accepted / Draft / Deferred / Rejected>`

  Decision Reference             `<reference if maintained separately>`
  ---------------------------------------------------------------------------

### Decision Rationale

`<governed rationale>`

### Conditions

Record explicit architecture conditions established by the decision, if
any.

-   `<condition or None>`

### Required Follow-up

-   `<follow-up or None>`

### Concurrence Confirmation

`<required concurrence satisfied / not applicable / references>`

## 14. Outcome-specific Record

Complete the applicable subsection only.

### 14.1 Approve → Accepted

Record the accepted Architecture Decision in concise authoritative form.

`<accepted decision>`

#### Expected Material Consequences

-   `<benefit>`
-   `<cost / constraint / risk / technical debt / operational implication / other>`

#### Baseline / Reassessment Consequence

`<none / governed reassessment required / revised basis reference / escalation reference>`

Acceptance establishes authoritative architecture for the governed
scope. It does not independently establish execution authority.

### 14.2 Return → Draft

Record what requires further analysis, clarification, correction,
evidence, or revision.

`<return rationale and required reconsideration>`

The ADR retains the same stable identity.

### 14.3 Defer → Deferred

#### Deferral Rationale

`<why the decision is deferred>`

#### Reconsideration Trigger / Condition / Dependency / Timing

`<trigger or condition>`

#### Re-entry History

When the ADR later re-enters the decision flow, record:

  -------------------------------------------------------------------------------
  Re-entry       Date / Reference     Reason         Resulting State
  -------------- -------------------- -------------- ----------------------------
  `<entry>`      `<date/reference>`   `<reason>`     `Draft / Ready for Review`

  -------------------------------------------------------------------------------

A Deferred ADR may re-enter Draft when additional analysis, evidence, or
proposition revision is required.

A Deferred ADR may re-enter Ready for Review where the proposition
remains materially unchanged and the condition preventing the decision
has been resolved.

Preserve the prior Defer outcome and rationale as governed history.

### 14.4 Reject → Rejected

#### Rejection Rationale

`<why the proposition was rejected>`

Rejected is terminal for the architecture proposition represented by
this ADR.

A materially renewed proposition requires a new ADR identity and SHOULD
reference this ADR where historically relevant.

## 15. Accepted Decision Consequences

Complete for an Accepted ADR, proportionate to significance.

### Benefits

-   `<benefit>`

### Costs / Trade-offs

-   `<cost or trade-off>`

### Constraints Introduced

-   `<constraint>`

### Risks / Technical Debt

-   `<risk or debt>`

### Operational / Security / Quality Consequences

-   `<consequence>`

### Validation Obligations

-   `<validation obligation>`

### Migration / Transition Obligations

-   `<obligation>`

### Future Engineering Constraints

-   `<constraint>`

### Material Uncertainty Remaining

-   `<uncertainty or None>`

## 16. Supersession

Complete when this ADR supersedes another Accepted ADR or is itself
superseded.

### Supersedes

  ----------------------------------------------------------------------------
  ADR                         Scope Superseded           Effective Point
  --------------------------- -------------------------- ---------------------
  `<ADR reference or None>`   `<full / partial scope>`   `<effective point>`

  ----------------------------------------------------------------------------

### Superseded By

  ----------------------------------------------------------------------------
  ADR                         Scope Superseded           Effective Point
  --------------------------- -------------------------- ---------------------
  `<ADR reference or None>`   `<full / partial scope>`   `<effective point>`

  ----------------------------------------------------------------------------

Where supersession is partial, make the affected scope explicit enough
to determine which architecture basis remains authoritative.

Supersession does not imply that the prior decision was incorrect.

## 17. Related Engineering Records and Evidence

  ------------------------------------------------------------------------------
  Relationship        Reference           Notes
  ------------------- ------------------- --------------------------------------
  Related ADR(s)      `<reference(s)>`    `<relationship>`

  Engineering         `<reference(s)>`    `<material realization consequence>`
  Delivery Record(s)                      

  Engineering         `<reference(s)>`    `<relevance>`
  Evidence                                

  Reassessment        `<reference(s)>`    `<relationship>`
  Decision(s)                             

  Other governed      `<reference>`       `<relationship>`
  record                                  
  ------------------------------------------------------------------------------

The ADR owns the durable reasoning for the Architecture Decision.

The EDR owns the material history of what occurred during Engineering
realization.

## 18. Governed Correction History

Use this section only for controlled non-substantive correction or
enrichment after Acceptance.

The substantive Architecture Decision of an Accepted ADR is immutable.

  ------------------------------------------------------------------------------------
  Revision       Date        Correction / Enrichment      Reason       Authorized By
  -------------- ----------- ---------------------------- ------------ ---------------
  `<revision>`   `<date>`    `<non-substantive change>`   `<reason>`   `<authority>`

  ------------------------------------------------------------------------------------

Material change to the accepted decision, architecture scope, rationale,
or architectural consequence requires a new ADR and applicable
Architecture Decision.

## 19. Record History

Preserve material ADR lifecycle and governance events.

  -----------------------------------------------------------------------------------------------------------------------------------------------
  Date / Reference     ADR State            Event / Decision                                                          Authority /     Notes
                                                                                                                      Actor           
  -------------------- -------------------- ------------------------------------------------------------------------- --------------- -----------
  `<date/reference>`   `Draft`              `Created`                                                                 `<actor>`       `<notes>`

  `<date/reference>`   `Ready for Review`   `<event>`                                                                 `<actor>`       `<notes>`

  `<date/reference>`   `<state>`            `<Approve / Return / Defer / Reject / re-entry / supersession / other>`   `<authority>`   `<notes>`
  -----------------------------------------------------------------------------------------------------------------------------------------------

## 20. Final Record Check

Before relying on this ADR according to its state, confirm:

This final record check is a convenience check within the ADR.

It does not replace the canonical Engineering Architecture Decision
Record Checklist where that checklist applies.

-   [ ] ADR identity is stable.
-   [ ] ADR state is canonical.
-   [ ] Architecture Decision outcome is not confused with ADR state.
-   [ ] Architecture scope is explicit.
-   [ ] Materiality is justified.
-   [ ] Decision context is sufficient.
-   [ ] Alternatives and trade-offs are proportionate to significance.
-   [ ] Relevant Engineering Evidence is referenced.
-   [ ] Recommendation is distinguishable from the governed decision.
-   [ ] Architecture Decision Authority is explicit.
-   [ ] Required concurrence is satisfied for an Accepted ADR.
-   [ ] Decision outcome and rationale are preserved.
-   [ ] Accepted decision substance is not silently rewritten.
-   [ ] Baseline consequences use applicable reassessment/governance.
-   [ ] Deferred re-entry preserves prior Defer history.
-   [ ] Rejected ADRs are not reopened.
-   [ ] Supersession relationships are explicit where applicable.
-   [ ] Material realization consequences are referenced through the EDR
    where applicable.
-   [ ] Historical integrity is preserved.

## 21. Canonical Interpretation

This template SHALL be interpreted according to the Engineering
Architecture Decision Specification and applicable Engineering
Governance and Artifact Model specifications.

The governing distinction is:

    Architecture Decision
        = governed determination

    Architecture Decision Record
        = governed record preserving
          that determination and its basis

And:

    Accepted ADR
        = authoritative architecture
          for its governed scope

    Accepted ADR
        ≠ execution authorization

Where an Accepted Architecture Decision materially changes an existing
governed execution basis, the applicable Engineering reassessment and
authority model governs any resulting baseline change.
