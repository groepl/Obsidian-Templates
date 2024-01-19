---
tags:
  - 
  - 
  - type/structure
  - 
  - 
  - 
aliases:
  - Kanban Board
created: 2022-06-04, 15:46
modified: 2023-11-03, 14:35
---
# Dataview - Kanban Board

<!-- Main STRUCTURE of my content -->

## 1_Backlog

```dataview
TABLE 
	file.cday AS "created", 
	priority AS prio,
	file.folder AS "folder" 
FROM #status/1_backlog 
SORT file.ctime ASCENDING
```

## 2_ToDo

```dataview
TABLE 
	file.cday AS "created", 
	priority AS prio,
	file.folder AS "folder" 
FROM #status/2_todo  
SORT file.ctime ASCENDING
```

## 3_Doing - WIP Limit: 3

```dataview
TABLE 
	file.cday AS "created", 
	priority AS prio,
	file.folder AS "folder" 
FROM #status/3_doing   
SORT priority DESC
```

## 4_Done

```dataview
TABLE 
	file.cday AS "created", 
	priority AS prio,
	file.folder AS "folder" 
FROM #status/4_done 
SORT file.ctime ASCENDING
LIMIT 5
```

