# Bokrah website | موقع بُكرة

Arabic and English landing page for Bokrah restaurant accounting, with a direct Windows installer download and an illustrative dashboard demo.

صفحة تعريفية عربية وإنجليزية لنظام بُكرة لمحاسبة المطاعم، مع تحميل مباشر لتطبيق ويندوز ونموذج توضيحي للواجهة.

## Local preview

Requires Node.js. No dependency installation or build step is needed.

```sh
npm run dev
```

Open http://127.0.0.1:4173. Run `npm run check` to check JavaScript syntax and the dashboard calculations.

## Deployment

The `.github/workflows/deploy-pages.yml` workflow checks the source, uploads `dist/`, and publishes it to GitHub Pages after each push to `main`. It can also be run manually from Actions. Repository Settings → Pages must use **GitHub Actions** as its publishing source.

Website: https://mahfoud-sa.github.io/bokrah-website/

## Editing

- `dist/index.html`: landing page and Arabic copy.
- `dist/landing.js`: English translations and language switch. Arabic is the default; the selected language is saved in the browser.
- `dist/landing.css`: responsive layout and Arabic/English styling.
- `dist/app.html`, `dist/app.js`, `dist/style.css`: illustrative dashboard, with sample records stored in the browser.

The installer is hosted in the separate [Bokrah application releases](https://github.com/Mahfoud-Sa/bokrah/releases). To point to a new release, update both `.download-link` URLs and the `release-info` text in `dist/index.html`.

The dashboard is a browser-local demonstration. It does not sync financial records to GitHub or a server.
