# Don't count ADA in Spending Scripts for vote (DRep Scripts still supported)

## Abstract

This proposal suggests removing the lovelaces that are under the control of a spending validator (smart contract) from the counts of the voting power delegated to a DRep.

This is proposed as a security measure against potential attacks at the governance structure of Cardano (we only get to screw up once), and to ensure a better representation of what is the sentiment of the original owners of the lovelaces (ADA).

## Motivation

DeFi platforms use spending scripts (smart contracts) to manage liquidity for many useful applications.

The liquidity providers are to be considered the owners of the voting power, however, while locked on the scripts, the lovelaces are under the effective control of the protocol (via DAO or even multisigs).

These protocols then vote using lovelaces that are not to be considered theirs, based on their will (either via external DAO token, or directly selling the votes), that doesn't necessarily meet the will of the original owners.

Under the proposed constitution, this action would be unconstitutional according to Article III section 3.

Additionally, this ability to buy votes (with significant leverage), dangerously threatens the stability of the governance structure of Cardano, to the point where an attacker could gain control of all the 3 arms of the governance body.

To prevent this catastrophic scenario, the suggested change is:

lovelaces on UTxOs whose address has a script as payment credentials are not eligible for votes.

This wording is carefully weighted to target specifically spending scripts (that do manage other's liquidity), while maintaining the possibility of creating DRep Scripts (that would still be able to vote, after explicit on-chain delegation).

## Rationale

By removing lovelaces managed by a smart contract from the final votes, we effectively neutralize the possibility of buying votes, in order to better reflect the sentiment of the ada owners that are rightfully eligible to vote.
