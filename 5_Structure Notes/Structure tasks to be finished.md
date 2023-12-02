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

# Structure tasks to be finished

<!-- Main STRUCTURE of my content -->
Sorted by `file.mday`
```dataview
TABLE WITHOUT ID
	length(file.tasks) AS "Tasks / Notes",
	file.link AS Note,
	lead AS Lead,
	file.mday AS Date
FROM "5_Structures" 
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