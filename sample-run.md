# Sample run: one lead, start to finish

The test lead from [`sample-lead.json`](sample-lead.json), run through the workflow's logic, with Claude doing the qualification step.

## 1. Lead comes in (Meta lead ad)

| Field | Value |
|---|---|
| Name | Omar Al Mansoori (test lead) |
| Budget | AED 1.5M – 2M |
| Looking for | 3-bed townhouse, Dubai Hills |
| Timeline | Within 3 months |
| Purpose | End use, relocating family |
| Message | "Looking for a townhouse near good schools, would like a payment plan." |

## 2. Claude qualifies it

**Score: 84 / 100 → HOT**

Why:
- Clear AED 1.5M–2M budget that fits a 3-bed townhouse in Dubai Hills
- Buying within 3 months for end use, driven by a family relocation
- Specific needs (schools, payment plan) show active, serious research

**Next best action for the rep:** call within 15 minutes; confirm move date, number of children and school preferences, then send 3 matched listings with payment plan breakdowns.

## 3. What the workflow does with it

| Step | Result |
|---|---|
| HubSpot | Contact created with lead status `OPEN`, AI score 84, tier, reasons and next action |
| Routing | 84 ≥ 70 threshold → hot branch |
| WhatsApp (seconds after the form) | "Hi Omar, thanks for your enquiry. I have a few 3-bed townhouses in Dubai Hills close to top-rated schools, with payment plans within your budget. Is now a good time for a quick call?" |
| Sales alert email | **HOT lead (84/100): Omar Al Mansoori, Dubai Hills**, with budget, timeline, reasons and next action |

## 4. Email drafted for follow-up

> **Subject:** Dubai Hills townhouses near schools
>
> Hi Omar,
>
> Thanks for your enquiry. Since you're relocating with family, I've shortlisted 3-bed townhouses in Dubai Hills within AED 1.5M–2M that are a short drive from well-rated schools and come with payment plans.
>
> Each one differs on handover date and monthly instalments, so it's quicker to walk you through them than to send a long list.
>
> Are you free for a 15-minute call this week?

**Result:** the lead is scored, logged in the CRM, contacted on WhatsApp and handed to a rep with context, all within seconds and without anyone touching it.
