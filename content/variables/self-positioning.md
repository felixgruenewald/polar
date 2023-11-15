---
Datasets:
  - cses
  - ess
title: Issue Self-Positioning
object:
  - left-right
---
## Variable description

Short 1-2 sentence description of the variable.

## Datasets & Variants
### [CSES]({{< ref "cses" >}})
---
##### LEFT-RIGHT - SELF
_E3020_

**Scale:** 0 (Left) - 10 (Right)

**Wording:** Where would you place yourself on this scale?

---
### [European Social Survey]({{< ref "ess" >}})
---
##### Placement on the left right scale
_lrscale_

**Scale:** 0 (Left) - 10 (Right)

**Wording:** In politics people sometimes talk of “left ́ and “right ́. Using this card, where would you place yourself on this scale, where 0 means the left and 10 means the right?

---
### [Eurobarometer]({{< ref "eb" >}})
---
#### Personal left right

**Scale:** 1 (Left) - 10 (Right)

**Wording:** In political matters people talk of "the left" and "the right". How would you place your views on this scale?"

---
### [EES]({{< ref "ees" >}})
---
##### Personal left right

**Scale:** 0 (Left) - 10 (Right)

**Wording:** In political matters people talk of "the left" and "the right". What is your position? Please indicate your views using any number on an 11-point-scale. On this scale, where 0 means "left" and 10 means "right," which number best describes your position?

---
### [World Value Survey]({{< ref "wvs" >}})
---
##### Self positioning in political scale

**Scale:** 0 (Left) - 10 (Right)

**Wording:** In political matters, people talk of "the left" and "the right." How would you place your views on this scale, generally speaking?
<!--
> 1. LEFT
> 2.
> 3.
> 4.
> 5.
> 6.
> 7.
> 8.
> 9.
> 10. RIGHT
> ...?-->
---
## Measures
Measure that use this variable:
```dataview
TABLE Name as "Measure", Polarization, Level
FROM "measures"
WHERE contains(variables, "self-positioning")
```