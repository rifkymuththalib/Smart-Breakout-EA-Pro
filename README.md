# Smart Breakout EA Pro - MT5 Expert Advisor

## Overview
Smart Breakout EA Pro is an advanced MetaTrader 5 Expert Advisor designed for breakout trading strategies. This EA uses intelligent breakout detection, multiple filters, and robust risk management to identify and trade high-probability breakout opportunities.

## 📊 Recommended Currency Pairs
The EA has been optimized and tested with the best performance on:
- **XAUUSD** (Gold) - Primary recommendation
- **USDCAD** - Secondary recommendation

While the EA can work on other pairs, these two have shown the most consistent and reliable results.

## ⚙️ Optimization Configuration
The EA should be optimized using the **Fast Genetic Based Algorithm** with **Complex Criterion Max** criterion for best results. This configuration balances optimization speed with finding robust parameter sets.

### Recommended Optimization Settings:
- **Optimization Method**: Fast genetic based algorithm
- **Criterion**: Complex Criterion max
- **Set File**: Use `Optimization Set file/Optimization For All.set`

## 🔧 Complete Optimization & Testing Process

### Step 1: Historical Data Preparation
1. Download **minimum 1 year** of high-quality historical data for your chosen symbol
2. Ensure data quality is good (no gaps, accurate tick data)
3. Use M15 or H1 timeframe for optimization (recommended)

### Step 2: Run Optimization
1. Open MetaTrader 5 Strategy Tester (Ctrl+R)
2. Select **SmartBreakoutEAPro** Expert Advisor
3. Choose your symbol (XAUUSD or USDCAD)
4. Set date range: Minimum 1 year of historical data
5. Click **"Load"** in the Inputs tab and select: `Optimization For All.set`
6. Set Optimization to: **Fast genetic based algorithm**
7. Set Optimization Criterion to: **Complex Criterion max**
8. Click **"Start"** and wait for optimization to complete

### Step 3: Select Best Parameters
After optimization completes:
1. Sort results by **lowest drawdown** (DD%)
2. Look for parameter sets with:
   - Lowest drawdown (typically <20%)
   - Positive profit factor (>1.5)
   - Reasonable number of trades (not too few)
   - Smooth equity curve
3. Select the top 2-3 parameter sets for further testing

### Step 4: Single Backtest
1. Load the best parameter set from optimization
2. Run a **single backtest** on the full 1-year period
3. Analyze the results:
   - Total net profit
   - Profit factor
   - Maximum drawdown
   - Win rate
   - Average profit per trade
   - Equity curve smoothness

### Step 5: Forward Test (1/4 Split)
1. Use the same parameters from Step 4
2. Run a **forward test** on the most recent 1/4 of your data
   - Example: If you used 12 months for optimization, test on the last 3 months
3. Compare forward test results with backtest:
   - Forward test should show similar performance characteristics
   - Drawdown should be within acceptable range
   - Profit factor should remain positive
4. **If forward test fails**: Return to Step 3 and select different parameters

### Step 6: Demo Account Testing (2 Weeks Minimum)
Once you're satisfied with backtest and forward test results:
1. Deploy the EA on a **demo account**
2. Run for **minimum 2 weeks**
3. Monitor performance daily:
   - Check if trades match backtest logic
   - Verify risk management is working correctly
   - Ensure no unexpected errors or issues
   - Track drawdown and profitability
4. **Only proceed to live if demo results are acceptable**

### Step 7: Live Account Deployment
If demo testing is successful:
1. Deploy on a **small live account**
2. Start with **minimum position sizes**
3. Monitor closely for the first week
4. **Risk Management**: Never risk more than **0.5%** of your total account size per trade

## 🔄 Re-Optimization Schedule

**CRITICAL**: The market changes constantly. You **MUST** re-optimize regularly to maintain EA performance.

### Re-Optimization Timeline:
- **Every 4-6 months**: Run a new optimization
- Use the most recent 1 year of data
- Follow Steps 1-7 again
- **Stop live trading** during re-optimization
- Only resume after completing forward test and demo validation

### Why Re-Optimize?
- Market conditions change (volatility, trends, correlations)
- Parameter sets that worked 6 months ago may be outdated
- Regular optimization keeps the EA adaptive to current market behavior
- Prevents strategy decay and reduces risk of losses

## 💰 Risk Management Rules

### Maximum Risk Per Trade: 0.5%
**NEVER exceed 0.5% of your total account balance per trade.**

Example calculations:
- $10,000 account → Maximum $50 risk per trade
- $50,000 account → Maximum $250 risk per trade
- $100,000 account → Maximum $500 risk per trade

### Risk Settings in the EA:
The optimization set includes `InpRiskPercent = 0.5` as the default. This parameter controls position sizing based on your account balance.

### Additional Risk Controls:
- **Max Daily Loss**: Set via `InpMaxDailyLoss` (default: 5%)
- **Max Concurrent Trades**: Limited via `InpMaxConcurrentTrades`
- **Stop Loss**: Automatically calculated using ATR (`InpStopLossATR`)

## 📋 Key EA Parameters

### Breakout Strategy
- **InpBreakoutType**: Type of breakout detection (0-5)
- **InpLookbackPeriod**: Number of bars to look back (10-100)
- **InpMinBreakoutPips**: Minimum breakout size in pips (2-15)
- **InpRequireRetest**: Wait for retest before entry (true/false)
- **InpConfirmationBars**: Bars to wait for confirmation (1-2)

### Risk Management
- **InpRiskPercent**: Risk per trade as % of balance (0.5% recommended)
- **InpMaxDailyLoss**: Maximum daily loss percentage (5% default)
- **InpMaxConcurrentTrades**: Maximum simultaneous trades (1-30)
- **InpStopLossATR**: Stop loss in ATR multiples (0.5-3)
- **InpTakeProfitRatio**: Take profit ratio vs stop loss (1-5)

### Filters
- **InpUseTrendFilter**: Enable trend filter (true/false)
- **InpUseATRFilter**: Enable ATR volatility filter (true/false)
- **InpUseSessionFilter**: Enable trading session filter (true/false)
- **InpUseVolumeFilter**: Enable volume filter (true/false)

### Indicators
- **InpATRPeriod**: ATR calculation period (10-140)
- **InpBollingerPeriod**: Bollinger Bands period (10-30)
- **InpBollingerDeviation**: Bollinger Bands deviation (1-4)

## 🚀 Quick Start Guide

1. **Install the EA** in MT5 Experts folder
2. **Load optimization set**: `Optimization For All.set`
3. **Run optimization** on XAUUSD or USDCAD (minimum 1 year data)
4. **Select parameters** with lowest drawdown
5. **Run forward test** on recent 3 months
6. **Test on demo** for 2 weeks
7. **Deploy to live** with 0.5% risk max
8. **Re-optimize** every 4-6 months

## ⚠️ Important Warnings

1. **Past performance does not guarantee future results**
2. **Always test on demo before going live**
3. **Never risk more than 0.5% per trade**
4. **Stop trading during major news events if EA doesn't have news filter**
5. **Monitor your account regularly**
6. **Re-optimize every 4-6 months without exception**
7. **Market conditions change - what works today may not work tomorrow**

## 📈 Performance Monitoring

Track these metrics weekly:
- Current drawdown vs historical max
- Win rate consistency
- Profit factor trend
- Average trade duration
- Slippage and execution quality

If performance degrades significantly from backtest results, consider:
1. Checking if market conditions have changed
2. Running a new optimization
3. Temporarily stopping the EA until re-optimization is complete

## 📞 Support & Updates

Regularly check for EA updates and improvements. Keep your MT5 terminal updated to the latest version for best performance and stability.

## 📄 License

All rights reserved. This EA is for personal use only.

---

**Remember**: Trading involves significant risk. Only trade with money you can afford to lose. Always use proper risk management and never exceed the 0.5% risk limit per trade.
