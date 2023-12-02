---
tags:
  - type/structure
aliases: 
lead: +++ Lead paragraph goes here +++
visual: "![[image.jpg]]"
created: 2023-10-29, 19:31
modified: 2023-11-25, 20:33
template_type: Structure
template-version: "1.8"
---

# Tasks from Permanent Notes to be finished

<!-- Main STRUCTURE of my content -->
Sorted by `file.mday`
```dataview
TABLE WITHOUT ID
	file.link AS Note,
	length(file.tasks) AS "Tasks",
	lead AS Lead,
	priority AS Prio,
	file.mday AS Date
FROM "3_Permanent Notes" 
WHERE length(file.tasks) != 0
SORT file.mday DESC
```


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