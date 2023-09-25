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
usecases:
- abedi_challenges_2002
- crepaz_impact_1990
- matakos_electoral_2016
- andrews_spatial_2009
- wessels_meaningful_2008
math: true
---
# Description
The range between the two most distant parties on the left-right dimension in a party system is one of the earliest, first used by [crepaz_impact_1990]({{< ref "crepaz_impact_1990" >}}), and most widely used measures of ideological polarization. While the measure has mostly been applied to CHES expert ratings and MARPOR estimates of party positions, it is in principle applicable to any estimates of party positions, regardless of their source.

# Operationalization
The range is defined as follows:
$$range = max(lr_p)-min(lr_p)$$

where $lr_p$ is the left-right position of a party $p$ and the measure captures the difference between the left-most and right-most party, i.e., the range.

# polaR
```r
tbd
```
We have written a custom R functions for coding this measure and assembled it, along with other functions, into an R package that is still under development. The package can be installed from and the code can be viewed on [GitHub](https://github.com/felixgruenewald/polref). Comments, suggestions, and feature requests are welcome.

# Use cases
*Publications that use this measure*:

```dataview
TABLE without ID Authors, Year, Title, Publication, DOI
FROM [range]({{< ref "range" >}})
SORT Year ASC
```