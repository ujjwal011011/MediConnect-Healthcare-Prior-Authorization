# Activity Diagram

~~~mermaid
flowchart TD
    A([Start]) --> B[Hospital EHR sends clinical data]
    B --> C[Receive HL7 message]
    C --> D[Validate HL7 structure]
    D --> E{HL7 valid?}
    E -- No --> F[Reject malformed message and provide actionable error]
    F --> G[Log / notify failure]
    G --> Z([End])
    E -- Yes --> H[Transform supported HL7 data to FHIR]
    H --> I[Review clinical and insurance/case information]
    I --> J[Create PA request]
    J --> K[Route request to correct payer]
    K --> L[Payer processes request]
    L --> M[Receive payer response]
    M --> N{More information required?}
    N -- Yes --> O[Add supplemental documents]
    O --> P[Resend PA request]
    P --> L
    N -- No --> Q[Store payer decision against case]
    Q --> R[Update EHR and notify relevant users]
    R --> S[Track audit / reporting information]
    S --> Z
~~~
