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
usecases: 
 - hobolt_mobilising_2019
 - bischof_voters_2019
 - moral_relationship_2023
math: true
---
# Description
Of course, polarization, i.e. the distribution of party or voter positions, can also be measured by calculating the standard deviation. It is used by a number of scholars, primarily to measure ideological polarization among the mass public, based on [cses]({{< ref "cses" >}}), [eb]({{< ref "eb" >}}) and [ees]({{< ref "ees" >}}) data.

# Operationalization
The standard deviation of party or voter positions is calculated as follows:
$$s_i = \sqrt{\frac{\sum_{i=1}^n(p_i-\bar{p})^2}{n}}$$
where the subscript $i$ stands for an individual respondent or party, $p_i$ is the position of a respondent or party $i$, $\bar{p}$ is the average position of all respondents or parties, and $n$ is the number of parties or respondents.

# polaR
```
# R code for coding the measure based on some input data
```
We have written a custom R functions for coding this measure and assembled it, along with other functions, into an R package that is still under development. The package can be installed from and the code can be viewed on [GitHub](https://github.com/felixgruenewald/polref). Comments, suggestions, and feature requests are welcome.

<iframe src="https://felixgruenewald.shinyapps.io/polarapp/?dataset=cses,eb,ess&measure=sd"
    frameborder="0"
    scrolling="yes" 
    style="overflow:hidden;width:100%" 
    height="1000" 
    width="100%"></iframe>

# Use cases
*Publications that use this measure*:
```dataview
TABLE without ID Authors, Year, Title, Publication, DOI
FROM [sd]({{< ref "sd" >}})
SORT Year ASC
```
