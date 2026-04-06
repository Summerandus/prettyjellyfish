# prettyjellyfish

Personal site — [prettyjellyfish.com](https://prettyjellyfish.com)

## Structure

```
prettyjellyfish/
├── _layouts/
│   ├── base.html       # nav, footer, canvas animation, cursor
│   ├── post.html       # writing article template
│   └── work.html       # work item template
├── _posts/             # writing — one file per post
│   └── YYYY-MM-DD-slug.md
├── _work/              # work items — one file per project
│   └── project-name.md
├── writing/
│   └── index.html      # all writing page
├── _config.yml
└── index.html          # homepage
```

## Adding a new post

Create a file in `_posts/` named `YYYY-MM-DD-your-title.md`:

```markdown
---
title: "your title here"
date: 2026-04-06
tags: [writing, water]
---

Your content here. Markdown works normally.

You can use **bold**, *italic*, and > blockquotes.
```

Push to main — it deploys automatically.

## Adding a work item

Create a file in `_work/` named `project-name.md`:

```markdown
---
title: "Project Name"
title_zh: "项目名称"
desc: "data · systems · 2026"
desc_zh: "数据 · 系统 · 2026"
order: 4
image: /assets/images/project-name.jpg  # optional
coming_soon: false
---

Description of the project...
```

## GitHub Pages setup

1. Go to repo Settings → Pages
2. Source: **GitHub Actions**
3. The workflow in `.github/workflows/deploy.yml` handles the rest

## Local preview (optional)

```bash
gem install bundler jekyll
bundle init
bundle add jekyll
bundle exec jekyll serve
```
