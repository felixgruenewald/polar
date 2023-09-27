---
datasets:
  - cses
  - ches
title: Party Positions on Issue Dimension
---
## Variable description

Short 1-2 sentence description of the variable.
## Measures
```dataview
TABLE Name as "Measure", Polarization, Level
FROM "measures"
WHERE contains(variables, party-position)
```
## Datasets
## [cses]({{< ref "cses" >}})
`Variable name` Variable label
> "question text"

> answers

Further variables:  list names and label of similar variable if same question is asked to multiple parties, for instance, for now it is sufficient to just copy and paste the first 1-2 further variable and end on ,... to indicate that the dataset has more variables