# Internal Contract Calls

This document describes how functions interact within the same smart contract.

## What Is an Internal Call?

An internal call occurs when a function within a contract invokes another function defined in the same contract.

Unlike external calls, internal calls do not involve switching to a different contract address.

## High-Level Flow

1. A function in the contract is executed.
2. That function invokes another function defined in the same contract.
3. The called function executes as part of the same execution context.
4. Control returns to the original function.

## Execution Context

Internal calls share:
- The same contract state
- The same transaction context
- The same address

No external message call is made to another contract.

## State Changes

Any state updates made during internal calls are applied to the same contract and become part of the blockchain state when the transaction is finalized.
