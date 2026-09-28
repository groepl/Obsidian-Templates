---
tags:
  - type/structure
  - structure/list
aliases:
lead: "Latest Update at GitHub: v11.0.0 - 14.07.2026"
visual: "![[image.jpg]]"
created: 2026-06-14, 12:44
modified: 2026-06-14, 12:44
template_type: Structure
template_version: "1.21"
license: © 2022-2025 by Edmund Gröpl under CC BY-NC-SA 4.0
---
<!--  See "Template Help" below for using properties -->

# Templates
<!--  Clear and descriptive title -->

> [!Note]
> `= this.lead`

<!-- Main STRUCTURE of my content -->

<!-- Table for 5_Structure Notes. Use as example and modify. -->
<!-- template_version: "0.1" -->
```dataview
TABLE WITHOUT ID
	file.link as "1_Fleeting", 
	template_type AS "Type", 
	template_version AS "Version", 
	dateformat(file.mday, "yyyy-MM-dd") AS Modified
FROM "Templates"
WHERE contains(file.name,"1_")
SORT file.name ASC
```

```dataview
TABLE WITHOUT ID
	file.link as "2_Literature", 
	template_type AS "Type", 
	template_version AS "Version", 
	dateformat(file.mday, "yyyy-MM-dd") AS Modified
FROM "Templates"
WHERE contains(file.name,"2_")
SORT file.name ASC
```

```dataview
TABLE WITHOUT ID
	file.link as "3_Permanent", 
	template_type AS "Type", 
	template_version AS "Version", 
	dateformat(file.mday, "yyyy-MM-dd") AS Modified
FROM "Templates"
WHERE contains(file.name,"3_")
SORT file.name ASC
```


```dataview
TABLE WITHOUT ID
	file.link as "4_Projects", 
	template_type AS "Type", 
	template_version AS "Version", 
	dateformat(file.mday, "yyyy-MM-dd") AS Modified
FROM "Templates"
WHERE contains(file.name,"4_")
SORT file.name ASC
```


```dataview
TABLE WITHOUT ID
	file.link as "5_Structure", 
	template_type AS "Type", 
	template_version AS "Version", 
	dateformat(file.mday, "yyyy-MM-dd") AS Modified
FROM "Templates"
WHERE contains(file.name,"5_")
SORT file.name ASC
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
	dateformat(date(created, "yyyy-mm-dd, HH:MM"), "yyyy-mm-dd") AS "created" ⚡️bug in DataView 


FROM #target/forumzettelkasten  : when using tags
FROM "Books"                                : when using folders
FROM ""                                          : when using all folders
FROM #status/open OR #status/wip

GROUP BY author

SORT created DESC
SORT file.name ASC

WHERE read = 2023
WHERE status = "open"
WHERE kanban = "backlog"
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

**Source**
<!-- Always keep a link to the source- --> 
- based_on::

**References**
<!-- Links to pages not referenced in the content. see: [[related note]] because <reason> -->
- see:: 

**Terms**
<!-- Links to definition pages. -->
- term:: [[Template]] at Merriam-Webster

**Target**
<!-- Link to project note or externally published content. -->
- used_in:: [[Version History - Obsidian Templates]]
- used_in:: [[Project Log - Obsidian Templates]]

---
**Tasks**
<!-- What remains to be done with this note? --> 
- 

**Questions**
<!-- What remains for you to consider? --> 
- question::

---
**Template Help**
<!-- Links to external help pages on GitHub. -->
- [Basic Template Structure](https://github.com/groepl/Obsidian-Templates#basic-template-structure)
- [How to Use Links](https://github.com/groepl/Obsidian-Templates#how-to-use-links)
- [How to Use Tags](https://github.com/groepl/Obsidian-Templates#how-to-use-tags)
- [How to Search Notes](https://github.com/groepl/Obsidian-Templates#how-to-search-notes)
- [Plugins Needed](https://github.com/groepl/Obsidian-Templates#obsidian-plugins-needed)
- [Find Latest Updates](https://github.com/groepl/Obsidian-Templates)