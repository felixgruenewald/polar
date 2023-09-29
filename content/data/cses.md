---
name: CSES
title: Comparative Study of Electoral Systems
link: https://cses.org/
---
## Description

The Comparative Study of Electoral Systems (CSES) is a collaborative program of election research teams from around the world. The CSES covers a wide range of topics with a focus on the behavior and attitudes of respondents at times of national elections, such as voting and turnout. CSES designs a core questionnaire that is regularly included in many academic national election surveys. 

Launched in 1996, the CSES has included five modules to date, covering topics such as citizens' views of political elites, representation and accountability, and the impact of electoral institutions. With regard to polarization, the CSES questionnaire includes several items that can be used to measure ideological polarization at the elite and mass levels and affective polarization at the mass level.

## Items
Items that can be found in this dataset:
- [Like-Dislike scores of parties]({{< ref "variables/like-dislike.md" >}})
- [Party Positions on Issue Dimension]({{< ref "variables/party-position.md" >}})
- [Issue Self-Positioning]({{< ref "variables/self-positioning.md" >}})

## Measures
Measures that use this dataset:

| Measure                                                        | Polarization | Level       |
| -------------------------------------------------------------- | ------------ | ----------- |
| [API]({{< ref "measures/api.md" >}})                                       | affective    | mass        |
| [Distance]({{< ref "measures/distance.md" >}})                             | affective    | mass        |
| [Spread]({{< ref "measures/spread.md" >}})                                 | affective    | mass        |
| [Party-System Extremism]({{< ref "measures/party-system_extremism.md" >}}) | ideological  | elite       |
| [Polarisation Index]({{< ref "measures/polarisation_index.md" >}})         | ideological  | elite, mass |
| [SD]({{< ref "measures/sd.md" >}})                                         | ideological  | elite, mass |
| [Variance]({{< ref "measures/variance_weighted.md" >}})                    | ideological  | elite       |

## Visualization
<iframe src="https://felixgruenewald.shinyapps.io/polarapp/?dataset=cses&measure=api,polarisation_index,spread_likedislike_wgt"
    frameborder="0"
    scrolling="yes" 
    style="overflow:hidden;width:100%" 
    height="1000" 
    width="100%"></iframe>

## Use cases
Publications that use this dataset:

| Title                                                                                                                            | Authors                        |
| -------------------------------------------------------------------------------------------------------------------------------- | ------------------------------ |
| [The Activists Who Divide Us]({{< ref "usecases/amitai_activists_2023.md" >}})                                                               | Amitai (2023)                  |
| [A regional perspective to the study of affective polarisation]({{< ref "usecases/bettarelli_regional_2023.md" >}})                          | Bettarelli et al. (2023)       |
| [Cleavage politics, polarisation and participation in Western Europe]({{< ref "usecases/borbath_cleavage_2023.md" >}})                       | Borbáth et al. (2023)          |
| [Modeling ideological polarisation in democratic party systems]({{< ref "usecases/dalton_modeling_2021.md" >}})                              | Dalton (2021)                  |
| [The Quantity and the Quality of Party Systems]({{< ref "usecases/dalton_quantity_2008.md" >}})                                              | Dalton (2008)                  |
| [Missing Links in Party-System Polarisation]({{< ref "usecases/curini_missing_2012.md" >}})                                                  | Curini and Hino (2012)         |
| [Party System Polarisation and Electoral Behavior]({{< ref "usecases/dassonneville_party_2021.md" >}})                                       | Dassonneville and Çakır (2021) |
| [Party-System Extremism in Majoritarian and Proportional Electoral Systems]({{< ref "usecases/dow_partysystem_2011.md" >}})                  | Dow (2011)                     |
| [The mobilising effect of political choice]({{< ref "usecases/hobolt_mobilising_2019.md" >}})                                                | Hobolt and Hoerner (2019)      |
| [Party Polarisation and Mass Partisanship]({{< ref "usecases/lupu_party_2015.md" >}})                                                        | Lupu (2015)                    |
| [On the relationship between party polarisation and citizen polarisation]({{< ref "usecases/moral_relationship_2023.md" >}})                 | Moral and Best (2023)          |
| [The relationship between affective polarisation and democratic backsliding]({{< ref "usecases/orhan_relationship_2022.md" >}})              | Orhan (2022)                   |
| [Fear and loathing across party lines (also) in Europe]({{< ref "usecases/reiljan_fear_2020.md" >}})                                         | Reiljan (2020)                 |
| [Patterns of Affective Polarisation toward Parties and Leaders across the Democratic World]({{< ref "usecases/reiljan_patterns_2023.md" >}}) | Reiljan et al. (2023)          |
| [Affective polarisation in multiparty systems]({{< ref "usecases/wagner_affective_2021.md" >}})                                              | Wagner (2021)                  |
| [Meaningful choices, political supply, and institutional effectiveness]({{< ref "usecases/wessels_meaningful_2008.md" >}})                   | Wessels and Schmitt (2008)     |

