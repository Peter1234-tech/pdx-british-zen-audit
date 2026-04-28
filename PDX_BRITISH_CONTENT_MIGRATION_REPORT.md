# PDX British — Content Migration Report
**Branch:** `safe-conversion-polish-v1`
**Date:** April 27, 2026
**Source of truth:** Current live website at pdxbritish.com
**Files modified:** 3 (index.html, about.html, services.html)
**Gallery:** Not touched (per owner instruction)

---

## What Was Migrated

### 1. `premium_site/index.html` — Testimonials replaced with real named customers

The three placeholder testimonials ("Long-time Customer," "Verified Customer," "Range Rover Sport Owner") were replaced with three real verbatim testimonials from the live site:

| Replaced with | Source |
|---|---|
| Kev & Julia — Discovery serviced, friendly/fast, treat you like family | Live site testimonials page |
| Michelle — Discovery since 1998, Watson family, magic of PDX British | Live site testimonials page |
| Barry — Discovery II, record time, lifetime customer | Live site testimonials page |

All text is verbatim from the live site (condensed for card format, meaning preserved exactly).

---

### 2. `premium_site/about.html` — Live site business description added

The live site's own footer/about description was added as a paragraph in the Our Story section:

> "Family owned since 1991, PDX British have taken care of thousands of happy Land Rover customers in Oregon and SW Washington. We strive to take care of your Land Rover as we would take care of ours… Experienced, fair and friendly service for all your Land Rover and Range Rover needs."

This is verbatim from the live site. The "thousands of happy customers" claim is flagged for owner verification in the checklist.

---

### 3. `premium_site/services.html` — Two service items corrected

| Item | Change |
|---|---|
| "Pre-purchase inspections" | Updated to "Pre-purchase & for-sale inspections" (live site lists both) |
| Mufflers | Added to the full service menu (present on live site, missing from new site) |

---

## What Was NOT Migrated (Flagged for Owner Review)

| Item | Reason not migrated |
|---|---|
| "Terry" in Heidi & Adam and Michael R testimonials | Live site mentions "Francis & Terry" and "Dear Terry" — new site only mentions Francis & Elsa Watson. Who is Terry? Needs owner clarification before publishing. |
| "PDX Rovers" in Heidi & Adam testimonial | Old business name referenced. Needs owner confirmation whether this is acceptable to include. |
| Fax number 503-236-6091 | Present on live site. Not currently on new contact page. Needs owner verification before adding. |
| Full Heidi & Adam testimonial | Contains "PDX Rovers" and "Francis & Terry" — cannot publish without owner clarification. |
| Full Michael R testimonial | Addressed to "Dear Terry" — cannot publish without owner clarification. |

---

## Conflicts Identified

| Conflict | Detail |
|---|---|
| "Terry" vs "Francis & Elsa Watson" | Live site testimonials reference a "Terry" who appears to be a staff member or co-owner. The new site only names Francis & Elsa Watson. These cannot be reconciled without owner input. |
| "PDX Rovers" vs "PDX British" | Heidi & Adam refer to "PDX Rovers" — this may be an old business name. Needs owner confirmation. |
| Hours not on live site | The live site shows no business hours. The new site shows Mon–Fri 8am–5pm, Sat by appointment. Needs owner confirmation. |
| "thousands of happy customers" | This is a live site claim now added to about.html. Flagged in owner checklist for confirmation. |

---

## Design Changes Made

**None.** All changes are content-only. No colors, fonts, layout, spacing, images, navigation, or component behavior was altered.

---

## Gallery

**Not touched.** Per owner instruction, gallery.html was excluded from this migration entirely.

---

## Next Steps for Owner Review

1. Confirm or correct the "Terry" references in testimonials
2. Confirm whether "PDX Rovers" is an acceptable historical reference
3. Confirm fax number 503-236-6091 for addition to contact page
4. Confirm "thousands of happy customers" language
5. Confirm business hours (Mon–Fri 8am–5pm, Sat by appointment)
6. Complete the full PDX_BRITISH_OWNER_VERIFICATION_CHECKLIST.md

---

*This branch is ready for owner review. Do not merge into master until the owner verification checklist is complete.*
