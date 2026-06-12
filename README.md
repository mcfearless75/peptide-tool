# CC PEP — Peptide Reference & Reconstitution Tool

A single-file, static web tool. Pick a peptide for its profile (benefits, route,
half-life, pairings, cautions, evidence status), then reconstitute and read off the
IU draw for a dose you choose. Mobile-responsive, animated, no backend, no dependencies.

## Files
- `index.html` — the entire app (everything is in here)
- `.nojekyll` — tells GitHub Pages to serve files as-is (no Jekyll processing)
- `CNAME` — (optional) add this only if using a custom domain

---

## Deploy to GitHub Pages (2 minutes)

### Option A — new repo (cleanest)
1. github.com → **New repository** → name it `peptide-tool` → **Public** → Create.
2. **Add file → Upload files** → drag in `index.html` and `.nojekyll` → **Commit**.
3. **Settings → Pages** → Source: **Deploy from a branch** → Branch: **main** / **/(root)** → **Save**.
4. Wait ~60 seconds. Live at:
   `https://mcfearless75.github.io/peptide-tool/`

### Option B — fold into an existing repo
1. Upload `index.html` into a subfolder, e.g. `/tools/peptide/index.html`.
2. With Pages already enabled on that repo, it's live at:
   `https://mcfearless75.github.io/<repo>/tools/peptide/`

---

## Custom domain (recommended for customer-facing use)

A branded subdomain reads far better than a github.io URL, e.g. `tools.cc-pep.com`.

1. Rename `CNAME.example` to `CNAME` and put **one line** in it — your domain only:
   ```
   tools.cc-pep.com
   ```
2. Commit it to the repo root.
3. At your DNS provider (GoDaddy / Cloudflare / wherever cc-pep.com lives), add:
   - **Type:** CNAME
   - **Name/Host:** `tools`
   - **Value/Target:** `mcfearless75.github.io`
4. Back in **Settings → Pages → Custom domain**, enter `tools.cc-pep.com` → Save.
5. Tick **Enforce HTTPS** once the certificate provisions (a few minutes to ~1 hr).

---

## Updating it later
Edit `index.html` in the repo (or re-upload) and commit. Pages redeploys automatically
in under a minute. Hard-refresh (Ctrl/Cmd+Shift+R) to bust the cache if you don't see changes.

## Notes
- Keep the deployed version factual and research-use framed (as built). A reconstitution/
  reference tool is benign; dosing-protocol content risks host AUP and payment-processor flags.
- Entirely client-side — no data leaves the browser, nothing to maintain server-side.
