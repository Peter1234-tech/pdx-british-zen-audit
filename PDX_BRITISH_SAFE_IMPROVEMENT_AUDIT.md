# PDX British — Safe Improvement Audit

**Document Version:** 1.0
**Date:** April 27, 2026
**Branch:** safe-conversion-polish-v1
**Auditor:** Manus AI (at direction of site owner)
**Scope:** Read-only analysis of `premium_site/` files. No files were modified.

> **Important:** This is a real website for a real business — PDX British, Portland, OR. All observations are based solely on code and content already present in the repository. No new facts have been introduced. No changes have been made.

---

## 1. Current Design Strengths

The `premium_site/` version of the PDX British website represents a significant upgrade over the prior public site. The design system is coherent, intentional, and premium in feel.

| Strength | Detail |
|---|---|
| **Color palette** | Dark forest green (`#0a2f2a`), warm gold (`#c9a03d`), and off-white cream (`#f5f0e8`) work together to convey trust, heritage, and quality — appropriate for a high-end automotive specialist |
| **Typography** | Cormorant Garamond (serif headings) paired with Inter (sans-serif body) is a classic premium pairing that reads as authoritative and refined |
| **Sticky header** | The white header with the phone number prominently displayed stays visible as users scroll — a direct fix over the prior site where the number was buried |
| **Top bar** | The dark green top bar with hours, service area, and phone number provides immediate orientation for first-time visitors |
| **Responsive layout** | All pages use CSS grid with defined breakpoints at 900px and 640px, ensuring the site adapts cleanly to mobile and tablet |
| **Consistent shared CSS** | All pages inherit from `shared.css`, meaning the visual baseline is unified and changes to one element propagate correctly |
| **Fade-up animations** | Subtle `fadeUp` entrance animations add polish without being distracting |
| **Image quality** | Hero, gallery, and service images are large, high-resolution, and contextually appropriate (shop, vehicles, off-road, engine work) |
| **Multi-page structure** | Five distinct pages (Home, Services, About, Gallery, Contact) give the site depth and improve SEO potential |

---

## 2. Current Conversion Strengths

The premium site has materially improved the conversion architecture compared to the prior public site, which had a broken contact page and no phone number above the fold.

| Conversion Element | Location | Status |
|---|---|---|
| Phone number `(503) 595-6600` | Top bar, sticky header, hero CTA, contact page, footer | Present on every page, multiple times |
| "Schedule Service" CTA button | Hero section, services page warranty band, CTA band | Gold button — high visual contrast |
| "Book Online" CTA button | Homepage CTA band | Links to contact page |
| Contact form | `contact.html` | Visually complete with fields for name, phone, email, vehicle, service type, and message |
| Quick contact band | `contact.html` | Three-column strip showing phone, email, and address at a glance |
| Google Maps embed | `contact.html` | Embedded map for directions |
| Hours of operation | Top bar, contact page, footer | Clearly stated on every page |
| Email address | Contact page, footer | `service@pdxbritish.com` |
| Fax number | Contact page | `(503) 236-6091` |

**Critical caveat:** The contact form on `contact.html` is currently **front-end only**. The `handleSubmit()` JavaScript function prevents default form submission, hides the form, and shows a success message — but **no data is actually sent anywhere**. A customer who fills out the form and sees "Thank you! Your message has been sent" will believe their request was received when it was not. This is the single most important functional issue on the current site.

---

## 3. Current Trust Signals Already Present

The site does an excellent job surfacing trust signals that were largely absent from the prior public version.

| Trust Signal | Where It Appears |
|---|---|
| **"Since 1991"** — 35+ years of expertise | Hero eyebrow, trust bar, intro badge, about page, footer |
| **4.8★ Google (40 reviews)** | Hero rating pills, stats band, about page trust grid |
| **4.3★ Yelp (38 reviews)** | Hero rating pills, about page trust grid |
| **A+ BBB Rating** | Hero rating pills, trust bar, stats band |
| **Factory T4 TestBook diagnostics** | Trust bar, intro features list, services page (detailed), footer |
| **24-Month / 24,000-Mile Warranty** | Trust bar, services page warranty band, about page amenities |
| **Family-owned by Francis & Elsa Watson** | Trust bar, intro text, about page story, footer |
| **"On-site every day"** | About page, contact page |
| **Three customer testimonials** | Homepage testimonials section (Yelp and Google attributed) |
| **Military discount** | Intro features list, about page amenities |
| **LGBTQ+ friendly** | Intro features list, about page amenities |
| **Written estimates** | About page amenities |
| **Walk-ins welcome** | About page amenities |
| **Free Wi-Fi** | About page amenities |
| **All major credit cards accepted** | About page amenities |

---

## 4. Current Service Sections Already Present

The services page is comprehensive and well-structured. The following are documented in the current code:

**Featured Service Blocks (with images and detailed descriptions):**
1. Factory T4 TestBook Diagnostics
2. EAS Air Suspension & Coil Conversions
3. Custom Off-Road Outfitting
4. Pre-Purchase & For-Sale Inspections

**Full Service Menu (16 items listed in the grid):**
Oil changes & scheduled maintenance · Air conditioning & heating · Automatic transmission service · Brakes / ABS systems · Computer diagnostics (T4 TestBook) · Cooling system repair · EAS / air suspension service · Engine & electrical diagnostics · Exhaust system repair · Ignition & fuel injection · Lift kits / bumpers / winches · Pre-purchase inspections · Off-road & expedition outfitting · Sunroof leak detection (ultrasound) · Transfer case & drivetrain · SRS / airbag systems

**Homepage services preview (3 cards):**
Factory Diagnostics · EAS & Suspension · Off-Road Outfitting

---

## 5. Factual Claims That Should Be Verified Before Publishing

The following claims appear in the current site code. They were sourced from prior research and public listings, not necessarily confirmed directly by the business owner. Each should be verified before the site goes live publicly.

| Claim | Where It Appears | Verification Needed |
|---|---|---|
| **4.8★ Google (40 reviews)** | Hero, stats band, about page | Confirm current Google rating and review count — these change over time |
| **4.3★ Yelp (38 reviews)** | Hero, about page | Confirm current Yelp rating and review count |
| **A+ BBB Rating** | Hero, trust bar, stats band | Confirm current BBB rating; prior audit noted the business is **not formally BBB-accredited** — the A+ rating exists but accreditation status should be clarified |
| **"Since 1991"** | Multiple pages | Confirm founding year with owner |
| **24-Month / 24,000-Mile Warranty** | Trust bar, services page, about page | Confirm this warranty is currently offered and the exact terms are accurate |
| **Francis & Elsa Watson, on-site daily** | Trust bar, about page, contact page | Confirm both owners are still active and on-site |
| **"Scott"** mentioned in testimonial | Homepage testimonials | A testimonial references "Francis and Scott" — confirm Scott is a current team member |
| **Fax: (503) 236-6091** | Contact page | Confirm fax number is still active |
| **Saturday: By Appointment Only** | Contact page hours table, footer | Confirm Saturday availability is current |
| **"Serving Portland, OR & SW Washington"** | Top bar, all pages | Confirm this service area is accurate |
| **6320 SW Macadam Ave, Portland, OR 97239** | Contact page, footer, Google Maps embed | Confirm address is current |
| **"Military discount available"** | Intro features, about amenities | Confirm this discount is still offered |
| **Google Maps embed coordinates** | Contact page | The embed uses approximate coordinates — confirm the pin lands on the correct location |
| **© 2025 PDX British** | Footer, all pages | Update copyright year to 2026 when ready |

---

## 6. Small Improvements That Could Increase Calls or Bookings Without Redesigning

These are functional or copy-level improvements only. None require changing the visual design, layout, colors, or typography.

**A. Fix the contact form so it actually sends submissions.**
The current form shows a fake success message but delivers nothing to the business. This is the highest-priority functional fix. Options include connecting it to Formspree, Netlify Forms, or a simple email service — all of which require no visual changes to the form itself.

**B. Add a `tel:` link to the top bar phone number.**
The top bar currently shows the phone number as plain text with a call-to-action link that reads "Emergency? Call (503) 595-6600 →". The number itself is already a `<a href="tel:...">` on the homepage top bar. Confirm this is consistent across all pages — on some pages the top bar phone is plain text, not a tap-to-call link.

**C. Add `rel="noopener noreferrer"` to external links.**
The footer links to Google Reviews and Yelp with `target="_blank"` but without `rel="noopener noreferrer"`. This is a minor security and performance best practice that takes seconds to fix.

**D. Add a `<meta name="robots">` tag and verify page titles are unique.**
Each page has a unique `<title>` tag, which is good. However, none of the pages include an explicit robots meta tag or a canonical URL tag. These are small SEO additions that do not affect visual design.

**E. Add a `lang` attribute confirmation and `<meta charset>` consistency check.**
All pages correctly include `<html lang="en">` and `<meta charset="UTF-8">` — no change needed here. This is already done correctly.

**F. Verify the Google Maps embed pin is accurate.**
The current embed uses approximate coordinates. If the pin does not land precisely on the shop, customers may be misdirected. This is a one-line fix to the iframe `src`.

**G. Update the copyright year in the footer.**
All pages show `© 2025 PDX British`. This should be updated to `© 2026` when the site goes live.

---

## 7. Risks of Changing Too Much

This section documents why restraint is the correct approach for this site.

**Risk 1 — Breaking a working visual baseline.**
The current `premium_site/` design is clean, coherent, and premium. It was built deliberately. Changing colors, fonts, layout, or spacing risks introducing visual inconsistencies that undermine the professional impression the site currently makes.

**Risk 2 — Introducing unverified facts.**
This is a real business with real customers. Adding claims that are not confirmed (certifications, pricing, team members, awards) could mislead customers and damage trust. Every new factual claim must be verified by the owner before it appears on the site.

**Risk 3 — Disrupting the contact flow.**
The contact page is the most conversion-critical page on the site. Any structural change to the form, the layout, or the CTA buttons risks breaking the user's path to reaching the business. Changes here must be tested carefully.

**Risk 4 — Overbuilding before the scheduling system is ready.**
The owner has confirmed that a scheduling/booking button is planned but not yet implemented. Adding placeholder booking UI before the backend is ready would create a broken experience similar to the form issue already present.

**Risk 5 — Changing copy without owner review.**
The current copy — particularly on the About page and the testimonials — reflects the real voice and story of the business. Rewriting it without owner input risks changing the tone, introducing inaccuracies, or losing the authenticity that makes the current content credible.

---

## 8. Recommended First 3 Micro-Improvements

These three improvements are the highest-value, lowest-risk changes that can be made immediately. Each is small, reversible, and does not alter any visual design.

---

### Micro-Improvement #1 — Fix the Contact Form Backend

**What:** Connect the contact form on `contact.html` to a real form submission service so that customer inquiries are actually delivered to the business.

**Why:** The form currently shows a fake success message. A customer who fills it out believes their request was received — but nothing is sent. This is a silent lead killer. It is the most urgent functional issue on the site.

**How (when ready):** Add a `action="https://formspree.io/f/[your-id]"` attribute to the `<form>` tag and remove the `onsubmit="handleSubmit(event)"` JavaScript handler, replacing it with Formspree's redirect or AJAX approach. No visual changes required.

**Risk level:** Low. The form's appearance does not change. Only the submission behavior changes.

---

### Micro-Improvement #2 — Verify and Update All Factual Claims

**What:** Go through the verification checklist in Section 5 of this document with the business owner and confirm or correct each claim before the site is published.

**Why:** Several claims (review counts, BBB accreditation status, warranty terms, team members) were sourced from public listings during prior research and may have changed. Publishing inaccurate information on a live business site creates legal and reputational risk.

**How:** Owner reviews the list in Section 5 and confirms, corrects, or removes each item. No design work required.

**Risk level:** Zero design risk. Pure content accuracy review.

---

### Micro-Improvement #3 — Add `rel="noopener noreferrer"` to All External Links

**What:** Add `rel="noopener noreferrer"` to all `<a target="_blank">` links across all five pages. Currently the footer links to Google Reviews and Yelp without this attribute.

**Why:** This is a standard web security and performance best practice. Without it, the linked page can access the `window.opener` object of the originating page, which is a minor but real security concern. It also prevents a tab-napping vulnerability. This is a one-line fix per link.

**How:** Find all instances of `target="_blank"` across the five HTML files and add `rel="noopener noreferrer"` to each. No visual change whatsoever.

**Risk level:** Zero. This change is invisible to users and cannot break anything.

---

## Summary Table

| Area | Current Status | Priority |
|---|---|---|
| Design quality | Strong — approved baseline | Preserve as-is |
| Conversion architecture | Good structure, broken form backend | Fix form urgently |
| Trust signals | Comprehensive and well-placed | Verify accuracy before launch |
| Service documentation | Thorough across all pages | No changes needed |
| Factual accuracy | Several claims need owner verification | Review before launch |
| Contact form | Visually complete, functionally broken | Highest priority fix |
| External link security | Missing `rel` attributes | Low-effort fix |
| Copyright year | Shows 2025 | Update to 2026 at launch |
| Scheduling button | Not yet implemented | Planned future work |

---

*This audit was created on the `safe-conversion-polish-v1` branch. No website files were modified. All changes described above must be reviewed and approved by the site owner before implementation.*
