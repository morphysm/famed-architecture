# Famed Systems Engineering Roadmap 22´


This document is intended for a non-technical audience. It represents the most **recent state of the development roadmap and is still subject to change** as external dependencies are also still changing.

The diagrams  reflect the current state but may also change at a later point in time. 

Please note that further technical details on the individual components, the security concept, and the data protection concept are provided at a later date.


## 0: Systems analysis, requirements definition and design (03/21 - 09/21)
## I: System development (09/21 - 09/22)

### A) dApp protototype components (09/21 - 06/22)

   1. **“Walls of fame”** Web App + Github/Web (09/21 - 03/22) 
    	1. Github App developer driven triage tool:  https://github.com/morphysm/famed-github-backend (02/22 - 03/22
    		- Data at rest: databaseless, static, fat client dApp 
    	3. Example Wall of fame:  https://www.famed.morphysm.com/teams/morphysm/famed-script-test-dev (01/22 - 03/22) 

   2. **Issue migration script** (from Hackerone, Bugcrowd, etc.) (03/22)
	1. e.g. CSV to github famed issues https://github.com/morphysm/famed-import-script
   4. **Github App Memory Encryption** + ASLR (05/22 - 09/22) 
   5. **Security Audit** + codebase hardening (08/22 - 09/22) 

### B) Web dApp (5/22 - 9/22)
1. **Login with Wallet connect/metamask** + Github to lower spam (5/22- 8/22)
	1. config option to require tokens in user's wallet to submit bugs 
2. **Conversational vulnerability submission form**: fat client implementation  (5/22- 8/22)
	1. supports databaseless operation: Ephemereal Triage to Messenger + Github 	
		1. Data at rest: databaseless, static, fat client dApp 
		2. Data ins transit: TLS + e2e encrypted, organization's public key is retrieved from ENS 
		3. Data in use, memory encryption, see A.3
3.  **Decentralized, privacy preserving bounties - zero knowledge commits/claims** (5/22 - 8/22)

- - Many users would prefer not to disclose their public keys. Claiming tokens in this manner mixes them with all other contributors, protecting their anonymity: 
  
  1. deploy an interface where contributors can generate a message ('commitment') 
  2. contributors can send commitments over a public channel (their address remains private) 
  3. commitments can be submitted to a contract storing a merkle tree of all commitments. 
  4. Later contributors can claim their portion NFTs/bounties by providing a zero-knowledge proof that they belong in the Merkle tree. 

4. **NFT badges/rewards**: Customization interface for Github App  (7/22 - 9/22)
 
## II: Famed Protocol Handbook (7/22 - 9/22)
- Documentation of the Famed social protocol
- Reward specification 
- Step by Step guide for the respective roles  

## III: Continuous System Integration and testing, System Acceptance, installation, deployment (06/22 - 12/22)
Sourcing and onboarding of security champions 
- Facilitate complete vulnerability lifecycles 
- Some components might not be finalized and need to replaced with traditional stack (e.g. Email/Messenger, manual NFT deployment)
- payout rewards 

## IV: System Improvements & Maintenance (01/22 - 02/23)

## V: System Evaluation: (01/22 - 03/23)

## VI: System Scaling: Automate all the things (9/22 - 02/23)
1. Multichannel conversational Triage automator (9/22 - 02/23)

	- Ships as part of the Github App which organizations can selfhost on their exisiting channels for decentralized Report submissions

2. Chatbot Plugin for different messengers with local; self contained, containerized AI 
Messenger in scope are: 
	- Email (gpg encrypted)
	- Status messenger 
	- Telegram
	- Discord
	- Slack 

## VII: System Scaling: 

1. Famed reward layer2  dApp in 2023
2. Famed as a Status Community 2023
