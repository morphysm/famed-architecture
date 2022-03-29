# FAMED PROTOCOL ARCHITECTURE

This document is intended for a technical audience. It represents the most **recent state of the architecture and is still subject to change** as external dependencies are also still changing.

The diagrams  reflect the current state but may also change at a later point in time. 

Please note that further technical details on the individual components, the security concept, and the data protection concept are provided at a later date.

We assume a close association of a crypto-wallet and its user, thus, equate the wallet (phone, app) and the person using it (person, user, individual) and use these terms interchangeably.

![Famed protocol Components](images/solution_architecture/Components.png "Famed protocol Components")

## TABLE OF CONTENTS

1. [INTRODUCTION](#introduction)
2. [GITHUB APP](#Github-app)
3. [WALL OF FAME BOARDS](#wall-of-fame-boards)
4. [TOKENIZATION LAYER-2](#tokenization-layer-2)
5. [RUNTIME ENVIRONMENT (HOSTING)](#runtime-environment-hosting)
   1. [Bandwidth estimations](#bandwidth-estimations)
5. [CROSS-DAO INTEROPERABILITY](#cross-dao-interoperability)
6. [LIMITATIONS](#limitations)
7. [PRIVACY-PRESERVING DATA DONATION](#privacy-preserving-data-donation)

## INTRODUCTION

This document describes an overview of famed, a decentralised social protocol for vulnerability coordination, bug bounties, responsible disclosure and governance for everyone involved in the life cycle of vulnerabilities. Famed aims to research&develop incentives for balanced defaults for tradeoffs for the objectives of product, security and development teams in a DAO.


Some [wip] design goals of the famed are:

- Continuous, asynchronous security improvements which are non-blocking to Development, Product, UX and Marketing teams of a DAO 
- Measurable, Testing driven 
- Incentives & Visibility for all contributors to a projects security, especially for reporting and fixing vulnerabilities


| ![Figure 1: High-level architecture overview](images/protocol_architecture/high_level_architecture.svg "Figure 1: High-level architecture overview") |
|:--:|

| **Figure 1: High-level architecture overview**|


## GITHUB APP

| ![Figure 7: Actors in the system, including external parties ](images/protocol_architecture/actors_in_the_system.svg "Figure 7: Actors in the system, including external parties ") |
|:--:|
| **Figure 7: Actors in the system, including external parties **|

## TOKENIZATION LAYER-2

## WALL OF FAME BOARDS

The Famed boards allow security efforts by an organization, teams and individual contributors to be visualized, publicly recognized and incentivized as a CVE based score. The board aggregates findings together with vulnerability data aggregated external sources (vuluntary reports, bug bounty programs and audits). 
The boards compresses incentives, roles and reward heuristics to increase measurability, visibility and abstract complexity of security work. Some notions and definitions are given in this doc, but all metrics are elidgible to organizational preferences and change.
The functional scope of the famed board applications is defined in the corresponding [scoping document](scoping_document.md). The boards are developed for desktop and mobile browsers. 

### Vulnerability Buckets

### Reward Calculation

### Data Transfer and Data Processing

## RUNTIME ENVIRONMENT (HOSTING)

### Bandwidth Estimations

## CROSS DAO INTEROPERABILITY

## LIMITATIONS

