---
datasets:
  - cses
  - ches
title: Party Positions on Issue Dimension
object:
  - left-right
  - left-right-economic
---
## Variable description

Short 1-2 sentence description of the variable.

## Datasets & Variants
### [CSES]({{< ref "cses" >}})
###### `E3019_A` LEFT-RIGHT - PARTY A
> "In politics people sometimes talk of left and right. Where would you place [PARTY A] on a scale from 0 to 10 where 0 means the left and 10 means the right?"

> 00. LEFT
> 01.
> 02.
> 03.
> 04.
> 05.
> 06.
> 07.
> 08.
> 09.
> 10. RIGHT
> 
> 95. VOLUNTEERED: HAVEN'T HEARD OF LEFT‐RIGHT
> 96. VOLUNTEERED: HAVEN'T HEARD OF PARTY
> 97. VOLUNTEERED: REFUSED
> 98. VOLUNTEERED: DON'T KNOW WHERE TO PLACE
> 99. MISSING

Further variables: `E3019_B`LEFT_RIGHT - PARTY B, `E3019_C`LEFT_RIGHT - PARTY C, `E3019_D`LEFT_RIGHT - PARTY D, `E3019_E`LEFT_RIGHT - PARTY E, `E3019_F`LEFT_RIGHT - PARTY F, `E3019_F`LEFT_RIGHT - ADDITIONAL - PARTY G, `E3019_H`LEFT_RIGHT - ADDITIONAL - PARTY H, `E3019_I`LEFT_RIGHT - ADDITIONAL - PARTY I.

### [CHES]({{< ref "ches" >}})
###### `LRGEN`Overall ideological stance
> "Position of the party in YEAR in terms of its overall ideological stance."

> 0. EXTREME LEFT
> 1.
> 2.
> 3.
> 4.
> 5. CENTER
> 6.
> 7.
> 8.
> 9.
> 10. EXTREME RIGHT

Further variables: -

###### `LRECON`Ideological stance on economic issues
> "Position of the party in YEAR in terms of its ideological stance on economic issues. Parties can be classified in terms of their stance on economic issues such as privatization, taxes, regulation, government spending, and the welfare state. Parties on the economic left want government to play an active role in the economy. Parties on the economic right want a reduced role for government."

> 0. EXTREME LEFT
> 1.
> 2.
> 3.
> 4.
> 5. CENTER
> 6.
> 7.
> 8.
> 9.
> 10. EXTREME RIGHT 

Further variables: -

###### `GALTAN`Position on social and cultural issues
>"position of the party in 2019 in terms of their views on social and cultural values. “Libertarian” or “postmaterialist” parties favor expanded personal freedoms, for example, abortion rights, divorce, and same-sex marriage. “Traditional” or “authoritarian” parties reject these ideas in favor of order, tradition, and stability, believing that the government should be a firm moral authority on social and cultural issues."

> 0. LIBERTARIAN / POSTMATERIALIST
> 1.
> 2.
> 3.
> 4.
> 5. CENTER
> 6.
> 7.
> 8.
> 9.
> 10. TRADITIONAL / AUTHORITARIAN

Further variables: -

### [EES]({{< ref "ees" >}})
###### `...` Party left right
> "And about where would you place the following political parties on this scale? Which number from 0 to 10, where '0' means "left" and '10' means "right" best describes these parties?"

> 0. LEFT
> 1.
> 2.
> 3.
> 4.
> 5.
> 6.
> 7.
> 8.
> 9.
> 10. RIGHT
> 
> 99. DON'T KNOW

Further variables: (matrix...?)

### [Marpor]({{< ref "marpor" >}})
###### `rile` Party left right
>"Right-left position of party as given in Michael Laver/Ian Budge (eds.)"

>-100.?
> ...
> 100. ?

Further variables: 

## Measures
Measures that use this variable:
```dataview
TABLE Name as "Measure", Polarization, Level
FROM "measures"
WHERE contains(variables, "party-position")
```