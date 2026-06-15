# Humble Hearted Jewelry — Shopify Design

Custom storefront design for **Humble Hearted Jewelry Co.**
(`humble-hearted-jewelry-co.myshopify.com`), built from the Claude Design mockups.

This repo contains the **custom design layer** (the files that were added on top of
the store's base **Drive** theme), the original design sources, and a standalone
HTML preview.

> ⚠️ **This repo is NOT a complete, standalone Shopify theme by itself.** A deployable
> Shopify theme needs ~150 base files (layout, config, locales, all templates, JS/CSS
> assets). Those base files live in the store's **"Copy of Drive"** theme. See
> **Deploying** below for the correct way to get a complete theme into GitHub.

---

## What's in here

```
custom-theme/                     # the custom files added to the Drive theme
  layout/hh-standalone.liquid     # minimal layout (no header/footer) for the homepage
  sections/hh-home.liquid         # full homepage design (hero, shop-the-look, best sellers, video, etc.)
  sections/hh-earrings-collection.liquid  # dark/gold collection grid design
  templates/index.json            # homepage template -> hh-home section + hh-standalone layout
  templates/collection.hh-earrings.liquid # standalone collection template
  assets/hh-logo.png              # HH logo
preview/earrings.html             # standalone static version of the Earrings page (open in any browser)
design-source/                    # original Claude Design mockups (.dc.html), README, chat transcript
```

## What was already done on the store

- **12 earring products** created (ACTIVE) with materials/specs, sustainability, and
  shipping/returns/warranty copy, New/Sale tags, and a compare-at sale price.
- **"Earrings" collection** created and published (`/collections/earrings`).
- The **homepage** and the **Earrings collection page** designs were pushed into the
  unpublished **"Copy of Drive"** theme. The live storefront (the **Drive** theme) was
  left untouched.

---

## Deploying

### Option A — Recommended: connect the theme to this repo (gets the COMPLETE theme)

The custom files above already live in the **"Copy of Drive"** theme on the store, so
letting Shopify push that theme to GitHub gives you a complete, deployable repo —
custom design included.

1. Shopify admin → **Online Store → Themes**
2. On **"Copy of Drive"** → **⋯ → Connect to GitHub**
3. Authorize GitHub, pick **`marcusworld82/HH`**, and choose a branch
   (e.g. `shopify-theme`).
4. Shopify commits the entire theme (all ~150 files **including these customizations**)
   to that branch.
5. From then on it's a real theme in GitHub — edits sync both ways, and you can publish
   from **Themes → Copy of Drive → Publish**.

### Option B — Apply the custom files to a Drive theme manually

If you already have a Drive theme in a repo/theme, copy the files from `custom-theme/`
into the matching folders (`layout/`, `sections/`, `templates/`, `assets/`), then in
the theme set the **Earrings** collection's template to `collection.hh-earrings`.

---

## Notes

- Product/category images render as the design's placeholder panels until real product
  photos are added — drop a photo on a product and it appears automatically.
- Nav links to Necklaces / Rings / Bracelets point to collections that don't exist yet
  (they'll 404 until created). Earrings works.
- The logo falls back to a "HUMBLE HEARTED" wordmark if no theme logo is set.

🤖 Built with [Claude Code](https://claude.com/claude-code)
