# solana-proximity-sonar
Hyper-Local Real-Time Job Matching Platform powered by Solana Smart Contracts.


# 📡 Solana Proximity Job-Sonar (Core Engine - Phase 1)

> **Decentralized, Hyper-Local Real-Time Job Matching Platform powered by Solana Smart Contracts.**

---

## 💡 Overview & Core Architecture

The **Solana Proximity Job-Sonar** is an emergency and short-term job-matching protocol. It bypasses traditional recruitment bureaucracy by matching verifiably identity-checked candidates with local businesses using high-precision location signals, dynamic fee structures, and on-chain escrow locks.

---

## 🛠 Tech Stack

* **Frontend:** React / Vite (PWA), Optimized for Phantom In-App Browser & Mobile Web.
* **Proximity & Audio:** HTML5 Geolocation API + Web Audio API (50m High-Pitch Beeper).
* **Smart Contracts:** Solana Program Library (SPL), Anchor Framework (Rust), `@solana/web3.js`.
* **Data Privacy:** Local encrypted client vault for ID documents (Selective 24h Chat Disclosure).

---

## 🚀 Key Functional Modules

### 1. Dual Onboarding & Identity Vault
* **Workers (Männchen mit Tasche):** Local encrypted storage of EU-ID / Passport + Proof of Residency. Zero public database broadcast.
* **Employers (Chef mit Häuschen):** Instant automated clearance via VAT-ID / Commercial Register API.

### 2. Dynamic Proximity Header (Fee Engine)
The UI continuously calculates SOL/USDC micro-fees based on GPS proximity:
* **🟩 Green Zone (> 2 km):** Global scan & filtering. *Cost: ~0.001 USD.*
* **🟧 Orange Zone (50m – 2 km):** Direct messaging & skill verification. *Cost: ~0.05–0.10 USD.*
* **🟥 Red Zone (< 50m):** Precision area. *Cost: 0.10 USD per 50 chars | 1.00 USD for 50m Audio Beeper trigger.*

### 3. Solana Escrow & Time-Lock (Protocol Economics)
* **Match Stake:** Both parties lock **$5.00 USD (in SOL/USDC)** upon deal initiation.
* **Time-Lock Auto-Refund:** Smart Contract executes automatic funds release back to the employer wallet if the 50m Ping or Job-Ack is not triggered within the specified window.
* **Instant Payout:** Under 1-second settlement to the worker wallet upon job completion release.

### 4. On-Chain Reputation System & Skill Parcours
* **3-Strike No-Show Rule:** Failure to trigger the 50m Ping results in an immutable Red-Flag token on the wallet identity. 3 Strikes = Instant Protocol Lockout.
* **Rehabilitation:** Users clear strikes by successfully completing interactive, gamified **Skill Parcours** (Proof-of-Skill Badges via SBTs).

---

## ⛔ Developer Governance & Mandatory Consultations

Developers working on this repository are **strictly prohibited** from making autonomous structural decisions regarding the following parameters. **Direct consultation with the Lead Architect is mandatory for:**

1. **Protocol Fee-Splitting Mechanics:** Exact percentages allocated to Treasury, Token-Burn, and Escrow-Pool.
2. **Oracle Integration:** Selection of the Solana Price-Feed Oracle (e.g., Pyth Network) for live fiat conversions in the Header.
3. **Smart Contract Unix Timestamps:** Final hardcoding of timeout windows for auto-refund triggers.
4. **Phase 2 & 3 Schema Extensions:** Database/Contract layout requirements for future **Courier Reverse-Auction Timers** and **Love-Sonar Solana Pay QR Terminals**.

---

## 📜 License
MIT License - Proprietary Core Logic & Architecture.


**********************************************************************************************************************************************************************************

---

## 🔮 Avisierte Visionsvorstellung & Ausbauphase (Future Roadmap)

> **HINWEIS FÜR ENTWICKLER:** Dieser Abschnitt beschreibt die visonäre Skalierung des Kern-Protokolls. Das nachfolgende Framework dient als Grundlage für spätere Modul-Integrationen. Der Code der Phase-1-Engine ist so zu strukturieren, dass diese Anwendungsfälle ohne Refactoring des Solana-Escrows angedockt werden können.

---

### 📦 Modul A: Hyper-Local Courier & Errand Sonar (Mikro-Logistik)
* **Das Konzept:** Spontane Botengänge, Einkäufe, Schnäppchen-Checks vor Ort oder Express-Bringdienste („Bring mir Paket X von Tor A“, „Hol mir die Aktion im Supermarkt um die Ecke“).
* **Reverse-Auction-Timer (Rückwärts-Auktion):**
  * Startpreis verfällt linear über einen definierten Countdown-Balken (z. B. 60 Sekunden).
  * Wer im Nahbereich zuerst akzeptiert, sichert sich den Auftrag zum aktuellen Live-Preis.
* **Dual-Vault Escrow System:**
  * **Vault 1:** Dienstleister-Lohn (dynamisch über den Auktionsbalken ermittelt).
  * **Vault 2:** Auslagen-Budget für den Einkauf (Freigabe erst nach Beleg-Upload im Chat + 50m-Nahbereichs-Ping vor Ort).

---

### ☕ Modul B: Love-Sonar (Proximity Match Engine)
* **Das Konzept:** Anonymes, ortsbezogenes Dating ohne Tagelanges Swipen – ausgelegt auf spontane Begegnungen im Nahbereich (Club, Park, Event).
* **Time-Locked Invite Escrow:**
  * Spendieren von Drinks/Kaffee per Solana-Smart-Contract.
  * Strikter **2-Stunden-Timer (Auto-Refund):** Reagiert die Person nicht oder kommt der 50m-Ping am Treffpunkt nicht zustande, fließen **100 % der Einladungssumme automatisch** in die Wallet des Einladenden zurück.
* **No-Terminal Gastro Clearance:**
  * **P2P Wallet-Freigabe:** Automatische Auszahlung des Getränke-Budgets an die Gegenseite direkt nach dem 50m-Ping vor Ort.
  * **API-Gutschein-Bridge:** Alternativer Auto-Import von digitalen Kassengutscheinen (Apple/Google Pay Voucher) ohne notwendige Krypto-Hardware vor Ort im Café/in der Bar.

---

### 📐 Standardisierte Ausbau-Kriterien (Vision-Governance)
Jedes zukünftige Modul nutzt verpflichtend die Kern-Komponenten der Plattform:
1. **Dynamic Proximity Header** (Live Cent/SOL-Rechner mit Grün-Orange-Rot Zonen).
2. **On-Chain Reputations-System** (3-Strike-Regel für No-Shows).
3. **50m High-Pitch Beeper** (Akustisches Signal zur Last-Mile-Identifikation).


