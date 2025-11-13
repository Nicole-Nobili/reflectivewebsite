# Hugo + PaperMod starter

This repo gives you a minimal site that looks like the Physical Intelligence homepage:
- Simple top nav (Home / Research / Join Us)
- Clean list of dated posts
- Markdown content

## 1) Install Hugo

- macOS: `brew install hugo`
- Linux: download from https://github.com/gohugoio/hugo/releases (choose the **extended** build)
- Windows (winget): `winget install Hugo.Hugo.Extended`

Verify: `hugo version`

## 2) Get the PaperMod theme

In this repo (after you `git init`), add PaperMod as a submodule:

```bash
git submodule add https://github.com/adityatelange/hugo-PaperMod themes/PaperMod
```

## 3) Run locally

```bash
hugo server -D
```

Then open http://localhost:1313

## 4) Edit content

- Homepage text: in `hugo.toml` under `[params.homeInfoParams]`
- Navigation: `hugo.toml` under `[menu]`
- Posts: add Markdown files under `content/posts/` with front matter:

```markdown
---
title: "My New Post"
date: 2025-06-01
description: "One-liner shown in the list."
draft: false
---

Your content here.
```

## 5) Deploy to GitHub Pages

Create a new repo on GitHub and push this folder. Then GitHub Actions will build and publish to the `gh-pages` branch using the workflow in `.github/workflows/gh-pages.yml`.

- In GitHub: **Settings → Pages** → set the branch to **gh-pages** / root
- Optional: set a custom domain, add a `CNAME` file under `static/CNAME` with your domain name.

## 6) Update `baseURL`

In `hugo.toml` set:

```
baseURL = "https://<your-username>.github.io/<repo-name>/"
```

(If you use a custom domain, set it to `https://yourdomain.com/`.)

## 7) Create a new post

```bash
hugo new content/posts/my-next-thing.md
# edit the file, then
hugo server -D
```

Enjoy!
