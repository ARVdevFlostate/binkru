# Engineering Delivery Record Template

## 1. Record Identity

**Engineering Delivery Record ID:**\
\[Stable EDR identifier\]

**Record State:**\
\[Active \| Finalized\]

**Engineering Realization:**\
\[Identity or concise description of the governed Engineering
realization\]

**Record Instantiated:**\
\[Date/time or authoritative reference\]

**Record Finalized:**\
\[Date/time or Not Applicable while Active\]

**Maintaining Actor / Responsibility:**\
\[Human, team, AI agent, automated system, or other authorized
maintainer where useful\]

------------------------------------------------------------------------

### Active Record Maintenance

While **Record State** is Active, sections of this template MAY remain incomplete, Pending, Not Applicable, or reference evolving authoritative sources.

The record SHALL be updated as materially relevant realization information arises.

Incompleteness during Active realization SHALL NOT be interpreted as record non-conformance where the information is not yet available or applicable.

A Finalized EDR SHALL satisfy the applicable finalization and Engineering conclusion requirements defined by the Engineering Delivery Record Specification.

## 2. Governing Basis

**Engineering-ready Epic:**\
\[Artifact identity and revision/reference\]

**Approved Investment Baseline:**\
\[Artifact identity and revision/reference, or Not Applicable\]

**Authorized Engineering Delivery Plan:**\
\[Artifact identity and authorized revision/reference\]

**Execution Readiness Decision:**\
\[Decision identity/reference\]

**Execution Baseline:**\
\[Execution Baseline identity/reference\]

**Applicable Architecture Decision Records:**\
\[ADR identities/references, or None\]

**Authorization Conditions:**\
\[Conditions or authoritative reference, or None\]

**Delivery Tolerances:**\
\[Tolerances or authoritative reference, or None\]

**Reassessment Triggers:**\
\[Triggers or authoritative reference, or None\]

**Other Governing Inputs:**\
\[Relevant governed inputs or references, or None\]

------------------------------------------------------------------------

## 3. Engineering Slice Outcomes

Record or reference each Engineering Slice material to the Engineering
conclusion.

  --------------------------------------------------------------------------------------------------------------------------------------
  Slice ID     Terminal       Realization     Validation Outcome      Evidence           Acceptance    Material Change  Residual
               Outcome        Disposition                             Reference(s)       Outcome       / Reassessment   Condition(s)
                                                                                                       Reference(s)     
  ------------ -------------- --------------- ----------------------- ------------------ ------------- ---------------- ----------------
  \[Slice      \[Complete /   \[Concise       \[Outcome/reference\]   \[Reference(s)\]   \[Not         \[Reference(s)   \[Condition(s)
  identity\]   Terminated\]   governed                                                   Applicable /  or None\]        or None\]
                              disposition\]                                              Pending /                      
                                                                                         Satisfied\]                    

  --------------------------------------------------------------------------------------------------------------------------------------

Add rows as required.

Materially relevant progression history MAY be referenced where
necessary to explain a governed outcome, material delay, dependency
consequence, reassessment, termination, or residual condition.

------------------------------------------------------------------------

## 4. Terminated Slice Dispositions

Complete this section for terminated realization material to the
Engineering conclusion.

### \[Slice ID\]

**Reason for Termination:**\
\[Governed reason\]

**Applicable Decision / Authority:**\
\[Decision or authority reference\]

**Realization End Point:**\
\[Point at which realization ended where material\]

**Remaining Execution Obligations:**\
\[Obligations and dispositions\]

**Evidence Produced Before Termination:**\
\[Reference(s), or None\]

**Effect on Dependent Slices:**\
\[Effect or None\]

**Effect on Governing Epic:**\
\[Effect or None\]

**Effect on Execution Baseline:**\
\[Effect or None\]

**Replacement / Superseding Realization:**\
\[Replacement Slice/reference or None\]

**Resulting Governed Disposition:**\
\[Disposition\]

Repeat for each applicable terminated Slice.

------------------------------------------------------------------------

## 5. Replacement and Superseding Realization

Record material replacement or superseding relationships.

  ---------------------------------------------------------------------------------------------------------
  Original    Original          Reason for     Governance Basis         Replacement /         Governed
  Slice       Disposition       Replacement /                           Superseding           Outcome
                                Supersession                            Realization           Continued /
                                                                                              Changed / No
                                                                                              Longer
                                                                                              Applicable
  ----------- ----------------- -------------- ------------------------ --------------------- -------------
  \[Slice     \[Disposition\]   \[Reason\]     \[Decision/reference\]   \[Slice/reference\]   \[Outcome\]
  ID\]                                                                                        

  ---------------------------------------------------------------------------------------------------------

If none:

**Replacement / Superseding Realization:** None.

------------------------------------------------------------------------

## 6. Material Execution Learning

Record only execution learning material to governed Engineering
realization.

### \[Learning ID or concise title\]

**Learning:**\
\[What was learned\]

**Material Consequence:**\
\[Engineering consequence\]

**Affected Governed Basis:**\
\[Baseline, scope, architecture, obligation, risk, cost, timing,
dependency, validation, evidence, acceptance, or other affected basis\]

**Resulting Disposition:**\
\[Adaptation, reassessment, escalation, continuation, or other governed
disposition\]

**Authoritative Reference(s):**\
\[Evidence, decision, issue, ADR, or other reference\]

Repeat as required.

If none:

**Material Execution Learning:** None.

------------------------------------------------------------------------

## 7. Material Governed Adaptations

Record adaptations that materially changed governed realization through
applicable governance.

### \[Adaptation ID or concise title\]

**Affected Realization:**\
\[Slice(s), obligation(s), or other affected realization\]

**Reason for Change:**\
\[Reason\]

**Affected Governed Basis:**\
\[Applicable basis\]

**Governance Decision:**\
\[Decision/reference\]

**Resulting Change to Future Realization:**\
\[Change\]

**Supporting Reference(s):**\
\[Artifact, decision, or evidence reference(s)\]

Repeat as required.

If none:

**Material Governed Adaptations:** None.

------------------------------------------------------------------------

## 8. Reassessment Outcomes

Record material governed reassessments.

### \[Reassessment ID or concise title\]

**Trigger / Material Concern:**\
\[Reassessment Trigger, tolerance exceedance, material learning,
uncertain materiality, or other concern\]

**Affected Realization:**\
\[Slice(s), obligation(s), Plan element(s), or other affected
realization\]

**Applicable Authority / Decision:**\
\[Authority or decision reference\]

**Resulting Disposition:**\
\[Continuation / authorized adaptation / revised Delivery Plan / new or
revised ADR / changed conditions or obligations / changed Slice
structure / return to Delivery Planning / upstream escalation / Slice
termination / replacement realization / other governed disposition\]

**Resulting Governed Basis:**\
\[New or revised basis/reference where changed, or Unchanged\]

Repeat as required.

If none:

**Material Reassessment Outcomes:** None.

------------------------------------------------------------------------

## 9. Material Execution Obligation Dispositions

Record material execution obligations whose dispositions are necessary
to support the Engineering conclusion.

  --------------------------------------------------------------------------------------------------
  Obligation       Obligation Type   Governing       Disposition     Decision /      Residual
                                     Source                          Evidence        Consequence
                                                                     Reference       
  ---------------- ----------------- --------------- --------------- --------------- ---------------
  \[Obligation\]   \[Authorization / \[Reference\]   \[Satisfied /   \[Reference\]   \[Consequence
                   Planning /                        Superseded / No                 or None\]
                   Architecture /                    Longer                          
                   Implementation /                  Applicable /                    
                   Validation /                      Transferred /                   
                   Evidence /                        Escalated /                     
                   Acceptance /                      Accepted                        
                   Dependency /                      Residual                        
                   External /                        Condition /                     
                   Other\]                           Other Governed                  
                                                     Disposition\]                   

  --------------------------------------------------------------------------------------------------

Add rows as required.

------------------------------------------------------------------------

## 10. Architecture Decisions During Realization

Reference new or revised Architecture Decision Records material to the
delivered Engineering outcome.

  --------------------------------------------------------------------------------
  ADR               Execution         Affected Realization       Resulting
                    Learning /                                   Engineering
                    Architecture                                 Consequence
                    Concern                                      
  ----------------- ----------------- -------------------------- -----------------
  \[ADR reference\] \[Concern\]       \[Slice(s)/realization\]   \[Consequence\]

  --------------------------------------------------------------------------------

If none:

**Architecture Decisions During Realization:** None.

------------------------------------------------------------------------

## 11. Technical Validation Outcomes

Preserve or reference technical validation sufficient to support
applicable Engineering claims.

  -------------------------------------------------------------------------------
  Validation        Scope / Claim  Outcome        Authoritative   Material
                                                  Evidence        Consequence
                                                  Reference       
  ----------------- -------------- -------------- --------------- ---------------
  \[Validation      \[What was     \[Satisfied /  \[Reference\]   \[Consequence
  identity/type\]   validated\]    Failed / other                 or None\]
                                   applicable                     
                                   outcome\]                      

  -------------------------------------------------------------------------------

Include only failed validation attempts that have material consequence
to the governed Engineering outcome.

------------------------------------------------------------------------

## 12. Applicable Acceptance Outcomes

Record acceptance outcomes only where the governing basis establishes an
applicable acceptance obligation.

  --------------------------------------------------------------------------------
  Acceptance        Affected Realization       Outcome           Authority /
  Obligation                                                     Evidence
                                                                 Reference
  ----------------- -------------------------- ----------------- -----------------
  \[Obligation\]    \[Slice(s)/realization\]   \[Not Applicable  \[Reference\]
                                               / Pending /       
                                               Satisfied\]       

  --------------------------------------------------------------------------------

If no acceptance obligation applies:

**Acceptance:** Not Applicable.

------------------------------------------------------------------------

## 13. Engineering Evidence References

Reference authoritative Engineering Evidence supporting material
Engineering claims.

  -----------------------------------------------------------------------
  Engineering Claim Evidence          Evidence Type /   Sufficiency
                    Reference         Source            
  ----------------- ----------------- ----------------- -----------------
  \[Claim\]         \[Reference\]     \[CI/CD / test /  \[Sufficient /
                                      validation / ADR  Incomplete\]
                                      / security /      
                                      performance /     
                                      migration /       
                                      deployment /      
                                      operational /     
                                      artifact / review 
                                      / other\]         

  -----------------------------------------------------------------------

Evidence SHOULD remain in its authoritative source where duplication is
unnecessary.

An evidence reference SHALL NOT be treated as sufficient merely because
it exists.

------------------------------------------------------------------------

## 14. Approved Exceptions

Record approved exceptions material to the resulting Engineering
outcome.

### \[Exception ID or concise title\]

**Affected Obligation / Governed Basis:**\
\[Obligation or basis\]

**Nature of Exception:**\
\[Exception\]

**Applicable Authority:**\
\[Authority/decision reference\]

**Material Conditions:**\
\[Conditions or None\]

**Duration / Applicability:**\
\[Duration/scope or Not Applicable\]

**Residual Consequence:**\
\[Consequence or None\]

**Related Evidence / Decision Reference(s):**\
\[Reference(s)\]

Repeat as required.

If none:

**Approved Exceptions:** None.

------------------------------------------------------------------------

## 15. Residual Conditions

Record unresolved governed residual conditions material to the
Engineering conclusion.

### \[Residual Condition ID or concise title\]

**Condition:**\
\[Accepted technical debt, deferred obligation, known limitation,
unresolved dependency, accepted risk, temporary exception, follow-on
Engineering requirement, or other residual condition\]

**Affected Realization:**\
\[Slice(s), Epic, obligation(s), or other affected realization\]

**Material Consequence:**\
\[Consequence\]

**Applicable Authority / Disposition:**\
\[Authority or governed disposition\]

**Expected Follow-on Treatment:**\
\[Follow-on treatment or reference\]

**Governing Basis Reference:**\
\[Reference\]

Repeat as required.

If none:

**Residual Conditions:** None.

------------------------------------------------------------------------

## 16. Engineering Conclusion

**Engineering Conclusion:**\
\[Epic Engineering Completion \| Non-Completion Engineering Conclusion\]

### 16.1 Realized Engineering Outcome

\[Concise statement of what Engineering actually realized against the
Execution Baseline.\]

### 16.2 Material Slice Dispositions

\[Summary or reference to material Complete, Terminated, replaced, or
superseded Slice outcomes.\]

### 16.3 Material Reassessment Consequences

\[Summary or reference, or None.\]

### 16.4 Approved Exceptions

\[Summary or reference, or None.\]

### 16.5 Residual Conditions

\[Summary or reference, or None.\]

### 16.6 Evidence Basis

\[Concise statement or references establishing why the Engineering
conclusion is supported.\]

------------------------------------------------------------------------

## 17. Epic Engineering Completion Basis

Complete this section when the Engineering Conclusion is **Epic
Engineering Completion**.

**Required Engineering Slice Outcomes Accounted For:**\
\[Yes, with reference/summary\]

**Integrated Technical Behavior:**\
\[Outcome/reference\]

**Cross-Slice Dependencies:**\
\[Outcome/reference\]

**Aggregate Technical Validation:**\
\[Outcome/reference\]

**Engineering Evidence Sufficiency:**\
\[Outcome/reference\]

**Architecture Conformance:**\
\[Outcome/reference\]

**Security Obligations:**\
\[Outcome/reference or Not Applicable\]

**Performance Obligations:**\
\[Outcome/reference or Not Applicable\]

**Reliability Obligations:**\
\[Outcome/reference or Not Applicable\]

**Operational Technical Obligations:**\
\[Outcome/reference or Not Applicable\]

**Terminated / Superseded Realization Accounted For:**\
\[Outcome/reference or Not Applicable\]

**Unresolved Governed Issues:**\
\[Disposition/reference or None\]

**Completion Basis Summary:**\
\[Concise basis for Epic Engineering Completion\]

If the Engineering Conclusion is Non-Completion Engineering Conclusion:

**Epic Engineering Completion Basis:** Not Applicable.

------------------------------------------------------------------------

## 18. Non-Completion Engineering Conclusion Basis

Complete this section when the Engineering Conclusion is
**Non-Completion Engineering Conclusion**.

**Specific Governed Reason:**\
\[Reason\]

**Applicable Authority / Decision:**\
\[Authority or decision reference\]

**Resulting Disposition:**\
\[Disposition\]

**Why Epic Engineering Completion Was Not Established:**\
\[Concise explanation\]

**Supporting Traceability / Evidence:**\
\[Reference(s)\]

The specific governed reason does not create a separate canonical
Engineering conclusion state.

If the Engineering Conclusion is Epic Engineering Completion:

**Non-Completion Engineering Conclusion Basis:** Not Applicable.

------------------------------------------------------------------------

## 19. Finalization Assessment

Before changing Record State to Finalized, confirm or reference the
basis for the following.

**Governed Engineering Realization Reached Applicable Conclusion:**\
\[Yes / reference\]

**Required Slice Outcomes Accounted For:**\
\[Yes / reference\]

**Material Terminated / Superseded Realization Dispositioned:**\
\[Yes / Not Applicable / reference\]

**Material Execution Learning Accounted For:**\
\[Yes / Not Applicable / reference\]

**Material Reassessment Outcomes Preserved:**\
\[Yes / Not Applicable / reference\]

**Material Execution Obligations Dispositioned:**\
\[Yes / reference\]

**Applicable Technical Validation Preserved / Referenced:**\
\[Yes / reference\]

**Engineering Evidence Sufficient for Conclusion:**\
\[Yes / reference\]

**Applicable Acceptance Outcomes Preserved:**\
\[Yes / Not Applicable / reference\]

**Approved Exceptions Accounted For:**\
\[Yes / Not Applicable / reference\]

**Residual Conditions Visible:**\
\[Yes / None / reference\]

**Engineering Conclusion Explicitly Represented:**\
\[Yes\]

------------------------------------------------------------------------

## 20. Finalization

**Final Record State:**\
Finalized

**Finalized By / Mechanism:**\
\[Actor or authoritative mechanism performing record finalization\]

**Engineering Conclusion Authority / Decision:**\
\[Authority or governed decision establishing the Engineering conclusion\]

**Finalization Date / Time:**\
\[Date/time\]

**Finalized Record Revision / Identity:**\
\[Revision or immutable identity where applicable\]

**Finalization Notes:**\
\[Optional concise notes\]

Finalization establishes this EDR as the governed evidentiary record of
the concluded Engineering realization.

Finalization does not alter the historical Execution Baseline.

------------------------------------------------------------------------

## 21. Post-Finalization Corrections

Use only where a legitimate post-finalization record correction is
required.

  ------------------------------------------------------------------------------------------
  Correction       Reason        Authority /     Date        Prior Record    Resulting
                                 Maintainer                  Reference       Record
                                                                             Reference
  ---------------- ------------- --------------- ----------- --------------- ---------------
  \[Correction\]   \[Factual     \[Reference\]   \[Date\]    \[Reference\]   \[Reference\]
                   error /                                                   
                   changed                                                   
                   reference /                                               
                   clerical                                                  
                   defect /                                                  
                   identifier                                                
                   change /                                                  
                   other                                                     
                   legitimate                                                
                   maintenance                                               
                   reason\]                                                  

  ------------------------------------------------------------------------------------------

A post-finalization correction SHALL NOT silently alter the historical
Engineering conclusion or governed realization.

Substantive changes to the Engineering conclusion require applicable
Engineering governance and preservation of prior governed history.

------------------------------------------------------------------------

## 22. Traceability Summary

Preserve sufficient traceability to reconstruct the governed Engineering
delivery path.

**Engineering-ready Epic → Approved Investment Baseline → Engineering
Delivery Plan → Execution Baseline:**\
\[References\]

**Execution Baseline → Engineering Slice Realization:**\
\[References\]

**Engineering Slice Realization → Engineering Evidence:**\
\[References\]

**Engineering Evidence → Engineering Conclusion:**\
\[References\]

Where material change occurred:

**Original Governed Basis → Material Learning / Trigger → Reassessment /
Decision → Revised Governed Basis → Resulting Realization:**\
\[References or Not Applicable\]

------------------------------------------------------------------------

## 23. Release Boundary

The Engineering Delivery Record MAY provide the Engineering basis for an
applicable downstream cross-system Release Admission decision.

A downstream Release process or record MAY reference this Finalized EDR.
The EDR does not require a reverse reference to a subsequently established
Release Admission decision.

This record does not itself establish:

-   Release Admission;
-   Release Authorization;
-   Release Readiness;
-   environment promotion authority;
-   Production promotion authority; or
-   commercial launch authority.

------------------------------------------------------------------------

## 24. Record Integrity Notes

Use this section only for information necessary to understand the
integrity or interpretation of the EDR.

\[Optional notes, or None.\]

The EDR is complete when it sufficiently supports the governed
Engineering conclusion. Completeness is not determined by the volume of
operational detail recorded.
