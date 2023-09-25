---
name: WVS
title: World Value Survey
---
# Description

The World Value Survey (WVS) is an international research group focused on measuring human values around the world. The program began in 1981 and has since conducted surveys in more than 120 countries worldwide. To date, the WVS has conducted seven waves of its representative comparative social survey, which is repeated every five years, making the WVS the largest cross-national survey of human beliefs and values.

WVS topics include social values, political attitudes, personal health and well-being, and attitudes toward the future. With regard to polarization, the WVS includes items that can be used to measure ideological polarization at the elite level.

**URL:** [worldvaluessurvey.org](https://www.worldvaluessurvey.org/wvs.jsp)
# Items
```dataview
TABLE name as "Item"
FROM "variables"
WHERE data = wvs
```

# Measures
```dataview
TABLE Name as "Measure", Polarization, Level
FROM "Measures"
WHERE contains(Data, [WVS]({{< ref "WVS" >}})) OR contains(Data, "*[WVS]({{< ref "WVS" >}})*")
```
# Use cases
```dataview
TABLE without ID Authors, Year, Title, Publication, DOI
FROM "Use cases"
WHERE contains(Data, [WVS]({{< ref "WVS" >}}))
SORT Year DESC
```
