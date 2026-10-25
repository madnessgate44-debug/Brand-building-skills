# ASIA Growth OS — Readiness and Mission Specification

**Status:** READY FOR EVIDENCE-GATHERING; NOT YET A VALIDATED CAMPAIGN  
**Workspace:** `madnessgate44-debug/Brand-building-skills`  
**Upstream method source:** [Markster OS](https://github.com/markster/markster-os)  
**Scope:** Build a repeatable sales-and-marketing operating process for ASIA. This document is an execution specification, not evidence that a campaign has run or produced results.

## 1. Requirements and acceptance criteria

| ID | Requirement | Acceptance evidence |
|---|---|---|
| R1 | Establish a fact-based business baseline | Approved context record; every material field marked VERIFIED, USER INPUT, ASSUMPTION, or UNKNOWN |
| R2 | Research local demand and customer segments | Dated source log, interview/survey notes where authorized, competitor/alternative map, and explicit evidence limitations |
| R3 | Select a customer segment and positioning | Segment comparison with evidence, selected problem/use case, differentiation supported by proof, and rejected alternatives recorded |
| R4 | Define an offer before promotion | Owner-approved menu/product details, price, availability, service limits, and any terms; no fabricated discounts or claims |
| R5 | Design an acquisition-to-purchase path | Channel → message/asset → call to action → ordering/visit path → tracking method; identify handoffs and failure points |
| R6 | Produce campaign assets | Approved copy/creative variants, audience/channel mapping, factual-claim review, and CTA tested for the actual path |
| R7 | Measure outcomes | KPI definitions, baseline, source of truth, owner, cadence, and actual values; mark missing data NOT AVAILABLE rather than estimating |
| R8 | Review and iterate | Weekly evidence review, decision log, one prioritized bottleneck, next experiment, and explicit stop/continue/change decision |
| R9 | Verify execution truthfully | Distinguish desk simulation, tool-executed work, published campaign, and measured real-world outcome |

## 2. Context ledger

### VERIFIED from repository/user-provided mission context
- ASIA is described as a food/restaurant business located in a mall in Alexandria, Egypt.
- Call-center employees are an identified potential target audience.
- The workspace has a Markster OS integration pointer in `.gitmodules` and a workspace guide in `MARKSTER-OS-WORKSPACE.md`.
- The workspace guide states that a submodule pointer alone does not install the upstream CLI or enable local slash commands in ChatGPT.

### USER INPUT
- The business and location details above, and the call-center audience, are provided as mission context. They have not been independently validated in this repository.

### ASSUMPTIONS — hypotheses only, not facts
- People working in nearby call centers may value convenient, affordable, predictable food options during defined breaks.
- Proximity, service speed, menu fit, price, ordering convenience, and break-time constraints may affect purchase decisions.
- Employer/group ordering may or may not be viable; validate before designing a B2B offer.

### UNKNOWN — must be resolved before a live campaign
- Official business name/brand spelling, exact mall/location, opening hours, contact/order details.
- Menu, prices, portions, gross margins, capacity, preparation/service time, delivery/pickup options, payment methods.
- Current footfall, customer mix, repeat-purchase rate, existing channels, historical sales and seasonality.
- Competitors and alternatives in the mall and around relevant workplaces.
- Customer needs, willingness to pay, break durations, decision-maker/buyer, and purchase frequency.
- Approved claims, photos, testimonials, reviews, permissions, budget, campaign owner, and business success target.

Do not convert an assumption into a claim without collecting evidence and recording its source and date.

## 3. Operating loop

Use the Markster principle of diagnosing the constraint, executing one priority action, checking whether the chosen metric moved, and repeating. Apply it to a local consumer/restaurant journey; do not blindly copy a B2B agency cold-outreach sprint.

1. **Diagnose:** record the business goal and current baseline; identify whether the main constraint is awareness, consideration, conversion, repeat purchase, capacity, or unknown due to missing measurement.
2. **Research:** map relevant customer occasions and alternatives; collect dated, ethical, permissioned evidence. Separate observed behavior from stated preference.
3. **Choose:** select one primary segment/use case and one measurable objective. Record why alternatives were not chosen.
4. **Offer:** verify the real menu/price/availability and operational feasibility with the owner before writing promotional claims.
5. **Build path:** specify channel, audience, message, asset, CTA, ordering/visit route, tracking, and responsible owner.
6. **Launch gate:** do not publish, contact customers, spend money, or change business accounts until the owner approves the exact assets, audience, budget, channel, and timing.
7. **Measure:** capture the baseline and actual outcomes from an identified source; include sample size and period where available.
8. **Learn:** compare results with the predefined objective, inspect qualitative feedback and operational constraints, then keep/change/stop the experiment.

## 4. Initial research plan — no campaign claims

### Research questions
- Which food occasions are realistically serviceable: before work, during breaks, after shifts, or another verified occasion?
- What are the actual break windows, group sizes, purchase routines, budget ranges, and constraints of the intended audience?
- What alternatives do customers currently use, and what verified unmet need exists?
- Which products can ASIA reliably serve at the relevant time and volume while meeting owner-approved margin and service constraints?
- Which purchase path is simplest and measurable: walk-in, pre-order, phone/message order, or another option that ASIA actually supports?

### Evidence collection
- Audit owner-provided menu, prices, hours, service capacity, channels, and historical sales if available.
- Observe publicly accessible competitor/alternative information and record source URLs and access dates.
- If authorized, conduct a small, consent-based customer discovery sample; log questions, sample size, dates, and limitations. Do not claim it represents the whole market.
- Verify the physical route, actual ordering steps, and handoff with staff before proposing a CTA.
- Produce a source log with fields: claim/question, source, date accessed, evidence excerpt/summary, confidence, limitation, and decision affected.

## 5. Funnel and measurement specification

Treat these as candidate metrics; use only those supported by real data and the actual ordering path.

| Funnel stage | Candidate metric | Required source |
|---|---|---|
| Reach | Relevant local reach/impressions | Platform or documented distribution count |
| Interest | Qualified inquiries, menu views, CTA clicks | Platform analytics or a defined manual log |
| Conversion | Attributed orders/purchases; conversion rate | Order/POS records linked to a defined campaign attribution method |
| Economics | Revenue and contribution after variable costs | Owner-approved sales and cost records |
| Repeat | Repeat customers/orders within a defined period | Privacy-respecting customer/order records with a defined method |
| Operations | Fulfilment time, unavailable items, service failures | Staff/operations log |

Define each metric before launch. A conversion rate is numerator divided by denominator for the same period and cohort; state both counts. Do not infer revenue, profit, return on ad spend, or campaign lift from likes or reach alone. If attribution is not credible, report it as un-attributed rather than claiming causation.

## 6. Deliverables required before campaign approval

- [ ] Approved company-context record and unresolved-unknowns list.
- [ ] Dated local market/alternative map and customer evidence log.
- [ ] Segment comparison and evidence-backed positioning recommendation.
- [ ] Owner-approved offer, operational constraints, and factual-claims checklist.
- [ ] End-to-end acquisition/purchase path with tracking and handoff checks.
- [ ] Draft creative/copy variants with source for every factual claim.
- [ ] KPI baseline, formulas, data sources, reporting cadence, and owner.
- [ ] Risk/privacy/permission review and explicit launch approval.
- [ ] Post-test report separating actual data, interpretation, limitations, and next decision.

## 7. Upstream reuse and attribution

Prefer the upstream consumer/DTC and relevant local-service patterns where applicable; use the marketing-agency segment only for transferable operating disciplines, not as a literal restaurant playbook. Inspect the actual upstream files and license before copying any content into this workspace. Preserve the upstream MIT license and trademark notices; do not present Markster/ScaleOS material as original or imply affiliation.

Useful upstream starting points:
- [Markster OS repository](https://github.com/markster/markster-os)
- [Consumer/DTC segment](https://github.com/markster/markster-os/blob/main/playbooks/segments/startup-archetypes/dtc-consumer.md)
- [Marketing-agency segment](https://github.com/markster/markster-os/blob/main/playbooks/segments/service-firms/marketing-agency.md)
- [Workspace integration guide](../MARKSTER-OS-WORKSPACE.md)

The branch/submodule checkout state and exact upstream default-branch paths must be verified before claiming these links are the version used for an execution.

## 8. Execution status and closure gates

- [x] Mission specification drafted with explicit unknowns and no invented offers/results.
- [ ] Verify the upstream submodule gitlink and pinned commit from the target repository tree.
- [ ] Verify upstream default branch, exact source files, and license at the pinned revision.
- [ ] Complete the business-context ledger from owner-approved evidence.
- [ ] Complete research and choose the first evidence-backed bottleneck.
- [ ] Create and review campaign assets; do not publish without explicit approval.
- [ ] Execute one bounded test and capture raw metrics.
- [ ] Review results and record a decision.
- [ ] Run repository checks and review the final diff.

**Closure rule:** A simulated workflow is not a live campaign. A draft asset is not a published asset. A published campaign is not proof of business impact until attributable outcome data is collected and reviewed.
