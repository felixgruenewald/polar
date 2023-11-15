---
name: Dispersion
title: (Weighted) Party System Dispersion
polarisation:
  - ideological
level:
  - elite
data:
  - marpor
variables:
  - party-position
usecases:
  - ezrow_variance_2007
  - dreyer_does_2019,
math: true
---
## Description
[Ezrow (2007)]({{< ref "ezrow_variance_2007 " >}}) proposed the (Weighted) Party System Dispersion measure, which is basically a weighted standard deviation formula. Both [Ezrow (2007)]({{< ref "ezrow_variance_2007" >}}) and [Dreyer and Bauer (2019)]({{< ref "dreyer_does_2019" >}}) use MARPOR data to measure party positions, but in principle it can be used with other datasets that contain the required information, i.e. party positions.

## Operationalization
The (weighted) party system dispersion is measured as follows:

$Weighted~party~system~dispersion = \sqrt{\sum_{j=1} VS_{j} (P_{jk} - \bar{P}_k)^2}$

where $P_{jk}$ is the ideological position of party $j$ in country $k$ and $\bar{P_k}$ is the weighted average of the left-right ideological positions of all parties in country year $k$. $VS_j$ is the vote share of party $j$ in the last national election.

## Visualization
{{< shinyapp cses "dispersion" >}}

## Use cases
_Publication that use this measure:_

| Title                                                                             | Authors                 |
| --------------------------------------------------------------------------------- | ----------------------- |
| [Does voter polarisation induce party extremism?]({{< ref "usecases/dreyer_does_2019.md" >}}) | Dreyer and Bauer (2019) |
| [The Variance Matters]({{< ref "usecases/ezrow_variance_2007.md" >}})                         | Ezrow (2007)            |

