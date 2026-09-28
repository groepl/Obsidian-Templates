<!-- "Quotes Index" for 5_Structure Notes. Use as example and modify. -->
<!-- template_version: "0.2" -->
```dataview
TABLE WITHOUT ID
	author AS Author, 
	quote AS Quote, 
	file.link as File
FROM #type/quote and 
	#theme/learning 
SORT author ASC
```
