---
name: competitive-analysis
description: >
  Conducts a structured competitive analysis on a product, market, or initiative.
  Use this skill whenever Jasmine asks for a competitive analysis, wants to understand
  what competitors are doing, how a product or initiative stacks up against the market,
  who the key players are in a space, or what differentiation opportunities exist.
  Trigger phrases include: "competitive analysis", "what do competitors do", "how do we
  compare", "who else is doing this", "landscape analysis", "market map", "what does
  [competitor] offer". Always collect inputs before writing. Always cite sources.
  Use this skill even if the request is casual or exploratory — e.g. "what's the
  competitive landscape for X" or "are there other companies doing Y".
---

# Competitive Analysis

This skill produces a structured competitive analysis grounded in established frameworks
from top consulting firms (BCG, McKinsey, Bain) and business school methodology, as
well as AI-era frameworks for evaluating moat, infrastructure posture, and
differentiation strategy in markets where AI is a core part of the product.

It combines primary sentiment research with structured output across eight dimensions.

Always cite specific sources. Always name the framework being applied to reach any
conclusion. Do not present claims without attribution.

---

## Step 0: Confirm Intent and Collect Inputs

Before doing any research, confirm with Jasmine and collect the following:

> "I'll run a competitive analysis for you. A few quick inputs before I start:"

1. **Market and ICP** — What market and customer profile are we analyzing?
   e.g. "RCM automation for health systems" or "prior auth software for ambulatory clinics"

2. **Timeframe** — What time horizon matters? (current state, 12-month trend, 3-year shift?)

3. **Framework preference** — Any specific framework to anchor on, or should I select
   the best fit based on the market? (See references/frameworks.md for options.)

4. **Known competitors** — Any specific competitors to include? Or should I identify them
   through research?

5. **Depth** — Quick scan (3-5 competitors, high-level) or deep dive (7+ competitors,
   full output)?

6. **AI lens** — Are any competitors AI-native startups (founded post-2022, product
   built on top of LLMs or ML)? If yes, include the AI Moat Analysis section in output.
   If unsure, research and determine during Step 3.

Do not proceed until these are confirmed. If any input is ambiguous, ask a clarifying
follow-up rather than assuming.

---

## Step 1: Framework Selection

Based on the market and ICP provided, select the most appropriate framework(s).
Read `references/frameworks.md` for the full menu of options with descriptions.

**Default selection logic:**
- Mature, well-defined market with clear competitors → Porter's Five Forces + Feature Matrix
- Emerging or fragmented market → Jobs-to-be-Done lens + Blue Ocean Strategy
- Strategic positioning question → BCG Growth-Share Matrix or McKinsey 3 Horizons
- Direct feature comparison → Feature Matrix + Value Proposition Canvas
- Go-to-market or pricing question → Business Model Canvas comparison
- Market with AI-native competitors → AI Moat Framework (see references/frameworks.md)
  applied alongside whichever traditional framework fits the market structure

Always name the selected framework(s) explicitly in the output and explain briefly why
they were chosen for this market.

---

## Step 2: Sentiment Gathering

Search social media, review sites, forums, and articles to capture authentic customer
voice about each competitor. Use web search across:

- Reddit (r/healthIT, r/rcm, relevant subreddits)
- G2, Capterra, Trustpilot, Google Reviews
- LinkedIn posts and comments
- Industry press (HFMA, Becker's, Healthcare Dive, MedCity News)
- Analyst reports where accessible

For each competitor, capture:

- **What customers love** — recurring positive themes, specific features praised
- **What customers dislike** — pain points, gaps, complaints, churn reasons
- **How customers frame value** — what outcomes they associate with the product
- **Competitive switching signals** — mentions of switching to/from this competitor

Record the source URL for every sentiment data point used in the output. Do not
paraphrase sentiment without attribution.

---

## Step 3: Competitive Research

For each competitor identified, research:

- Core product features and capabilities
- Business model (SaaS, services, hybrid, usage-based, etc.)
- Pricing signals (published pricing, analyst estimates, customer mentions)
- Stated value proposition and positioning language (use their own words)
- ICP and personas targeted (inferred from marketing, case studies, sales content)
- Marketing emphasis — which features or outcomes they lead with
- Strategic partnerships (EHR integrations, payer relationships, channel partners)
- Market share signals (funding, customer count, press coverage, analyst mentions)

**For AI-native competitors, additionally research:**
- What AI infrastructure are they building on? (foundation model APIs, fine-tuned models,
  proprietary models, open-source, or hybrid)
- What is their claimed or apparent data moat? (proprietary training data, outcome data,
  feedback loops, exclusive data partnerships)
- What is their AI cost structure? (inference costs relative to value delivered, usage-based
  pricing signals, gross margin signals from investor materials or press)
- Where are they investing in vertical integration vs. relying on third-party AI? (are
  they building their own models or buying intelligence as a commodity?)
- What workflow depth have they achieved? (API-level wrapper vs. deeply embedded in
  customer workflows with switching costs)
- Are they building agentic capabilities? (autonomous multi-step execution vs. assistive AI)
- What is their feedback loop architecture? (does usage make the product smarter?
  how quickly does their model improve from production data?)

Use company websites, press releases, LinkedIn, Crunchbase, and industry press.
Cite sources for every data point.

---

## Step 4: Output

Produce the competitive analysis using this exact structure:

---

### Competitive Analysis: [Market / ICP]
**Date:** [date]
**Framework(s) applied:** [name frameworks and one-line rationale]
**Sources:** [running list of all URLs cited throughout]

---

#### 1. Feature Matrix

Table with features as rows, competitors as columns. Mark support with ✓, partial
support with ◑, and absence with —. Add a row for the user's own product if provided.

| Feature | [Competitor A] | [Competitor B] | [Competitor C] |
|---|---|---|---|
| [Feature] | ✓ | — | ◑ |

Note source for any feature claim that isn't self-evident from the product website.

---

#### 2. Business Model and Pricing

For each competitor: model type, pricing structure (if known), contract terms signals,
and any notable pricing strategy observations. Flag estimates clearly.

---

#### 3. Unique Value Proposition to ICP

For each competitor: their stated UVP, the outcome they promise, and how they
differentiate it for the ICP. Use their own language where possible, with source.

---

#### 4. Personas Targeted

For each competitor: the buyer persona, end user persona, and any notable persona
shifts observed in recent marketing. Infer from case studies, sales pages, and ads.

---

#### 5. Marketing Emphasis

What features or outcomes does each competitor lead with in their marketing? What
problems do they position against? Note any recent campaign shifts.

---

#### 6. Strategic Partnerships

EHR integrations, payer relationships, channel partners, technology alliances.
Note depth of integration where discernible (certified vs. mentioned vs. native).

---

#### 7. Market Share

T-shirt size estimate (XL / L / M / S) with rationale — based on funding, customer
count signals, press coverage, and analyst mentions. Always flag as estimate.

---

#### 8. AI Moat Analysis *(include when any competitor is AI-native)*

For each AI-native competitor, evaluate across five dimensions of AI-era defensibility.
Read `references/frameworks.md` → AI Moat Framework section before completing this.

**a) Model layer posture**
Is this competitor building proprietary models, fine-tuning on domain data, or wrapping
foundation model APIs with minimal differentiation? Rate: Thin wrapper / Tuned / Proprietary.

**b) Data moat**
What proprietary data assets does this competitor have or appear to be accumulating?
Is the data unique, exclusive, and improving the model over time through production use?
Rate: Weak / Moderate / Strong. Flag if unclear.

**c) Workflow integration depth**
How deeply embedded is the AI in the customer's actual workflow? Are there meaningful
switching costs, or is this a tool that sits on top of existing systems without integration?
Rate: Surface / Integrated / Mission-critical.

**d) Feedback loop architecture**
Does usage make the product smarter? Is there a compounding data flywheel — where more
customers → more data → better model → more customers? Rate: None / Passive / Active flywheel.

**e) AI cost structure and margin signals**
What do inference costs appear to be relative to value delivered? Is this company
likely to improve margins as models commoditize, or are they vulnerable to being
undercut by cheaper foundation models? Flag any pricing signals or investor commentary
on unit economics.

**Summary:** For each AI-native competitor, one paragraph synthesizing their overall
moat strength and primary vulnerability from an AI-era lens.

---

#### 9. Strategic Implications

Apply the selected framework(s) to synthesize findings into 3-5 strategic observations.
What whitespace exists? Where is the market converging? What are the highest-leverage
differentiation opportunities? Label each observation with the framework lens used.

For markets with AI-native competitors, include at least one observation on the AI moat
landscape: who is building durable differentiation vs. who is at risk of commoditization
as foundation models improve and cheapen.

---

## Guardrails

- Every data point must have a source. Never present a claim without attribution.
- Always name the framework applied to reach any strategic conclusion.
- Flag estimates, inferences, and unverified claims explicitly — don't present them
  as fact.
- If a competitor's pricing is unknown, say so rather than guessing.
- Do not editorialize beyond what the data supports without labeling it as inference.
- If sentiment data is thin for a competitor, note the gap rather than extrapolating.
- Keep feature matrix rows consistent across all competitors — don't add rows that
  only apply to one player.
