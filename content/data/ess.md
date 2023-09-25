---
name: ESS
title: European Social Survey
---
# Description

The European Social Survey (ESS) is a pan-European survey conducted every two years since 2002. Over the last 10 waves, almost all European countries have been included, providing researchers with a broad basis for comparative research. The survey is conducted through face-to-face interviews and includes questions on a wide range of topics related to political attitudes and beliefs. 

Topics in the core questionnaire include attitudes toward democracy and politics, human values, immigration, and national and ethnic identity. In addition, each wave includes additional rotating modules containing items suggested by researchers. With regard to polarization, the ESS includes items that can be used to measure ideological polarization at the elite and mass levels.

**URL:** [europeansocialsurvey.org](https://www.europeansocialsurvey.org/)
# Items
```dataview
TABLE Name as "Item"
FROM "variables"
WHERE contains(datasets, ess)
```

# Measures
```dataview
TABLE Name as "Measure", Polarization, Level
FROM "measures"
WHERE contains(datasets, ess) OR contains(datasec, ess)
```
# Use cases
```dataview
TABLE without ID Authors, Year, Title, Publication, DOI
FROM "Use cases"
WHERE contains(Data, [ESS]({{< ref "ESS" >}}))
SORT Year DESC
```