# Measures
Measures that use this dataset:

<%*  
const dv = app.plugins.plugins["dataview"].api;  
const query = 'TABLE without ID link(file.link, name) as "Measure", join(polarisation, ", ") as "Polarization", join(level, ", ") as "Level" FROM "measures" SORT polarisation asc WHERE contains(data, "' + tp.file.title + '")';  
let out = await dv.queryMarkdown(query)  
tR += out.value

%>
