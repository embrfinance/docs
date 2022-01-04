# Token Emissions

Minting EMBR
We utilize MasterChef for minting and distribution of new EMBR tokens. The MasterChef contract is the owner of the EMBR token. See the owner section on the EMBR contract.

This means only the MasterChef has the permission to mint new EMBR tokens. There is no way to transfer ownership of the EMBR token from the MasterChef. 

## Distrubution

The reminaing 78% of the total supply will be minted over 4 years following the Emission Schedule. The emissions will be distributed as follows:

<center>

| Allocation | % of Max Supply | Number of Tokens After 3 Years |
| ----------------- | ------------------------------------ | ------ |
| LP Farm Rewards | 68%  |  17,000,000 |
| Treasury Funds | 10%  |  2,500,000 |

</center>

## Emmission Schedule 

Using the MasterChef for minting and distribution of those flamy new EMBR. Following the emission schedule, the MasterChef mints the set amount of EMBR per Second. 10% of them are minted directly to the Treasury multisig wallet. The remaining 90.0% are distributed to all farms according to their weight. 

TBD. Current schedule based on EMBR / block but is being reworked to emit over time to account for avalanches variable block times.

People joining a farm receive their share of those emissions based on their share of the total liquidity in this farm. Lets see how this works in a sample:

Lets assume these numbers:  

*  we mint 10 EMBR per second according to the emission schedule
*  we have 5 farms, all with a weight of 20. The weight of all farms combined is 100. This means each farm has 20% of the total rewards.
*  We enter with 100$ into farm A which pushes the total value locked in this farm to 1000$.

```
// First we need to get the amount of EMBR the farm we entered received
shareOfOurFarm = weightOfMyFarm / totalWeight // 20 / 100 = 0.2
embrForOurFarm = embrPerSec * shareOfOurFarm // 10 * 0.2 = 2
// now we know, our farm gets 0.2 EMBR per block.
// next we need to know how much our share is of those EMBR
 ourShare = ourInvestment / totalInvestments // 100 / 1000 = 0.1
 // so we own 10% of the liquidity in this farm, this means
 // we should get 10% of the EMBR
 ourRewardedEMBR = ourShare * embrForOurFarm // 0.1 * 2 = 0.2
 // so this means, we get 0.2 EMBR for each second we stay in the farm.
 // after 3600 seconds (one hour), we can harvest 720 EMBR
```