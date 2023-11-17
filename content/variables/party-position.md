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

A commonly surveyed item, and therefore used in early measures of ideological polarization such as the [CSES polarization index]({{< ref "polarisation" >}}), this item captures parties' positions on different issues. Most commonly, this means a placement on a left-right scale, but other issue dimensions such as a socioeconomic or ecological one are possible as well. 

Party position scores can come from different sources. Survey data like the CSES asks respondents' about their perception of party positions, expert surveys like the CHES queries the evaluations of experts and Marpor uses codings of party manifestos as the base of their scores. 

## Datasets & Variants
### [CSES]({{< ref "cses" >}})

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

#### Party Left-Right

**Scale:** 0 (Left) - 10 (Right)

**Wording:** And about where would you place the following political parties on this scale? Which number from 0 to 10, where '0' means "left" and '10' means "right" best describes these parties?

---
### [Marpor]({{< ref "marpor" >}})

#### Party left right
_RILE_

**Scale:** ?

**Wording:** Right-left position of party as given in Michael Laver/Ian Budge (eds.)"

---
## Measures
Measures that rely on these items:

| Measure                                                            | Polarization |
| ------------------------------------------------------------------ | ------------ |
| [Party-System Compactness]({{< ref "measures/party-system_compactness.md" >}}) | ideological  |
| [Dispersion]({{< ref "measures/party_system_dispersion.md" >}})                | ideological  |
| [Party-System Extremism]({{< ref "measures/party-system_extremism.md" >}})     | ideological  |
| [Polarisation Index]({{< ref "measures/polarisation_index.md" >}})             | ideological  |
| [Range]({{< ref "measures/range.md" >}})                                       | ideological  |
| [SD]({{< ref "measures/sd.md" >}})                                             | ideological  |
| [Variance]({{< ref "measures/variance_weighted.md" >}})                        | ideological  |

