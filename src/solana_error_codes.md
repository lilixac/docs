# Tokens Gateway Error Codes

| SN | Hex  | Error                        | Message                                                         |
| -- | ---- | ---------------------------- | --------------------------------------------------------------- |
| 1  | 0x01 | InvalidToken                 | Invalid Token                                                   |
| 2  | 0x02 | InvalidAmount                | Invalid Amount                                                  |
| 3  | 0x03 | InvalidIndex                 | Invalid Length                                                  |
| 4  | 0x04 | InvalidAccount               | Invalid Account                                                 |
| 5  | 0x05 | InvalidReceiver              | Invalid Receiver                                                |
| 6  | 0x06 | InvalidL1Token               | Invalid L1 Token                                                |
| 7  | 0x07 | InvalidBatchNumber           | Invalid BatchNumber                                             |
| 8  | 0x08 | InvalidPDA                   | Invalid PDA derived                                             |
| 9  | 0x09 | InvalidInstructionData       | Invalid Instruction                                             |
| 10 | 0x0A | InvalidTransaction           | Invalid Transaction                                             |
| 11 | 0x0B | InvalidTokenAccount          | Invalid Token Account                                           |
| 12 | 0x0C | InvalidAddress               | Invalid address provided                                        |
| 13 | 0x0D | ReceiverAccountNotFound      | Receiver account not found                                      |
| 14 | 0x0E | WithdrawalAlreadyExecuted    | Withdraw is already executed                                    |
| 15 | 0x0F | InvalidTokenAddress          | Invalid Token address format                                    |
| 16 | 0x10 | SerializeFailed              | Failed to serialize the state                                   |
| 17 | 0x11 | NonceNotFound                | Nonce not found in withdrawals                                  |
| 18 | 0x12 | PublicValueDecodeFailed      | Failed to decode public value                                   |
| 19 | 0x13 | InvalidL2Token               | Invalid L2 token address format                                 |
| 20 | 0x14 | TokenNotFound                | Token mint not found in the vault.                              |
| 21 | 0x15 | RemoveFailed                 | Failed to remove the particular role                            |
| 22 | 0x16 | BatchNotCommitted            | Batch needs to be committed before finalization                 |
| 23 | 0x17 | Overflow                     | Overflow occurred while updating total deposits.                |
| 24 | 0x18 | QueueOverflow                | The deposit queue has reached its maximum capacity.             |
| 25 | 0x19 | InvalidArgument              | Invalid Argument provided for signature verification.           |
| 26 | 0x1A | Unauthorized                 | Unauthorized: Caller does not have the required role.           |
| 27 | 0x1B | TokenMappingNotFound         | Token decimal mapping not found for the specified token         |
| 28 | 0x1C | InsufficientFundsForTransfer | Insufficient funds in user's token account for transfer.        |
| 29 | 0x1D | BatchNotFinalized            | Batch needs to be finalized before finalizing withdrawal        |
| 30 | 0x1E | InsufficientFunds            | Insufficient funds in the vault for the requested withdrawal.   |
| 31 | 0x1F | PublicKeyMismatch            | The provided public key does not match the expected public key. |
| 32 | 0x20 | FailedToSerializeEvent       | Failed to serialize event.                                      |


# Twine Chain Error Codes

| SN | Hex  | Error                            | Message                                                                 |
| -- | ---- | -------------------------------- | ----------------------------------------------------------------------- |
| 1  | 0x01 | InvalidIndex                     | Invalid Index                                                           |
| 2  | 0x02 | NonceNotFound                    | Nonce not found                                                         |
| 3  | 0x03 | InvalidStateRootSequence         | State root mismatch                                                     |
| 4  | 0x04 | InvalidInstructionData           | Invalid Instruction                                                     |
| 5  | 0x05 | TwineVerificationError           | Error in verification                                                   |
| 6  | 0x06 | InvalidReceiptRoot               | Receipt root mismatch                                                   |
| 7  | 0x07 | InvalidTransactionType           | Invalid Transaction Type                                                |
| 8  | 0x08 | UninitializedAccount             | Account not initialized yet                                             |
| 9  | 0x09 | EmptyPreviousBatch               | Previous Batch Data is empty                                            |
| 10 | 0x0A | SerializeFailed                  | Failed to serialize the state                                           |
| 11 | 0x0B | PublicValueDecodeFailed          | Failed to decode public value                                           |
| 12 | 0x0C | InvalidDataLength                | Input data exceeds max length                                           |
| 13 | 0x0D | InvalidTokenAddressFormat        | Invalid Token Address Format                                            |
| 14 | 0x0E | InvalidBatchSequence             | Finalize in Serial batch order                                          |
| 15 | 0x0F | InsufficientFundsForTransfer     | Insufficient Funds for Transfer                                         |
| 16 | 0x10 | InvalidReceiverAddressFormat     | Invalid Receiver Address Format                                         |
| 17 | 0x11 | TokenMappingNotFound             | Token Decimal Mapping Not Found                                         |
| 18 | 0x12 | InvalidL2TokenAddressFormat      | Invalid L2 Token Address Format                                         |
| 19 | 0x13 | BatchNotFinalized                | Batch needs to be finalized first                                       |
| 20 | 0x14 | DepositRollingHashMismatch       | Deposit Rolling Hash is mismatched                                      |
| 21 | 0x15 | InvalidNonceGap                  | Copied Nonce must have required gap                                     |
| 22 | 0x16 | WithdrawRollingHashMismatch      | Withdraw Rolling Hash is mismatched                                     |
| 23 | 0x17 | PreviousBatchNotFinalized        | Previous Batch needs to be finalized                                    |
| 24 | 0x18 | RemoveFailed                     | Failed to remove the particular role                                    |
| 25 | 0x19 | LayerZeroRollingHashMismatch     | LayerZero Rolling Hash is mismatched                                    |
| 26 | 0x1A | EmptyBatchCommitment             | Commitment of Empty Batch not allowed                                   |
| 27 | 0x1B | InvalidBatchFinalizationSequence | Finalization should be done in sequence                                 |
| 28 | 0x1C | LastCommitedBatchHashMismatch    | Last commited batch hash did not match                                  |
| 29 | 0x1D | MessageExecutedCountError        | Cannot execute less message than before                                 |
| 30 | 0x1E | InvalidPDA                       | PDA derived does not equal PDA passed in                                |
| 31 | 0x1F | LastFinalizedBatchHashMismatch   | Last finalized batch hash did not match                                 |
| 32 | 0x20 | InvalidStartNonce                | Blocks must be comitted in sequential order                             |
| 33 | 0x21 | InvalidBlockCommitmentSequence   | Messages must be copied in sequential order                             |
| 34 | 0x22 | BatchHashMismatch                | Calculated and Provided Batch Hash did not match                        |
| 35 | 0x23 | InvalidSigner                    | The provided account did not sign the transaction.                      |
| 36 | 0x24 | Unauthorized                     | Unauthorized: Caller does not have the required role                    |
| 37 | 0x25 | BatchNotFilled                   | All batch data needs to be filled before finalization                   |
| 38 | 0x26 | InvalidBlockData                 | Provided startBlock/endBlock and the block data mismatch                |
| 39 | 0x27 | OverflowError                    | Overflow occurred while updating total deposits or withdrawals.         |
| 40 | 0x28 | WithdrawalAlreadyExecuted        | The withdrawal with the provided nonce has already been executed.       |
| 41 | 0x29 | GreaterCount                     | The transaction count is greater than transactions present in the queue |
| 42 | 0x2A | FailedToSerializeEvent           | Failed to serialize event.                                              |
