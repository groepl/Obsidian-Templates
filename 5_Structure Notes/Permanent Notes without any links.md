---
tags: type/structure structure/list type/tooltip  structure/inspect
aliases: 
created: 2022-12-27, 17:17
modified: 2023-11-25, 20:42
template_type: Structure
template-version: "1.2"
cc: CC BY-SA 4.0
legalcode: https://creativecommons.org/licenses/by-sa/4.0/legalcode
---

# Permanent Notes without any links

<!-- Main STRUCTURE of my content -->
Orphans sorted by `file.cday`
```dataview
table without id 
	file.link as Name, 
	length(file.inlinks) as "In",
	length(file.outlinks) as "Out",
		file.cday as Date
FROM "3_Permanent Notes"
WHERE (length(file.inlinks) = 0) AND (length(file.outlinks) = 0)
SORT file.name asc
```

---
##### Questions
<!-- What remains for you to consider? --> 
- 


##### Terms
<!-- Links to definition pages -->
- 


##### References
<!-- Links to pages not referenced in the content -->
- 


