# Requirements Engineering

## 1. Problem Statement

**Community Solar Credit Allocation Manager – Problem Statement #63**

The system manages solar-generation credits for households participating in a community solar program.

## 2. Actors

### Prosumer Resident
A household/user who participates in the community solar program. The resident can view credit balances, transfer eligible credits, and apply eligible credits toward electricity bills.

### Co-op Manager
An authorized manager who monitors solar-credit activities and reviews relevant account, billing, and transaction information.

## 3. Functional Requirements

### FR1 – Record Solar Generation
The system shall record solar-generation information received from participating smart meters and associate the readings with the correct household/account.

### FR2 – View Solar Credit Balance
The system shall allow an authorized user to view the current available solar-credit balance for their account.

### FR3 – Transfer Solar Credits
The system shall allow an eligible user to transfer available solar credits to another eligible community account after validating the sender balance and recipient account.

### FR4 – Apply Credits to Electricity Bill
The system shall allow eligible solar credits to be applied toward an electricity bill and update the remaining credit balance after a successful operation.

### FR5 – View Credit and Billing Information
The system shall allow authorized users to view relevant credit-transfer records and billing information.

## 4. Non-Functional Requirements

### NFR1 – Availability
The system shall target **99.9% availability** during normal service operation.

### NFR2 – Performance and Scalability
The system shall support **hourly smart-meter telemetry for 500 households** while keeping normal credit, balance, and account operations responsive.

## 5. Constraints and Assumptions

- Only authorized users can access account and transaction information.
- A credit transfer shall not exceed the sender's available transferable balance.
- Smart-meter readings shall be associated with a valid household/account.
- Credit and billing operations shall be recorded for traceability.
- The system architecture should allow telemetry processing to operate without unnecessarily blocking interactive account operations.

## 6. Requirement Summary

| ID | Type | Requirement |
|---|---|---|
| FR1 | Functional | Record solar generation |
| FR2 | Functional | View solar-credit balance |
| FR3 | Functional | Transfer solar credits |
| FR4 | Functional | Apply credits to electricity bill |
| FR5 | Functional | View credit and billing information |
| NFR1 | Non-functional | 99.9% availability target |
| NFR2 | Non-functional | Hourly telemetry for 500 households with responsive operations |
