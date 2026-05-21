# 📄 System Documentation Template

!!! tip "How to use this template"
    Copy this file when documenting any new GVVSS system, app, or script. Fill out the relevant tables and delete any sections that do not apply.

## Section 01 — Overview & Purpose
* **System Name:** [App/System Name]
* **App Type:** [e.g., Google Apps Script / Web App / Python Automation]
* **Business Purpose:** [Why does this exist? What problem does it solve?]
* **Business Rules:** [Important constraints, especially regarding vape/tobacco regulations]

## Section 02 — Process Flow
**Step-by-Step Workflow:**
1. **Trigger:** [How does it start? e.g., Time-driven, User click, Webhook]
2. **Action 1:** [What happens next?]
3. **Action 2:** [Next step]

!!! warning "Error Handling & Exception Flows"
    * **If X fails:** [Do Y]
    * **If data is missing:** [Trigger Z]

## Section 03 — Code & Version Control
* **Repository Location:** [GitHub URL or Google Drive Link]
* **File/Module Structure:** [Brief list of main files]
* **Branching Convention:** [e.g., `main` for prod, `dev` for staging]

**Version History Log:**

| Version | Date | Author | Summary of Changes |
|---------|------|--------|--------------------|
| 1.0.0   | Date | Name   | Initial deployment |

## Section 04 — Database & Storage
Since most apps live in lightweight DBs or Google Sheets, inventory them here.

| Table / Sheet Name | Key Fields | Data Sensitivity | Retention Policy |
|--------------------|------------|------------------|------------------|
| `Raw_Data` | `id`, `date`, `store` | High (PII) | 30 Days then archive |

## Section 05 — API & Automation
Document each endpoint or automated function individually.

* **Endpoint / Function:** `/api/v1/process` or `runMain()`
* **Method:** `POST`
* **Auth / Credentials:** [Where are secrets stored? e.g., GitHub Secrets, Script Properties]
* **Rate Limits:** [e.g., 50 requests per minute]
* **Failure Behavior:** [e.g., Retries 3 times, then alerts L2 Support]

## Section 06 — Deployment & Environment Config
* **Production Environment:** [Where does the live version live?]
* **Staging Environment:** [Where do we test?]
* **Environment Constants:** [List any specific variables like `PROD_URL` vs `STAGING_URL`]

## Section 07 — Known Issues & Change Log
!!! failure "Fragile Components (For BPO Handoffs)"
    * **Known Issue 1:** The script times out if the PDF is over 50 pages. 
    * **Workaround:** Split the PDF before uploading.

## Section 08 — Access, Permissions & Contacts
| Escalation Tier | Role | Contact Person | When to Contact |
|-----------------|------|----------------|-----------------|
| **L1** | BPO / Operations | [Name] | Basic usage, password resets |
| **L2** | Technical / Dev | [Name] | Script failures, API timeouts |
| **L3** | Ops / CEO | [Name] | Access approvals, feature requests |