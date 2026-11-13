# Marmot Cards — STAGED, awaiting Matt's pick (one of two)

**UPDATE 2026-11-12 (subagent build run): Matt picked PreCip Eco Pro. Card INSERTED into site/index.html (Hunt dept, after HotHands, before TideWe ThermCore) — buy href still `CJ_TRACKED_LINK_PRECIP` placeholder. NOT deployed, zip NOT rebuilt, counts NOT updated (still "58 products" / "sixteen deer-season picks" in the file — see count note below).**
- **Prices re-verified TODAY 2026-11-12 ~14:43 UTC (fresh crawls <1 min old):** DealNews still lists **$64 vs $160, InStock** — free Marmot Rewards signup knocks the half-price down another 20%; Marmot's own product page shows **$79.99 sale / $160 list, InStock** (the $64 figure needs the Rewards signup — card copy "$64 with Rewards" is accurate). REI $119.73 / 4.7 stars / 131 reviews last confirmed by the main agent 2026-11-10 (REI crawl 15 days old; not re-verified today — secondary cross-check only, card price is the Marmot one). **Both live prices end Fri Nov 13, 2026 at 11:58pm CT — the CJ link + deploy must happen by then or the card price goes stale.**
- **Image verified on disk:** `site/img/marmot-precip-eco-pro.jpg` (540×720 JPEG, 26,953 bytes, official Marmot on-model Black shot).
- **Card HTML verified:** 59 product articles in index.html (was 58); HTML parses clean, no unclosed tags.
- **COUNT NOTE — needs a decision at deploy:** inserting PreCip makes Hunt 17 products, so "sixteen deer-season picks" (hunt band, deer-season guide, Nov 12 countdown reels) is now one short, and the store total becomes 59. At deploy, either update the band/guide to seventeen and the store counts to 59, or accept the mismatch — do NOT deploy with "sixteen" still printed next to 17 Hunt cards without deciding.
- **STILL BLOCKED (needs the main agent's browser):** (1) CJ tracked deep link — NOT built; a Nov 10 browser attempt found no saved CJ login in the guest browser. Build in CJ Account Manager (CID 8107750, programme 4961511), destination https://www.marmot.com/p/mens-precip-eco-pro-rain-jacket-fall-2025/SP_3185004/AFS_195115271213.html (verified live + InStock today). Swap the `CJ_TRACKED_LINK_PRECIP` placeholder for the real link, curl it, confirm HTTP 200 on the live Marmot page. (2) Rebuild the zip and deploy via Cloudflare Pages direct upload (saved Vault password; skip any 2FA setup interstitial without changing settings). (3) Verify live on blackpinefield.com, then report to Matt. **Do NOT deploy with the placeholder href.**

**UPDATE 2026-11-10 21:34 UTC: Matt picked PreCip Eco Pro (Option A). Deploy ONLY Option A — never the Montreal coat, never both. Price re-verified 2026-11-10 ~22:54 UTC: DealNews (crawled ~1h earlier) still lists $64 vs $160 with free Marmot Rewards signup, offer valid through 11/13/26 at 11:58pm CT; REI still $119.73 (25% off), 4.7 stars / 131 reviews. Re-checked again 2026-11-10 23:55 UTC: DealNews page crawled <1 min earlier still shows $64 vs $160, InStock; REI listing still shows $119.73, 4.7 stars / 131 reviews (page crawl dated Oct 27, price confirmed by main agent Nov 10). Specs cross-checked via GearJunkie (updated Nov 10, 2026): 3-layer NanoPro, 20K/20K waterproof-breathability, 13 oz — staged card's "3-layer NanoPro shell" is accurate; do NOT use the older 2.5-layer PreCip Eco specs. A CJ deep-link build was started in the browser 2026-11-10 ~23:58 UTC (task browser-task:3a681849-026a-54b6-bda2-69b7ecf274da) — link + image pending its result; do NOT deploy until the CJ link is verified landing on the live Marmot PreCip Eco Pro page.**

Status: both candidate cards fully written below except the buy link and the
product image. Deploy ONLY the one Matt picks — never both, never on a guess.
Sale prices on both end **Friday, November 13, 2026 at 11:58pm CT** (Marmot
Early Black Friday, verified 2026-11-10 via DealNews).

## What's verified (2026-11-10, this run)
- Marmot approved on CJ 2026-11-10 12:55 ET, programme 4961511, tiered
  commission (no % stated in the welcome email), 10-day cookie, deep linking
  allowed. Per-sale earnings are UNKNOWN until CJ shows the tier — do NOT
  quote a $/sale figure for either card.
- **PreCip Eco Pro rain jacket** — $160 list. $64 direct from Marmot with a
  free Marmot Rewards signup (50% off + extra 20%; DealNews 2026-10-24,
  re-verified 2026-11-10). $119.73 at REI (25% off) and 4.7 stars / 131 REI
  reviews — per the main-agent check 2026-11-10, not re-verified by me.
  Specs: 3-layer NanoPro waterproof/breathable shell, 100% seam-taped,
  underarm PitZips, attached adjustable hood, limited lifetime warranty.
  Men's version is the $64 deal; a women's version exists at the same $160
  list (Nordstrom).
- **Women's Montreal down coat** — $251 vs $335 list (25% off, Marmot Early
  Black Friday; DealNews, re-verified 2026-11-10). Specs: 700-fill down,
  7.1 oz fill, 2 lbs 2.2 oz, fleece-lined interior, fur-rimmed hood,
  knee-length parka (Switchback Travel review).
- **Stockholm 700-fill down jacket at $105 is DEAD** — October deal, gone.
  Do NOT stage it. (Corrected to Matt 2026-11-10 19:02 UTC.)

## Lean (judgment, not a fact)
PreCip is the stronger first Marmot card: a $64 headline price on a $160
jacket, men's/unisex rain gear that fits the Hunt shelf and the hiking crowd,
and a 4.7-star track record. Montreal is the bigger ticket ($251) so it
would earn more per sale IF the CJ tier is percentage-based — but that is
not confirmed, and it is women's-only, a narrower buyer on this shelf.
Matt decides; the lean is PreCip.

## Still missing for either card
1. CJ tracked deep link — build in CJ Account Manager (CID 8107750,
   programme 4961511); may need Matt's signed-in CJ session if the login
   has lapsed. Curl it and confirm it lands on the live Marmot product
   page (HTTP 200) before deploying — do NOT deploy a link to a dead page.
   **UPDATE 2026-11-10 ~23:59 UTC: background guest browser has NO saved CJ login (members.cj.com redirects to signin.cj.com) — link NOT built. The main-agent browser previously built the Kings Camo CJ link, so try there first; if that session has lapsed, the link needs Matt's CJ sign-in. Destination URL (verified live 2026-11-10 18:58 ET): https://www.marmot.com/p/mens-precip-eco-pro-rain-jacket-fall-2025/SP_3185004/AFS_195115271213.html — "Men's PreCip® Eco Pro Rain Jacket (Fall 2025)", 3L NanoPro, 4.8 stars / 116 reviews on Marmot's own page. PRICE NOTE: Marmot's own page shows $79.99 sale / $160 list; the $64 figure is the extra 20% off with a free Marmot Rewards signup per DealNews (still listed $64 on DealNews, crawled 23:55 UTC) — card copy "$64 with Rewards" is accurate only with the signup, $79.99 is the on-page sale price. REI $119.73 / 4.7 stars / 131 reviews stands.**
2. Product image — **DONE 2026-11-10 ~23:59 UTC**: official Marmot on-model front-view shot (Black), saved as `site/img/marmot-precip-eco-pro.jpg` (540×720 JPEG, 27 KB, converted from Marmot's Scene7 original https://s7d1.scene7.com/is/image/NewellBrands/m15884-001_onmodel_01_f25?$NB_Image_Gallery$&wid=1200 — 1200×1600). Fits the .showcase frame (object-fit contain). No further image work needed.

## Card HTML — insert after the HotHands card's closing </article>
(site/index.html, inside <section id="hunt">, before the closing </div>)

### Option A — PreCip Eco Pro

      <article class="product">
        <figure class="showcase"><img src="img/marmot-precip-eco-pro.jpg" alt="Marmot PreCip Eco Pro rain jacket" loading="lazy"></figure>
        <h3>Marmot PreCip Eco Pro Rain Jacket</h3>
        <p class="spec-line">3-layer NanoPro shell · 100% seam-taped · PitZips · $64 with Rewards</p>
        <p class="pick">The rain shell that made the PreCip a legend, rebuilt lighter. Three-layer NanoPro fabric, every seam taped, underarm zips to dump heat on the climb — and right now it's $64 direct from Marmot with a free Rewards signup, down from $160. 4.7 stars across 131 REI reviews.</p>
        <p class="verdict-line">Field verdict: the $64 shell that outruns jackets triple its price.</p>
        <a class="buy" href="CJ_TRACKED_LINK_PRECIP" rel="sponsored nofollow noopener" target="_blank">Check price</a>
      </article>

### Option B — Women's Montreal Down Coat

      <article class="product">
        <figure class="showcase"><img src="img/marmot-montreal-down-coat.jpg" alt="Marmot Women's Montreal down coat" loading="lazy"></figure>
        <h3>Marmot Women's Montreal Down Coat</h3>
        <p class="spec-line">700-fill down · 7.1 oz fill · 2 lbs 2.2 oz · knee-length parka</p>
        <p class="pick">The winter coat that shows up everywhere for a reason. 700-fill down, fleece-lined, fur-rimmed hood, knee-length cut that actually covers you — $251 in Marmot's Early Black Friday sale, down from $335. Sale ends Friday, November 13 at 11:58pm CT.</p>
        <p class="verdict-line">Field verdict: the cold-weather coat that earns its keep.</p>
        <a class="buy" href="CJ_TRACKED_LINK_MONTREAL" rel="sponsored nofollow noopener" target="_blank">Check price</a>
      </article>

## Deploy steps (main agent, on Matt's pick)
1. Build the CJ tracked deep link for the picked product only; curl it,
   confirm HTTP 200 on the live Marmot page.
2. Pull the official product image, save under site/img/ with the filename
   in the card above, and check it renders.
3. Insert ONLY the picked card in site/index.html after the HotHands card.
4. Deploy via the normal Cloudflare Pages zip path (see site/DEPLOY.md);
   update the "58 products" count to 59 in the hero, sign-open line, and
   meta description.
5. Verify live on blackpinefield.com, then report the card live to Matt.
6. Also push the text layer to the GitHub source of truth per his standing
   preference.

No refund language, no untracked link — CJ tracked only, per the
profitable-shelves rule. Do NOT retarget another brand's button to Marmot.
