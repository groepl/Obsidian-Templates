---
tags:
  - type/structure
  - structure/list
  - structure/inspect
aliases: 
lead: +++ Lead paragraph goes here +++
visual: "![[image.jpg]]"
created: 2023-11-13, 21:15
modified: 2023-11-24, 19:46
template_type: Structure
template_version: "1.10"
---
<!--  See "Template Help" below for using properties -->

# Notes without lead

```dataview
TABLE WITHOUT ID
	file.link AS Sketchnotes,
	lead AS "Lead Paragraph",
	modified AS "Modified",
	file.folder AS Folder
FROM "3_Permanent Notes" 
WHERE (lead = null) OR (lead = "+++ Lead paragraph goes here +++")
SORT modified DESC
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