---
name: EES
title: European Election Studies
---
# Description

The European Election Studies (EES) provide data on voter behavior in European elections. By combining collected survey data with media studies and data from the Euromanifestos project, the EES cover a wide range of topics, thus allowing comparative and longitudinal analyses across EU countries. The EES is conducted by the international European Election Research Group after every European election.

Topics covered by the EES include a wide range of attitudes such as social trust, human values, or attitudes towards immigration, as well as additional information such as socio-demographics, or subjective well-being. With regard to polarization, the EES includes items that can be used to measure ideological polarization at both the elite and mass levels.

**URL:** [gesis.org](https://www.gesis.org/en/services/finding-and-accessing-data/international-survey-programs/european-election-studies)
# Items
```dataview
TABLE Name as "Item"
FROM "Variables"
WHERE contains(datasets, [EES]({{< ref "EES" >}}))
```
# Measures
```dataview
TABLE Name as "Measure", Polarization, Level
FROM "Measures"
WHERE contains(Data, [EES]({{< ref "EES" >}})) OR contains(Data, "*[EES]({{< ref "EES" >}})*")
```
# Use cases
```dataview
TABLE without ID Authors, Year, Title, Publication, DOI
FROM "Use cases"
WHERE contains(Data, [EES]({{< ref "EES" >}}))
SORT Year DESC
```