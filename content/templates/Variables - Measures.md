## Measures
Measures that rely on these items:

<%*  
const dv = app.plugins.plugins["dataview"].api;  
const query = 'TABLE without ID link(file.link, name) as "Measure", join(polarisation, ", ") as "Polarization" FROM "measures" WHERE contains(variables, "' + tp.file.title + '")';  
let out = await dv.queryMarkdown(query)  
tR += out.value

%>
