# GitHub Copilot Prompts

Use these prompts during the actual GitHub Copilot activity. Keep screenshots of the real interaction if required by the submission.

## Prompt 1 – Credit Balance Validation

Create a clean function for a Community Solar Credit Allocation Manager that validates whether a sender has enough available solar credits for a requested transfer. Reject zero or negative transfer amounts and return a clear success/failure result.

## Prompt 2 – Credit Transfer

Implement a service method for transferring solar credits between two eligible accounts. Validate the sender balance and recipient account, update both balances consistently, and record a transaction. Do not allow partial updates if the operation fails.

## Prompt 3 – Telemetry Validation

Create a function that validates hourly smart-meter telemetry for a household. Validate household ID, timestamp, generation value, and reject invalid or negative generation readings.

## Prompt 4 – Unit Tests

Generate unit tests for credit-transfer validation covering:

1. Successful transfer.
2. Insufficient credits.
3. Invalid recipient.
4. Zero or negative transfer amount.

## Prompt 5 – Code Review

Review the generated credit-transfer code for correctness, input validation, transaction consistency, security, and maintainability. Suggest improvements while preserving the intended business rules.
