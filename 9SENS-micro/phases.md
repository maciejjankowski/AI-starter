# 9SENS-micro: Two-Phase Analysis System

**Version**: 1.0.0
**Phases**: 2 (Research, Analysis)
**Output**: Structured deliverables in `deliverables/YYYY-MM-DD - TOPIC/`

---

## Overview

9SENS-micro operates in two distinct phases:

1. **Phase 1: Research** → Gather data and validate facts
2. **Phase 2: Analysis** → Multi-perspective synthesis and recommendations

Each phase has specific inputs, processes, outputs, and quality gates.

---

## Phase 1: RESEARCH

**Primary Persona**: BILL
**Supporting Personas**: NASH (financial optimization), STEVE (market trends)

### Purpose

Establish factual foundation through systematic research across 5 core topics:
1. **Market** - TAM/SAM/SOM, growth rates, segments, trends
2. **Competitors** - Players, pricing, gaps, differentiation opportunities
3. **Technical** - Feasibility, build time, stack recommendations, risks
4. **User** - Personas, pain points, willingness to pay, validation methods
5. **Financial** - Pricing models, CAC, LTV, margins, breakeven

### Process

#### Step 1: Topic Scoping (15 min)
```
Input: Business idea or problem statement
Output: 5 research prompts (one per topic)

Example:
Idea: "AI-powered CRM for real estate agents"

Generated Prompts:
1. [MARKET] What is the TAM/SAM/SOM for real estate CRM software? Growth rate?
2. [COMPETITORS] Who are the top 5 real estate CRM competitors? Pricing? Gaps?
3. [TECHNICAL] How complex is building AI-powered CRM? Tech stack? Build time?
4. [USER] What are real estate agent pain points with current CRMs? WTP?
5. [FINANCIAL] What are typical CAC, LTV, margins for B2B SaaS in real estate vertical?
```

#### Step 2: Research Execution (1-3 hours)

**Recommended Tools**:
- Perplexity Pro (real-time web search, recent data)
- Claude/GPT-5 (structured reasoning, analysis)
- Manual research (industry reports, case studies)

**Process**:
1. Copy prompt to AI tool
2. Review output for quality
3. Save as YAML (see schema below)
4. Repeat for all 5 topics

**Quality Gate**: Each topic must have:
- Confidence score ≥ 0.75
- At least 3 credible sources
- Data recency < 6 months (for market/competitive data)
- No contradictions between sources

#### Step 3: Research Synthesis (30 min)

BILL reviews all 5 research outputs and:
- Validates data consistency
- Identifies contradictions
- Flags low-confidence findings
- Exposes unsupported assumptions

**Output**: `deliverables/YYYY-MM-DD - TOPIC/research_synthesis.yaml`

### YAML Schema (per topic)

```yaml
research_topic: "market|competitor|technical|user|financial"
research_date: "YYYY-MM-DD"
confidence: 0.XX

findings:
  key_insight_1: "..."
  key_insight_2: "..."
  key_insight_3: "..."

  # Topic-specific fields
  # Market: tam, sam, som, cagr, segments, trends
  # Competitor: players, pricing, gaps, differentiation
  # Technical: complexity, build_time, stack, risks
  # User: personas, pain_points, willingness_to_pay, validation
  # Financial: pricing, cac, ltv, margin, breakeven

sources:
  - title: "Report Title"
    url: "https://..."
    date: "YYYY-MM-DD"
    reliability: "high|medium|low"

  - title: "Another Source"
    url: "https://..."
    date: "YYYY-MM-DD"
    reliability: "high|medium|low"

recommendations:
  - text: "Recommendation based on research"
    priority: "high|medium|low"
    rationale: "Why this matters"

  - text: "Another recommendation"
    priority: "high|medium|low"
    rationale: "Why this matters"
```

### Deliverables

1. `market_research.yaml`
2. `competitor_research.yaml`
3. `technical_research.yaml`
4. `user_research.yaml`
5. `financial_research.yaml`
6. `research_synthesis.yaml` (BILL's validation)

---

## Phase 2: ANALYSIS

**All Personas**: BILL → NASH → STEVE (sequential)

### Purpose

Transform research data into actionable insights through multi-persona analysis:
- **BILL** validates data and exposes patterns
- **NASH** optimizes decisions through expected value analysis
- **STEVE** positions strategically and identifies opportunities

### Process

#### Step 1: BILL's Data Analysis (20 min)

BILL takes all research and:
- Validates consistency across topics
- Identifies patterns (trends, correlations, anomalies)
- Exposes assumptions vs facts
- Flags contradictions or data gaps
- Provides declarative findings

**Output**: `bill_analysis.md`

**Example**:
```markdown
# BILL's Analysis: AI-Powered Real Estate CRM

## Data Validation
Market size: $4.2B (validated across 3 sources, confidence: 0.85)
CAGR: 23% (2024-2029, consistent in 2 reports)
Competitors: 47 identified, 12 with >$10M funding

## Patterns Detected
1. Failed attempts cluster 2018-2020 (8 shutdowns)
   - Common cause: Poor UX, not AI capability
2. Successful players focus on lead gen, not CRM
3. Real estate agents churn 40% annually (industry data)

## Assumptions Exposed
ASSUMPTION: "AI gives competitive advantage"
REALITY: AI is table stakes. 7/12 competitors already use AI.

ASSUMPTION: "Agents will pay $99/month"
REALITY: Current market pricing: $29-79/month. $99 is outlier.

## Contradictions Found
Research claims "$50B TAM" but validated TAM is $4.2B.
Discrepancy: 11.9x. Source error or segment mismatch.

## Data Gaps
- No churn data for AI-specific CRM features
- Missing: Real estate vertical CAC benchmarks
- User pain points documented but not quantified
```

#### Step 2: NASH's Decision Optimization (20 min)

NASH takes BILL's analysis + financial research and:
- Calculates expected value for scenarios
- Maps decision trees
- Analyzes opportunity costs
- Identifies optimal resource allocation
- Applies Pareto principle

**Output**: `nash_analysis.md`

**Example**:
```markdown
# NASH's Analysis: AI-Powered Real Estate CRM

## Expected Value Analysis

SCENARIO A (Current plan: $99/mo premium positioning):
- P(success) = 0.20 (market expects $79-89)
- Payoff = $2.4M (3yr exit, 800 customers)
- EV = $480K

SCENARIO B (Market-rate pricing: $79/mo with upsell):
- P(success) = 0.50 (aligned with market)
- Payoff = $1.8M (3yr exit, 1000 customers)
- EV = $900K

SCENARIO C (Pivot to brokerages B2B2C):
- P(success) = 0.35 (unproven channel)
- Payoff = $4.5M (5yr exit, enterprise value)
- EV = $1.575M

RECOMMENDATION: Scenario C (highest EV)

## Opportunity Cost Analysis

Building this CRM = 18 months
Alternative A: AI sales coaching tool = $3M+ EV (larger TAM)
Alternative B: Lead marketplace = $5M+ EV (network effects)

Opportunity cost of building CRM vs alternatives: -$1.4M to -$3.4M

CRITICAL QUESTION: Is this the highest-value use of 18 months?

## Pareto Principle Application

80% of revenue will come from 20% of features:
- MUST-HAVE (20%): Contact management, email integration, lead scoring
- NICE-TO-HAVE (80%): AI coaching, document gen, market analytics, mobile app

RECOMMENDATION: Build MVP with top 20% features only
- Cut scope by 75%
- Launch in 4 months instead of 18
- Test market thesis faster
- Pivot or scale based on data

## Game Theory Considerations

Competitive response timeline:
- Month 0-6: You launch, competitors unaware
- Month 6-12: Competitors notice, start copying
- Month 12-18: Copies launch, advantage erodes

First-mover advantage window = 6-12 months MAX

STRATEGIC IMPLICATION: Speed > perfection
Launch fast, iterate based on data, build moat through network effects

## Decision Tree

[1] Build full product (18 months)
    ├─ [1a] Success (P=0.35) → $1.8M
    └─ [1b] Fail (P=0.65) → -$180K

[2] Build MVP (4 months)
    ├─ [2a] Validate (P=0.60) → Scale to full product
    │       ├─ Success (P=0.50) → $2.2M
    │       └─ Fail (P=0.50) → -$80K
    └─ [2b] Invalidate (P=0.40) → Pivot to Alternative A
            └─ Success (P=0.60) → $3M

EV[1] = $495K
EV[2] = $1.14M

OPTIMAL PATH: Build MVP (4 months) → Validate → Scale or Pivot
```

#### Step 3: STEVE's Strategic Synthesis (20 min)

STEVE takes BILL + NASH outputs and:
- Assesses market positioning
- Identifies blue ocean opportunities
- Evaluates timing and moat
- Provides strategic recommendations
- Charts execution path

**Output**: `steve_analysis.md`

**Example**:
```markdown
# STEVE's Analysis: AI-Powered Real Estate CRM

## Strategic Reality
You're in a RED OCEAN. 47 competitors, bloody margins, race to bottom.

## Blue Ocean Adjacent
Don't build "better CRM" → Build "relationship intelligence platform"

Key shift:
- FROM: Store contacts, send emails
- TO: Predict which leads convert, auto-prioritize, AI-coached conversations

## Market Timing
EARLY. Market needs 18 months to mature.

Evidence:
- Enterprise buyers abandoning monoliths (trend: 3 years)
- But SMB real estate = survival mode, not growth mode
- Agents adopt slowly, churn fast

## Strategic Pivot Required
Current: Target individual agents ($79/month)
Recommended: Target brokerages ($5K/month for 50-agent teams)

Why:
- B2B2C lowers CAC (one sale = 50 users)
- Brokerages have budget + retention incentive
- Network effects within brokerage create moat

## Inimitable Moat
Network effects + proprietary data = defensible

Execution:
1. Start with 5 brokerages (proof of concept)
2. Build agent success stories
3. Use data to improve AI (flywheel)
4. Competitors can't replicate your dataset

## Competitive Moat Analysis
Current moat: NONE (AI is commodity)
Required moat: Data network effects

## Execution Gap
You lack distribution. Options:
1. Partner with brokerage software (Dotloop, SkySlope)
2. Hire brokerage sales team (expensive)
3. White-label to existing CRM (fast but low margin)

Recommendation: Partner. Speed > margin at this stage.

## Strategic Roadmap
Year 1: Partner with 1 major brokerage software
Year 2: Build direct sales, 20 brokerages
Year 3: Exit to strategic (CRM giant needs your AI + data)

## Timing Windows
- Enter now: Too early, burn cash educating market
- Enter in 18 months: Competitors will have entrenched
- RECOMMENDED: Build in stealth, launch in 12 months (perfect timing)

## Final Verdict
Current plan: 4/10 (incremental improvement, red ocean)
Pivot plan: 8/10 (blue ocean, defensible, but execution risk HIGH)
```

### Deliverables

1. `bill_analysis.md` (Data validation + patterns)
2. `midas_analysis.md` (Financial viability)
3. `steve_analysis.md` (Strategic positioning)
4. `synthesis_report.md` (Combined recommendations)

---

## Output Structure

All outputs go to: `deliverables/YYYY-MM-DD - TOPIC/`

Example:
```
deliverables/
└── 2025-11-08 - AI Real Estate CRM/
    ├── research/
    │   ├── market_research.yaml
    │   ├── competitor_research.yaml
    │   ├── technical_research.yaml
    │   ├── user_research.yaml
    │   ├── financial_research.yaml
    │   └── research_synthesis.yaml
    │
    └── analysis/
        ├── bill_analysis.md
        ├── nash_analysis.md
        ├── steve_analysis.md
        └── synthesis_report.md
```

---

## Quality Gates

### Research Phase Must Pass:
- ✅ All 5 topics completed
- ✅ Average confidence ≥ 0.75
- ✅ At least 3 sources per topic
- ✅ Data recency < 6 months
- ✅ No major contradictions

### Analysis Phase Must Pass:
- ✅ BILL validates data consistency
- ✅ NASH calculates expected values and identifies optimal path
- ✅ STEVE provides strategic direction
- ✅ Synthesis resolves persona conflicts
- ✅ Actionable recommendations provided

---

## Limitations (By Design)

9SENS-micro stops after Analysis. Full framework includes:

**Not Included in Micro**:
- Phase P2: Design/Architecture
- Phase P3: Implementation/Build
- Phase P4: Testing/Validation
- Phase P5: Reflection/Learning
- Adversarial validation gate
- Automated decision logging
- Integration testing
- Full DRAF methodology

**To Get Full Framework**: Contact for 9SENS complete system

---

## Next Steps

After completing both phases:

1. Review `synthesis_report.md` for key decisions
2. Validate assumptions flagged by BILL
3. Stress-test financial model per MIDAS
4. Execute strategic pivots per STEVE
5. Decide: Build, pivot, or kill

---

**Ready to start**: See `CLAUDE.md` for AI agent instructions
