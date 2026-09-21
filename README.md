# COLAVA

Bilingual Food and Candles studio website. Food Forms 01 is the first digital guide, priced at €19 for the English and Italian editions. Custom molds, materials and kits are coming soon.

## Deploy on Vercel

Import this repository in Vercel. Use the Other framework preset, repository root as the root directory, no build or install command, and `dist` as the output directory. `vercel.json` includes the static-site configuration.

## Configure checkout

Edit `dist/config.js` and add your Stripe Payment Link to `stripePaymentLinks.food`. Accepted HTTPS hosts are buy.stripe.com and checkout.stripe.com. Do not put secret API keys in this file: everything in dist is public.

When no payment link is configured, checkout opens an honest coming-soon notice and a free preview. Secure paid-PDF delivery must be configured separately before accepting payments. The complete paid guides are not included in this public repository.

## Edit the site

- `dist/app.js`: English/Italian text, Food/Candles views and interactions.
- `dist/style.css`: responsive layout, motion and mobile checkout styles.
- `dist/assets/`: photography, font and free preview PDFs.
- `dist/privacy.js`, `dist/legal.js`: cookie preferences, footer and bilingual information pages.
- `dist/index.html`: pre-rendered English Food page plus client-side rendering.

After editing the markup generator, refresh the initial static HTML in index.html to match. The site has no package dependencies or build step.

## Local preview

Run `python3 -m http.server 8000 --directory dist` and open http://localhost:8000.

## Launch checklist

Add the business support email and full address, complete the privacy and digital-purchase information, configure Stripe and secure delivery, then test payment and download end to end. Existing browser checks cover source syntax and asset paths; visual device testing remains recommended.

Generated product photography is labelled as AI concept imagery. Physical products and custom services are not yet available to order.
