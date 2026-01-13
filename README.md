# vzkn.eu

Personal website hosted on Cloudflare Pages.

## Stack

- **HTML** + **Tailwind CSS** (CDN)
- **Cloudflare Pages** (hosting)
- **JetBrains Mono** (font)

No build step required. Pure static HTML.

## Local Development

```bash
# Serve locally
npx serve src

# Open http://localhost:3000
```

## Deployment

### Cloudflare Pages Setup

1. Go to [Cloudflare Dashboard](https://dash.cloudflare.com) → Pages
2. Create project → Connect to Git
3. Select `vzkn-eu` repository
4. Configure:
   - **Build command**: (leave empty or `cp -r src/* dist/`)
   - **Build output directory**: `src` (or `dist` if using build command)
5. Deploy

### Custom Domain

1. In Cloudflare Pages → Custom domains
2. Add `vzkn.eu`
3. DNS is automatically configured (if domain is on Cloudflare)

## Structure

```
vzkn-eu/
├── src/
│   └── index.html    # Main page
├── public/           # Static assets (if needed)
├── package.json      # For local dev server
└── README.md
```

## Updating Content

Just edit `src/index.html` and push. Cloudflare Pages auto-deploys.

## License

MIT
