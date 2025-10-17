# Options Dataframe - All Columns in Table Format

## Dataset Overview
- **Total Rows**: 3,041 Apple options
- **Total Columns**: 39
- **Quote Dates**: January 17, 2020 and March 20, 2020
- **Data Source**: OptionMetrics

---

## Complete Column Reference

| # | Column Name | Data Type | Range/Values | Non-Null | Null | Description |
|---|---|---|---|---|---|---|
| 1 | `index` | int64 | 166 - 2,345 | 3,041 | 0 | Original row index from data source |
| 2 | `secid` | Float64 | 101594 (const) | 3,041 | 0 | OptionMetrics security ID (Apple) |
| 3 | `date` | object | 2020-01-17 or 2020-03-20 | 3,041 | 0 | **Quote date** - KEY FOR FILTERING |
| 4 | `symbol` | string | AAPL YYMMDDCPSTRIKE | 3,041 | 0 | CBOE ticker symbol (e.g., AAPL 200124C240) |
| 5 | `symbol_flag` | string | "1" | 3,041 | 0 | Symbol type flag (data quality) |
| 6 | `exdate` | object | 2020-01-24 - 2022-06-17 | 3,041 | 0 | **Expiration date** - KEY FOR MATURITY |
| 7 | `last_date` | string | 2019-09-19 - 2020-03-20 | 3,041 | 0 | Last trading date before quote date |
| 8 | `cp_flag` | string | "C" or "P" | 3,041 | 0 | **Call/Put flag** - KEY FOR OPTION TYPE |
| 9 | `best_bid` | Float64 | $0.11 - $271.00 | 3,041 | 0 | **Highest bid price** in market |
| 10 | `best_offer` | Float64 | $0.14 - $275.50 | 3,041 | 0 | **Lowest ask/offer price** in market |
| 11 | `volume` | Float64 | 0 - 29,443 | 3,041 | 0 | Trading volume (contracts traded) |
| 12 | `open_interest` | Float64 | 1 - 28,015 | 3,041 | 0 | Open contracts (used in filtering) |
| 13 | `impl_volatility` | float64 | 20.93% - 199.88% | 3,041 | 0 | **Provider's IV** (proprietary algo) - GROUND TRUTH |
| 14 | `delta` | Float64 | -0.9899 - +0.9899 | 3,041 | 0 | Option delta (used in filtering: 0.01-0.99) |
| 15 | `gamma` | Float64 | 0.00004 - 0.04284 | 3,041 | 0 | Option gamma (Greeks) |
| 16 | `vega` | Float64 | 0.265 - 193.543 | 3,041 | 0 | Option vega (Greeks) |
| 17 | `theta` | Float64 | -329.04 - +2.57 | 3,041 | 0 | Option theta (Greeks) |
| 18 | `optionid` | Float64 | 119.4M - 133.2M | 3,041 | 0 | Unique option contract ID |
| 19 | `cfadj` | Float64 | 1.0 (const) | 3,041 | 0 | Corporate action adjustment (always 1.0) |
| 20 | `am_settlement` | Float64 | 0.0 (const) | 3,041 | 0 | Settlement flag (always 0.0) |
| 21 | `contract_size` | Float64 | 100.0 (const) | 3,041 | 0 | Shares per contract (US standard) |
| 22 | `ss_flag` | string | "0" | 3,041 | 0 | Security status flag (normal = 0) |
| 23 | `forward_price` | string | NULL | 0 | 3,041 | ❌ Not used - entirely missing |
| 24 | `expiry_indicator` | string | "w" or NULL | 855 | 2,186 | Weekly option indicator (28% populated) |
| 25 | `root` | string | NULL | 0 | 3,041 | ❌ Not used - entirely missing |
| 26 | `suffix` | string | NULL | 0 | 3,041 | ❌ Not used - entirely missing |
| 27 | `hash` | uint64 | 507.8T - 184.4T | 3,041 | 0 | Hash identifier (data integrity) |
| 28 | `strike` | Float64 | $75.00 - $520.00 | 3,041 | 0 | **Strike price (K)** - KEY FOR PRICING |
| 29 | `option_price` | Float64 | $0.13 - $273.25 | 3,041 | 0 | Option price at quote date |
| 30 | `is_call` | boolean | True or False | 3,041 | 0 | Boolean call flag (True=call, False=put) |
| 31 | `DTM` | int64 | 7 - 882 days | 3,041 | 0 | **Days to maturity** - USE FOR CRR STEPS (Q5) |
| 32 | `YTM` | float64 | 0.0192 - 2.4164 years | 3,041 | 0 | **Years to maturity (T)** - KEY FOR BMS |
| 33 | `risk_free` | float64 | 0.46% - 1.74% | 3,041 | 0 | **Risk-free rate (r)** - decimal form |
| 34 | `stock_price` | float64 | $229.24 - $318.73 | 3,041 | 0 | Current stock price at quote date |
| 35 | `stock_exdiv` | float64 | $226.09 - $318.73 | 3,041 | 0 | **Stock price minus dividends ($\hat{S}_t$)** - USE IN FORMULAS |
| 36 | `implied_forward_price` | float64 | $227.46 - $325.07 | 3,041 | 0 | Forward price from put-call parity |
| 37 | `implied_vol_bms` | float64 | 20.98% - 165.66% | 3,039 | 2 | **BMS IV** (pre-computed) - COMPARE AGAINST |
| 38 | `implied_vol_bid` | float64 | 0.44% - 160.18% | 2,907 | 134 | IV from bid price (4.4% missing) |
| 39 | `implied_vol_ask` | float64 | 21.12% - 252.79% | 3,041 | 0 | IV from ask price |

---

## 🔴 Critical Columns for Assignment (Highlighted)

### Time to Maturity
| Column | Type | Usage | Formula |
|--------|------|-------|---------|
| `date` | object | Filter data | date == dt.date(2020,1,17) or dt.date(2020,3,20) |
| `exdate` | object | Determine maturity | T = exdate - date |
| `DTM` | int64 | CRR tree steps (Q5) | n_steps = 5 * DTM |
| `YTM` | float64 | **Time parameter (T)** | Use directly in BMS: $T = YTM$ |

### Option Specifications  
| Column | Type | Usage | Values |
|--------|------|-------|--------|
| `cp_flag` | string | Call/Put classification | "C" = call, "P" = put |
| `is_call` | boolean | Boolean form (convenient) | True = call, False = put |
| `strike` | Float64 | Strike price (K) | $75 - $520 |

### Market Prices (Bid-Ask Spread)
| Column | Type | Range | Usage |
|--------|------|-------|-------|
| `best_bid` | Float64 | $0.11 - $271.00 | Bid side of spread |
| `best_offer` | Float64 | $0.14 - $275.50 | Ask side of spread |
| `option_price` | Float64 | $0.13 - $273.25 | Mid price or published price |
| **Calculated** | - | - | **mid_price = (best_bid + best_offer) / 2** |

### Greeks (from Market)
| Column | Type | Range | Usage |
|--------|------|-------|-------|
| `delta` | Float64 | -0.99 to +0.99 | Used in filtering & hedging |
| `gamma` | Float64 | 0.00004 - 0.04284 | Greeks for risk |
| `vega` | Float64 | 0.265 - 193.543 | Sensitivity to vol |
| `theta` | Float64 | -329.04 - +2.57 | Time decay |

### Underlying Stock (CRITICAL)
| Column | Type | Formula | Usage |
|--------|------|---------|-------|
| `stock_price` | float64 | $S_t$ | Current stock price |
| `stock_exdiv` | float64 | $\hat{S}_t = S_t - \text{dividends}$ | **USE THIS in BMS formulas, not stock_price** |
| **Dividend** | Calculated | $S_t - \hat{S}_t$ | Accumulated dividends over option life |

### Risk-Free Rate (CRITICAL)
| Column | Type | Format | Range | Usage |
|--------|------|--------|-------|-------|
| `risk_free` | float64 | Decimal (0.0156 = 1.56%) | 0.46% - 1.74% | **Use directly (r)** in BMS formulas |

### Implied Volatilities (COMPARE THESE)
| Column | Type | Range | Coverage | Purpose |
|--------|------|-------|----------|---------|
| `impl_volatility` | float64 | 20.93% - 199.88% | 100% | **Provider's IV (ground truth)** - Q4, Q6, Q7 |
| `implied_vol_bms` | float64 | 20.98% - 165.66% | 99.9% (2 missing) | **BMS IV (pre-computed)** - Q3, Q4 |
| `implied_vol_bid` | float64 | 0.44% - 160.18% | 95.6% (134 missing) | IV from bid side |
| `implied_vol_ask` | float64 | 21.12% - 252.79% | 100% | IV from ask side |

---

## 📊 Key Formulas Using These Columns

| Formula | Columns Used | Question |
|---------|--------------|----------|
| **Moneyness** | $M = \frac{\text{strike}}{\text{stock\_exdiv}} = \frac{K}{\hat{S}_t}$ | Q3 |
| **OTM Filter** | Puts: $M \leq 1$, Calls: $M > 1$ | Q3 |
| **Dividend Yield** | $y \approx \frac{\text{stock\_price} - \text{stock\_exdiv}}{\text{stock\_price} \times \text{YTM}}$ | Q5 |
| **BMS Call** | $C = e^{-yT}\hat{S}_t N(d_1) - e^{-rT}K N(d_2)$ | Q1-Q6 |
| **BMS Put** | $P = e^{-rT}K N(-d_2) - e^{-yT}\hat{S}_t N(-d_1)$ | Q1-Q6 |
| **IV Ratio** | $100 \times \left(\frac{\text{impl\_volatility}}{\text{implied\_vol\_bms}} - 1\right)$ | Q4 |
| **CRR Steps** | $n\_steps = 5 \times \text{DTM}$ | Q5 |
| **Borrow Fee** | $h_t^Q \approx -\frac{\sigma_c - \sigma_p}{\sqrt{2\pi(T-t)}}$ | Q7 |

---

## ✅ Filters Already Applied to Data

| Filter | Condition | Result |
|--------|-----------|--------|
| **Before maturity** | date < exdate | All 3,041 ✓ |
| **Open interest** | open_interest > 0 | All 3,041 ✓ |
| **Delta range** | 0.01 ≤ \|delta\| ≤ 0.99 | All 3,041 ✓ |
| **IV range** | 0.03 ≤ impl_volatility ≤ 2.0 | All 3,041 ✓ |
| **Bid-ask spread** | best_offer > best_bid AND best_bid > 0.1 | All 3,041 ✓ |

---

## 📈 Data Characteristics

### By Quote Date
| Date | Stock Price | Risk-Free Rate | Implied Vol (avg) | Notes |
|------|-------------|---------------|--------------------|-------|
| **Jan 17, 2020** | $318.73 | 1.5-1.7% | ~40-80% | Pre-COVID |
| **Mar 20, 2020** | $229.24 | 0.46-1.74% | ~50-120% | COVID crash (-28%), rate cuts, vol spike |

### By Option Type
| Type | Count | Delta Range | IV Range |
|------|-------|-------------|----------|
| **Calls** | ~1,500 | 0.01 to 0.99 | 20.93% - 199.88% |
| **Puts** | ~1,500 | -0.99 to -0.01 | 20.93% - 199.88% |

### By Maturity
| Metric | Min | Max | Avg |
|--------|-----|-----|-----|
| **DTM** | 7 days | 882 days | ~180 days |
| **YTM** | 0.0192 years | 2.4164 years | ~0.50 years |

---

## 🎯 Which Columns to Use for Each Question

| Question | Primary Columns | Secondary Columns |
|----------|-----------------|-------------------|
| **Q1** | date, YTM, risk_free | exdate |
| **Q2** | date, stock_price, stock_exdiv | exdate |
| **Q3** | strike, stock_exdiv, cp_flag, implied_vol_bms, exdate, date | YTM, is_call |
| **Q4** | impl_volatility, implied_vol_bms, strike, stock_exdiv, cp_flag | exdate, date |
| **Q5** | DTM, YTM, stock_price, stock_exdiv, risk_free, strike, cp_flag, impl_volatility | exdate |
| **Q6** | DTM, YTM, strike, stock_exdiv, risk_free, cp_flag, impl_volatility, option_price | exdate, date |
| **Q7** | DTM, YTM, strike, stock_exdiv, risk_free, cp_flag, best_bid, best_offer, exdate, date | impl_volatility |

---

## 🔍 Data Quality Summary

| Aspect | Status | Notes |
|--------|--------|-------|
| **Completeness** | ✅ Excellent | 36/39 columns fully populated |
| **Missing Values** | ✅ Minimal | Only 3 columns missing (not needed) |
| **Duplicate Rows** | ✅ None | All 3,041 unique option contracts |
| **Consistency** | ✅ Good | Filters already applied |
| **Outliers** | ✅ Checked | IV capped at 2.0, delta between 0.01-0.99 |

---

## 💡 Quick Reference

### Use `stock_exdiv`, NOT `stock_price`
- In BMS formulas, always use: $\hat{S}_t =$ `stock_exdiv`
- The difference `stock_price - stock_exdiv` = accumulated dividends

### `risk_free` is Already Decimal
- Value 0.0156 means 1.56% per annum
- Use directly in BMS: $r =$ `risk_free`

### `YTM` is Years, NOT Days
- To convert to years: $T =$ `YTM`
- To convert to days: $D =$ `DTM`
- For CRR steps: $n = 5 \times$ `DTM`

### Moneyness Matters
- Define as: $M = \frac{K}{\hat{S}_t} = \frac{\text{strike}}{\text{stock\_exdiv}}$
- OTM puts: $M \leq 1.0$
- OTM calls: $M > 1.0$

### Compare Three IVs
1. **impl_volatility** - Provider's algorithm (ground truth)
2. **implied_vol_bms** - Already computed via BMS
3. **Your own IVs** - You'll compute in Q3-Q7

