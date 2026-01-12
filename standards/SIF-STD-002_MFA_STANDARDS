# 🔑 SIF-STD-002: Multi-Factor Authentication (MFA) Standard

| Metadata | Detail |
| :--- | :--- |
| **Standard ID** | SIF-STD-002 |
| **Status** | 🔴 Mandatory |
| **Version** | 1.0 (2026) |
| **Classification** | Restricted |

## 1. Objective
To ensure that access to the "Hub" and all "Spoke" accounts requires physical possession of a cryptographic secret. We aim to eliminate all "out-of-band" vulnerabilities where a third party (like a mobile carrier) can be exploited to gain access to your data.

## 2. The Source of Truth: FIDO2 Hardware
In this framework, your identity is verified by **possession**, not just knowledge. 
* All critical accounts **must** use FIDO2/WebAuthn hardware-bound credentials as the primary MFA factor.
* **Authorized Devices:** Smart Rings (NFC/FIDO2), YubiKeys, or Biometric Smart Cards.
* **The "2+1" Registration Rule:** Every account must have at least **two** physical keys registered (Primary + Backup) plus one set of printed recovery codes in the **Fireproof Safe**.

---

## 3. The Prohibition of SMS & Voice-Call MFA
**Short Message Service (SMS) and Voice-call authentication are strictly prohibited.**
* These methods are vulnerable to **SIM-swapping**, **SS7 interception**, and **lock-screen leaks**.
* If a service *forces* a phone number for "Identity Verification," a **VOIP or Masked Number** must be used (Refer to [MIG-001: SMS Removal](../migrations/MIGRATION_SMS_REMOVAL.md)).
* **Compliance Rationale:** See **[SIF-RAT-001: Why SMS is Prohibited](./WHY_NO_SMS.md)** for full technical details.

---

## 4. Hierarchical Factor Selection

When configuring a new "Spoke" (account), factors must be chosen in this order of priority:

| Priority | Method | Implementation |
| :--- | :--- | :--- |
| **1 (Gold)** | **FIDO2 / Passkey** | Physical Hardware Key tap or Biometric Smart Ring. |
| **2 (Silver)**| **TOTP (6-digit code)** | Stored in an encrypted, hardware-secured Manager. |
| **3 (Bronze)**| **Push Notification** | Only via encrypted apps (e.g., Apple's native prompt). |
| **PROHIBITED**| **SMS / Voice / Email** | **Never permitted as a security factor.** |

---

## 5. Configuration & Failsafe Protocols

### 5.1 The Backup Key Requirement
To prevent permanent lockout, a backup hardware key (e.g., a YubiKey 5C) must be kept in the **Fireproof Safe**. This key is only removed to be registered to new accounts or during the **Annual Security Audit**.

### 5.2 Recovery Code Governance
Upon disabling SMS, platforms generate a one-time "Master Recovery Key" or "Backup Codes."
* **Action:** These codes must be printed (Physical Media) and stored in the **Recovery Folder**.
* **Prohibition:** Do not store these as unencrypted `.txt` or `.pdf` files on any cloud drive.

### 5.3 Biometric "Platform" Use
Native biometrics (FaceID/TouchID) are permitted for daily convenience on "Trusted Devices," provided they are mathematically linked to the hardware-bound "Hub" identity.

---

## 6. Compliance Checklist

- [ ] Has SMS been removed/disabled as an MFA factor on the Hub?
- [ ] Are there at least two hardware keys registered to your primary email?
- [ ] Are the printed recovery codes physically secured in the safe?
- [ ] Does the `Master_Sync_Matrix` reflect the "FIDO2" status for this account?

---

**Next Step:** Ensure you have procured your backup hardware before executing **[MIG-001: SMS Removal](../migrations/MIGRATION_SMS_REMOVAL.md)**.
