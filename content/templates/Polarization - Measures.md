# Measures

<%*  
const dv = app.plugins.plugins["dataview"].api;  
const query = 'TABLE without ID link(file.link, name) as "Measure", join(level, ", ") as "Level" FROM "measures" WHERE contains(polarisation, "' + tp.file.title + '")';  
let out = await dv.queryMarkdown(query)  
tR += out.value

%>
