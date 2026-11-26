---
name: sales-planning
description: Builds menu-mix-based sales forecasts, order targets, realized average order value, and six-month revenue scenarios.
---

# Sales Planning

## Purpose
Turn menu economics and demand assumptions into an operational sales forecast.

## Inputs
- Menu item and bundle prices
- Expected paid order count
- Item mix / basket composition
- Realized discounts and promotions
- Days and hours open
- Production and handoff capacity
- New vs repeat customer orders

## Model rules
1. Forecast orders by channel and customer type, not only a single total.
2. Forecast item/basket mix across all menu categories. Never assume every order is a combo.
3. Distinguish orders from items: one order may contain multiple items; the user currently expresses the target as orders/day.
4. Calculate realized average order value from weighted basket mix and actual discount rates. If the mix is unknown, show sensitivity ranges, not a fabricated point estimate.
5. Monthly orders = daily average paid orders × actual open days. Use calendar month lengths or clearly state a 30-day planning month.
6. Net sales = paid order count × realized average order value. Sampled meals produce zero sales.
7. Under the user's current planning assumption: total costs = 50% of sales; contribution = sales × 50%. Explicitly flag costs not included if the user later identifies any.
8. Never double-count combo components or treat list price as realized revenue after a discount.
9. Constrain forecast to realistic demand and assembly/handoff capacity; operator-stated capacity is a ceiling, not demand.
10. Present conservative, base, and upside scenarios with formulas and assumptions.

## Required monthly table
Month | paid orders/day | paid orders/month | average realized order value | sales | assumed costs (50%) | contribution | new customers | repeat orders | samples | main growth driver.

## Decision rules
- If order growth rises but realized AOV falls, inspect discount dependence and mix.
- If samples/QR scans rise without first paid orders, test offer, menu clarity, and ordering friction.
- If first orders rise but repeat purchase stays low, investigate food consistency, wait time, value, and retention offers.
