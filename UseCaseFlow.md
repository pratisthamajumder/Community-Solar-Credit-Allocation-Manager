# Use Case Flow – Transfer Solar Credits

## Use Case Information

**Use Case:** Transfer Solar Credits  
**Primary Actor:** Prosumer Resident

## Preconditions

1. The user is authenticated.
2. The sender account is active.
3. The recipient account is valid and eligible.
4. The sender has sufficient transferable solar credits.

## Main Success Scenario

1. The Prosumer Resident opens the credit-transfer function.
2. The system asks for the recipient account and transfer amount.
3. The user enters the recipient and amount.
4. The system validates the recipient account.
5. The system checks the sender's available transferable credit balance.
6. The system authorizes the transfer.
7. The system deducts the transferred amount from the sender.
8. The system adds the transferred amount to the recipient.
9. The system records the transaction.
10. The system displays a successful-transfer confirmation.

## Alternate Flow A – Insufficient Credits

At Step 5, if the requested amount is greater than the sender's available transferable balance:

1. The system rejects the transfer.
2. No account balance is changed.
3. The system displays an insufficient-credit message.
4. The failed request is not recorded as a successful transfer.

## Alternate Flow B – Invalid Recipient

At Step 4, if the recipient is invalid or not eligible:

1. The system rejects the transfer.
2. No account balance is changed.
3. The system informs the user that the recipient is invalid.
4. The user may enter another recipient.

## Postconditions – Successful Transfer

- Sender balance is reduced by the transferred amount.
- Recipient balance is increased by the transferred amount.
- A transaction record is created.
- The user receives confirmation.
