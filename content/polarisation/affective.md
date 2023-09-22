---
title: Affective Polarisation
---
# Measures

```dataview
TABLE Name as "Measure", Polarization, Level
FROM "Measures"
WHERE contains(Polarization, [Affective]({{< ref "Affective" >}}))
```
# Use cases
```dataview
TABLE without ID Authors, Year, Title, Publication, DOI
FROM "Use cases"
WHERE contains(Polarization, [Affective]({{< ref "Affective" >}}))
SORT Year DESC
```