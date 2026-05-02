# 2. MkDocs Configuration

This document explains how to configure MkDocs for your project, including site settings, themes, plugins, and navigation behavior.

## 1. Purpose of mkdocs.yml

MkDocs uses a single configuration file named mkdocs.yml located at the root of your repository. This file controls:
- Site name
- Theme selection
- Plugin activation
- Documentation directory
- Navigation behavior

## 2. Basic Configuration

Create a file named mkdocs.yml at the root of your repository and add the following:

site_name: MkDocs Example Site  
docs_dir: knowledge  

theme:  
  name: material  

plugins:  
  - search  
  - awesome-pages  

This configuration:
- Sets the site title
- Points MkDocs to the knowledge directory
- Enables the Material theme
- Enables built-in search
- Enables automatic navigation generation

## 3. Understanding Key Settings

site_name  
Displayed at the top of your documentation site.

docs_dir  
Specifies the folder containing your Markdown files.  
This example uses: knowledge

theme  
Material provides a modern, responsive UI.

plugins  
search enables full-text search.  
awesome-pages automatically builds navigation based on folder structure.

## 4. Optional Enhancements

You may add optional features later, such as:

markdown_extensions:  
  - admonition  
  - toc  
  - tables  

extra_css:  
  - stylesheets/custom.css  

extra_javascript:  
  - scripts/custom.js  

These are optional and not required for the basic example.

## 5. Validate Configuration

To test your configuration, run:

mkdocs serve

Then open:

http://127.0.0.1:8000

If the site loads correctly, your configuration is valid.
