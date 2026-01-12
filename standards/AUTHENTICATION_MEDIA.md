# 📜 SIF Standard: Authentication Media & Factors

> **Document ID:** SIF-STD-006  
> **Status:** Mandatory  
> **Focus:** Multi-Modal Passkeys (Something You Have + Something You Are)

To ensure phishing-resistant access, the Shadow Identity Framework (SIF) mandates the use of FIDO2/WebAuthn "Passkeys" across all devices.

---

## 💍 1. Roaming Authenticators (Wearables & Cards)
These are physical devices that store your "Shadow Identity" keys and can be used across multiple computers or phones via NFC, Bluetooth, or USB.

| Media Type | Verification Method | Recommended Use |
| :--- | :--- | :--- |
| **Smart Ring** | Built-in Fingerprint | Daily "High-Frequency" login (Email Hub). |
| **Biometric Smart Card** | Built-in Fingerprint + NFC | Professional/Work-site access and Alumni accounts. |
| **Classic Security Key** | Physical Tap + PIN | Emergency Recovery / Vault Access. |

---

## 🤳 2. Platform Authenticators (Device-Bound)
These are the biometrics built directly into your primary hardware.

* **Facial Recognition:** Apple FaceID / Windows Hello. Must be backed by a 6-digit PIN.
* **Fingerprint:** TouchID / Android Biometric.
* **Standard:** Platform authenticators are permitted for "Spoke" accounts (shopping, social) but must be paired with a Roaming Authenticator for the "Hub."

---

## ⚖️ 3. The "Two-Touch" Rule for High-Value Assets
For accounts marked "Critical" in the **Master Sync Matrix** (Banking, Primary Vault):
1.  **Possession:** You must present a Roaming Authenticator (Ring or Card).
2.  **Inherence:** You must verify with a Biometric (Fingerprint or Face).
*This prevents someone from using your Ring or Card while you are asleep.*
