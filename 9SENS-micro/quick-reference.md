# 9SENS-micro: Quick Reference Card

**Print this** | **Pin this** | **Reference this constantly**

---

## ⚡ 30-Second Overview

**3 Personas** → BILL (data), NASH (optimization), STEVE (strategy)
**2 Phases** → Research (gather data), Analysis (multi-perspective synthesis)
**Output** → `deliverables/YYYY-MM-DD - TOPIC/` with GO/NO-GO recommendation

---

## 🎭 Persona Triggers (When to Use Each)

| Persona | Use When You Need... | Output Style |
|---------|---------------------|--------------|
| **BILL** | Data validation, pattern detection, BS elimination | Declarative facts, no hedging |
| **NASH** | Decision optimization, expected value, resource allocation | Probabilistic, game theory |
| **STEVE** | Market positioning, competitive moat, strategic direction | Paradigm shifts, blue ocean |

**Sequence**: Always BILL → NASH → STEVE (never parallel)

---

## 📋 Phase Checklist

### Phase 1: RESEARCH (2-4 hours)

- [ ] Market research (TAM/SAM/SOM, CAGR, segments, trends)
- [ ] Competitor research (players, pricing, gaps, differentiation)
- [ ] Technical research (feasibility, build time, stack, risks)
- [ ] User research (personas, pain points, WTP, validation)
- [ ] Financial research (pricing, CAC, LTV, margins, breakeven)
- [ ] BILL's synthesis (validate consistency, expose contradictions)

**Quality Gate**: Avg confidence ≥0.75, ≥3 sources/topic, data <6mo old

### Phase 2: ANALYSIS (1-2 hours)

- [ ] BILL analyzes (data validation, patterns, gaps)
- [ ] NASH analyzes (expected values, decision trees, opportunity costs)
- [ ] STEVE analyzes (positioning, moat, timing, roadmap)
- [ ] Synthesis report (combined recommendations, GO/NO-GO)

**Quality Gate**: BILL validates data, NASH calculates EV and optimal path, STEVE provides strategy

---

## 🎯 Quality Gate Thresholds

| Gate | Threshold | Status |
|------|-----------|--------|
| Research confidence | ≥0.75 average | ✅ PASS / ❌ FAIL |
| Sources per topic | ≥3 credible | ✅ PASS / ❌ FAIL |
| Data recency | <6 months | ✅ PASS / ❌ FAIL |
| LTV/CAC ratio | ≥3x | ✅ PASS / ⚠️ FLAG |
| Payback period | ≤12 months | ✅ PASS / ⚠️ FLAG |
| Persona consensus | All agree OR conflicts resolved | ✅ PASS / ⚠️ FLAG |

---

## 📁 Output Structure

```
deliverables/YYYY-MM-DD - TOPIC/
├── research/
│   ├── market_research.yaml
│   ├── competitor_research.yaml
│   ├── technical_research.yaml
│   ├── user_research.yaml
│   ├── financial_research.yaml
│   └── research_synthesis.yaml (BILL)
│
└── analysis/
    ├── bill_analysis.md
    ├── midas_analysis.md
    ├── steve_analysis.md
    └── synthesis_report.md (GO/NO-GO)
```

---

## 🚦 GO/NO-GO Decision Tree

```
START
  ↓
BILL: Data validated?
  ├─ NO → KILL (bad data = bad decisions)
  └─ YES → Continue
       ↓
NASH: Positive expected value?
  ├─ NO → Higher-EV alternatives exist?
  │        ├─ YES → PIVOT (pursue better opportunity)
  │        └─ NO → KILL (opportunity cost too high)
  └─ YES → Continue
       ↓
STEVE: Defensible moat?
  ├─ NO → Blue ocean alternative?
  │        ├─ NO → KILL (red ocean = death)
  │        └─ YES → PIVOT
  └─ YES → Continue
       ↓
All 3 Aligned?
  ├─ YES → GO (high confidence)
  ├─ 2/3 → GO with caution (address dissent)
  └─ 1/3 or 0/3 → NO-GO or major PIVOT
```

---

## 💬 Persona Voice Quick Guide

### BILL Speaks Like This:
```
Market is $4.2B (Gartner 2024). Your claim of $50B is off by 11.9x.
Pattern detected: 8 shutdowns in 2018-2020.
Churn is 65%. This is structural, not fixable with marketing.
```

**Never**: "It seems", "perhaps", "might be"
**Always**: Declarative, cited, pattern-focused

### NASH Speaks Like This:
```
Expected Value Analysis:
SCENARIO A: $500K payoff × 0.30 prob = $150K EV
SCENARIO B: $1.8M payoff × 0.60 prob = $1.08M EV
RECOMMENDATION: Scenario B (7x higher EV)

Opportunity cost: Building this = forgoing $3M+ EV alternatives
Pareto: 80% of value from 20% of features - cut scope, launch faster
```

**Never**: Certainty without probabilities, ignoring alternatives
**Always**: Probabilistic, decision trees, opportunity cost explicit

### STEVE Speaks Like This:
```
You're in red ocean. 47 competitors, bloody margins.
Blue ocean adjacent: Not "better CRM" but "relationship intelligence".
Timing: EARLY. Market needs 18 months to mature.
Inimitable moat required. Network effects + proprietary data = defensible.
```

**Never**: Incremental improvements, short-term thinking
**Always**: Paradigm shifts, Darwinian language, long-term vision

---

## ⚠️ Common Mistakes to Avoid

| Mistake | Fix |
|---------|-----|
| Running personas in parallel | Always sequence: BILL → NASH → STEVE |
| Hedging language in BILL | Use declarative statements only |
| Skipping quality gates | Validate confidence, sources, recency |
| Ignoring persona conflicts | Address in synthesis, don't ignore |
| Vague recommendations | Be specific, actionable, data-driven |

---

## 🔢 Key Financial Formulas

```
LTV/CAC Ratio = Lifetime Value ÷ Customer Acquisition Cost
  Target: ≥3x (SaaS standard)

Payback Period = CAC ÷ Monthly Revenue per Customer
  Target: ≤12 months (ideally ≤6)

Churn Rate = (Customers Lost ÷ Total Customers) × 100
  Target: <5% monthly (SaaS), <40% annually (subscription boxes)

Unit Economics = Revenue per Customer - Variable Cost per Customer
  Target: Positive + expanding over time

TAM = Total Addressable Market (everyone who could buy)
SAM = Serviceable Addressable Market (who you can reach)
SOM = Serviceable Obtainable Market (who you'll actually get)
```

---

## 📊 Research YAML Schema (Quick Template)

```yaml
research_topic: "market|competitor|technical|user|financial"
research_date: "YYYY-MM-DD"
confidence: 0.XX

findings:
  key_insight_1: "..."
  key_insight_2: "..."
  # Topic-specific fields here

sources:
  - title: "..."
    url: "..."
    date: "YYYY-MM-DD"
    reliability: "high|medium|low"

recommendations:
  - text: "..."
    priority: "high|medium|low"
    rationale: "..."
```

---

## 🎬 Quick Start Commands

### Claude Code / Claude
```
Load 9SENS-micro from /path/to/9SENS-micro/CLAUDE.md
Analyze: [your business idea]
```

### GitHub Copilot
```
// Run 9SENS-micro analysis on: [your business idea]
```

### ChatGPT / Perplexity
```
[Paste CLAUDE.md content]
Then: Analyze this business idea: [your idea]
```

---

## 🔗 File Navigation

| What You Need | Where to Find It |
|---------------|------------------|
| Persona details | `personas.md` |
| Phase workflows | `phases.md` |
| AI instructions | `CLAUDE.md` |
| Getting started | `README.md` |
| Example output | `deliverables/2025-11-08 - EXAMPLE Pet Snake Subscription Box/` |
| Research templates | `templates/research-prompts.md` |
| GO/NO-GO scorecard | `templates/go-nogo-scorecard.md` |

---

## ⏱️ Time & Cost Estimates

| Phase | Duration | Cost (with paid AI) |
|-------|----------|---------------------|
| Research | 2-4 hours | $20-50 |
| Analysis | 1-2 hours | $10-20 |
| **Total** | **3-6 hours** | **$30-70** |

**Free option**: Use ChatGPT or manual research (0 cost, +2 hours time)

---

## 🎯 Success Metrics

After analysis, you should have:

- ✅ Clear GO/NO-GO/PIVOT recommendation
- ✅ 3-5 critical assumptions to validate
- ✅ Data-driven financial model (CAC, LTV, margins)
- ✅ Strategic positioning (red ocean vs blue ocean)
- ✅ Specific next steps (with timeline)

**If you don't have these, re-run analysis with more specific input.**

---

## 🆘 Troubleshooting

| Problem | Solution |
|---------|----------|
| Low confidence scores (<0.75) | Need better sources, more research time |
| Personas contradict | Good! Synthesis resolves. If irresolvable, it's a red flag. |
| Can't find data | BILL flags this. It's a signal (not a bug). |
| Negative expected value | NASH flags. Either fix assumptions or pivot to better opportunity. |
| No clear moat | STEVE flags. Find blue ocean or don't build. |

---

## 📈 When to Upgrade to Full 9SENS

**You should upgrade if**:
- ✅ 9SENS-micro caught issues (it works!)
- ✅ You need adversarial validation (4-persona gate saves $$$)
- ✅ You want Design → Build → Test phases
- ✅ You need automated decision logging
- ✅ You're building multiple products (ROI compounds)

**Full framework adds**:
- 4 more personas (SILAS, LARRY, DAVID, ONE)
- Adversarial gate (DARO, BOŻENKA, ASHY-SLASHY, EMKA)
- 4 more phases (Design, Build, Test, Reflect)
- Automated quality gates + decision logging
- Integration with Prolog, Pytest, etc.

**ROI**: Pays for itself if it prevents ONE bad decision.

---

**Keep this card handy when running 9SENS-micro analyses.**

**Print it. Pin it. Reference it constantly.**

**🚀 Good luck!**
