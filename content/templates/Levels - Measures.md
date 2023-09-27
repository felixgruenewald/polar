## Measures

<%*  
const dv = app.plugins.plugins["dataview"].api;  
const query = 'TABLE without ID link(file.link, name) as "Measure", join(polarisation, ", ") as "Polarisation" FROM "measures" WHERE contains(level, "' + tp.file.title + '")';  
let out = await dv.queryMarkdown(query)  
tR += out.value

%>
