# IRIS Phase II Automated Research Report

Corpus size: 800 words.
Best current layout: best_greedy_optimized_layout.
Score improvement vs QWERTY control: 34.83%.

## What Improved

The best layout reduced average full-sequence ambiguity from 1.519 to 1.097, with convergence AUC moving from 11.622 to 6.570.
Intent convergence also improved: average uniqueness step is 11.598 for the winner versus 13.481 for the control.

## Why It Improved

Winning layouts improve intent resolution first: they collapse candidate sets earlier, raise reconstruction confidence, and then trade off channel balance, edge-finger load, and hand alternation.
Zero-collision comparison layouts in this run: none.

## Emerging Design Principles

- a and b consistently separate in top_1_percent. (1.000)
- a and c consistently separate in top_1_percent. (1.000)
- a and d consistently separate in top_1_percent. (1.000)
- a and e consistently separate in top_1_percent. (1.000)
- a and f consistently separate in top_1_percent. (1.000)
- a and g consistently separate in top_1_percent. (1.000)
- a and h consistently separate in top_1_percent. (1.000)
- a and i consistently separate in top_1_percent. (1.000)
- a and j consistently separate in top_1_percent. (1.000)
- a and k consistently separate in top_1_percent. (1.000)

## Hypotheses To Test Next

- Test whether zero-collision layouts remain stable on larger phrase and command corpora.
- Test whether the current core-channel target should be lower for comfort.
- Compare multiple hand maps instead of assuming channels 0-4 left and 5-9 right.
- Validate whether the learnability proxy matches human recall tests.

## Assumptions Challenged

- Preserving QWERTY is not supported by the current ambiguity results.
- Pure frequency spreading is not enough; convergence behavior dominates.
- A random layout can beat QWERTY, but evolution and greedy search find better structure.

## Current Limits

- This report is based on corpus simulation, not live human trials.
- The learnability index is a heuristic and should be calibrated experimentally.
- No AI decoder has been built yet; reconstruction quality is inferred from convergence and ambiguity.
