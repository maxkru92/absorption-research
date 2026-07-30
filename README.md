# KC Krupp Capital — Absorption Analytics

Vercel-deployed scaffold for **absorption-research.vercel.app**, branded with the KC **purple** favicon variant from the [Krupp Capital favicon pack](/Users/maximiliankrupp/Desktop/kc-favicon-pack).

| constant        | value   |
|-----------------|---------|
| Pine Script     | `C_PURPLE` |
| c1 (canonical)  | `#9D4EDD` |
| c2 (deeper)     | `#7B3DBA` |
| persona         | Absorption Analytics |

## Local dev

```bash
npx serve public -l 3000   # http://localhost:3000
```

## Rebuild favicons

```bash
npm run kc:deploy   # runs deploy.py --sites=absorption-research (idempotent)
```

## What lands in `public/`

| file                         | purpose                              |
|------------------------------|--------------------------------------|
| `favicon.ico`                | legacy windows shortcut              |
| `favicon.svg`, `icon.svg`    | modern gradient                      |
| `favicon-16.png`             | browser tab @1x                      |
| `favicon-32.png`             | browser tab @2x                      |
| `apple-touch-icon.png`       | 180×180 iOS home screen              |
| `icon-192.png`, `icon-512.png` | PWA icons                          |
| `og-image.png`               | 1200×630 social share                |
| `site.webmanifest`           | PWA manifest, theme_color = {P['c2']} |

## Deploy to Vercel

```bash
vercel link --yes
vercel deploy --prod
```

Vercel auto-detects static-site mode and serves `public/` from the URL root.
