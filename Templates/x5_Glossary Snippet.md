<!-- "Glossary Entries" for 5_Structure Notes. Use as example and modify. -->
<!-- template_version: "0.3" -->
```dataview
TABLE WITHOUT ID
	file.link as Terms, 
	lead AS "Definitions",
	length(file.inlinks) as "In"
FROM #type/term
WHERE lead != empty
SORT file.name ASC
```
