﻿# Internal Render Network Team Review on RNP-001 (v2)
## Final Results:
***The Render Network Team approves the elevation of RNP-001 (v2) to Live Pending status; however, requests the author of RNP-001 defer submitting for final vote until the Render Network Foundation officially assumes governance.***
### Summary of Feedback
The Render Network Team has [previously summarized](https://medium.com/render-token/behind-the-network-btn-july-29th-2022-7477064c5cd7) revisions between RNP-001 (v1) and RNP-001 (v2), where additional detail on the Burn-and-Mint Equilibrium (BME) proposal mechanism was provided by the author of RNP-001. Key additions were made, including the inclusion of detailed emission information that modeled out a preliminary emissions cycle. Additionally, more detail on the weighting of emissions across the user base pool over time was discussed.

Like the commentary between RNP-001 (v1) and (v2), there have been some implementation considerations that the Community and the Render Network Team have noted for additional commentary from the RNP-001 Author. These community questions about implementation of the Live Pending RNP-001 (v2) **do not need to be resolved prior to voting on RNP-001**. However, **they will need to be resolved if/once the Burn and Mint Model is implemented**, so have been summarized below.
### Feedback for Commentary:
- **Emissions Cap** - additional definition of how emissions cap mechanism functions in practice will be an important feature in implementation. Key considerations should be:
  - Specificity on what general percentages Net Emissions Cap tokens can be emitted at while not interfering with the BME equilibrium.
  - Modeling to show how net emissions affect supply / demand equilibrium
 
- **Variable Pricing** - dynamic pricing may be needed for the Render Network, so ensuring that the BME would be able to function with Variable and Surge pricing is a key requisite.
  - Because the BME model is priced in *fiat*, it can function regardless of the fiat price, making variable/surge/price adjustments possible.
  - Render Network Team recommends modeling how variable pricing mechanisms would operate with the BME to provide a framework for future RNPs focused on dynamic pricing.
- **Creator Usage Multipliers** - Creator emissions are intended to encourage use on the network. As a result, providing incentives to re-use Creator emissions on the network will help reward the intended behavior of Creator BME emissions.
  - Mechanism(s) for rewarding Creator emission reuse allows the network to weight Creator emissions in such a way that benefits Nodes in the long run, because as Creator emissions are reused, they convert into Node emissions over time.
  - Consider proposing an emission usage multiplier or other incentive mechanism(s) that rewards Creators for reusing emissions on the network.
- **Creator Consistency Rewards** - Creator emissions are designed to encourage “sticky” repeat use of the Render Network. This is important because consistent demand increases the predictability and, therefore, the economic stability for participants in a multi-sided marketplace.
  - Consider including commentary on rewards that encourage consistent, repeat Creator usage - similar to “Availability Rewards'' for Node Operators that can be expanded on in follow up RNPs to RNP-001 (v2).
- **Emissions Release/Unlock Mechanism** 
  - Emissions may benefit from graduated release periods for withdrawal to prevent sudden spikes in supply / demand that harm network equilibrium. Nevertheless they also have to be quickly withdrawable for nodes to pay operational costs.
  - Propose unlock mechanisms in RNP-001 (v2) or commentary on how additional unlock mechanisms can be proposed in follow up RNPs in such a way to complement the BME introduced in RNP-001 (v2), while providing sufficient liquidity for node operators - for example, 24-48 hour unlock.
- **Blockchain Foundation (Which Blockchain)**
  - If the BME model is approved by the community for implementation, it would represent a fundamental shift in tokenomics on the network. Immediate considerations for which blockchain the Render Network should operate on/continue to operate on should be discussed/proposed alongside, given the fundamental re-writing of the Network operations.

## Appendix: Community Comments
-   Concerns initially expressed by the community that the BME model is unsustainable in the long-term. Fears assuaged partially after emissions schedule released by Shayon, though more detailed long-term emissions should be released.
    -  *Render Network Team Member*: "It seems the [initial](https://discord.com/channels/976195870825529354/1002279564254396456/1002773150188187668) [sentiment](https://discord.com/channels/976195870825529354/1002279564254396456/1002781518575448064) [to the proposal](https://discord.com/channels/976195870825529354/1002279564254396456/1002994872418062386) was met with a lot of focus and disdain towards the 107M proposed inflation and the 107M allocated to ‘partners’. Some in the community saw the diluting of the network as unnecessary and deliberately allocated the newly minted coins to partners (almost identical numerical match). The spreadsheet caused a fair chunk of caution and confusion around this particular topic. Is it possible to rework the spreadsheet to provide some clarity for those concerned? - Another user mentioned the spreadsheet for emissions is a little confusing and suggested perhaps a circulating supply schedule with typical cliffs."
- Network User [Pockets](https://discord.com/channels/976195870825529354/1002279564254396456/1002294478318604470) recommends BME model is not introduced on the network until after Multi-render support (Arnold and Redshift) is added “as a 5x increase in payments to node ops at a <10% yearly inflation rate will require a decently sized demand burn to compensate, either that, or make a decent part of this emission also go toward liquidity stakers”. 
  - *Render Network Engineers*: “There are concerns about pegging mechanic launches on specific usage numbers given variability in usage rates (which could be affected by factors outside of Network control such as feature implementation/removal for individual rendering engines).”
- *Render Network Team Member*: "It was mentioned that token rewards and distributions can be variable depending on which “side of the marketplace” needs to be scaled - are there any processes outlined for how this decision is made and by who?  A DAO decision? For some it may be a point for concern that tokens could potentially be allocated in a malicious way."
  - *Render Network Team*: “We suggest that any reward structure not be decided or implemented immediately, at least within the first month if this structure is agreed upon and put into place, for both security and stability reasons."
- Network User [IS00](https://discord.com/channels/976195870825529354/984510098938417193/985109310193430618) asked: “Is it still going to be a fixed dollar value per OBh? If so, this value will have to be adjusted due to technical progress (the future GPUs will provide 10x OBh with the same price tag of the GPU itself). 
Are there going to be any immediate surge price mechanics (Uber-like)?”
  - *Render Network Engineers*: “While surge mechanics are possible, they are not outlined within this proposal, and would need to be better defined/understood in order to be properly reviewed from a technical point of view. 
As the author [Shayon](https://discord.com/channels/976195870825529354/984510098938417193/985895073067720764) responded regarding Tier/OBh shifts: 'tier/OBh prices are likely to change over time, but this is outside the mandate of this proposal; The core of BME is to scale either demand or supply side of multi-sided marketplaces'"
- Network User [ConcordNZ](https://discord.com/channels/976195870825529354/1002279564254396456/1002381605521862686) expressed concerns that increased creator demand would not be properly stoked through token incentives, as a large section of creators are not already within the crypto-space and token incentives would theoretically need to be astronomically lucrative to encourage changes in workflow.
  - *Render Network Team*: "A description of how the BME model is designed to make the Render Network more accessible for non-cryptonative creators will help assuage concerns on crypto-economic rewards for new users."