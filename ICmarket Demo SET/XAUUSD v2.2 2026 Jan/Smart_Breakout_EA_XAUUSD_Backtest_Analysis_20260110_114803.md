# Smart Breakout EA Pro - XAUUSD Backtest Analysis Report

**Date:** 2026-01-10 15:46:35  
**Analysis Period:** 2025.01.06 - 2026.01.05  
**Timeframe:** 1H (Hourly)  
**Symbol:** XAUUSD (Gold/USD)  

---

## Executive Summary

I've analyzed **5 different configurations** of the Smart Breakout EA Pro for **XAUUSD** over a **1-year period**. Each configuration uses different drawdown limits and risk parameters, resulting in distinct performance characteristics.

| Configuration | Net Profit | Profit Factor | Max Drawdown | Win Rate | Key Characteristics |
|---------------|------------|---------------|--------------|----------|---------------------|
| **0.3DD** | $3,225.29 | 2.41 | 0.32% ($322.30) | 71.11% | Most conservative, highest win rate |
| **0.4DD** | $5,148.08 | 2.91 | 0.45% ($464.78) | 50.00% | Balanced approach |
| **0.5DD** | $5,312.20 | **3.31** | 0.51% ($523.88) | 43.24% | Best risk-adjusted returns |
| **0.7DD** | **$6,817.85** | 2.41 | 0.74% ($760.41) | 40.43% | Most aggressive, highest profit |
| **0.3DD-5000P** | $5,082.92 | 2.99 | 0.37% ($386.68) | 51.52% | Conservative with profit filter |

---

## Detailed Performance Metrics

### 1. 0.3DD Configuration (Most Conservative)
- **Net Profit:** $3,225.29
- **Profit Factor:** 2.41
- **Total Trades:** 90
- **Win Rate:** 71.11% (64 wins, 26 losses)
- **Max Drawdown:** 0.32% ($322.30)
- **Average Profit/Trade:** $86.19
- **Average Loss/Trade:** -$88.12
- **Expected Payoff:** $35.84

**Best for:** Traders prioritizing capital preservation and consistency over high returns.

### 2. 0.4DD Configuration (Balanced)
- **Net Profit:** $5,148.08
- **Profit Factor:** 2.91
- **Total Trades:** 70
- **Win Rate:** 50.00% (35 wins, 35 losses)
- **Max Drawdown:** 0.45% ($464.78)
- **Average Profit/Trade:** $224.19
- **Average Loss/Trade:** -$77.10
- **Expected Payoff:** $73.54

**Best for:** Traders seeking a middle-ground approach between risk and reward.

### 3. 0.5DD Configuration (Optimal Risk-Reward)
- **Net Profit:** $5,312.20
- **Profit Factor:** **3.31** (Best)
- **Total Trades:** 74
- **Win Rate:** 43.24% (32 wins, 42 losses)
- **Max Drawdown:** 0.51% ($523.88)
- **Average Profit/Trade:** $237.84
- **Average Loss/Trade:** -$54.73
- **Expected Payoff:** $71.79

**Best for:** Traders focused on maximizing risk-adjusted returns.

### 4. 0.7DD Configuration (Most Aggressive)
- **Net Profit:** **$6,817.85** (Highest)
- **Profit Factor:** 2.41
- **Total Trades:** 141 (Most)
- **Win Rate:** 40.43% (57 wins, 84 losses)
- **Max Drawdown:** 0.74% ($760.41)
- **Average Profit/Trade:** $204.16
- **Average Loss/Trade:** -$57.37
- **Expected Payoff:** $48.35

**Best for:** Aggressive traders with high risk tolerance seeking maximum profits.

### 5. 0.3DD-5000P Configuration (Conservative with Filter)
- **Net Profit:** $5,082.92
- **Profit Factor:** 2.99
- **Total Trades:** 66 (Fewest)
- **Win Rate:** 51.52% (34 wins, 32 losses)
- **Max Drawdown:** 0.37% ($386.68)
- **Average Profit/Trade:** $224.48
- **Average Loss/Trade:** -$79.67
- **Expected Payoff:** $77.01

**Best for:** Conservative traders who want better returns than 0.3DD with minimal additional risk.

---

## Comprehensive Comparison Table

| Metric | 0.3DD | 0.4DD | 0.5DD | 0.7DD | 0.3DD-5000P |
|--------|-------|-------|-------|-------|-------------|
| **Net Profit** | $3,225.29 | $5,148.08 | $5,312.20 | **$6,817.85** | $5,082.92 |
| **Gross Profit** | $5,516.47 | $7,846.48 | $7,610.92 | $11,637.31 | $7,632.25 |
| **Gross Loss** | -$2,291.18 | -$2,698.40 | -$2,298.72 | -$4,819.46 | -$2,549.33 |
| **Profit Factor** | 2.41 | 2.91 | **3.31** | 2.41 | 2.99 |
| **Expected Payoff** | $35.84 | $73.54 | $71.79 | $48.35 | $77.01 |
| **Total Trades** | **90** | 70 | 74 | 141 | 66 |
| **Win Rate** | **71.11%** | 50.00% | 43.24% | 40.43% | 51.52% |
| **Loss Rate** | 28.89% | 50.00% | 56.76% | 59.57% | 48.48% |
| **Max Drawdown** | **0.32%** | 0.45% | 0.51% | 0.74% | 0.37% |
| **Drawdown Amount** | $322.30 | $464.78 | $523.88 | $760.41 | $386.68 |
| **Average Profit/Trade** | $86.19 | $224.19 | $237.84 | $204.16 | $224.48 |
| **Average Loss/Trade** | -$88.12 | -$77.10 | -$54.73 | -$57.37 | -$79.67 |
| **Largest Profit Trade** | $108.57 | $284.70 | $506.43 | $506.09 | $297.60 |
| **Largest Loss Trade** | -$101.65 | -$111.94 | -$102.32 | -$104.00 | -$111.94 |

---

## Key Findings

### 🏆 Best Performers by Metric

1. **Highest Net Profit:** 0.7DD ($6,817.85)
2. **Best Profit Factor:** 0.5DD (3.31)
3. **Lowest Drawdown:** 0.3DD (0.32%)
4. **Highest Win Rate:** 0.3DD (71.11%)
5. **Best Risk-Adjusted Return:** 0.5DD (Profit Factor 3.31 with 0.51% DD)

### 🔍 Trade-off Analysis

There's a clear **trade-off between risk and return**:
- Higher drawdown limits (0.7DD) yield **higher absolute profits** but with **greater risk**
- Lower drawdown limits (0.3DD) provide **better consistency** but **lower returns**
- The **0.5DD configuration** offers the **best balance** with the highest profit factor

---

## Recommendations

### Based on Trading Style:

#### 1. **Conservative Traders (Capital Preservation Focus)**
- **Recommended:** 0.3DD or 0.3DD-5000P
- **Why:** Lowest drawdown, highest win rate, maximum capital protection

#### 2. **Balanced Traders (Risk-Adjusted Returns Focus)**
- **Recommended:** 0.5DD
- **Why:** Best profit factor (3.31), strong net profit with moderate drawdown

#### 3. **Aggressive Traders (Maximum Returns Focus)**
- **Recommended:** 0.7DD
- **Why:** Highest absolute returns, suitable for high risk tolerance

### General Recommendation:
> **0.5DD configuration** is recommended for most traders as it offers the optimal balance of risk and reward with the highest profit factor.

---

## Important Caveats

1. **Past Performance ≠ Future Results** - These are historical backtests only
2. **Market Conditions Change** - The EA may perform differently in live markets
3. **Re-optimization Required** - The README recommends re-optimizing every 4-6 months
4. **Risk Management Essential** - Never risk more than 0.5% of account per trade
5. **Demo Testing Mandatory** - Always test on demo before deploying to live account

---

## Next Steps

1. **Select configuration** based on your risk tolerance
2. **Test on demo account** for at least 2 weeks
3. **Start with minimum position sizes** when going live
4. **Monitor drawdown closely** - stop trading if it exceeds comfort level
5. **Schedule re-optimization** every 4-6 months

---

## File Information

- **Analysis Date:** 2026-01-10 15:46:35
- **Source Data:** XAUUSD_v2.2_2026_Jan.zip
- **EA Version:** Smart Breakout EA Pro v2.2
- **Broker:** ICMarketsSC-Demo (Build 5430)
- **Time Period:** 2025.01.06 - 2026.01.05 (1 year)
- **Timeframe:** 1H (Hourly)

*This analysis was generated by Agent Zero AI Assistant.*
