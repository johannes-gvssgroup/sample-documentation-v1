# 🚀 GVVSS Documentation Portal Repository

This repository contains the source code for the **GVVSS Documentation Portal**. 

It uses a **"Docs-as-Code"** pipeline. Our operational manuals are version-controlled, peer-reviewed, and deployed automatically via GitHub Actions, ensuring our team always has access to the most up-to-date procedures.

## 🌐 Live Website Links
* **Portal Link:** [https://johannes-gvssgroup.github.io/sample-documentation-v1/](https://johannes-gvssgroup.github.io/sample-documentation-v1/)
* **Version:** 1.0 (Latest)

---

## ⚙️ How the System Works
You do not need to know HTML to update the website. The pipeline handles everything:
1. **Write:** You write your manual using simple Markdown (`.md`) files.
2. **Push:** You save (commit) your changes to the `main` branch.
3. **Deploy:** GitHub Actions uses **MkDocs Material** to automatically convert your text into a styled web page and updates the live site.

## 📂 Repository Structure
* `mkdocs.yml`: The main settings file. Edit this to change colors, logos, or the top menu.
* `.github/workflows/deploy.yml`: The automation script that builds the site.
* `docs/`: The main folder. **All of your manuals, templates, and images live here.**

---

## ✍️ How to Add or Edit Documentation

1. Open the `docs/` folder in GitHub.
2. To edit an existing guide, click on the file (e.g., `docs/ocr-system/index.md`) and click the pencil icon to edit. 
3. To create a new guide, create a new folder, copy the text from `docs/template/index.md`, and fill it out.
4. Drop any screenshots into your folder (e.g., `docs/ocr-system/files/image/1.jpg`).
5. If you created a brand new page, open `mkdocs.yml` and add the link under the `nav:` section so it shows up in the menu.
6. **Commit your changes.** The website will automatically update in 1-2 minutes.

---

## 🔄 Versioning Guide (For Admins)

We use a tool called **`mike`** to handle version control. This creates the version dropdown menu in the top right corner of the live website.

### For Daily Edits (Status Quo)
Do not change the version number! Just edit the `.md` files and push to GitHub. The system will overwrite the current `1.0` folder with your new edits automatically.

### For Major Process Changes (Releasing a new version)
If GVVSS changes a massive process and we want to archive the old `1.0` rules forever, we release a new version.
1. Open `.github/workflows/deploy.yml`.
2. Find the deployment command at the very bottom:
   `mike deploy --push --update-aliases 1.0 latest`
3. Change `1.0` to `1.1` (or `2.0`).
4. Commit and push.
5. The system will freeze the old folder forever, create a brand new `1.1` folder, and update the website's dropdown menu so users can toggle between the old and new rules.