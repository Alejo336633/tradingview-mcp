---
name: trading-daily
description: Generate a daily pre-market trading brief with live market data, trade setups, and risk management plan. Uses TradingView MCP + web search.
---

# Daily Trading Brief

Generate a comprehensive pre-market trading analysis. Follow this exact workflow:

## Step 1: Check TradingView Connection
Try `tv_health_check`. If TradingView is not running, note it and proceed with web data only.

## Step 2: Gather Market Data

### If TradingView is connected:
1. Run `chart_get_state` to see what's loaded
2. Run `batch_run` with symbols `["ES1!", "NQ1!", "BTCUSD", "ETHUSD"]` and action `"get_ohlcv"` with `summary: true`
3. Run `data_get_study_values` for indicator readings
4. Run `data_get_pine_lines` for key levels
5. Run `capture_screenshot` for visual reference

### Always (web search):
Search for these in parallel:
- "stock market today pre-market futures S&P 500" (current date)
- "bitcoin ethereum crypto price today" (current date)  
- "forex EUR USD GBP USD today" (current date)
- "economic calendar this week events CPI FOMC" (current date)

## Step 3: Analyze & Produce Brief

Create an Artifact page (HTML) with the daily brief containing:

1. **Alert Banner** — Today's key event/catalyst
2. **Market Tiles** — Price snapshots for major instruments
3. **Market Context** — Macro analysis in plain Spanish
4. **Trade Setups Table** — Max 4 setups with entry, SL, TP, R:R, risk level, condition
5. **Capital Plan** — Sizing recommendations by account tier
6. **Monthly Target** — 3-5% realistic monthly goal with math
7. **Risk Rules** — The 6 non-negotiable rules

## Step 4: Recommendations

End with specific action items:
- What to watch before market open
- Which setups to prepare orders for
- When to check back for updates

## Model Usage
- Use Fable 5.2 for daily brief generation (fast, cheap)
- Escalate to Opus 5.5 for complex analysis or Pine Script work
- Use Haiku 5.5 for quick price checks during the day

## Language
All output in Spanish. Technical terms in English where standard (stop loss, take profit, etc.)
