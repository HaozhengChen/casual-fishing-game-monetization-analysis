# 05. User Segmentation

## 1. Segmentation Model

~~~mermaid
flowchart TD
	A["User Analysis"] --> B{"Paid in last 7 days?"}
	B -- "No" --> C{"Watched rewarded ads?"}
	C -- "No" --> D["F2P User"]
	C -- "Yes" --> E["Ad User"]
	B -- "Yes" --> F{"Payment Amount"}
	F -- "Low" --> G["Low Spender"]
	F -- "Medium" --> H["Mid Spender"]
	F -- "High" --> I["Heavy Spender"]
	A --> J{"Activity decreasing?"}
	J -- "Yes" --> K["Churn-risk User"]
	A --> L{"Returned after inactivity?"}
	L -- "Yes" --> M["Returning User"]
~~~

## 2. Segment Table

| Segment | Behavior | Systems of Interest | Operation Strategy | Triggered Offers / Events | Metrics |
|---|---|---|---|---|---|
| F2P | Does not pay; relies on free rewards | Login, daily tasks, rewarded ads, low-entry events | Ensure basic playability and reduce early pressure | Free pack, ad reward, 7-day login | D1 / D7 retention, coin gap, churn |
| Ad User | Watches ads for resources | Rewarded video, reward doubling, revival | Improve ad value while limiting fatigue | Ad chest, ad task, free draw | Ad watch rate, completion rate, ad ARPDAU |
| Low Spender | Buys low-price packs occasionally | First purchase, daily pack, bankruptcy pack | Provide clear value and low-friction payment | Starter pack, daily pack, low pass tier | First purchase rate, repeat purchase |
| Mid Spender | Pays during events and pass cycles | Battle pass, weekly pack, event pack | Provide achievable event goals | Weekly pack, event milestone pack | ARPPU, event completion, payer retention |
| Heavy Spender | Pays frequently; competes for ranking | VIP, cumulative recharge, ranking, rare cosmetics | Provide status, competition, and rare rewards | High-tier recharge, ranking push pack | High payer retention, VIP distribution |
| Returning User | Comes back after inactivity | Return tasks, catch-up rewards | Reduce return friction and rebuild habit | Return pack, 7-day return mission | Return rate, return D1 / D7 retention |
| Churn-risk User | Activity decline, repeated shortage, failed tasks | Bankruptcy protection, easy tasks, recovery rewards | Reduce frustration and offer short-term goals | Recovery pack, free supply, low-pressure event | Activity decline, exit point, shortage frequency |

## 3. Segment-specific Design Logic

### F2P Users

F2P users provide activity, community volume, ad revenue, and long-term conversion potential. The system should not block them too early.

Design focus:

- Basic daily resource floor
- Low-pressure activity targets
- Rewarded ads as continuation support
- Clear but non-forced first purchase exposure

### Low Spenders

Low spenders need high clarity and low regret.

Design focus:

- Small price points
- Visible value comparison
- Useful resources rather than luxury-only rewards
- Purchase timing tied to real gameplay need

### Mid Spenders

Mid spenders are sensitive to fairness and goal attainability.

Design focus:

- Milestone rewards
- Achievable event targets
- Pass completion confidence
- Avoid putting all meaningful rewards behind top rankings

### Heavy Spenders

Heavy spenders need status, competition, and long-term identity.

Design focus:

- VIP growth
- Ranking competition
- Rare cosmetics
- High-value recharge goals
- Avoid excessive direct power gap in casual environments