---
name: CHES
title: Chapel Hill Expert Surveys
---
# Description

The Chapel Hill Expert Surveys (CHES) estimate party positioning by surveying political scientists specializing in European parties and integration in six waves from 1999 to 2019. The most recent wave includes all 27 European member states as well as Iceland, Norway, Switzerland, and Turkey. 

CHES topics include party positions on European integration, EU policies, the general left/right dimension, the economic left/right dimension, and the cultural left/right dimension. More recent surveys also include questions on non-EU policy issues such as anti-elite rhetoric, immigration, redistribution, decentralization, and environmental policy. With regard to polarization, the CHES includes several items and dimensions that can be used to measure ideological polarization at the elite level. 

**URL**: [chesdata.eu](https://www.chesdata.eu)

# Variables
```dataview
TABLE Name as "Item"
FROM "variables"
WHERE contains(datasets, "ches")
```

# Measures
<!--```dataview
TABLE name as "Measure", polarisation, level
FROM "measures"
WHERE contains(data, "ches") OR contains(datasec, "ches")
```-->

|File|Measure|polarisation|level|
|---|---|---|---|
|[range](app://obsidian.md/measures/range.md)|Range|- ideological|- elite|
|[sd](app://obsidian.md/measures/sd.md)|SD|- ideological|- elite<br>- mass|


# Use cases
```dataview
TABLE without ID Authors, Year, Title, Publication, DOI
FROM "usecases"
WHERE contains(data, "ches") OR contains(datasec, "ches")
SORT Year DESC
```
