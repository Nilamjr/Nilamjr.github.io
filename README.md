# Nilam Rakholiya — Portfolio Site

A plain HTML/CSS/JS portfolio site — no build step, no framework, so it
deploys straight to GitHub Pages for free.

## Structure

```
index.html                              → homepage (about, experience, projects, blog preview, contact)
styles.css                              → shared design system
script.js                               → mobile nav toggle
blog/
  index.html                            → blog listing page
  day-1-2-shopify-theme-setup.html      → first blog post
assets/
  images/                                → screenshots used in blog posts
  resume/nilam-rakholiya-resume.pdf     → downloadable résumé
```

## Before you deploy — three things to update

1. **GitHub links.** Search every HTML file for `Nilamjr` and
   replace it with your actual GitHub username (and real repo names once
   those repos exist - the theme repo, the product automation repo, etc).
   Easiest way: open the project folder in VS Code, use **Find & Replace
   in Files** (Ctrl+Shift+H / Cmd+Shift+H), search `Nilamjr`,
   replace with your username.

2. **Headline.** The hero currently uses "Front-End Developer · Shopify &
   E-Commerce Specialist" — swap it in `index.html` for whichever headline
   you land on.

3. **Project cards.** Update the status (`Live` / `In progress`) and
   descriptions in the Projects section as those repos actually get built.

## Deploying to GitHub Pages (free, no domain needed)

1. Create a new GitHub repository named **exactly**
   `Nilamjr.github.io` (this exact naming is what makes
   GitHub serve it automatically at the root URL, no extra config).
2. Push this whole folder's contents into that repo:
   ```
   git init
   git add .
   git commit -m "Initial portfolio site"
   git branch -M main
   git remote add origin https://github.com/Nilamjr/Nilamjr.github.io.git
   git push -u origin main
   ```
3. In the repo on GitHub: **Settings → Pages** → under "Build and
   deployment," Source should already show "Deploy from a branch," branch
   `main`, folder `/ (root)`. If not, set it and save.
4. Wait 1–2 minutes, then visit `https://Nilamjr.github.io` —
   it's live.

Every time you `git push` after this, the live site updates automatically
within a minute or two — no redeploy step needed.

## Adding a new blog post later (Day 3 onward)

1. Duplicate `blog/day-1-2-shopify-theme-setup.html` as a new file, e.g.
   `blog/day-3-header-mega-menu.html`.
2. Replace the title, meta description, header text, and the article body
   with the new post's content. Keep the same `<nav>`, `<header
   class="post-header">`, and `<footer>` structure so it matches the rest
   of the site.
3. Add a new entry to the `post-list` in `blog/index.html`, and to the
   blog preview section in `index.html`, following the existing pattern
   (there's a commented example already in `blog/index.html`).
4. Drop any new screenshots into `assets/images/`.
