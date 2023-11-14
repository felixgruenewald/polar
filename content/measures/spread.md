---
name: Spread
title: (Weighted) Spread of like-dislike scores
polarisation:
  - affective
level:
  - mass
data:
  - cses
variables:
  - like-dislike
usecases:
  - wagner_affective_2021
  - bettarelli_regional_2023
  - borbath_cleavage_2023
  - garzia_affective_2023
math: true
---
## Description
The (weighted) spread of like-dislike scores is a measure originally proposed by Wagner (2020), who considers it superior to the [distance]({{< ref "distance" >}}) from the most-liked party, and has since been used by a number of scholars to measure affective polarization. It measures the average spread of party like-dislike scores within respondents, weighted by the size of the parties. To aggregate to the party system, one simply calculates the unweighted average of all respondents' [spread]({{< ref "spread" >}}) scores. Wagner computes the (weighted) spread of like-dislike scores based on the CSES dataset, but in principle it can be applied to other datasets that contain the required items, i.e., like-dislike scores.

## Operationalization
Wagner proceeds in two steps. First, they calculate the (weighted) spread of like-dislike scores for each respondent. Second, they aggregate to the party-system level by taking the mean of the respondents' distance scores. The unweighted and weighted distance measures are calculated as follows:

## Individual-level

Spread: $Spread_i = \sqrt{\frac{\sum_{p=1}^p (like_{ip} - \bar{like_i})^2}{n_p}}$

Weighted spread:  $Spread_i = \sqrt{\sum_{p=1}^p v_p (like_{ip} - \bar{like_i})^2}$

where $i$ = individual, $p$ = party, $v_p$ voteshare of party $p$, and $\bar{like_i} = \sum_{p=1}^p (v_{p} like_{ip})$ 

Aggregation to the party system is done by taking the unweighted mean of all respondents' affective polarization scores:

$Spread_k = \frac{\sum_{i=1}^n Spread_{ik}}{N_{ik}}$

This means that the spread of party like-dislike scores at the party system level $k$ is obtained by summing the spread score of all respondents $i$ in a country-year sample $k$ and dividing by the number of respondents $N_k$.

## polaR
```r 
## Illustrative R code for coding the measure based on the CSES data
cses_imd <- polaR_import(source = "cses_imd", path = "datasets/cses/cses_imd.dta")

cses_imd <- spread_likedislike(cses_imd)
```
We have written a custom R functions for coding this measure and assembled it, along with other functions, into an R package that is still under development. The package can be installed from and the code can be viewed on [GitHub](https://github.com/felixgruenewald/polref). Comments, suggestions, and feature requests are welcome.

## Visualization
<iframe src="https://felixgruenewald.shinyapps.io/polarapp/?dataset=cses&measure=spread_likedislike,spread_likedislike_wgt"
    frameborder="0"
    scrolling="yes" 
    style="overflow:hidden;width:100%" 
    height="1000" 
    width="100%"></iframe>

## Use cases
_Publication that use this measure:_

| Title                                                                                                     | Authors                  |
| --------------------------------------------------------------------------------------------------------- | ------------------------ |
| [A regional perspective to the study of affective polarisation]({{< ref "usecases/bettarelli_regional_2023.md" >}})   | Bettarelli et al. (2023) |
| [Affective Polarisation in Comparative and Longitudinal Perspective]({{< ref "usecases/garzia_affective_2023.md" >}}) | Garzia et al. (2023)     |
| [Affective polarisation in multiparty systems]({{< ref "usecases/wagner_affective_2021.md" >}})                       | Wagner (2021)            |

