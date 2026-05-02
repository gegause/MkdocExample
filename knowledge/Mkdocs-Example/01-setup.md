# 1. Project Setup

This document walks you through preparing a GitHub repository to host a documentation site built with MkDocs. It covers installation, repository structure, local development, and preparing your Markdown content.

## 1. Overview

MkDocs is a static site generator designed for project documentation. It converts Markdown files into a clean, searchable website that can be deployed directly to GitHub Pages.

This example repository demonstrates:
- How to structure your Markdown files
- How to install MkDocs and plugins
- How to preview your site locally
- How to prepare for deployment

## 2. Prerequisites

Before you begin, ensure you have:

Python 3.8+ installed  
Check with: python --version

pip (Python package manager)  
Check with: pip --version

Git installed  
Check with: git --version

A GitHub account

## 3. Create or Clone the Repository

Option A — Create a new repository on GitHub  
1. Go to GitHub → New Repository  
2. Name it something like: MkdocExample  
3. Clone it locally:  
git clone https://github.com/<your-user>/MkdocExample  
cd MkdocExample

Option B — Use an existing repository  
cd <your-repo>

## 4. Create the Documentation Directory

MkDocs needs a directory containing your Markdown files. In this example, we use a folder named “knowledge”.

Create it:  
mkdir knowledge

Add your Markdown files inside this folder. For example:  
knowledge/  
  01-setup.md  
  02-configuration.md  
  03-deployment.md  
  04-testing.md  
  05-troubleshooting.md

MkDocs will treat this folder as the root of your documentation.

## 5. Install MkDocs and Required Plugins

Install MkDocs:  
pip install mkdocs

Install the Material theme:  
pip install mkdocs-material

Install the Awesome Pages plugin (for automatic navigation):  
pip install mkdocs-awesome-pages-plugin

Verify installation:  
mkdocs --version

You should see something like:  
mkdocs, version X.X.X

## 6. Create the MkDocs Configuration File

At the root of your repository, create a file named:  
mkdocs.yml

Add the following minimal configuration:

site_name: MkDocs Example Site  
docs_dir: knowledge  

theme:  
  name: material  

plugins:  
  - search  
  - awesome-pages  

This configuration:
- Sets the site title  
- Points MkDocs to the “knowledge” directory  
- Enables the Material theme  
- Enables search and auto-navigation  

## 7. Preview the Site Locally

From the root of your repository, run:  
mkdocs serve

This starts a local development server.

Open the site in your browser:  
http://127.0.0.1:8000

As you edit Markdown files, the site will automatically refresh.

## 8. Verify Your File Structure

Your repository should now look like this:

MkdocExample/  
  knowledge/  
    01-setup.md  
    02-configuration.md  
    03-deployment.md  
    04-testing.md  
    05-troubleshooting.md  
  mkdocs.yml

If this structure is correct, MkDocs will build and serve your site without issues.

## 9. Commit Your Work

Once everything is set up, commit your changes:

git add .  
git commit -m "Initial MkDocs setup with documentation files"  
git push

Your repository is now ready for deployment to GitHub Pages (covered in 03-deployment.md).

## 10. Next Steps

Continue to:
- 02-configuration.md to learn how to customize your MkDocs site  
- 03-deployment.md to deploy your site to GitHub Pages  
- 04-testing.md to verify your deployment  
- 05-troubleshooting.md for common issues  

Your MkDocs project is now fully initialized and ready for configuration and deployment.