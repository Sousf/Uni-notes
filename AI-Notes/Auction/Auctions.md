## Overview
- An auction takes place between an **auctioneer agent**, who allocates a good or service among a **set of agents called bidders**.
- Auctions are a mechanism to allocate resources in mutli-agent environments


## Key terms
- **Winner determination**: which bidder wins, and what do they pay?
	- **[[First-price auctions]]** - bidder with highest bid is allocated the good
	- **[[Second-price auctions]]** -  bidder with highest bid wins, but pays the price of the second highest bidder.

-  **Knowledge of bids**: who can see the bids?
	- **[[Open-cry]]**: every bidder can see all bids from all other bidders
	- **[[Sealed-bid]]**: bidder can see only its own bids, can't see others' bids

- **Order of bids**: in what order can bids be made?
	- **[[One shot]]**: each bidder can make only one bid
	- **[[Ascending]]**: each successive bid must exceed the previous bid
	- **[[Descending]]**: auctioneer starts from a high price, and each bid must be lower than the previous bid

- **Number of goods**: How many goods are for sale?
	- **[[Single good]]**: only one individual visible good is for sale
	- **[[Many goods]]**: many goods are available in the auction, so bids can include both the price and number of goods wanted by the bidder. Known as a *combinatorial auction*.

- **[[Private value]]**: Each bidder $i$ has a utility value $v_i$ that reflects the worth of the good to the bidder.
- **[[Common value]]**: The worth of the good is the same for all bidders, but that worth is unknown a priori, and must be estimated by each bidder.
- [[Winner's curse]]: The winner might have valued the good too highly because there are no other bids

## Desirable properties of an aunction
- **[[Efficient]]**: The goods go to the agent who values them the most

- **[[Discourage collusion]]**: The auction mechanism should discourage illegal or unfair agreements between two or more bidders to manipulate prices. 

- **[[Dominant Strategy]]**: There exists a dominant strategy for bidders, *where a strategy is dominant if it gives the bidder a better pay-off than any other strategy.* 

- **[[Truth-revealing]]**: The dominant strategy results in bidders revealing their true value for the good

## Types of Auction
[[English Auction]]
[[Dutch Auction]]
[[First-price sealed-bid auction]]
[[Vickrey auction]]


## Case study
- **ebay and Google AdWords**: https://canvas.lms.unimelb.edu.au/courses/124700/pages/week-8-making-complex-decisions-auctions?module_item_id=3519939 (slide 24)
