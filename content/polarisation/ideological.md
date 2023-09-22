---
title: Ideological Polarisation
---
# Measures
```dataview
TABLE Name as "Measure", Polarization, Level
FROM "Measures"
WHERE contains(Polarization, [Ideological]({{< ref "Ideological" >}}))
```
# Use cases
```dataview
TABLE without ID Authors, Year, Title, Publication, DOI
FROM "Use cases"
WHERE contains(Polarization, [Ideological]({{< ref "Ideological" >}}))
SORT Year DESC
```