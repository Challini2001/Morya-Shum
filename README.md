# Morya Shum — website

A static, single-page site. No build step, no dependencies — `index.html` plus an `assets/` folder of images. Fonts load from Google Fonts at runtime.

```
.
├── index.html
├── assets/            product, process, and logo images
├── netlify.toml       tells Netlify how to publish this repo
└── .gitignore
```

## 1. Push this to GitHub

From inside this folder:

```bash
git init
git add .
git commit -m "Initial site"
git branch -M main
git remote add origin https://github.com/<your-username>/<your-repo>.git
git push -u origin main
```

(Create the empty repo on GitHub first — github.com/new — then use the URL it gives you in place of the one above.)

## 2. Connect it to Netlify

1. Go to [app.netlify.com](https://app.netlify.com) and log in.
2. **Add new site → Import an existing project → Deploy with GitHub**.
3. Authorize Netlify and pick this repository.
4. Build settings are already read from `netlify.toml` — leave the build command empty and the publish directory as `.` (repo root). Click **Deploy**.

Netlify will give you a `*.netlify.app` URL immediately. Every push to `main` redeploys automatically.

## 3. Optional: custom domain

**Site settings → Domain management → Add a domain**, then point your domain's DNS at Netlify (either their nameservers, or a CNAME to your `*.netlify.app` address) as instructed on that screen.

## Editing content later

Everything — copy, product info, section order — lives in `index.html` as plain HTML/CSS. Images referenced as `assets/filename.jpg`; add new ones to `assets/` and reference them the same way. No rebuild step: commit and push, Netlify redeploys.
