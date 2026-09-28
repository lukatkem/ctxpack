# How the three packers differ

Given the teaching case (4 docs, 400-char budget, one 300-char doc scored 8.0):

- **greedy** takes the 8.0 doc first, exhausts the budget → total score **8.0**
- **density** skips it (8.0/300 chars is terrible value-per-character) and packs
  three smaller docs → total **15.0**
- **exact** runs a knapsack DP over bucketed character costs → **15.0** optimally

When to use which: greedy when scores already encode size trade-offs, density
when they don't, exact when the budget is hard and the score is the contract.
