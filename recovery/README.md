# 🚨 Recovery: The Last Line of Defense

> **Folder Status:** CRITICAL  
> **Standard ID:** GRC-REC-000  
> **Mission:** Ensure 100% data and identity restoration in the event of hardware loss, theft, or biometric failure.

This directory contains the "Break-Glass" protocols for the **Shadow Identity Framework (SIF)**. In a system built on hardware-bound passkeys and biometric signatures, the risk of permanent lockout is high. The documentation here provides the mathematical and physical path back to your data.

---

## 🏛️ Recovery Architecture

The SIF recovery model follows the **"2+1 Rule"**:
1.  **Something You Have:** A secondary, off-site Hardware Key (YubiKey/Smart Card).
2.  **Something You Know:** A high-entropy Master Passphrase (stored in the safe).
3.  **The Failsafe (+1):** A set of 28-character platform recovery codes for your "Hub" (iCloud/Google).



---

## 📂 Recovery Documentation Index

| Document | Purpose | Type |
| :--- | :--- | :--- |
| **[SIF-REC-001: Break-Glass Protocol](./IDENTITY_RECOVERY_PLAN.md)** | Step-by-step instructions for theft, loss, or biometric failure. | Manual |
| **[Recovery Ledger (Template)](../templates/RECOVERY_LEDGER.md)** | A map of where recovery codes and physical keys are hidden. | Template |
| **[Digital Inheritance Plan](./INHERITANCE_PLAN.md)** | Instructions for family members to access the archive if you are incapacitated. | Legal/Tech |
| **[Account Restoration Log](./RESTORATION_LOG.md)** | A log to track which accounts have been reset during an active incident. | Audit |

---

## 🛡️ The "Fireproof Safe" Requirements

To comply with the **SIF Recovery Standard**, your physical "Offline Vault" must contain the following items in a fireproof/waterproof enclosure:

* **Authorized Hardware (Backup):** At least one registered FIDO2 key (e.g., YubiKey) that is *not* your daily-use Smart Ring.
* **The Master Passphrase:** A printed "Diceware" phrase for your password manager.
* **Encrypted Storage Key:** The password/recovery key for your **M-DISC** and **SSD** hardware backups.
* **Platform Recovery Codes:** Printed QR codes and alphanumeric keys for the "Hub" (iCloud/Google/Microsoft).

---

## 🔄 Annual Recovery Drill (The "Fire Drill")

To ensure this folder is functional, perform the following audit every **January**:

1.  **Hardware Check:** Plug in your backup YubiKey/Smart Card to ensure the firmware is active and the key hasn't been corrupted.
2.  **Credential Check:** Verify your Master Passphrase still opens your local password manager database.
3.  **Code Verification:** Check that your printed platform recovery codes haven't been "rotated" or invalidated by a recent account change.
4.  **Hardware Update:** If you purchased a new **Smart Ring** this year, ensure a backup key was also registered to the same accounts.

---

## ⚠️ Security Warning
The files in this folder describe how to bypass your primary security. 
* **Never** store actual passwords or recovery codes in this GitHub repository.
* **Never** leave this folder open on a public-facing device.
* Use these documents as **Blueprints**, but store the **Data** in your physical safe.

---

**Next Step:** Would you like me to generate the **[Digital Inheritance Plan](./INHERITANCE_PLAN.md)**? This document explains how to safely pass your digital "Kingdom" to your kids or spouse without compromising your "Shadow Identity" while you are still active.
