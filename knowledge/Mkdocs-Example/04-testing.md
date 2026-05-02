# 4. Testing Your MkDocs Site

This document explains how to verify that your MkDocs site is deployed correctly and functioning as expected.

## 1. Confirm the gh-pages Branch Exists

In GitHub:
- Go to the Branches view
- Look for a branch named gh-pages

If it exists, deployment succeeded.

## 2. Verify GitHub Pages Settings

Navigate to:
Settings → Pages

Ensure:
- Source = gh-pages  
- Folder = /  

GitHub should display a confirmation banner with your published URL.

## 3. Visit the Live Site

Open your published URL in a browser:

https://<your-user>.github.io/<repo>/

Example:  
https://gegause.github.io/MkdocExample/

You should see:
- Your site title
- Navigation menu
- Rendered Markdown pages

## 4. Test Local Build

If something looks wrong online, test locally:

mkdocs serve

Then open:

http://127.0.0.1:8000

If the site works locally but not on GitHub Pages, the issue is usually:
- Incorrect docs_dir setting
- Missing mkdocs.yml
- GitHub Pages not pointing to gh-pages
