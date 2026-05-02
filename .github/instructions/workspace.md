# Workspace Best Practices

## Project Structure
- Keep documentation in `docs/` or `knowledge/` directory
- Use `mkdocs.yml` for configuration
- Store assets (images, files) in appropriate subdirectories
- Use `README.md` as project overview

## File Naming
- Use lowercase with hyphens for file names (e.g., `getting-started.md`)
- Use descriptive, SEO-friendly names
- Avoid spaces and special characters in filenames
- Use `index.md` for directory index pages

## Content Organization
- Group related topics in subdirectories
- Use consistent hierarchy (topic/subtopic/file.md)
- Maintain table of contents in mkdocs.yml
- Use front matter for page metadata (title, description, etc.)

## MkDocs Conventions
- Configure navigation in mkdocs.yml
- Use themes and plugins appropriately
- Enable search and navigation features
- Test builds locally before committing

## Git Practices
- Commit frequently with descriptive messages
- Use branches for new features
- Keep .gitignore updated for build artifacts
- Use semantic versioning for releases

## Code Quality
- Follow Markdown best practices
- Validate links and references
- Keep content up-to-date
- Use consistent formatting across files

## Collaboration
- Use issues for feature requests and bugs
- Review pull requests thoroughly
- Document contribution guidelines
- Maintain changelog for updates