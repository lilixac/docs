# Ethereum Error Codes

This section lists the error codes and their selectors for various Ethereum components in the Twine project.

## L1 Errors

### Gateway Errors

#### ITwineL1Gateway

| Selector     | Error                   |
|--------------|-------------------------|
| 0xd92e233d   | ZeroAddress()           |
| 0x1f2a2005   | ZeroAmount()            |
| 0x0a56e9ba   | InsufficientGasValue()  |

#### IL1ERC20Gateway

| Selector     | Error                       |
|--------------|-----------------------------|
| 0x078e1d85   | ZeroDepositAmount()         |
| 0x73442b08   | NonZeroMsgValue()           |
| 0xd376f27c   | L2TokenMismatch()           |
| 0x6de6e1b8   | NoCorrespondingL2Token()    |

#### IL1ETHGateway

| Selector     | Error                            |
|--------------|----------------------------------|
| 0x339fa7f8   | WrongL2Token()                   |
| 0x786e0a99   | InsufficientContractBalance()    |
| 0xb12d13eb   | ETHTransferFailed()              |
| 0x8d712b1b   | LessThanMessageValue()           |

#### L1GatewayRouter

| Selector     | Error                           |
|--------------|---------------------------------|
| 0xd92e233d   | ZeroAddress()                   |
| 0x66c26ad4   | OnlyNotInContext()              |
| 0xb9d9bda8   | OnlyInDepositContext()          |
| 0xfecd80a9   | NoGatewayAvailable()            |
| 0x7fb532e6   | NoETHGatewayAvailable()         |
| 0xff633a38   | LengthMismatch()                |
| 0xddf71e2d   | NotAccessibleFromRouter()       |

### Messenger Errors

#### IL1TwineMessengerBase

| Selector     | Error              |
|--------------|--------------------|
| 0xa7f9319d   | ErrorZeroAddress() |

### Message Handler Errors

#### IL1MessageHandler

| Selector     | Error              |
|--------------|--------------------|
| 0x3e5d9c77   | OnlyMessenger()    |
| 0x63df8171   | InvalidIndex()     |
| 0x7a47c9a2   | InvalidChainId()   |
| 0xa7f9319d   | ErrorZeroAddress() |

### Twine Chain Errors

#### ITwineChain

| Selector     | Error                                   |
|--------------|-----------------------------------------|
| 0xa7f9319d   | ErrorZeroAddress()                      |
| 0xed4b2a9e   | InvalidVerificationKeys()               |
| 0x5d2bd23c   | GenesisBlockAlreadyCommitted()          |
| 0x9d2d39ad   | NotAtGenesis()                          |
| 0xc3028de4   | InvalidBatchSequence()                  |
| 0x4f99981d   | BatchMustBeFinalizedSequentially()      |
| 0x98adb9b4   | CommittedBatchHashMismatch()            |
| 0x3b328caf   | PreviousBatchHashMismatch()             |
| 0x7d372368   | LastFinalizedBatchHashMismatch()        |
| 0x7d254912   | InvalidMessageCount()                   |
| 0x9a83650b   | RefundAlreadyProcessed()                |
| 0x395c1f11   | WithdrawalAlreadyProcessed()            |
| 0x3f2b8e66   | TransactionMustBeDepositType()          |
| 0x70024ac1   | TransactionMustBeWithdrawType()         |
| 0x9b2aafee   | BatchNotFinalizedYet()                  |
| 0xe641eb12   | BatchHashMismatch()                     |
| 0x7e598527   | MessageHashNotFound()                   |

## L2 Errors

### Gateway Errors

#### ITwineL2Gateway

| Selector     | Error                                    |
|--------------|------------------------------------------|
| 0xa7f9319d   | ErrorZeroAddress()                       |
| 0x85bd908d   | ErrorCallerIsNotMessenger()              |
| 0xf6281e60   | ErrorCallerIsNotCounterpartGateway()     |