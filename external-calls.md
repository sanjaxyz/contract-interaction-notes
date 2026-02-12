# External Contract Calls

This document describes how one smart contract interacts with another smart contract on Ethereum.

## What Is an External Call?

An external call occurs when a smart contract invokes a function that exists in a different contract.

In this interaction:
- The calling contract initiates the request
- The target contract executes its logic
- Control returns to the calling contract after execution

## High-Level Flow

1. Contract A calls a function in Contract B.
2. Contract B processes the request.
3. Contract B may modify its own state.
4. Contract B may return data to Contract A.
5. Control returns to Contract A.

## State Changes

If Contract B modifies its state during execution, those changes become part of the blockchain state when the transaction is finalized.

## Events

If Contract B emits events, those events are recorded in the transaction logs and can be observed by external applications.
