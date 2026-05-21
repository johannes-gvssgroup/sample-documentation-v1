# 🚀 GVVSS Documentation Portal

This repository contains the source code and Markdown files for the **GVVSS Documentation Portal**. It is built using a "Docs-as-Code" methodology, meaning our operational manuals and system guides are version-controlled, peer-reviewed, and deployed exactly like software.

## 🌐 Live Website
**[Link to your live GitHub Pages URL here]**

## ⚙️ Tech Stack
This portal relies on a fully automated CI/CD pipeline. You do not need to manually write HTML or manage web hosting.
* **[MkDocs](https://www.mkdocs.org/):** The core static site generator that translates our text into web pages.
* **[Material for MkDocs](https://squidfunk.github.io/mkdocs-material/):** The modern, responsive UI theme featuring dark mode and advanced search.
* **[GitHub Actions](https://github.com/features/actions):** The automation engine that builds and deploys the site whenever a change is saved.
* **[Mike](https://github.com/jimporter/mike):** The versioning tool that manages our version dropdown (e.g., v1.0, v2.0) and archives old manuals.

## 📂 Repository Structure
* `mkdocs.yml`: The master configuration file. This controls the site name, color theme, and the left-sidebar navigation menu.
* `.github/workflows/deploy.yml`: The automation script that tells GitHub how to build the site.
* `docs/`: The main directory containing all the raw Markdown (`.md`) files and images. **All content goes here.**

## ✍️ How to Update the Documentation

Updating the live website requires zero coding knowledge. 

1. Navigate to the `docs/` folder.
2. Edit the relevant `.md` file, or create a new one using the standard template.
3. Drop any required images into the respective `files/image/` folder.
4. If you created a *new* file, open `mkdocs.yml` and add it to the `nav:` section.
5. **Commit and Push** your changes to the `main` branch.

As soon as you push your changes, GitHub Actions will automatically wake up, rebuild the website, and publish the update to the live URL within 1–2 minutes.

## 💻 Local Development (For System Admins)
If you need to make massive structural changes and want to preview the site on your local computer before pushing it to the live server, run the following commands in your terminal:

```bash
# Install the required Python packages
pip install mkdocs-material mike

# Start the local live-reload server
mkdocs serve