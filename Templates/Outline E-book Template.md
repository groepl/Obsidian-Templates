---
tags: type/chapter target/ebook
#theme/ - build cluster 
#index/ - define entry point
# 
#type/ - note characteristics
#source/ - where note comes from
#target/ - where note will go to
# 
#chart/ - from #type/chart 
#kanban/ - from #type/kanban
#role/ - from #type/person
#structure/ - from #type/structure
#visual/ - from #type/visual
#
aliases:
#
title_short: "Take Useful Notes"
chapter: "0.0"
version: "0.3"
status: draft
# status: draft, final, published, rework
#
created: {{date}}, {{time}}
modified: {{date}}, {{time}}
published:
#
template-type: Ebook
template-version: "1.4"
cc: "CC BY-SA 4.0"
legalcode: https://creativecommons.org/licenses/by-sa/4.0/legalcode
source: https://github.com/groepl/Obsidian-Templates
---

# {{Title}}

<!-- What remains to be done do get the final version? --> 
- [ ] Prepare final version 

- - -
<!-- Main content of this chapter -->
. 


---
## Questions
<!-- What remains for you to consider in the draft version? --> 
- 

## Table of Content
<!-- Links to chapters from e-book -->

```dataview
TABLE WITHOUT ID
	chapter AS "",
	file.link AS Title,
	modified AS Modified,
	status AS Status
FROM #type/chapter
WHERE title_short = "Smart Sketchnotes"
SORT chapter ASC
```

## References
<!-- Links to pages not referenced in the content -->
- [eBook - Take Useful Notes](eBook%20-%20Take%20Useful%20Notes.md)












