# Famed Systems Engineering Roadmap 22´


This document is intended for a non-technical audience. It represents the most **recent state of the development roadmap and is still subject to change** as external dependencies are also still changing.

The diagrams  reflect the current state but may also change at a later point in time. 

Please note that further technical details on the individual components, the security concept, and the data protection concept are provided at a later date.


## 0: Systems Analysis, Requirements Definition and Design (03/21 - 09/21)
## I: System Development (09/21 - 09/22)

### A) dApp Protototype Components (09/21 - 06/22)

   1. **“Walls of Fame”** Web App + GitHub/Web (09/21 - 03/22) 
    	1. GitHub App developer driven triage tool:  https://github.com/morphysm/famed-github-backend (02/22 - 03/22
    		- Data at rest: databaseless, static, fat client dApp 
    	3. Example "Wall of Fame":  https://www.famed.morphysm.com/teams/morphysm/famed-script-test-dev (01/22 - 03/22) 

   2. **Issue Migration Script** (from Hackerone, Bugcrowd, etc.) (03/22)
	1. e.g. CSV to GitHub famed issues https://github.com/morphysm/famed-import-script
   4. **GitHub App Memory Encryption** + ASLR (05/22 - 09/22) 
   5. **Security Audit** + codebase hardening (08/22 - 09/22) 

### B) Web dApp (5/22 - 9/22)
1. **Login with WalletConnect/Metamask** + GitHub to lower spam (5/22- 8/22)
	1. Config option to require tokens in user's wallet to submit bugs 
2. **Conversational Vulnerability Submission Form**: fat client implementation  (5/22- 8/22)
	1. Supports databaseless operation: Ephemereal Triage to Messenger + GitHub 	
		1. Data at rest: databaseless, static, fat client dApp 
		2. Data ins transit: TLS + e2e encrypted, organization's public key is retrieved from ENS 
		3. Data in use, memory encryption, see A.3
3.  **Decentralized, Privacy Preserving Bounties - Zero Knowledge Commits/Claims** (5/22 - 8/22)

- Many users would prefer not to disclose their public keys. Claiming tokens in this manner mixes them with all other contributors, protecting their anonymity: 
  
  1. Deploy an interface where contributors can generate a message ('commitment') 
  2. Contributors can send commitments over a public channel (their address remains private) 
  3. Commitments can be submitted to a contract storing a merkle tree of all commitments. 
  4. Later contributors can claim their portion NFTs/bounties by providing a zero-knowledge proof that they belong in the Merkle tree. 

4. **NFT Badges/Rewards**: Customization interface for GitHub App  (7/22 - 9/22)
 
## II: Famed Protocol Handbook (7/22 - 9/22)
- Documentation of the Famed social protocol
- Reward specification 
- Step by step guide for the respective roles  

## III: Continuous System Integration and Testing, System Acceptance, Installation, Deployment (06/22 - 12/22)
Sourcing and onboarding of security champions 
- Facilitate complete vulnerability lifecycles 
- Some components might not be finalized and need to replaced with traditional stack (e.g. email/messenger, manual NFT deployment)
- Payout rewards 

## IV: System Improvements & Maintenance (01/22 - 02/23)

## V: System Evaluation: (01/22 - 03/23)

## VI: System Scaling: Automate All the Things (9/22 - 02/23)
1. Multichannel conversational triage automator (9/22 - 02/23)

	- Ships as part of the GitHub App which organizations can selfhost on their exisiting channels for decentralized report submissions

2. Chatbot plugin for different messengers with local; self contained, containerized AI 
Messenger in scope are: 
	- Email (gpg encrypted)
	- Status messenger 
	- Telegram
	- Discord
	- Slack 

## VII: System Scaling: 

1. Famed reward layer2  dApp in 2023
2. Famed as a Status Community 2023
