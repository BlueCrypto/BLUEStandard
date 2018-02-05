# Infinite Minting Prevention

## Preamble
    BIP: 1
    Author: Uni Banker, <uni@etherblue.org)
    Status: Complete
    Created: 2018-02-01

## Simple Summary
"If you can't explain it simply, you don't understand it well enough." Provide a simplified and layman-accessible explanation of the BIP.

## Abstract
Token creators can optionally choose to opt-in to giving themeselves or others the ability to mint tokens. We believe this should be limited in time, scope, or quantity. Whether intentional or accidental we should introduce a fuzz-testing layer to the EVM that can try random inputs until it is determined that the total supply may be increased or decreased through smart contract interactions.

## Motivation
Currently, there is no clear way for the average investor to know that a token may increase or decrease it's supply. The only way for investors to understand the different is to read and understand the source code of every item they trade. Not only is this time-consuming for the skilled investor, it is impossible for the novice investor. As a result there is a large quantity of blind trading happening, where investors have no idea whether or not their tokens are backed by a constant supply, or a fixed-rate fluctuating supply

## Implementation Details
It is trivial to implement fuzz testing on an ethereum side-chain and simply try random input parameters, and then calculate the total supply to measure whether or not any set of inputs changes the total supply. If it does, as a matter of standard metadata output, we include this as a boolean flag in the `tokenMeta.json` in BLUE Geth.

## Copyright
Copyright and related rights waived via [CC0](https://creativecommons.org/publicdomain/zero/1.0/).
