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
# Description
The weighted variance of party ideology scores was the first measure used to measure ideological polarization. It was first used by [taylor_party_1971]({{< ref "taylor_party_1971" >}}) and is still very popular. The variance formula includes weights to account for the different sizes of the parties, which some operationalize as seat shares (e.g. [taylor_party_1971]({{< ref "taylor_party_1971" >}}), [hazan_centre_1997]({{< ref "hazan_centre_1997" >}})), while others use vote shares (e.g. [bejar_elite_2020]({{< ref "bejar_elite_2020" >}}), [sigelman_leftright_1978]({{< ref "sigelman_leftright_1978" >}})). The measure has been applied to a variety of data sources, including the [cses]({{< ref "cses" >}}), [wvs]({{< ref "wvs" >}}), and [marpor]({{< ref "marpor" >}}).

# Operationalization
The formula for the weighted variance is as follows:

$$V= \sum_{i=n}^N \omega_i (x_i - \bar{x})^2$$

where $N$ is the number of parties, $\omega_i$ is the vote or seat share of party $p$, $\bar{p}$ is the weighted average of the positions of all parties. If survey data are used, $p_j$ is determined as the average of all respondents' rankings of party $p$.

# polaR
```r
# r code for coding the measure based on some input data
```

We have written a custom R functions for coding this measure and assembled it, along with other functions, into an R package that is still under development. The package can be installed from and the code can be viewed on [GitHub](https://github.com/felixgruenewald/polref). Comments, suggestions, and feature requests are welcome.
# Use cases
*Publications that use this measure*:
```dataview
TABLE without ID Authors, Year, Title, Publication, DOI
FROM [variance_weighted]({{< ref "variance_weighted" >}})
SORT Year ASC
```