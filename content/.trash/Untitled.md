<%*  
const dv = app.plugins.plugins["dataview"].api;  
const query = 'TABLE Name as "Item" FROM "variables" WHERE contains(data, cses)';  
let out = await dv.queryMarkdown(query)  
tR += out.value

%>
