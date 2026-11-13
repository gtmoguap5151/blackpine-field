# WILDGUARDER Card — STAGED, join not yet done

**Invite arrived 2026-11-12 12:19 UTC (07:19 ET) via Awin** — WILDGUARDER invited
BLACKPINE FIELD (Publisher 3131873) to join their programme. Merchant/profile
126831 on Awin. This is an INVITATION, not an approval yet — the join click
still has to happen in Awin, and the 15% / 30-day terms below are the
inviter's stated terms, to be re-verified in Awin's Commission Manager
after joining (MeoWant's email terms differed from its Awin profile in
2026-11-06, so do not treat the email as the final rate).

## Terms (per the invite email, 2026-11-12)
- **15% standard commission** on qualifying Awin sales
- **30-day attribution window**
- No cost to join, reversible (same pattern as TideWe / Piscifun / MeoWant)

## Why it fits
- On-brand Hunt optics — night vision, trail cameras, rangefinder binoculars.
  The store has NO night-vision product yet (checked site/index.html
  2026-11-12: Hunt has a Stealth Cam trail cam and a Vortex rangefinder,
  both Amazon-linked; nothing night-vision). WG9700 fills a gap, it does
  not duplicate a card.
- At 15%, WG9700 would be the **second-biggest per-sale card on the store**
  after MeoWant SC09 (~$78–$97.50): **~$51/sale**.

## Pick: WG9700 (verified 2026-11-12 ~12:56 UTC, store.wildguarder.com)
- **Price: $339.99, InStock** (JSON-LD Product.offers on the live product page)
- 4K video / 30fps, 36MP photos, 8X digital zoom
- Night vision up to 1000m, 940nm invisible IR (no visible red glow),
  1/1.8" super-starlight sensor, 0.0001 lux, full-colour low-light
- Naked-eye 3D dual-screen display, 2.2" HD screen
- 6000mAh rechargeable battery, IP54, 516g (1.14 lb), F1.0 35mm lens,
  ±6 diopter adjustment, electronic compass, USB-C
- Live page: https://store.wildguarder.com/product/4k-3d-night-vision-binoculars-with-super-starlight/
- Commission at stated 15%: $339.99 × 0.15 ≈ **$51.00/sale**

## Honest caveats (do not hide from Matt)
- Ships direct from WILDGUARDER (support UTC+8): free registered airmail,
  **7–20 business days to the US** after 2–7 business days processing.
  Slower than Amazon — buyers wait. Do not promise fast delivery in copy.
- Other models in the invite are **NOT priced/verified yet** — Hawknite 1 Pro,
  OWLER1, RB4000 rangefinder binoculars, WG-740 solar trail camera,
  TL3100 time-lapse camera. Do NOT quote prices or stage cards for them
  until their live pages are checked. WG9801 (a second night-vision model)
  is $189.99 on the same store (~$28.50/sale at 15%) — a cheaper
  alternative if Matt prefers a lower ticket, but WG9700 is the featured
  pick in the invite and the bigger earner.
- Queue: this is THIRD behind PreCip (sale ends Fri Nov 13, 11:58pm CT)
  and Pinnacle (link 404s today, price now $100). Do not displace either.
  Night vision is scouting/after-dark gear, not opener-day gear — there
  is no Nov 14 deadline pressure on this one.

## Still missing for the card
1. **Awin join** — click "Join Programme" in Awin (merchant 126831),
   accepting the programme T&Cs. Precedent: TideWe and Piscifun were
   joined under the operator directive (affiliate joins are execution,
   not asks); MeoWant was asked first only because it was off-brand.
   WILDGUARDER is on-brand Hunt, so the join follows the TideWe pattern.
   Expect the Awin 2-Step Verification setup prompt at sign-in again
   (Matt declined it 2026-11-06 — 2SV still NOT set up); if the browser
   session has lapsed, the join may need his tap to decline it again.
2. **Awin tracked link** — build in Awin Link Builder after joining
   (pattern: https://www.awin1.com/cread.php?awinmid=126831&awinaffid=3131873&ued=<URL-encoded product URL>).
   Curl it and confirm it lands on the live WG9700 page (HTTP 200)
   before deploying — do NOT deploy a link to a dead page.
3. **Product image** — official WG9700 product shot, save under
   site/img/wildguarder-wg9700.jpg. Not yet pulled (the store page
   did not expose a usable og:image to curl on 2026-11-12).

## Card HTML — insert in the Hunt shelf, after the HotHands card
(site/index.html, inside <section id="hunt">, before the closing </div>.
NOTE: Marmot PreCip and Kings Pinnacle both want the same insertion point —
insert sequentially and bump the product count once per card deployed;
58 → 59 for the first of the three, not 59 for all three.)

      <article class="product">
        <figure class="showcase"><img src="img/wildguarder-wg9700.jpg" alt="WILDGUARDER WG9700 4K night vision binoculars" loading="lazy"></figure>
        <h3>WILDGUARDER WG9700 Night Vision Binoculars</h3>
        <p class="spec-line">4K video · 36MP photos · 1000m night vision · 940nm invisible IR</p>
        <p class="pick">See the field after dark without giving yourself away. A super-starlight sensor holds full colour in near-darkness, 940nm infrared reaches out to 1,000 metres with no visible red glow, and it records in 4K with a 6,000mAh battery behind it. The one for spotting hogs and coyotes — or just knowing what's moving out there before first light.</p>
        <p class="verdict-line">Field verdict: the night-vision pick for hunters who scout after dark.</p>
        <a class="buy" href="AWIN_TRACKED_LINK_WG9700" rel="sponsored nofollow noopener" target="_blank">Check price</a>
      </article>

## Deploy steps (main agent)
1. Join WILDGUARDER on Awin (merchant 126831); verify "(Joined)" + the
   commission/cookie in Commission Manager, and report the confirmed rate
   (do not keep quoting 15% if Awin shows otherwise).
2. Build the Awin tracked deep link for WG9700; curl-verify HTTP 200 on
   the live product page.
3. Pull the official product image, save as site/img/wildguarder-wg9700.jpg,
   check it renders.
4. Insert ONLY this card in site/index.html in the Hunt shelf.
5. Deploy via the normal Cloudflare Pages zip path; update the product
   count in the hero/sign-open line/meta description by +1 for this card.
6. Verify live on blackpinefield.com, then report the card live to Matt.
7. Also push the text layer to the GitHub source of truth per his standing
   preference.

No refund language, no untracked link — Awin tracked only, per the
profitable-shelves rule. Do NOT retarget another brand's button to
WILDGUARDER.
