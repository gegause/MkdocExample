
---

# 📄 `knowledge/05-troubleshooting.md`

```markdown
# 5. Troubleshooting

Common issues and how to fix them.

---

## ❌ Issue: GitHub Pages shows a 404

### ✔ Fix
- Ensure the `gh-pages` branch exists
- Ensure GitHub Pages is configured to use `gh-pages`
- Wait 1–3 minutes for GitHub Pages to build

---

## ❌ Issue: Navigation is missing

### ✔ Fix
If using `awesome-pages`:

- Ensure the plugin is listed in `mkdocs.yml`
- Ensure your Markdown files have valid filenames
- Ensure there are no empty directories

---

## ❌ Issue: Local build works, GitHub Pages does not

### ✔ Fix
Check:

```yaml
docs_dir: knowledge
