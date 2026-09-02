# Ruid Clothing — taking full control, a plan for Findlay & Andrew

Built from Andy's handover note (`RUIDHANDOVER.md`, 11 August 2026). This document turns that into a step-by-step plan for you two to take over running the store yourselves through your own Claude Code account. Plain English, no jargon.

---

## How to use this

Work through the steps in order. Steps 1–3 are about taking proper ownership of the accounts and tools — do these first, before anything else, so nobody else is relying on Andy's Mac or Andy's logins. Steps 4 onward are the ongoing running of the shop.

---

## Step 1 — Get access properly in your own hands

| What | Who | Action |
|---|---|---|
| Shopify admin login | Andrew | You already have the current password (it was changed recently and only you can get in). Keep it somewhere safe — a password manager, not a note. |
| Findlay's access | Andrew | Findlay is 14, so don't hand him the owner login. Instead, in Shopify admin go to **Settings → Users and permissions → Add staff account**, create one for Findlay, and only tick the permissions he needs (Products, Online Store, Content). Leave off Payments, Settings, and anything financial. |
| Theme Access token | Both | This is what lets Claude Code make design/layout changes. Andy's old token still works — replace it. Shopify admin → **Apps → Theme Access → Create password**, generate your own, then delete Andy's old one so it's no longer valid. |
| The project files | Both | Andy's copy lives on his Mac (`/Users/user/Claude Cowork/Outputs/Ruid-Headwear/ruid-theme-v6-work`). Ask him to send you that whole folder (zip it, AirDrop/USB/cloud transfer) so you have your own copy with full change history. Don't rely on his Mac still being available later. |

**Do this before anything else in section 3 of Andy's note (sold-out caps, payments, etc.) — otherwise you're still depending on someone else's login.**

---

## Step 2 — Lock things down (security tidy-up)

Once you've got your own token and Findlay's staff account set up:

1. Confirm Andy's Theme Access token is deleted (Step 1 above).
2. Change the Shopify admin password again now that it's fully in your hands, and turn on **two-step authentication** if it isn't already on (Settings → Users and permissions).
3. Keep a note somewhere private (not in any shared doc) of:
   - The real store address: **`b6kcb8-r6.myshopify.com`** — not `ruid-clothing`. Any tool asking for "myshopify domain" needs this, or you'll get a confusing wrong-password error for no reason.
   - The Founders collection's internal handle is **`core`**, not `founders`.

These two gotchas already wasted time once (see Andy's section 6) — worth keeping written down somewhere you'll actually check.

---

## Step 3 — Set up your own Claude Code control room

What you need:

- A Mac with Claude Code installed.
- Your own copy of the project folder (Step 1).
- Your own Theme Access token (Step 1) — this is what Claude Code uses to push design/layout changes.
- Andrew's Shopify admin login for anything Claude Code *can't* do directly — products, prices, stock levels, payments (see note below).

**Important distinction to keep in mind:**
- **Theme changes** (layout, homepage wording, new sections, how pages look) → Claude Code can do this directly via the Theme Access token.
- **Admin changes** (marking something sold out, changing a price, turning on payments, editing menus) → these currently need someone logged into the Shopify admin in a browser. The Theme Access token doesn't cover this.

**Optional, later:** if you want Claude Code to also handle stock/price changes directly (not just design), Shopify supports creating a **custom app with Admin API access** (Settings → Apps and sales channels → Develop apps). This is a separate, more powerful credential than the Theme Access token — worth doing once you're comfortable with the basics, not something to rush into, since it can write to products, inventory and orders. Ask me when you're ready and I can help set it up safely (scoped to only what's needed).

**Two habits to keep from day one:**
- Ask for changes to go to a **preview** first, check it looks right, then publish. Don't publish straight to the live site.
- Describe *what* you want, not *how*: "mark the burgundy cap as sold out" or "the Founders caps should show on the homepage too" — not the technical steps.

---

## Step 4 — Clear the blockers (do these first, in this order)

These are carried over from Andy's note — nothing has changed, they're still open:

| Priority | Action | Owner | Why |
|---|---|---|---|
| 1 | **Set up Shopify Payments** (Settings → Payments) — has to be in Andrew's name with business + bank details, since Findlay's 14 | Andrew | Right now only PayPal works. Nobody can pay by card until this is done. |
| 2 | **Mark Burgundy, Olive and Navy Heritage caps as sold out** | Andrew (or Claude Code once admin access is confirmed) | Still showing as buyable even though they're out of stock. Steps: Products → click the cap → Inventory → quantity to 0 → **untick "Continue selling when out of stock"** → Save. A red cross image is not enough — the buy button has to actually be switched off. |
| 3 | **Confirm the Founders price** (currently £25, copied from Heritage as a placeholder) | Andrew | Nobody's actually confirmed this is right. |
| 4 | **Send the Materials wording** for each product | Andrew | Left blank deliberately — fabric composition has to come from the manufacturer, not guessed. Send the real text and it can go straight in. |

---

## Step 5 — Ongoing responsibilities, going forward

Once the blockers above are cleared, this is roughly how the ongoing work splits:

**Andrew — the business/admin side**
- Payments, pricing, stock levels, sold-out/back-in-stock updates.
- Anything involving money, legal pages, or the Shopify admin login.
- Approving bigger changes (new collections, price changes, structural site changes).

**Findlay — the content/brand side**
- Get Instagram (@ruid.clothing), TikTok (@ruidclo) and Facebook properly active and posting regularly.
- Post the launch video (`ruid-launch-10s.mp4`) across Reels/TikTok.
- Collect and send photos for the **Worn by** page — it's built to grow, and each photo can carry a name and a line of text, so it can double as testimonials.
- Day-to-day wording/photo requests to Claude Code (homepage headline, new sections, page copy).

**Both**
- First week: work through Step 4 together so nothing's left half-done.
- Keep using the preview-before-publish habit from Step 3.

---

## Step 6 — A simple ongoing rhythm

Doesn't need to be formal, but worth having *some* cadence rather than only reacting when something breaks:

- **Weekly (5 minutes):** check stock levels against what's actually sold, check for any "sold out" items that need switching back on or off.
- **Whenever something sells out or comes back:** use the sold-out steps in Step 4, row 2.
- **Monthly:** review the socials/photos backlog (new Worn by photos, any competition posts, whether the poster date needs updating — the current one wrongly says it closes 31 August **2025**).

---

## Backlog — not urgent, worth doing when there's time

- Tidy the Founders collection's web address from `/collections/core` to `/collections/founders` (safe to rename — Shopify auto-redirects).
- Run a UK trademark search on "Ruid" for clothing (class 25) before spending more on branding.
- Build out star ratings/testimonials on the Worn by page.
- A dedicated "follow us" socials page.

---

## Quick-reference: things that will waste your time if you forget them

1. **Store address for tools/logins:** `b6kcb8-r6.myshopify.com`, not `ruid-clothing`.
2. **Founders collection's real handle:** `core`, not `founders`.
3. **Marking something sold out** = set quantity to 0 **and** untick "Continue selling when out of stock". A cross on the photo alone does nothing — people can still buy it.
4. **Theme Access token** = design/layout only. **Admin login** = products, prices, stock, payments. Two different jobs, two different credentials.

---

*This plan is based on Andy Heald's handover note dated 11 August 2026. Original file kept for reference; this document is the actionable, ownership-focused version of it for Findlay and Andrew going forward.*
