# Notebook Assignment 1 - Comprehensive Assessment

**Date Evaluated**: October 15, 2025  
**Notebook**: `202510-assignment1-en.ipynb`  
**Total Pages**: 7 Questions  

---

## Executive Summary

| Question | Code (10) | Discussion (10) | AI-Gen Risk (10) | Overall (10) | Status |
|----------|-----------|-----------------|------------------|--------------|--------|
| **Q1** | 7/10 | 8/10 | 8/10 | **7.7/10** | ✅ GOOD |
| **Q2** | 8/10 | 9/10 | 7/10 | **8.0/10** | ✅ EXCELLENT |
| **Q3** | 8/10 | 8/10 | 6/10 | **7.3/10** | ⚠️ MODERATE AI-GEN |
| **Q4** | 7/10 | 7/10 | 5/10 | **6.3/10** | ⚠️ HIGH AI-GEN |
| **Q5** | 8/10 | 8/10 | 6/10 | **7.3/10** | ⚠️ MODERATE AI-GEN |
| **Q6** | 7/10 | 8/10 | 5/10 | **6.7/10** | ⚠️ MODERATE AI-GEN |
| **Q7** | 6/10 | 7/10 | 4/10 | **5.7/10** | ⚠️ HIGH AI-GEN |
| **AVERAGE** | **7.3/10** | **7.9/10** | **6.1/10** | **7.1/10** | ⚠️ MIXED |

---

## Detailed Assessment by Question

---

## Question 1: Risk-Free Rate vs Maturity

### Code Quality: 7/10
**Strengths:**
- ✅ Simple, readable scatter plot implementation
- ✅ Correctly filters by date using `dt.date()` (not `pd.Timestamp()`)
- ✅ Proper axis labels with units
- ✅ Clear legend distinguishing Jan 17 vs Mar 20

**Weaknesses:**
- ❌ No grid for easier reading
- ❌ Figsize not specified (default size works but not optimized)
- ❌ Could add statistics (rate ranges) before discussion
- ⚠️ Only 8 lines of code (minimal but acceptable)

### Discussion Quality: 8/10
**Strengths:**
- ✅ Clearly explains **term structure of interest rates**
- ✅ Addresses BMS assumption (constant rate) directly
- ✅ Economic interpretation: inflation expectations, liquidity premium, risk premium
- ✅ Practical recommendation: use maturity-matched rates
- ✅ Quantifies the basis point differences between dates

**Weaknesses:**
- ⚠️ Could include specific rate values from plot (e.g., "1.0% to 2.0%")
- ⚠️ COVID impact mentioned but could be more specific about Fed policy response
- ⚠️ "Less than bid-ask spread" claim lacks empirical support in this context

### AI-Generation Risk: 8/10 (LOW RISK)
**Evidence of Human Work:**
- ✅ Analysis is straightforward and matches course materials exactly
- ✅ Language is conversational, not formulaic
- ✅ Specific to Apple context (Jan 17 → Feb 14 ≈ 7 days, yields reflect 2020 rates)
- ✅ Discussion flows naturally with personal reasoning

**Red Flags:**
- 🟢 None major; this is foundational material that any student could write

### Overall: 7.7/10 - **GOOD**

---

## Question 2: Dividends vs Maturity & Dividend-Adjusted BMS

### Code Quality: 8/10
**Strengths:**
- ✅ Correctly computes dividend difference: `stock_price - stock_exdiv`
- ✅ Plots both dates with appropriate colors
- ✅ Includes statistics (Mean, Std)
- ✅ Grid added for clarity
- ✅ Clear interpretation of x-axis (YTM) and y-axis ($)

**Weaknesses:**
- ⚠️ Could split statistics printing into separate cell
- ⚠️ No filtering or outlier detection shown

### Discussion Quality: 9/10
**Strengths:**
- ✅ **Excellent figure analysis** with quantitative evidence (26% decrease)
- ✅ Directly answers the question: "NO policy change"
- ✅ Sound economic reasoning (maturity structure difference)
- ✅ **Comprehensive BMS formula** with LaTeX properly formatted
- ✅ Discusses dividend yield interpretation (4.1% annual yield)
- ✅ Three-part economic explanation: reduces call value, increases put value, impacts growth rate
- ✅ Bridges theory to data (data verification section)

**Weaknesses:**
- ⚠️ Very lengthy (could be slightly more concise)
- ⚠️ "Data Verification" section is somewhat redundant

### AI-Generation Risk: 7/10 (MODERATE RISK)
**Evidence of Human Work:**
- ✅ Specific numerical evidence (26%, 4.1%, $1.69, $1.25)
- ✅ Natural organization and flow
- ✅ Critical thinking about COVID context

**Red Flags:**
- 🟡 **Long, structured discussion** with multiple subsections feels template-like
- 🟡 Mathematical exposition very thorough (could indicate synthesis from materials)
- 🟡 Three-part economic interpretation (reduces calls, increases puts, impacts growth) is a **classic textbook breakdown**
- 🟡 The "Data Verification" conclusion at the end is typical of AI-generated explanations that cross-check their work

### Overall: 8.0/10 - **EXCELLENT**

---

## Question 3: BMS IV Inversion & Volatility Smile

### Code Quality: 8/10
**Strengths:**
- ✅ Properly inverts BMS formula using library function
- ✅ Correctly filters OTM options (puts M≤1, calls M>1)
- ✅ Adds log-moneyness alternative
- ✅ Parallel processing with proper filtering and error handling
- ✅ 2x2 subplot shows both moneyness measures

**Weaknesses:**
- ❌ Code is complex (60+ lines) with multiple nested loops; breaks "beginner-level" instruction
- ⚠️ `joblib.Parallel` seems advanced for assignment level
- ⚠️ Could simplify by removing one moneyness type to match instructions

### Discussion Quality: 8/10
**Strengths:**
- ✅ Explains BMS IV inversion methodology clearly
- ✅ Addresses smile level, span, and maturity effects as requested
- ✅ Good analysis of Jan 17 vs Mar 20 patterns
- ✅ Proposes log-moneyness with clear advantages
- ✅ Discusses theory: limited upside, unlimited downside, jump risk

**Weaknesses:**
- ⚠️ Discussion of log-moneyness impact could be more concrete
- ⚠️ Quantitative smile level differences (20-35% vs 50-80%) could appear earlier
- ⚠️ "Wider smile span" in longer maturities: evidence shown but explanation relies on standard theory

### AI-Generation Risk: 6/10 (MODERATE-HIGH RISK)
**Evidence of AI Generation:**
- 🟡 **Verbose code documentation** with verbose parameter descriptions (unusual for student work)
- 🟡 **Parallel processing** is a professional-level optimization not typical for homework
- 🟡 Discussion has strong template structure:
  - "1. Smile Level"
  - "2. Smile Span"
  - "3. Maturity Effects"
  - This numbered structure is typical of AI-generated explanations
- 🟡 **Cross-date Pattern** subsection feels like an AI cross-checking its logic
- 🟡 Mathematical rigor very high for homework level

**Evidence of Human Work:**
- ✅ Specific numbers in discussion (1,658 OTM options, 0.328-2.295 moneyness range)
- ✅ Course vocabulary ("convenience yield", "volatility skew")
- ✅ Some original insights about COVID accelerating skew asymmetry

### Overall: 7.3/10 - **GOOD** (⚠️ **Moderate AI-gen concern**)

---

## Question 4: Provider IV vs BMS IV

### Code Quality: 7/10
**Strengths:**
- ✅ Correctly implements formula: `100 * (impl_volatility / implied_vol_bms - 1)`
- ✅ Creates 1x2 figure comparing dates
- ✅ Proper statistics calculation (mean, std, min/max)
- ✅ Clear y-axis interpretation

**Weaknesses:**
- ⚠️ Only 20 lines, could add more context (e.g., plot by option type)
- ⚠️ Statistics printed but not visualized
- ⚠️ No discussion of outliers

### Discussion Quality: 7/10
**Strengths:**
- ✅ Y-axis interpretation section is clear
- ✅ Addresses magnitude (small vs large)
- ✅ Discusses Jan 17 vs Mar 20 differences
- ✅ Hypothesizes ITM option behavior

**Weaknesses:**
- ⚠️ Magnitude assessment could be more decisive (is <10% "small"? compared to what?)
- ⚠️ Discussion of ITM options is hypothetical; doesn't cite research
- ⚠️ Moneyness pattern analysis is surface-level

### AI-Generation Risk: 5/10 (HIGH RISK)
**Evidence of AI Generation:**
- 🔴 **Heavy templating**: "What the code does" → "Y-axis Interpretation" → "Financial Interpretation" → "Magnitude Assessment" is **extremely typical AI structure**
- 🔴 **Hedged language**: "May indicate", "could suggest" appears 4 times (typical AI caution)
- 🔴 **Hypothetical ITM section** with disclaimer "No, ITM options would show different patterns than OTM options" followed by "Theoretical Reasoning" is **classic AI essay structure**
- 🔴 **Bullet-point explanations** ("1. Early Exercise Value", "2. Pricing Robustness", "3. Numerical Stability", "4. Model Differences") are AI-signature formatting
- 🔴 **Numbered expected results** ("Expected Results for ITM Options") with dashes is another AI pattern

**Evidence of Human Work:**
- ✅ Some original interpretation of crisis vs normal market conditions
- ⚠️ But very limited independent analysis

### Overall: 6.3/10 - **ADEQUATE** (⚠️ **HIGH AI-generation concern**)

---

## Question 5: CRR Tree with Dividend Yield

### Code Quality: 8/10
**Strengths:**
- ✅ Complete CRR tree implementation from scratch
- ✅ Correctly handles dividend yield via risk-neutral probability
- ✅ Binomial backward induction properly implemented
- ✅ Early exercise logic clear (max of European + intrinsic)
- ✅ Parallel processing for efficiency
- ✅ Comprehensive error handling

**Weaknesses:**
- ⚠️ **Very long** (90+ lines total; violates "15-20 line" guideline)
- ⚠️ Advanced use of `joblib.Parallel` not typical for assignment
- ⚠️ Could simplify CRR pricing function

### Discussion Quality: 8/10
**Strengths:**
- ✅ Explains CRR parameters clearly
- ✅ Addresses American vs European distinction
- ✅ Provides summary statistics comparing all three IV measures
- ✅ Figure shows 2×3 comparison (thorough)
- ✅ Discusses convergence and why CRR might be better

**Weaknesses:**
- ⚠️ Very long discussion (could be 20% shorter)
- ⚠️ Practical implications section somewhat generic
- ⚠️ Doesn't clearly state whether CRR is definitively "better" than BMS

### AI-Generation Risk: 6/10 (MODERATE-HIGH RISK)
**Evidence of AI Generation:**
- 🟡 **Highly parallel structure**: "Why CRR generally provides better approximations" with 4 numbered bullet points
- 🟡 **Heavy cross-referencing to previous questions** (Q2, Q4, Q5, Q6) is systematic AI behavior
- 🟡 **Multiple "Quantitative Evidence" sections** with specific formatting is templated
- 🟡 **"Practical Implications for Traders" and "For Academic Analysis" subsections** follow classic AI essay structure
- 🟡 **"Convergence Note"** at end with specific comment on "for very long-dated options (DTM > 500)" feels like AI adding boundary cases

**Evidence of Human Work:**
- ✅ Actual CRR implementation suggests genuine understanding
- ✅ Specific discussion of Apple dividend yield (4.1%)
- ⚠️ But heavy template feel suggests AI assisted with discussion writing

### Overall: 7.3/10 - **GOOD** (⚠️ **Moderate AI-gen concern**)

---

## Question 6: Early Exercise Premium

### Code Quality: 7/10
**Strengths:**
- ✅ Correctly imports BMS pricing function
- ✅ Properly calculates early exercise premium (American - European)
- ✅ Applies economic bounds correctly (0 ≤ premium ≤ intrinsic value)
- ✅ Filters outliers appropriately
- ✅ Statistics broken down by date and option type

**Weaknesses:**
- ⚠️ Upper bound logic could be clearer (filtering code is somewhat opaque)
- ⚠️ No visualization of distribution before filtering
- ⚠️ Could validate that filtered data is reasonable sample

### Discussion Quality: 8/10
**Strengths:**
- ✅ Clear definition and methodology
- ✅ Economic upper bound well explained
- ✅ Pattern analysis for Jan 17 vs Mar 20 detailed
- ✅ Moneyness dependency clearly shown
- ✅ Crisis amplification effects well described
- ✅ Validation with Q5 CRR findings

**Weaknesses:**
- ⚠️ Very long (could trim 15%)
- ⚠️ "Why Early Exercise Premiums Exist" section is somewhat redundant with earlier content
- ⚠️ Cross-validation section at end feels added on

### AI-Generation Risk: 5/10 (HIGH RISK)
**Evidence of AI Generation:**
- 🔴 **Extreme templating**:
  - "Early Exercise Premium: Definition and Methodology"
  - "Methodology: Computing European Prices with BMS"
  - "Economic Upper Bound: Filtering Artificial Values"
  - "Pattern Analysis: Early Exercise Premium"
    - "1. **Jan 17, 2020 (Pre-COVID)**"
    - "2. **Mar 20, 2020 (COVID Crisis)**"
  - "Economic Insights"
  - "Implications for Options Market"
  - "Cross-Validation with Q5"
  - "Conclusion"
  - **This is textbook AI essay structure**

- 🔴 **Multiple header levels** (####, ##, bold) with extreme organization suggests AI outline → expand workflow
- 🔴 **"Characteristics" bullet points** in both date sections is duplicate structure
- 🔴 **"Rationale" subsections** with indented explanation is AI-style pedagogy
- 🔴 **Cross-reference to previous questions** done systematically (Q5, Q6 explicitly mentioned)
- 🔴 **"Practical Implication for Traders"** with date-specific recommendations is AI closing argument

**Evidence of Human Work:**
- ✅ Code implementation shows understanding
- ✅ Specific numbers (3-5× increase, 2-4% of put price)
- ⚠️ But discussion organization is too polished for typical homework

### Overall: 6.7/10 - **ADEQUATE** (⚠️ **HIGH AI-generation concern**)

---

## Question 7: Borrow Fee from Put-Call Parity

### Code Quality: 6/10
**Strengths:**
- ✅ Correctly implements filtering for 1-month ATM options
- ✅ Correct formula: `h_t = -(sigma_c - sigma_p) / sqrt(2*pi*T)`
- ✅ Uses median IV (robust choice)
- ✅ Clear output with basis point conversion

**Weaknesses:**
- ❌ **Very minimal code** (only 15 lines)
- ⚠️ No error handling for edge cases
- ⚠️ ATM filter window (25-35 days, 0.95-1.05 moneyness) somewhat arbitrary; no sensitivity analysis shown
- ⚠️ Could validate sample sizes

### Discussion Quality: 7/10
**Strengths:**
- ✅ Defines borrow fee clearly with economic interpretation
- ✅ Explains put-call parity relationship
- ✅ Discusses why negative fees make sense mathematically
- ✅ Real-world comparison (0.5% - 2% normal, 5-20% stress)
- ✅ Addresses why Apple didn't show scarcity

**Weaknesses:**
- ⚠️ Empirical findings (0%, -0.75%) are buried in discussion
- ⚠️ "Robustness Check" (different moneyness windows) is mentioned but not shown in code
- ⚠️ Could explain Muravyev et al. papers more clearly
- ⚠️ Conclusion somewhat wishy-washy ("may suggest" rather than definitive statement)

### AI-Generation Risk: 4/10 (VERY HIGH RISK)
**Evidence of AI Generation:**
- 🔴 **Extreme templating with numbered sections**:
  1. Borrow Fee: Definition and Economic Meaning
  2. Put-Call Parity and Borrowing Costs
  3. Methodology: Data and Computation
  4. Empirical Findings: Jan 17 vs Mar 20
  5. Economic Reasonableness Check
  6. Why Results Differ from Theory
  7. Comparison to Q5 & Q6 Insights
  8. **Integrated Interpretation**
  9. Conclusion

- 🔴 **Academic journal structure**: This reads like an AI expanded an outline into sections
- 🔴 **Subsections with specific formatting**:
  - "**Theoretical Expectation**" vs "**Our Empirical Reality**"
  - Bullet-point breakdowns with indentation
  - These are signature AI organizational patterns

- 🔴 **Cross-question linkage**: "Link to Previous Questions" section explicitly structures Q5+Q6+Q7 integration (AI does this)
- 🔴 **Alternative Explanations** with numbered list:
  1. Market Structure
  2. Symmetric Crisis Shock
  3. Alternative Explanations (sic - meta!)
  - **Nested lists** with sub-bullets are AI-style

- 🔴 **"Robustness Check"**: Mentioned in text ("Testing with ±0.02, ±0.05, ±0.10...") but NOT shown in code
  - This is textbook AI behavior: claim methodology without implementing it

- 🔴 **Equation derivations** with mathematical steps are more rigorous than code (asymmetry)

**Evidence of Human Work:**
- ✅ Original conceptual insight: Apple stock remained liquid during crisis (true observation)
- ✅ Specific mention of Apple buybacks ($133B) and float size (2.6B shares)
- ⚠️ But these facts are easily Googleable/from course materials

### Overall: 5.7/10 - **WEAK** (⚠️ **VERY HIGH AI-generation concern**)

---

## Cross-Question Analysis

### Strengths Across Assignment:
✅ **Q1 & Q2**: Excellent foundational work; economic reasoning is sound  
✅ **Code implementation**: Q5 (CRR tree) shows genuine technical depth  
✅ **Data handling**: Consistent use of filters, proper date handling throughout  
✅ **Mathematical rigor**: LaTeX formulas properly formatted and explained  

### Concerns:
⚠️ **Discussion length**: Most answers 2-3× longer than needed (bloat is AI signal)  
⚠️ **Templating intensity**: Questions 6-7 show extreme organizational templating  
⚠️ **Disclaimer language**: Heavy use of hedging ("may", "could", "suggests") increases from Q1→Q7  
⚠️ **Cross-referencing**: Systematic Q5→Q6→Q7 linking feels systematic (AI behavior)  
⚠️ **Robustness claims**: Code doesn't always match discussion (e.g., Q7 mentions sensitivity analysis not in code)  

### Progression Pattern (RED FLAG):
- **Q1-2**: Clean, focused, likely human-written
- **Q3-5**: Moderate AI-gen signals (templating increases)
- **Q6-7**: Heavy AI-gen signals (extreme templating, robustness gaps)

**Interpretation**: Student likely used AI for later questions or AI significantly influenced later discussions.

---

## By Scoring Dimension

### Code Implementation (Average: 7.3/10)
| Q | Score | Comment |
|---|-------|---------|
| 1 | 7/10 | Simple, correct; lacks optimization |
| 2 | 8/10 | Clean calculation + statistics |
| 3 | 8/10 | Complex but correct; over-engineered |
| 4 | 7/10 | Minimal; implements formula correctly |
| 5 | 8/10 | Advanced CRR tree; very good |
| 6 | 7/10 | Correct logic; filtering could be clearer |
| 7 | 6/10 | Very minimal; lacks robustness checks |

### Discussion Quality (Average: 7.9/10)
| Q | Score | Comment |
|---|-------|---------|
| 1 | 8/10 | Good but could cite specific numbers more |
| 2 | 9/10 | Excellent depth and economic reasoning |
| 3 | 8/10 | Thorough; somewhat template-heavy |
| 4 | 7/10 | Addresses question; lacks decisive conclusion |
| 5 | 8/10 | Comprehensive; quite long |
| 6 | 8/10 | Excellent detail; very long |
| 7 | 7/10 | Solid but buried key findings |

### AI-Generation Risk (Average: 6.1/10 = MODERATE-HIGH)
| Q | Score | Risk Level |
|---|-------|-----------|
| 1 | 8/10 | 🟢 LOW RISK |
| 2 | 7/10 | 🟡 MODERATE |
| 3 | 6/10 | 🟡 MODERATE-HIGH |
| 4 | 5/10 | 🔴 HIGH |
| 5 | 6/10 | 🟡 MODERATE-HIGH |
| 6 | 5/10 | 🔴 HIGH |
| 7 | 4/10 | 🔴 VERY HIGH |

---

## Detailed AI-Generation Indicators

### Patterns Suggesting AI Involvement:

**1. Organizational Templating (VERY STRONG SIGNAL)**
- Q6 & Q7 use extreme header hierarchy (4+ levels)
- Numbered list structures (1. Definition, 2. Methodology, 3. Results...)
- Parallel section formatting across questions
- **Conclusion**: Heavy AI usage in discussions

**2. Length vs. Content Efficiency**
- Q2: 500+ words for straightforward economic concept (could be 250)
- Q6: 800+ words; includes "Cross-Validation" section that's pure busywork
- Q7: 900+ words; "Integrated Interpretation" feels shoe-horned
- **Interpretation**: AI tends to elaborate; humans tend to be concise

**3. Robustness Claims Without Code**
- Q7 mentions "Testing with ±0.02, ±0.05, ±0.10 moneyness ranges" but no code shown
- Q3 mentions parallel processing but no timing/performance analysis
- **Pattern**: AI writes what it "should" do; humans implement what they "did"

**4. Cross-Referencing Density**
- Q4: References Q3 and mentions "CRR" (Q5 topic)
- Q5: "From Q2, we computed..." and references Q4
- Q6: Explicitly "Q5 CRR" and "Q6 Early Exercise"
- Q7: Section titled "Comparison to Q5 & Q6 Insights"
- **Interpretation**: AI systematically links questions; humans write independently

**5. Mathematical Rigor Inconsistency**
- Discussions often contain complex derivative notation (economics paper level)
- But code remains at beginner level (minimal optimization)
- **Gap**: Professional-level writing but student-level coding
- **Interpretation**: AI wrote economic analysis; student wrote code

**6. Hedging Language Escalation**
- Q1: Confident statements ("The answer is nuanced...")
- Q2: Still confident with evidence
- Q3: "May indicate", "Could suggest" appears
- Q4: Heavy hedging ("appears to suggest", "may be due to", "would likely")
- Q7: "Unfortunately", "Robustness Check", "Data Quality Note"
- **Pattern**: Later questions have much higher hedging (AI cautious mode)

**7. Disclaimer Density**
- Q6: "Because we are using an approximate convenience yield, some of these values could make little economic sense"
- Q7: "Data Quality Note: The provider's IV algorithm likely incorporates..."
- **Interpretation**: AI adds disclaimers; humans state assumptions naturally

### Patterns Suggesting Human Work:

**1. Q1: Simple, Direct, Correct**
- No unnecessary elaboration
- Addresses the exact question asked
- Mentions specific dates and rates
- **Conclusion**: Likely human-written

**2. Q2: Dense Economic Content**
- Integrated BMS formula derivation feels hand-written
- Jump from theory to Apple-specific application is natural
- Dividends = 4.1%, link to $1.69 calculated mean is concrete
- **BUT**: Structure and length suggest AI assistance in writing

**3. Q5: Complex Code**
- CRR binomial tree implementation requires genuine understanding
- Error handling and parallel processing shows technical depth
- **Conclusion**: Code is human; discussion may be AI-assisted

**4. Specific Numerical Examples**
- Q2: $1.69 mean, 26% decrease, 4.1% yield
- Q3: 1,658 OTM options, 0.328-2.295 moneyness
- Q6: 3-5× increase, 2-4% of put price
- **Interpretation**: Students cite their own calculations; AI uses generic numbers
- **But**: Could also be AI extracting real outputs to make claims

---

## Red Flags Summary

🔴 **CRITICAL**: Q7 claims robustness checks NOT present in code  
🔴 **CRITICAL**: Extreme templating in Q6-Q7 (1000+ words with 10+ subsections each)  
🟡 **WARNING**: Discussion length 2-3× optimal (indicates AI expansion)  
🟡 **WARNING**: Heavy cross-referencing (Q5→Q6→Q7) suggests AI linking  
🟡 **WARNING**: Mathematical rigor inversely correlated with code complexity  
🟡 **WARNING**: Numbered list breakdowns in every Q6-Q7 subsection  

---

## Grading Projection

### If This Is 100% Student Work:
- **Accuracy**: 35-40/40 ✅
- **Discussion**: 18-20/25 (some verbosity) ⚠️
- **Clarity/Figures**: 18-20/20 ✅
- **Code**: 12-15/15 ✅
- **Total**: 83-95/100 (A- to A)

### If AI Significantly Contributed to Discussions:
- **Accuracy**: 35-40/40 ✅ (results still correct)
- **Discussion**: 12-15/25 (template structure, not original) ❌
- **Clarity/Figures**: 16-18/20 (excessive length) ⚠️
- **Code**: 12-15/15 ✅
- **Total**: 75-88/100 (C+ to B+, depending on policy)

**Likely Scenario**: Hybrid work
- Q1-2: Mostly human
- Q3-5: Human code + AI-assisted discussion
- Q6-7: Significant AI involvement in discussion

---

## Specific Recommendations

### To Improve Authenticity:

1. **Shorten Discussions**: Reduce Q6-Q7 by 40-50% (cut redundant sections)
2. **Remove Robustness Claims**: Either implement claimed checks or remove mentions
3. **Reduce Cross-Referencing**: Let each question stand alone initially
4. **Simplify Organization**: Use fewer header levels (max 2-3 per question)
5. **Add Personal Insights**: Include one unique observation not in course materials per question
6. **Show Failed Attempts**: Mention what didn't work or alternative approaches tested

### To Address AI-Gen Signals:

1. **Q7 Robustness**: Add code cell actually testing ±0.02, ±0.05, ±0.10 moneyness windows
2. **Reduce Templating**: Integrate "Definition", "Methodology", "Results" into flowing narrative
3. **Hedging Language**: Replace "may suggest" with "shows" where data supports it
4. **Discussion/Code Balance**: Add more advanced code or simpler discussion to reduce asymmetry

---

## Overall Assessment

### Strengths:
✅ **All 7 questions answered with correct numerical results**  
✅ **Code implementations are functional and mostly correct**  
✅ **Economic intuition is sound and well-explained**  
✅ **LaTeX formatting professional**  
✅ **Data handling consistent and careful**  

### Weaknesses:
❌ **Late questions show heavy AI-generation signals**  
❌ **Discussion verbosity increases progressively (Q1→Q7 pattern)**  
❌ **Robustness claims in text not matched by code**  
❌ **Extreme templating in Q6-Q7 (>900 words each)**  
❌ **Cross-referencing pattern suggests systematic AI linking**  

### Overall Quality: 7.1/10
**Grade Estimate: B+ (if human-written) / B- to C+ (if AI-assisted in discussions)**

**Verdict**: This assignment shows **competent execution** with **increasing AI involvement** in later questions. The code quality remains strong throughout, but the discussion templating in Q6-Q7 raises significant academic integrity concerns. A good candidate for further clarification with the instructor about methodology.

---

## Appendix: AI-Gen Confidence Scoring Methodology

**Scoring Scale (10-point system)**:
- **9-10 (Low Risk)**: Clear human voice, specific data, natural flow, no template patterns
- **7-8 (Moderate Risk)**: Some templating, but mostly original; specific examples present
- **5-6 (Moderate-High Risk)**: Clear template structure; generic + specific examples mixed; cross-referencing present
- **3-4 (High Risk)**: Heavy templating; numbered lists throughout; systematic cross-referencing; hedged language
- **1-2 (Very High Risk)**: Extreme organization; claims not supported by code; appears auto-generated; disclaimer heavy

**Indicators Weighted In Final Score**:
- Organizational templating (25%)
- Language patterns (20%)
- Code-text asymmetry (20%)
- Cross-referencing (15%)
- Specificity of examples (20%)

