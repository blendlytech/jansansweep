**Document:** Website Legal Pages (Attorney-Review Drafts)
**Version:** 1.0
**Updated:** September 3, 2026
**Status:** Draft — not cleared for publication
**Authority:** `00-START-HERE.md` — governed by `06-COMPLIANCE-AND-DATA.md`

---

# JanSan Sweep — Website Legal Pages

## Status and Limitations — Read First

These are **drafts written to give an attorney something concrete to mark up.** They are not legal advice and have not been reviewed by counsel. `06-COMPLIANCE-AND-DATA.md` already requires attorney review of the service agreement and outreach model, and these four pages sit directly on top of that requirement.

Two of them carry real risk if published unreviewed:

- **Terms of Service** and the **Client Outreach Agreement** create binding obligations, allocate liability, and are the documents that matter if a prospect complains about a call made on a client's behalf.
- **Privacy Policy** and the **Do-Not-Call Policy** are lower risk but still make factual representations about your practices. They are accurate only as long as your practices match them — if you later add call recording, texting, or any automated tooling, both go stale immediately.

Recommended sequence: publish the site with these four pages live in draft form only if you must launch before counsel is engaged, and get them reviewed before accepting the first client's data. Do not accept client records under an unreviewed Client Outreach Agreement.

### Identifying details used throughout

| Field | Value |
|---|---|
| Business | **R. Clay Mills**, a sole proprietor doing business as **JanSan Sweep** |
| Mailing address | **PO Box 2524, Rimrock, AZ 86335** |
| Phone | **928-298-8405** |
| Email | **info@jansansweep.com** |
| Established | May 2, 2025 |
| Governing law | Arizona; venue Coconino County |

If an LLC is formed later, the entity name in all four pages changes and the sole-proprietor phrasing comes out. Tell counsel which structure is in place at review time.

### Every identifying detail is now filled in

All four pages carry **Effective September 4, 2026**. One caveat that matters: that date is a promise about when these terms took effect, so it is only true if the pages are actually live on jansansweep.com that day. If the launch slips, move the date forward to the real publication date rather than leaving a date the site cannot support.

Resolved on 2026-09-03 and logged in `09-ROADMAP-AND-DECISIONS.md`:

- Public location is **Flagstaff, AZ**; published mailing address is **PO Box 2524, Rimrock, AZ 86335**, not the home address. The box is also the postal address required in outreach email footers — see the section below.
- Venue is **Coconino County**, confirmed by Clay. It follows where the business operates rather than where the mailbox sits, so the Rimrock box in Yavapai County does not change it. Counsel should still confirm this at review, since two Arizona counties appear across the documents.

A note on the two cities: it is ordinary for a business to operate in one town and keep a mailbox in another, and nothing here misrepresents anything. But the footer will read "Flagstaff, AZ" next to a Rimrock mailing address, so expect an occasional question about it, and make sure the answer is simply that the mailbox is in Rimrock.

---

## What the Footer Is Actually Required to Carry

I am not a lawyer and this is not legal advice. The four links were carried forward from `07-MARKETING-AND-WEBSITE.md` rather than derived from any legal requirement, so here is the honest breakdown for counsel to confirm.

### Of the four, only one is required in practice

| Page | Status | Reasoning |
|---|---|---|
| **Privacy Policy** | Effectively required | California's online privacy law requires any commercial website that collects personally identifiable information from California residents to post a conspicuous privacy policy. The audit request form collects name, phone, and email, which triggers it regardless of where the business sits. Several other states have similar rules with revenue or volume thresholds this business is far below. |
| **Terms of Service** | Not required, strongly advised | No statute compels it. It is what limits liability, sets the refund terms, and defines the no-guarantee promise. For a prepaid service sold to strangers over the phone, publishing it is worth far more than it costs. |
| **Client Outreach Agreement** | Not required | Published by choice. For a business whose whole pitch is "we tell your prospects exactly who we are," showing the authorization publicly is a credibility asset, not a legal obligation. |
| **Do-Not-Call Policy** | Not required to be published | Telemarketing rules require maintaining an internal do-not-call list and a written policy available on demand; they do not require posting it on a website. B2B calls sit largely outside the national registry rules. Publishing it anyway is the same credibility play. |

### Three things worth adding

1. **Refund and cancellation terms, linked directly.** Not a separate legal requirement — the terms already live in Terms of Service §7. But this is a prepaid service invoiced through PayPal, and in a PayPal dispute the published, pre-purchase refund policy is the strongest thing to point at. Add a fifth footer link, `Refund Policy`, that jumps to the Terms anchor rather than creating a new page.

2. **An affirmative no-tracking line.** No cookie banner is needed *because* the build spec forbids analytics and tracking libraries. Say so instead of staying silent — it costs one line and reinforces the brand promise:

   > This site sets no advertising or analytics cookies and uses no third-party trackers.

   **That line has a trigger.** It stops being true the moment anything is added that sets cookies — Google Analytics, a Meta pixel, a chat widget, or an embedded scheduler. A Calendly or Cal.com embed is the likely culprit here, since embedded schedulers commonly set third-party cookies. Before shipping Path A's embed, check what it sets; if it sets cookies, either use a link-out button to the booking page instead of an inline embed, or drop this line and add a short cookie notice.

3. **The postal address, which does double duty.** The PO box belongs in the footer, and it is also the postal address that federal commercial-email rules require in the outreach emails sent during a sprint. Those emails must also carry accurate header information, a non-deceptive subject line, and a working opt-out that is honored promptly — all of which `06-COMPLIANCE-AND-DATA.md` already requires operationally. Make sure the email templates in `05-DELIVERY-SOP.md` carry PO Box 2524 and an opt-out line before the first sprint.

### Two things deliberately not added

- **An accessibility statement.** No US statute requires one for a private business website. Web accessibility litigation under the ADA is real, but the protection comes from the site actually meeting WCAG AA — which the Prompt 6 audit checks — not from a statement claiming it does.
- **A cookie consent banner.** Unnecessary without cookies, and adding one to a site that sets none would be theater. Revisit only if item 2's trigger fires.

### One business-formation note

Arizona does not require registering a trade name, so operating as "R. Clay Mills d/b/a JanSan Sweep" is lawful without it. Registering the name with the Secretary of State is inexpensive and usually makes it easier to open a business bank account and a PayPal business account under "JanSan Sweep" rather than a personal name — which matters here, because clients will be paying an invoice and the name on it should match the name on the website.

---

# Page 1 — Privacy Policy

**Effective September 4, 2026**

JanSan Sweep ("we," "us") is a proposal follow-up service operated by R. Clay Mills, a sole proprietor doing business as JanSan Sweep, in Arizona. This policy explains what information we collect through jansansweep.com and in the course of delivering a Recovery Sprint, and how we handle it.

## Information We Collect

**From website visitors.** If you submit the audit request form, we collect the business name, contact name, direct phone, email address, and the answers you give about your proposal volume. We collect this only when you submit it. We do not require an account.

**From clients.** To deliver a sprint, a client sends us a list of up to 20 of their own prior commercial cleaning proposals. Those records typically contain the prospect's business name, a contact name and role, a business phone number and email address, the facility, the proposal date and scope, and the client's last-known status notes.

**Automatically.** Our host records standard server logs, including IP address and pages requested, for security and availability. We do not run advertising trackers, behavioral analytics, or third-party marketing pixels on this site.

## What We Do Not Collect

We do not accept, and clients must not send us, consumer contact lists, payment card numbers, bank account details, Social Security numbers, medical information, or employee records. If such data reaches us, we delete it and notify the client.

## How We Use Information

Website form submissions are used to contact you about a bid audit or a sprint, and for nothing else. Client-supplied records are used solely to perform the follow-up work that client has authorized, and to produce that client's outcome report.

We do not sell, rent, trade, or share client records or prospect contact information with anyone. We do not use one client's records to benefit another client, and we do not retain prospect data as a marketing list of our own.

## Business-Contact Data

The people we call and email during a sprint are business contacts at companies that previously engaged with our client. We contact them on that client's behalf and identify ourselves and the client on every contact. If you are one of those contacts and want to know why you were contacted, or want your information removed, see the Do-Not-Call Policy or write to info@jansansweep.com.

## Service Providers

We use ordinary business tools — email, telephone service, spreadsheet and file storage, calendar scheduling, and PayPal for invoicing — that necessarily process some of this information. We limit what each tool receives to what it needs. Payments are handled by PayPal; we do not receive or store your full payment card or bank details.

## AI Tools

We do not upload client proposal files or identifiable campaign lists to third-party AI services. We use general-purpose AI tools only for internal templates, process design, and non-identifiable work. If that ever changes, we will disclose it and obtain written client authorization first.

## Security

Client data is kept in one access-controlled folder per client, with public link sharing disabled and two-factor authentication enabled on the accounts that hold it. Access is limited to Clay and to users the client authorizes. Client campaign data is kept separate from our own prospecting records. No system is perfectly secure, and we do not claim otherwise.

## Retention and Deletion

We keep working records for the duration of a sprint, deliver the final report, and confirm client receipt. We then delete or return working copies within 30 days unless the client renews the engagement or the law requires longer retention.

One exception: we permanently retain the minimum information needed to honor a do-not-contact request — typically a name, business, phone number, and email — so that we do not contact that person again. Deleting a suppression record would defeat its purpose.

## Your Choices

You may ask us what information we hold about you, ask us to correct it, or ask us to delete it, subject to the suppression-list exception above and to any records we must keep by law. Write to info@jansansweep.com or call 928-298-8405.

## Children

This is a business-to-business service. The site is not directed to anyone under 18 and we do not knowingly collect information from children.

## Changes

If we change this policy we will update the effective date above. Material changes affecting existing clients will be communicated directly.

## Contact

R. Clay Mills, d/b/a JanSan Sweep · PO Box 2524, Rimrock, AZ 86335
info@jansansweep.com · 928-298-8405

---

# Page 2 — Terms of Service

**Effective September 4, 2026**

These terms govern your use of jansansweep.com and, where a separate signed agreement does not control, the purchase of a JanSan Sweep Recovery Sprint from R. Clay Mills, a sole proprietor doing business as JanSan Sweep ("JanSan Sweep," "we," "us").

## 1. What We Sell

The JanSan Sweep Recovery Sprint is a fixed-scope, prepaid service: manual follow-up on up to 20 qualified dormant commercial cleaning proposals that you previously submitted, delivered over seven business days from complete intake and approval, ending in a record-level outcome dashboard and a closeout call.

The founding price is $199 prepaid, limited to the first three clients. The standard price thereafter is $299 prepaid.

## 2. What Is Not Included

The sprint does not include cold lead generation, purchasing contact lists, consumer outreach, automated dialing or prerecorded calls, rewriting or repricing your proposals, negotiating binding terms on your behalf, more than 20 records, continued outreach after the sprint ends, or contact with restricted government procurement officials.

## 3. No Guarantee of Results

**We do not guarantee replies, conversations, meetings, revision requests, contract awards, revenue, or return on investment.** We cannot: the outcome of a commercial cleaning bid depends on your pricing, your capacity, your references, and the prospect's budget and decision process, none of which we control.

What we do commit to is defined and measurable: disciplined manual execution of the approved outreach sequence, immediate handoff of live interest, truthful representation of ourselves and of you, and a complete, honest record-level report covering every record you submit — including the ones that produced nothing.

You agree that no statement on our website, in a call, or in an email creates any guarantee of a commercial result.

## 4. Your Responsibilities

You represent and warrant that every record you submit concerns a commercial cleaning opportunity; that the prospect previously requested a quote, participated in a walkthrough, or received a proposal from you; that you have a legitimate business basis for follow-up; that the record is not subject to a procurement communication blackout; and that you authorize us to contact that business on your behalf.

You are responsible for the accuracy of the records you provide, for approving the contact wording and cadence before any outreach begins, and for responding promptly when we hand off a live opportunity.

You must not submit purchased lists, consumer or residential contacts, or records for which you cannot substantiate prior engagement.

## 5. Our Authority Is Limited

We act as your authorized representative for follow-up communication only. We have no authority to bind you, to quote or change pricing, to modify scope, to accept or negotiate terms, or to make commitments on your behalf. We identify ourselves truthfully on every contact as JanSan Sweep following up on your behalf, and we never represent ourselves as your employee.

## 6. Payment

Sprints are prepaid. We invoice through PayPal. Work begins after payment is received and intake is complete and approved.

## 7. Cancellation and Refunds

*(The "Refund Policy" link in the site footer anchors to this section.)*

- Full refund if you cancel before intake work begins, less any unavoidable processing fees that were disclosed to you.
- No change-of-mind refund after data work has begun.
- Full refund if we decline your campaign because the records are ineligible.
- If fewer than 10 eligible records remain after validation, you may substitute records, accept a reduced-scope audit, or take a refund — provided outreach has not yet begun.
- No refund is available solely because prospects did not reply or did not award work. That outcome is a documented result, not a failure to deliver.

## 8. Confidentiality

We treat your records, pricing, and proposal information as confidential and use them only to perform your sprint. We handle, secure, retain, and delete that data as described in our Privacy Policy.

## 9. Compliance

All outreach is conducted manually by a human, during business hours, using accurate caller identification, with truthful disclosure of who we are and whom we represent. We do not use automated telephone dialing systems, artificial or prerecorded voices, ringless voicemail, cold text messaging, or unsolicited consumer outreach. Do-not-contact requests are honored immediately and permanently. See our Do-Not-Call Policy.

## 10. Termination

Either party may terminate a sprint in writing. If you terminate after outreach begins, you receive the records and outcomes completed to that point, and Section 7 governs any refund. We may terminate and refund in full if we determine that records are ineligible, that the requested outreach would be unlawful or misleading, or that you have asked us to misrepresent our role.

## 11. Limitation of Liability

To the maximum extent permitted by law, our total liability arising out of or relating to a sprint is limited to the amount you paid for that sprint. We are not liable for indirect, incidental, consequential, special, or punitive damages, or for lost profits or lost business opportunity.

## 12. Indemnity

You agree to indemnify and hold us harmless from claims arising out of records you submitted that did not meet the eligibility representations in Section 4, or from outreach you directed us to make that you were not authorized to direct.

## 13. Independent Contractor

We are an independent contractor. Nothing in these terms creates an employment, partnership, joint venture, or agency relationship beyond the limited communication authority described in Section 5.

## 14. Governing Law

These terms are governed by the laws of the State of Arizona, without regard to conflict-of-law rules. Venue for any dispute lies in Coconino County, Arizona.

## 15. Changes

We may update these terms. The version in effect when you purchase a sprint governs that sprint.

## Contact

R. Clay Mills, d/b/a JanSan Sweep · PO Box 2524, Rimrock, AZ 86335
info@jansansweep.com · 928-298-8405

---

# Page 3 — Client Outreach Agreement

**Effective September 4, 2026**

This is the authorization a client gives JanSan Sweep before any contact is made on their behalf. It is published here so that prospects who receive our calls, and clients evaluating the service, can read exactly what we are and are not permitted to do.

Clients sign this — or an equivalent counsel-reviewed agreement — before submitting records.

## 1. Authorization Granted

The Client authorizes R. Clay Mills, doing business as JanSan Sweep, to contact, by manually dialed telephone call and personalized email, the specific business contacts identified in the record list the Client submits and approves, for the sole purpose of following up on commercial cleaning proposals the Client previously submitted to those businesses.

This authorization covers only the approved records, only for the duration of the sprint, and only using contact wording and cadence the Client has approved in writing.

## 2. Client Representations

The Client represents that, for every submitted record:

1. The opportunity is commercial, not residential or consumer.
2. The prospect previously requested a quote, participated in a walkthrough, or received a proposal from the Client.
3. The Client has a legitimate business basis for follow-up and can substantiate the prior engagement if asked.
4. The record is not subject to a government procurement communication blackout, and the contact is not a restricted procurement official.
5. The contact information was obtained by the Client in the ordinary course of its own business and was not purchased as a cold list.
6. The Client has not received a do-not-contact request from that person.

## 3. Identity Disclosure

JanSan Sweep will identify itself truthfully on every contact, substantially as follows:

> "Hi, this is Clay with JanSan Sweep, following up on behalf of [Client Company] regarding the cleaning proposal for [facility] sent around [date]."

JanSan Sweep will not represent itself as an employee of the Client, will not conceal the Client's identity, and will not claim a prior relationship that the record does not support.

## 4. Scope of Authority

JanSan Sweep is authorized to: ask whether the opportunity is still active, identify the correct decision-maker, record the reason a bid was lost, identify a future rebid or renewal date, request a review conversation, note a requested revision, and hand the opportunity back to the Client.

JanSan Sweep is **not** authorized to: quote or change prices, modify scope, accept or negotiate contract terms, make commitments of any kind on the Client's behalf, or bind the Client in any way.

## 5. Prohibited Outreach

JanSan Sweep will not, under any instruction: use an autodialer, artificial or prerecorded voice, or ringless voicemail; send cold text messages to mobile numbers; contact consumers or residences; call outside ordinary business hours in the recipient's local time; use inaccurate caller identification; record calls without first reviewing applicable consent law; or make any statement misrepresenting results, affiliation, pricing, or urgency.

If the Client requests any of the above, JanSan Sweep will decline and may terminate the engagement.

## 6. Opt-Outs

Any recipient request to stop contact is honored immediately and permanently, is added to both the campaign suppression list and JanSan Sweep's own suppression list, and is reported to the Client in the final dashboard as a DNC record. The Client agrees to honor those requests in its own subsequent outreach.

## 7. Data Handling

Records are stored in a single access-controlled folder for that Client, with two-factor authentication enabled and public sharing disabled. Working copies are deleted or returned within 30 days of the Client confirming receipt of the final report, except for the minimum suppression data described in Section 6. No Client data is shared with any other client or third party.

## 8. No Guarantee

This authorization creates no promise of replies, meetings, revisions, awards, revenue, or ROI. It authorizes defined communication work and nothing more.

## 9. Termination

Either party may withdraw this authorization in writing at any time. Upon withdrawal, JanSan Sweep ceases all outreach immediately and delivers the outcomes recorded to that point.

## Contact

Questions about outreach conducted under this agreement — from clients or from contacted businesses — go to info@jansansweep.com or 928-298-8405.

---

# Page 4 — Do-Not-Call Policy

**Effective September 4, 2026**

## How to Stop Contact From Us

Tell us, and we stop. Immediately and permanently.

- **Phone:** 928-298-8405
- **Email:** info@jansansweep.com
- Or simply say so to Clay on the call. No explanation is needed and no reason will be requested.

Your request is recorded the same day, and you will not be contacted again by JanSan Sweep on behalf of that client or any other.

## Why You May Have Heard From Us

JanSan Sweep makes follow-up calls on behalf of commercial cleaning companies, to businesses that previously requested a quote, hosted a walkthrough, or received a written proposal from that company. Every call names the cleaning company we are calling for and the proposal we are calling about.

We do not use purchased lists. If you believe you were contacted without any prior dealing with the named company, tell us — we will remove you and investigate the record with our client.

## How We Operate

- Every call is dialed manually by a person. There is no autodialer, no artificial or prerecorded voice, and no ringless voicemail.
- Every email is written for the specific recipient. There is no mass blasting.
- We do not send cold text messages.
- We call during ordinary business hours in your local time.
- We use accurate caller identification.
- We call business numbers, not consumers or residences.

## Our Suppression Lists

We maintain two lists: one for each client campaign, and a permanent internal list for JanSan Sweep as a whole. A request to stop goes on both. We keep the minimum information necessary — typically your name, business, phone number, and email — for the sole purpose of ensuring you are never contacted again. Deleting that entry would remove the protection, so it stays.

Do-not-contact requests are reported to the client whose proposal we were following up on, so the client can honor them in its own outreach as well.

## Registry Compliance

Our outreach is business-to-business follow-up on prior engagements. We also honor any request from a recipient regardless of whether the number appears on any federal or state registry. Registry status does not have to be established for us to stop.

## Complaints

If you believe you were contacted in a way that does not match this policy, contact us directly at info@jansansweep.com or 928-298-8405. Complaints are reviewed by Clay personally.

R. Clay Mills, d/b/a JanSan Sweep · PO Box 2524, Rimrock, AZ 86335
