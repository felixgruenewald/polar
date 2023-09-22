---
name: Polarisation Index
title: CSES Polarisation Index
polarisation:
  - ideological
level:
  - elite
  - mass
data:
  - cses
variables: 
usecases:
  - dalton_quantity_2008
  - dalton_modeling_2021
  - borbath_cleavage_2023
  - curini_missing_2012
  - amitai_activists_2023
  - matakos_electoral_2016
math: true
---
# Description
---
[dalton_quantity_2008]({{< ref "dalton_quantity_2008" >}}) proposes the Polarization Index, which measures ideological polarization among parties based on CSES respondents' placement of parties on a left-right scale. It is the most widely used measure of ideological polarization and can also be used to measure ideological polarization at the mass level (see [reiljan_fear_2020]({{< ref "reiljan_fear_2020" >}})).

# Operationalization
---
The Polarization Index can be calculated as follows. First, the party positions are calculated as an average of the left-right scores assigned to parties by respondents, and then the polarization index is calculated using the following formula:

$$PI_k = \sqrt{V_{jk} (\frac{P_{jk}-\bar{P_k}}{5})^2 }$$
where $P_{jk}$ is the left-right position of party $j$ in a country-year sample $k$ and $\bar{P_k}$ is the average position of all parties considered. V_{jk}$ is the vote share of party $P_{jk}$.
# polaR

```r
# Illustrative R code for coding the measure based on the CSES data
cses_imd <- polaR_import(source = "cses_imd", path = "datasets/cses/cses_imd.dta")

cses_imd <- cses_polarisation_index(cses_imd)
```
We have written a custom R functions for coding this measure and assembled it, along with other functions, into an R package that is still under development. The package can be installed from and the code can be viewed on [GitHub](https://github.com/felixgruenewald/polref). Comments, suggestions, and feature requests are welcome.
# Use cases
---
*Publications that use this measure*:

```dataview
TABLE without ID Authors, Year, Title, Publication, DOI
FROM [polarisation_index]({{< ref "polarisation" >}})
SORT Year ASC
```