---
name: Distance
title: (Weighted) mean distance from the most-liked party
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
math: true
---
## Description
The (weighted) mean distance from the most liked party is a measure suggested by [Wagner (2021)]({{< ref "wagner_affective_2021" >}}), although he considers it inferior to the (weighted) spread. It measures the average discrepancy between like for the most liked party and like/dislike for all other parties. Wagner computes the (weighted) distance based on the CSES dataset, but in principle it can be applied to other datasets that contain the required items, i.e., like-dislike scores.
​
## Operationalization
Wagner proceeds in two steps. First, they calculate the (weighted) mean distance for each respondent. Second, they aggregate to the party-system level by taking the mean of the respondents' distance scores. The unweighted and weighted distance measures are calculated as follows:

Unweighted: $Distance_i = \sqrt{\frac{\sum_{p=1}^p (like_{ip} - like_{max,i})^2}{n_p}}$

Weighted: $Distance_i = \sqrt{\sum_{p=1}^p v_p (like_{ip} - like_{max,i})^2}$

The subscript $i$ denotes an individual respondent, $p$ denotes a party, $max$ is the most liked party, and $v_p$ is the percentage of votes received by a party.
​
## polaR
```r
## Illustrative R code for coding the measure based on the CSES data
cses_imd <- polaR_import(source = "cses_imd", path = "path/to/dataset.dta")

cses_imd <- distance(cses_imd)
```
{{< polarref >}}
​
## Visualization
{{< shinyapp cses "distance,distance_wgt" >}}

## Use cases
_Publication that use this measure:_

| Title                                                                               | Authors       |
| ----------------------------------------------------------------------------------- | ------------- |
| [Affective polarisation in multiparty systems]({{< ref "usecases/wagner_affective_2021.md" >}}) | Wagner (2021) |

