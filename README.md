# Tritonet Web Embed

Use Tritonet Brainwave on any website.

## What this repo contains

- `dist/Tritonet_Web.html` — self-contained Tritonet app
- `examples/index.html` — example host page with regular content + Tritonet embed

## Quick usage (recommended: iframe)

```html
<iframe
  src="./dist/Tritonet_Web.html"
  title="Tritonet Brainwave"
  width="1100"
  height="734"
  style="border:0; max-width:100%;"
  allow="midi; autoplay"
></iframe>
```

## Why iframe is recommended

- Isolates styles and scripts from your main site
- Keeps Tritonet keyboard behavior predictable
- Easiest integration into CMS or static sites

## Browser notes

- For Web MIDI, use **HTTPS** (or localhost during development)
- Browser may require a click inside Tritonet before keyboard input is active

## Local preview

From this repo folder:

```bash
python3 -m http.server 8080
```

Open:

- `http://localhost:8080/examples/index.html`

## Keep dist updated

Copy the latest generated file from your source workspace:

```bash
cp ../Tritonet_Brainwave_SingleFile.html ./dist/Tritonet_Web.html
```

## Publish with GitHub Pages

1. Push this folder as its own repository
2. In GitHub repo settings, enable **Pages** from the `main` branch root
3. Your demo page will be available at:
   - `https://<your-user>.github.io/<repo-name>/examples/index.html`
