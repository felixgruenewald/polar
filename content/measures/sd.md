---
name: SD
title: Standard Deviation
polarisation:
  - ideological
level:
  - elite
  - mass
data:
  - cses
  - eb
  - ees
  - ches
datasec:
  - ess
  - marpor
variables:
  - self-positioning
  - party-position
usecases:
  - hobolt_mobilising_2019
  - bischof_voters_2019
  - moral_relationship_2023
math: true
---
## Description
Of course, polarization, i.e. the distribution of party or voter positions, can also be measured by calculating the standard deviation. It is used by a number of scholars, primarily to measure ideological polarization among the mass public, based on [cses]({{< ref "cses" >}}), [eb]({{< ref "eb" >}}) and [ees]({{< ref "ees" >}}) data.

## Operationalization
The standard deviation of party or voter positions is calculated as follows:
$$s_i = \sqrt{\frac{\sum_{i=1}^n(p_i-\bar{p})^2}{n}}$$
where the subscript $i$ stands for an individual respondent or party, $p_i$ is the position of a respondent or party $i$, $\bar{p}$ is the average position of all respondents or parties, and $n$ is the number of parties or respondents.



## polaR
{{< polarref >}}
``` r
sd_data <- sd_mass(cses5, issue = "leftright")
```

## Visualization
{{< shinyapp "cses,eb" "sd_mass,sd_partyperception,sd_expert_parties" >}}

## Use cases
_Publication that use this measure:_

| Title                                                                                                            | Authors                   |
| ---------------------------------------------------------------------------------------------------------------- | ------------------------- |
| [Do Voters Polarize When Radical Parties Enter Parliament?]({{< ref "usecases/bischof_voters_2019.md" >}})                   | Bischof and Wagner (2019) |
| [The mobilising effect of political choice]({{< ref "usecases/hobolt_mobilising_2019.md" >}})                                | Hobolt and Hoerner (2019) |
| [On the relationship between party polarisation and citizen polarisation]({{< ref "usecases/moral_relationship_2023.md" >}}) | Moral and Best (2023)     |

