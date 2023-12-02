---
created: 2023-04-18, 21:28
modified: 2023-11-25, 20:33
tags:
  - type/structure
  - structure/list
  - theme/zettelkasten
aliases: 
lead: +++ Lead paragraph goes here +++
visual: "![[image.jpg]]"
template_type: Frontmatter
template-version: "1.8"
---
<!--  See "Template Help" below for using properties -->---

# Notes not in Permanent Note Folder

<!-- DataView table, use example and modify -->
```dataview
TABLE WITHOUT ID
	file.link as notes, 
	file.folder AS "folder" 
FROM 
	#type/note OR 
	#type/sketchnote OR 
	#type/question OR 
	#type/recipe OR 
	#type/tool AND 
	-"3_Permanent Notes" AND
	-"6_Project Notes"
SORT file.folder ASC 
SORT file.link ASC
```

<!-- Options 
TABLE WITHOUT ID
	file.folder AS ...
	file.link AS ...
	file.name AS ...
	file.etags AS ...
	length(file.outlinks) AS …
	length(file.inlinks) AS …
	length(file.etags) AS …
	dateformat(file.cday, "yyyy-MM-dd") AS Date
	dateformat(file.cday, "yyyy-LLL-dd") AS Date

FROM #target/forumzettelkasten  : when using tags
FROM "Books"                                : when using folders
FROM ""                                          : when using all folders
FROM #status/open OR #status/wip

SORT created DESC
SORT file.name ASC

WHERE read = 2023
WHERE status = "open"
WHERE contains(file.name,"LernOS Zettelkasten")
WHERE sketchnote != empty

LIMIT 3

---
More about: 
https://github.com/blacksmithgu/obsidian-dataview/blob/master/docs/docs/queries/query-types.md
https://github.com/blacksmithgu/obsidian-dataview/blob/master/docs/docs/queries/data-commands.md

Source: 
https://github.com/groepl/Obsidian-Templates
-->


---
# Back Matter
## Source
<!-- Always keep a link to the source- --> 
- 

## Tasks
<!-- What remains to be done with this note? --> 
- [ ] Add to [Inspect and Adapt - Dashboard](Inspect%20and%20Adapt%20-%20Dashboard.md)

## Questions
<!-- What remains for you to consider? --> 
- 

## Terms
<!-- Links to definition pages. -->
- 

## References
<!-- Links to pages not referenced in the content. -->
- [Inspect and Adapt - Dashboard](Inspect%20and%20Adapt%20-%20Dashboard.md)

## Template Help
<!-- Links to external help pages on GitHub. -->
- [Basic Template Structure](https://github.com/groepl/Obsidian-Templates#basic-template-structure)
- [How to Use Links](https://github.com/groepl/Obsidian-Templates#how-to-use-links)
- [How to Use Tags](https://github.com/groepl/Obsidian-Templates#how-to-use-tags)
- [How to Search Notes](https://github.com/groepl/Obsidian-Templates#how-to-search-notes)
- [Plugins Needed](https://github.com/groepl/Obsidian-Templates#obsidian-plugins-needed)
- [Find Latest Updates](https://github.com/groepl/Obsidian-Templates)