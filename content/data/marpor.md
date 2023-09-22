---
title: MARPOR
---
# Description

The Manifesto Research on Political Representation (MARPOR), formerly known and still often referred to as the "Manifesto Project", provides a comprehensive collection and content analysis of party election manifestos, including over 1000 parties from 50 countries worldwide. Because the collected manifestos are content analyzed, MARPOR offers a wide range of topics related to party preferences, party program offerings, the relationship between parties and voters, or the translation of party programs into policies.

With regard to polarization, MARPOR includes items and information that can be used to measure ideological polarization at the elite level. 

**URL:** [manifestoproject.wzb.eu](https://manifestoproject.wzb.eu)
# Items
```dataview
TABLE Name as "Item"
FROM "Variables"
WHERE contains(datasets, [MARPOR]({{< ref "MARPOR" >}}))
```
# Measures
```dataview
TABLE Name as "Measure", Polarization, Level
FROM "Measures"
WHERE contains(Data, [MARPOR]({{< ref "MARPOR" >}})) OR contains(Data, "*[MARPOR]({{< ref "MARPOR" >}})*")
```
# Use cases
```dataview
TABLE without ID Authors, Year, Title, Publication, DOI
FROM "Use cases"
WHERE contains(Data, [MARPOR]({{< ref "MARPOR" >}}))
SORT Year DESC
```