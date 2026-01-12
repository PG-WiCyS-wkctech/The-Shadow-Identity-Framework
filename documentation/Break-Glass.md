# 🚨 SIF: Identity Recovery & "Break-Glass" Protocol

> **Document ID:** SIF-REC-001  
> **Classification:** RESTRICTED / PHYSICAL ONLY  
> **Location:** Fireproof Safe / Safety Deposit Box

This document is the final failsafe for the **Shadow Identity Framework**. If your biometrics fail, your smart ring is lost, or your primary device is stolen, follow these protocols to regain sovereignty over your digital life.

---

## 📦 1. The Physical "Safe" Inventory
*Ensure your fireproof safe contains the following physical assets:*

1.  **The Master Ledger:** A printed copy of your `Master_Sync_Matrix`.
2.  **The Backup Roaming Authenticator:** A secondary, registered YubiKey or Smart Card (never carried on your person).
3.  **The Cold Passphrase:** Your 15-20 word "Diceware" Master Password for your Password Manager.
4.  **Platform Recovery Sheets:** Printed 28-character recovery codes for Apple ID (iCloud) and Google (Gmail).
5.  **The "Key" Drive:** An encrypted USB containing your S/MIME certificates (.p12) and PGP Private Keys.

---

## 🛠️ 2. Recovery Scenarios

### Scenario A: Smart Ring or Hardware Key is Lost/Stolen
1.  **Immobilize:** Log in to your **iCloud/Google Vault** using your backup Hardware Key from the safe.
2.  **De-Authorize:** Navigate to "Security > Passkeys & Security Keys." 
3.  **Revoke:** Identify the lost Ring/Key by its label in the matrix and click **"Revoke Access."**
4.  **Replace:** Register the new hardware device and update the `Master_Sync_Matrix`.

### Scenario B: Primary Smartphone is Stolen (Phone/FaceID/Passkey)
1.  **Remote Wipe:** Use a trusted computer to log in to "Find My" (Apple) or "Find My Device" (Google). Execute a **Remote Wipe** immediately.
2.  **Bypass Biometrics:** On a trusted PC, log in to your Hub account. When it asks for FaceID/Passkey, select **"Try another way"** and use your **Physical Backup Key** from the safe.
3.  **Reset "Trusted Devices":** Remove the stolen phone from your trusted device list to invalidate its internal Passkeys.

### Scenario C: Biometric Sensor Failure (Injury or Hardware Malfunction)
1.  **Fallback to PIN:** Use the 6-digit device PIN (ensure this is recorded in your Safe Ledger).
2.  **Fallback to Hardware:** If the OS refuses biometrics, use your **Roaming Authenticator (Ring/Card)** via NFC to bypass the device-bound biometric requirement.

---

## 🔑 3. The "Master Recovery Key" Protocol
If you lose access to your **Master Password** or your **Password Manager** database is corrupted:

1.  **Retrieve the Diceware Sheet:** Open the sealed envelope in your safe.
2.  **Manual Entry:** Type the passphrase into a clean, offline machine (if possible).
3.  **Database Restore:** Locate the "Last Known Good" backup of your `.kdbx` or Bitwarden export on your **Encrypted SSD** (Hardware Layer).
4.  **Re-Sync:** Restore the database and immediately verify the "Vault" login credentials.

---

## 📑 4. Emergency Instructions for Family
*In the event that the primary user is incapacitated, the following steps allow a designated "Digital Heir" to access the archive:*

1.  **Locate the Safe:** [Insert Location of Safe].
2.  **Access the Master Ledger:** This contains the "Map" of all accounts.
3.  **Use the Physical Key:** The YubiKey labeled "PRIMARY BACKUP" will grant access to all "Vault" accounts when plugged into a PC.
4.  **Follow the Matrix:** Use the recovery emails listed in the `Master_Sync_Matrix` to reset secondary "Spoke" accounts.

---

## 🛑 Post-Recovery Audit
Once access is restored, you **must** perform a "Security Reset":
- [ ] Generate new Recovery Codes for Apple/Google.
- [ ] Print a new `Master_Sync_Matrix`.
- [ ] Re-encrypt the "Key" Drive with a new password.
- [ ] Securely shred all old Recovery Sheets.
