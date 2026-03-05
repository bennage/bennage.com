# bennage.com

The official and very serious website of the Bennage family.

A single-page static site hosted on [GitHub Pages](https://pages.github.com/).

## Local Development

No build tools needed. Just open `index.html` in a browser:

```sh
# macOS
open index.html

# Windows
start index.html

# or use any local server
python -m http.server 8000
npx serve .
```

## Adding Photos

1. Drop your photos into the `images/` directory
2. Edit `index.html` — replace the `src="images/placeholder-N.svg"` with your image filenames
3. Update the `alt` text to describe each photo
4. Optionally update the `<figcaption>` with a funny caption

**Tip:** For best results, optimize images before committing (aim for < 500KB each). Tools like [Squoosh](https://squoosh.app/) work great.

## DNS Setup (DNSimple → GitHub Pages)

Add these records in your [DNSimple dashboard](https://dnsimple.com/):

### Apex domain (`bennage.com`)

| Type | Name | Value             |
|------|------|-------------------|
| A    |      | 185.199.108.153   |
| A    |      | 185.199.109.153   |
| A    |      | 185.199.110.153   |
| A    |      | 185.199.111.153   |

### www subdomain

| Type  | Name | Value                          |
|-------|------|--------------------------------|
| CNAME | www  | `<your-username>.github.io`    |

> Replace `<your-username>` with your GitHub username.

### Enable GitHub Pages

1. Push this repo to GitHub
2. Go to **Settings → Pages**
3. Source: **Deploy from a branch** → **main** / **/ (root)**
4. Custom domain: `bennage.com`
5. Check **Enforce HTTPS** (may take a few minutes to provision the certificate)

## Git Worktrees

This repo is set up to support [git worktrees](https://git-scm.com/docs/git-worktree). To create a worktree for a feature branch:

```sh
git worktree add ../bennage-feature feature-branch-name
```
