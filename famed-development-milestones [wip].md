## Famed Development Roadmap 


This document is intended for a non-technical audience. It represents the most **recent state of the development roadmap and is still subject to change** as external dependencies are also still changing.

The diagrams  reflect the current state but may also change at a later point in time. 

Please note that further technical details on the individual components, the security concept, and the data protection concept are provided at a later date.


## 0: Systems analysis, requirements definition and design (03/21 - 09/21)
## I: System development (09/21 - 09/22)

### dApp protototype components (09/21 - 06/22)

  #### i)  “Walls of fame” Web App + Github/Web (09/21 - 03/22) (✅)
  
    - Github App:  https://github.com/morphysm/famed-github-backend (02/22 - 03/22) (✅)
    - Wall of fame:  https://www.famed.morphysm.com/teams/morphysm/famed-script-test-dev (01/22 - 03/22) (✅)

  #### ii) Migration tool (from Hackerone, Bugcrowd, etc.) (03/22) (✅)
  
     - CSV to github famed issues https://github.com/morphysm/famed-import-script 

  #### iii) Github App Memory Encryption + ASLR (03/22 - 06/22) 

  #### iv) Security Audit + codebase hardening (06/22 - 09/22) 

### Web dApp (5/22 - 8/22)

  #### i) Login with Wallet connect/metamask + Github to lower spam (5/22- 7/22)
    - config option to require tokens in user's wallet to submit bugs 

  #### ii) Bug submission form: fat client implementation with e2e encryption (5/22- 7/22)
  - requires a side channel to securely verify the organization's public key 
  - See, for instance EF's current bug submission form: https://forms.gle/Gnh4gzGh66Yc3V7G8
  
  #### iii) Decentralized, privacy preserving bounties** - zero knowledge commits/claims (5/22 - 8/22)

  Instead of requesting addresses for bounties over a public or private channel, many users would prefer not to disclose their public keys. The following components will adress this problem: 
  - deploy an interface where contributors can generate a message ('commitment') 
  - contributors can send commitments over a public channel (their address remains private) 
  - commitments can be submitted to a contract storing a merkle tree of all commitments. 
  - Later contributors can claim their portion NFTs/bounties by providing a zero-knowledge proof that they belong in the Merkle tree. 
  
  Claiming tokens in this manner mixes them with all other contributors, protecting their anonymity.

  ##### iv) Interface for projects to customize Github App** with NFT badges/rewards (7/22 - 9/22)

### To be specified: 
##### II: Famed Protocol Handbook (7/22 - 9/22)
##### III: Continuous System Integration and testing, System Acceptance, installation, deployment (04/22 - 12/22)
##### IV: System Improvements & Maintenance (04/22 - 12/22)
#### VI: System Improvements & Maintenance (01/22 - 02/23)


## V: System Evaluation: (03/22 - 02/23)
    - “The Motherboard” Metrics/Analytics Dashboard, to compare security work among teams/projects (03/22 - 07/22)
    

## VII: System Scaling: Automate all the things (9/22 - 02/23)
Multichannel conversational Triage automator 9/22 - 02/23


Ships as part of the Github App which organizations can selfhost , One App per Organization/Repoe 
- decentralized Report submissions
	
Chatbot Plugin for different messengers with local; self contained, containerized AI 

Form from Web Interface as a messenger conversation for reports submitted as: 

Email
Telegram
Status.im
Discord


## VIII: System Scaling: 

### Famed reward layer2  dApp on 2023

**Currently evaluating: Zksync, Loopring, Optimism** 

### Famed as a Status Community 2023



