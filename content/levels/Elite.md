---
title: Elite Polarisation
---


# Measures
```dataview
TABLE Name as "Measure", Polarization, Level
FROM "Measures"
WHERE contains(Level, [Elite]({{< ref "Elite" >}}))
```
# Uses cases
```dataview
TABLE without ID Authors, Year, Title, Publication, DOI
FROM "Use cases"
WHERE contains(Level, [Elite]({{< ref "Elite" >}}))
SORT Year DESC
```