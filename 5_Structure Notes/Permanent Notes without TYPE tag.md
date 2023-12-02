---
created: 2023-11-08, 21:44
modified: 2023-11-25, 20:43
tags: type/structure
aliases: 
lead: +++ Lead paragraph goes here +++
visual: "![[image.jpg]]"
template_type: Structure
template-version: "1.9"
---
<!--  See "Template Help" below for using properties -->


# Permanent Notes without TYPE tag

<!-- Main STRUCTURE of my content -->
Sorted by `file.cday DESC`
```dataview
table without id 
	file.link as Name, 
	file.etags as Tags,
	length(file.inlinks) as "In",
	length(file.outlinks) as "Out",
	file.cday as Date
FROM "3_Permanent Notes"
WHERE (length(file.etags) != 0) AND !contains(file.etags,"type")
SORT file.link ASC
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