# BlockTrack Supply Chain Verification Protocol (V2.0)

![License](https://img.shields.io/badge/license-MIT-blue.svg)
![Version](https://img.shields.io/badge/version-2.0-green.svg)
![Status](https://img.shields.io/badge/status-Active-success.svg)

> **Trustless transparency for real-world products.**

## 📖 Overview

BlockTrack is a dual-layer anti-counterfeit protocol combining physical seals with cryptographic verification. Standard QR codes can be copied. **BlockTrack cannot.**

### Why It Exists

| 🔴 The Problem | 🟢 The Solution: Dual-Key Identity |
| :--- | :--- |
| **QR codes are easily cloned.** | Each product receives two keys: |
| Copy genuine code → paste on fake product → system fails. | 1. **Public ID** (Printed on packaging)<br>2. **Private Key** (Hidden under scratch-off seal) |
| Consumers can't verify authenticity. | **Trust the math, not the manufacturer.** |

---

## 🔐 Security Model

1.  **Physical Lock:** Private Key protected by a scratch-off layer.
2.  **Digital Lock:** Once the Private Key is claimed, the product becomes **CONSUMED** on-chain.
3.  **Counterfeit Trap:** Any re-scan of a consumed ID triggers a **🔴 "Product Has Been Claimed Before"** warning.

---

## 🛠 Tech Stack

**Frontend**
* React, Vite, Tailwind CSS
* Axios, Lucide Icons, Native Camera API
* **Modes:** Public Verify / Private Claim

**Backend**
* Node.js, Express.js
---

## 🚀 System Flow

1.  **Minting:** Manufacturer mints asset → Gets Public QR + Sealed Private Key.
2.  **Logistics:** Simulation of flow (Factory → Truck → Pharmacy).
3.  **Verify (Consumer):** Scans Public ID → Sees **VERIFIED** + Supply chain timeline.
4.  **Claim (Consumer):** Scratches seal & enters Private Key → Backend verifies → Status = **CONSUMED**.
5.  **Trap:** Re-scanning this ID now triggers a red counterfeit warning.

---

## ⚙️ Setup and Configuration

Follow this guide to set up the project locally.

### Prerequisites

* **[Node.js](https://nodejs.org/)** (Version 16.20.1 or higher)

### 1. Clone the Repository

```bash
git clone [https://github.com/pushkarthisside/blocktrack-bitmin](https://github.com/pushkarthisside/blocktrack-bitmin)
cd blocktrack-bitmin
