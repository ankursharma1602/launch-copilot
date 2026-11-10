MOCK HANDOFF for a portfolio demo. Not Clio internal data.

# Closed beta handoff: Clio Timekeeping

> HYPOTHETICAL. A mock handoff written to demo Launch CoPilot. The product description follows Clio's public help article and ClioCon 2026 coverage (sources in `context/proof-points.md`). The beta accounts, numbers, quotes, tickets and Slack messages below are invented and labelled "illustrative". No real firm or person is named.

**From:** Product manager, Timekeeping (role, no name)
**To:** Product marketing
**Status:** Beta complete. Going to general availability (mock)
**General availability date (launch day, L-0):** Tuesday, February 2, 2027 (illustrative)

**The ask to product marketing:** plan and run the GA launch, from the end of beta to launch day and the 90 days after. Customer-facing assets announce general availability. They do not market the beta.

## 1. Epic summary

**Epic (mock key TIME-100): Clio Timekeeping**

Clio Timekeeping is an AI-powered feature that captures billable activity and drafts time entries for the lawyer to review. The lawyer checks each entry, edits it if needed and marks it bill-ready.

**Problem.** Lawyers do the work first and write the time down later, if at all. Work in email, documents and calls is easy to forget by the end of the week. Time that never gets recorded never reaches a bill.

**Who it's for.**
- Primary: solo and small-firm lawyers who record their own time.
- Secondary: managing partners who care about utilization, realization and profitability, and billing or office admins who prepare bills.

**User stories.**

| Story | As a... | I want to... | So that... | Status |
|---|---|---|---|---|
| TIME-101 Set up | Lawyer | connect Outlook and OneDrive in Clio Manage and turn on computer activity capture in the Clio Desktop App | Timekeeping can start capturing | Done, in beta |
| TIME-102 Capture | Lawyer | have billable activity captured as I work, including calls made in the Clio mobile app | I do not rely on memory | Done, in beta |
| TIME-103 Matter match | Lawyer | get a suggested matter for work outside the web app, such as email, based on names, email addresses and other available information | entries land on the right matter | Done, in beta |
| TIME-104 Review | Lawyer | open My time entries, see the captured activity behind each entry, edit it and switch on Bill-ready | I stay in control of what is billed | Done, in beta |
| TIME-105 Flat-fee view | Managing partner | see captured time on flat-fee matters, which does not appear on the invoice | I can tell whether the work was profitable | Done, in beta |

**Availability.**
- Today: opt-in beta (public, per ClioCon 2026 coverage). At GA: available to every Clio Manage customer (illustrative).
- Setup is required before Timekeeping creates entries.
- Plans at GA: included on all Clio Manage plans at no extra cost (illustrative assumption for this demo).
- Regions at GA: United States and Canada, English (illustrative).
- Launch date: Tuesday, February 2, 2027 (illustrative).

**GA success metrics (targets illustrative).**
- Adoption: 15% of active Clio Manage firms complete setup within 60 days of GA
- Engagement: 70% of drafted entries are marked Bill-ready within 7 days
- Value: billable time recorded per active user up 10% versus the 30 days before setup
- Retention signal: 80% of firms that complete setup still have drafted entries reviewed in week 8

**Competitive notes.**
- Customers today write time by hand, use a timer, or rebuild time from email and calendar at month end.
- Named competitors: [NEED PROOF: no public source in hand]

## 2. Release notes (engineering, beta build)

**Clio Timekeeping, beta build (mock build notes)**

Added
- Setup: connect Outlook and OneDrive in Clio Manage. Computer activity is captured through the Clio Desktop App.
- Mobile calls: calls made in the Clio mobile app can be logged automatically.
- Matter suggestion for work outside the web app, based on names, email addresses and other available information.
- Drafted time entries appear about 15 minutes after the activity.
- Review in Clio Manage under Activities > "My time entries", or "View entries" from the Clio Desktop App. Edit with the pencil icon. Switch on "Bill-ready" to add the entry to the matter's unpaid bills.
- Selecting an entry shows the captured activity behind it in the right-hand panel.

Known limitations
- Nothing is created until setup is finished.
- Users can only see and review their own entries.
- Matter suggestions can be wrong, so entries need review. (illustrative wording, confirm with Product)

GA build (illustrative)
- Same capabilities as beta, plus a guided setup checklist in Clio Manage so firms know nothing is created until setup is finished.

## 3. Notes from the demo

Internal demo to Product, Sales Engineering and Support (mock notes, roles only).

- Demo opened with a lawyer who had spent the morning in email and documents and had logged nothing. After setup, draft entries appeared in My time entries.
- The moment the room reacted: selecting an entry and seeing the captured activity behind it in the right-hand panel.
- The presenter changed one entry with the pencil icon, switched on Bill-ready, and showed it land in the matter's unpaid bills.
- The presenter showed a flat-fee matter: captured time did not appear on the invoice but showed whether the work was profitable.
- Questions from the room: what data is captured from the desktop, who else can see entries, and how often the matter suggestion is wrong. None was answered in the demo. See open questions below.
- Support asked for plain wording on "entries usually appear about 15 minutes after the activity" before wider release.

## 4. Closed beta stats

> ILLUSTRATIVE. Mock numbers for the demo. Small group, internal, not for external use.

| Measure | Value |
|---|---|
| Beta period | 6 weeks (illustrative) |
| Firms invited | 20 (illustrative) |
| Firms that completed setup | 14 (illustrative) |
| Firms with at least one drafted entry reviewed | 12 of 14 (illustrative) |
| Drafted entries created | 1,100 (illustrative) |
| Entries edited before Bill-ready | 410 of 1,100 (illustrative) |
| Entries marked Bill-ready | 780 of 1,100 (illustrative) |
| Firms that opened the activity panel behind an entry | 11 of 14 (illustrative) |
| Firms using flat-fee or hybrid matters | 6 of 14 (illustrative) |
| Firm sizes in the beta | Solo, small, mid-size (illustrative) |

## 5. Closed beta customer feedback

> ILLUSTRATIVE. These quotes are invented for the demo. They are not from real customers. Roles only, no names.

**Solo lawyer (illustrative)**
"I used to rebuild my week on Friday afternoon from my sent folder. Now I open the list and check it."
"I like that I can see what it based the entry on before I switch on Bill-ready."

**Managing partner, small firm (illustrative)**
"For flat-fee matters I never knew if we made money. Seeing the captured time helped."
"I want to know exactly what it captures from the desktop before I roll it out to the firm."

**Associate, mid-size firm (illustrative)**
"Most drafts were right. A few landed on the wrong matter and I fixed them with the pencil."
"I only see my own entries, which my partner asked about."

**Billing coordinator, small firm (illustrative)**
"If lawyers mark entries Bill-ready earlier, my bill run is easier. I cannot see their entries myself though."

**Other feedback themes (illustrative, summarized by Product)**
- Three beta firms asked how to tell which entries came from which application.
- Two firms did not realise setup was needed before anything was created.
- Two firms asked whether admins can review entries for other people.
- Before the beta, firms said they wrote time by hand, used timers, or reconstructed time later.

## 6. Open questions from the Slack thread

Pasted from the #timekeeping-wider-release thread (mock, roles only).

- **Product manager, Timekeeping:** Pricing and packaging confirmed: included on all Clio Manage plans at GA, no extra cost (illustrative). GA is February 2 (illustrative).
- **Support lead:** The help article says entries usually appear about 15 minutes after activity. Do we say "about 15 minutes" in marketing, or avoid a number?
- **Sales Engineering:** What exactly is captured from the computer through the Clio Desktop App? We have no privacy or data-handling wording.
- **Legal:** Please check any wording about data capture, privacy and "AI" before it goes public.
- **Engineering lead:** How the matter suggestion is ranked is not documented.
- **Customer success:** Whether admins or billers can see other users' entries is not settled. The help article says users see only their own.
- **Product manager, Timekeeping:** GA covers the US and Canada, in English (illustrative). Other regions follow later.
- **Sales Engineering:** Can we compare to other time capture tools? We have no public source naming one.
- **Revenue operations:** We cannot yet track opt-ins by firm size in the CRM.
- **Product marketing:** Can we use any beta numbers or quotes externally? Firms have not agreed to that.
