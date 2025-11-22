BlockTrack
Supply Chain Verification Protocol (V2.0)

Trustless transparency for real-world products.

Overview

BlockTrack is a dual-layer anti-counterfeit protocol combining physical seals with cryptographic verification.
Standard QR codes can be copied. BlockTrack cannot.

Why It Exists
Problem

QR codes are easily cloned.

Copy genuine code → paste on fake product → system fails.

Solution: Dual-Key Identity

Each product receives:

Public ID — printed on packaging

Private Key — hidden under scratch-off seal

Once the private key is claimed, the product becomes CONSUMED on-chain.
Any later scans expose counterfeits instantly.
Trust the math, not the manufacturer.

Security Model

Physical Lock: Private Key protected by scratch layer.

Digital Lock: Claimed Private Key permanently marks the asset as consumed.

Counterfeit Trap: Re-scan of consumed ID → “Product Has Been Claimed Before”.

Tech Stack

Frontend: React, Vite, Tailwind, Axios, Lucide Icons, Native Camera API
Backend: Node.js, Express, SHA-256 Crypto, In-memory append-only ledger

What’s Inside
Backend

POST /mint – create Public + Private keys

GET /scan/:id – check asset status + history

POST /claim – verify private key + mark consumed

Frontend

Dark SaaS UI

Full-screen QR Scanner

Supply-chain timeline visualizer

Modes: Public Verify / Private Claim

System Flow

Manufacturer mints asset → gets Public QR + sealed Private Key

Logistics flow simulated (Factory → Truck → Pharmacy)

Consumer Verify scans Public ID → sees VERIFIED + timeline

Consumer Claim enters Private Key → backend verifies → status = CONSUMED

Re-scan triggers red counterfeit warning

Folder Structure
blocktrack-bitmin/
├── backend/
│   ├── server.js
│   ├── routes/
│   ├── controllers/
│   ├── utils/
│   └── package.json
└── frontend/
    ├── src/
    ├── public/
    ├── package.json
    └── vite.config.js

Run Locally
Clone
git clone https://github.com/pushkarthisside/blocktrack-bitmin
cd blocktrack-bitmin

Backend
cd backend
npm install
node server.js


Backend runs at: http://localhost:5000

Frontend
cd ../frontend
npm install
npm run dev


Frontend runs at: http://localhost:5173

License

MIT License — open, simple, and permissive.
