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
---
#### LEFT-RIGHT - PARTY A
_E3019_A_

**Scale:** 0 (Left) - 10 (Right)

**Wording:** In politics people sometimes talk of left and right. Where would you place [PARTY A] on a scale from 0 to 10 where 0 means the left and 10 means the right?"
<!--
> 95. VOLUNTEERED: HAVEN'T HEARD OF LEFT‐RIGHT
> 96. VOLUNTEERED: HAVEN'T HEARD OF PARTY
> 97. VOLUNTEERED: REFUSED
> 98. VOLUNTEERED: DON'T KNOW WHERE TO PLACE
> 99. MISSING

Further variables: `E3019_B`LEFT_RIGHT - PARTY B, `E3019_C`LEFT_RIGHT - PARTY C, `E3019_D`LEFT_RIGHT - PARTY D, `E3019_E`LEFT_RIGHT - PARTY E, `E3019_F`LEFT_RIGHT - PARTY F, `E3019_F`LEFT_RIGHT - ADDITIONAL - PARTY G, `E3019_H`LEFT_RIGHT - ADDITIONAL - PARTY H, `E3019_I`LEFT_RIGHT - ADDITIONAL - PARTY I.
-->
---
### [CHES]({{< ref "ches" >}})
---
#### Overall ideological stance
_LRGEN_

**Scale:** 0 (Extreme left) - 5 (Center) - 10 (Extreme right)

**Wording:** Position of the party in YEAR in terms of its overall ideological stance."

---
#### Ideological stance on economic issues
_LRECON_

**Scale:** 0 (Extreme left) - 5 (Center) - 10 (Extreme right)

**Wording:** Position of the party in YEAR in terms of its ideological stance on economic issues. Parties can be classified in terms of their stance on economic issues such as privatization, taxes, regulation, government spending, and the welfare state. Parties on the economic left want government to play an active role in the economy. Parties on the economic right want a reduced role for government."

---
#### Position on social and cultural issues
_GALTAN_

**Scale:** 0 (Libertarian/Postmaterialist) - 5 (Center) - 10 (Traditional/Authoritarian)

**Wording:** Position of the party in YEAR in terms of their views on social and cultural values. “Libertarian” or “postmaterialist” parties favor expanded personal freedoms, for example, abortion rights, divorce, and same-sex marriage. “Traditional” or “authoritarian” parties reject these ideas in favor of order, tradition, and stability, believing that the government should be a firm moral authority on social and cultural issues.

---
### [EES]({{< ref "ees" >}})
---
#### Party Left-Right

**Scale:** 0 (Left) - 10 (Right)

**Wording:** And about where would you place the following political parties on this scale? Which number from 0 to 10, where '0' means "left" and '10' means "right" best describes these parties?

---
### [Marpor]({{< ref "marpor" >}})
---
###### Party left right
_RILE_

**Scale:** ?

**Wording:** Right-left position of party as given in Michael Laver/Ian Budge (eds.)"

---
## Measures
Measures that use this variable:
```dataview
TABLE Name as "Measure", Polarization, Level
FROM "measures"
WHERE contains(variables, "party-position")
```