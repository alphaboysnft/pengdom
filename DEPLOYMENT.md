# Deploy PENGDOM to Cloudflare

The website and all media are in `dist/`. No build is required.

## Cloudflare Pages (Git integration)
1. Create a Pages project and connect alphaboysnft/pengdom.
2. Production branch: main.
3. Framework preset: None.
4. Build command: exit 0.
5. Build output directory: dist.
6. Deploy and verify the generated pages.dev address before adding a custom domain.

Pushes to main deploy automatically after the Git connection is enabled.

## Cloudflare Workers (alternative)
This repository also includes wrangler.jsonc for a static-assets Worker.
Connect this repository using Workers Builds, use no build command (or exit 0), and set the deploy command to:
`npx wrangler deploy`

The configured Worker name is pengdom. If connecting to an existing differently named Worker, update the name in wrangler.jsonc first.

## Application settings
The official X handle and launch post are currently unset in dist/index.html (campaign).
X actions stay disabled until these are configured.
Profiles and task confirmations are stored on each visitor's device.
NFT previews are concepts; there is no live mint or wallet integration.
Video audio is muted; penguin ambience has its own mute/volume controls.

## Local preview
Run `python3 -m http.server 8080 --directory dist` and visit http://localhost:8080.
