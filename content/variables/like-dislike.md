---
datasets:
  - cses
title: Like-Dislike scores of parties
---
## Variable description
Short 1-2 sentence description of the variable.

## Measures
```dataview
TABLE Name as "Measure", Polarization, Level
FROM "measures"
WHERE contains(variables, like-dislike)
```
## Datasets
## [cses]({{< ref "cses" >}})

`IMD3008_A` LIKE-DISLIKE - PARTY A
> "I'd like to know what you think about each of our political parties. After I read the name of a political party, please rate it on a scale from 0 to 10, where 0 means you strongly dislike that party and 10 means that you strongly like that party. If I come to a party you haven't heard of or you feel you do not know enough about, just say so. The first party is [PARTY A]."

> 00. STRONGLY DISLIKE
> 01.
> 02.
> 03.
> 04.
> 05.
> 06.
> 07.
> 08.
> 09.
> 10. STRONGLY LIKE
> 
> 96. HAVEN'T HEARD OF PARTY
> 97. VOLUNTEERED: REFUSED
> 98. DON'T KNOW ENOUGH ABOUT/DON'T KNOW WHERE TO RATE
> 99. MISSING

Further variables: `IMD3008_B` LIKE-DISLIKE - PARTY B, ...