# Methodology for calculating the stringency index

The stringency index for Brazilian subnational units was calculated based on the ***stringency index*** described in the [OxCGRT Index Methodology 3.1](https://github.com/OxCGRT/covid-policy-tracker/blob/master/documentation/index_methodology.md). We briefly describe this calculation below.

The index is the simple average of the individual component indicators. This is described in equation 1 below where _k_ is the number of component indicators in an index and _I<sub>j</sub>_ is the [sub-index score](#calculating-sub-index-scores-for-each-indicator) for an individual indicator.

![overall mean equation](https://latex.codecogs.com/png.latex?%281%29%5Cqquad%20index%3D%5Cfrac%7B1%7D%7Bk%7D%5Csum_%7Bj%3D1%7D%5E%7Bk%7DI_%7Bj%7D)


## Calculating sub-index scores for each indicator

The index uses ordinal indicators where policies a ranked on a simple numerical scale. Some indicators – C1-C7, and H1 – have an additional binary flag variable that can be either 0 or 1. This flag corresponds to the geographic scope of the policy.

The [subnational codebook](codebook_subnational.md) has details about each indicator and what the different values represent.

Because different indicators (_j_) have different maximum values (_N<sub>j</sub>_) in their ordinal scales, and only some have flag variables, each sub-index score must be calculated separately. The different indicators are:

| Indicator | Max. value (_N<sub>j</sub>_) | Flag? (_F<sub>j</sub>_) |
| --- | --- | --- |
| C1 | 3 (0, 1, 2, 3) | yes=1 |
| C2 | 3 (0, 1, 2, 3) | yes=1 |
| C3 | 2 (0, 1, 2) | yes=1 |
| C4 | 4 (0, 1, 2, 3, 4) | yes=1 |
| C5 | 2 (0, 1, 2) | yes=1 |
| C6 | 3 (0, 1, 2, 3) | yes=1 |
| C7 | 2 (0, 1, 2) | yes=1 |
| C8 | 4 (0, 1, 2, 3, 4) | no=0 |
| H1 | 2 (0, 1, 2) | yes=1 |

Each sub-index score (_I_) for any given indicator (_j_) on any given day (_t_), is calculated by the function described in equation 2 based on the following parameters:

- the maximum value of the indicator (_N<sub>j</sub>_)
- whether that indicator has a flag (_F<sub>j</sub>_=1 if the indicator has a flag variable, or 0 if the indicator does not have a flag variable)
- the recorded policy value on the ordinal scale (_v<sub>j,t</sub>_)
- the recorded binary flag for that indicator (_f<sub>j,t</sub>_)

This normalises the different ordinal scales to produce a sub-index score between 0 and 100 where each full point on the ordinal scale is equally spaced. For indicators that do have a flag variable, if this flag is recorded as 0 (ie if the policy is geographically _targeted_ or for E1 if the support only applies to _informal sector workers_) then this is treated as a half-step between ordinal values.

Note that the database only contains flag values if the indicator has a non-zero value. If a government has no policy for a given indicator (ie the indicator equals zero) then the corresponding flag is blank/null in the database. For the purposes of calculating the index, this is equivalent to a sub-index score of zero. In other words, _I<sub>j,t</sub>_=0 if _v<sub>j,t</sub>_=0.

![sub-index score equation](https://latex.codecogs.com/png.latex?%282%29%5Cqquad%20I_%7Bj%2Ct%7D%3D100%5Cfrac%7Bv_%7Bj%2Ct%7D-0.5%28F_%7Bj%7D-f_%7Bj%2Ct%7D%29%7D%7BN_%7Bj%7D%7D)

(_if v<sub>j,t</sub>=0 then the function F<sub>j</sub>-f<sub>j,t</sub> is also treated as 0, see paragraph above._)
