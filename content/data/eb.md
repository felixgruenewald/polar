---
name: EB
title: Eurobarometer
link: https://europa.eu/eurobarometer/screen/home
---
# Description

The Eurobarometer (EB) surveys public opinion in Europe, covering the state of public opinion on issues related to the European Union as well as other political or social issues. Launched by the European Commission in 1974, the EB was first conceived as a means of "revealing Europeans to themselves." Since then, it has evolved and expanded significantly with different survey instruments and is conducted twice a year. In 2007, the European Parliament launched its own regular series of Eurobarometer surveys, focusing on issues specific to the European Parliament, including the European elections.

The combination of a wide range of topics covered regularly over a long period of time and its broad geographical coverage make the Eurobarometer a unique source of data on public opinion in Europe. With regard to polarization, EB surveys include several items that can be used as measures of ideological polarization at the elite and mass levels.

# Items
```dataview
TABLE Name as "Item"
FROM "Variables"
WHERE contains(datasets, [EB]({{< ref "EB" >}}))
```

# Measures
```dataview
TABLE Name as "Measure", Polarization, Level
FROM "Measures"
WHERE contains(Data, [EB]({{< ref "EB" >}})) OR contains(Data, "*[EB]({{< ref "EB" >}})*")
```
# Use cases
```dataview
TABLE without ID Authors, Year, Title, Publication, DOI
FROM "Use cases"
WHERE contains(Data, [EB]({{< ref "EB" >}}))
SORT Year DESC
```