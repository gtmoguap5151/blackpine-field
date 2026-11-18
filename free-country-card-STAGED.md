# Free Country Card — STAGED, CJ tracked link not yet built

**Free Country APPROVED on CJ 2026-11-17, 18:20 ET** (welcome email from
noreply@cj.com, Gmail 1a1ebcf7124dd3f4): 3% baseline commission, 30-day
cookie. CJ's listing had shown 10% and the live CJ dashboard on Nov 17
showed "Sale 10%" — the welcome email's 3% governs per the task brief;
rate discrepancy still unresolved, check program terms before quoting a
rate anywhere else. Promo code WINTER50 (up to 50% off pet jackets),
frequent promotions up to 60% off.

**Pick: Men's Lanier Super Softshell® Jacket** — Matt delegated the pick
("call as you see fit", 2026-11-18 voice call); Xena picked the Lanier as
the highest-ticket Free Country option. (Matt's "Langer Super Soft" on
the call was the Lanier Super Softshell.)

## Terms (per the welcome email, 2026-11-17)
- **3% baseline commission** on orders (welcome email governs)
- **30-day cookie**
- CJ advertiser/programme ID: **5683766** (per FMTC's public CJ merchant
  directory, corroborated in two FMTC listings — NOT yet confirmed inside
  the CJ dashboard; confirm when pulling the link)
- Publisher PID for Blackpine links: **101911619** (same as Marmot/Kings)

## Why it fits
- On-brand Hunt-shelf apparel — a wind/water-resistant softshell for cold
  mornings in the stand. Sits naturally beside the Marmot PreCip shell.
- At 3%, the per-sale is small ($126 × 3% ≈ **$3.78/sale**) — volume +
  the promo hook is the play, not big-ticket dollars.

## Pick: Lanier Super Softshell (verified live 2026-11-18 ~17:22 ET, freecountry.com)
- **Price: $126.00, InStock** (Shopify product JSON, live just now;
  compare-at price also $126 — full price direct right now)
- 3-layer bonded fabric: poly-spandex high-denier yarns + water-resistant
  membrane + plush fleece interior lining
- Four-way stretch · Wind resistant · Water resistant · Convertible
  collar · Full zip · Chest zip pocket · Lower zip pockets · Attached
  storm cuffs · Interior adjustable drawcord at lower hem
- FreeCycle® recycled fabric; Best Seller tag on freecountry.com
- 8 colors (Evergreen, Mushroom, Olive, Storm, Black, Dark Navy, Saddle,
  Coal), sizes S–XXL
- Live page: https://freecountry.com/products/mens-lanier-super-softshell-jacket
- Context only (NOT the card destination): Macy's had it at $69.30
  (crawl 3 days old), Kohl's sale $88.20. The CJ programme pays on
  freecountry.com sales, so the card links there at $126.

## Image — official Free Country product shot (verified, NOT AI)
- **Card uses the live brand CDN URL** (hotlinked — see note below):
  https://cdn.shopify.com/s/files/1/2097/1975/files/543MOF5138_EVERGREEN_106_FC.jpg?v=1757946876&width=800
  (800px, 44,958 bytes, HTTP 200 image/jpeg, verified 2026-11-18 ~17:22 ET;
  model wearing the jacket in Evergreen, front view, white background —
  visually checked, clean product shot.)
- **Local 800×800 copy staged** at
  `~/workspace/blackpine-field/site/img/free-country-lanier-softshell.jpg`
  (53,054 bytes, resized from the 3000×2999 brand original) for a later
  GitHub web upload to `site/img/` — binary images cannot go through the
  GitHub connector or direct git push.
- NOTE: hotlinking is a deviation — every other card image in index.html
  is a local `img/` file. Prefer swapping the `src` to
  `img/free-country-lanier-softshell.jpg` once the web upload lands.

## Card HTML — insert in the Hunt shelf, after the Marmot PreCip card
(site/index.html, inside <section id="hunt">, between the Marmot PreCip
article and the Kings XKG Pinnacle article. Bump the product count 61 →
62 in THREE places: meta description line 9, hero caption line 50,
dept strip line 64. The hero-note "Sixty products" line 38 is already
stale — leave it, do not touch.)

      <article class="product">
        <figure class="showcase"><img src="https://cdn.shopify.com/s/files/1/2097/1975/files/543MOF5138_EVERGREEN_106_FC.jpg?v=1757946876&amp;width=800" alt="Free Country Men's Lanier Super Softshell Jacket in Evergreen" loading="lazy"></figure>
        <h3>Free Country Men's Lanier Super Softshell Jacket</h3>
        <p class="spec-line">3-layer bonded shell · 4-way stretch · Wind + water resistant · $126</p>
        <p class="pick">The softshell that does the quiet work on a cold morning. Three-layer bonded fabric — high-denier poly-spandex outside, a water-resistant membrane in the middle, plush fleece against you — with four-way stretch, a convertible collar, a chest zip pocket, storm cuffs, and a drawcord hem. Wind and water resistant, built on FreeCycle recycled fabric, and a Best Seller in eight colors, S to XXL. $126 direct from Free Country.</p>
        <p class="verdict-line">Field verdict: the everyday softshell that covers the walk in, the glass, and the drive home.</p>
        <a class="buy" href="CJ_TRACKED_LINK_FREECUNTRY_LANIER" rel="sponsored nofollow noopener" target="_blank">Check price</a>
      </article>

## BLOCKER — the CJ tracked link (one missing piece)
- **Missing: the CJ link ID (AID) for a Free Country text link** — the
  second number in `https://www.<cj-domain>/click-101911619-<AID>?url=<encoded
  product URL>`. It is NOT the programme ID: Marmot's programme is
  4961511 but its link AID is 13876409; Kings' programme is 7016567 but
  its link AID is 15784057. The AID comes only from the CJ dashboard.
- Searched 2026-11-18: workspace files (welcome email has no ID or
  usable link — its "Get Html" URLs are opaque CJ email redirects),
  FMTC directory (programme ID 5683766 only), public web (no Free
  Country CJ click link surfaced). **Do NOT guess an AID.**
- **How to get it:** CJ Account Manager (needs Matt's signed-in session
  if the login has lapsed) → Links → Search "Free Country" → Get Link
  on any text link, or the Deep Link Generator on the product URL.
  Expected shape (by analogy with Marmot/Kings):
  `https://www.<cj-domain>/click-101911619-<AID>?url=https%3A%2F%2Ffreecountry.com%2Fproducts%2Fmens-lanier-super-softshell-jacket`
  (the CJ click domain varies per advertiser — use the one CJ returns).
- Curl-verify the finished link lands on the live product page
  (HTTP 200) before deploying — do NOT deploy a link to a dead page.
- **Do NOT publish this card with an untracked buy button.** The
  profitable-shelves rule (2026-11-02): every NEW card tracked from day
  one. The card stays staged until the CJ link exists.

## Deploy steps (main agent, once the link exists)
1. Get the CJ tracked link (above); curl-verify HTTP 200 to the live
   Lanier page.
2. Replace CJ_TRACKED_LINK_FREECUNTRY_LANIER in the card HTML above.
3. Insert the card after Marmot PreCip in site/index.html; bump 61 → 62
   in meta description, hero caption, dept strip.
4. Push text via the GitHub connector / git push to main (Pages
   auto-deploys). Optionally web-upload the staged 800×800 image to
   site/img/ and switch the img src to local.
5. Verify live on blackpinefield.com by curl (card + tracked link +
   image serve), then report the card live to Matt.
6. Update STATUS.md (Free Country bullet + a 2026-11-18 entry).

No refund language, no untracked link, no invented price/spec/image —
every number above was verified live 2026-11-18.
