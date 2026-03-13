# lauki-site

Landing page for **Lauki Antonson** — the first AI agent running full operations for paying clients.

**Live:** [lauki.ai](https://lauki.ai)

## What

Headcount: Zero — one AI agent, fifteen clients, full operations. Marketing, outreach, deployments, monitoring, community, email, code. $500/month flat. All on-chain.

## Stack

- Static HTML/CSS — no framework, no build step
- Hosted on Cloudflare Pages (`lauki-site` project)
- Custom domain: `lauki.ai`
- Fonts: Figtree + Space Mono (Google Fonts)

## Files

```
index.html            — main landing page
playbook/index.html   — Lauki's Playbook page
hero.jpg              — hero composition (orb + LAUKI text)
avatar.jpg            — profile image
og.png                — Open Graph preview image
favicon.png           — favicon
apple-touch-icon.png  — iOS icon
```

## Deployment (CI/CD)

Deployments are automated via GitHub Actions. Push to a branch and it deploys automatically.

| Branch | Deploys to | URL |
|--------|-----------|-----|
| `master` | Production | [lauki.ai](https://lauki.ai) |
| `stage` | Preview | `stage.lauki-site.pages.dev` |

**Workflow:** `.github/workflows/deploy.yml`

### How it works

1. Push to `master` → auto-deploys to **lauki.ai** (production)
2. Push to `stage` → auto-deploys to **stage preview URL** (for review)
3. All changes go on `stage` first → review → merge to `master` → auto-deploys to production

### Manual deploy (if needed)

```bash
wrangler pages deploy . --project-name=lauki-site --branch=master
```

### Secrets (GitHub repo)

- `CLOUDFLARE_API_TOKEN` — Cloudflare API token
- `CLOUDFLARE_ACCOUNT_ID` — Cloudflare account ID

## Rules

- **NEVER push directly to `master`** without review
- All changes go on `stage` branch first
- Review on the preview URL, then merge to `master`

## Legacy

The old version at [antonson.io](https://antonson.io) runs separately on the `headcount-zero` Cloudflare Pages project with gold/amber styling. This repo (`lauki-site`) is the active, maintained version with the green accent and hero orb.
