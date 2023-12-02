---
tags:
  - type/structure
aliases: 
lead: +++ Lead paragraph goes here +++
visual: "![[image.jpg]]"
created: 2023-10-29, 19:31
modified: 2023-11-25, 20:43
template_type: Structure
template-version: "1.8"
---

# Project Note tasks to be finished

<!-- Main STRUCTURE of my content -->
Sorted by `file.mday`
```dataview
TABLE WITHOUT ID
	file.link AS Note,
	length(file.tasks) AS "Tasks",
	priority AS Prio,
	lead AS Lead,
	modified AS Modified
FROM "6_Project Notes" 
WHERE length(file.tasks) != 0 AND !completed
SORT modified DESC
```

WHERE !completed AND contains(tags, "#shopping")

---
# Back Matter
## Source
<!-- Always keep a link to the source. --> 
- 

## Tasks
<!-- What remains to be done with this note? --> 
- 

## Questions
<!-- What remains for you to consider? --> 
- 

## Terms
<!-- Links to definition pages -->
- 

## References
<!-- Links to pages not referenced in the content -->
- 