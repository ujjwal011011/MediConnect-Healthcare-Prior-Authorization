# Use Case Diagram

~~~mermaid
flowchart LR
  Provider([Provider])
  PA([PA Team / Care Coordinator])
  Billing([Billing Staff])
  Admin([Administrator])
  PayerReviewer([Payer Reviewer])
  EHR([Hospital EHR])
  Payer([Payer System])

  subgraph System["Prior Authorization Management System"]
    Access((Access System))
    ManagePA((Manage Prior Authorization Request))
    Intake((Capture Patient & Case Information))
    CreateCase((Create PA Case))
    Docs((Manage Supporting Documents))
    Submit((Submit Prior Authorization Request))
    Response((Process Payer Response))
    Notify((Update EHR & Notify Users))
    Audit((View Audit Trail & Case History))
    Reports((Generate Reports & Monitor Cases))
    Clinical((Acquire Clinical Data))
    Validate((Validate Clinical Data))
    HL7((Process HL7 Messages))
    Transform((Transform HL7 to FHIR))
    FHIR((Manage FHIR API Services))
    Users((Manage User Accounts))
  end

  Provider --- Access
  PA --- Access
  PA --- ManagePA
  PA --- Intake
  PA --- CreateCase
  PA --- Docs
  PA --- Submit
  PA --- Response
  PA --- Audit
  PA --- Reports
  Admin --- Access
  Admin --- Users
  Billing --- Access
  Billing --- ManagePA
  EHR --- Clinical
  EHR --- HL7
  EHR --- Notify
  Payer --- Submit
  Payer --- Response
  PayerReviewer --- Response
~~~

**Scope note:** The functional requirements specify a separate Payer System. They do not define a specific payer vendor interface or UI.
