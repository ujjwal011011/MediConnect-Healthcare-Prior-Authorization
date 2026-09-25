# Sequence Diagram

~~~mermaid
sequenceDiagram
    participant EHR as Hospital EHR
    participant PA as PA Coordinator
    participant MC as MediConnect Platform
    participant INT as HL7/FHIR Integration
    participant PAYER as Payer System
    participant N as Notification / EHR Update

    EHR->>MC: Send HL7 Message / Clinical Data
    MC->>INT: Process HL7 Message
    INT->>INT: Validate HL7 Structure
    alt Invalid HL7
        INT-->>MC: Validation Error
        MC->>N: Notify transmission / processing failure
    else Valid HL7
        INT->>INT: Transform HL7 to FHIR
        INT-->>MC: FHIR Resources
    end

    PA->>MC: Create / Review PA Request
    PA->>MC: Submit PA Request
    MC->>PAYER: Send PA Request
    PAYER-->>MC: Decision / Additional Information Request
    MC->>N: Update EHR / Notify Relevant Users

    alt More Information Required
        PA->>MC: Add Supplemental Documents
        PA->>MC: Resend PA Request
        MC->>PAYER: Resubmit PA Request
    end
~~~
