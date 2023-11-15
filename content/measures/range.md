---
name: Range
title: Range Between Outer-Right and -Left Parties
polarisation:
  - ideological
level:
  - elite
data:
  - marpor
  - ches
variables:
  - party-position
usecases:
  - abedi_challenges_2002
  - crepaz_impact_1990
  - matakos_electoral_2016
  - andrews_spatial_2009
  - wessels_meaningful_2008
math: true
---
## Description
The range between the two most distant parties on the left-right dimension in a party system is one of the earliest, first used by [Crepaz (1990)]({{< ref "crepaz_impact_1990" >}}), and most widely used measures of ideological polarization. While the measure has mostly been applied to CHES expert ratings and MARPOR estimates of party positions, it is in principle applicable to any estimates of party positions, regardless of their source.

## Operationalization
The range is defined as follows:
$$range = max(lr_p)-min(lr_p)$$

where $lr_p$ is the left-right position of a party $p$ and the measure captures the difference between the left-most and right-most party, i.e., the range.

## polaR
```r
range_data <- range(cses5, issue = "leftright")
```
{{< polarref >}}

## Visualization
{{< shinyapp cses "range_ind,range_agg" >}}

## Use cases
_Publication that use this measure:_

| Title                                                                                                          | Authors                    |
| -------------------------------------------------------------------------------------------------------------- | -------------------------- |
| [Challenges to established parties]({{< ref "usecases/abedi_challenges_2002.md" >}})                                       | Abedi (2002)               |
| [The Spatial Structure of Party Competition]({{< ref "usecases/andrews_spatial_2009.md" >}})                               | Andrews and Money (2009)   |
| [The impact of party polarisation and postmaterialism on voter turnout]({{< ref "usecases/crepaz_impact_1990.md" >}})      | Crepaz (1990)              |
| [Reflections]({{< ref "usecases/mair_reflections_1997.md" >}})                                                             | Mair and Castles (1997)    |
| [Electoral Rule Disproportionality and Platform Polarisation]({{< ref "usecases/matakos_electoral_2016.md" >}})            | Matakos et al. (2016)      |
| [Meaningful choices, political supply, and institutional effectiveness]({{< ref "usecases/wessels_meaningful_2008.md" >}}) | Wessels and Schmitt (2008) |

