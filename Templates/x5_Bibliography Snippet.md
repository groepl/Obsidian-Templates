<!-- "Bibliography table" for 5_Structure Notes with data from "2_Book Template". Use as example and modify. -->
<!-- template_type: Bibliography Snippet -->
<!-- template_version: "0.1" -->
```dataview 
TABLE WITHOUT ID
	bibliography AS "Books",
	file.link as Notes
From #type/book 
Where contains(status, "reading") 
SORT bibliography ASC
```  
