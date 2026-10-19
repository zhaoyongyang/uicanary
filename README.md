# UICanary landing page

Static presale site for [UICanary](https://uicanary.xingqingnet.com), a visual regression testing product for developers (CI screenshot comparison). The product is not launched: there is no GitHub Action, no backend, and no live free tier. This repository is the marketing site for a paid validation — a $1 refundable presale and a waitlist.

## What’s in the repo

- `index.html` — landing page
- `privacy.html`, `terms.html` — presale policies
- `diff-mock.html`, `diff-mock.png` — concept mock of the planned diff UI

Plain static HTML. There is no build step, no package manager, and no framework.

## Deployment

Hosted on Cloudflare Pages, connected to this GitHub repository.

- Production branch: `main`
- Build command: none
- Output directory: repository root

A push to `main` publishes the files as they are.

## Visit analytics

Daily landing-page visits should come from Cloudflare Web Analytics. Do not commit a third-party tracker or a script with a made-up token.

Turn it on from the dashboard, with no code in this repo. Docs: [Enable Web Analytics on Pages](https://developers.cloudflare.com/pages/how-to/web-analytics/).

1. In the Cloudflare dashboard, go to **Workers & Pages**.
2. Open the Pages project for this site.
3. Go to **Metrics** and select **Enable** under **Web Analytics**.

Cloudflare adds its beacon on the next deployment. These pages are already valid HTML, which that injection needs. Read the counts under **Web Analytics**, on the site tied to the project. Page views there are the daily visit count.

Each HTML file has a commented-out beacon in front of `</body>`. Leave it commented out. Use it only if dashboard setup is switched to a manual JS snippet: paste the real token from the dashboard over `YOUR_CLOUDFLARE_WEB_ANALYTICS_TOKEN`, then uncomment that script. The placeholder collects nothing.

Presale and waitlist controls have distinct ids so clicks can be told apart later: `presale-cta-nav`, `presale-cta-hero`, `presale-cta-pricing`, `presale-cta-final`, `waitlist-cta-hero`, `waitlist-cta-free`, `waitlist-cta-pro`, and `waitlist-cta-tally`. Web Analytics’ default page-view report does not break those out by itself.
