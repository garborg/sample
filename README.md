## Description
Picking well-balanced treatment groups. Focusing on something that works in all cases first before adding simplified routines for common cases.

## Missing features:
- Weighting some variables more than others
- Let group sizes wander within a band (where balance is more important than exact size, possibly speed)
- Optionally execute split by key rather than by observation
- Optionally measure balance against a reference group (including external/pre-computed) instead of pairwise
- Optionally leaving out some observations
- Ordinal and TimeSeries scales

## Other todos:
- Replace monolithic `balance!` with composable routines
- Smart routine selection -- on one extreme: non-iterative routine when #obs is high relative to #(/levels of)vars
- Because `getmetric` dominates runtime:
    * Smarter data structures for less allocation, updating rather than recomputing metrics
    * Mix in cheaper metrics
    * More reason to focus on smarter routines
