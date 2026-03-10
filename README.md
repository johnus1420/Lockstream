LockStream

A decentralized token streaming and time-locked distribution smart contract built in **Clarity** for the **Stacks blockchain**.

---

Overview

**LockStream** is a smart contract designed to manage time-based token distributions through programmable streaming schedules. It enables organizations, DAOs, and protocols to lock funds in a contract and release them gradually to recipients over a specified period.

Instead of sending large payments upfront, LockStream distributes tokens incrementally based on deterministic schedules. This ensures transparency, accountability, and predictable compensation for recipients.

LockStream provides an automated and verifiable infrastructure for vesting programs, grant payments, contributor compensation, and long-term incentive structures within the Stacks ecosystem.

---

 Problem Statement

Traditional token distribution systems often face several issues:

- Lack of transparency in vesting schedules
- Manual payment processing
- Risk of early token dumping
- Complex tracking of payout timelines
- Reliance on centralized administrators

LockStream solves these problems by:

- Locking tokens in a smart contract
- Releasing tokens automatically over time
- Providing verifiable payout schedules
- Ensuring deterministic and tamper-proof distributions
- Eliminating manual payment processes

---

 Architecture

 Built With

- **Language:** Clarity  
- **Blockchain:** Stacks  
- **Framework:** Clarinet  

 Stream Model

Each payment stream includes:

- Stream ID
- Sender address
- Recipient address
- Total token allocation
- Start timestamp
- End timestamp
- Release rate
- Amount already claimed

---

 Roles

1. Stream Creator

The entity responsible for creating token streams.

Capabilities:
- Create streaming payment schedules
- Deposit tokens for streaming
- Define lock duration and release rate

---

2. Recipient

The beneficiary of a streaming payment.

Capabilities:
- Claim available tokens
- Track streaming balance
- Verify payout schedule

---

3. Observers / Verifiers

Any user can verify:

- Stream existence
- Remaining locked tokens
- Claimable balances
- Streaming progress

---

 Streaming Lifecycle

1. Stream creator initializes a payment stream.
2. Tokens are deposited into the contract.
3. Stream begins at the specified start time.
4. Tokens gradually unlock over the defined period.
5. Recipients claim tokens periodically.
6. Stream completes once the full amount is distributed.

---

 Core Features

- Time-based token streaming  
- Programmable lock and release schedules  
- Deterministic incremental payouts  
- Secure escrow of streaming funds  
- Recipient claim functionality  
- Transparent stream tracking  
- Immutable streaming records  
- Clarinet-compatible architecture  

---

 Security Design Principles

- Deterministic release calculations
- Transparent stream state tracking
- Immutable streaming schedules
- Secure escrow of locked funds
- Minimal and auditable contract logic

---

License

MIT License

---
 Development & Testing

1. Install Clarinet

Follow the official Stacks documentation to install **Clarinet**.

2. Initialize Project

```bash
clarinet new lockstream
