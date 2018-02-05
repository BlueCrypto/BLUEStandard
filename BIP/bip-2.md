# Smart contract locking

## Preamble
    BIP: 2
    Author: Alex, @ATotallySmartPerson
    Status: Complete
    Created: 2018-02-01

## Simple Summary
Smart Contract Locking gives too much centralized power, and is a security nightmare

## Abstract
Token pause function is gaining in popularity. Its abusable, on top of being a security nightmare.

## Motivation
Bring more security to a function that most smart contracts don't need anyway.
In the current implementation a token owner can send to an exchange and pause everyone's ability to dump it.
Before anyone knows whats happening he pumped the price(without other people being able to sell) and dumped.

In case of a lost-private key. A hacker can pause all trades and effectively kill a billion dollar token. 
There should be no central power in tokens. Even in utility ones. This brings too many attack vectors.

## Implementation Details
Rules for pausing a smart contract :

A clearly stated reason why it cannot be done by a burning smart-contract in case of main-net swaps
In the case of a clear reason - implement a multi-signature between a trusted 3rd party(lawyer) and 2+ developers to pause the token.

## Copyright
Copyright and related rights waived via [CC0](https://creativecommons.org/publicdomain/zero/1.0/).
