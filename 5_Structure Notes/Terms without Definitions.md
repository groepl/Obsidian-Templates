---
tags:
  - type/structure
  - structure/list
  - structure/inspect
aliases: 
lead: +++ Lead paragraph goes here +++
visual: "![[image.jpg]]"
created: 2023-11-13, 21:15
modified: 2023-11-25, 20:43
template_type: Structure
template-version: "1.9"
---
<!--  See "Template Help" below for using properties -->

# Terms without Definitions

<!-- Main STRUCTURE of my content -->
```dataview
TABLE WITHOUT ID
	file.link as Terms, 
	template_type AS "Type", 
	lead AS Definition,
	file.folder AS "folder" 
FROM #type/term
WHERE lead = null
SORT file.name ASC
```


---
# Back Matter

## Source
<!-- Always keep a link to the source- --> 
- 

## Tasks
<!-- What remains to be done with this note? --> 
- 

## Questions
<!-- What remains for you to consider? --> 
- 

## Terms
<!-- Links to definition pages. -->
- 

## References
<!-- Links to pages not referenced in the content. -->
- 

## Template Help
<!-- Links to external help pages on GitHub. -->
- [Basic Template Structure](https://github.com/groepl/Obsidian-Templates#basic-template-structure)
- [How to Use Links](https://github.com/groepl/Obsidian-Templates#how-to-use-links)
- [How to Use Tags](https://github.com/groepl/Obsidian-Templates#how-to-use-tags)
- [How to Search Notes](https://github.com/groepl/Obsidian-Templates#how-to-search-notes)
- [Plugins Needed](https://github.com/groepl/Obsidian-Templates#obsidian-plugins-needed)
- [Find Latest Updates](https://github.com/groepl/Obsidian-Templates)