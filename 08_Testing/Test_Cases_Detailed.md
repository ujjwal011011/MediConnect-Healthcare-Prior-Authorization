# System Test Cases — Detailed Coverage

The source workbook contains 37 test cases. All are currently marked **Not Executed** with Actual Result set to **To be executed**.

| ID | Req. | User Story | Test Scenario | Status |
|---|---|---|---|---|
| TC-01 | FR-01 | US-01 | Verify role-based system access | Not Executed |
| TC-02 | FR-01 | US-01 | Verify unauthorized feature access is blocked | Not Executed |
| TC-03 | FR-01 | US-01 | Verify invalid login handling | Not Executed |
| TC-04 | FR-01 | US-02 | Verify administrator can create a user account | Not Executed |
| TC-05 | FR-01 | US-03 | Verify administrator can update a user account | Not Executed |
| TC-06 | FR-01 | US-04 | Verify administrator can disable a user account | Not Executed |
| TC-07 | FR-02 | US-05 | Verify manual patient and case intake | Not Executed |
| TC-08 | FR-02 | US-06 | Verify case creation from incoming EHR referral | Not Executed |
| TC-09 | FR-02 | US-07 | Verify case identifier is preserved | Not Executed |
| TC-10 | FR-03 | US-09 | Verify clinical data is received from Hospital EHR | Not Executed |
| TC-11 | FR-03 | US-10 | Verify required clinical information can be captured | Not Executed |
| TC-12 | FR-03 | US-11 | Verify required clinical fields are validated | Not Executed |
| TC-13 | FR-04 | US-12 | Verify HL7 message is accepted and associated with correct patient/case | Not Executed |
| TC-14 | FR-04 | US-13 | Verify malformed HL7 message is rejected | Not Executed |
| TC-15 | FR-04 | US-14 | Verify inbound and outbound HL7 activity is logged | Not Executed |
| TC-16 | FR-05 | US-15 | Verify supported HL7 data is transformed to FHIR | Not Executed |
| TC-17 | FR-05 | US-16 | Verify required data is mapped to FHIR structures | Not Executed |
| TC-18 | FR-05 | US-17 | Verify unmapped/incomplete data is flagged | Not Executed |
| TC-19 | FR-06 | US-18 | Verify FHIR API service exposes patient/authorization data | Not Executed |
| TC-20 | FR-06 | US-19 | Verify create/read/update/query operations | Not Executed |
| TC-21 | FR-06 | US-20 | Verify standardized API responses | Not Executed |
| TC-22 | FR-07 | US-21 | Verify PA request creation from clinical and insurance data | Not Executed |
| TC-23 | FR-07 | US-22 | Verify routing to correct payer | Not Executed |
| TC-24 | FR-07 | US-23 | Verify PA workflow status transitions | Not Executed |
| TC-25 | FR-07 | US-24 | Verify supplemental documents and resend | Not Executed |
| TC-26 | FR-08 | US-25 | Verify payer decision is stored against case | Not Executed |
| TC-27 | FR-08 | US-26 | Verify approval, denial and additional-information responses | Not Executed |
| TC-28 | FR-08 | US-27 | Verify payer reasons, remarks and next steps are captured | Not Executed |
| TC-29 | FR-09 | US-28 | Verify EHR receives PA status update | Not Executed |
| TC-30 | FR-09 | US-29 | Verify user notification for important PA events | Not Executed |
| TC-31 | FR-09 | US-30 | Verify transmission failure notification | Not Executed |
| TC-32 | FR-10 | US-31 | Verify audit trail captures case and user actions | Not Executed |
| TC-33 | FR-10 | US-32 | Verify audit details | Not Executed |
| TC-34 | FR-10 | US-33 | Verify authorized users can view case history | Not Executed |
| TC-35 | FR-11 | US-34 | Verify reporting of case volume and outcomes | Not Executed |
| TC-36 | FR-11 | US-35 | Verify stalled/missing-information cases can be identified | Not Executed |
| TC-37 | FR-11 | US-36 | Verify report export | Not Executed |

## Requirement Coverage

- FR-01: TC-01 to TC-06
- FR-02: TC-07 to TC-09
- FR-03: TC-10 to TC-12
- FR-04: TC-13 to TC-15
- FR-05: TC-16 to TC-18
- FR-06: TC-19 to TC-21
- FR-07: TC-22 to TC-25
- FR-08: TC-26 to TC-28
- FR-09: TC-29 to TC-31
- FR-10: TC-32 to TC-34
- FR-11: TC-35 to TC-37

For execution, the XLSX workbook remains the working test-management artefact; this Markdown file provides recruiter-friendly visibility into coverage without inventing execution results.
