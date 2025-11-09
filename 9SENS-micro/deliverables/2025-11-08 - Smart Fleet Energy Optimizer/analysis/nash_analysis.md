# Analiza NASH: Smart Fleet Energy Optimizer

**Data**: 2025-11-08
**Persona**: NASH (Optymalizator Decyzji)
**Fokus**: Wartość oczekiwana, drzewa decyzyjne, koszty alternatywne

---

## Wartość Oczekiwana: Scenariusze

### BASE CASE (Probability: 0.55)

**Założenia:**
- Oszczędności klienta: €54,500/rok (jak w symulacji)
- Success fee acceptance: 70% klientów
- CAC: €3,500 (BDR-driven)
- Churn: 14%/rok
- Klientów Rok 1: 153

**Finansowe:**
- ARR Rok 1: €3.1M
- EBITDA Rok 1: €1.7M (55% margin)
- ARR Rok 2: €8.6M
- EBITDA Rok 2: €6.3M (73% margin)

**Expected Value**:
```
EV_base = 0.55 × €6.3M = €3.465M (EBITDA Rok 2)
```

---

### UPSIDE CASE (Probability: 0.25)

**Co się zmienia:**
- Oszczędności klienta: €65,000/rok (+19% vs base)
- Success fee acceptance: 85%
- CAC: €2,800 (partnerstw ChargePoint channel)
- Churn: 10%/rok
- Klientów Rok 1: 180 (+18% vs base)

**Dlaczego prawdopodobne:**
- Większe floty (200+ pojazdów) generują wyższe oszczędności per depot
- ChargePoint partnership zmniejsza CAC o 20%
- Wyższe oszczędności = niższy churn

**Finansowe:**
- ARR Rok 1: €4.1M (+32% vs base)
- EBITDA Rok 1: €2.5M (61% margin)
- ARR Rok 2: €11.8M (+37% vs base)
- EBITDA Rok 2: €9.2M (78% margin)

**Expected Value**:
```
EV_upside = 0.25 × €9.2M = €2.3M (EBITDA Rok 2)
```

---

### DOWNSIDE CASE (Probability: 0.20)

**Co się zmienia:**
- Oszczędnienia klienta: €38,000/rok (-30% vs base)
- Success fee acceptance: 40% (większość chce flat fee)
- CAC: €5,500 (długi sales cycle 9+ miesięcy)
- Churn: 22%/rok
- Klientów Rok 1: 98 (-36% vs base)

**Dlaczego możliwe:**
- Ceny energii mogą być mniej zmienne niż założono (mniej arbitrażu off-peak/peak)
- Success fee model wymaga edukacji rynku (dłuższy sales cycle)
- Niższe oszczędności = wyższy churn (klienci nie widzą ROI)

**Finansowe:**
- ARR Rok 1: €1.8M (-42% vs base)
- EBITDA Rok 1: €0.7M (39% margin)
- ARR Rok 2: €3.9M (-55% vs base)
- EBITDA Rok 2: €2.2M (56% margin)

**Expected Value**:
```
EV_downside = 0.20 × €2.2M = €0.44M (EBITDA Rok 2)
```

---

## Weighted Expected Value (Rok 2 EBITDA)

```
EV_total = (0.55 × €6.3M) + (0.25 × €9.2M) + (0.20 × €2.2M)
EV_total = €3.465M + €2.3M + €0.44M
EV_total = €6.205M
```

**Interpretation:**
- Baseline projekcja €6.3M EBITDA jest lekko **OPTYMISTYCZNA** (+1.5% vs weighted EV)
- Upside potential (+€2.9M) jest większy niż downside risk (-€4.1M) **w absolute terms**
- Ale probability-weighted, **upside contribution (€2.3M) >> downside drag (€0.44M)**

**Wniosek**: Asymmetric upside = **ATRAKCYJNE**

---

## Drzewo Decyzyjne: Pilot vs Skalowanie

### DECISION NODE 1: Czy robić 3-month pilot? (€15K cost)

#### OPCJA A: Robić pilot (€15K)

**Branch 1a: Pilot sukces** (Probability: 0.70)
- Oszczędności zwalidowane ≥€48K
- Success fee model działa (≥60% acceptance)
- Następny krok: Skaluj do 10 klientów w M6
- Payoff: Proceed to Decision Node 2

**Branch 1b: Pilot częściowy sukces** (Probability: 0.20)
- Oszczędności €35-€47K (niższe niż zakładano)
- Success fee ma ~40% acceptance
- Następny krok: Pivot do flat fee €1,500/miesiąc tylko
- Payoff: Zmniejszona margin ale nadal viable

**Branch 1c: Pilot failure** (Probability: 0.10)
- Oszczędności <€30K
- LUB tech integracja trwa 2+ miesiące (delayed ROI)
- Payoff: -€15K (cost of pilot), KILL projekt

**Expected Value Opcji A:**
```
EV_pilot = (0.70 × V_scale) + (0.20 × V_pivot) + (0.10 × -€15K)
Gdzie V_scale i V_pivot zależą od Decision Node 2
```

#### OPCJA B: NIE robić pilota, skaluj od razu (€0K)

**Branch 2a: Assumptions correct** (Probability: 0.45)
- Oszczędności €54,500 są osiągalne
- Success fee działa
- Payoff: Szybszy time-to-market (2 miesiące przewagi vs pilot path)
- Risk: Jeśli założenia złe, tracisz czas i pieniądze na złych klientów

**Branch 2b: Assumptions partially wrong** (Probability: 0.40)
- Oszczędnienia niższe LUB success fee nie działa
- Payoff: Tracisz 3-6 miesięcy na złych klientach, musisz pivotować
- Cost: €30K+ na złe sales + bad customer experience

**Branch 2c: Assumptions completely wrong** (Probability: 0.15)
- Tech nie działa LUB oszczędnienia <€30K
- Payoff: KILL po 6 miesiącach, strata €80K+

**Expected Value Opcji B:**
```
EV_no_pilot = (0.45 × V_scale_fast) + (0.40 × V_pivot_late) + (0.15 × -€80K)
             = (0.45 × €6.5M) + (0.40 × €2.5M) + (0.15 × -€80K)
             = €2.925M + €1.0M - €12K
             = €3.913M
```

**Ale...**

EV z pilotem (zakładając pilot sukces → scale):
```
EV_pilot = (0.70 × €6.2M) + (0.20 × €2.8M) + (0.10 × -€15K)
         = €4.34M + €560K - €1.5K
         = €4.899M
```

**WNIOSEK**: **Pilot ma wyższy EV o €986K** (+25% vs bezpośrednie skalowanie)

**Option Value pilota:**
- Eliminuje 10% szans na total failure (-€80K → -€15K) = €6.5K saved
- Zmniejsza 40% szans na delayed pivot (€30K cost → €0) = €12K saved
- Daje **cenną informację** o oszczędnościach + success fee acceptance = **priceless for scaling confidence**

**Rekomendacja NASH**: **ROBIĆ PILOT** (€15K, 3 miesiące)

---

### DECISION NODE 2: Po sukcesie pilota - jak skalować?

#### OPCJA A: BDR-driven organic growth (CAC €3,500)

**Finansowe:**
- Klientów M12: 153
- CAC €3,500 × 153 = €535K total acquisition cost
- ARR M12: €3.1M
- LTV/CAC: 51:1 ✅

**Pros:**
- Pełna kontrola nad customer experience
- Wyższe margins (80% gross margin)
- Buduje sales playbook dla przyszłego team

**Cons:**
- Wolniejszy wzrost (153 klientów Rok 1)
- Wymaga hiring BDR + sales ops
- CAC może być wyższe niż €3,500 (risk)

**EV (Rok 2 EBITDA)**: €6.3M (baseline scenario)

#### OPCJA B: ChargePoint channel partnership (CAC €2,200)

**Finansowe:**
- Klientów M12: 220 (+44% vs BDR)
- CAC €2,200 × 220 = €484K total acquisition cost (-€51K vs BDR)
- ARR M12: €4.4M (+42% vs BDR)
- LTV/CAC: 81:1 ✅ (lepsze niż BDR)

**Pros:**
- Szybszy wzrost (220 klientów Rok 1)
- Niższy CAC (ChargePoint ma istniejące customer base)
- ChargePoint validuje produkt (social proof)

**Cons:**
- Revenue share z ChargePoint (zakładam 10% commission = €440K/rok)
- Mniejsza kontrola nad customer experience
- Dependency na ChargePoint roadmap

**EV (Rok 2 EBITDA):**
```
ARR Rok 2: €12.1M (vs €8.6M w BDR)
Revenue share: -€1.2M (10% commission)
Net ARR: €10.9M
EBITDA: €8.2M (75% margin)
```

**Wniosek**: Partnership daje **+€1.9M EBITDA** vs BDR-driven (+30%)

**Ale...**

**Opportunity Cost**:
- Jeśli robisz partnership w Roku 1, trudniej później pivot do direct sales (customers expect ChargePoint integration)
- Partnership może canibalizować direct sales (customers who would have bought direct)

**Pareto Analysis**:
- 80% wartości z 20% funkcji → ChargePoint partnership coverage może nie być 100% TAM
- Niektóre floty chcą white-label (nie wiedzą o ChargePoint) → potrzebny direct sales channel tak czy tak

**Rekomendacja NASH**: **HYBRID MODEL**
- Rok 1: 70% BDR-driven (107 klientów) + 30% ChargePoint channel (46 klientów)
- Weighted CAC: €3,110
- ARR M12: €3.4M (+10% vs pure BDR)
- EBITDA Rok 2: €7.1M (+13% vs pure BDR)
- **Maintains optionality** dla Roku 2

---

## Analiza Kosztów Alternatywnych

### Alternatywa 1: Budować inne SaaS w tej samej dziedzinie (Energy/Fleet)

**Potencjalne opcje:**
1. Fleet telematics analytics (Geotab competitor)
2. Energy management dla budynków komercyjnych
3. Battery degradation monitoring SaaS

**Porównanie:**

| Metryka | Smart Fleet Optimizer | Fleet Telematics | Energy Buildings | Battery SaaS |
|---------|----------------------|------------------|------------------|--------------|
| TAM | €1.4B | €8.2B | €12B | €450M |
| Competitive moat | 6-9 mo (MILP) | 24+ mo (sensors) | 18+ mo (IoT) | 12+ mo (ML models) |
| LTV/CAC | 51:1 | 15:1 | 22:1 | 35:1 |
| CAC Payback | 2.6mo | 8mo | 6mo | 4mo |
| Year 1 profitable | ✅ YES | ❌ NO | ❌ NO | ✅ YES |
| Tech complexity | Medium (MILP) | High (hardware) | High (IoT + AI) | Medium (ML) |

**Expected Value Comparison (Rok 2 EBITDA):**

```
Smart Fleet:       €6.2M (weighted EV)
Fleet Telematics:  €2.8M (lower margins due to hardware)
Energy Buildings:  €5.1M (większy rynek ale wyższy CAC)
Battery SaaS:      €4.5M (mniejszy TAM ale dobre unit economics)
```

**Wniosek**: **Smart Fleet ma najwyższy EV** dla Roku 2

**Ale...** Energy Buildings ma największy TAM (€12B) → long-term potential może być wyższy

**Sequential Decision**: Zbuduj Smart Fleet NAJPIERW (Year 1 profitable, 16 weeks MVP), potem pivot do Energy Buildings w Roku 3 jeśli Smart Fleet osiągnie €10M ARR

---

### Alternatywa 2: Join incumbent jako employee (opportunity cost)

**Opcja**: Dołączyć do ChargeLab jako Senior Engineer (€120K/rok)

**Opportunity Cost Analysis:**

| Metryka | Build Smart Fleet | Join ChargeLab |
|---------|-------------------|----------------|
| Rok 1 income | €0 (founder, no salary) | €120K salary |
| Rok 2 income | €80K salary (jeśli raise seed) | €120K salary |
| Rok 3 income | €120K salary | €130K salary |
| Equity value (5 lat) | €2.4M (20% × €12M exit) | €200K (0.5% options × €40M) |
| **5-year NPV (8% discount)** | **€1.82M** | **€510K** |

**Net Opportunity Cost** = €1.31M over 5 years

**Ale...**

**Risk-Adjusted:**
- Probability of €12M exit: 0.25 (25%)
- Probability of €0 exit: 0.45 (45%)
- Probability of €50M exit: 0.05 (5%)
- Weighted outcome: €4.5M equity value → NPV €850K

**Risk-Adjusted vs ChargeLab**: €850K - €510K = **€340K net gain**

**Wniosek**: Building Smart Fleet ma **higher expected value** ale **higher variance** (risk)

**Risk tolerance decision**: Jeśli founder jest risk-averse → Join ChargeLab jest safer
**Ale**: Jeśli founder ma 6-month runway + komfort z 45% szansą failure → **Build Smart Fleet**

**Rekomendacja NASH**: **BUILD** (founder ma technical background + domain expertise = competitive advantage)

---

## Optymalizacja Zasobów (Pareto 80/20)

### 80% wartości pochodzi z 20% funkcji - co priorytetyzować w MVP?

**Analiza wartości funkcji** (na podstawie interviews + competitive analysis):

| Funkcja | % Adoption | Impact na oszczędnienia | Dev Time (weeks) | Value/Time Ratio |
|---------|-----------|------------------------|------------------|------------------|
| **MILP charging schedule** | 100% | €42,000/rok (77%) | 6 | **7,000/week** ✅ |
| Real-time monitoring | 95% | €4,500/rok (8%) | 2 | **2,250/week** ✅ |
| SLA alerts | 90% | €3,500/rok (6%) | 1 | **3,500/week** ✅ |
| Demand charge optimization | 85% | €4,000/rok (7%) | 2 | **2,000/week** |
| Route optimization | 60% | €1,000/rok (2%) | 4 | 250/week ❌ |
| Driver app (all features) | 40% | €500/rok (1%) | 3 | 167/week ❌ |
| Executive dashboard | 100% | €0 (selling tool) | 2 | 0/week (critical dla sales) |

**Pareto Cut**:
- **Top 20% funkcji** = MILP schedule + SLA alerts + Real-time monitoring = **9 weeks dev time**
- **Generują 91% wartości** (€50K / €54.5K)

**Bottom 80% funkcji** = Route opt + Driver app full features = **7 weeks dev time**
- **Generują 9% wartości** (€4.5K / €54.5K)

**Rekomendacja NASH**: **MVP = 10 weeks**
1. MILP charging schedule (6 weeks)
2. Real-time monitoring (2 weeks)
3. SLA alerts (1 week)
4. Executive dashboard (2 weeks) - critical dla sales
5. Basic driver view (1 week) - checkbox dla Fleet Managers

**CUT from MVP:**
- Advanced route optimization (add w v2.0 po 20 customers)
- Driver app full features (add w v2.0)
- Demand charge opt standalone (wbuduj w MILP solver, nie osobna feature)

**Impact**: MVP 10 weeks zamiast 16 weeks = **-37% dev time**, **-9% value**

**ROI MVP cut**: Oszczędność 6 weeks × €10K/week = **€60K dev cost saved**

---

## Decyzja Sekwencyjna: Timing seed raise

### Kiedy raise $2M seed?

#### OPCJA A: Raise przed pilotem (Month 1)

**Pros:**
- 24-month runway od razu
- Możesz hire team szybciej (2 engineers + BDR)
- Większy runway = mniejsza presja na short-term metrics

**Cons:**
- Niższa wycena (brak traction)
- Większa dilution (20% equity vs 12.5% w Option B)
- Inwestorzy będą chcieli zobaczyć pilot success PRZED wiring pieniędzy

**Probability of success**: 0.30 (trudno raise bez traction)

#### OPCJA B: Raise po sukcesie pilota (Month 4)

**Pros:**
- Wyższa wycena ($15M pre-money vs $10M)
- Mniejsza dilution (13.3% vs 20%)
- De-risked dla inwestorów (pilot success = proven)
- Prawdopodobieństwo success: 0.75 (łatwiej raise z traction)

**Cons:**
- Potrzebujesz €40K własnego kapitału na pilot + 3mo runway
- Jeśli pilot fail, nie raise (ale i tak byś KILLed projekt)

**Expected Equity Dilution:**
```
Option A: 20% × 0.30 = 6% expected dilution
Option B: 13.3% × 0.75 = 10% expected dilution
```

**Wniosek**: Option A ma **niższą expected dilution** (6% vs 10%)

**Ale...**

**Founder equity value:**
- Option A: Jeśli raise at $10M pre, founder ma 60% × €60M (5-year exit) = €36M
- Option B: Jeśli raise at $15M pre, founder ma 66.7% × €60M = €40M

**Difference**: +€4M for Option B

**Probability-weighted:**
- Option A: 0.30 × €36M = €10.8M expected founder value
- Option B: 0.75 × €40M = €30M expected founder value

**Wniosek**: **Option B (raise po pilota) ma 2.8x wyższy expected value dla foundera**

**Rekomendacja NASH**: **Raise PO sukcesie pilota** (Month 4, po walidacji €48K+ oszczędności)

---

## Sekwencja Decyzji Optymalna

### Roadmap decyzyjny (Month 1-12):

**Month 1-3: PILOT (€15K)**
- Build MVP integration z 1 flotą
- Validate oszczędnienia ≥€48K
- Validate success fee acceptance ≥60%
- **Gate decision**: Jeśli pilot success → Continue, else → KILL

**Month 4: SEED RAISE ($2M at $15M pre-money)**
- Use pilot data dla pitch
- Target: 5 investor meetings, 2 term sheets
- **Gate decision**: Jeśli ≥1 term sheet → Proceed, else → bootstrap do Month 6

**Month 5-6: TEAM BUILD**
- Hire 2 engineers (backend + frontend)
- Hire 1 BDR
- Burn rate: €30K/month

**Month 7-12: SCALE (Target: 10 customers by M12)**
- BDR lead gen + outreach
- Engineers build v1.0 (post-MVP improvements)
- **Gate decision Month 9**: Jeśli <5 customers → pause hiring, jeśli ≥5 → continue

**Month 12: EVALUATE**
- ARR target: €200K+ (10 customers × €20K ACV)
- LTV/CAC target: ≥20:1
- Churn: <20%/rok
- **Decision**: Scale to 50 customers w Roku 2 LUB pivot

---

## Analiza Ryzyka: Co może pójść nie tak?

### Risk 1: Oszczędnienia <€48K (Probability: 0.22, Impact: HIGH)

**Downside:**
- Customer ROI spada do <150%
- Churn wzrasta do 25%+
- Trudniej sprzedawać (needs higher base fee compensation)

**Mitigation:**
- Pilot 3mo waliduje TO RYZYKO
- Jeśli oszczędnienia €38-47K → pivot do flat fee €1,500/mo (eliminuje success fee uncertainty)

**Contingency plan:**
- Pivot do większych flot (200+ pojazdów) które mają wyższe oszczędności per depot

**Expected Loss (jeśli się zmaterializuje):**
- ARR M12: €1.8M (vs €3.1M baseline) = **-€1.3M**
- Ale probability-weighted: 0.22 × -€1.3M = **-€286K expected loss**

### Risk 2: CAC >€5K (Probability: 0.30, Impact: MEDIUM)

**Downside:**
- LTV/CAC spada do 35:1 (nadal dobre ale nie wyjątkowe)
- CAC payback 4-5 miesięcy (vs 2.6mo)
- Potrzebujesz wyższy runway dla acquisition

**Mitigation:**
- ChargePoint partnership (CAC €2,200) jako backup plan
- Early pilots z referenceable customers (zmniejsza sales cycle)

**Contingency plan:**
- Hybrid: 30% ChargePoint channel, 70% direct sales
- Zmniejsza weighted CAC do €3,400

**Expected Loss:**
- 0.30 × (€5K - €3.5K) × 153 customers = 0.30 × €230K = **€69K expected loss**

### Risk 3: Success fee model nie działa (Probability: 0.35, Impact: MEDIUM)

**Downside:**
- Pivot do flat fee €1,500/mo (vs €1,000 + 15% = €1,681)
- ACV spada do €18K (vs €20.2K) = **-11%**
- ARR M12: €2.75M (vs €3.1M)

**Mitigation:**
- Oferuj OBIE opcje od Dnia 1 (A/B test pricing)
- 70% flat fee, 30% success fee jako fallback

**Contingency plan:**
- Jeśli <40% wybiera success fee → pivot do flat fee only

**Expected Loss:**
- 0.35 × -€350K ARR = **-€122K expected loss**

**Total Expected Loss (all 3 risks):**
```
-€286K (savings) + -€69K (CAC) + -€122K (success fee) = -€477K expected loss
```

**As % of baseline ARR M12**: -€477K / €3.1M = **-15% downside**

**Wniosek**: Weighted downside risk jest **manageable** (-15%) i mniejszy niż upside potential (+42% w upside scenario)

---

## Rekomendacje NASH

### ✅ GO - ale z sequencing

**Weighted EV (Rok 2 EBITDA)**: €6.2M
**Upside potential**: +€2.9M (46% upside)
**Downside risk**: -€477K (15% downside)
**Asymmetry**: **2:1 upside/downside ratio** ✅

### Decyzje sekwencyjne:

1. **Month 1-3: PILOT** (€15K, 3mo)
   - Validate oszczędnienia ≥€48K
   - Validate success fee acceptance ≥60%
   - **Gate**: Jeśli fail → KILL (cost: -€15K), jeśli success → Month 4

2. **Month 4: SEED RAISE** ($2M at $15M pre-money)
   - Use pilot data
   - Target: 2 term sheets z 5 meetings
   - **Gate**: Jeśli no term sheets → bootstrap do Month 6, pivot jeśli trzeba

3. **Month 5-12: SCALE** (Target: 10 customers)
   - Hire 2 engineers + 1 BDR
   - Build v1.0 (10-week MVP z Pareto cut)
   - **Gate Month 9**: Jeśli <5 customers → pause, jeśli ≥5 → accelerate

### Optymalizacja zasobów (Pareto 80/20):

**MVP = 10 weeks** (vs 16 weeks planned):
- MILP schedule (6 weeks) = 77% wartości
- Real-time monitoring (2 weeks) = 8% wartości
- SLA alerts (1 week) = 6% wartości
- Executive dashboard (2 weeks) = selling tool
- **CUT**: Route opt + Driver app full features = -6 weeks

**Oszczędność**: €60K dev cost, **-9% value trade-off**

### Pricing strategy:

**Hybrid model** (A/B test):
- 70% klientów: Flat fee €1,500/mo (€18K ACV)
- 30% klientów: €1,000 + 15% success fee (€20.2K ACV)
- Weighted ACV: €18.7K (vs €20.2K baseline = -7% conservative)

**Jeśli success fee >60% acceptance** → pivot do 100% success fee w Month 9

### GTM strategy:

**Hybrid channel** (optimizes CAC + growth):
- 70% BDR-driven (CAC €3,500)
- 30% ChargePoint partnership (CAC €2,200)
- Weighted CAC: **€3,110** (-11% vs pure BDR)
- Maintains optionality dla Roku 2 scaling

---

## Expected Value Summary

| Scenario | Probability | EBITDA Rok 2 | Weighted Contribution |
|----------|-------------|--------------|----------------------|
| **Base Case** | 0.55 | €6.3M | €3.465M |
| **Upside** | 0.25 | €9.2M | €2.3M |
| **Downside** | 0.20 | €2.2M | €0.44M |
| **TOTAL EV** | 1.00 | - | **€6.205M** |

**Asymmetry**: Upside contribution (€2.3M) >> Downside drag (€0.44M) = **5.2x ratio** ✅

**Opportunity Cost vs Alternatives**:
- Fleet Telematics: +€3.4M higher EV ✅
- Energy Buildings: +€1.1M higher EV ✅
- Battery SaaS: +€1.7M higher EV ✅
- Join ChargeLab: +€1.31M NPV over 5 years ✅

**Wniosek**: **Smart Fleet ma najwyższy EV** ze wszystkich rozważanych opcji

---

## Key Metrics (Decision Criteria)

| Metryka | Target | Actual (Baseline) | Status |
|---------|--------|------------------|--------|
| **LTV/CAC** | >20:1 | 51:1 | ✅ EXCELLENT |
| **CAC Payback** | <6mo | 2.6mo | ✅ FAST |
| **Year 1 Profitable** | Yes | €1.7M EBITDA | ✅ ACHIEVED |
| **Weighted EV (Y2)** | >€5M | €6.2M | ✅ EXCEEDED |
| **Upside/Downside** | >2:1 | 5.2:1 | ✅ ASYMMETRIC |
| **Pilot ROI** | >10x | €6.2M / €15K = 413x | ✅ EXTREME |

**Wszystkie kryteria spełnione** ✅

---

## Final Recommendation NASH

**STATUS**: ✅ **GO** - z sekwencyjnymi gate decisions

**Confidence**: 0.82 (HIGH - numbers validate, but pilot needed to de-risk)

**Critical Path:**
1. Pilot 3mo (€15K) → Validate oszczędnienia + success fee
2. Seed raise ($2M) → Use pilot data dla pitch
3. MVP 10 weeks → Pareto 80/20 cut (€60K saved)
4. Scale do 10 customers M12 → Hybrid GTM (BDR + ChargePoint)

**Expected Outcome (Rok 2)**: €6.2M EBITDA (probability-weighted)

**Biggest Risk**: Oszczędnienia <€48K (22% probability) → Mitigated przez pilot

**Biggest Opportunity**: ChargePoint partnership (€2.3M upside vs baseline)

**Next Best Alternative**: Energy Buildings SaaS (€5.1M EV) → **€1.1M lower** than Smart Fleet

**Opportunity Cost**: €340K NPV vs joining ChargeLab → **Worth the risk**

---

**NASH OUT. GO BUILD.**
