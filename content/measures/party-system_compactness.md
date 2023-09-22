---
name: Compactness
title: Party-system compactness
polarisation:
 - ideological
level: 
 - elite
data: 
 - other
variables: 
 - self_positioning
 - party_position
usecases: 
 - alvarez_party_2004
math: true
---
# Description
---
Party-system compactness, proposed by [alvarez_party_2004]({{< ref "alvarez_party_2004" >}}), measures the dispersion of voters' ideological positions relative to the dispersion of parties' positions. Alvarez and Nagler apply the measure to data from the American National Election Study (ANES), the British Election Study (BES), and the Canadian Election Study (CES). In principle, it can also be applied to other survey data, such as the [cses]({{< ref "cses" >}}).

# Operationalization
---
Alvarez and Nagler calculated an unweighted and a weighted version of the measure, the latter using the parties' vote shares as weights. Their measures of party-system compactness are calculated as follows:
$$CP_k = \frac{\sigma_k}{max|(P_{jk}-P_{lk})|} \forall j,l$$
where $CP_k$ is the party-system compactness on issue $k$, $P_{jk}$ is the position of party $j$ on issue $k$, $P_{lk}$ is the position of party $l$ and issue $k$, and $\sigma_k$ is the standard deviation of respondents' position on issue $k$. The weighted version is calculated as follows:
$VWCP_k = \frac{\sigma_k}{\sum_{j=1}^N V_j|(P_{jk}-\bar{P_{k}})|}$
where this formula uses the same concepts and adds $V_j$, which is the vote share of the $j$th party. 

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
FROM [party-system_compactness]({{< ref "party-system_compactness" >}})
SORT Year ASC
```