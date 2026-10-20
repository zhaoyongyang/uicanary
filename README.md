# UICanary

UICanary has been discontinued and will not launch. This repository is the static shutdown notice for [uicanary.xingqingnet.com](https://uicanary.xingqingnet.com). The service never shipped, and no presale payments were collected.

## What’s in the repo

- `index.html` — the shutdown notice
- `privacy.html`, `terms.html` — short notes that the service never launched, that no payments were taken, and how to ask for waitlist data to be deleted
- `diff-mock.html`, `diff-mock.png` — an archived concept drawing, not a product

Plain static HTML. There is no build step, no package manager, and no framework.

## Deployment

Hosted on Cloudflare Pages, connected to this GitHub repository.

- Production branch: `main`
- Build command: none
- Output directory: repository root

A push to `main` publishes the files as they are.

## Visit analytics

Cloudflare Pages can count visits from the dashboard, with no code in this repo. Docs: [Enable Web Analytics on Pages](https://developers.cloudflare.com/pages/how-to/web-analytics/).

1. In the Cloudflare dashboard, go to **Workers & Pages**.
2. Open the Pages project for this site.
3. Go to **Metrics** and select **Enable** under **Web Analytics**.

Each HTML file still has a commented-out beacon in front of `</body>`. Leave it commented out. Use it only if you switch the dashboard to a manual snippet and paste the real token over `YOUR_CLOUDFLARE_WEB_ANALYTICS_TOKEN`.
