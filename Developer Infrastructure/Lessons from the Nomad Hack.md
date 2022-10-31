# Lessons from the Nomad Hack

Status: Draft 📝  
Speaker(s): [Odysseas](https://app.devcon.org/speakers/WB8KEZ)    
Date: Day 4 - Oct 14, 2022  
Skill level: Intermediate   
Track: Developer Infrastructure  
Keywords: Solidity, Foundry, cross-chain applications (xapps)
Video link: https://archive.devcon.org/archive/watch/6/lessons-from-the-nomad-hack/?tab=YouTube  
Slides link:  
> Disclaimer: Odysseas is not there on behalf of [Illusory], and the views he expresses in his talk are his own and do not reflect those of the company. There was no Q&A as it is an ongoing investigation.

# What is Nomad?
Nomad is an optimistic protocol for interoperability. Allowing applications to **meaningfully** react...

It supports arbitrary messages between domains.

## Life cycle of a message in Nomad
    >Dispatch message 
    > Relay Root 
    {optimistic window}
    > Prove Message 
    > Process Message

## How bridges work?
Sending chain
Ethereum > Evmos
Weth madWeth

# How did the incident happen?


## Nomad Now
Restarting the protocol (easy)
Restarting the bridge (hard)

Principles:

# What suggestions do we have for protocols

## Test
Unit Tests
Property-based Tests
Integrations Tests
Forking Tests
Invariant Tests

Static Analysis Tools
Storage 

## Observe

### Web2 tactics
Google SRE handbook (https://landing.google.com/sre/sre-book/toc/index.html)

### Hereustic and Invariant Alerts

## Engage
Explicit ownership
Explicit outcomes
Gameday. Gameday. Gameday.

## Communicate

Talk with legal do not talk to users, think what users want.

Honesty, do not sugarcoat.
Pre-approved messaging...

### First days after the incident
