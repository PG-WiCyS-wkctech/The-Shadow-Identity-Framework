# 💿 MIG-003: Storage Offload (The Cloud Purge)

> **Standard ID:** GRC-MIG-003  
> **Status:** Operational Guide  
> **Objective:** Transition from "Cloud Renting" to "Physical Ownership" to achieve a $0/mo storage cost.

In the Shadow Identity Framework, we treat the Cloud as a **"Transit Hub,"** not a **"Permanent Warehouse."** This guide outlines the "Burn and Purge" workflow to move your legacy data (photos, videos, tax records) onto 1,000-year M-DISC media and encrypted SSDs.

---

## 🏛️ The Three-Tier Storage Model

To achieve $0 cloud costs, data must be classified and moved according to its "Temperature."



| Tier | Type | Location | Cost | Access |
| :--- | :--- | :--- | :--- | :--- |
| **Hot** | Daily Files | iCloud/Google (Free Tier) | $0 | Instant |
| **Warm** | Active Projects | **Encrypted SSD (Local)** | One-time | Fast |
| **Cold** | Historical/Photos| **M-DISC (Archival)** | One-time | Manual |

---

## 🛠️ Step-by-Step Execution

### Phase 1: Data Triage (The Audit)
- [ ] **Identify the "Storage Wall":** Determine which account is closest to its "Billing Wall" (e.g., 14GB of 15GB on Google).
- [ ] **Large File Discovery:** Use Google One or iCloud Storage settings to find the "Top 100" largest files/videos.
- [ ] **Labeling:** Mark folders as "Archive Ready" once they are no longer being edited monthly.

### Phase 2: The Physical Bridge (SSD Transfer)
1.  **Download:** Use **Google Takeout** or **iCloud.com** to download full albums or folder structures.
2.  **Verify:** Ensure the download is complete.
3.  **Local Encryption:** Move the files onto your **Hardware-Encrypted SSD**. 
4.  **Organization:** Follow the SIF naming convention: `YYYY-MM-DD_ProjectName_ARCHIVE`.

### Phase 3: The Permanent Burn (M-DISC)
1.  **Stage:** Create a folder on your computer that is exactly 4.3GB (for DVD M-DISC) or 23GB (for Blu-ray M-DISC).
2.  **Burn:** Use an M-DISC compatible burner to write the data to the disc.
3.  **Validate:** Perform a "Data Verification" check after the burn to ensure no sectors are corrupt.
4.  **Physical Label:** Use a non-solvent pen to label the disc with the **Archive ID** found in your `Data_Inventory_Ledger`.



### Phase 4: The Purge (Cloud Deletion)
1.  **The Double-Check:** Confirm the data exists on both the **SSD** (Warm) and the **M-DISC** (Cold).
2.  **Delete:** Permanently delete the files from the cloud service.
3.  **Empty Trash:** Ensure you empty the "Bin" or "Recently Deleted" folder to immediately reclaim the storage space.
4.  **Downgrade:** Once your usage drops below the free limit (e.g., <5GB for iCloud), cancel the monthly subscription.

---

## 📊 Data Inventory Ledger (Integration)
Every time you perform an offload, you must update the **`templates/DATA_INVENTORY_LEDGER.xlsx`** with:
* **Disc/Drive ID:** (e.g., M-DISC-001)
* **Content Summary:** (e.g., "Family Photos 2015-2020")
* **Physical Location:** (e.g., "Safe 1, Shelf B")
* **Checksum:** (Optional: SHA-256 hash for future verification)

---

## ⚠️ Critical Safety Rules
* **The "3-2-1" Rule:** Keep **3** copies of data, on **2** different types of media (SSD + M-DISC), with **1** copy off-site (e.g., a safety deposit box).
* **No "Cloud-Only" Backups:** If the file only exists in the cloud, it doesn't exist.
* **Format Stability:** Only archive files in "Universal" formats (PDF for docs, JPG/DNG for photos, MP4 for video) to ensure they can be read in 20+ years.

---

## ✅ Migration Completion Checklist
- [ ] Paid cloud subscriptions cancelled/downgraded to Free.
- [ ] All "Cold" data verified on physical M-DISC.
- [ ] Master Sync Matrix updated with new "Storage Status."
- [ ] Physical media placed in Fireproof Safe.

---

**Next Step:** Would you like me to draft the **[Hardware Procurement Guide](../hardware/PROCUREMENT_GUIDE.md)** so you know exactly which M-DISC burner and Encrypted SSD models meet these GRC standards?
