# 🛡️ Security Rationale: Prohibition of SMS-MFA

> **Standard ID:** GRC-RAT-001  
> **Status:** Mandatory Rationale  
> **Target:** All accounts within the Shadow Identity Framework.

Within the **Shadow Identity Framework (SIF)**, Short Message Service (SMS) and Voice-call authentication are strictly prohibited as primary or secondary Multi-Factor Authentication (MFA) methods. This document outlines the technical and procedural vulnerabilities that lead to this prohibition.

---

## 🚫 The 5 Fatal Flaws of SMS-MFA

### 1. SIM Swapping (Social Engineering)
The greatest risk to personal identity in 2026 is the **SIM Swap**. An attacker convinces a mobile carrier employee to port your phone number to a new SIM card in the attacker's possession. 
* **Impact:** The attacker receives all 2FA codes, allowing them to reset passwords on banking and email accounts in real-time.

### 2. SS7 Protocol Insecurity
The global telecommunications backbone (SS7) used for SMS was designed in the 1970s without modern encryption.
* **Impact:** Sophisticated actors can intercept SMS messages "in flight" across the cellular network without ever needing physical access to your phone or carrier.

### 3. Lock-Screen Exposure (Physical Risk)
By default, most smartphones display a preview of incoming SMS messages on the lock screen.
* **Impact:** A stolen or even a momentarily unattended phone allows a bystander to see a 6-digit login code without needing to unlock the device.

### 4. Lack of Cryptographic Binding
SMS codes are "headless." They do not know which website requested them.
* **Impact:** An attacker can build a fake (phishing) login page. You enter your password and your SMS code; the attacker captures both and logs into the real site before the code expires. **Passkeys and Hardware Keys prevent this via cryptographic handshakes.**

### 5. Dependency on Third-Party Governance
When you use SMS, you are trusting the security protocols of a mobile carrier (e.g., Verizon, AT&T) to protect your "Vault."
* **Impact:** This violates the SIF principle of **Data Sovereignty**. If the carrier has a data breach or a corrupt employee, your security is compromised.

---

## 📊 Security Factor Comparison

| Method | Strength | Phishing Resistant? | Controlled by You? |
| :--- | :--- | :--- | :--- |
| **SMS / Voice** | 🔴 Low | **No** | **No** (Carrier-owned) |
| **TOTP (Apps)** | 🟡 Medium | **No** | **Yes** (Device-owned) |
| **FIDO2 / Passkeys** | 🟢 High | **Yes** | **Yes** (Hardware-bound) |

---

## 🏛️ The "Zero-Trust" Conclusion
The Shadow Identity Framework operates on a **Zero-Trust** model regarding telecommunication infrastructure. We assume the cellular network is compromised. By moving to Hardware Keys, Biometric Smart Cards, and Smart Rings, we ensure that the "Keys to the Kingdom" remain physically in your possession.

---

**Next Step:** Review the [MFA Standards](./MFA_STANDARDS.md) to see the approved alternatives.
