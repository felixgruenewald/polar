These things need to be done before we are ready to publish, optimally in this order:

# Links
- The citations now use the citekeys in-text, which is not the most pretty solution. We can uses aliases to makes this look better:
	- Instead of regular Links: `[ezrow_variance_2007]({{< ref "ezrow_variance_2007" >}})`
	- We write the display text behind a "|": `[Ezrow (2007)]({{< ref "ezrow_variance_2007" >}})`
	- This way it shows up like this: [Ezrow (2007)]({{< ref "ezrow_variance_2007" >}})
	- If we add the display name as a property under "aliases", we can also type the display name in brackets directly

# Dataview
- Right now, the dataview tables don't work anymore, because the variable names have changed
- Inside the dataview command, we need to change the folder names (mostly just to lower case)
- as well as the variable names. E.g., instead of:
```
dataview
TABLE Name as "Item"
FROM "Variables"
WHERE contains(Datasets, [CHES]({{< ref "CHES" >}}))
```
- We need this:
```
dataview
TABLE Name as "Item"
FROM "variables"
WHERE contains(datasets, "ches")
```

# Tables
- The dataview tables are no real markdown tables and don't show up correctly when converting to HTML
- However, we can just copy the dataview table and paste it as a markdown table
- When the tables are done and formatted correctly, highlight the full table with your cursor, CTRL+C, and then paste it right below. It should show as a markdown table
- Format it, if necessary, to look nice for publishing
- Then comment out the dataview code (<!-- ... -->), so it doesn't show but we can reuse it later when necessary

# ~~Front Matter~~
- in the use cases section, the front matter is not quite ready
- In most entries, it's a single line:
```
---
levels: elite
measures: range, api
---
```
- For polarisation, levels, measures, data, we need to turn this into lists that the website's html can loop through:
```
---
levels:
 - elite
measures:
 - range
 - api
---
```
- We don't change this for variables where there can possibly only be one value (title, name, year, authors etc.)
- You can do this using the text editor (Source Mode), or just right click the entries and change the property type to "List"


```dataviewjs
dv.table(["Title","Date"],dv.pages('"data"') .sort(p => p.date, 'desc') .map(b => ['['+b.title+']({{< ref "'+b.file.name+'" >}})', b.link]) ) 
```

