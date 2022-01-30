# Overview

Purpose of this program is allow  transaction to fail if thumbstone already exists.

## Example

You transfer SPL tokens to account. 
But transactions fails with unknown state.
Next time you send same transaction, and transfer same amount again. Making double pay.
If to prefix transaction with thumbstone instruction, than transaction will fail before transfer if thumbstone detected.

## Instructions

### CreateThumbstone

Creates emtpy thumbstone account.

Account address is PDA derived from arbitrary 32 bit byte stream and from account.

Amount of SOL passed to account should be enough to it exists for period of time passed as input.
Examples, enough seconds to fit 24 hours.

## Alternative

Could may root Event account. Make it an owner. Any thumbstone is derived from that event account too.
Owner of event account can 

## Implementation

- Rust instructions documentation
- Positive end to end test
- TS SDK
- Rust CLI exampl


## Price

Will 4 SOL for this program.
