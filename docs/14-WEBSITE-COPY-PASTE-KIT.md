**Document:** Website Copy Paste Kit (Claude Design)
**Version:** 1.0
**Updated:** September 3, 2026
**Status:** Active
**Authority:** `00-START-HERE.md` — copy sourced verbatim from `07-MARKETING-AND-WEBSITE.md` v1.2

---

# JanSan Sweep — Website Copy Paste Kit

Seven self-contained prompts. Each block below is complete: layout direction, the exact approved copy, and the guardrails, already assembled. Copy one block, paste it into Claude Design, review against the acceptance check, move to the next.

**Do not edit the copy inside these blocks.** It is reproduced verbatim from `07-MARKETING-AND-WEBSITE.md`, which is the copy authority. If something reads wrong, fix it in that document first and regenerate here — otherwise the site and the spec drift apart and the compliance review in `10-CLAUDE-PROMPTS.md` becomes meaningless.

**Attach to the Claude Design conversation:** `images/jansansweep-logo.jpg` (for every prompt) and `images/founder.jpg` (for Prompt 3).

**Sequence and acceptance checks** live in `11-CLAUDE-DESIGN-BUILD-PLAN.md` §5. This document is the payload; that one is the process.

---

## Prompt 0 — Context + Style Tile

```text
I'm building a single-page marketing site for JanSan Sweep, a proposal follow-up
service for independent commercial cleaning companies. I've attached the logo.
Before any page layout, build me a Style Tile artboard only.

Show: the color tokens below as labeled swatches; the Inter type scale (hero H1,
section H2, subhead, body, small, tabular figures); primary / secondary / ghost
button states; the eyebrow badge; a card; a table header and row treatment; and
the three status badge styles (emerald "recovered," amber "pending," slate
"closed").

BRAND TOKENS

  BASE / SURFACES
  --navy-900   #0F172A   page base, footer, dark bands
  --navy-800   #1B2438   logo navy, sampled from the wordmark; dark cards
  --slate-700  #334155   dark-surface borders, muted text on dark
  --slate-500  #64748B   secondary body text on light
  --slate-200  #E2E8F0   crisp neutral borders on light
  --slate-50   #F8FAFC   alternating section band
  --white      #FFFFFF   primary page surface

  ACCENT
  --blue-600   #2563EB   primary accent, buttons, links
  --blue-50    #EFF6FF   accent tint for eyebrow badges and callouts

  STATUS BADGES
  --emerald    #059669   recovered / live interest  (RR, RV, OP, RB)
  --amber      #D97706   pending / unresolved       (NR)
  --slate      #64748B   closed / dead              (WI, LI, LP, LT, BD, DNC, X)

  TYPOGRAPHY
  Headings and body: Inter, fallback Outfit. Tabular figures on all numbers,
  prices, and dashboard tables. No serif, no display script, no all-caps body.

  GEOMETRY
  Radius 8px cards / 6px buttons / 4px badges. Border 1px --slate-200.
  Shadows minimal, one soft elevation on cards only. No gradients on text.
  Max content width 1120px. Section rhythm 96px desktop / 56px mobile.

The accent #2563EB is a near-exact match for the blue in the attached logo
wordmark (#3B74E5) — treat them as the same color and use #2563EB throughout.

Aesthetic direction: high-credibility B2B utility. Think a well-made operations
dashboard or a contractor's written estimate — clean, dense, legible, zero
decoration. Avoid the generic gradient-blob SaaS landing page look entirely.

The logo is a JPEG with a white background. Show me both how it sits on white
and a proposed light/knockout version for the navy footer.

NON-NEGOTIABLE RULES FOR THIS BUILD:

1. Use the copy I give you VERBATIM. Do not rewrite, shorten, "punch up," or add
   headlines, taglines, or microcopy of your own. If a layout needs a label I did
   not supply, write [NEEDS COPY] and tell me.

2. Never write any of these — they are compliance violations for this business:
   - guaranteed contracts, guaranteed revenue, guaranteed ROI, "results guaranteed"
   - "cold leads," "we find you new clients," "new customer acquisition"
   - AI voice agents, automated outreach, autodialer, robocall, "AI-powered"
   - "explode your pipeline," "7-figure," "10x," growth-hacking hype
   - artificial urgency: countdown timers, "only 2 spots left today," "ends tonight"
   - "pay only if you close," commission-based or performance-based pricing

3. Invent nothing. No testimonials, no client logos, no star ratings, no "trusted
   by 500+ companies," no fabricated statistics, no made-up case studies, no
   placeholder company names in a logo strip. This business has zero paid clients
   today and the page must be honest about that.

4. No stock photography of cleaners, offices, or handshakes. Use structural
   design — type, spacing, borders, badges, tables, and the JS mark — to carry
   credibility. Real screenshots and the founder's real photo only.

5. There is no online checkout. Payment is a PayPal invoice sent by the founder.
   Never build a cart, a card form, a pricing toggle, "instant access," or a
   payment trust-badge row.

Tone: direct, pragmatic, calm. This page is read by blue-collar commercial
cleaning owner-operators who distrust marketing agencies. Credible utility, not
startup polish.
```

---

## Prompt 1 — Nav + Hero + Problem

```text
Start the Desktop — 1440 artboard. Build the top three sections only, stacked,
using this exact copy.

=== NAV ===
Logo left. Links: How It Works | What It Is | Pricing | FAQ
Right-side button: Book a 15-Min Bid Audit
Sticky, white, 1px bottom border.

=== HERO ===

Eyebrow badge:
DEDICATED PROPOSAL FOLLOW-UP FOR COMMERCIAL CLEANING OPERATORS

H1:
Turn Dormant Commercial Cleaning Proposals Into Clear Decisions.

Subheadline:
You walked the facility. You scoped the square footage. You sent the proposal.
Then the prospect went quiet. JanSan Sweep runs a disciplined, 7-business-day
human follow-up sprint across up to 20 past proposals—recovering review calls,
revision requests, and future rebid dates while closing dead records.

Primary button: Claim a $199 Founding Sprint
Secondary text link: Schedule a 15-Minute Bid Review

Trust strip, four items in a row with small check or shield icons:
100% Manual, Live US-Based Calls
Client-Approved Scripts & Identity
Zero Cold Lists or Robocalls
Complete Record-Level Outcome Dashboard

The hero has no illustration and no hero photo. For the right-hand visual, use a
realistic mock of the Outcome Dashboard with columns: Business | Facility |
Proposal Date | Disposition | Next Step. Use exactly these five rows:

Northline Medical Plaza | Medical clinic | 2026-05-12 | RR Review requested | Owner call scheduled
Valley Freight Terminal | Industrial | 2026-06-03 | RV Revision requested | Revised quote
Sunview Dental Group | Dental office | 2026-02-24 | RB Rebid date | March renewal
Lakewood Family Practice | Medical clinic | 2026-04-14 | LP Lost — price | Close record
Copper Hills Apartments | Multi-family | 2026-02-19 | NR No response | Close record

Badge colors: RR, RV and RB emerald; NR amber; LP slate.

Directly beneath the mock, in small but legible text:
Sample dashboard — illustrative format only. Not client results.

=== PROBLEM SECTION === (on a #F8FAFC band)

H2:
The Walkthrough Was Weeks Ago. What Happened to the Bid?

Body:
Running an independent commercial cleaning business means fighting daily
operational fires:

- Cleaners call off at 4:30 PM.
- A supply order didn't arrive.
- A property manager demands an immediate walk-through inspection.

Meanwhile, legitimate commercial proposals you labored over sit untouched in your
inbox, spreadsheet, or bidding software. You called once or twice. They didn't
pick up. Now weeks have passed, and nobody owns the next touch.

Then three cards side by side, under the label "The Three Hidden Costs of
Dormant Bids":

1. Forgotten Pipeline
   Prospects get busy. Many meant to award the work or need a simple scope
   adjustment, but got distracted.

2. Lost Rebid Timing
   If a competitor won, that contract will come up for renewal in 12 months.
   Without follow-up, you will never know the rebid date.

3. False Pipeline Hope
   Keeping dead bids on your mental ledger wastes attention. A definitive "no"
   cleans your board so you focus on live revenue.

NON-NEGOTIABLE RULES FOR THIS BUILD:

1. Use the copy I give you VERBATIM. Do not rewrite, shorten, "punch up," or add
   headlines, taglines, or microcopy of your own. If a layout needs a label I did
   not supply, write [NEEDS COPY] and tell me.

2. Never write any of these — they are compliance violations for this business:
   - guaranteed contracts, guaranteed revenue, guaranteed ROI, "results guaranteed"
   - "cold leads," "we find you new clients," "new customer acquisition"
   - AI voice agents, automated outreach, autodialer, robocall, "AI-powered"
   - "explode your pipeline," "7-figure," "10x," growth-hacking hype
   - artificial urgency: countdown timers, "only 2 spots left today," "ends tonight"
   - "pay only if you close," commission-based or performance-based pricing

3. Invent nothing. No testimonials, no client logos, no star ratings, no "trusted
   by 500+ companies," no fabricated statistics, no made-up case studies, no
   placeholder company names in a logo strip. This business has zero paid clients
   today and the page must be honest about that.

4. No stock photography of cleaners, offices, or handshakes. Use structural
   design — type, spacing, borders, badges, tables, and the JS mark — to carry
   credibility. Real screenshots and the founder's real photo only.

5. There is no online checkout. Payment is a PayPal invoice sent by the founder.
   Never build a cart, a card form, a pricing toggle, "instant access," or a
   payment trust-badge row.

Tone: direct, pragmatic, calm. This page is read by blue-collar commercial
cleaning owner-operators who distrust marketing agencies. Credible utility, not
startup polish.
```

---

## Prompt 2 — Positioning Table + 5-Step Sprint + Deliverables

```text
Continue the Desktop — 1440 artboard below the problem section.

=== IS / IS NOT ===

H2:
Clear Separation. Zero Gimmicks.

Subhead:
We are not a generic lead agency or an automated software bot. We are a
specialized follow-up sprint.

Two-column comparison. Left column header "What JanSan Sweep Is" with a subtle
emerald check. Right column header "What JanSan Sweep Is NOT" with a neutral
slate ×. Six rows:

1. Follow-up on legitimate proposals you already submitted
   | Cold lead generation or purchased email/phone lists

2. Manual, professional human calls and tailored emails
   | AI voice bots, autodialers, or mass automated blasts

3. Complete pipeline cleanup with documented outcome codes
   | A guarantee of signed contracts, meetings, or revenue

4. Immediate handoff the moment a prospect wants to talk
   | Proposal repricing or contract negotiation (you keep control)

5. Future rebid date tracking for long-term contract pipeline
   | Debt collection or aggressive telemarketing

6. Low-risk 7-day sprint with a hard 20-record scope
   | An open-ended retainer before value is proven

Do NOT make the right column red or alarming. It is a clarification, not a
warning.

=== HOW IT WORKS ===

H2:
Five Steps. Seven Business Days. Total Clarity.

Five numbered steps as a stepper with a connecting rule:

Step 1: 15-Minute Kickoff & Intake
You send a spreadsheet of up to 20 dormant commercial proposals (business name,
contact, facility type, proposal date, last-known notes).

Step 2: Eligibility Check & Script Approval
We verify that records represent legitimate prior business engagement. You review
and approve the exact contact language and calling cadence before a single call
is placed.

Step 3: Disciplined Human Outreach
Over seven business days, Clay personally conducts manual phone calls and
personalized emails. Transparent identity: "Hi, this is Clay with JanSan Sweep
following up on behalf of [Your Company]..."

Step 4: Immediate Live Handoff
The second a prospect requests a walkthrough review, asks for a revised quote, or
wants to speak with the owner, their details and conversation notes are handed
directly to you in real time.

Step 5: Outcome Dashboard & Closeout
At the end of Day 7, you receive a clean disposition dashboard showing the status
of every single proposal—including future renewal dates, confirmed losses, and
recommended 30/90-day next steps.

Set the quoted identity line inside Step 3 as a pull-quote in the accent tint.
That sentence is a core trust asset and should be visually prominent.

=== DELIVERABLES ===

H2:
Everything Included in Your Sprint

Three grouped columns:

Kickoff & Data Cleanliness
- 15-minute strategy and handoff alignment call.
- Data normalization, duplicate removal, and verification.
- Opportunity prioritization (recent bids and high-value facility types worked first).

Outreach Execution
- Up to 20 qualified dormant commercial records worked.
- Manual, professional human telephone calls.
- Targeted, personalized follow-up emails.
- Strict compliance with business-hour calling rules and instant opt-out honoring.

Reporting & Asset Delivery
- Real-time notification for hot leads, revision requests, or scheduled calls.
- Final Outcome Dashboard (Excel / Google Sheets) with standardized disposition codes.
- Recorded loss reasons (e.g., price, incumbent retained, project cancelled).
- Identified rebid / renewal calendar for future pipeline outreach.
- 15-minute closeout review with actionable next steps.

NON-NEGOTIABLE RULES FOR THIS BUILD:

1. Use the copy I give you VERBATIM. Do not rewrite, shorten, "punch up," or add
   headlines, taglines, or microcopy of your own. If a layout needs a label I did
   not supply, write [NEEDS COPY] and tell me.

2. Never write any of these — they are compliance violations for this business:
   - guaranteed contracts, guaranteed revenue, guaranteed ROI, "results guaranteed"
   - "cold leads," "we find you new clients," "new customer acquisition"
   - AI voice agents, automated outreach, autodialer, robocall, "AI-powered"
   - "explode your pipeline," "7-figure," "10x," growth-hacking hype
   - artificial urgency: countdown timers, "only 2 spots left today," "ends tonight"
   - "pay only if you close," commission-based or performance-based pricing

3. Invent nothing. No testimonials, no client logos, no star ratings, no "trusted
   by 500+ companies," no fabricated statistics, no made-up case studies, no
   placeholder company names in a logo strip. This business has zero paid clients
   today and the page must be honest about that.

4. No stock photography of cleaners, offices, or handshakes. Use structural
   design — type, spacing, borders, badges, tables, and the JS mark — to carry
   credibility. Real screenshots and the founder's real photo only.

5. There is no online checkout. Payment is a PayPal invoice sent by the founder.
   Never build a cart, a card form, a pricing toggle, "instant access," or a
   payment trust-badge row.

Tone: direct, pragmatic, calm. This page is read by blue-collar commercial
cleaning owner-operators who distrust marketing agencies. Credible utility, not
startup polish.
```

---

## Prompt 3 — Pricing + Dispositions + Proof + FAQ

Attach `images/founder.jpg` with this prompt.

```text
Continue the Desktop — 1440 artboard.

=== PRICING ===

H2:
Simple, Transparent Pricing. No Long Contracts.

Two cards side by side.

CARD 1 — emphasized, accent border:
Founding Pilot Sprint
Price: $199 (Prepaid)
Availability: Limited to the first 3 cleaning operators.
Scope: Up to 20 qualified dormant commercial cleaning proposals.
Duration: 7 business days from intake approval.
Includes: Full 5-stage sprint, manual outreach, immediate handoffs, and final
disposition dashboard.
Button: Claim Founding Pilot ($199)

CARD 2 — neutral:
Standard Recovery Sprint
Price: $299 (Prepaid)
Availability: Standard rate after the first 3 pilot completions.
Scope: Up to 20 qualified dormant commercial cleaning proposals.
Duration: 7 business days from intake approval.
Includes: Complete sprint execution, verified reporting, and rebid calendar.
Button: Book an Intake Call

Beneath both cards, as a quiet footnote — NOT a highlighted callout:
Note: Expanded scope options and ongoing follow-up arrangements are under
development and not yet available. Contact Clay directly to discuss future needs.

"Limited to the first 3 cleaning operators" is a factual scope statement. Style it
as a plain badge. No countdown timer, no progress bar, no spots-remaining counter.

=== DISPOSITIONS ===

H2:
Silence Turned Into 12 Documented Dispositions.

Subhead:
Every proposal you hand us receives one of twelve clean outcomes:

A 12-item grid, 3 or 4 across. Each item shows the code as a tabular/monospace
badge, then the name, then the one-line definition:

RR  Review Requested — Prospect wants a phone call or meeting to revisit the bid.
RV  Revision Requested — Prospect wants scope, frequency, or pricing updated.
OP  Open Pending — Project is still active with a firm future decision date.
RB  Rebid Date — Competitor or incumbent won; renewal month identified for next year.
WI  Won Independently — Prospect already awarded the contract; records updated.
LI  Lost — Competitor / Incumbent — Prospect retained current cleaner or chose another vendor.
LP  Lost — Price — Prospect indicated budget or price was the deciding factor.
LT  Lost — Timing / Budget — Facility project postponed or budget unavailable.
NR  No Response — Full multi-touch sequence completed with no reply.
BD  Bad Data — Facility closed, contact left, or invalid contact details.
DNC Do Not Contact — Recipient requested no further contact (suppressed immediately).
X   Ineligible — Record did not meet commercial proposal standards.

Badge colors: emerald for RR, RV, OP, RB. Amber for NR. Slate for WI, LI, LP, LT,
BD, DNC, X.

=== PROOF ===

H2 (use exactly this):
Who Actually Makes the Calls

LEFT — founder block:
Clay, founder of JanSan Sweep. Background in B2B cold calling, appointment
setting, and sales pipeline organization. Every call on your account is dialed by
him personally.
Phone: 928-298-8405
Email: info@jansansweep.com
Flagstaff, AZ (Mountain Standard Time)
Use the attached photo, cropped square or 4:5 portrait.

RIGHT — two artifacts:
(a) The sample Outcome Dashboard: a table with columns Business | Facility |
Proposal Date | Attempts | Disposition | Notes | Next Step | Rebid Date. Show
eight to ten rows so the format is legible; use the rows I gave you in the hero
plus additional generic examples in the same style.

(b) The approved calling script, styled as a document card:
"Hi [Name], this is Clay with JanSan Sweep following up on behalf of [Your
Company] regarding the cleaning proposal for [Facility] sent back in [Month]...
Is that project still under consideration, did you select another provider, or
would a revised conversation be useful?"

Directly under the dashboard, place this label in a bordered note — visible
caption weight, NOT fine print:
Sample dashboard — illustrative format only. Business names, dates, and outcomes
shown are fictional examples created to demonstrate the report structure. They are
not client results. JanSan Sweep publishes real anonymized outcomes only after a
completed sprint and with written client permission.

BELOW BOTH — "The Qualified Record Standard":
Records must be commercial cleaning opportunities (offices, medical clinics,
industrial facilities, churches, schools, dealerships) where the prospect
previously requested a quote, invited you to a walkthrough, or received a
proposal. We do not accept residential cleaning leads, purchased cold lists, or
government opportunities under sealed-bid communication blackouts.

This section must make clear the business is new and pre-validation. No proof it
hasn't earned. Every figure in the dashboard is a fictional example — do not
summarize it into a headline statistic anywhere on the page.

=== FAQ ===

H2:
Frequently Asked Questions

Eight accordion items, collapsed by default except the first.

Q1. Why shouldn't I just have my office manager or myself do this?
You can, and if you have the hours to consistently call, email, track notes, and
categorize 20 older bids while managing cleaners, inspections, and payroll, you
should. JanSan Sweep exists for owners who recognize that while they can do it, it
consistently slips down their priority list.

Q2. Aren't proposals from 6 months ago completely dead?
Some are. Finding out they are dead is valuable—it clears false pipeline off your
plate. But in commercial cleaning, contracts frequently drag out: managers get
sidetracked, incumbents slip in quality after 90 days, or budgets unlock in a new
quarter. More importantly, when an incumbent was retained, we uncover the exact
month that contract comes up for bid again.

Q3. Do you guarantee signed cleaning contracts?
No. Anyone promising guaranteed signed commercial cleaning contracts is either
overpromising or misrepresenting what they do. We do not control your bid pricing,
your operational capacity, or the facility manager's budget. We guarantee
disciplined, high-caliber human execution, transparent communication, and complete
record reporting.

Q4. Why won't you work purely on commission?
Closing a commercial cleaning deal depends on your labor rates, square-foot
pricing, walkthrough credibility, references, and client negotiation—none of which
JanSan Sweep controls. We deliver dedicated labor, research, calling, and
reporting. You pay for the execution of a professional sprint, just as you pay an
estimator or inspector for their work.

Q5. How do you introduce yourself to my prospects?
We are completely transparent. We say: "Hi [Name], this is Clay with JanSan Sweep
following up on behalf of [Your Company] regarding the cleaning proposal for
[Facility] sent back in [Month]..." We never pretend to be your full-time internal
employee, nor do we misrepresent our role. Facility managers appreciate the honest,
professional follow-up.

Q6. What kind of records qualify for the sprint?
Records must be commercial cleaning opportunities (offices, medical clinics,
industrial facilities, churches, schools, dealerships) where the prospect
previously requested a quote, invited you to a walkthrough, or received a
proposal. We do not accept residential cleaning leads, purchased cold lists, or
government opportunities under sealed-bid communication blackouts.

Q7. What happens when a prospect says they want to talk?
We do not attempt to price jobs or negotiate terms. We immediately confirm the
best time and contact info, notify you via email/phone within minutes, and hand
the opportunity back to you with detailed conversation notes so you can close it.

Q8. Is this an automated AI dialer or robocalling service?
No. Every phone call is manually dialed by a human being. Every voicemail and
email is personalized. We do not use soundboard bots, ringless voicemails,
autodialers, or automated mass blasting.

NON-NEGOTIABLE RULES FOR THIS BUILD:

1. Use the copy I give you VERBATIM. Do not rewrite, shorten, "punch up," or add
   headlines, taglines, or microcopy of your own. If a layout needs a label I did
   not supply, write [NEEDS COPY] and tell me.

2. Never write any of these — they are compliance violations for this business:
   - guaranteed contracts, guaranteed revenue, guaranteed ROI, "results guaranteed"
   - "cold leads," "we find you new clients," "new customer acquisition"
   - AI voice agents, automated outreach, autodialer, robocall, "AI-powered"
   - "explode your pipeline," "7-figure," "10x," growth-hacking hype
   - artificial urgency: countdown timers, "only 2 spots left today," "ends tonight"
   - "pay only if you close," commission-based or performance-based pricing

3. Invent nothing. No testimonials, no client logos, no star ratings, no "trusted
   by 500+ companies," no fabricated statistics, no made-up case studies, no
   placeholder company names in a logo strip. This business has zero paid clients
   today and the page must be honest about that.

4. No stock photography of cleaners, offices, or handshakes. Use structural
   design — type, spacing, borders, badges, tables, and the JS mark — to carry
   credibility. Real screenshots and the founder's real photo only.

5. There is no online checkout. Payment is a PayPal invoice sent by the founder.
   Never build a cart, a card form, a pricing toggle, "instant access," or a
   payment trust-badge row.

Tone: direct, pragmatic, calm. This page is read by blue-collar commercial
cleaning owner-operators who distrust marketing agencies. Credible utility, not
startup polish.
```

**Note on the FAQ:** Q3 uses the word "guarantee" twice — deliberately, and in the compliant direction ("We guarantee disciplined, high-caliber human execution," not results). This is the one place the word is allowed. If Claude Design flags it against rule 2, tell it to keep the copy as written.

---

## Prompt 4 — Final CTA + Intake Form + Footer

```text
Finish the Desktop — 1440 artboard.

=== FINAL CTA === (full-width #0F172A navy band)

Headline:
Find Out What Happened to Your Last 20 Proposals.

Two paths side by side.

PATH A — "Book a 15-Minute Proposal Audit"
A form with these fields, in this order:
1. Business Name
2. Owner / Contact Name
3. Direct Phone
4. Email
5. Approximately how many commercial proposals have you sent in the last 3–12
   months? (select: 1–5 / 6–15 / 16–30 / 30+)
6. Do you currently have at least 10 unclosed proposals stored in email,
   spreadsheets, or bidding software? (Yes / No / Not Sure)
Submit button: Book My Bid Audit
A scheduling widget embeds here at build time — leave a clearly marked embed slot
labeled [CALENDLY EMBED].

PATH B — "Ready Now"
A compact card:
JanSan Sweep Founding Sprint — $199 prepaid
Up to 20 dormant commercial proposals, worked over 7 business days.
Button: Request My Founding Sprint
Under the button, in plain readable text:
Clay sends a PayPal invoice. Your seven-day sprint starts once it's paid and your
records are in.

There is no online checkout. Do not build a cart, a card form, a pricing toggle,
or a payment trust-badge row. This button opens the same request form as Path A
with the sprint pre-selected, or a short two-field version (name + email).

Use the light/knockout logo on this band, not the white-background JPEG.

=== FOOTER === (navy)

Logo, then:

Business description:
JanSan Sweep is an independent proposal follow-up and pipeline reactivation
service for commercial cleaning companies.

Compliance statement (reproduce in full, do not shorten):
All outreach is conducted manually via direct B2B communication on behalf of
authorized clients. JanSan Sweep does not use automated telephone dialing systems,
artificial or prerecorded voices, or unsolicited consumer outreach.

Legal links row (five links):
Privacy Policy | Terms of Service | Refund Policy | Client Outreach Agreement | Do-Not-Call Policy

Tracking statement, on its own line beneath the compliance statement:
This site sets no advertising or analytics cookies and uses no third-party trackers.

Contact line:
Clay · 928-298-8405 · info@jansansweep.com
PO Box 2524, Rimrock, AZ 86335 · Mountain Standard Time

Copyright:
© 2026 JanSan Sweep. All rights reserved.

The compliance statement must be legible body text, not 10px grey legalese. For
this business it is a selling point, not fine print.

NON-NEGOTIABLE RULES FOR THIS BUILD:

1. Use the copy I give you VERBATIM. Do not rewrite, shorten, "punch up," or add
   headlines, taglines, or microcopy of your own. If a layout needs a label I did
   not supply, write [NEEDS COPY] and tell me.

2. Never write any of these — they are compliance violations for this business:
   - guaranteed contracts, guaranteed revenue, guaranteed ROI, "results guaranteed"
   - "cold leads," "we find you new clients," "new customer acquisition"
   - AI voice agents, automated outreach, autodialer, robocall, "AI-powered"
   - "explode your pipeline," "7-figure," "10x," growth-hacking hype
   - artificial urgency: countdown timers, "only 2 spots left today," "ends tonight"
   - "pay only if you close," commission-based or performance-based pricing

3. Invent nothing. No testimonials, no client logos, no star ratings, no "trusted
   by 500+ companies," no fabricated statistics, no made-up case studies, no
   placeholder company names in a logo strip. This business has zero paid clients
   today and the page must be honest about that.

4. No stock photography of cleaners, offices, or handshakes. Use structural
   design — type, spacing, borders, badges, tables, and the JS mark — to carry
   credibility. Real screenshots and the founder's real photo only.

5. Any value I have not given you renders as a visible [PLACEHOLDER] token. Do not
   fabricate a phone number, URL, address, or email.

Tone: direct, pragmatic, calm. This page is read by blue-collar commercial
cleaning owner-operators who distrust marketing agencies. Credible utility, not
startup polish.
```

---

## Prompt 5 — Mobile Artboard

```text
Create the Mobile — 390 artboard: the same page, adapted. Do not change any copy.

Specific requirements:

- Nav collapses to logo plus a single visible "Book a Bid Audit" button. If you
  use a hamburger, the CTA stays outside it.
- The hero subheadline stays complete. Do not truncate it on mobile.
- The Is / Is Not comparison becomes stacked pairs, not a horizontally scrolling
  table — each row shows its "Is" and its "Is NOT" as a linked pair so the
  contrast survives.
- The five-step sprint becomes a vertical stepper.
- The three deliverables columns stack; keep the group headings.
- The 12 dispositions become a single-column list, code badge left, text right.
- The dashboard mock scrolls horizontally inside its own container. The page body
  must never scroll sideways.
- Pricing cards stack, Founding Pilot first.
- The FAQ stays as an accordion, all items collapsed by default.
- All tap targets at least 44px. Buttons full-width. Section rhythm drops to 56px.
- The footer compliance statement stays full length and legible.

NON-NEGOTIABLE RULES FOR THIS BUILD:

1. Use the copy I give you VERBATIM. Do not rewrite, shorten, "punch up," or add
   headlines, taglines, or microcopy of your own. If a layout needs a label I did
   not supply, write [NEEDS COPY] and tell me.

2. Never write any of these — they are compliance violations for this business:
   - guaranteed contracts, guaranteed revenue, guaranteed ROI, "results guaranteed"
   - "cold leads," "we find you new clients," "new customer acquisition"
   - AI voice agents, automated outreach, autodialer, robocall, "AI-powered"
   - "explode your pipeline," "7-figure," "10x," growth-hacking hype
   - artificial urgency: countdown timers, "only 2 spots left today," "ends tonight"
   - "pay only if you close," commission-based or performance-based pricing

3. Invent nothing. No testimonials, no client logos, no star ratings, no
   fabricated statistics, no made-up case studies.

4. No stock photography.

5. There is no online checkout. Payment is a PayPal invoice sent by the founder.

Tone: direct, pragmatic, calm. Credible utility, not startup polish.
```

---

## Prompt 6 — QA Sweep + Export

```text
Final pass. Audit both artboards and report your findings BEFORE changing
anything:

1. COPY DIFF — list every string on the page that does not appear verbatim in the
   copy I supplied across our earlier prompts. I expect that list to be empty
   except for [PLACEHOLDER], [NEEDS COPY], and [CALENDLY EMBED] tokens.

2. PROHIBITED LANGUAGE SCAN — check every string against the banned list in my
   rules and report any hit. Note: the FAQ answer about guarantees intentionally
   contains the phrase "We guarantee disciplined, high-caliber human execution."
   That one is approved and stays.

3. INVENTED CONTENT SCAN — flag any testimonial, client logo, statistic, rating,
   or company name I did not supply. Confirm the sample-dashboard label is present
   and legible next to every dashboard on the page.

4. CHECKOUT SCAN — confirm there is no cart, card form, pricing toggle, "instant
   access" language, or payment trust-badge row anywhere.

5. CONTRAST — verify all text meets WCAG AA against its background, especially
   slate-on-white body text and anything on the navy bands.

6. PLACEHOLDERS — list every remaining placeholder token so I know exactly what I
   still owe before launch.

Then fix only what the audit flagged.

Afterward, export the design as static HTML/CSS: semantic markup, a system-font
fallback stack for Inter, no JavaScript frameworks, no analytics or tracking
libraries, images optimized. Target a sub-second load on a static host.
```

---

## After All Six Passes

Return to `11-CLAUDE-DESIGN-BUILD-PLAN.md` §6 (reject-and-re-prompt checklist) and §7 (pre-launch sequence: copy compliance re-check, Calendly link, transparent logo and favicon, legal pages, decision log entry).
