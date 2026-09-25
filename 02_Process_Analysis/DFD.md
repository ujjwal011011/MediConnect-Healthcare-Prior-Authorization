# Data Flow Diagram

~~~mermaid
flowchart LR
  EHR[Hospital EHR] -->|HL7 / Patient & Clinical Data| MC[MediConnect Prior Authorization Platform]
  MC -->|HL7 Validation & HL7 to FHIR| INT[Interoperability Processing]
  INT -->|Clinical / FHIR Data| PA[Prior Authorization Processing]
  PA -->|PA Request| PAYER[Payer System]
  PAYER -->|Decision / Response| PA
  PA -->|Status Update| EHR
  PA -->|Notification| USERS[PA Team / Relevant Users]
  PA --> AUDIT[Audit & Tracking]
  PA --> REPORT[Reporting & Monitoring]
~~~

This is a conceptual business/system flow derived from the documented functional requirements.
