---
created: 2023-03-18, 23:13
modified: 2023-11-28, 15:42
tags:
  - type/structure
  - structure/list
aliases: 
lead: +++ Lead paragraph goes here +++
visual: "![[image.jpg]]"
template_type: Structure
template-version: "1.10"
---
<!--  See "Template Help" below for using properties -->

# Permanent Notes with unresolved links 

<!-- DataView table, use example and modify -->
```dataview
TABLE WITHOUT ID 
	key AS "Unresolved Links",
	rows.file.link AS "Permanent Notes"
FROM "3_Permanent Notes"
FLATTEN file.outlinks as outlinks 
WHERE !(outlinks.file) AND 
	!(contains(meta(outlinks).path, "/")) AND 
	!(contains(meta(outlinks).path, "."))
GROUP BY outlinks
SORT key ASC
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
- [Ghost notes](Ghost%20notes.md)
- [Broken links](Broken%20links.md)
- [Review unresolved links](Review%20unresolved%20links.md)

## Template Help
<!-- Links to external help pages on GitHub. -->
- [Basic Template Structure](https://github.com/groepl/Obsidian-Templates#basic-template-structure)
- [How to Use Links](https://github.com/groepl/Obsidian-Templates#how-to-use-links)
- [How to Use Tags](https://github.com/groepl/Obsidian-Templates#how-to-use-tags)
- [How to Search Notes](https://github.com/groepl/Obsidian-Templates#how-to-search-notes)
- [Plugins Needed](https://github.com/groepl/Obsidian-Templates#obsidian-plugins-needed)
- [Find Latest Updates](https://github.com/groepl/Obsidian-Templates)