# Haze Watch

Single-page app showing Singapore haze (PSI, PM2.5, PM10 by area) and weather for Singapore and ASEAN cities.

- **Haze data:** National Environment Agency (NEA) via data.gov.sg real-time PSI API — Singapore only.
- **Weather:** Open-Meteo, for every city.
- Plain static site: no build step, no dependencies, no API keys.

## Files
- `index.html` — the whole app (HTML, CSS, JS)
- `favicon.svg` — site icon
- `vercel.json` — clean URLs and basic security headers

## Deploy to Vercel
1. Push this folder to a GitHub repository.
2. In Vercel: **Add New → Project**, import the repo.
3. Framework Preset: **Other**. Leave Build Command and Output Directory empty (root directory is served as-is).
4. Click **Deploy**.

## Run locally
Open `index.html` in a browser, or run `npx serve .`.

## Notes
- Data is fetched in the visitor's browser. If NEA or Open-Meteo can't be reached, the page shows an error with a retry button instead of placeholder numbers.
- The NEA API is rate-limited per IP; for heavy traffic, add a data.gov.sg API key via a small serverless proxy.
- Area map boundaries are approximate.
