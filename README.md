# 📘 gh-pages · GitHub Actions Template

![Deploy Status](https://github.com/TamerOnLine/gh-pages/actions/workflows/deploy.yml/badge.svg)

🎯 This is a reusable GitHub Actions **template** for deploying [MkDocs](https://www.mkdocs.org/) sites to GitHub Pages.

> 🧩 Use this template in any repository to instantly add a working `gh-pages` deployment workflow — no extra setup needed.

---

## ✅ Features

- Deploys your MkDocs site automatically on push to `main`
- Built-in support for Python 3.12
- Easy to plug into any project with one line of code
- Supports private and public repositories

---

## 📦 Requirements in Your Target Project

Add a file named `gh-pages-requirements.txt` in your project’s root:

```txt
mkdocs
mkdocs-material
# ... other plugins or themes
```

---

## 🚀 Usage (in your target project)

In your own repository, create the workflow file (e.g., `.github/workflows/deploy.yml`) and use:

```yaml
name: 📘 Deploy Docs

on:
  push:
    branches: [main]

jobs:
  deploy:
    uses: TamerOnLine/gh-pages/.github/workflows/deploy.yml@main
    secrets:
      GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
```

That’s it! 🎉  
When you push to `main`, MkDocs will build and deploy your documentation to GitHub Pages.

---

## 🛠 Maintained by [@TamerOnLine](https://github.com/TamerOnLine)

License: MIT  
Status: ✅ Ready for reuse
