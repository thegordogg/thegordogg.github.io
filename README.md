# thegordogg.github.io

Portfolio site for Gordon Heltzel (https://thegordogg.github.io). Hosted free on GitHub Pages; built automatically by Jekyll from the Markdown files in this repository. No local tools are needed to edit it.

## How to edit text

1. On github.com, open the file (for example `work/assistant-benchmarking.md`).
2. Click the pencil icon (Edit this file), change the text, click **Commit changes**.
3. The site rebuilds in about a minute. Hard-refresh the page if you still see the old text.

Each page starts with a small block between `---` lines (the "front matter"): `title` is the page title and browser tab; `description` is what Google and LinkedIn previews show. Everything below the second `---` is ordinary Markdown.

## Where things are

| You want to change | File |
|---|---|
| Home page | `index.md` |
| Work list and the two short "Also" items | `work/index.md` |
| A case study | `work/<name>.md` |
| How I work | `methods.md` |
| Publications | `publications.md` |
| About | `about.md` |
| Résumé PDF | replace `assets/Gordon_Heltzel_Resume.pdf` (upload a file with the same name) |
| Images | `assets/img/` (upload, then reference as `/assets/img/filename.jpg`) |
| Navigation, footer | `_layouts/default.html` |
| Colors, fonts, spacing | `assets/css/style.css` |
| Site title, email, LinkedIn, Scholar links | `_config.yml` |

## Adding a case study

1. In `work/`, click **Add file > Create new file**, name it `work/short-name.md`.
2. Paste the contents of an existing case study, change the front matter and the text. Keep the shape: decision at stake, what I did, what changed, what I'd do differently.
3. Add a link to it in `work/index.md` (and on `index.md` if it belongs in Selected work).

## Rules for anything on this site

- Public-safe only: method numbers (sample sizes, agreement statistics) yes; metric values, lifts, shares, partner or competitor names, unreleased features, internal tools no. Figures from industry work are illustrative and say so.
- Outcome first, then method, then n.
- Plain sentences; no buzzwords; no em dashes.

## Custom domain (optional, later)

Buy a domain (about $10–15/year). In the repository: Settings > Pages > Custom domain, enter it and save (GitHub creates a `CNAME` file). At the registrar, add a CNAME record for `www` pointing to `<username>.github.io` and the four GitHub A records for the apex domain (listed in GitHub's Pages docs). Tick "Enforce HTTPS" once it verifies.
