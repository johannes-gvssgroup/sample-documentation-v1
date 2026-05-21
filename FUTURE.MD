# 🗺️ GVVSS Documentation Portal — Future Roadmap & Improvements

This file tracks planned features, structural updates, and styling adjustments intended to improve the utility, compliance, and appearance of the documentation portal.

---

## 🎨 1. UI & Branding Customization (Design Updates)
*Targeting feedback regarding the portal's style and visual presentation.*

* [ ] **Implement Custom Corporate CSS:** Create a `docs/stylesheets/custom.css` file to override the default Material theme colors. Map the primary header and accent colors to match official GVVSS corporate branding.
* [ ] **Typography Standardization:** Update `mkdocs.yml` to pull specific Google Fonts (e.g., Roboto or Open Sans) preferred by leadership instead of the default theme fonts.
* [ ] **Custom HTML Overrides:** Utilize the `overrides/` folder directory on the `main` branch to customize structural layouts (e.g., adding a persistent company footer or modifying the search bar layout) without breaking the build pipeline.

---

## 📊 2. Visual & Content Enhancements (For the BPO Team)
*Improving how information is consumed by offshore and operations teams.*

* [ ] **Text-Based Flowcharts (Mermaid.js):** Enable the Material theme's native Mermaid.js extension. This allows developers to type flowcharts in plain text and render them as clean, interactive process diagrams directly inside "Section 02 — Process Flow" pages.
* [ ] **Automated PDF Export:** Install the `mkdocs-pdf-export-plugin` to automatically compile and generate downloadable offline PDF manuals every time the site builds. This is critical for external regulatory audits.
* [ ] **Page Feedback System:** Integrate a simple "Was this page helpful? [Yes] [No]" widget at the footer of documents to gather data on which workflows need rewriting.

---

## 🛡️ 3. Automation, Governance & Security (System Admin)
*Protecting the integrity of our documentation and creating bulletproof audit trails.*

* [ ] **Enforce Pull Request Workflows:** Transition away from committing directly to the `main` branch. Require all changes to be submitted via a Git "Pull Request" (PR) so that updates must be peer-reviewed and approved by a technical manager before going live.
* [ ] **Automated Broken Link Checking:** Add a nightly GitHub Action (using a tool like `lychee`) to scan all Markdown files. If a Google Drive folder ID changes or an external link breaks, it should automatically alert the system administrator.
* [ ] **Google Analytics Integration:** Paste a tracking ID into `mkdocs.yml` to monitor portal traffic. This will show which manuals are viewed most frequently and what terms the BPO team is searching for.
* [ ] **Evaluate Secure Hosting (Long-term):** If documents become too sensitive for a public GitHub Pages deployment, evaluate moving the repository to **Private** status and hosting the static files behind a corporate server or a secure host utilizing employee email verification (2FA).