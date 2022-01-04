# Pools

## Weighted Pools

Weighted Pools are a generalization of the standard constant product AMM popularized by Uniswap. Each pool can contain up to 8 different tokens and each token is assigned a weight defining what fraction of the pool is made up by each asset. Balancer's weighted pool equation is a generalization of the x*y=k by accounting for uneven weights and more assets:
<center>
![Pool Maths](/images/pool-math.png)
</center>
where V is constant, B is an asset's balance, and W is an asset's weight in the pool.
As the price of each token changes, traders and arbitrageurs rebalance the pool by making swaps. This maintains the desired weighting of the value held by each token whilst collecting trading fees from the traders.

## Stable Pools

For certain assets that are expected to consistently trade at near parity (e.g. different varieties of stablecoins or synthetics) a more efficient design is the StableSwap AMM as popularized by Curve. These pools allow for larger trades of these assets before encountering significant price impact.

## MetaStable Pools (Coming soon)

These are a generalization of stable pools that contain tokens with known exchange rates. They use equations similar to those of stable pools, but can be used to facilitate swaps between tokens that have gradually shifting prices. 

Example use cases:

* DAI/cDAI
    *cDAI slowly accumulates lending fees and appreciates relative to DAI
* ArbitraryStableUsdToken/StaBAL3-USD
    * StaBAL3-USD Pool token collects trade fees relative to other Stable USD tokens

## Liquidity Bootstrapping Pools (Coming soon)

These pools are useful for launching tokens and swapping large amounts over time. They feature weight shifting mechanisms that results in high start prices with continuously changing sell pressure. 