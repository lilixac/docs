# Solana Events

## Twine Chain Events

### 1. MessageTransaction

Emitted after deposit/ForcedWithdraw transaction is successfully added to the queue.

```rust
pub struct MessageHandledEvent {
    pub event: String,
    pub nonce: u64,
    pub l1_pubkey: String,
    pub twine_address: String,
    pub l1_token: String,
    pub l2_token: String,
    pub chain_id: u64,
    pub amount: String,
    pub data: Vec<u8>, 
    pub message_type: String,
    pub slot_number: u64,
}
```

Example:
```json
{
  "amount": "1000000000",
  "chain_id": 900,
  "data": "",
  "event": "MessageTransaction",
  "l1_pubkey": "BdhpXtonNKnVKpEK7iSzZvVU1gKSWtMjUaTuQZ4rvJkS",
  "l1_token": "11111111111111111111111111111111",
  "l2_token": "0x4ed7c70F96B99c776995fB64377f0d4aB3B0e1C1",
  "message_type": "Withdraw",
  "nonce": 11,
  "slot_number": 403666786,
  "twine_address": "0xf39Fd6e51aad88F6F4ce6aB8827279cffFb92266"
}
```

### 2. CommitedBatch

Emitted after a batch is successfully committed.

```rust
let event = json!({
  "event": "CommitedBatch",
  "batch_number": u64,
  "chain_id": u64,
  "batch_hash": [u8;32],
  "slot_number": u64
}).to_string();

msg!(&event);
```

### 3. FinalizedBatch

Emitted after a batch is successfully finalized.

```rust
let event = json!({
  "event": "FinalizedBatch",
  "batch_number": u64,
  "messages_handled_on_twine": u64,    
  "chain_id": u64,
  "batch_hash": [u8;32],
  "slot_number": u64
}).to_string();

msg!(&event);
```

### 4. BatchCommitmentAndFinalizationSuccessful

Emitted after a batch is committed and finalized in a single transaction directly.

```rust
let event = json!({
  "event": "BatchCommitmentAndFinalizationSuccessful",
  "messages_handled_on_twine": u64,
  "batch_number": u64,
  "chain_id": u64,
  "batch_hash": [u8;32],
  "slot_number": u64
}).to_string();

msg!(&event);
```

## Tokens Gateway Events

### 1. NativeRefundSuccessful

Emitted after a successful refund of sol.

```rust
let event = json!({
  "event": "NativeRefundSuccessful",
  "nonce": u64,
  "l1_receiver_address": String,
  "l1_token_address": String,
  "chain_id": u64,
  "amount": u64,
  "slot_number": u64 
}).to_string();

msg!(&event);
```

### 2. NativeForcedWithdrawalSuccessful

Emitted after a forced withdrawal of native token executed successfully.

```rust
let event = json!({
  "event": "NativeForcedWithdrawalSuccessful",
  "nonce": u64,
  "l1_receiver_address": String,
  "l1_token_address": String,
  "chain_id": u64,
  "amount": u64,
  "slot_number": u64
}).to_string();

msg!(&event);
```

### 3. SplForcedL2WithdrawExecuted

Emitted after a forced withdrawal of spl token executed successfully.

```rust
let event = json!({
  "event": "SplForcedL2WithdrawExecuted",
  "nonce": u64,
  "l1_token": String,
  "l2_token": String,
  "l1_receiver_address": String,
  "chain_id": u64,
  "amount": u64,
  "slot_number": u64
}).to_string();

msg!(&event);
```