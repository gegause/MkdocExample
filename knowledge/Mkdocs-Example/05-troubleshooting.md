# 5. Troubleshooting

This document lists common MkDocs and GitHub Pages issues and how to resolve them.

---

## Issue: GitHub Pages shows a 404

Fix:
- Ensure the gh-pages branch exists
- Ensure GitHub Pages is configured to use gh-pages
- Wait 1–3 minutes for GitHub Pages to build

---

## Issue: Navigation is missing

Fix:
- Ensure awesome-pages is listed in mkdocs.yml
- Ensure filenames are valid
- Ensure no empty directories exist

---

## Issue: Local build works, GitHub Pages does not

Fix:
Check that mkdocs.yml contains:

docs_dir: knowledge

If GitHub Pages cannot find your docs, it will render a blank site.

---

## Issue: mkdocs gh-deploy fails

Fix:
Install required packages:

pip install mkdocs  
pip install mkdocs-material  
pip install mkdocs-awesome-pages-plugin

Then try again.

---

## Issue: GitHub Actions workflow fails

Fix:
Ensure your workflow installs all required plugins:

pip install mkdocs-material mkdocs-awesome-pages-plugin
