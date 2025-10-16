# GitHub Copilot Instructions for Assignment 1

Read this file at each stage of answering questions. These instructions ensure consistency, accuracy, and quality across all 7 questions.

ALWAYS USE THE FILE "202510-assignment1-en.ipynb" IN THE CONTEXT OF OUR CHAT BY DEFAULT
ALSO DONT FORGET THAT THE THEORY USED FOR THE ASSIGNEMNT IS IN THE FILE "Contents and exercices.md"

## ⭐ CRITICAL: Read Course Materials First! ⭐

**BEFORE GENERATING ANY ANSWER:**
1. **Read the exercise file**: `202510-assignment1-en.ipynb` - the question description
2. **Read corresponding course materials**: Check Contents and exercices.md for relevant chapters (e.g., ch01, ch02, ch04)
4. **Check class notes**: Make sure your discussion uses vocabulary and concepts from class (from Contents and exercices.md)

**Why?** Your teacher knows what was covered in class. Answers that reflect class concepts will receive better grades than generic explanations. Use the exact terminology taught (e.g., "volatility smile", "convenience yield", "early exercise premium", not just "variation in volatility").

**Examples of how to verify alignment:**
- If discussing BMS formula, match the notation from course materials
- If explaining dividend yield, use the same symbol/formula from class
- If mentioning economic interpretations, reference concepts taught
- Cite specific topics from course materials when relevant

---

## General Instructions (All Questions)

### Code Style
- Use **beginner-level code** (simple and readable, not fancy)
- No intermediate variables unless necessary
- Direct filtering without complex lambda functions
- **Max ~15-20 lines of code per cell** (split into logical blocks if needed)
- Split code into logical blocks with separators and descriptions:

### Date Filtering (CRITICAL)
```python
# CORRECT: Use dt.date()
options['date'] == dt.date(2020, 1, 17)  ✓ Works!

# WRONG: Never use pd.Timestamp()
options['date'] == pd.Timestamp('2020-01-17')  ✗ Returns 0 rows
```

### Stock Price Usage
- Always use `stock_exdiv` (not `stock_price`) in formulas
- `stock_exdiv` = stock price minus dividends already paid
- Difference = accumulated dividends: `stock_price - stock_exdiv`

### Risk-Free Rate Format
- Already in decimal form: 0.0156 = 1.56%
- Use directly in formulas without converting

### Plots Must Include
- ✓ Clear title
- ✓ Axis labels with units
- ✓ Legend when multiple colors/lines
- ✓ Grid (optional but recommended)
- ✓ Appropriate size (figsize not too large)

### Discussions Must Include
- ✓ What the plot shows
- ✓ Key findings (numbers)
- ✓ Interpretation (what it means)
- ✓ Answer to specific question asked
- ✓ Mathematical formulas where needed (LaTeX)

---

## Question 1: Risk-Free Rate vs Maturity

### Checklist
- [ ] Filter data correctly using `dt.date()`
- [ ] X-axis: YTM (Years to Maturity)
- [ ] Y-axis: 100 * risk_free (as percentage)
- [ ] Two colors: blue for Jan 17, red for Mar 20
- [ ] Discussion explains term structure
- [ ] Mentions BMS constant rate assumption
- [ ] Recommends using appropriate rate per maturity

### Key Points to Discuss
1. Plot shows clustering by maturity
2. BMS assumes one constant rate
3. Reality: yield curve (rates vary by maturity)
4. Recommendation: use appropriate rate for each option

### Statistics to Report
- Rate range for Jan 17
- Rate range for Mar 20
- Difference between dates (COVID impact)

---

## Question 2: Dividends vs Maturity

### Checklist
- [ ] Calculate: `div_diff = stock_price - stock_exdiv`
- [ ] X-axis: YTM (Years to Maturity)
- [ ] Y-axis: Dividend amount in dollars
- [ ] Two colors: blue for Jan 17, red for Mar 20
- [ ] Print statistics: Mean and Std for both dates
- [ ] Discussion proves NO dividend policy change
- [ ] Include dividend-adjusted BMS formula
- [ ] Use LaTeX for mathematical formulas

### Key Points to Discuss
1. Longer options accumulate more dividends (expected)
2. Mar 20 dividends lower than Jan 17 (~26% less)
3. This is NOT a policy change (shorter maturities)
4. COVID-19 economic uncertainty factor
5. BMS dividend-yield formula: $C = e^{-yT}S_t N(d_1) - e^{-rT}K N(d_2)$

### Statistics to Report
- Mean dividend Jan 17 vs Mar 20
- Std deviation for both dates
- Percentage change between dates

---

## Question 3: BMS IV & Volatility Smiles

### Checklist
- [ ] Import BMS module: `from dorion_francois.black_merton_scholes import implied_volatility`
- [ ] Calculate moneyness: `M = strike / stock_exdiv`
- [ ] Filter OTM options: Puts with M ≤ 1, Calls with M > 1
- [ ] Create `otm_options` dataframe
- [ ] Add BMS IV column by inverting BMS formula
- [ ] Create 1x2 subplot (two panels)
- [ ] LEFT panel: Jan 17 (exp Feb 14 + Jul 17) and Mar 20 (exp Apr 17)
- [ ] RIGHT panel: Jan 17 (exp Feb 14 + Jul 17) and Mar 20 (exp Oct 16)
- [ ] Scatter your IVs on top of line plots for `implied_vol_bms`
- [ ] Discuss smile level, span, and maturity effects
- [ ] Suggest alternate moneyness measure
- [ ] Show figure with alternate measure

### Key Points to Discuss
1. Volatility smile pattern (IV varies with moneyness)
2. Level: how high/low is the smile
3. Span: how wide across moneyness range
4. Maturity effects: different for different expirations
5. Alternate measure: log-moneyness or moneyness-squared
6. Does alternate measure improve analysis?

### Data to Report
- Number of OTM options
- Moneyness range
- IV ranges by expiration and date

---

## Question 4: IV Comparison (Provider vs BMS)

### Checklist
- [ ] Use same OTM options from Q3
- [ ] Use same moneyness measure as Q3
- [ ] Calculate: `100 * (impl_volatility / implied_vol_bms - 1)`
- [ ] Scatter vs moneyness
- [ ] Y-axis interpretation: percentage difference in IV
- [ ] Discuss if magnitude is large or small
- [ ] Compare CRR vs BMS for ITM options (discuss, don't implement)

### Key Points to Discuss
1. Y-axis is percentage difference: positive = provider IV higher
2. Are differences small (< 5%) or large (> 10%)?
3. Pattern across moneyness?
4. For ITM options: would CRR differ significantly from BMS?

### Statistics to Report
- Mean percentage difference
- Range of differences
- Percentage of options with |diff| > threshold

---

## Question 5: CRR Tree with Dividend Yield

### Checklist
- [ ] Convert dividends to convenience yield: `y = (stock_price - stock_exdiv) / (stock_price * YTM)`
- [ ] Import CRR from binomial_tree module
- [ ] Set n_steps = 5 * DTM
- [ ] Calculate CRR IV for each option
- [ ] Compare with `impl_volatility` (not implied_vol_bms)
- [ ] Report summary statistics (mean, std, rmse)
- [ ] Create figure comparing the three IVs
- [ ] Discuss: is CRR better than BMS?

### Key Points to Discuss
1. Convenience yield calculation and interpretation
2. CRR tree convergence to BMS as steps increase
3. Does CRR fit better than BMS?
4. Summary statistics: MAE, RMSE, correlation
5. Visual comparison of the three IV measures

### Statistics to Report
- Dividend yield statistics (mean, range)
- CRR IV statistics
- Comparison metrics: mean absolute error, RMSE
- Percentage improvement vs BMS

---

## Question 6: Early Exercise Premium

### Checklist
- [ ] Use convenience yield from Q5
- [ ] Use `impl_volatility` field (NOT implied_vol_bms)
- [ ] Price European options using BMS formula
- [ ] Calculate: American price (from data) - European price
- [ ] Apply upper bound filter (use economic intuition)
- [ ] Plot early exercise value vs moneyness or strike
- [ ] Discuss patterns observed
- [ ] Note: some values might be negative (explain why)

### Key Points to Discuss
1. What is early exercise premium (call value of holding vs exercising early)
2. Economic upper bound: premium can't exceed intrinsic value
3. Patterns: usually higher for deep ITM puts
4. Why some values are negative (approximate yield issue)
5. Typical magnitude of early exercise premium

### Statistics to Report
- Mean early exercise value
- Maximum early exercise value
- Percentage of options with positive premium
- Premium as % of option price

---

## Question 7: Borrow Fee from Put-Call Parity

### Checklist
- [ ] Find 1-month ATM options (calls and puts separately)
- [ ] Get IVs for both: `sigma_c` (calls) and `sigma_p` (puts)
- [ ] Calculate: `h_t = -(\sigma_c - \sigma_p) / sqrt(2*pi*(T-t))`
- [ ] Compute for both dates (Jan 17 and Mar 20)
- [ ] Express as percentage or basis points
- [ ] Discuss interpretation and magnitudes
- [ ] Compare between dates
- [ ] Relate to economic conditions (COVID impact)

### Key Points to Discuss
1. What is borrow fee (stock lending rate)
2. Put-call parity relationship to borrowing
3. How IV difference reflects borrowing costs
4. Computed fees for both dates
5. Why fees higher in Mar 20 (COVID uncertainty)
6. Magnitude: is it economically reasonable?

### Statistics to Report
- Borrow fee Jan 17 (in %)
- Borrow fee Mar 20 (in %)
- ATM IV for calls and puts on each date
- Comparison to actual stock lending rates (if known)

---

## Quality Checklist (Before Submitting Each Question)

### Accuracy (40%)
- [ ] All calculations correct
- [ ] All filters work (check row counts)
- [ ] Dates formatted correctly
- [ ] Units correct (%, $, years, etc.)
- [ ] No NaN or infinite values

### Discussion (25%)
- [ ] Answers the question completely
- [ ] Includes numerical evidence
- [ ] Clear interpretation
- [ ] Proper mathematical notation (LaTeX)
- [ ] Concise (not too long)

### Figures (20%)
- [ ] Title and labels present
- [ ] Legend included where needed
- [ ] Appropriate scaling
- [ ] Grid helpful (not distracting)
- [ ] Clear and professional

### Code (15%)
- [ ] Beginner-level (simple)
- [ ] Well-commented where needed
- [ ] No unnecessary complexity
- [ ] Variables named clearly
- [ ] No hard-coded values (use column names)

---

## Common Mistakes to Avoid

### Date Issues
- ❌ Using `pd.Timestamp()` instead of `dt.date()`
- ❌ Comparing dates with wrong type
- ❌ Filtering by index instead of date

### Data Issues
- ❌ Using `stock_price` instead of `stock_exdiv` in formulas
- ❌ Forgetting to convert risk_free rate (it's already decimal!)
- ❌ Using implied_vol_bms where impl_volatility requested

### Plot Issues
- ❌ Missing titles or axis labels
- ❌ Forgetting units (Years, %, $, etc.)
- ❌ No legend when multiple series shown
- ❌ Figure too small or too large

### Discussion Issues
- ❌ No numbers or statistics
- ❌ Just describing plot without interpretation
- ❌ Forgetting to answer the specific question asked
- ❌ No mathematical formulas where needed

### Code Issues
- ❌ Using complex list comprehensions for beginners
- ❌ Creating unnecessary intermediate variables
- ❌ Over-formatting plots (don't need fontsize for everything)
- ❌ Hard-coding numbers (use column names instead)

---

## Helpful Commands Reference



### Filtering
```python
# Single date
options[options['date'] == dt.date(2020, 1, 17)]

# Single expiration
options[options['exdate'] == dt.date(2020, 2, 14)]

# Multiple conditions
options[(options['date'] == dt.date(2020, 1, 17)) & (options['exdate'] == dt.date(2020, 2, 14))]

# Call vs Put
options[options['is_call'] == True]
options[options['cp_flag'] == 'C']
```

### Statistics
```python
data.mean()
data.std()
data.min()
data.max()
data.describe()
```

### Plotting
```python
plt.scatter(x, y, c='color', label='label', alpha=0.6, s=30)
plt.plot(x, y, 'line_style', label='label')
plt.xlabel('label')
plt.ylabel('label')
plt.title('title')
plt.legend()
plt.grid(True, alpha=0.3)
plt.show()
```

### Moneyness
```python
moneyness = options['strike'] / options['stock_exdiv']
otm_puts = options[options['moneyness'] <= 1.0]
otm_calls = options[options['moneyness'] > 1.0]
```

---

## Deadline Reminder
**October 17, 2025 at 11:55 PM** - Submit to ZoneCours
- Must be .ipynb format
- Include all .py files needed
- Student IDs in first cell
- All 7 questions answered
- Grading: 40% accuracy, 25% discussion, 20% figures, 15% code

---

## Questions? Issues?

If you encounter problems:
1. Check this file first
2. Review the Q1_Q2_SUMMARY.md for examples
3. Check OPTIONS_DATAFRAME_COLUMNS_TABLE.md for column meanings
4. Read the course materials in Content/ folder
5. Run tests/validations before submitting

Good luck! 🎯
