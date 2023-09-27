## Use cases
Publications that use this dataset:

<%*  
const dv = app.plugins.plugins["dataview"].api;  
const query = 'TABLE without ID link(file.link, title) as "Title", join(aliases, ", ") as "Authors" FROM "usecases" WHERE contains(data, "' + tp.file.title + '")';  
let out = await dv.queryMarkdown(query)  
tR += out.value

%>
