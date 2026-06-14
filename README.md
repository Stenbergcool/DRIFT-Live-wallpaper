# Drift — website

Static landing page and documentation for Drift, the live video wallpaper for Windows 11.

## Files

- `index.html` — landing page
- `docs.html` — documentation

Both are fully self-contained (Tailwind, fonts and icons load from CDNs), so there's no build step.

## Hosting

Upload the `web-page` folder to any static host — GitHub Pages, Netlify, Cloudflare Pages, Vercel, or plain S3/nginx. `index.html` is the entry point. To preview locally, just open `index.html` in a browser, or run a tiny server:

```powershell
# from inside web-page/
python -m http.server 8080
# then visit http://localhost:8080
```

## Before you go live — wire up the download link

The site currently has no real installer URL. Search both HTML files for `TODO` and the `#download` / `#` placeholder hrefs on the **Download for Windows** buttons, and point them at your actual installer (for example a GitHub Releases `.exe` URL). There are three on the landing page (nav, hero, CTA) and the nav/Download button on the docs page links back to `index.html#download`.

## Notes on accuracy

This site describes only what Drift actually does today: live video wallpapers, the three multi-monitor modes (Every screen / Span / Custom), the clip timeline, library, presets, audio/power settings and the tray. The version shown is `v0.1.0`. There is intentionally no mention of macOS, a CLI installer, cloud sync, audio-reactive shaders, widgets or keyboard shortcuts, since the app doesn't have those — update the copy if that changes.
