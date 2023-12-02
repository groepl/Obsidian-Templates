---
tags:
  - type/structure
aliases: 
lead: +++ Lead paragraph goes here +++
visual: "![[image.jpg]]"
created: 2023-10-29, 21:12
modified: 2023-11-25, 20:43
template_type: Structure
template-version: "1.8"
---

# Permanent Notes without in-links

<!-- Main STRUCTURE of my content -->
Sorted by `file.cday`
```dataview
table without id 
	file.link as Name, 
	length(file.inlinks) as "In",
	length(file.outlinks) as "Out",
	file.cday as Date
FROM "3_Permanent Notes"
WHERE (length(file.inlinks) = 0) AND (length(file.outlinks) != 0)
SORT file.cday desc
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