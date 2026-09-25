# MediConnect User Stories & Acceptance Criteria

## FR-01 — User Access and Role Management

### US-01
**User Story:** As a Provider, Care Coordinator, Billing Staff member, or Administrator, I want to access the system according to my assigned role so that I can access the appropriate features and information.

**Acceptance Criteria**
- Valid credentials allow access.
- The system identifies the assigned role after login.
- Features and information are available according to the assigned role.
- PA Coordinator can access PA request management.
- Administrator has administrative/system-management access.
- Unauthorized features/information are blocked.
- Invalid credentials show an error.

### US-02
**User Story:** As an Administrator, I want to create a user account so that authorized users can access MediConnect according to their assigned role.

### US-03
**User Story:** As an Administrator, I want to update user accounts so that user information and access assignments remain current.

### US-04
**User Story:** As an Administrator, I want to disable a user account so that access can be removed when required.

## FR-02 — Patient and Case Intake

### US-05
**User Story:** As a PA Coordinator, I want to capture patient demographic information so that the patient details required for the PA case are available.

### US-06
**User Story:** As a PA Coordinator, I want to capture payer, plan, policy, and member information so that the case contains the insurance information required for authorization processing.

### US-07
**User Story:** As a PA Coordinator, I want to create a PA case manually or from an incoming EHR referral so that authorization cases can enter MediConnect through the supported intake methods.

### US-08
**User Story:** As a PA Coordinator, I want the case identifier to be preserved across downstream transactions so that related authorization activity remains associated with the correct case.

## FR-03 — Clinical Data Acquisition

### US-09
**User Story:** As a PA Coordinator, I want to receive patient clinical data from the hospital EHR so that the clinical information required for the prior authorization case is available in MediConnect.

### US-10
**User Story:** As a PA Coordinator, I want to capture available diagnosis codes, procedure codes, medications, allergies, notes, and supporting documentation so that the PA request contains the required clinical information.

### US-11
**User Story:** As a PA Coordinator, I want the system to validate required clinical fields before submission so that incomplete clinical information is identified before the payer workflow.

## FR-04 — HL7 Integration

### US-12
**User Story:** As a PA Coordinator, I want the system to accept HL7 messages from the hospital EHR and associate them with the correct patient or case so that the received information is linked to the appropriate record.

### US-13
**User Story:** As a PA Coordinator, I want the system to validate the structure of incoming HL7 messages and reject malformed messages with an actionable error message so that invalid data does not proceed for processing.

### US-14
**User Story:** As a PA Coordinator, I want the system to log inbound and outbound HL7 message activity so that HL7 transactions can be traced when required.

## FR-05 — HL7 to FHIR Transformation

### US-15
**User Story:** As a PA Coordinator, I want the system to transform supported HL7 data elements into FHIR resources so that the clinical data can be used for downstream processing.

### US-16
**User Story:** As a PA Coordinator, I want patient, encounter, condition, observation, and document data to be mapped into the appropriate FHIR structures so that the required information is represented in a standardized format.

### US-17
**User Story:** As a PA Coordinator, I want the system to flag unmapped or incomplete data elements for review so that missing or unsupported information is not silently dropped.

## FR-06 — FHIR API Services

### US-18
**User Story:** As a PA Coordinator, I want the system to expose FHIR-based APIs for exchanging patient and authorization data so that this data can be exchanged using standardized FHIR interfaces.

### US-19
**User Story:** As a PA Coordinator, I want the system to support create, read, update, and query operations for authorization-related FHIR resources so that authorization data can be managed through the available FHIR services.

### US-20
**User Story:** As a PA Coordinator, I want the system to return standardized API responses for successful requests, validation errors, and downstream processing states so that the outcome of an API request is clearly communicated.

## FR-07 — Prior Authorization Workflow

### US-21
**User Story:** As a PA Coordinator, I want to create a prior authorization request from the available clinical and insurance data so that the request contains the information required for authorization processing.

### US-22
**User Story:** As a PA Coordinator, I want the system to route the prior authorization request to the correct payer based on plan and payer rules so that the request is sent to the appropriate payer.

### US-23
**User Story:** As a PA Coordinator, I want the system to maintain the prior authorization request status so that I can track the request through Draft, Submitted, Pending Review, Approved, Denied, and More Information Required states.

### US-24
**User Story:** As a PA Coordinator, I want to add supplemental documents and resend the prior authorization request when additional information is requested so that the payer receives the required information for further processing.

## FR-08 — Payer Response Handling

### US-25
**User Story:** As a PA Coordinator, I want the system to receive payer decisions and store them against the associated authorization case so that the outcome of the prior authorization request is recorded in MediConnect.

### US-26
**User Story:** As a PA Coordinator, I want the system to support payer responses for approval, denial, and requests for additional information so that different payer decision outcomes can be handled appropriately.

### US-27
**User Story:** As a PA Coordinator, I want the system to capture payer reasons, remarks, and next-step instructions where provided so that the case contains the relevant information received from the payer.

## Note
User stories above are the working BA mapping of the functional requirements. Acceptance criteria are maintained in the project RTM/test artefacts.
