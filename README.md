# Quarto Website Starter (CV + Papers)

A minimal website to host your CV and papers using **Quarto** + **GitHub Pages** (free).

## 1) Install prerequisites (Windows/macOS/Linux)

- Install **Git**: <https://git-scm.com/downloads>
- Install **Quarto**: <https://quarto.org/docs/get-started/>
  - (No R or Python is required unless you want notebooks.)

## 2) Preview locally

```bash
quarto preview
```

This starts a local server (usually http://localhost:4200). Edits hot-reload.

## 3) Add your content

- Replace "Your Name" in `_quarto.yml` and in `index.qmd`.
- Put your CV at `cv/cv.pdf`.
- Put your papers in `papers/` and link them from `research.qmd`.

## 4) Publish to GitHub Pages (simplest)

1. Create a new **public** repo on GitHub (e.g., `my-site`), **empty** (no README).
2. In this folder, initialize git and push:

```bash
git init
git add .
git commit -m "Initial site"
git branch -M main
git remote add origin https://github.com/<your-username>/<your-repo>.git
git push -u origin main
```

3. Publish with Quarto (will create a `gh-pages` branch):

```bash
quarto publish gh-pages
```

4. GitHub will serve your site at: `https://<your-username>.github.io/<your-repo>/`

If you see 404 initially, wait 1–2 minutes and refresh.

## 5) Optional: custom domain

1. Buy a domain (e.g., from Namecheap, Google Domains, Cloudflare, etc.).
2. In GitHub → Repo → Settings → Pages, set your custom domain and save.
3. Your repo will get a `CNAME` file. In your DNS, create records:
   - `A` records pointing the root `@` to GitHub Pages IPs.
   - `CNAME` record for `www` pointing to `<your-username>.github.io.`
4. DNS can take a while to propagate.

## 6) Update the site

- Edit files, commit, and run again:

```bash
git add -A
git commit -m "Update content"
git push
quarto publish gh-pages
```

You're done!
