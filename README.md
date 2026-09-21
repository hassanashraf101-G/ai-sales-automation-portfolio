# 03 · Weekly Pipeline + A/B Test Report with AI Insights

**Problem:** leadership asks "how's the pipeline?" and someone spends Monday morning pulling numbers together by hand.
**Solution:** every Monday at 09:00 this workflow pulls deals from HubSpot and outbound results from the lead sheet, calculates the numbers that matter, has AI write a short summary with actions, and emails a clean HTML report.

```mermaid
flowchart LR
    A[Monday 09:00] --> B[HubSpot: deals, last 90 days]
    B --> C[Sheet: outbound log]
    C --> D[Calculate metrics]
    D --> E[AI: headline, insights, actions]
    E --> F[HTML report] --> G[Email leadership]
```

## What's in the report

| Section | Metric |
|---|---|
| Headline | The single most important number this week |
| Pipeline | Open pipeline value, deals won, win rate |
| By stage | Deal count and value per stage |
| Stalled deals | Open deals with no update in 14+ days |
| A/B test | Emails sent, replies and reply rate per variant |
| Actions | Up to 3 specific actions for the week |

The metrics are calculated in code, not by AI. The AI only interprets numbers it is given and is instructed never to invent any.

## Setup

- **HubSpot** private app with deals read access. Stage names are mapped for the default pipeline. Edit `stageNames` in `Calculate Pipeline Metrics` for custom stages.
- **Google Sheet:** the same `Leads` tab used by workflow 02.
- **Email:** set sender and leadership addresses in `Email Leadership`.
- **Volume:** the HubSpot search returns up to 100 deals. For larger pipelines, add pagination using the `paging.next.after` cursor.
