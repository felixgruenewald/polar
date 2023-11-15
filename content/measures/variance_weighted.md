---
name: Variance
title: Weighted Variance
polarisation:
  - ideological
level:
  - elite
data:
  - cses
  - wvs
  - marpor
variables:
  - party-position
usecases:
  - sigelman_leftright_1978
  - hazan_centre_1997
  - bejar_elite_2020
  - birch_political_2020
  - lupu_party_2015
  - taylor_party_1971
  - dassonneville_party_2021
math: true
---
## Description
The weighted variance of party ideology scores was the first measure used to measure ideological polarization. It was first used by [Taylor and Herman (1971)]({{< ref "taylor_party_1971" >}}) and is still very popular. The variance formula includes weights to account for the different sizes of the parties, which some operationalize as seat shares (e.g., [Taylor and Herman (1971)]({{< ref "taylor_party_1971" >}}), [Hazan (1997)]({{< ref "hazan_centre_1997" >}})), while others use vote shares (e.g., [Béjar et al. (2020)]({{< ref "bejar_elite_2020" >}}), [Sigelman and Yough (1978)]({{< ref "sigelman_leftright_1978" >}})). The measure has been applied to a variety of data sources, including the [cses]({{< ref "cses" >}}), [wvs]({{< ref "wvs" >}}), and [marpor]({{< ref "marpor" >}}).

## Operationalization
The formula for the weighted variance is as follows:

$$V= \sum_{i=n}^N f_i (x_i - \bar{x})^2$$

where $N$ is the number of parties, $f_i$ is the vote or seat share of party $i$, $x_i$ is the ideological position of party $i$, and $\bar{x}$ is the weighted average of the positions of all parties. If survey data are used, $x_i$ is determined as the average of all respondents' rankings of party $f$.

## polaR
```r
variance_data <- variance(cses5)
```
{{< polarref >}}

## Visualization
{{< shinyapp cses "variance_wgt" >}}

## Use cases
_Publication that use this measure:_

| Title                                                                                      | Authors                        |
| ------------------------------------------------------------------------------------------ | ------------------------------ |
| [Elite polarisation and voting turnout in Latin America]({{< ref "usecases/bejar_elite_2020.md" >}})   | Béjar et al. (2020)            |
| [Political polarisation and environmental attitudes]({{< ref "usecases/birch_political_2020.md" >}})   | Birch (2020)                   |
| [Party System Polarisation and Electoral Behavior]({{< ref "usecases/dassonneville_party_2021.md" >}}) | Dassonneville and Çakır (2021) |
| [Centre Parties]({{< ref "usecases/hazan_centre_1997.md" >}})                                          | Hazan (1997)                   |
| [Party Polarisation and Mass Partisanship]({{< ref "usecases/lupu_party_2015.md" >}})                  | Lupu (2015)                    |
| [Left-Right Polarisation In National Party Systems]({{< ref "usecases/sigelman_leftright_1978.md" >}}) | Sigelman and Yough (1978)      |
| [Party Systems and Government Stability]({{< ref "usecases/taylor_party_1971.md" >}})                  | Taylor and Herman (1971)       |

