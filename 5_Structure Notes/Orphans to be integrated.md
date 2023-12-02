---
tags:
  - type/note
aliases: 
lead: An easy way to find notes that are not linked, do not link to other notes and do not use tags.
visual: "![[image.jpg]]"
created: 2023-10-30, 10:01
modified: 2023-11-25, 20:33
template_type: Note
template-version: "1.18"
---
<!--  See "Template Help" below for using properties -->

# Orphans to be integrated

<!--  Main idea of my thoughts -->

> [!Note]
> `= this.lead`

<!-- Other content of my note  -->
```dataview
table without id 
	file.link as Name, 
	file.tags as Tags,
	length(file.inlinks) as "In",
	length(file.outlinks) as "Out",
	file.cday as Date,
	file.folder as Folder
FROM "3_Permanent Notes" OR "4_References" OR "5_Structures"
WHERE length(file.inlinks) = 0 AND 
	length(file.outlinks) = 0 AND
	length(file.tags) = 0
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
https://forum.obsidian.md/t/find-orphan-notes/817/16

## Template Help
<!-- Links to external help pages on GitHub. -->
- [Basic Template Structure](https://github.com/groepl/Obsidian-Templates#basic-template-structure)
- [How to Use Links](https://github.com/groepl/Obsidian-Templates#how-to-use-links)
- [How to Use Tags](https://github.com/groepl/Obsidian-Templates#how-to-use-tags)
- [How to Search Notes](https://github.com/groepl/Obsidian-Templates#how-to-search-notes)
- [Plugins Needed](https://github.com/groepl/Obsidian-Templates#obsidian-plugins-needed)
- [Find Latest Updates](https://github.com/groepl/Obsidian-Templates)