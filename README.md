# nightjartools.github.io

The Nightjar Tools site. Plain static HTML — no build step, no dependencies, no framework.

```
index.html            landing page
channel-planner/      free Zigbee/Wi-Fi/Thread channel planner
power-calc/           free homelab running-cost calculator
assets/               logo, avatar, banner
```

## Deploying

This repo is named `nightjartools.github.io`, so GitHub serves it at
`https://nightjartools.github.io/` automatically once Pages is enabled:

**Settings → Pages → Source: Deploy from a branch → `main` / `root` → Save.**

First build takes a minute or two.

## Custom domain

Once `nightjartools.com` is registered, add a file called `CNAME` at the repo root
containing exactly:

```
nightjartools.com
```

Then point the domain's DNS at GitHub — four A records for the apex
(185.199.108.153, 185.199.109.153, 185.199.110.153, 185.199.111.153) and a CNAME for
`www` pointing at `nightjartools.github.io`. Tick "Enforce HTTPS" in Settings → Pages
after the certificate provisions.

## Editing

Everything is hand-written HTML with inline CSS. The palette is defined once in the
`:root` block of `index.html` and matches `_publish/BRAND.md` in AppFactory.

The two tools are copied verbatim from their product builds — if you rebuild either
product, re-copy the file rather than editing it here, so the site and the product
don't drift apart.
