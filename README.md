# Jewelry Travel Organizer — Pricing & Cost Laboratory
Mission 3. Static application; no backend, account, paid API, or API key. Original venture website is not modified.

## Run
Serve this folder with any static HTTP server. Node 18+ can run `npm test` and `npm run build`. `dist/` is an optional production copy; GitHub Pages can publish the root directly. All assets and data are local and use relative URLs.

## Model and evidence
USD monthly operating model. One unit/bundle per order, domestic standard Shopify Payments cards, seller-funded shipping, constant unit costs. 23 startup and operating expense suggestions. Shopify pricing checked October 28, 2026 (official Basic monthly $39, standard cards 2.9% + $0.30). USPS official retail starting postage $8.40 is a contextual floor: actual postage is an estimate until weight/zone are known. Manufacturing, packaging, labor, insurance, returns and other inputs are explicitly Estimated or Illustrative, not supplier quotes or industry averages. Competitor data is the unchanged Mission 1 snapshot from October 27, 2026 (4 direct competitors / 8 offers).

Startup cash is separate. Selected depreciation enters monthly fixed expense. Opening inventory funding does not duplicate per-sale cost. Shared overhead allocated by units or revenue, counted once for business profit. Multi-product break-even holds quantity mix constant. Break-even units round up; break-even revenue and margin of safety use unrounded threshold. Zero sales gives undefined mix. Nonpositive contribution gives no finite positive break-even.

## Decision workflow
Edit assumptions → Evaluate → write justification and acknowledge findings → Confirm → download genuine DOCX and JSON. Model edits invalidate evaluation and confirmation. Both exports are generated from one snapshot. Confirmation does not persist on refresh: re-evaluate and reconfirm. Working inputs and scenarios persist locally; back up using JSON export/import. Customer-facing JSON fields contain public product information only; other fields include private working financial assumptions. Do not publish an exported decision JSON without reviewing its contents.

## Tests
`node test.mjs` independently checks rounding, annualization, startup depreciation, disabled costs, multiple-product allocations, zero/negative contribution, zero sales, scenarios, import validation, risk classifications, and report structure. `node test.mjs --fixture` generates a clearly labeled QA-only report outside this project. Browser QA covers sliders, edits, products, scenarios, risk and stale-review handling, required statement/acknowledgment, and actual DOCX/JSON downloads. DOCX ZIP/XML and agreement with its JSON were checked; all report pages were rendered and inspected.

## Boundaries
Illustrative scenarios are not sales forecasts, tax advice or financial predictions. All-product variable expenses apply to each product; reassign expenses when adding unlike products. Inventory funding must be adjusted manually when changing planned purchase quantity. Cost/volume stress tests hold the other assumptions constant; no elasticity or capacity model. Refresh prices and obtain supplier, shipping and insurance quotes before launch.

Sources: https://www.shopify.com/pricing ; https://www.usps.com/ship/ground-advantage.htm ; individual competitor official URLs inside competitor_data.json.
