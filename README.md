# SG Drives — sgdrives.com

Static website for Singapore car ownership tools. Hosted on Cloudflare Pages, deployed automatically from this repo.

## How to update the site
1. Edit any file here on GitHub (click the file, then the pencil icon), OR upload a new version via **Add file > Upload files**.
2. Click **Commit changes** (green button).
3. Cloudflare rebuilds automatically — live in ~30-60 seconds.

## IMPORTANT: after changing any page
Bump the cache version in `sw.js` so returning visitors get the fresh files:
change `sgdrives-vN` to the next number (v2 -> v3 -> v4 ...), then commit.

## Publishing a COE post (every bidding Wednesday)
1. Copy the folder `blog/coe-results-jun-2026-2nd/` to a new name, e.g. `blog/coe-results-jul-2026-1st/`.
2. Edit the new `index.html`: fill in the [BRACKETS] with the round's figures and notes, update the title, canonical, og:url and date.
3. Add the new URL to `sitemap.xml` and link it at the top of `blog/index.html`.
4. Commit. Done.

## Pages
- `/` homepage (live COE hero board)
- `/coe-prices-singapore/` COE results, chart, outlook
- `/rule-78-loan-settlement-calculator/`
- `/car-depreciation-calculator-singapore/`
- `/ev-vs-petrol-cost-calculator-singapore/`
- `/vrn-ncd-appeal-letter-generator-singapore/`
- `/vrn-checksum-calculator-singapore/`
- `/services/` valuation + car hunting
- `/blog/` guides & COE analysis

## Live data
COE figures come from LTA's public dataset on data.gov.sg (auto-updates).
Petrol/charging prices in the EV tool are baked — update the dates/values in
`ev-vs-petrol-cost-calculator-singapore/index.html` periodically.
