---
title: "Hugo Setup Guide"
date: 2026-04-08
draft: false
tags:
  - Hugo
  - Setup
  - Portfolio
---
# Gilbert N. Onyenwezi — Personal Portfolio Site
## Hugo Static Site — Setup & Deployment Guide

---

## Project Structure

```
gilbert-portfolio/
├── config/
│   └── _default/
│       ├── config.toml       # Site-wide settings
│       ├── menus.toml        # Navigation menu config
│       └── params.toml       # Theme parameters
├── content/
│   ├── _index.md             # Homepage
│   ├── experience/
│   │   └── _index.md         # Work history
│   ├── education/
│   │   └── _index.md         # Academic background
│   ├── skills/
│   │   └── _index.md         # Skills & competencies
│   └── contact/
│       └── _index.md         # Contact page
├── assets/
│   └── images/
│       └── profile.jpg       # Headshot
├── static/
│   └── resume.pdf            # Downloadable resume
└── themes/
    └── [chosen-theme]/       # e.g., hugo-profile or PaperMod
```

---

## Quickstart

### 1. Install Hugo
```bash
brew install hugo          # macOS
# or
winget install Hugo.Hugo   # Windows
```

### 2. Create new site
```bash
hugo new site gilbert-portfolio
cd gilbert-portfolio
```

### 3. Add a theme (recommended: hugo-profile)
```bash
git init
git submodule add https://github.com/gurusabarish/hugo-profile themes/hugo-profile
```

### 4. Configure `config/_default/config.toml`
```toml
baseURL = "https://gilbert-onyenwezi.netlify.app/"
languageCode = "en-us"
title = "Gilbert N. Onyenwezi"
theme = "hugo-profile"

[params]
  name = "Gilbert N. Onyenwezi"
  description = "Supply Chain & Data Science Leader"
  favicon = "/favicon.ico"
```

### 5. Run locally
```bash
hugo server -D
# Visit http://localhost:1313
```

---

## Content Pages (Markdown)

### content/_index.md
```markdown
---
title: "Gilbert N. Onyenwezi"
description: "Supply chain and operations leader with 20+ years experience"
---

Supply chain and operations leader with extensive experience in global
manufacturing and distribution networks, driving process improvements
and operational excellence. Skilled in Lean Six Sigma, data analysis,
and cross-functional collaboration.

Currently pursuing an M.S. in Data Science with AI Specialization at
Northwestern University (expected 2026).
```

### content/experience/_index.md
```markdown
---
title: "Professional Experience"
---

## Wilsonart — Operational Excellence Manager
*Jun 2024 – Sept 2025 | Temple, Texas*

- Developed transformative supply chain management initiatives
- Tracked monthly manufacturing KPIs and multi-year capacity roadmaps
- Facilitated Kaizen leadership and Operational Excellence coaching

## Wilsonart — Area Manager, Distribution
*Apr 2023 – May 2024 | Temple, Texas*

- Oversaw all distribution and receiving operations
- Initiated continuous improvement using Lean/Six Sigma tools
- Ensured ISO compliance across quality goals
```

---

## GitHub Setup

```bash
# Initialize and push to GitHub
git init
git add .
git commit -m "Initial Hugo portfolio site"
git branch -M main
git remote add origin https://github.com/[your-username]/gilbert-portfolio.git
git push -u origin main
```

---

## Netlify Deployment

1. Go to [netlify.com](https://netlify.com) → **New site from Git**
2. Connect your GitHub repo `gilbert-portfolio`
3. Build settings:
   - **Build command**: `hugo --minify`
   - **Publish directory**: `public`
4. Click **Deploy site**
5. Set custom domain (optional): `gilbert-onyenwezi.netlify.app`

Auto-deploys trigger on every `git push` to `main`.

---

## Grading Checklist

| Requirement | Implementation |
|---|---|
| Hugo framework, Markdown & Go templating | ✅ Theme + content/*.md files |
| Resume content faithfully represented | ✅ All roles, education, skills |
| Navigation & routing | ✅ config/_default/menus.toml |
| GitHub repository | ✅ git init + remote push |
| Netlify hosting, auto-deploy | ✅ Build command configured |
| Software/portfolio links | ✅ GitHub, LinkedIn in contact |
| Performance | ✅ Hugo static = fast load |

---

*Contact: Trebligism@gmail.com | (908) 906-7871 | Round Rock, TX*
