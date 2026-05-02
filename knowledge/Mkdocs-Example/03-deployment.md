# 3. Deployment to GitHub Pages

This document explains how to deploy your MkDocs site to GitHub Pages using the built-in deployment command.

## 1. Overview

MkDocs includes a command that automatically:
- Builds your documentation site
- Creates or updates a branch named gh-pages
- Pushes the built site to GitHub

Once deployed, GitHub Pages hosts your site publicly.

## 2. Deploy the Site

From the root of your repository, run:

mkdocs gh-deploy

This command:
- Builds the site into a temporary directory
- Pushes the output to the gh-pages branch
- Creates the branch if it does not exist

## 3. Enable GitHub Pages

In GitHub:
1. Go to Settings  
2. Select Pages  
3. Under Source, choose:  
   Branch: gh-pages  
   Folder: / (root)

GitHub will publish your site at:

https://<your-user>.github.io/<repo>/

Example:  
https://gegause.github.io/MkdocExample/

## 4. Force Deployment (Optional)

If you need to overwrite the gh-pages branch:

mkdocs gh-deploy --force

## 5. Automate Deployment with GitHub Actions (Optional)

Create a workflow file at:  
.github/workflows/ci.yml

Add:

name: ci  
on:  
  push:  
    branches: [ main ]  

permissions:  
  contents: write  

jobs:  
  deploy:  
    runs-on: ubuntu-latest  
    steps:  
      - uses: actions/checkout@v4  
      - uses: actions/setup-python@v5  
        with:  
          python-version: 3.x  
      - run: pip install mkdocs-material mkdocs-awesome-pages-plugin  
      - run: mkdocs gh-deploy --force

This automatically deploys your site whenever you push to main.
