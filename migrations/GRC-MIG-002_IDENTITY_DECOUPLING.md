# 🎭 MIG-002: Identity Decoupling Guide

> **Standard ID:** GRC-MIG-002  
> **Status:** Operational Guide  
> **Objective:** To separate "Authentication" from "Communication" across all high-value accounts.

Identity Decoupling ensures that even if a service (like a bank or social media platform) suffers a data breach, your primary "Vault" email remains unknown to the public. You log in with a secret; you communicate with a mask.

---

## 🏛️ The Architecture of a Decoupled Account

In a standard setup, your email is your username AND your contact point. In a Decoupled setup, we split these functions.



1.  **The Vault (Login Only):** A high-security, secret email address (the "Secret Identity") used exclusively for sign-in and password resets.
2.  **The Mask (Communication Only):** A public-facing alias (e.g., iCloud "Hide My Email" or a custom domain alias) where all notifications, receipts, and human interactions occur.

---

## 🛠️ Step-by-Step Execution

### Phase 1: Preparation
- [ ] **Identify the Spoke:** Choose the account to decouple (e.g., Chase Bank, LinkedIn).
- [ ] **Generate the Vault Address:** Create or select a secret email address (e.g., `vault_x92@icloud.com`).
- [ ] **Generate the Mask Alias:** Create a service-specific alias (e.g., `chase.bank.mask@icloud.com`).

### Phase 2: The "Vault" Flip (Authentication)
1.  Log into the service using your current credentials.
2.  Navigate to **Security Settings** or **Login & Security**.
3.  Change the **Primary Email Address** or **Username** to your **Vault Address**.
4.  **Verify:** You will likely receive a confirmation link at the new Vault address. Click it.
5.  **MFA Check:** Ensure your **Smart Ring** or **Hardware Key** is still the primary MFA for this account now that the login has changed.

### Phase 3: The "Mask" Setup (Communication)
1.  Navigate to **Profile Settings** or **Contact Information**.
2.  Look for a field labeled "Preferred Email," "Contact Email," or "Notifications."
3.  Set this to your **Mask Alias**.
4.  **Test:** Send a "Test Notification" or "Forgot Username" request to ensure it arrives at the Mask (which forwards to your Hub) and not directly to the Vault's inbox.

---

## 🏦 Special Case: Financial Institutions
Banks are often resistant to having two different emails. Use this hierarchy:
* **Primary Sign-in:** The Vault.
* **Security Alerts:** The Vault (must be high-priority).
* **Statements/Marketing/Standard Notifications:** The Mask.

---

## ✅ Post-Migration Validation
A decoupling is successful only if it passes the **"Leak Test"**:

1.  **Matrix Update:** Log the change in your `Master_Sync_Matrix`.
2.  **Metadata Check:** Send an email from that service to a secondary test account. 
3.  **Audit:** Open the "Original Message" or "Headers" of that email. 
    * **Success:** You see the Mask address. 
    * **Failure:** You see the Vault address in the `Return-Path` or `X-Sender` fields.

---

## ⚠️ Common Pitfalls
* **The "Forwarding Loop":** Ensure your Mask isn't forwarding to your Vault, and your Vault isn't forwarding to your Mask. Both should forward independently to your **iCloud Hub**.
* **Browser Autofill:** Clear your browser cache or update your **Password Manager** immediately after the flip. Your browser will try to log you in with your old "Mask" email, which will now fail.

---

**Next Step:** Would you like to create the **[Header Audit Checklist](../checklists/HEADER_AUDIT.md)** to perform the technical verification mentioned in the validation section?
