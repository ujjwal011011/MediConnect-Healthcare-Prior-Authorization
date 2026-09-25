# Prior Authorization Business Workflow

1. Hospital EHR provides patient/clinical information to MediConnect through supported integration interfaces.
2. MediConnect validates incoming HL7 structure where applicable.
3. Supported HL7 data is transformed into FHIR resources.
4. Patient and insurance/case information is available for PA processing.
5. PA Coordinator creates or reviews the PA request using available clinical and insurance data.
6. MediConnect routes the PA request to the appropriate payer based on payer/plan rules.
7. Payer returns a decision or requests additional information.
8. MediConnect stores the payer response against the associated case.
9. MediConnect updates the hospital EHR with authorization status and notifies relevant users.
10. Audit and reporting functions support tracking and monitoring.

**Important scope note:** The functional requirements specify a separate "Payer System"; they do not define a specific payer vendor platform or payer-side user interface.
