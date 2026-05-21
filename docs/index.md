# 🚀 Welcome to the GVVSS Documentation Portal

Welcome to the central knowledge base for GVVSS internal systems. This portal provides standardized, step-by-step documentation for all operational workflows, custom applications, and automation scripts.

---

## 📚 Official Guides & Manuals

* **[GVVSS Reports Portal (OCR System)](ocr-system/index.md)** - The primary user manual for uploading and processing store-level scanned forms.
* **[OCR Google Apps Script Setup](ocr-google-script/index.md)** - Technical setup guide for deploying the backend Google Apps Script.
* **[Standard Documentation Template](template/index.md)** - The required blueprint for creating any new documentation.

---

## ⚙️ How This Portal Works (Docs-as-Code)

This website is not a standard Google Site or WordPress page. It is built using a **Docs-as-Code** methodology. 
* **The Storage:** All manuals are typed in simple text files and stored securely in our [GitHub Repository](https://github.com/johannes-gvssgroup/sample-documentation-v1).
* **The Automation:** Whenever a change is saved to GitHub, an automated robot (GitHub Actions) wakes up, converts the text into this beautiful website, and publishes it live within 2 minutes. 
* **The Benefit:** No one has to format HTML or manage web servers. We just write the steps, and the system handles the rest.

---

## 🔄 How the Versioning Works

In a regulated environment, it is critical to know what the rules were on any given day. This portal uses an automated versioning tool to freeze old documentation.

* **The Version Dropdown:** Look at the top right corner of this screen (next to the search bar). You will see a dropdown menu labeled with our current version (e.g., **1.0 (latest)**).
* **Daily Updates:** For typos, minor edits, or new pages, the system stays on the current version. 
* **Major Changes:** When a massive process change occurs (like replacing the OCR system entirely), the IT team will release version **1.1** or **2.0**. The old version is permanently frozen and archived. You can use the dropdown menu at any time to travel back and read the old rules!

---

## 📞 Escalation & Support

If you encounter an undocumented error, please follow the standard escalation path:
1. **L1 (BPO/Operations):** Attempt documented error-handling steps.
2. **L2 (Technical):** Flag issues with Demian via the Portal for system hangs or API failures.
3. **L3 (Ops/Exec):** Escalate to Joseph for process adjustments or workflow changes.