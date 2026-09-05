# Ruid — handover

For Findlay and Andrew. Written 11 August 2026. Plain English, no jargon.

---

## 1. Where things stand

**The website is live and public at [ruidclothing.co.uk](https://ruidclothing.co.uk).** No password. Anyone can visit it.

What's on it:

- **Homepage** — cover photo showing both ranges, three buttons (Shop Heritage / Shop Founders / Our Story), a product row for each collection, and the brand statement.
- **Worn by** (`/pages/worn-by`) — all 12 photos: the rugby players, the team shot, JJ's Ice Cream. Plus a call-out telling people to tag Ruid on socials to get featured, and a line saying to check back for new drops and competitions.
- **Our Story** (`/pages/our-story`) — Findlay's story with the Euston photos, captioned.
- **10 products**, all £25: five Heritage (Slate/Grey, Black, Navy, Olive, Burgundy) and five Founders (Black, Grey, Blue, Light Blue, Green).
- **Legal pages** — Privacy Policy, Delivery, Returns, Contact, Care Instructions. Email signup forms have proper consent wording linked to the Privacy Policy.

---

## 2. The one thing blocking real trading

**The shop can only take PayPal.** Card payments are not switched on.

To accept cards, **Shopify Payments** must be set up. It has to be in **Andrew's name** with business and bank details, because Findlay is 14 and the account can't be in his name.

Where: Shopify admin → **Settings → Payments**.

Until that's done, anyone who wants to pay by card can't check out.

---

## 3. Open actions

### Andrew

| # | Action | Why it matters |
|---|---|---|
| 1 | **Set up Shopify Payments** | Only PayPal works right now. This is the big one. |
| 2 | **Mark the sold-out caps** | Andrew asked for Burgundy, Olive and Navy to show as sold out. **This has not been done** — all five Heritage caps are still showing as available and buyable. See section 5 for exactly how. |
| 3 | **Confirm the Founders price** | £25 was copied across from Heritage as a placeholder. Nobody has confirmed it's right. |
| 4 | **Materials wording** | The "Materials" tab on every product is deliberately blank. Fabric composition legally has to come from the manufacturer — it was left empty rather than guessed. Send the real wording and it can go in. |

### Findlay

| # | Action | Why it matters |
|---|---|---|
| 1 | **Get the socials properly live and posting** | Instagram (@ruid.clothing), TikTok (@ruidclo) and Facebook are already linked on the site. |
| 2 | **Post the launch video** | `ruid-launch-10s.mp4` — 10 seconds, vertical, with sound. Countdown → logo → caps → "we are live" → the web address. Made for Reels/TikTok. |
| 3 | **Collect photos for Worn by** | The page is built to grow. Every photo can have a name and a line of text under it, so it can become testimonials as well as pictures. |

### Nice-to-haves, not urgent

- The Founders collection's web address is `/collections/core` rather than `/collections/founders`. It displays correctly as "Founders Collection" — it's just untidy underneath. Renaming it is safe; Shopify sets up the redirect automatically.
- The competition poster in circulation says it closes **31 August 2025**. It's 2026.
- No UK trademark search has been done on "Ruid" in clothing (class 25). Worth doing before spending on branding.
- Wanted but not built yet: star ratings/testimonials on Worn by, and a dedicated "follow us" socials page.

---

## 4. How to get in

| What | Where |
|---|---|
| Shop (public) | ruidclothing.co.uk |
| Shopify admin | admin.shopify.com/store/**ruid-clothing** |

**Note:** the admin password was changed recently, so only Andrew can get into the admin at the moment. Anything in section 3 that involves products, prices, stock, pages or payments needs that admin login.

---

## 5. How to mark a cap as sold out

This is the most likely thing you'll need to do, so here it is step by step.

Do **not** just put a red cross on the photo. A cross is only a picture — the Buy button would still work, someone could still pay for a cap that doesn't exist, and you'd have to refund them.

Do this instead:

1. Shopify admin → **Products**
2. Click the cap (e.g. *Ruid Heritage – Burgundy*)
3. Scroll to **Inventory**
4. Set the **quantity to 0**
5. **Untick "Continue selling when out of stock"** ← this is the important bit. If it stays ticked, people can still buy it.
6. **Save**

The website then automatically shows a grey **"Sold out"** badge and switches the Buy button off. Nothing else needs changing.

To put it back on sale, set the quantity above 0 again.

---

## 6. Two things that will waste your time if you don't know them

**1. The store's real address isn't what you'd expect.**
The admin URL says `ruid-clothing`, but the store's actual internal address is **`b6kcb8-r6.myshopify.com`**. Any tool that asks for the "myshopify domain" needs `b6kcb8-r6`, not `ruid-clothing`. Using the wrong one fails with a confusing "invalid password" error even when the password is perfectly fine. This cost a lot of time already — don't repeat it.

**2. The Founders collection is called `core` underneath.**
Anything that points at `founders` silently fails to find it. This is what broke the homepage panel — it looked like a missing image, but it was actually pointing at a collection that doesn't exist. Use `core`.

---

## 7. The website files

There's a full copy of the website on Andy's Mac with a complete history of every change:

```
/Users/user/Claude Cowork/Outputs/Ruid-Headwear/ruid-theme-v6-work
```

- **Live theme:** `ruid-theme-v6` (id `201685139790`)
- **Backup:** `ruid-theme-v3` (id `200979284302`) — kept unpublished. If anything ever goes badly wrong, publishing this rolls the whole site back to how it was before.

Design and layout changes can still be made using a **Theme Access token**, which is separate from the admin password and still works. When you take over, the tidy thing to do is create your own: Shopify admin → **Apps → Theme Access → Create password**, then delete the old one.

Worth knowing: **theme changes** (layout, wording in the design, new sections, photos in the design) and **admin changes** (products, prices, stock, pages, menus, payments) are two different jobs. The token only covers the first.

---

## 8. Running it yourselves with Claude Code

The plan is for you two to control this directly rather than going through anyone else.

Claude Code is a tool that runs on a Mac. You describe what you want in normal English — "mark the burgundy cap as sold out", "add these five photos to the Worn by page", "change the homepage headline" — and it makes the change and pushes it to the site.

What you'll need:
- A Mac
- Claude Code installed
- The project folder above
- Your own Theme Access token (section 7)
- Andrew's Shopify admin login for anything involving products, stock or payments

Two habits worth keeping:
- **Ask to see it before it goes live.** Changes can be pushed to a private preview version of the site first, checked, and only then published.
- **Say what you want, not how to do it.** "The Founders caps should show up on the homepage too" works better than trying to describe the technical fix.

---

## 9. What was done in the last session, in case you're curious

Fifteen tracked changes, including: the Worn by page built and published (it had been promised twice and never appeared), Our Story with Findlay's photos, a new homepage cover showing both ranges, a Founders product row so both collections get equal billing, a broken homepage panel fixed, email consent wording added to every signup form, and a placeholder "TODO" removed that was showing to customers in the footer.

---

**Short version:** the site is live and looks good. Andrew needs to sort card payments and the sold-out caps. Findlay needs to get the socials moving and keep the photos coming. Everything else is tidy-up.
