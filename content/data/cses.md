---
title: CSES
---
# Description

The Comparative Study of Electoral Systems (CSES) is a collaborative program of election research teams from around the world. The CSES covers a wide range of topics with a focus on the behavior and attitudes of respondents at times of national elections, such as voting and turnout. CSES designs a core questionnaire that is regularly included in many academic national election surveys. 

Launched in 1996, the CSES has included five modules to date, covering topics such as citizens' views of political elites, representation and accountability, and the impact of electoral institutions. With regard to polarization, the CSES questionnaire includes several items that can be used to measure ideological polarization at the elite and mass levels and affective polarization at the mass level.

**URL:** [cses.org](https://cses.org/)
# Items
```dataview
TABLE Name as "Item"
FROM "Variables"
WHERE contains(datasets, [CSES]({{< ref "CSES" >}})) OR contains(Data, "*[CSES]({{< ref "CSES" >}})*")
```
# Measures
```dataview
TABLE Name as "Measure", Polarization, Level
FROM "Measures"
WHERE contains(Data, [CSES]({{< ref "CSES" >}}))
```
# Use cases
```dataview
TABLE without ID Authors, Year, Title, Publication, DOI
FROM "Use cases"
WHERE contains(Data, [CSES]({{< ref "CSES" >}}))
SORT Year DESC
```

