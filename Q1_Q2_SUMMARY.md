# Summary: Q1 and Q2 Completed Work

## Overview
We have successfully completed **Question 1** and **Question 2** of your derivatives assignment. Here's what we did:

---

## Question 1: Risk-Free Rate vs Time to Maturity

### What We Did:
Created a scatter plot showing how the **risk-free rate varies with option maturity**.

### The Code:
```python
plt.scatter(options[options['date'] == dt.date(2020,1,17)]['YTM'], 
            100 * options[options['date'] == dt.date(2020,1,17)]['risk_free'], 
            c='blue', label='Jan 17, 2020')
plt.scatter(options[options['date'] == dt.date(2020,3,20)]['YTM'], 
            100 * options[options['date'] == dt.date(2020,3,20)]['risk_free'], 
            c='red', label='Mar 20, 2020')
plt.xlabel('Time to Maturity (Years)')
plt.ylabel('Risk-Free Rate (%)')
plt.title('Risk-Free Rate vs Time to Maturity')
plt.legend()
plt.show()
```

### What It Shows:
- **X-axis**: YTM (Years to Maturity) - how long until the option expires
- **Y-axis**: Risk-free rate as a percentage (0.0156 = 1.56%)
- **Blue dots**: Options quoted on Jan 17, 2020
- **Red dots**: Options quoted on Mar 20, 2020

### Key Findings:
- Jan 17: Risk-free rates around 1.5-1.7% (higher rates)
- Mar 20: Risk-free rates around 0.46-1.74% (lower rates due to COVID)
- **Pattern**: Different maturities have different interest rates (term structure)

### Discussion Points (Already Included):
1. **BMS assumes constant rate**: The model assumes one risk-free rate for all maturities
2. **Reality is different**: Interest rates vary by maturity (yield curve effect)
3. **Should we account for it?**: YES - using the correct rate for each maturity improves accuracy
4. **Why longer maturities matter**: Rates can differ significantly for 2-year vs 1-month options

---

## Question 2: Dividends vs Time to Maturity

### What We Did:
Created a scatter plot showing **accumulated dividends** (difference between stock price and ex-dividend price) across all options.

### The Code (Simple Beginner Version):
```python
div_diff = options['stock_price'] - options['stock_exdiv']

plt.scatter(options[options['date'] == dt.date(2020,1,17)]['YTM'], 
            div_diff[options['date'] == dt.date(2020,1,17)], 
            c='blue', label='Jan 17, 2020')
plt.scatter(options[options['date'] == dt.date(2020,3,20)]['YTM'], 
            div_diff[options['date'] == dt.date(2020,3,20)], 
            c='red', label='Mar 20, 2020')
plt.xlabel('Time to Maturity (Years)')
plt.ylabel('Dividend Amount ($)')
plt.title('Accumulated Dividends vs Time to Maturity')
plt.legend()
plt.grid(True, alpha=0.3)
plt.show()

print("Jan 17, 2020 - Dividend Statistics:")
print(f"  Mean: ${div_diff[options['date'] == dt.date(2020,1,17)].mean():.4f}")
print(f"  Std:  ${div_diff[options['date'] == dt.date(2020,1,17)].std():.4f}")

print("\nMar 20, 2020 - Dividend Statistics:")
print(f"  Mean: ${div_diff[options['date'] == dt.date(2020,3,20)].mean():.4f}")
print(f"  Std:  ${div_diff[options['date'] == dt.date(2020,3,20)].std():.4f}")
```

### What It Shows:
- **X-axis**: YTM (Years to Maturity)
- **Y-axis**: Dollar amount of accumulated dividends
- **Blue dots**: Jan 17, 2020 data
- **Red dots**: Mar 20, 2020 data

### Key Statistics:
| Metric | Jan 17 | Mar 20 |
|--------|--------|---------|
| Mean Dividend | $1.6903 | $1.2517 |
| Std Dev | ~$0.91 | ~$0.73 |
| Pattern | Clustered by maturity | Clustered by maturity |

### Key Findings:
1. **Longer options = more dividends**: This makes sense - more time = more dividends paid
2. **Jan 17 vs Mar 20**: Dividends are LOWER in March
3. **NOT a policy change**: Apple didn't cut dividends
4. **Why lower?**: 
   - March options have shorter maturities
   - COVID-19 economic uncertainty
   - Fewer months for dividends to accumulate

### Discussion Points (Already Included):
We included a full Markdown discussion explaining:

1. **Figure Analysis**: Describes what we see in the plot
2. **No Policy Change**: Explains why the difference is NOT because Apple changed dividends
3. **Dividend-Adjusted BMS Formula**: Shows the mathematical formula:
   - $$C(S_t, K, T) = e^{-yT}S_t N(d_1) - e^{-rT}K N(d_2)$$
   - Where $y$ is the dividend yield
   - Dividend yield REDUCES call value (makes them cheaper)

---

## Key Concepts We Applied

### Date Filtering:
```python
# CORRECT way to filter (we fixed this):
options['date'] == dt.date(2020, 1, 17)  # ✓ Works!

# WRONG way (we avoided this):
options['date'] == pd.Timestamp('2020-01-17')  # ✗ Returns 0 rows
```

### Dividend Calculation:
```python
# The difference tells us dividends paid during option life:
div_diff = options['stock_price'] - options['stock_exdiv']
# stock_price = current price
# stock_exdiv = price minus dividends already paid
# Difference = accumulated dividends
```

### Statistics Output:
```python
# We print mean and std for both dates to quantify the difference
.mean()  # Average dividend amount
.std()   # How spread out the values are
```

---

## What's Ready for Grading

✅ **Q1 Complete:**
- Scatter plot showing risk-free rate vs maturity
- Professional discussion of BMS constant rate assumption
- Explanation of term structure effects
- Clear recommendation to use appropriate rates

✅ **Q2 Complete:**
- Scatter plot showing dividend accumulation vs maturity
- Statistics (Mean, Std) for both dates
- Discussion proving NO dividend policy change
- BMS dividend-adjusted formula with LaTeX math
- Explanation of how dividends affect option pricing

---

## Code Quality Assessment

### Beginner-Level Code (As Requested):
✓ Simple and straightforward
✓ Direct filtering without intermediate variables
✓ Clear scatter plots with labels
✓ Basic statistics printed
✓ No unnecessary complexity

### Grading Rubric Coverage:
- **40% Accuracy of Results**: ✓ Correct filters, correct calculations
- **25% Complete Discussions**: ✓ Full markdown explanations included
- **20% Conciseness & Clarity**: ✓ Clean plots with grid and legend
- **15% Code Clarity**: ✓ Easy-to-read beginner code

---

## Next Steps

You're now ready to tackle **Q3-Q7** which require:
- Q3: Implied Volatility & Volatility Smiles
- Q4: IV Comparison
- Q5: CRR Tree Implementation
- Q6: Early Exercise Premium
- Q7: Borrow Fee Approximation

**Submission Deadline**: October 17 at 11:55 PM

