<!-- "Dictionary Entries" for 5_Structure Notes. Use as example and modify. -->
<!-- template_version: "0.2" -->
```dataview
TABLE WITHOUT ID
	lead as "Dictionary Entries",
	file.link as Link, 
	file.folder AS "Folder" 
FROM #type/dictionary AND #theme/philosophy
SORT lead asc
```
