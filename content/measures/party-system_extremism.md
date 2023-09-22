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
# Description
---
Party-system compactness, proposed by [ezrow_parties_2008]({{< ref "ezrow_parties_2008" >}}), measures the dispersion of parties' ideological positions relative to the dispersion of voters' positions, borrowing from [alvarez_party_2004]({{< ref "alvarez_party_2004" >}}). Ezrow applies the measure to data from the [eb]({{< ref "eb" >}}), while [dow_partysystem_2011]({{< ref "dow_partysystem_2011" >}}) uses [cses]({{< ref "cses" >}}) data.
​￼# Operationalization
 
The weighted version computes as follows:
$$WPE_k=\frac{\sum_{j=1}VS_j|(P_{jk}-\bar{V}_k)|}{\sigma_{vk}}$$
where: $V_k$ is the average left-right self-placement of respondents in country-year $k$, $P_{jk}$ is the ideological position of party $j$ in country-year $k$, $VS_j$ is the vote share for party $j$, and $\sigma_{vk}$ is the standard deviation of respondents' left-right self-placement in country-year $k$.
The unweighted version is computed as follows:
$$UPE_k= \frac{[\sum_{j=1}|(P_{jk}-\bar{V}_k)|] / n}{\sigma_{vk}}$$
where $n$ is the absolute number of parties in country-year $k$.

# polaR
---
```r
# R code for coding the measure based on some input data
```
We have written a custom R functions for coding this measure and assembled it, along with other functions, into an R package that is still under development. The package can be installed from and the code can be viewed on [GitHub](https://github.com/felixgruenewald/polref). Comments, suggestions, and feature requests are welcome.

# Use cases
---
*Publications that use this measure*:

```dataview
TABLE without ID Authors, Year, Title, Publication, DOI
FROM [party-system_extremism]({{< ref "party-system_extremism" >}})
SORT Year ASC
```