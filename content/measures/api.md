---
name: API
title: Affective Polarisation Index
polarisation:
  - affective
level:
  - mass
data:
  - cses
variables:
  - like-dislike
usecases:
  - reiljan_fear_2020
  - garzia_affective_2023
  - reiljan_patterns_2023
math: true
datasec: []
---
## Description
The Affective Polarisation Index (API) was developed by [Reiljan (2020)]({{< ref "reiljan_fear_2020" >}}). It is based on Dalton's Polarisation Index and measures the (weighted) average difference between partisans' like of their party, including leaners, and their dislike of all other parties. Reiljan computes the API based on the CSES dataset, but in principle it can be applied to other datasets that contain the required items, i.e., like-dislike scores and partisan identification questions. For example, [Garzia et al. (2023)]({{< ref "garzia_affective_2023" >}}) applies the measure to The West European Voter Dataset and national election studies from Australia, Canada, New Zealand, and the United States.

## Operationalization
Reiljan proceeds in two steps. They first calculate an AP score for each partisan group (i.e., those who at lean toward a party). In a party system with $N$ relevant parties, the relative AP of each party is defined as:
$$AP_n = \sum_{m=1;m\neq n}^N [(Like_n - Like_m) \times (\frac{Vote~share_m}{1-Vote~share_n})]$$
where the subscript $n$ denotes the in-party and $m$ denotes the out-party. Vote shares are expressed as decimals (e.g., 10% = 0.1). In a second step, they calculate the weighted average of all relevant parties' AP score in a given party system as:

$$API = \sum_{n=1}^N (AP_n \times Vote~share_n)$$
Both steps taken together can be expressed as follows:
$$API = \sum_{n=1}^N[\sum_{m=1; m \neq n}^N ((Like_n-Like_m) \times (\frac{Vote~share_m}{1 - Vote~share_n}))\times Vote~share_n]$$

Given a like-dislike scale ranging from 0 to 10, the API score can  range from –10 to +10.
​
## polaR
```r
## Illustrative R code for coding the measure based on the CSES data
cses_imd <- polaR_import(source = "cses_imd", path = "path/to/dataset.dta")

cses_imd <- api(cses_imd)
```
We have written a custom R functions for coding this measure and assembled it, along with other functions, into an R package that is still under development. The package can be installed from and the code can be viewed on [GitHub](https://github.com/felixgruenewald/polref). Comments, suggestions, and feature requests are welcome.
​
<iframe src="https://felixgruenewald.shinyapps.io/polarapp/?dataset=cses&measure=api"
    frameborder="0"
    scrolling="yes" 
    style="overflow:hidden;width:100%" 
    height="1000" 
    width="100%"></iframe>
## Use cases
_Publication that use this measure:_

| Title                                                                                                                            | Authors               |
| -------------------------------------------------------------------------------------------------------------------------------- | --------------------- |
| [Cleavage politics, polarisation and participation in Western Europe]({{< ref "usecases/borbath_cleavage_2023.md" >}})                       | Borbáth et al. (2023) |
| [Affective Polarisation in Comparative and Longitudinal Perspective]({{< ref "usecases/garzia_affective_2023.md" >}})                        | Garzia et al. (2023)  |
| [The relationship between affective polarisation and democratic backsliding]({{< ref "usecases/orhan_relationship_2022.md" >}})              | Orhan (2022)          |
| [Fear and loathing across party lines (also) in Europe]({{< ref "usecases/reiljan_fear_2020.md" >}})                                         | Reiljan (2020)        |
| [Patterns of Affective Polarisation toward Parties and Leaders across the Democratic World]({{< ref "usecases/reiljan_patterns_2023.md" >}}) | Reiljan et al. (2023) |

