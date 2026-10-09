# Software Requirements Specification (SRS)

## 1. Introduction

### 1.1 Project Name
Community Solar Credit Allocation Manager

### 1.2 Problem Statement
Problem Statement #63.

### 1.3 Purpose
The purpose of the system is to manage solar-generation credits for participating community households and provide controlled operations for viewing, transferring, and applying those credits.

## 2. Scope

The system covers:

- Household/prosumer account access.
- Solar-generation data ingestion.
- Solar-credit balance management.
- Solar-credit transfers.
- Application of eligible credits to electricity bills.
- Billing and transaction information.

## 3. Users

### Prosumer Resident
Can view their account and credit balance, transfer eligible credits, and apply credits to electricity bills.

### Co-op Manager
Can monitor community solar-credit activity and review relevant billing and transaction information.

## 4. Functional Requirements

- **FR1:** Record solar generation.
- **FR2:** View solar-credit balance.
- **FR3:** Transfer solar credits.
- **FR4:** Apply credits to electricity bill.
- **FR5:** View credit and billing information.

## 5. Non-Functional Requirements

- **NFR1:** Target 99.9% availability.
- **NFR2:** Support hourly smart-meter telemetry for 500 households while maintaining responsive interactive operations.

## 6. Main Use Case – Transfer Solar Credits

### Preconditions
- User is authenticated.
- Sender account is active.
- Recipient is valid and eligible.
- Sender has sufficient transferable credits.

### Main Flow
1. User selects credit transfer.
2. User enters recipient and amount.
3. System validates recipient.
4. System checks available balance.
5. System authorizes the operation.
6. System deducts sender credits.
7. System adds recipient credits.
8. System records the transaction.
9. System confirms the transfer.

### Failure Conditions
- Insufficient balance.
- Invalid recipient.
- Invalid transfer amount.
- Inactive account.

No partial balance update should occur when a transfer fails.

## 7. System Architecture

Major components:

- Prosumer Portal / UI
- Order Manager
- Payment Service
- Smart Meter Data Service
- Solar Credit Database

Interfaces:

- Credit Transfer API
- Payment Processing API
- Meter Telemetry API
- Credit / Account API
- Billing Data API

## 8. Data Requirements

The system should maintain information such as:

- Household/account identifier
- Solar-generation readings
- Solar-credit balance
- Credit-transfer records
- Billing information
- Transaction timestamp
- Transaction status

## 9. Security Requirements

- Authenticate users before protected operations.
- Authorize access to account and transaction data.
- Validate transfer amounts.
- Validate recipient eligibility.
- Prevent unauthorized direct database access from the UI.
- Record important credit and billing operations for traceability.

## 10. Performance and Availability

The system targets 99.9% availability and is designed to support hourly telemetry from 500 households. Telemetry ingestion should be separated from interactive account operations so that normal user actions remain responsive.

## 11. Acceptance Criteria

The system should demonstrate:

1. Solar-generation data can be recorded.
2. A user can view a correct credit balance.
3. A valid credit transfer updates both accounts correctly.
4. An insufficient-balance transfer is rejected without changing balances.
5. Eligible credits can be applied to a bill.
6. Credit and billing transaction information can be retrieved by authorized users.
