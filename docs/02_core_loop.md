# 02. Core Loop Breakdown

## 1. Core Loop Diagram

~~~mermaid
flowchart TD
	A["Enter Game"] --> B["Claim Login / Offline Rewards"]
	B --> C["Choose Room / Mode / Event"]
	C --> D["Start Gameplay"]
	D --> E["Consume Coins / Ammo / Stamina / Tickets"]
	E --> F["Catch Fish / Defeat Boss / Complete Objective"]
	F --> G["Receive Coins / Items / Event Tokens"]
	G --> H["Complete Tasks / Achievements / Pass Missions"]
	H --> I["Enter Event / Ranking / Boss Challenge"]
	I --> J{"Enough Resources?"}
	J -- "Yes" --> C
	J -- "No" --> K["Resource Shortage Trigger"]
	K --> L{"Supplement Path"}
	L -- "Rewarded Ads" --> M["Watch Ads for Resources"]
	L -- "Paid Bundle" --> N["Buy Starter / Daily / Bankruptcy / Event Pack"]
	L -- "Recharge" --> O["Hard Currency / VIP / Recharge Rewards"]
	M --> C
	N --> C
	O --> C
	J -- "Too Much Pressure" --> P["Exit / Churn Risk"]
~~~

## 2. Step-by-step Analysis

| Step | Player Motivation | System Purpose | Possible Variables |
|---|---|---|---|
| Enter game | Continue progress, collect rewards | Drive DAU and habit formation | Login count, DAU, return interval |
| Claim rewards | Receive free resources | Reduce early friction and support retention | Login reward value, offline reward cap |
| Choose room / mode | Find suitable risk and reward | Segment users by resource level | Entry requirement, room tier, cannon multiplier |
| Start gameplay | Immediate fun and feedback | Activate core loop | Session length, round count, firing frequency |
| Consume resources | Participate and pursue rewards | Create resource sink | Coin cost, ammo cost, stamina cost, ticket cost |
| Defeat target | Obtain reward and excitement | Provide variable reward feedback | Drop rate, payout multiplier, boss HP |
| Receive reward | Continue playing and progress | Balance resource return | Expected reward, net resource change |
| Complete tasks | Gain structured objectives | Increase session depth | Task completion, pass EXP, activity points |
| Enter event | Pursue limited rewards | Increase activity participation and consumption | Event participation, event token output |
| Resource shortage | Desire to continue despite shortage | Trigger monetization or ad supply | Resource gap, bankruptcy rate |
| Ads / bundles / recharge | Continue gameplay or gain advantage | Monetize shortage and motivation | Ad watch rate, bundle conversion, payer rate |
| Exit / churn | Stop when pressure exceeds motivation | Risk indicator | Churn rate, next-day retention, negative feedback |

## 3. Core Design Logic

A casual / fishing-style monetization loop depends on the tension between:

- Immediate gameplay reward
- Continuous resource consumption
- Controlled shortage
- Optional replenishment
- Event-driven motivation
- Segment-specific monetization

The loop should create enough resource pressure to make rewards, ads, and bundles meaningful, but not so much pressure that non-paying or low-paying users feel blocked too early.