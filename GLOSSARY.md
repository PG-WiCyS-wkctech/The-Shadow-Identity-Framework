# 📖 Project Glossary: Shadow Identity Framework (SIF)

> **Document ID:** SIF-REF-001  
> **Status:** Reference Document  
> **Purpose:** To standardize the terminology used in the Governance, Risk, and Compliance (GRC) of personal digital identity.

---

## 🎭 Identity Architecture

**The Vault (Secret Identity)** The primary, non-identifiable email address (e.g., `x7_alpha@icloud.com`) used strictly for **authentication**. It is never shared with humans and is only used to log in to high-value services.

**The Mask (Public Identity)** A service-specific alias or "proxy" email (e.g., `amazon.shopping@mask.com`) used for **communication**. All marketing, receipts, and notifications go here. If a Mask is leaked or spammed, it can be deleted without changing your Vault login.

**The Hub** The central "Command Center" account (typically iCloud) where all communications from various Spokes are aggregated. It is the most heavily guarded asset in the framework.

**The Spoke** Any third-party service (Bank, Social Media, School, Utility) that connects to your framework. Each Spoke should be "Decoupled" so it only knows your Mask, not your Vault.



---

## 🔐 Authentication & Security

**FIDO2 / WebAuthn** The modern gold standard for passwordless authentication. It uses hardware-bound cryptography to prove identity, making it immune to phishing.

**Passkey** A digital credential tied to a specific device (Phone, PC) or Hardware Key. It replaces passwords with a biometric scan or hardware tap.

**Roaming Authenticator** A physical security device that is not tied to a single computer (e.g., **Smart Ring**, **YubiKey**, or **Biometric Smart Card**). You carry this with you to log in on any device.

**Platform Authenticator** Biometrics built directly into your hardware, such as **FaceID**, **TouchID**, or **Windows Hello**.

**SIM Swapping** A high-risk attack where a hacker steals your phone number by tricking a carrier. This is the primary reason **SMS-MFA** is prohibited in this framework.

---

## 💿 Storage & Sovereignty

**M-DISC** An archival disc technology (Blu-ray/DVD) that uses a rock-like data layer instead of organic dye. It is rated to last **1,000 years**, protecting data against "bit rot."

**Cloud Renting** The act of paying monthly fees (e.g., Google One, iCloud+) to store data. SIF aims to eliminate this in favor of physical ownership.

**Data Temperature (Hot/Warm/Cold)** * **Hot:** Daily files synced to the cloud ($0 tier).
* **Warm:** Active projects stored on encrypted local SSDs.
* **Cold:** Historical archives (photos/records) stored on M-DISC.

**3-2-1 Backup Strategy** The gold standard for data safety: Keep **3** copies of your data, on **2** different types of media (e.g., SSD and M-DISC), with **1** copy stored off-site.

---

## 🏛️ Governance & Compliance

**GRC (Governance, Risk, and Compliance)** A professional management strategy. In SIF, we apply these corporate standards to personal life to ensure data is managed legally, safely, and consistently.

**Master Sync Matrix** The central "Source of Truth" spreadsheet that tracks every account, its Vault address, its Mask address, and its **Authorized Hardware**.

**Header Audit** The process of inspecting the "Raw Code" of an email to ensure that the secret Vault address is not being leaked in hidden metadata fields like `X-Sender` or `Return-Path`.

**Digital Inheritance** The legal and technical protocol for passing access to your digital "Kingdom" to your heirs in the event of death or incapacitation.

---

**Next Step:** Now that you know the language, ensure your **[Master Sync Matrix](./templates/MASTER_SYNC_MATRIX.md)** columns reflect these definitions.
