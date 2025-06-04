```markdown
# Enhanced Due Diligence (EDD) Policy  
**Document Owner:** Compliance Team  
**Effective Date:** 01/02/2025  
**Review Period:** Annual (or as triggered by regulatory changes)  
**Applicable Entity:** CoinPort (AUSTRAC-registered cryptocurrency exchange)  

---

## 1. Purpose  
This policy outlines CoinPort's Enhanced Due Diligence (EDD) procedures to mitigate high-risk financial crime exposures, ensuring compliance with:  
- **Anti-Money Laundering and Counter-Terrorism Financing Act 2006 (AML/CTF Act)**  
- **AUSTRAC regulatory guidelines**  
- **FATF Recommendations (Virtual Asset Service Providers)**  

---

## 2. Scope  
EDD applies to:  
- **High-risk customers** (e.g., PEPs, non-residents, high-volume traders, darknet-linked wallets).  
- **Unusual transactions** (e.g., structuring, cross-jurisdictional flows).  
- **Business relationships** involving private wallets, shell companies, or high-risk jurisdictions.  

---

## 3. EDD Triggers  
### 3.1 Customer Risk Factors  
| **Risk Category**       | **Examples**                          |  
|--------------------------|---------------------------------------|  
| **Politically Exposed Persons (PEPs)** | Government officials, their families/associates. |  
| **Jurisdictional Risk**  | Customers from FATF blacklisted countries (e.g., Iran, North Korea). |  
| **Behavioral Red Flags** | Rapid deposits/withdrawals, use of mixers/Tumblers. |  

### 3.2 Transaction Risk Factors  
- Single transactions > **AUD 10,000** without clear economic purpose.  
- Frequent cross-border transfers to/from high-risk jurisdictions.  
- Mismatched activity (e.g., unemployed individual trading $50,000/day).  

---

## 4. EDD Procedures  
### 4.1 Identity Verification  
- **Tier 1 KYC:** Standard ID (Passport/Driver’s License + Proof of Address).  
- **Tier 2 EDD:**  
  - **Source of Wealth (SoW):** Bank statements, tax returns, or business licenses.  
  - **Source of Funds (SoF):** Transaction history (e.g., mining rewards, fiat on-ramp proofs).  
  - **UBO Declaration:** For corporate accounts, Ultimate Beneficial Ownership >25%.  

### 4.2 Ongoing Monitoring  
- **KYT (Know Your Transaction) Tools:** Chainalysis/TRM Labs integration for real-time blockchain analysis.  
- **Adverse Media Screening:** WorldCheck or local databases for crime/terrorism links.  

### 4.3 Senior Management Approval  
- EDD cases require **Chief Compliance Officer (CCO) sign-off** before onboarding.  

---

## 5. Documentation & Retention  
- **EDD records** retained for **7 years** post-account closure.  
- **Audit Trail:** Logs of all EDD reviews, alerts, and resolutions.  

---

## 6. Roles & Responsibilities  
| **Role**                | **Duties**                              |  
|--------------------------|-----------------------------------------|  
| **Compliance Officer**   | Conducts EDD reviews, files SMRs.       |  
| **MLRO**                 | Oversees high-risk escalations.         |  
| **IT Team**              | Maintains KYC/KYT tool integrations.    |  

---

## 7. Review & Updates  
- Policy reviewed **annually** or after:  
  - New AUSTRAC guidance.  
  - Emerging crypto threats (e.g., privacy coin usage).  

**Approved by:** Peter Cooney  
**Date:** 01/02/2025  
```  


# Enhanced Due Diligence (EDD) for Politically Exposed Persons (PEPs)  
**Applicable to:** CoinPort Pty Ltd (AUSTRAC-licensed exchange)  

---

## 1. PEP Definition & Risk Exposure  
**PEPs** are individuals entrusted with prominent public functions (or their close associates/family members), posing higher money laundering risks due to potential:  
- **Abuse of power** (e.g., bribery, corruption proceeds).  
- **Complex ownership structures** to hide illicit funds.  
- **Reputational risk** to the exchange if linked to financial crimes.  

### 1.1 PEP Categories  
| **Tier**       | **Examples**                                                                 | **Risk Level** |  
|----------------|-----------------------------------------------------------------------------|---------------|  
| **Domestic PEPs** | Australian MPs, judges, senior military/government officials.               | Medium-High   |  
| **Foreign PEPs**  | Heads of state, ministers, central bank governors (non-Australian).        | High          |  
| **International Organization PEPs** | Senior UN, IMF, or World Bank officials.                     | Medium        |  

---

## 2. PEP Identification Process  
### 2.1 Screening Tools  
- **Automated Databases:** WorldCheck, Refinitiv, or local AUSTRAC PEP lists.  
- **Manual Checks:** Google searches for adverse media (e.g., "[Name] + corruption scandal").  

### 2.2 Red Flags for PEPs  
- Use of **third-party accounts** (e.g., family members transferring crypto).  
- Transactions linked to **high-risk jurisdictions** (e.g., Venezuela, Zimbabwe).  
- Sudden **large crypto purchases** inconsistent with declared income.  

---

## 3. Enhanced Due Diligence (EDD) for PEPs  
### 3.1 Documentation Requirements  
- **Standard KYC:** Passport, proof of address.  
- **Additional PEP-Specific:**  
  - **Declaration of Public Office** (position, dates of service).  
  - **Source of Wealth (SoW):** Salary slips, government disclosures, or asset registries.  
  - **Source of Funds (SoF):** For crypto deposits >AUD 10,000, provide fiat origin proof (e.g., bank statements).  

### 3.2 Approval Workflow  
1. **Compliance Officer** flags account as PEP during onboarding.  
2. **MLRO** reviews SoW/SoF documents and conducts adverse media screening.  
3. **CCO** grants final approval before account activation.  

---

## 4. Ongoing Monitoring  
- **Transaction Alerts:** PEP accounts trigger mandatory review for:  
  - Cross-border transfers.  
  - Transactions >AUD 5,000 (lower threshold than standard customers).  
- **Annual Reassessment:** Re-verify PEP status and SoW/SoF.  

---

## 5. Restrictions & Mitigations  
- **Activity Caps:** Limit daily withdrawals (e.g., AUD 20,000) pending CCO approval.  
- **Senior Management Oversight:** CCO receives quarterly PEP activity reports.  
- **Exit Strategy:** Terminate relationships if PEP fails to provide SoW/SoF evidence.  

---

## 6. PEP Policy Exceptions  
- **Deceased/Retired PEPs:** EDD requirements apply for **12 months** post-office.  
- **Low-Risk PEPs:** E.g., Australian local councillors with verified legitimate income.  

```


### **4. Crypto-Specific Risks in EDD**  
#### **4.1 Anonymity-Enhanced Technologies (AETs)**  
| **Risk**                | **Mitigation**                                                                 |
|--------------------------|-------------------------------------------------------------------------------|
| **Privacy Coins** (Monero, Zcash) | Block inbound/outbound transactions or require additional SoF documentation. |
| **Mixers/Tumblers**      | Auto-flag transactions linked to known mixing services (e.g., Tornado Cash).   |
| **Decentralized Exchanges (DEXs)** | Screen for wallet addresses interacting with unregulated DEXs.              |

#### **4.2 Blockchain-Specific Red Flags**  
- **UTXO Chaining:** Frequent small inputs consolidated into large withdrawals (structuring).  
- **High-Velocity Wallets:** Addresses with rapid inflows/outflows (>50 tx/day).  
- **Darknet Links:** Wallets tied to Hydra, Silk Road, or ransomware payments (use Chainalysis/TRM).  

#### **4.3 Cross-Jurisdictional Risks**  
- **Nested Services:** Crypto deposits from high-risk VASPs (e.g., Seychelles/Cayman Islands-based).  
- **Geolocation Mismatches:** User IP address ≠ declared residency (VPN detection).  

#### **4.4 Stablecoin Manipulation**  
- **USDT/USDC Flows:** Large stablecoin transfers with no clear trading purpose (possible layering).  
- **Off-Ramp Risks:** Fiat conversions via shadow banking corridors (e.g., Hong Kong/MSBs).  

#### **4.5 Smart Contract Risks**  
- **DeFi Protocols:** Funds routed through unaudited contracts (e.g., yield farming pools).  
- **NFT Wash Trading:** Fake sales to inflate asset values (trace OpenSea/Blur activity).  

---

### **5. Enhanced Controls for Crypto Risks**  
1. **On-Chain Forensics**  
   - Integrate **KYT tools** (e.g., Elliptic, Crystal Blockchain) to trace VASP-to-VASP flows.  
   - Tag wallets associated with:  
     - Sanctioned entities (OFAC SDN List).  
     - Stolen funds (e.g., CoinGecko hack alerts).  

2. **Transaction Pattern Analysis**  
   - **Cluster Analysis:** Link multiple deposit addresses to a single user.  
   - **Time-of-Day Monitoring:** Unusual activity outside user’s timezone.  

3. **Strict Off-Ramp Rules**  
   - Require **fiat conversion approvals** for withdrawals >AUD 10,000.  
   - Block transfers to **unhosted wallets** for high-risk customers.  

---

### **6. Examples of Suspicious Crypto Activity**  
| **Scenario**               | **EDD Action**                                                                 |
|----------------------------|-------------------------------------------------------------------------------|
| User deposits 15 BTC from a mixer-linked wallet. | Freeze funds, demand SoF, file SMR.                                      |
| PEP receives $500k USDT from a Seychelles VASP. | Verify SoW, limit account, notify AUSTRAC.                                |
| New account trades $1M NFTs with self-funded wallets. | Investigate for wash trading/market manipulation.                        |

---

### **7. Policy Enforcement**  
- **Automated Alerts:** Real-time flags for AETs, sanctioned wallets, or high-risk jurisdictions.  
- **Training:** Staff education on crypto laundering typologies (e.g., "chain hopping").  

**Approval:** CCO + MLRO  
**Review:** Biannual (aligns with FATF VASP updates).  

--- 

**Approved by:** Peter Cooney  
**Date:** 01/02/2025  
