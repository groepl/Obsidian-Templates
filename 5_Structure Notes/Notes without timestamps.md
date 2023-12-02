---
tags:
  - type/structure
aliases: 
lead: +++ Lead paragraph goes here +++
visual: "![[image.jpg]]"
created: 2023-10-29, 21:23
modified: 2023-11-25, 20:33
template_type: Structure
template-version: "1.8"
updated: 2023-11-07T19:38
---

# Notes without timestamps

<!-- Main STRUCTURE of my content -->
Sorted by `file.mday desc`
```dataview
table without id 
	file.link as Notes, 
	length(file.inlinks) as "In",
	length(file.outlinks) as "Out",
	modified as Modified,
	created as Created,
	file.cday as cDay 
FROM "3_Permanent Notes"
WHERE (modified = null) OR (created = null)
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