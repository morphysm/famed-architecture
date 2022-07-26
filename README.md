
# FAMED PROTOCOL ARCHITECTURE

This document is intended for a technical audience. It represents the most **recent state of the architecture and is still subject to change** as external dependencies are also still changing.

The diagrams  reflect the current state but may also change at a later point in time. 

Please note that further technical details on the individual components, the security concept, and the data protection concept are provided at a later date.

![Famed protocol Components](images/solution_architecture/Components.png "Famed protocol Components")

## TABLE OF CONTENTS

1. [INTRODUCTION](#introduction)
2. [ACCOUNTS](#accounts)
3. [WALL OF FAME BOARDS](#wall-of-fame-boards)
4. [GITHUB APP](#github-app)
5. [RESPONSIBLE DISCLOSURE CHANNELS](#responsible-disclosure-channels)
   1. [Wep DApp](#web-dapp)
   2. [Messengers ](#messengers)  
6. [INCENTIVES AND REWARDS](#incentives-and-rewards)
7. [LAYER 2](#layer-2)
8. [RUNTIME ENVIRONMENT (HOSTING)](#runtime-environment-hosting)
   1. [Bandwidth estimations](#bandwidth-estimations)
9. [CROSS-DAO INTEROPERABILITY](#cross-dao-interoperability)
10. [LIMITATIONS](#limitations)


## INTRODUCTION

This document describes an overview of famed, a decentralised social protocol for vulnerability coordination, bug bounties, responsible disclosure and governance for everyone involved in the life cycle of vulnerabilities. Famed aims to research&develop incentives for balanced defaults for tradeoffs between the objectives of product, security and development teams in a DAO.


Some [wip] design goals of the famed are:

- Continuous, asynchronous security improvements which are non-blocking to Development, Product, UX and Marketing teams of a DAO 
- Measurable, Testing driven 
- Incentives & Visibility for all contributors to a projects security, especially for reporting and fixing vulnerabilities


| ![Figure 1: High-level architecture overview](images/protocol_architecture/high_level_architecture.svg "Figure 1: High-level architecture overview") |
|:--:|

| **Figure 1: High-level architecture overview**|

## ACCOUNTS

We assume a close association of a crypto-wallet and its user, thus, equate the wallet (phone, app) and the person using it (person, user, individual) and use these terms interchangeably.

<!--  Loopring: Metamask, Wallet connect -->
<!-- Loopring: https://docs.loopring.io/en/basics/key_mgmt.html -->

## WALL OF FAME BOARDS

The Famed boards allow security efforts by an organization, teams and individual contributors to be visualized, publicly recognized and incentivized as a CVE based score. The board aggregates findings together with vulnerability data aggregated external sources (vuluntary reports, bug bounty programs and audits). 
The boards compress incentives, roles and reward heuristics to increase measurability, visibility and abstract complexity of security work. Some notions and definitions are given in this doc, but all metrics are elidgible to organizational preferences and change.
The functional scope of the famed board applications is defined in the corresponding [scoping document](scoping_document.md). The boards are developed for desktop and mobile browsers. 

## GITHUB APP

### Famed GitHub App
The GitHub app faciliates developer driven triage of vulnerability reports in private or public GitHub repositories. 
If the GitHub App is installed in a Repo with Issue/Pull Request and Webhook permissions, GitHub sends an Event to the Famed BFF using the registered Webhook each time a Issue is changes. The Famed BFF filters the events for changes which are relevant. If a relevant change occures a new Comment is posted or a current comment is updated via the GitHub API.

### Wall of Fame Data Flow
![Famed Flow](https://user-images.githubusercontent.com/11260050/162227373-3010ac5d-3f13-4d38-8e86-471d800404fd.png)

### Wall of Fame BFF and Frontend
The Walls of Fame frontend requests the list of contributors from the Famed BFF (Backend for Frontend), when a user vistis the Walls of Fame website. The Fame BFF then calls the Github API and requests all Github Issues of the repo. The Github Issues are filtered by qualifying properties, closed and labeled “Fame”. For each qualifying issue the Github Issue Events are requested from the Github API. Based on the events and the issue information, a list of contributors is generated and populated with information about performance and rewards. The list is then returned to the Fame Board frontend and displayed to the user.


## RESPONSIBLE DISCLOSURE CHANNELS

### Web DApp

### Messengers 

| ![Figure 7: Actors in the system, including external parties ](images/protocol_architecture/actors_in_the_system.svg "Figure 7: Actors in the system, including external parties ") |
|:--:|
| **Figure 7: Actors in the system, including external parties **|


## INCENTIVES AND REWARDS

### Rewards
Bug bounties paid out by organizations using the Famed boards can be directly processed via Famed. Here, we especially care about a secure and privacy-preserving channel. (See Layer 2)


### Incentive Model
Bug bounty programs set incentives for security researchers to hunt and disclose bugs by rewarding them with compensation. Leaderboards add a reward of recognition.
Organizations that use a Famed board can integrate several further incentive schemes to promote security work beyond the red team. We are currently thinking of the following extensions:

1. Vouch and invite: promote mentorship and referral among security researchers 
   Rewards earned with famed can be staked to invite new members to the famed DAO. If reffered members earn famed rewards, the referraing member gets a share of the rewards. Once economically well calibrated, this incentive promotes and rewards mentorship of high performing security researchers to help tackle the urgent talent shortage in (web3)-security. 
   
2. Famed Governance and Services 
   With current web3 platforms, legal risks and concerns of security researchers often remain unadressed. While tech and legal interdependencies grow rapidly, often not even basic safe harbor agreements protecting the researchers are in place when security testing engagements are taking place. The famed DAO offers security researchers a safe space to conduct security research and protects its members from potential legal repercussions. 
   
4. Rewards for security engineers/blue teamers for fast and clean fixes of reported vulnerabilities
5. Rewards for security liasons for well managing bug bounty programs
6. Increase cooperation within teams via peer pressure mechanisms

Rewards can be in the form of tokenized compensation or in the form of NFTs batches.


## LAYER 2 

Famed pays out bug bounties and other rewards through ZK-Rollups. This ensures
- high privacy through zero-knowledge
- low fees and fast payouts via the scalability advantage of rollups

Until this technology matures, we opt for Optimism since it is EVM-compatible. This allows us to migrate to a ZK-EVM-compatible rollup at a later stage.
An EVM-compatible solution is in general prefered as it allows high flexibility around the use of other tokens as well as the future integrations of a Famed token. 

<!--  Loopring -->
<!--  zksync -->
<!--  optimism -->


### Vulnerability Buckets

### Reward Calculation

### Data Transfer and Data Processing

## RUNTIME ENVIRONMENT (HOSTING)

### Bandwidth Estimations

## CROSS DAO INTEROPERABILITY

## LIMITATIONS

<!--  FAMED TOKEN MODEL -->
