---
tags: type/structure structure/list type/dataview status/3_doing
aliases: 
lead: Notes with type/term, type/quote and type/book belong to 4_References Folder.
created: 2023-04-22, 12:07
modified: 2023-11-25, 20:33
template_type: Structure
template-version: "1.5"
---

# Notes in wrong folders

<!-- Main STRUCTURE of my content -->

<!-- DataView table, use example and modify -->
## type/term
```dataview
TABLE WITHOUT ID
	file.link as Terms, 
	template_type AS "Type", 
	lead AS Definition,
	file.folder AS "folder" 
FROM #type/term AND !"4_References"
SORT file.name ASC
```

## type/quote
```dataview
TABLE WITHOUT ID
	file.link as Quotes, 
	template_type AS "Type", 
	lead AS Definition,
	file.folder AS "folder" 
FROM #type/quote AND !"4_References"
SORT file.name ASC
```

## type/book
```dataview
TABLE WITHOUT ID
	file.link as Books, 
	template_type AS "Type", 
	lead AS Definition,
	file.folder AS "folder" 
FROM #type/book AND !"4_References"
SORT file.name ASC
```
## type/tool
```dataview
TABLE WITHOUT ID
	file.link as Tools, 
	template_type AS "Type", 
	lead AS Definition,
	file.folder AS "folder" 
FROM #type/tool AND !"4_References"
SORT file.name ASC
```

## type/person
```dataview
TABLE WITHOUT ID
	file.link as Terms, 
	template_type AS "Type", 
	lead AS Definition,
	file.folder AS "folder" 
FROM #type/person AND !"4_References"
SORT file.name ASC
```

***
## Done
```dataview
TABLE WITHOUT ID
	file.link as Terms, 
	template_type AS "Type", 
	lead AS Definition,
	file.folder AS "folder" 
FROM (#type/term OR #type/quote OR #type/book) AND "4_References"
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
## Tasks
- [ ] Add lead for term descriptions

## Questions
<!-- What remains for you to consider? --> 
- 


## Terms
<!-- Links to definition pages -->
- [Term](Term.md)


## References
<!-- Links to pages not referenced in the content -->
- 


