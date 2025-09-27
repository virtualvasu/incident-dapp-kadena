# Incident Management DApp on Kadena

A decentralized application (DApp) for professional incident reporting with blockchain verification, built on Kadena EVM testnet.

## 🌐 Deployment Details

**Test application for road incident reporting on Kadena testnet: chain@20**

- **Contract Address:** `0x3ab0dCEF4F1A3d005B68F2527F96C47FAb656BAC`
- **Block Explorer:** [View on Chainweb Explorer](https://chain-20.evm-testnet-blockscout.chainweb.com/address/0x3ab0dCEF4F1A3d005B68F2527F96C47FAb656BAC)
- **Network:** Kadena EVM Testnet (Chain 20)

## 🔧 Smart Contract Functions

The `IncidentManager` contract provides the following functionality:

### Core Functions
- **`reportIncident(string _description)`** - Submit a new incident report to the blockchain
- **`getIncident(uint _id)`** - Retrieve incident details by ID
- **`incidentCounter`** - Get the total number of reported incidents

### Data Structure
Each incident contains:
- **ID:** Unique incident identifier
- **Description:** IPFS URL containing the full incident report
- **Reporter:** Ethereum address of the person who submitted the report
- **Timestamp:** Block timestamp when the incident was recorded

## 🚀 DApp Workflow

This DApp follows a comprehensive 5-step process to ensure professional incident reporting with immutable blockchain storage:

### Step 1: Incident Details Collection
- **Input Fields:**
  - Location of the incident
  - Detailed description of what happened
  - Checkbox for elderly person involvement
  - Optional photo/evidence upload
- **Validation:** All required fields are validated before proceeding

### Step 2: Professional PDF Generation
- **Automated Report Creation:**
  - Generates a professional-grade incident report using PDF-lib
  - Includes company branding and formatting
  - Contains all incident details, timestamps, and report ID
  - Automatically adds evidence photos as a second page if provided
- **Report Features:**
  - Professional layout with headers and footers
  - Unique report ID generation (RPT-XXXXXX format)
  - Proper formatting for legal and insurance purposes
  - Metadata embedding for document verification

### Step 3: Decentralized Storage Upload
- **Web3.Storage Integration:**
  - Uploads the generated PDF to IPFS via Storacha (Web3.Storage)
  - Returns a Content Identifier (CID) for permanent storage
  - Files are stored on the Filecoin network for long-term preservation
- **Benefits:**
  - Immutable storage - files cannot be altered
  - Decentralized - no single point of failure
  - Permanent - files persist indefinitely

### Step 4: Blockchain Submission
- **Smart Contract Interaction:**
  - Connects to user's MetaMask wallet
  - Submits the IPFS CID to the IncidentManager contract
  - Records the incident permanently on Kadena blockchain
- **Transaction Details:**
  - Gas fees paid by the reporter
  - Immutable record with timestamp and reporter address
  - Generates unique incident ID for future reference

### Step 5: Completion & Verification
- **Success Summary:**
  - Displays all transaction details (incident ID, block number, tx hash)
  - Provides links to view the report on IPFS
  - Shows blockchain explorer link for verification
- **Record Keeping:**
  - Users can bookmark the incident ID for future reference
  - All data is permanently accessible via blockchain and IPFS

## 🎯 Key Benefits

### For Users:
- **Professional Reporting:** Automated PDF generation with proper formatting
- **Permanent Records:** Immutable storage on blockchain and IPFS
- **Verifiable Data:** Cryptographic proof of when and by whom reports were submitted
- **Easy Access:** Simple web interface, no technical blockchain knowledge required

### For Organizations:
- **Audit Trail:** Complete transparency and traceability of all incidents
- **Compliance Ready:** Professional reports suitable for insurance and legal purposes
- **Cost Effective:** Minimal gas fees, no centralized server costs
- **Scalable:** Decentralized infrastructure handles unlimited reports

## 🔒 Security & Trust

1. **Immutable Records:** Once submitted, incident reports cannot be altered or deleted
2. **Cryptographic Verification:** All submissions are cryptographically signed by the reporter
3. **Decentralized Storage:** No single point of failure or data loss risk
4. **Transparent Process:** All transactions are publicly verifiable on the blockchain

## 🌟 Technical Architecture

- **Frontend:** React + TypeScript + Vite
- **Smart Contract:** Solidity on Kadena EVM
- **Storage:** IPFS via Web3.Storage (Storacha)
- **Wallet Integration:** MetaMask for transaction signing
- **PDF Generation:** PDF-lib for professional document creation

This comprehensive workflow ensures that incident reporting is professional, secure, permanent, and verifiable while maintaining ease of use for end users.