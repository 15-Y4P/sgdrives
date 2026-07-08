# SG Drives — Deploy Guide (Cloudflare Pages)

## One-time setup (~30 min)

### 1. Deploy the site
1. Go to https://dash.cloudflare.com and create a free account.
2. Workers & Pages → Create → Pages → "Upload assets".
3. Name the project `sgdrives`.
4. Drag the entire contents of this `site/` folder in (all files and folders, not the folder itself).
5. Deploy. You get a preview URL: https://sgdrives.pages.dev

### 2. Test on the preview URL
- All 4 calculators (run a real number through each)
- Letter generator: generate, copy, print
- Mobile layout (open on your phone)
- WhatsApp buttons open your chat (6580336863)

### 3. Point the domain (Wix-registered domain)
1. In Cloudflare: Add a site → sgdrives.com → Free plan. Cloudflare shows you 2 nameservers.
2. In Wix: Settings → Domains → sgdrives.com → Advanced/DNS → change nameservers to the 2 Cloudflare ones.
3. Wait for activation email from Cloudflare (minutes to a few hours).
4. In the Pages project → Custom domains → add sgdrives.com and www.sgdrives.com.
5. Done — SSL is automatic.

Optional later: transfer the domain registration itself from Wix to Cloudflare Registrar
(cheaper renewal, ~US$10/yr). Not urgent; nameserver change alone makes the site live.
NOTE: if you use Wix for email on this domain, copy the MX records into Cloudflare DNS
BEFORE changing nameservers.

### 4. After go-live
- Google Search Console: re-verify property, submit https://www.sgdrives.com/sitemap.xml
- Downgrade Wix to free plan at next renewal (keep the account as backup).

## Updating the site later
Edit any file → Cloudflare dashboard → your Pages project → "Create new deployment"
→ drag the folder in again. Live in ~30 seconds. Or bring the file back to Claude to edit.


## Analytics (recommended, free, no cookie banner needed)
1. Cloudflare dashboard -> Web Analytics -> Add a site -> sgdrives.com
2. Copy the JS snippet Cloudflare gives you.
3. Paste it just before </body> in every page (or ask Claude to add it in one pass).

## Updating baked price data
- COE fallback: coe-prices-singapore/index.html -> FALLBACK array (only needed if the live feed breaks; homepage bar + COE page auto-update from data.gov.sg).
- Petrol & charging info bars: ev-vs-petrol-cost-calculator-singapore/index.html -> the two .ibar blocks near the top. Update the prices and the "Updated" dates. Sources: petrolprice.sg / Fuel Kaki (petrol), revolt.sg price index (charging).
- Charger network stats: same page, .chargers-note block.

## PWA
The site is installable (Add to Home Screen). After deploying changes, bump the cache
version in sw.js (sgdrives-v1 -> v2) so returning visitors get the fresh files immediately.
