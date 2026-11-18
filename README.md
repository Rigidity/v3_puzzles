# Project overview


These puzzles are designed to implement concentrated liquidity in chia. This is still in a working progress and I would appreciate any feedback as the project progresses.

# Design overview
## Pool singleton
In simple terms, the pool singleton will have information about the current tick with all prices stored as the square root price scaled to 10**12. All pricing will be done in mojo pricing rather than converting between different mojos per CAT. The web interface will then interpret the non-human readable amounts to more readable amounts with different puzzles operating with non-human readable amounts. This is just to make the puzzle easier to design.
## Tick singleton
This singleton will store a list with different ticks. Each tick will contain the tick index defined as stored price / ticking spacing, scaled sqrt tick price, gross liquidity, net liquidity, amount0 fees, and amount1 fees.
## Liquidity vault singletons (2 per pool)
These singletons will store the reserve currencies for each pool, but will only be able to be spent with swapping, adding liquidity, or removing liquidity.
## Position singletons
These will store the pool_id, upper price, lower price, and liquidity, one singleton per liquidity provider. This would need to me autheniticated with the pool somehow so nobody cannot make arbitary position singletons.