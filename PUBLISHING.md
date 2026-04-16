# PUBLISHING.md

## GitHub Pages configuration for neuraltube-site

**Repository**: `Z3r0DayZion-install/neuraltube-site` (public)  
**Branch**: `main`  
**Folder**: `/` (repo root)  
**Live URL**: `https://z3r0dayzion-install.github.io/neuraltube-site/`

## Enable steps

1. Go to **Settings → Pages** in the `neuraltube-site` repo
2. Source: **Deploy from a branch**
3. Branch: **`main`**
4. Folder: **`/ (root)`**
5. Click **Save**

Pages propagates within ~2 minutes. The live URL above will resolve once the first deployment completes.

## Post-publish checks

Run after the site goes live:

```bash
NT_PAGES_URL=https://z3r0dayzion-install.github.io/neuraltube-site node tmp_pages_live_check.cjs
```

Expected: 7/7 checks pass, exit code 0.

Manual checks:
- Homepage loads and hero renders
- `release-record.html` loads and shows `82585128`
- `release-portal.html` loads
- Favicon appears in browser tab
- `robots.txt` returns 200
- `sitemap.xml` returns 200
- Bogus path (e.g. `/does-not-exist`) returns the branded 404 page

## Truth constraints

- Do not add download links unless a public download is actually available
- Do not claim open-source availability unless the app repo is public
- Release references (`82585128`, `neuraltube-proof-go-2026-04-15`) are factual — keep them
- Do not link to private repository pages that unauthenticated users cannot open
