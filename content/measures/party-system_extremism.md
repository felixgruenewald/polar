---
name: Party-System Extremism
title:  Party-System Extremism
polarisation:
 - ideological
level: 
 - elite
data: 
 - eb
 - cses
variables: 
usecases: 
 - ezrow_parties_2008
 - dow_partysystem_2011
math: true
---
## Description
Party-system compactness, proposed by [Ezrow (2008)]({{< ref "ezrow_parties_2008" >}}), measures the dispersion of parties' ideological positions relative to the dispersion of voters' positions, borrowing from [Alvarez and Nagler (2004)]({{< ref "alvarez_party_2004" >}}). Ezrow applies the measure to data from the [eb]({{< ref "eb" >}}), while [Dow (2011)]({{< ref "dow_partysystem_2011" >}}) uses [cses]({{< ref "cses" >}}) data.

## Operationalization 
The weighted version computes as follows:
$$WPE_k=\frac{\sum_{j=1}VS_j|(P_{jk}-\bar{V}_k)|}{\sigma_{vk}}$$
where: $V_k$ is the average left-right self-placement of respondents in country-year $k$, $P_{jk}$ is the ideological position of party $j$ in country-year $k$, $VS_j$ is the vote share for party $j$, and $\sigma_{vk}$ is the standard deviation of respondents' left-right self-placement in country-year $k$.
The unweighted version is computed as follows:
$$UPE_k= \frac{[\sum_{j=1}|(P_{jk}-\bar{V}_k)|] / n}{\sigma_{vk}}$$
where $n$ is the absolute number of parties in country-year $k$.

## Use cases
_Publication that use this measure:_

| Title                                                                                                           | Authors      |
| --------------------------------------------------------------------------------------------------------------- | ------------ |
| [Party-System Extremism in Majoritarian and Proportional Electoral Systems]({{< ref "usecases/dow_partysystem_2011.md" >}}) | Dow (2011)   |
| [Parties' Policy Programmes and the Dog that Didn't Bark]({{< ref "usecases/ezrow_parties_2008.md" >}})                     | Ezrow (2008) |

