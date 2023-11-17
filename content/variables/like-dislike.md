---
datasets:
  - cses
title: Like-Dislike scores
object:
  - parties
  - leaders
---
## Variable description

The like-dislike scale is, in various forms, one of the most common tools to measure affective polarization. Respondents are asked about their feelings towards a range of parties. This allows to get an understanding of their view of the overall party system and to compute measures such as the [spread of likes]({{< ref "spread" >}}) or the [affective polarization index]({{< ref "api" >}}) that try to capture just that.

It can be found in a wider range of datasets, most importantly the [CSES]({{< ref "cses" >}}). Other variations are, e.g., the feeling thermometer in the American National Election Survey which asks for feelings towards parties on a 0-100 scale.

## Datasets & Variants
### [CSES]({{< ref "cses" >}})

#### LIKE-DISLIKE PARTY X
_Label: IMD3008_X, E3017_X_

**Scale:** 0 (strongly dislike) - 10 (strongly like)

**Wording**: _"I'd like to know what you think about each of our political parties. After I read the name of a political party, please rate it on a scale from 0 to 10, where 0 means you strongly dislike that party and 10 means that you strongly like that party. If I come to a party you haven't heard of or you feel you do not know enough about, just say so. The first party is [PARTY A]."_

<!--
> 96. HAVEN'T HEARD OF PARTY
> 97. VOLUNTEERED: REFUSED
> 98. DON'T KNOW ENOUGH ABOUT/DON'T KNOW WHERE TO RATE
> 99. MISSING
-->

<!--
Further variables: **IMD3008_B** **E3017_B**LIKE-DISLIKE - PARTY B, **E3017_C** LIKE-DISLIKE - PARTY C, **E3017_D**LIKE-DISLIKE - PARTY D, **E3017_E** LIKE-DISLIKE - PARTY E, **E3017_F** LIKE-DISLIKE - PARTY F, **E3017_G** LIKE-DISLIKE - ADDITIONAL - PARTY G, **E3017_H** LIKE-DISLIKE - ADDITIONAL - PARTY H, **E3017_I**LIKE-DISLIKE - ADDITIONAL - PARTY I.
-->
---
#### LIKE-DISLIKE LEADER X
_E3018_A_

**Scale:** 0 (strongly dislike) - 10 (strongly like)

**Wording:** And what do you think of the presidential candidates/party leaders? After I read the name of a presidential candidate/party leader, please rate them on a scale from 0 to 10, where 0 means you strongly dislike that candidate and 10 means that you strongly like that candidate. If I come to a presidential candidate/party leader you haven't heard of or you feel you do not know enough about, just say so. The first is [LEADER A].

<!--
>1. HAVEN'T HEARD OF LEADER
>2. VOLUNTEERED: REFUSED
>3. DON'T KNOW ENOUGH ABOUT/DON'T KNOW WHERE TO RATE
>4. MISSING

Further Variables: **E3018_B**LIKE-DISLIKE - LEADER B, **E3018_C**LIKE-DISLIKE - LEADER C, **E3018_D**LIKE-DISLIKE - LEADER D, **E3018_E**LIKE-DISLIKE - LEADER E, **E3018_F**LIKE-DISLIKE - LEADER F, **E3018_G** LIKE-DISLIKE - ADDITIONAL - LEADER G, **E3018_H**LIKE-DISLIKE - ADDITIONAL - LEADER H, **E3018_I**LIKE-DISLIKE - ADDITIONAL -LEADER I.
-->
---

## Measures
Measures that rely on these items:

| Measure                            | Polarization |
| ---------------------------------- | ------------ |
| [API]({{< ref "measures/api.md" >}})           | affective    |
| [Distance]({{< ref "measures/distance.md" >}}) | affective    |
| [Spread]({{< ref "measures/spread.md" >}})     | affective    |

