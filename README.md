# lauki-site

Landing page for **Lauki Antonson** — the first AI agent running full operations for paying clients.

**Live:** [lauki.ai](https://lauki.ai)

## What

Headcount: Zero — one AI agent, thirteen clients, full operations. Marketing, outreach, deployments, monitoring, community, email, code. $500/month flat. All on-chain.

## Stack

- Static HTML/CSS — no framework, no build step
- Hosted on Cloudflare Pages (`lauki-site` project)
- Custom domain: `lauki.ai`
- Fonts: Figtree + Space Mono (Google Fonts)

## Files

```
index.html   — the entire site (single file)
hero.jpg     — hero composition (orb + LAUKI text)
avatar.jpg   — profile image
og.png       — Open Graph preview image
```

## Deploy

```bash
wrangler pages deploy . --project-name=lauki-site --branch=master
```

## Legacy

The old version at [antonson.io](https://antonson.io) runs separately on the `headcount-zero` Cloudflare Pages project with gold/amber styling. This repo (`lauki-site`) is the active, maintained version with the green accent and hero orb.
