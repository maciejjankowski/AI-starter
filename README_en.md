# 9SENS-micro: Simplified Multi-Persona Business Analysis Framework

**Version**: 1.0.0
**Purpose**: Showcase the power of multi-perspective AI analysis
**Use Case**: Validate business ideas, market opportunities, strategic decisions

---

## What Is This?

9SENS-micro is a **simplified version** of the full 9SENS framework, designed to demonstrate the value of multi-persona analysis without overwhelming complexity.

**What you get**:
- 3 AI personas (BILL, NASH, STEVE) with distinct analytical lenses
- 2-phase workflow (Research → Analysis)
- Structured, actionable deliverables
- Professional-grade business intelligence

**What you DON'T get** (available in full 9SENS):
- 4 additional personas (7 total in full framework)
- Adversarial validation gate (catches 80%+ of fatal flaws)
- Design, Build, Test, Reflect phases
- Automated decision logging and quality gates
- Integration with external tools (Prolog, Pytest, etc.)

**Think of 9SENS-micro as**: Test drive before buying the car

---

## Quick Start (5 Minutes)

### For Claude Code Users

1. **Copy this folder** to your project directory
2. **Open Claude Code** in your IDE
3. **Paste this command**:
   ```
   Load the 9SENS-micro framework from /path/to/9SENS-micro/CLAUDE.md
   ```
4. **Give it a business idea**:
   ```
   Analyze this idea: [Your business concept in detail]
   ```
5. **Get comprehensive analysis** in `deliverables/YYYY-MM-DD - [TOPIC]/`

### For GitHub Copilot Users

1. **Copy this folder** to your project root
2. **Copilot will auto-load** `copilot-instructions.md`
3. **In your code editor**, write a comment:
   ```
   // Analyze business idea: [Your concept here]
   ```
4. **Copilot will execute** the 9SENS-micro analysis

### For Other AI Tools (ChatGPT, Perplexity, etc.)

1. **Copy content** of `CLAUDE.md` into chat
2. **Paste your business idea**
3. **AI will follow** the 9SENS-micro framework
4. **Manually save outputs** to `deliverables/YYYY-MM-DD - [TOPIC]/`

---

## How It Works

### Three Personas Analyze Your Idea

**BILL** (Data-Driven Truth Engine):
- Validates market data
- Exposes contradictions
- Identifies patterns
- No BS, pure facts

**NASH** (Decision Optimizer):
- Calculates expected values
- Maps decision trees
- Analyzes opportunity costs
- Optimizes resource allocation

**STEVE** (Strategic Advisor):
- Assesses market positioning
- Identifies blue ocean opportunities
- Evaluates timing and moat
- Provides strategic direction

### Two-Phase Process

**Phase 1: RESEARCH** (2-4 hours)
- Gather data across 5 topics: Market, Competitors, Technical, User, Financial
- Validate sources and confidence
- BILL synthesizes findings

**Phase 2: ANALYSIS** (1-2 hours)
- BILL analyzes data and patterns
- NASH optimizes decisions via expected value analysis
- STEVE provides strategic synthesis
- Combined synthesis report with GO/NO-GO recommendation

---

## Example Use Cases

### 1. Validate a Startup Idea
**Input**: "AI-powered meal planning app for busy parents"
**Output**:
- Market size, growth rate, competition
- Unit economics (CAC, LTV, pricing)
- Strategic positioning and differentiation
- GO/NO-GO recommendation with rationale

### 2. Assess a Market Opportunity
**Input**: "Should we enter the European market?"
**Output**:
- Market analysis (TAM/SAM/SOM, trends)
- Competitive landscape and gaps
- Financial projections and ROI
- Strategic roadmap and timing

### 3. Evaluate a Strategic Pivot
**Input**: "Should we shift from B2C to B2B model?"
**Output**:
- Market comparison (B2C vs B2B)
- Financial model changes
- Strategic implications and risks
- Recommendation with execution plan

---

## What You'll Get

### Structured Deliverables

All outputs saved to `deliverables/YYYY-MM-DD - [TOPIC]/`

**Research Outputs**:
- `market_research.yaml` - TAM/SAM/SOM, growth, segments
- `competitor_research.yaml` - Players, pricing, gaps
- `technical_research.yaml` - Feasibility, stack, risks
- `user_research.yaml` - Personas, pain points, WTP
- `financial_research.yaml` - Pricing, CAC, LTV, margins
- `research_synthesis.yaml` - BILL's data validation

**Analysis Outputs**:
- `bill_analysis.md` - Data patterns, contradictions, gaps
- `midas_analysis.md` - Financial viability, ROI, risks
- `steve_analysis.md` - Strategic positioning, moat, roadmap
- `synthesis_report.md` - Combined recommendations + GO/NO-GO

### Sample Synthesis Report Structure

```markdown
# Synthesis Report: [Your Idea]

## Executive Summary
[2-3 paragraphs: key findings, GO/NO-GO recommendation]

## Key Insights
1. BILL: [Data-driven insight]
2. NASH: [Expected value insight]
3. STEVE: [Strategic insight]

## Critical Assumptions
[Top 3 assumptions to validate before proceeding]

## Recommendation: GO / NO-GO / PIVOT
[Clear decision with confidence level]

## Next Steps
[Specific, actionable steps if proceeding]
```

---

## Reading the Outputs

### BILL's Analysis = TRUTH CHECK
- **Look for**: Data contradictions, exposed assumptions, patterns
- **Red flags**: Low confidence scores, missing data, contradictions
- **Green lights**: Validated data, clear patterns, high confidence

### NASH's Analysis = OPTIMIZATION CHECK
- **Look for**: Expected values, decision trees, opportunity costs
- **Red flags**: Negative EV, better alternatives exist, high opportunity cost
- **Green lights**: Positive EV, optimal resource allocation, clear decision path

### STEVE's Analysis = STRATEGY CHECK
- **Look for**: Blue ocean opportunities, competitive moat, timing assessment
- **Red flags**: Red ocean (lots of competition), no moat, bad timing
- **Green lights**: Blue ocean, defensible moat, perfect timing

---

## Tips for Best Results

### 1. Be Specific in Your Input
❌ Bad: "Analyze a food delivery app"
✅ Good: "Analyze a ghost kitchen marketplace for home chefs in Poland, targeting busy families willing to pay 25% premium for home-cooked meals"

### 2. Provide Context When Available
Include:
- Target market (geography, demographics)
- Unique value proposition
- Initial assumptions (pricing, CAC estimates, etc.)
- Specific questions you want answered

### 3. Validate Critical Assumptions
After getting analysis:
1. Note assumptions flagged by BILL
2. Run small experiments to test them
3. Update decision tree per NASH
4. Adjust strategy per STEVE

### 4. Use Iteratively
- Run analysis on v1 of idea
- Get feedback, pivot
- Run analysis on v2
- Compare recommendations

---

## Limitations & Scope

### What 9SENS-micro Does

✅ **Market validation** - Size, growth, trends, segments
✅ **Competitive analysis** - Players, pricing, gaps, differentiation
✅ **Technical feasibility** - Complexity, build time, stack
✅ **User research** - Personas, pain points, willingness to pay
✅ **Financial modeling** - CAC, LTV, margins, breakeven, ROI
✅ **Strategic positioning** - Blue ocean, moat, timing, roadmap

### What 9SENS-micro Doesn't Do

❌ **Design & Architecture** - Tech stack decisions, system design
❌ **Implementation** - Code generation, build execution
❌ **Testing & Validation** - Automated testing, assumption validation
❌ **Reflection & Learning** - Pattern extraction, continuous improvement
❌ **Adversarial Validation** - 4-persona gate that catches fatal flaws
❌ **Decision Logging** - Automated audit trail of all decisions
❌ **Integration** - Prolog logic validation, Pytest integration, etc.

**For full capabilities**: Upgrade to complete 9SENS framework

---

## Upgrading to Full 9SENS

### What You Get in Full Framework

**4 More Personas**:
- SILAS (Counter-Intel Analyst) - Exposes propaganda and systemic issues
- LARRY (Boundary Violator) - Breakthrough via absurdity
- DAVID (Promethean Catalyst) - Democratizes power via tools
- ONE (Infinite Compassion) - Wisdom and ethical analysis

**Adversarial Validation Gate**:
- DARO (Short Seller) - Attacks business viability
- BOŻENKA (Auditor) - Demands evidence for every claim
- ASHY-SLASHY (BS Chainsaw) - Cuts through complexity
- EMKA (Empathy) - Validates problem intensity
- **Proven value**: Saved $200K on Smart Fleet project (caught 6 fatal issues)

**4 Additional Phases**:
- P2: Design & Architecture (system design, tech stack validation)
- P3: Implementation (code generation, TDD, integration)
- P4: Testing & Validation (automated testing, assumption experiments)
- P5: Reflection & Learning (pattern extraction, continuous improvement)

**Advanced Features**:
- Automated decision logging (audit trail)
- Integration with Prolog (logic validation)
- Integration with Pytest/Pyright (code quality)
- DRAF research methodology (90% token optimization)
- Real-time quality gates
- Budget tracking and optimization

**ROI**: Full framework pays for itself if it prevents ONE bad decision.

---

## Frequently Asked Questions

### Q: How long does an analysis take?
**A**: 3-6 hours total (2-4 hours research, 1-2 hours analysis). Can be faster with AI tools like Perplexity Pro.

### Q: How much does it cost?
**A**: $30-70 if using paid AI tools (Perplexity Pro, Claude API). Free if using ChatGPT or manual research.

### Q: Can I use this for any business idea?
**A**: Yes! Works for startups, market entries, strategic pivots, product launches, partnership evaluations, etc.

### Q: What if personas contradict each other?
**A**: That's the point! Contradictions reveal blind spots. The synthesis report resolves conflicts with data-driven recommendations.

### Q: Do I need technical knowledge?
**A**: No. The framework is designed for founders, PMs, strategists, consultants - technical details are handled by the AI.

### Q: Can I customize the personas?
**A**: In 9SENS-micro, no. In full 9SENS, yes - you can create custom personas for specific domains.

### Q: How is this different from just using ChatGPT?
**A**: ChatGPT gives one perspective. 9SENS-micro gives THREE distinct perspectives, each with specialized expertise, plus structured deliverables and quality gates.

---

## File Structure Reference

```
9SENS-micro/
├── README.md                  ← You are here
├── CLAUDE.md                  ← AI agent instructions
├── copilot-instructions.md    ← GitHub Copilot config (same as CLAUDE.md)
├── personas.md                ← BILL, NASH, STEVE definitions
├── phases.md                  ← Research & Analysis workflows
└── deliverables/              ← Your analysis outputs go here
    └── YYYY-MM-DD - TOPIC/
        ├── research/
        │   ├── market_research.yaml
        │   ├── competitor_research.yaml
        │   ├── technical_research.yaml
        │   ├── user_research.yaml
        │   ├── financial_research.yaml
        │   └── research_synthesis.yaml
        └── analysis/
            ├── bill_analysis.md
            ├── nash_analysis.md
            ├── steve_analysis.md
            └── synthesis_report.md
```

---

## Support & Contact

### Getting Help

1. **Read the docs**: Start with `personas.md` and `phases.md`
2. **Check examples**: See `deliverables/` for sample outputs
3. **Ask AI**: Load `CLAUDE.md` into Claude and ask questions about the framework

### Reporting Issues

If you find bugs or have suggestions:
1. Check if it's a limitation by design (see "Limitations" section)
2. Document the issue with example input/output
3. Contact framework provider with details

### Upgrading to Full 9SENS

Interested in the complete framework?
- Contact: [Your contact info]
- Include: Brief description of your use case
- We'll schedule a demo and discuss pricing

---

## License & Attribution

**License**: MIT (for 9SENS-micro simplified version)
**Attribution**: When using outputs commercially, please credit "9SENS-micro framework"
**Full Framework**: Separate licensing and pricing

---

## Quick Command Reference

### Claude Code
```
Load 9SENS-micro from /path/to/9SENS-micro/CLAUDE.md
Analyze business idea: [your idea here]
```

### GitHub Copilot
```
// Run 9SENS-micro analysis on: [your idea here]
```

### ChatGPT / Claude / Perplexity
```
[Paste CLAUDE.md content]

Then:

Analyze this business idea: [your idea here]
```

---

## What's Next?

**Step 1**: Test it on a real business idea
**Step 2**: Review the deliverables
**Step 3**: Validate critical assumptions
**Step 4**: Execute or kill based on data

**If 9SENS-micro saves you from one bad decision, it's paid for itself 100x over.**

**If you want to go deeper**, consider upgrading to full 9SENS with 7 personas, adversarial validation, and 6 complete phases.

---

**Ready to start? Load `CLAUDE.md` into your AI tool and give it a business idea to analyze.**

**Questions? Read `personas.md` and `phases.md` for detailed explanations.**

**Good luck! May your ideas be validated (or invalidated) with data. 🚀**
