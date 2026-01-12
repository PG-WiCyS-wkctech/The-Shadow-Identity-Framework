# ✅ Migration Guide: Killing the SMS Link

> **Standard ID:** GRC-MIG-001  
> **Status:** Critical Operational Guide  
> **Objective:** Transitioning from carrier-dependent SMS-MFA to user-owned Cryptographic MFA.

Removing your phone number as a recovery/MFA method is the final step in securing your **Shadow Identity**. This guide ensures you do so without accidentally locking yourself out of your accounts.

---

## 🛠️ Phase 1: The Pre-Flight Safety Check
**Do not skip these steps.** You must have your "Safety Net" in place before disabling SMS.

1.  **Possess Two Keys:** Ensure you have both your primary (e.g., Smart Ring) and your backup (e.g., YubiKey) registered.
2.  **Generate Recovery Codes:** Every platform (Google, Apple, Microsoft) provides a one-time list of 10-15 recovery codes. 
    * **Action:** Print these out and put them in your Fireproof Safe immediately.
3.  **Audit the Matrix:** Ensure the "Vault" address for the account is correctly logged in your `Master_Sync_Matrix`.

---

## 📋 Phase 2: Platform Execution

### 1. Google Account (The Vault)
* **Navigate:** Google Account > Security > 2-Step Verification.
* **Step A:** Add your **Hardware Keys/Passkeys** first.
* **Step B:** Add a **TOTP Authenticator App** (Bitwarden or Google Authenticator).
* **Step C (The Verification):** Log out and log back in. Use the Hardware Key to enter.
* **Step D (The Cut):** Only after a successful login, click the "Trash" icon next to your Phone Number.

### 2. Apple ID (The Hub)
* **Navigate:** Settings > [Your Name] > Sign In & Security > Two-Factor Authentication.
* **Step A:** Select **"Account Recovery"** and generate a **Recovery Key**. Write this down!
* **Step B:** Select **"Security Keys"** and add your physical FIDO2 keys.
* **Step C:** Apple requires "Trusted Phone Numbers." While you can't always remove the last number, you can **disable** it as a primary sign-in factor.

### 3. Microsoft / Outlook
* **Navigate:** Security Dashboard > Advanced Security Options.
* **Step A:** Select "Add a new way to sign in or verify." 
* **Step B:** Choose "Use a security key" or "Face/Fingerprint."
* **Step C:** Enable **"Passwordless Account"** mode if supported. This makes the hardware key mandatory.
* **Step D:** Remove the phone number from the "Text a code" section.

---

## 🕵️ Phase 3: The "Ghost Number" Trap
Some services (Banks, Legacy Apps) insist on a phone number for "Identity Verification" even if they don't use it for MFA.

* **The Strategy:** Use a **VOIP or Masked Number** (e.g., Google Voice or MySudo) rather than your actual SIM-card number.
* **The Benefit:** If your physical SIM is swapped, the attacker still cannot access the VOIP number because that number is protected by your Hardware-Secured Gmail/iCloud account.
* **The Rule:** Your **Real Phone Number** should never be the "Key" to your **Secret Vault**.

---

## 🚨 Troubleshooting: "I'm locked out!"
If a platform demands an SMS code you no longer have access to:
1.  **Use the Recovery Code:** Use one of the 10-15 codes you printed in Phase 1.
2.  **Use the "Trusted Device":** Usually, your iPad or Macbook can "Vouch" for your new login without a code.
3.  **Hardware Fallback:** Plug in your Backup YubiKey.

---

## ✅ Final Compliance Check
- [ ] Is the phone number removed from the 2FA list?
- [ ] Has at least one Hardware Key been tested?
- [ ] Are the 10 Backup Codes in the Fireproof Safe?
- [ ] Is the `Master_Sync_Matrix` updated to "MFA Type: FIDO2/Passkey"?

---

**Next Step:** Would you like to create a **"Header Audit Checklist"**? This will help you verify that after removing SMS, your sent emails aren't still leaking your "Vault" identity in the background metadata.
