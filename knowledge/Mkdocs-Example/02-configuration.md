
---

# 📄 `knowledge/02-configuration.md`

```markdown
# 2. MkDocs Configuration

MkDocs uses a single configuration file named `mkdocs.yml` at the root of your repository.

Below is a minimal configuration tailored for this example.

## Example `mkdocs.yml`

```yaml
site_name: MkDocs Example Site
docs_dir: knowledge

theme:
  name: material

plugins:
  - search
  - awesome-pages
