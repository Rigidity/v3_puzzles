# Project over view

These puzzles are designed to implement concentrated liquidity in chia. This is still in a working progress and I would appreciate any feedback as the project progresses.

# Design overview
## Pool singleton
In simple terms, the pool singleton will have information about the current tick with all prices stored as the square root price scaled to 10**12. All priceing will be done in mojo pricing rather than converting between different mojos per CAT. The web interface will then interpret the non human readable amounts to more readable amounts with different puzzles operating with non human readable amounts. This is just to make the puzzle easier to design.
## Tick singleton
## Liquidity vault singleton