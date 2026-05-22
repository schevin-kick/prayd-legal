# Prayd — public legal pages (for GitHub Pages)

`privacy.html`, `terms.html`, `index.html` — generated from the in-app text via `node scripts/genlegal.mjs`
(edit `app/settings/privacy.tsx` / `terms.tsx`, then regenerate to keep them in sync).

## Publish on GitHub Pages
1. Create a **new public repo** on GitHub, e.g. `prayd-legal`.
2. Add these three files to it. Easiest path: on github.com → the new repo → **Add file → Upload files** → drag `privacy.html`, `terms.html`, `index.html`. Commit.
   *(Or via git: `cd legal && git init && git add . && git commit -m "legal" && git branch -M main && git remote add origin https://github.com/<you>/prayd-legal.git && git push -u origin main`)*
3. Repo → **Settings → Pages** → Source: **Deploy from a branch** → Branch **main**, folder **/(root)** → **Save**.
4. Wait ~1 minute. Your URLs:
   - Privacy: `https://<you>.github.io/prayd-legal/privacy.html`
   - Terms:   `https://<you>.github.io/prayd-legal/terms.html`

## Where to paste them
- **App Store Connect** → your app → App Privacy → **Privacy Policy URL** (Privacy). Terms can go in the description or EULA field.
- **Google Play Console** → Store listing / App content → **Privacy Policy** (Privacy URL).

## Contact email
All pages use **hello.prayd@outlook.com** (one address for privacy, DMCA, and support). To change it later, edit `app/settings/privacy.tsx` + `terms.tsx` and re-run `node scripts/genlegal.mjs`.
