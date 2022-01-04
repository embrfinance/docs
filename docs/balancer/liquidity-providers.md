# Liquidity Providers

## How do Liquidity Providers earn yield?

When there is a trade in a pool, the pool collects a trade fee. The trade fee is denominated in the input token. Each pool has its own trade fee set based on the underlying assets.
In addition, liquidity providers can stake their LP tokens in the appropriate farms to earn additional EMBR liquidity mining incentives.

## How do I get my trade fees?

As the pool collects fees, your Embr Pool Tokens automatically collect fees because they represent your proportional share of the pool. 

Let's say Alice, Bob, Chuck, and Diana all provide liquidity in the same pool starting out worth $100. After some time, it has earned many trade fees and is now worth $200. The pool itself grows while their proportional shares stay the same. 

| Person | Proportional Share | Initial Value | Value After Trading |
| ------ | ------------------ | ------------- | ------------------- |
|    Alice    |     50.0%               |   $50      |     $100      |
|    Bob    |     25.0%               |   $25      |     $50      |
|    Chuck    |     12.5%               |   $12.50      |     $25      |
|    Diana    |     12.5%              |   $12.50     |     $25      |


## How does a pool determine the price of tokens?

In general the AMM logic determines the prices that traders pay. For example, Weighted Pools, use a constant product formula and Stable Pools, use a StableSwap formula.

## How does the self-balancing index fund work?
Embr allows for the creation of self-balancing index funds. Instead of paying a portfolio manager to continuously rebalance the fund, as investors do with an ETF, liquidity providers collect fees as traders rebalance the trading pools. This works because market actors are incentivized to rebalance the portfolio to take advantage of arbitrage opportunities. 
