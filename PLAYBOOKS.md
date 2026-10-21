# Segment playbooks v1 (for calls, emails, WhatsApp)

Purpose: before approaching a company, know how its business works, where it loses money or time, and what specific thing we can build. These are working hypotheses from general industry knowledge. The first 5 calls per segment should confirm or correct them. Update this file after each call.

How to use: pick the segment, read "How they make money" and "Where it breaks", choose ONE pain point that fits the evidence found on the company, and open with that. Never list everything.

---
## 1. Event, exhibition and wedding companies

**How they make money:** fixed project fee or per-event contract, with margin made by controlling vendor, crew and logistics cost. Many events run at once in peak season (Oct to Mar in India, wedding season, exhibitions). Most crew are freelancers or daily-wage.

**Where it breaks**
- Crew and freelancer attendance is on WhatsApp groups and paper sheets. Payout disputes follow ("I worked 3 days, you paid 2").
- The manager does not know who actually reached the venue, who is late, who left early.
- Cost overruns: overtime, extra crew, transport and food are found after the event, not during it.
- Many vendors and many deliveries (stage, AV, lights, catering, decor). Last-minute changes live in chats.
- Client approvals and changes spread across calls and WhatsApp, then disputed at billing.
- Post-event: payouts to 50 to 300 people done by hand in Excel.

**What we can build (specific)**
1. Crew check-in app (PWA): crew mark arrival with photo and location at the venue, supervisor approves, event-wise attendance auto-builds.
2. Roster and shift allocation: who is on which event and role, confirmation by WhatsApp.
3. Payout sheet: attendance x rate + overtime = payable per person, exported for bank transfer.
4. Event cost tracker: planned vs actual cost per event, updated from phone.
5. Vendor and deliverables checklist per event with status and photos.
6. Client change log: every change request with date and approval, so billing is not argued.

**Signals to look for in research:** many events per year, "we are hiring" posts for event executives or crew, large team photos at events, exhibitions or concerts with many stalls, multi-city work.

**Discovery questions (calls)**
- How many events are running in a busy week, and how many crew per event?
- How do you know on the day who actually showed up?
- How long does it take to settle payouts after an event? Any disputes?
- Do you find out an event went over budget during it or after it?

**Do not say:** "AI", "digital transformation", "website". Talk about attendance, payouts, budget, disputes.

---
## 2. Manufacturing (auto components, electrical, plastics, packaging, garments)

**How they make money:** volume orders from OEMs or dealers, margin depends on machine uptime, scrap, on-time dispatch and receivables. Customers (large OEMs) audit them on quality and delivery.

**Where it breaks**
- Paper job cards and production logs; data typed into Excel at day end. Owner sees yesterday's numbers tomorrow.
- Machine breakdowns reported by shouting or WhatsApp; no record of downtime reasons or repeat faults.
- Maintenance is reactive. No schedule for preventive checks, no history per machine.
- Quality: rejection and rework recorded late, so the root cause is gone.
- Stores and raw material: stock in registers; shortages stop the line.
- Dispatch and invoicing mismatches; payment follow-up for dealers done from memory.
- Attendance and overtime for contract labour (many are through contractors).

**What we can build (specific)**
1. Shift production entry on a phone or tablet: quantity, rejection, downtime reason per machine. Live dashboard for the owner.
2. Breakdown ticket: operator raises it, maintenance gets a WhatsApp alert, time to fix is logged, repeat faults flagged.
3. Preventive maintenance calendar with reminders per machine.
4. Inward and outward gate and stores register (replace paper).
5. Dealer follow-up: outstanding invoices, promised payment dates, reminder to the dealer on WhatsApp.
6. Contract labour attendance and overtime summary for payroll.

**Signals to look for:** ISO or IATF certificates (they need records), "supplier to [OEM]", multiple plants, job posts for maintenance or production planning, tender or vendor-registration pages.

**Discovery questions**
- How do you know today's output before the shift ends?
- What does a machine breakdown cost you per hour, and how do you track the reasons?
- What is your rejection rate, and how quickly do you see it?
- Who chases dealer payments and how?

**Do not say:** "ERP replacement". They have often been burned by large ERP projects. Say "one small tool for one problem, live in 2 weeks".

---
## 3. Facility management, security and housekeeping agencies

**Money:** monthly contract per site; margin made on staffing efficiency and penalties avoided.
**Breaks:** guard and housekeeper attendance across many sites, shift gaps, client complaints with no proof, wage and overtime calculation, uniform and consumable stock per site.
**Build:** guard check-in with photo and location, site patrol checkpoints (QR), incident log with photos, shift-gap alert, monthly attendance and wage summary per site, client-facing report.
**Signals:** many sites listed, "manpower" or "guarding" in services, hiring for supervisors.
**Questions:** how do you know a post is empty right now? How do clients see proof of service?

## 4. Staffing and manpower agencies

**Money:** margin per placed worker per month.
**Breaks:** attendance from client sites, timesheet disputes, payroll and compliance (PF/ESI) data, candidate follow-up.
**Build:** worker attendance with client approval, timesheet to payroll export, candidate pipeline with WhatsApp reminders.
**Signals:** "bulk hiring", "contract staffing", many client logos.
**Questions:** how do you collect timesheets, and how long before you can invoice?

## 5. Logistics, fleet and distribution

**Money:** per-trip or per-tonne revenue; margin depends on fuel, empty returns and on-time delivery.
**Breaks:** trip and driver tracking by calls, proof of delivery on paper, fuel and expense reconciliation, delayed invoicing because POD copies arrive late.
**Build:** trip log with driver app, photo proof of delivery, trip expense entry, auto customer update by WhatsApp, POD-linked invoice list.
**Signals:** many vehicles, multiple depots, "pan-India", "express".
**Questions:** how long after delivery do you get the signed POD? How do you reconcile driver expenses?

---
