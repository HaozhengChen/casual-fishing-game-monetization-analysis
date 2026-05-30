# 08. Simulated Case Study

## 1. Case Background

A casual fishing-style game launches a 5-day limited event:

**Deep Sea Treasure Boss Challenge**

Rules:

- Players obtain Deep Sea Tickets from normal gameplay.
- Tickets are consumed to enter the Boss Room.
- Boss Room coin consumption is 1.8x normal room consumption.
- Defeating bosses grants event tokens.
- Event tokens can be exchanged for cannon skins, coins, freeze items, and premium rewards.
- A leaderboard is active during the event.
- Event bundles and cumulative recharge rewards are available.

## 2. Simulated Metrics

| Metric | Before Event | During Event | Change |
|---|---:|---:|---:|
| DAU | 100,000 | 108,000 | +8% |
| Event Participation Rate | N/A | 62% | High |
| Payer Rate | 3.2% | 4.1% | +0.9 pct |
| ARPU | 0.85 CNY | 1.08 CNY | +27% |
| ARPPU | 26.5 CNY | 26.3 CNY | Flat |
| D1 Retention | 34% | 30% | -4 pct |
| F2P Bankruptcy Rate | 18% | 31% | +13 pct |
| Mid-spender Event Completion | N/A | 42% | Low |
| Event Bundle Conversion | N/A | 6.5% | Medium |
| Ad Watch Rate | 22% | 35% | +13 pct |

## 3. Positive Signals

| Signal | Possible Explanation |
|---|---|
| DAU increased | Limited-time activity created urgency and freshness |
| Event participation high | Event entry and rewards were attractive |
| Payer rate increased | Resource shortage and event goals triggered purchases |
| Ad watch rate increased | F2P users looked for resource recovery paths |

## 4. Negative Signals

| Signal | Possible Explanation |
|---|---|
| D1 retention decreased | Event pressure caused frustration after participation |
| F2P bankruptcy increased | Boss Room consumption was too high |
| Mid-spender completion low | Event target was not achievable for moderate spenders |
| ARPPU flat | More users paid, but mostly low-price rescue packs |
| Ad watch rate increased but retention dropped | Ads delayed shortage but did not solve pressure |

## 5. Root Cause Analysis

### 5.1 Consumption Curve Too Steep

Boss Room cost is 1.8x normal consumption from the beginning.

Impact:

- F2P users run out of coins quickly.
- Low spenders buy small packs but still cannot progress far.
- Mid spenders feel continuous pressure.

Core issue:

The event creates monetization pressure but does not provide enough segment-specific completion paths.

### 5.2 Leaderboard Rewards Too Top-heavy

If the best rewards are concentrated in top rankings:

- Heavy spenders receive clear competition goals.
- Mid spenders may feel their spending is inefficient.
- F2P users only receive weak participation rewards.

Core issue:

The event over-serves top competition and under-serves middle progression.

### 5.3 Free Supply Is Not Enough

Ad watch rate increased from 22% to 35%, but retention still dropped.

Possible meaning:

- Users want to continue.
- Ad rewards are not enough to sustain event play.
- Free tickets or coins are insufficient.

Core issue:

Rewarded ads are present but not strong enough as a safety valve.

### 5.4 Single Event Target for All Users

The same event structure is applied to all users.

Impact:

- F2P users can only sample the event.
- Low spenders cannot reach meaningful milestones.
- Mid spenders feel pressured.
- Heavy spenders dominate ranking.

Core issue:

The event lacks layered goals.

## 6. Tuning Recommendations

### 6.1 Adjust Consumption Curve

| Item | Current | Suggested Tuning |
|---|---:|---:|
| Boss Room Cost | 1.8x normal | First 3 daily entries at 1.2x, then scale upward |
| Free Tickets | Limited | Daily tasks guarantee 3–5 entries |
| Coin Return | Low | Add participation floor reward |
| High-cost Stage | Starts immediately | Move to advanced difficulty or late event stages |

### 6.2 Add Layered Rewards

| Segment | Goal | Reward |
|---|---|---|
| F2P | Daily participation | Coins, basic items, small tokens |
| Ad Users | Watch ads for extra entries | Tickets, reward doubling |
| Low Spenders | Complete normal exchange path | Item fragments, pass EXP |
| Mid Spenders | Complete event mainline | Full cosmetic, premium items |
| Heavy Spenders | Ranking and high milestones | Title, avatar frame, rare cosmetic |

### 6.3 Improve Leaderboard Structure

Recommended adjustments:

- Add personal milestone rewards.
- Use grouped leaderboards based on player level, spending history, or room tier.
- Keep top rewards more cosmetic than power-based.
- Ensure participation rewards are meaningful.

### 6.4 Improve Rewarded Ad Supply

| Scenario | Adjustment |
|---|---|
| Coin shortage | Higher reward for first few ads, then diminishing returns |
| Ticket shortage | Ads grant limited extra tickets |
| Boss failure | One ad-based retry opportunity |
| Reward doubling | Apply to normal rewards, not premium paid rewards |

### 6.5 Evaluate Event Success Beyond Revenue

Monitor after-event indicators:

| Metric | Purpose |
|---|---|
| Post-event D1 / D3 retention | Check whether event over-consumed users |
| Coin balance distribution | Identify large-scale bankruptcy |
| Mid-spender repeat purchase | Check whether mid payers remain healthy |
| Event completion by segment | Identify unfair difficulty |
| Next event participation | Measure long-term trust |