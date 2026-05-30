# 03. Currency and Resource System

## 1. Resource System Overview

| Resource | Source | Consumption | Design Purpose | Risk | Observable Metrics |
|---|---|---|---|---|---|
| Soft Currency: Coins | Login rewards, gameplay drops, tasks, ads, bundles, recharge exchange | Ammo firing, room entry, events, upgrades | Main loop resource and shortage driver | Too fast consumption causes churn; too much output weakens payment | Coin balance, coin gap, bankruptcy rate |
| Hard Currency: Diamonds | Recharge, first purchase, premium rewards | Buy bundles, exchange coins, buy items | Connect real money to virtual economy | Over-distribution weakens price perception | Diamond purchase rate, diamond spending |
| Stamina / Tickets | Natural recovery, tasks, ads, bundles | Enter special modes or boss rooms | Control high-value gameplay frequency | Too restrictive damages fun | Entry rate, ticket shortage, stamina usage |
| Ammo / Cannon Cost | Coins, bundles, activity rewards | Core gameplay action | Convert play frequency into resource sink | High multiplier can cause rapid bankruptcy | Firing count, cannon multiplier distribution |
| Items | Tasks, bundles, events, shops | Freeze, lock-on, burst, bomb, revive | Add tactical choices and paid value | Overpowered items create pay-to-win feeling | Item usage, item purchase, boss clear rate |
| Event Tokens | Event tasks, boss rewards, recharge, ranking | Event shop, lottery, milestone rewards | Create short-cycle event economy | Excessive grind or forced spending | Token income, token spending, exchange rate |
| VIP EXP | Recharge, monthly card, paid pass | Not consumed; unlocks privilege | Long-term payer identity and retention | Strong VIP benefits may hurt fairness | VIP distribution, VIP retention |
| Pass EXP | Daily / weekly tasks, event missions | Upgrade pass levels | Build mid-cycle retention target | Too grindy reduces purchase intent | Pass level, purchase rate, completion rate |
| Paid Bundles | Cash purchase, diamond purchase | Provide coins, items, tickets, tokens | Segment monetization and resource relief | Too many packs create fatigue | Exposure, click, conversion, ARPPU |
| Rewarded Ads | Video ads, reward doubling, revival | Provide coins, stamina, tickets | F2P safety valve and ad revenue | High frequency damages experience | Ad watch rate, completion rate, ad ARPDAU |

## 2. Resource Flow Diagram

~~~mermaid
flowchart LR
	A["Player Time"] --> B["Gameplay Sessions"]
	B --> C["Coin / Ammo Consumption"]
	C --> D["Resource Shortage"]
	D --> E["Rewarded Ads"]
	D --> F["Paid Bundles"]
	D --> G["Recharge"]
	B --> H["Tasks / Pass EXP"]
	H --> I["Event Participation"]
	I --> C
	I --> J["Event Tokens"]
	J --> K["Event Shop Rewards"]
~~~

## 3. Key Economy Principles

### 3.1 Coins as the Main Loop Resource

Coins determine whether the player can continue playing. They function as both gameplay fuel and monetization pressure.

Important questions:

- How many minutes can a free player continue after login?
- How often does a player fall below the minimum room entry requirement?
- Does the player have a lower-risk room to return to?
- Does the system offer a fair recovery path?

### 3.2 Hard Currency as Paid Value Carrier

Diamonds or premium currency should preserve price clarity.

Important questions:

- Is the exchange rate understandable?
- Are premium rewards clearly different from free rewards?
- Do too many discounts weaken regular recharge value?

### 3.3 Tickets and Stamina as Activity Gates

Tickets and stamina allow designers to separate high-value event gameplay from normal coin circulation.

Important questions:

- Can free users participate at least a few times per day?
- Are paid users buying efficiency or mandatory access?
- Does the event end before most users can redeem meaningful rewards?

### 3.4 Rewarded Ads as a Safety Valve

Rewarded ads should reduce churn risk without fully replacing paid bundles.

Important questions:

- Does ad reward support short-term continuation?
- Does paid purchase still provide higher efficiency?
- Is ad frequency capped to avoid fatigue?