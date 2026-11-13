# Pinnacle Card — STAGED, link NO LONGER lands anywhere usable (re-checked 2026-11-12)

**CORRECTION 2026-11-12 ~12:00 UTC (curl, checked twice + HEAD): the existing CJ
tracked link https://www.tkqlhce.com/click-101911619-15780364 now redirects to
https://kingscamo.com/products/xkg-pinnacle-jacket (the OLD slug) and returns
HTTP 404 — Shopify NotFoundController, pageType 404. It does NOT land on the
homepage today, despite the 2026-11-11 11:57 ET browser check landing there.
Do NOT deploy the card with this link: buyers would hit a dead page.**
The live product page is https://kingscamo.com/products/kings-xkg-pinnacle-jacket
— HTTP 200, re-verified 2026-11-12 ~12:05 UTC and again ~15:05 UTC.
**PRICE CORRECTION 2026-11-12 ~15:05 UTC (main agent, product JSON): the
jacket is $139.99 flat — all 12 variants price 13999, compare_at 13999. The
"$100 sale" in the earlier 2026-11-12 note was WRONG: the "$100" on the page
is a collection tag ("Popular Items at $100+"), not the jacket price. Card
copy stays $139.99, commission ≈ $7/sale at 5% CJ.** Fix path (no Andrew
needed): build a FRESH CJ deep link in CJ Account Manager (CID 8107750,
Kings Camo programme 7016567) to the correct slug, curl-verify it returns
200 on the product page, then deploy. Andrew still silent (no reply since
the 2026-11-02 follow-up; no new email in the 2026-11-12 inbox) — a nudge
with the exact correct URL is drafted in the 2026-11-12 proactivity work if
Matt wants it sent. KY gun opener is Nov 14 — two days away — so this is
the last window to get the card live ahead of it.

Status: card fully built. The blocker changed 2026-11-11.
**UPDATE 2026-11-11 11:57 ET — re-checked the existing CJ tracked link
https://www.tkqlhce.com/click-101911619-15780364 in the browser: it NO LONGER
404s.** It redirects to the Kings Camo homepage
https://kingscamo.com/?cjdata=MXxOfDB8WXww&utm_medium=affiliate&utm_source=CommissionJunction&utm_campaign=101911619&utm_content=Shop+XKG+Pinnacle+Jacket+at+Kings+Camo&cjevent=ff37913fddf011f180dd00480a1eba24
— page loads, tracking params (cjdata / cjevent / utm_source=CommissionJunction)
preserved, so a purchase within the 14-day CJ cookie still credits. BUT it is
the homepage, not the product page: no Pinnacle name or price is shown on the
landing page. The live product page is still
/products/kings-xkg-pinnacle-jacket (verified 2026-11-03).
Decision now Matt's (pre-approved 2026-11-02: "we'll get it live ahead of the
Nov 14 opener"): deploy now with the existing link landing on the homepage, or
keep waiting on Andrew for a product-page link. Andrew has been silent 9 days
since the follow-up reached him 2026-11-02; no reply in any inbox check since.
Re-verify the $139.99 price on the live product page before deploying — the
specs/price below were last verified 2026-11-03.

## What's ready
- Image: site/img/xkg-pinnacle-jacket.png (720x900, 826KB — resized 2026-11-03,
  official Kings Camo product shot, matches other card image sizes)
- Product facts (verified 2026-11-03 from kingscamo.com/products/kings-xkg-pinnacle-jacket):
  $139.99 · 400GSM body / 320GSM sleeve body-mapping fleece · 18.7 oz ·
  Polygiene odor control · hood cut back for peripheral vision ·
  4.9/5 across 154 reviews · 5% CJ commission ≈ $7/sale

## Card HTML — insert after the HotHands card's closing </article>
(site/index.html line 546, inside <section id="hunt">, before the closing </div>)

      <article class="product">
        <figure class="showcase"><img src="img/xkg-pinnacle-jacket.png" alt="Kings Camo XKG Pinnacle Jacket in XK7 camouflage" loading="lazy"></figure>
        <h3>XKG Pinnacle Jacket</h3>
        <p class="spec-line">400GSM body-mapping fleece · 18.7 oz · Polygiene odor control</p>
        <p class="pick">The mid-layer reviewers keep coming back to. 400GSM body-mapped fleece — heavier through the core, lighter where you move — with a hood cut back so your peripheral vision stays open, Polygiene odor control for the long sit, and thumbholes that keep the cuffs put. 4.9 stars across 154 reviews.</p>
        <p class="verdict-line">Field verdict: the consensus mid-layer.</p>
        <a class="buy" href="FIXED_CJ_TRACKED_LINK" rel="sponsored nofollow noopener" target="_blank">Check price</a>
      </article>

**FRESH CJ DEEP LINK BUILT + VERIFIED 2026-11-12 ~10:13 ET (browser task +
main-agent curl check): https://www.tkqlhce.com/click-101911619-15784057?url=https%3A%2F%2Fkingscamo.com%2Fproducts%2Fkings-xkg-pinnacle-jacket — lands on
the live product page, HTTP 200, CJ tracking intact (cjdata/cjevent,
utm_source=CommissionJunction), $139.99. Built in CJ Account Manager (CID
8107750, programme 7016567) from the Evergreen Link (link ID 15784057) with
destination set to the correct slug; the old link (15780364) was NOT reused.
No programme settings changed. Use THIS link as FIXED_CJ_TRACKED_LINK.**

## Deploy steps (main agent)
1. Build the fresh CJ deep link (CID 8107750, Kings Camo programme 7016567)
   to https://kingscamo.com/products/kings-xkg-pinnacle-jacket; curl-verify it
   lands on the product page at HTTP 200 before use.
2. Insert the card in site/index.html after the HotHands </article> (Hunt
   section). Price $139.99 flat (≈$7/sale at 5% CJ).
3. Update counts: products 59 → 60 (after the PreCip deploy lands), Hunt
   "seventeen deer-season picks" → "eighteen".
4. Deploy via the normal Cloudflare Pages zip path (see site/DEPLOY.md) —
   AFTER the in-flight PreCip deploy has landed, so production keeps both
   cards.
5. Verify live on blackpinefield.com, then report the card live to Matt.
6. Also push the text layer to the GitHub source of truth per his standing preference.

Pre-approved by Matt: "we'll get it live ahead of the Nov 14 opener" (2026-11-02).
No refund language, no untracked link — CJ tracked only, per the profitable-shelves rule.
