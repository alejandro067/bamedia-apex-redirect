# bamediastudio.com — apex redirect

Serves the apex `bamediastudio.com` via GitHub Pages (free Let's Encrypt SSL) and
issues a path-preserving 301 to `https://www.bamediastudio.com`.

Why GitHub Pages: the domain is registered + DNS-hosted at Wix (NS locked to
wixdns.net), so the apex can't be a Cloudflare Pages custom domain. www is on
Cloudflare Pages; apex points here.

**Manual step (PAT lacks `pages` scope):** Settings → Pages → Deploy from a
branch → `main` / `/ (root)` → Save. Custom domain auto-fills from CNAME.
Enforce HTTPS once the cert provisions.
