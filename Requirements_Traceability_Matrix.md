# Requirements Traceability Matrix

| Requirement | Related Feature / Use Case | Architecture Component(s) | Verification Evidence |
|---|---|---|---|
| FR1 – Record Solar Generation | Smart-meter telemetry ingestion | Smart Meter Data Service, Solar Credit Database | Telemetry validation / integration test |
| FR2 – View Solar Credit Balance | View balance | Prosumer Portal / UI, Solar Credit Database | Balance retrieval test |
| FR3 – Transfer Solar Credits | Transfer Solar Credits use case | Prosumer Portal / UI, Order Manager, Solar Credit Database | Successful transfer and insufficient-balance tests |
| FR4 – Apply Credits to Electricity Bill | Bill-credit application | Prosumer Portal / UI, Payment Service, Solar Credit Database | Bill-credit test |
| FR5 – View Credit and Billing Information | Transaction/billing view | Prosumer Portal / UI, Payment Service, Solar Credit Database | Billing/transaction retrieval test |
| NFR1 – 99.9% Availability | Service availability | All service components | Availability review / deployment test |
| NFR2 – 500-household hourly telemetry | Telemetry processing | Smart Meter Data Service, Solar Credit Database | Scalability/load test plan |
