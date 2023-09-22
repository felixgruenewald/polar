# Before you start

- Turn off sync for the folder `.obsidian` in the Nextcloud settings
- This creates an individual setting (incl. plugins) file for you, while keeping contents of the vault synced

# Plugins

## Citations

- Install and activate the plugin "Citations" by Jon Gauthier
- Change database to _BibLaTex_ and paste the filepath to your exported PolRef Zotero database
- Set "Literature note folder" to `Use cases`
- The "Literature note title template" should be "{{citekey}}"
    - This will be the filename of the literature note, e.g., abou-chadi_causal_2018
- "Literature note content template": this is the strucutre of the information that the plugin imports from Zotero. There is a wide range of information that can be imported but we should have it in the same format.
    - If you put something before "::", the dataview plugin can acces that information.
    - Insert the following code into the template box:

```

>[!Info]
>**Authors**:: {{authorString}}
>**Year**:: {{year}}
>**Title**:: {{title}}
>**Publication**:: {{containerTitle}}
>**DOI**:: [{{DOI}}](https://doi.org/{{DOI}})
>**Polarization**::
>**Level**::
>**Measure**::
>**Data**::

> [!Abstract]
> {{abstract}}

```

- Press CTRL + P to open up the command list, choose "Citation: Insert literature note link" to open up the list of Zotero entries, choose one to create a link and entry for a new literature note
    - Go to Settings/Hotkeys to set up a general shortcut to directy call the command

## Dataview

- Install and activate the plugn "Dataview"
- The dataview plugin allows you to create tables by accessing information from papers
# Export
- Dataview tables are not gonna show up when we export the .md files. Therefore, we need to copy the HTML source code behind them.
- Click View > Developer Tools; click the little mouse icon top left of the developer screen, click on the dataview table. The developer window will highlight the HTML code for the table, copy that code and paste it into the exported markdown.