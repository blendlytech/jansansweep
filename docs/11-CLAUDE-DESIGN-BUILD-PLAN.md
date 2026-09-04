**Document:** Claude Design Build Plan (jansansweep.com)
**Version:** 1.0
**Updated:** September 3, 2026
**Status:** Active
**Authority:** `00-START-HERE.md` — copy authority is `07-MARKETING-AND-WEBSITE.md`

---

# JanSan Sweep — Claude Design Build Plan

This is the operating plan for building **jansansweep.com** in Claude Design. It defines what to prepare before the first prompt, the exact prompt sequence, the standing guardrails to repeat in every prompt, and the acceptance check to run after each pass.

**Governing rule for the whole build:** `07-MARKETING-AND-WEBSITE.md` owns the words. Claude Design owns the layout. Never let the design tool rewrite approved copy — every compliance risk in this project lives in the language, not the pixels.

---

## 1. Build Strategy — Passes, Not One Mega Prompt

One giant prompt produces a generic SaaS template with invented copy. Build in six passes instead, reviewing after each:

| Pass | Output | Why separate |
|---|---|---|
| P0 | Brand context + style tile artboard | Locks tokens before any layout exists |
| P1 | Desktop: nav + hero + problem | Sets the visual system on the highest-stakes screen |
| P2 | Desktop: positioning table + 5-step sprint + deliverables | Dense structural content, needs its own attention |
| P3 | Desktop: pricing + 12 dispositions + proof + FAQ | Conversion and credibility block |
| P4 | Desktop: final CTA + intake form + footer | Compliance-sensitive; must be exact |
| P5 | Mobile artboard (390px) | Table and grid fallbacks are a design problem, not a resize |
| P6 | QA + compliance sweep + export | Catches drift accumulated across passes |

Work on **three artboards on one canvas**: `Style Tile`, `Desktop — 1440`, `Mobile — 390`.

---

## 2. Pre-Flight — Gather Before Prompt 0

### Assets — finished, in `images/`

Vectorized from the Leonardo original on 2026-09-03. Attach the SVGs to Claude Design; use them in the build rather than the JPEG.

| File | Use |
|---|---|
| `logo-navy.svg` | Primary logo, white and light surfaces. 9KB, viewBox cropped to artwork. |
| `logo-white.svg` | Knockout for the navy footer and CTA band |
| `logo-mark.svg` / `logo-mark-white.svg` | JS monogram alone, no wordmark |
| `favicon-16/32/48/180/512.png` | Navy mark, transparent — light browser tabs |
| `favicon-*-ondark.png` | White mark, transparent — dark browser tabs |
| `favicon.ico` | 16/32/48 bundle for `/favicon.ico` |
| `apple-touch-icon-180.png` / `-512.png` | Opaque navy tile, white mark — iOS home screen and PWA |
| `jansansweep-logo.jpg` | Original 2048px raster. Reference only — do not ship. |
| `logo-flat-for-trace.png`, `logo-transparent.png` | Intermediates from the vectorizing pass. Keep for future re-traces. |

Colors are locked to the exact tokens: `#1B2438` navy, `#2563EB` blue.

**Head markup for the finished site:**

```html
<link rel="icon" href="/favicon.ico" sizes="any">
<link rel="icon" type="image/png" href="/favicon-32.png" media="(prefers-color-scheme: light)">
<link rel="icon" type="image/png" href="/favicon-32-ondark.png" media="(prefers-color-scheme: dark)">
<link rel="apple-touch-icon" href="/apple-touch-icon-180.png">
```

### Confirmed values — use these verbatim

| Value | Status |
|---|---|
| Business phone | **928-298-8405** |
| Business email | **info@jansansweep.com** |
| Location | Flagstaff, AZ (Mountain Standard Time) |
| Founder photo | `images/founder.jpg` — real photo of Clay, 1195×896 landscape. Crop to a square or 4:5 portrait for the proof block. |
| Sample Outcome Dashboard | `docs/13-SAMPLE-OUTCOME-DASHBOARD.md` and `templates/sample-outcome-dashboard.csv` — **must ship with its sample-data label**, see below |
| Legal pages | Drafted in `docs/12-WEBSITE-LEGAL-PAGES-DRAFT.md` — publish only after the review step in §7 |
| Payment | **PayPal invoice. There is no checkout URL and no self-serve purchase.** |
| Scheduling link | `[PLACEHOLDER — CALENDLY URL]` — still outstanding |

### Two things that change the page design

**1. No checkout means no "buy now" path.** Payment is a PayPal invoice sent by Clay, so the site cannot take money. Every "buy" CTA becomes a *request* CTA, and the page must say plainly how payment works — an owner who clicks expecting a cart and gets nothing is a lost lead. Approved language:

> Request your Founding Sprint. Clay sends a PayPal invoice, and the seven-day clock starts once it's paid and your records are in.

This is arguably better for a $199 first sale to a skeptical owner: a human step where a card form would have been. Do not let Claude Design build a checkout, a cart, a pricing toggle, or a "secure payment" trust badge row.

**2. The sample dashboard is a format example, not client proof.** JanSan Sweep has no completed sprints, so the dashboard shown on the site is constructed from fictional records. It must carry a visible label saying so, adjacent to the table. The full rationale and the exact label wording are in `docs/13-SAMPLE-OUTCOME-DASHBOARD.md` §"What This Is." Publishing invented records as anonymized real results would violate the guardrails in §4 of this plan.

---

## 3. Brand Token Sheet — Paste This Into Prompt 0

Colors sampled directly from `images/jansansweep-logo.jpg` and reconciled with the design tokens in `07-MARKETING-AND-WEBSITE.md` §5.

```
BASE / SURFACES
--navy-900   #0F172A   page base, footer, dark bands (spec token)
--navy-800   #1B2438   logo navy — sampled from the wordmark; dark cards
--slate-700  #334155   dark-surface borders, muted text on dark
--slate-500  #64748B   secondary body text on light
--slate-200  #E2E8F0   crisp neutral borders on light
--slate-50   #F8FAFC   alternating section band
--white      #FFFFFF   primary page surface

ACCENT
--blue-600   #2563EB   primary accent, buttons, links (spec token)
--blue-logo  #3B74E5   sampled "SWEEP" blue — within a hair of #2563EB, so
                       keep #2563EB as the system accent; the logo reads as a match
--blue-50    #EFF6FF   accent tint for eyebrow badges and callouts

STATUS BADGES (disposition codes)
--emerald    #059669   recovered / live interest  (RR, RV, OP, RB)
--amber      #D97706   pending / unresolved       (NR)
--slate      #64748B   closed / dead              (WI, LI, LP, LT, BD, DNC, X)

TYPOGRAPHY
Headings and body: Inter (fallback Outfit). Tabular figures on all numbers,
prices, and dashboard tables. No serif, no display script, no all-caps body.

GEOMETRY
Radius 8px cards / 6px buttons / 4px badges. Border 1px --slate-200.
Shadows minimal — one soft elevation on cards only. No gradients on text.
Max content width 1120px. Section rhythm 96px desktop / 56px mobile.
```

---

## 4. The Standing Guardrail Block

**Paste this at the end of every prompt, P0 through P6.** It is the most important part of this plan.

```
NON-NEGOTIABLE RULES FOR THIS BUILD:

1. Use the copy I give you VERBATIM. Do not rewrite, shorten, "punch up,"
   or add headlines, taglines, or microcopy of your own. If a layout needs
   a label I did not supply, write [NEEDS COPY] and tell me.

2. Never write any of these — they are compliance violations for this business:
   - guaranteed contracts, guaranteed revenue, guaranteed ROI, "results guaranteed"
   - "cold leads," "we find you new clients," "new customer acquisition"
   - AI voice agents, automated outreach, autodialer, robocall, "AI-powered"
   - "explode your pipeline," "7-figure," "10x," growth-hacking hype
   - artificial urgency: countdown timers, "only 2 spots left today," "ends tonight"
   - "pay only if you close," commission-based or performance-based pricing

3. Invent nothing. No testimonials, no client logos, no star ratings, no
   "trusted by 500+ companies," no fabricated statistics, no made-up case
   studies, no placeholder company names in a logo strip. This business has
   zero paid clients today and the page must be honest about that.

4. No stock photography of cleaners, offices, or handshakes. Use structural
   design — type, spacing, borders, badges, tables, and the JS mark — to carry
   credibility. Real screenshots and the founder's real photo only.

5. Any value I have not given you (phone number, booking link, checkout link)
   renders as a visible [PLACEHOLDER] token. Do not fabricate a phone number,
   URL, address, or email.

Tone: direct, pragmatic, calm. This page is read by blue-collar commercial
cleaning owner-operators who distrust marketing agencies. Credible utility,
not startup polish.
```

---

## 5. The Prompt Sequence

The prompts below are annotated with `[paste ...]` markers so you can see where each piece of copy comes from. **For the actual build, use `14-WEBSITE-COPY-PASTE-KIT.md` instead** — it contains these same seven prompts with every copy block and the guardrails already inlined, ready to paste without assembly. Read this section for the reasoning and the acceptance checks; paste from the kit.

### Prompt 0 — Context + Style Tile

> I'm building a single-page marketing site for **JanSan Sweep**, a proposal follow-up service for independent commercial cleaning companies. I've attached the logo. Before any page layout, build me a **Style Tile artboard** only.
>
> Show: the color tokens below as labeled swatches; the Inter type scale (hero H1, section H2, subhead, body, small, tabular figures); primary / secondary / ghost button states; the eyebrow badge; a card; a table header and row treatment; and the three status badge styles (emerald "recovered," amber "pending," slate "closed").
>
> [PASTE THE BRAND TOKEN SHEET FROM §3]
>
> Aesthetic direction: high-credibility B2B utility. Think a well-made operations dashboard or a contractor's written estimate — clean, dense, legible, zero decoration. Avoid the generic gradient-blob SaaS landing page look entirely.
>
> The logo is a JPEG with a white background. Show me both how it sits on white and a proposed light/knockout version for the navy footer.
>
> [PASTE THE STANDING GUARDRAIL BLOCK]

**Accept when:** swatches match the tokens, the type scale is legible at small sizes, buttons don't look like a stock template, nothing decorative crept in.

---

### Prompt 1 — Nav + Hero + Problem

> Start the **Desktop — 1440** artboard. Build the top three sections only, stacked, using this exact copy.
>
> **NAV** — logo left. Links: How It Works | What It Is | Pricing | FAQ. Right-side button: `Book a 15-Min Bid Audit`. Sticky, white, 1px bottom border.
>
> **HERO**
> - Eyebrow badge: DEDICATED PROPOSAL FOLLOW-UP FOR COMMERCIAL CLEANING OPERATORS
> - H1: Turn Dormant Commercial Cleaning Proposals Into Clear Decisions.
> - Subhead: [paste the full hero subheadline from 07-MARKETING-AND-WEBSITE.md, Section 2]
> - Primary button: `Claim a $199 Founding Sprint`
> - Secondary text link: `Schedule a 15-Minute Bid Review`
> - Trust strip, four items in a row with small check or shield icons: 100% Manual, Live US-Based Calls · Client-Approved Scripts & Identity · Zero Cold Lists or Robocalls · Complete Record-Level Outcome Dashboard
>
> The hero has **no illustration and no hero photo.** If it needs a right-hand visual, use a small realistic mock of the Outcome Dashboard — columns Business, Facility, Proposal Date, Disposition, Next Step. Use exactly these five rows: [paste rows 001, 003, 005, 011, and 013 from `13-SAMPLE-OUTCOME-DASHBOARD.md`]. They cover one of each badge color. Add the short sample-data caption beneath the mock.
>
> **PROBLEM SECTION** on a `#F8FAFC` band.
> - H2: The Walkthrough Was Weeks Ago. What Happened to the Bid?
> - [paste the body copy and the three-bullet operational fires list]
> - Then three cards side by side: Forgotten Pipeline / Lost Rebid Timing / False Pipeline Hope, each with its paragraph from the doc.
>
> [PASTE THE STANDING GUARDRAIL BLOCK]

**Accept when:** the H1 is the first thing you see, the trust strip reads as information rather than decoration, the dashboard mock looks like a real spreadsheet and not an abstract chart, and no copy was invented.

---

### Prompt 2 — Positioning Table + 5-Step Sprint + Deliverables

> Continue the Desktop artboard below the problem section.
>
> **IS / IS NOT** — H2: Clear Separation. Zero Gimmicks. Subhead: [paste]. Then a two-column comparison. Left column "What JanSan Sweep Is" with a subtle emerald check; right column "What JanSan Sweep Is NOT" with a neutral slate ×. Six rows — [paste all six pairs]. Do **not** make the right column red or alarming; it is a clarification, not a warning.
>
> **HOW IT WORKS** — H2: Five Steps. Seven Business Days. Total Clarity. Five numbered steps as a stepper with a connecting rule. [paste all five step titles and bodies]. Step 3 contains the transparent-identity script line — set it as a pull-quote in the accent tint. That sentence is a core trust asset and should be visually prominent.
>
> **DELIVERABLES** — H2: Everything Included in Your Sprint. Three grouped columns — Kickoff & Data Cleanliness / Outreach Execution / Reporting & Asset Delivery — each with its bullet list [paste].
>
> [PASTE THE STANDING GUARDRAIL BLOCK]

**Accept when:** the comparison reads at a glance, the stepper's numbers don't crowd out the text, the script pull-quote is prominent.

---

### Prompt 3 — Pricing + Dispositions + Proof + FAQ

> Continue the Desktop artboard.
>
> **PRICING** — H2: Simple, Transparent Pricing. No Long Contracts. Two cards side by side.
> - Card 1 (emphasized, accent border): Founding Pilot Sprint, **$199** prepaid. [paste availability, scope, duration, includes]. Button: `Claim Founding Pilot ($199)`
> - Card 2 (neutral): Standard Recovery Sprint, **$299** prepaid. [paste]. Button: `Book an Intake Call`
> - Below both, the note about expanded scope as a quiet footnote — **not** a highlighted callout.
>
> "Limited to the first 3 cleaning operators" is a factual scope statement. Style it as a plain badge. **No countdown timer, no progress bar, no spots-remaining counter.**
>
> **DISPOSITIONS** — H2: Silence Turned Into 12 Documented Dispositions. Subhead: [paste]. A 12-item grid, 3 or 4 across. Each item: the two-letter code as a tabular/monospace badge, the name, the one-line definition. Color the badges by group — emerald for RR/RV/OP/RB, amber for NR, slate for WI/LI/LP/LT/BD/DNC/X. [paste all twelve]
>
> **PROOF** — use this H2 exactly: Who Actually Makes the Calls. Left: the founder block for Clay — background in B2B cold calling, appointment setting, and pipeline organization; direct phone `928-298-8405`; email `info@jansansweep.com`; his photo (attached, `founder.jpg`) cropped square or 4:5 portrait. Right: two artifacts — the sample Outcome Dashboard, and the approved calling script shown as a document card.
>
> Under the dashboard, place this label so it is impossible to miss: [paste the sample-data label from `13-SAMPLE-OUTCOME-DASHBOARD.md`]. Style it as a visible caption in a bordered note, not as fine print.
>
> Below both, a short "The Qualified Record Standard" block listing which records are accepted and which are refused [paste from FAQ #6].
>
> This section must make clear the business is new and pre-validation. No proof it hasn't earned. Every figure in the dashboard is a fictional example — do not summarize it into a headline statistic anywhere on the page.
>
> **FAQ** — H2: Frequently Asked Questions. Eight accordion items, collapsed by default except the first. [paste all eight Q&As verbatim — these answers are compliance-load-bearing, especially #3 on guarantees and #8 on automation]
>
> [PASTE THE STANDING GUARDRAIL BLOCK]

**Accept when:** no urgency mechanics anywhere, all 12 codes present and correctly grouped, FAQ answers unedited, and the proof section contains zero fabricated social proof.

---

### Prompt 4 — Final CTA + Intake Form + Footer

> Finish the Desktop artboard.
>
> **FINAL CTA** — full-width `#0F172A` navy band. Headline: Find Out What Happened to Your Last 20 Proposals. Two paths side by side:
> - Path A — "Book a 15-Minute Proposal Audit": a form with Business Name; Owner / Contact Name; Direct Phone; Email; "Approximately how many commercial proposals have you sent in the last 3–12 months?" (select: 1–5 / 6–15 / 16–30 / 30+); "Do you currently have at least 10 unclosed proposals stored in email, spreadsheets, or bidding software?" (Yes / No / Not Sure). Submit: `Book My Bid Audit`. A Cal.com/Calendly widget goes here at build time — leave a clearly marked embed slot.
> - Path B — "Ready Now": a compact card, $199 prepaid, button `Request My Founding Sprint`. Under the button, in plain readable text: "Clay sends a PayPal invoice. Your seven-day sprint starts once it's paid and your records are in." **There is no online checkout — do not build a cart, a card form, a pricing toggle, or a payment trust-badge row.** The button opens the same request form as Path A with the sprint pre-selected, or a short two-field version (name + email).
>
> Use the knockout/light logo on this band, not the white-background JPEG.
>
> **FOOTER** — navy. Logo, then:
> - Business description: [paste]
> - Compliance statement: [paste in full — legally load-bearing, do not shorten]
> - Legal links row: Privacy Policy | Terms of Service | Refund Policy | Client Outreach Agreement | Do-Not-Call Policy
> - Tracking statement: This site sets no advertising or analytics cookies and uses no third-party trackers.
> - Contact: Clay · 928-298-8405 · info@jansansweep.com · PO Box 2524, Rimrock, AZ 86335 · Mountain Standard Time
> - © 2026 JanSan Sweep. All rights reserved.
>
> The compliance statement should be legible body text, not 10px grey legalese. For this business it is a selling point, not fine print.
>
> [PASTE THE STANDING GUARDRAIL BLOCK]

**Accept when:** the compliance paragraph is readable, the form fields match the spec exactly, and there is no white logo box on the navy band.

---

### Prompt 5 — Mobile Artboard

> Create the **Mobile — 390** artboard: the same page, adapted. Specific requirements:
>
> - Nav collapses to logo plus a single visible `Book a Bid Audit` button. If you use a hamburger, the CTA stays outside it.
> - The Is / Is Not comparison becomes stacked pairs, not a horizontally scrolling table — each row shows its "Is" and "Is NOT" as a linked pair so the contrast survives.
> - The 12 dispositions become a single-column list, code badge left, text right.
> - The dashboard mock scrolls horizontally inside its own container; the page body never scrolls sideways.
> - All tap targets ≥ 44px. Buttons full-width. Section rhythm drops to 56px.
> - The hero subheadline stays complete — do not truncate it on mobile.
>
> [PASTE THE STANDING GUARDRAIL BLOCK]

**Accept when:** nothing is truncated, there is no horizontal page scroll, and the comparison still communicates contrast.

---

### Prompt 6 — QA Sweep + Export

> Final pass. Audit both artboards and report before changing anything:
>
> 1. **Copy diff** — list every string on the page that does not appear verbatim in the copy I supplied. I expect that list to be empty except for [PLACEHOLDER] and [NEEDS COPY] tokens.
> 2. **Prohibited language scan** — check every string against the banned list in my rules block and report any hit.
> 3. **Invented content scan** — flag any testimonial, logo, statistic, rating, or company name I did not supply.
> 4. **Contrast** — verify all text meets WCAG AA against its background, especially slate-on-white body text and anything on the navy bands.
> 5. **Placeholders** — list every [PLACEHOLDER] so I know exactly what I still owe before launch.
>
> Then fix only what the audit flagged. Afterward, export the design as static HTML/CSS: semantic markup, a system-font fallback stack for Inter, no JavaScript frameworks, no analytics or tracking libraries, images optimized. Target a sub-second load on a static host.

**Accept when:** the copy diff is empty, the placeholder list matches §2, and contrast passes.

---

## 6. Review Checklist — Reject and Re-Prompt If You See

- Any sentence you don't recognize from `07-MARKETING-AND-WEBSITE.md`
- A testimonial, a "trusted by" logo strip, a star rating, or a statistic with no source
- A countdown, a spots-remaining counter, or any urgency device beyond the plain "first 3 operators" fact
- Stock photos of cleaners, mops, sparkling offices, or handshakes
- The words *guarantee*, *AI*, *automated*, *leads*, or *10x* anywhere on the page
- The white-background logo JPEG sitting on a navy section
- Body text below 16px, or the compliance statement shrunk into grey fine print
- A hero that says something vaguer than the approved headline

---

## 7. After the Build

1. Run the finished copy back through the **Website Copy Refinement** prompt in `10-CLAUDE-PROMPTS.md` as an independent compliance check.
2. Replace the remaining `[PLACEHOLDER — CALENDLY URL]` with the real scheduling link, or remove Path A's embed and route the audit request through the form plus a phone number. Do not launch with a dead calendar slot.
3. Logo and favicon assets are done — see §2. Ship the SVGs, not the JPEG, and include the four `<link>` tags in the head.
4. Publish the four legal pages from `12-WEBSITE-LEGAL-PAGES-DRAFT.md`. They are complete: R. Clay Mills d/b/a JanSan Sweep, PO Box 2524 Rimrock, Coconino County venue, effective September 4, 2026. Two things remain — move the effective date forward if the launch slips past the 4th, and complete the attorney review that `06-COMPLIANCE-AND-DATA.md` already requires. Do not accept a client's records under an unreviewed Client Outreach Agreement.
5. Verify the site never implies self-serve purchase: no cart, no card form, no "instant access." Payment is a PayPal invoice from Clay.
6. Log the launch, and any pricing or claim change the site introduces, in `09-ROADMAP-AND-DECISIONS.md`.
7. When the first three $199 sprints complete, replace the sample dashboard's fictional records with real anonymized results per `07-MARKETING-AND-WEBSITE.md` Section 10 — with written permission only — and drop the sample-data label at that point.
