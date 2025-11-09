# Sample Research Prompts

**Purpose**: Copy/paste these prompts into Perplexity Pro, ChatGPT, Claude, or any AI research tool
**Time savings**: ~30 minutes per analysis
**Usage**: Replace `[BUSINESS IDEA]` with your actual idea

---

## Instructions

For each of the 5 research topics below:

1. **Copy the prompt**
2. **Replace `[BUSINESS IDEA]`** with your specific business concept
3. **Paste into AI tool** (Perplexity Pro recommended for real-time data)
4. **Review output**
5. **Save as YAML** using the schema in `phases.md`
6. **Validate**: Check confidence, sources, recency

---

## Topic 1: MARKET RESEARCH

### Prompt
```
Analyze the market for [BUSINESS IDEA].

Please provide:

1. **Total Addressable Market (TAM)**: Global market size in USD
2. **Serviceable Addressable Market (SAM)**: Market you can realistically reach
3. **Serviceable Obtainable Market (SOM)**: Market share you could capture (be realistic)
4. **Growth Rate (CAGR)**: Compound annual growth rate for next 3-5 years
5. **Market Segments**: Key customer segments within this market
6. **Trends**: 3-5 major trends driving or inhibiting growth
7. **Market Maturity**: Is this market emerging, growing, mature, or declining?

Format your response with clear data points, cite sources, and include dates for all statistics.
Prioritize recent data (<6 months old) from credible sources (Gartner, McKinsey, industry reports, etc.).
```

### Example (AI-powered CRM for real estate)
```
Analyze the market for AI-powered CRM software specifically for real estate agents.

[... rest of prompt]
```

---

## Topic 2: COMPETITOR RESEARCH

### Prompt
```
Analyze the competitive landscape for [BUSINESS IDEA].

Please provide:

1. **Top 5 Competitors**: Name, description, market share (if available)
2. **Pricing Models**: How do competitors charge? (subscription, one-time, freemium, etc.)
3. **Pricing Range**: Actual prices (monthly, annually, per user, etc.)
4. **Market Gaps**: What are competitors NOT doing well? Where do customers complain?
5. **Differentiation Opportunities**: Based on gaps, where could a new entrant differentiate?
6. **Competitive Moat**: What makes current players defensible? (network effects, switching costs, etc.)
7. **Recent Failures**: Have any competitors shut down? Why?

Format your response with clear data, cite sources, and be specific about pricing.
Look for customer reviews, complaints, and feature comparison matrices.
```

### Example (Pet snake subscription box)
```
Analyze the competitive landscape for subscription boxes specifically for pet snake owners.

[... rest of prompt]
```

---

## Topic 3: TECHNICAL FEASIBILITY

### Prompt
```
Assess the technical feasibility of building [BUSINESS IDEA].

Please provide:

1. **Complexity Level**: Low, Medium, High (and why)
2. **Estimated Build Time**: For MVP (minimum viable product)
3. **Recommended Tech Stack**: Languages, frameworks, infrastructure
4. **Key Technical Risks**: What could go wrong? (scalability, integration, etc.)
5. **Third-Party Dependencies**: APIs, services, platforms needed
6. **Technical Talent Required**: What skills are needed to build this?
7. **Existing Solutions**: Can you use existing tools/platforms vs building from scratch?

Be specific about build time (in hours or weeks) and justify complexity assessment.
Consider both development time and ongoing maintenance.
```

### Example (AI meal planning app)
```
Assess the technical feasibility of building an AI-powered meal planning app for busy parents that generates personalized meal plans based on dietary restrictions, preferences, and pantry inventory.

[... rest of prompt]
```

---

## Topic 4: USER RESEARCH

### Prompt
```
Analyze the target users for [BUSINESS IDEA].

Please provide:

1. **User Segments**: 2-4 distinct customer segments (demographics, psychographics)
2. **Top 3 Pain Points**: What problems do these users face? (be specific)
3. **Current Solutions**: What do users currently do to solve these problems?
4. **Willingness to Pay (WTP)**: What would users pay for a solution? (monthly, annually, one-time)
5. **Demand Validation**: How can we validate demand before building? (surveys, landing pages, etc.)
6. **User Acquisition Channels**: Where do these users hang out? (online, offline)
7. **Decision Criteria**: What factors influence their buying decisions?

Include data on user behavior, spending patterns, and real quotes/reviews where possible.
Cite sources for WTP estimates (benchmarks, competitor pricing, surveys, etc.).
```

### Example (Coding bootcamp for seniors)
```
Analyze the target users for a coding bootcamp specifically designed for people aged 55+ who want to learn programming for career transition or personal projects.

[... rest of prompt]
```

---

## Topic 5: FINANCIAL MODELING

### Prompt
```
Provide financial benchmarks for [BUSINESS IDEA].

Please provide:

1. **Optimal Pricing**: What should we charge? (based on competitor analysis + value delivered)
2. **Customer Acquisition Cost (CAC)**: Typical CAC for this market/channel
3. **Lifetime Value (LTV)**: Expected LTV based on pricing, retention, upsells
4. **LTV/CAC Ratio**: Is 3x achievable? If not, why?
5. **Profit Margins**: Typical gross and net margins for this type of business
6. **Breakeven Analysis**: How many customers needed to break even?
7. **Unit Economics**: Revenue per customer - variable costs per customer
8. **Churn Rate**: Expected monthly/annual churn rate for this market

Cite specific benchmarks from similar businesses, industry reports, or case studies.
Be realistic about CAC (don't assume $0 organic growth).
```

### Example (B2B SaaS for manufacturing)
```
Provide financial benchmarks for a B2B SaaS tool that helps small manufacturing companies (10-50 employees) track inventory and optimize production schedules. Expected pricing: $299/month.

[... rest of prompt]
```

---

## Advanced Tips

### 1. Customize Prompts for Your Context

Add specifics to get better results:
- **Geography**: "... in Poland" or "... in North America"
- **Vertical**: "... specifically for healthcare" or "... in fintech"
- **Scale**: "... for enterprises (1000+ employees)" or "... for solopreneurs"

### 2. Use Follow-Up Questions

After initial response, ask:
- "Can you provide 3 credible sources for the TAM estimate?"
- "What assumptions are you making about churn rate?"
- "Which of these trends has the highest confidence?"

### 3. Validate Across Multiple Tools

Run same prompt in:
- Perplexity Pro (best for recent data)
- ChatGPT/Claude (best for analysis + synthesis)
- Manual research (Google, industry reports, case studies)

Compare results. If they diverge, dig deeper.

### 4. Save Raw Outputs

Before converting to YAML:
- Save AI output as markdown
- Include prompt used (for reproducibility)
- Note confidence level + source quality

---

## Example: Complete Research Flow

**Business Idea**: "AI-powered legal document review for small law firms"

### Step 1: Market Research
```
Analyze the market for AI-powered legal document review software specifically for small law firms (1-10 attorneys).

[Use Market Research prompt above]
```

**Output**: Save as `market_research.yaml`

### Step 2: Competitor Research
```
Analyze the competitive landscape for AI-powered legal document review software specifically for small law firms (1-10 attorneys).

[Use Competitor Research prompt above]
```

**Output**: Save as `competitor_research.yaml`

### Step 3-5: Repeat for Technical, User, Financial

**Result**: 5 YAML files ready for BILL's synthesis

---

## Quality Checklist

Before moving to Analysis phase, verify each research output has:

- ✅ Confidence score ≥ 0.75
- ✅ At least 3 credible sources cited
- ✅ Data recency < 6 months (for market/competitive)
- ✅ No major contradictions between sources
- ✅ Specific numbers (not "large market" but "$4.2B")
- ✅ Actionable insights (not just facts)

---

## What to Do with Outputs

1. **Save as YAML** using schema in `phases.md`
2. **Run BILL synthesis** (validate consistency across all 5 topics)
3. **Proceed to Analysis phase** (BILL → NASH → STEVE)

---

**Pro Tip**: Bookmark this page. You'll use these prompts for every analysis.

**Time savings**: 30 minutes per analysis (vs writing prompts from scratch)

**Quality improvement**: Consistent structure = better AI outputs
