# Product

<!-- impeccable:product-schema 1 -->

## Platform

web

## Stack

Static HTML/CSS/JS, single file in `site/`, no build step. Deployed to Vercel at https://newsleaf.ai.

## Users

Primary surface audience: competition judges with an investor mindset, reading the pitch page alone with no presenter. Product audience: individual investors and financial advisers who hold oil, gas, shipping and airline exposure.

## Product Purpose

Newsleaf reads energy news for investors. Every weekday at 06:00 it sends an issue listing what changed since the previous issue (new, weakened, unchanged events) and which way each change pushes oil, gas, shipping and airline investments, with links to source articles. Subscribers also get search over the full news graph, including as-of-earlier-day queries.

## Positioning

Direction, not sentiment: the same headline pushes crude up and airlines down. Newsleaf keeps news as a time-stamped graph of events, entities and affected investments, so it reports deltas (what changed) instead of re-reporting stories, and every published direction is scored against the price move that followed in a public scorecard.

## Operating Context

Pipeline: watch (six sources: publisher RSS, GDELT, NewsAPI.org, SEC EDGAR, EIA, OPEC) → ingest (raw archive) → extract and classify (LLM) → merge (events, entity resolution) → link to investments (human-reviewed event-type table) → store with time (bitemporal arrows with decaying weight) → delta → publish (editor review, 06:00 weekdays). Subscriptions sold through Substack.

## Capabilities and Constraints

- Pre-launch; demo runs on a small synthetic example graph (3 invented events). Must be labeled as sample data.
- Bloomberg and FT excluded from v1 (terms forbid automated collection).
- Not personal investment advice.

## Evidence on Hand

- EIA (May 2026): Hormuz oil flows fell from 20.7 to 14.6 million barrels/day in one quarter; Brent up more than 45% since the start of the war in Iran.
- Pricing: $30/month or $300/year; about $259 net per $300 after Substack 10% and card fees. Competitors: Doomberg $400, Doomberg Pro $1,200, Energy Outlook Advisors $420 (2023), large general Substacks $50–220.
- Funding ask $25,000: news data $5,388; model usage $3,000; hosting $1,800; legal $5,000; first subscribers $6,000; contingency $3,812.
- From year two, running costs about $10,200/yr, covered by 40 annual subscribers; target 100 subscribers by month 12 (~$25,900/yr).
- Team: Sairam Krishnan (product and technical lead), Katera Mujadidi (CFO and venture capital specialist; originated the idea).
- No testimonials, customers, or track record yet. Do not fabricate any.

## Product Principles

1. Show direction, not tone.
2. Report what changed, not what was repeated.
3. Every claim is checkable: sources linked, directions scored publicly.
4. Old news fades; nothing is silently deleted.

## Brand Commitments

- The page is dark green throughout: background #0E1614, surfaces #15201D / #1C2926, rules #2B3935, ink #E3EBE8, muted #97A7A2, teal accent #4DB6A7, amber #E9A553 for "up", periwinkle #9DAAF2 for "down". These are the original site's dark-theme colours, and the user wants them as the page's look. Confirmed 2026-10-02.
