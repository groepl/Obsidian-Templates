<!-- DataView table, use example and modify -->
```dataview
TABLE WITHOUT ID
	file.link as books, 
	read AS "read", 
	file.folder AS "folder" 
FROM #type/book
SORT file.name ASC
WHERE read = 2023
LIMIT 5
```

<!-- Options 
TABLE WITHOUT ID
	file.folder AS ...
	file.link AS ...
	file.name AS ...
	file.etags AS ...

FROM #target/forumzettelkasten  : when using tags
FROM "Books"                                : when using folders
FROM ""                                          : when using all folders
FROM #status/open OR #status/wip

SORT created DESC
SORT file.name ASC

WHERE read = 2023
WHERE status = "open"
---
More about: 
https://github.com/blacksmithgu/obsidian-dataview/blob/master/docs/docs/queries/query-types.md
https://github.com/blacksmithgu/obsidian-dataview/blob/master/docs/docs/queries/data-commands.md

Source: 
https://github.com/groepl/Obsidian-Templates
-->
