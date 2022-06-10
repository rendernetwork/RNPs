## **RNP 001: Burn-and-mint Equilibrium**


| RNP # |           Title           |    Category    |      Author     |   Created  |
|:-----:|:-------------------------:|:--------------:|:---------------:|:----------:|
| 001   | Burn-and-Mint Equilibrium | Core-Technical | Shayon Sengupta | 06-09-2022 |

### Overview

We propose that the usage of RNDR as the payment denomination between artists and node operators continues. Instead, artists would burn the required amount of RNDR in exchange for non-fungible work credits which are distributed to node operators.

Independently of the amount of work that is processed, the network would mint RNDR tokens (or allocate some portion of its treasury reserve) over some epoch. These tokens would be distributed to node operators pro-rata work completed, and potentially weighed against some reputation score. The number of tokens generated would be variable, and we could dynamically adjust this value based on which side of the marketplace needs to be scaled at any given time.

Note that this model is similar to Helium Network’s [Burn-and-Mint equilibrium](https://www.helium.com/token) model.

### Category

This is a core proposal within the technical subcategory.

### Motivation

The key advantage of the burn-and-mint model over the payment token model is twofold:

1. RNDR would be treated as commodity asset, further in line with the network’s long-term aim of establishing a standard for tokenized compute
2. RNDR would have the potential to become a deflationary asset, allowing for strong value accrual to the token in the circumstance of strong network utilization and growth

### Stakeholders

This proposal impacts all members of the Render Network community

### Implementation

The Render Network would switch to a burn-and-mint equilibrium model with capped net emissions. Given that the Render Network is currently a two-sided marketplace, this model would serve node operators, creators and in turn, liquidity providers. Note that this burn-and-mint model has been widely used by the Helium Network (HNT).

The Render Network burn-and-mint model would work as follows:

The network currently consists of two key stakeholders: **Creators** (or parties with jobs-to-be-done) and **Node Operators** (or parties performing jobs-to-be-done).

*Example: The job-to-be-done is “provide rendering power for creators” over the Render Network. The requester is “creators looking to get their projects rendered on the Render Network”. The fulfiller is the actual nodes processing these jobs.*

The primary unit of exchange that intermediates value transfer across the network is the **RNDR Token (RNDR)**, which would act as the proprietary payment currency.

Each job-to-be-done would be priced in USD, and the requestor would burn an equivalent dollar value of RNDR tokens to submit to the network. Once the requestor burns the required amount of base token (RNDR), a set of non-transferrable, non-fungible **Coupon Tokens** (Render Credits) would be issued to requesters and allocated among fulfillers to keep record of jobs completed on the network

1. Note that the amount of base token burned to access the underlying service would be denominated in USD, but the denomination of the tokens burnt would be the base token.
2. The intended effect of this is that the requestor would demonstrate on-chain that the fulfiller has completed the work for the money that was burned.
    
    *Example: A Render Network creator burns $5 worth of RNDR to produce 5 Render Credits, which are non-fungible and non-transferrable*
    

Node operators would be compensated for completing jobs via base-asset issuance incentives:

1. Independent of the base token burning and coupon token issuance process, the network would **mint a number of base tokens per epoch** (set by the network) and distribute them to fulfillers according to predefined rules.
    1. Node operators would therefore be compensated for performing work or providing value on the network in the base token asset. These rewards would generally be segmented into two buckets;
        1. Availability rewards and incentives: Incentives for showing that the fulfiller is available to complete work on the network
        2. Job-to-be-done completion rewards: Incentives for actually completing jobs-to-be-done submitted to the network
    2. Note that the number of base tokens minted in an epoch would not have to be static. It could be variable, as long as it is not a function of burned tokens (this would create a circular dependency, and ultimately defeat the purpose of the BME model)
        
        *Example:* 
        
        *Data transfer rewards (Job-to-be-done completion rewards): If 2% of RNDR burned during an epoch were in the name of Node Operator A as represented in the Render Credits log, then Node Operator A would receive 2% of newly minted RNDR allocated for data transfer rewards.*
        
        *Availability rewards: If the same node were to complete 5% of uptime challenges defined to assess the reliability of the node network, it would receive an additional 5% of newly minted RNDR allocated for availability rewards.*
        

A **net emissions** cap would be designed to ensure that once the supply cap for the base token has been reached by the network, fulfillers are still able to receive rewards for performing work on the network

1. On an epoch by epoch basis, net emissions would “recycle” (i.e. mint) some set of burned base tokens available for use in rewarding fulfillers when there are no longer enough provided through minting.
2. Net emissions allow rewards to exist in later years, while also not extinguishing deflationary pressure after the cap has been reached. However, they need to be capped at some percentage of current issuance to maintain the core burn and mint equilibrium.

Emission amount and distribution per epoch would be **adjusted as per the growth requirements of the networ**k i.e. valued stakeholders at different stages could receive greater shares of emissions.

If the system were running near equilibrium state, the fulfillers would always be paid the appropriate amount. This model assumes that both consumers and service providers never want to actually hold the proprietary payment currency. Rather, this model assumes that service providers only want to hold general purpose currencies.

Let’s assume there are no market speculators and that the network runs on average at about a 10,000 RNDR token rate per month. With this model, the network would be in equilibrium—meaning that the number of tokens in circulation remains unchanged— if 10,000 tokens are burned per epoch.

If usage grows and 15,000 tokens are burned in an epoch, then total supply will decrease, creating upwards price pressure. This upwards price pressure means fewer tokens need to be burned to purchase the same amount of service from the network, bringing the system back into equilibrium.

The same system works in reverse: If usage slows and more tokens are minted than burned in a given month, supply increases, creating downward price pressure, meaning more tokens have to be burned for the same amount of service, bringing the system back to equilibrium.

### Technical Considerations:

Implementation of this new model would require a smart contract migration.

It would also require forming and incentivizing distributed liquidity pools to allow for sufficient liquidity to facilitate automated RNDR purchase.

Here is how the Render Network burn-and-mint model could work for Creators,, Node Operators and Liquidity Providers:

1. **Creators:** On an epoch basis, Creators will receive a percentage of their RNDR spent that epoch back in the form of RNDR token rewards. This could ideally incentivize further use of the network and reward power users by allowing for more creations to be rendered on the Render Network. Percentage returns could be as high as 100% of RNDR spent initially, and could gradually taper as time goes on.

2. **Node operators:** Node operators will be rewarded for performing work or providing value. These rewards could generally be segmented into two buckets:

1. **Coupon Token Rewards:** Incentives for completing jobs submitted to the network
2. **Availability Rewards:** Incentives for node operator liveness

3. **Liquidity Providers:**  Liquidity providers will be rewarded per epoch for contributing staked tokens to the liquidity pools on partnered exchanges, allowing for RNDR to be available for the new burn-and-mint equilibrium system. Liquidity providers could be rewarded with an additional percentage of tokens staked that epoch, as determined by the network.

### Drawbacks

With this proposal, the Network would need to create a balanced emissions schedule with set parameters to ensure that emission quantities are flexible enough to reward the three key stakeholders of the network (node operators, artists, and liquidity providers) proportional to the value they contribute to the growth of the network at any given time.

Emissions quantities would also need to be able to support rewards for new stakeholders or future forms of activity on the network e.g. proof-of-render up-time, content staking.

In addition, the Net Emissions cap will need to be established at some percentage of current issuance to maintain the core burn and mint equilibrium.

Implementation of the BME will be a change to node operators and will have a slight learning curve, however, the new model will greatly benefit all members of the network as a whole once it is up and running.
