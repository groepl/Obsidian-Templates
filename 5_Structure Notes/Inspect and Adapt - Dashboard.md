---
tags: type/structure structure/list structure/dashboard target/forumobsidian target/forumzettelkasten type/dataviewjs
aliases: 
lead: +++ Lead paragraph goes here +++
rule: Simple Rules for Gardening
visual: "![[image.jpg]]"
created: 2023-10-29, 11:39
modified: 2023-12-02, 15:27
template_type: Structure
template-version: "1.8"
updated: 2023-11-07T19:36
---

# Inspect and Adapt - Dashboard

<!-- Main STRUCTURE of my content -->
## Overview 
```dataviewjs 
// === WORKFLOW ===
// --- Count UNFINISHED notes
var count_fleeting = dv.pages('"1_Fleeting Notes"').length; 
var count_literature = dv.pages('"2_Literature Notes"').length; 
var count_onenote = dv.pages('"OneNote"').length; 
var count_daily = dv.pages('"5_Structures"')
	.where(s => s.tasks >= 1).length;
var sum_workflow =
	count_fleeting + count_literature + count_onenote + count_daily;

// === NOTES ===
// --- Count notes in WITHOUT TIMESTAMP 
var count_timestamp = dv.pages('"3_Permanent Notes"')
	.where(y => y.modified == null)
	.length;

// --- Count notes in WITHOUT LEAD 
var count_lead = dv.pages('"3_Permanent Notes"')
	.where(y => y.lead == null || y.lead == "+++ Lead paragraph goes here +++")
	.length;

// --- Count sketchnotes in WITHOUT VISUAL 
var count_visual = dv.pages('#type/sketchnote')
	.where(y => y.visual == null || y.visual == "![[image.jpg]]")
	.length;
		
// --- Count books in WITHOUT AUTHORS 
var count_books = dv.pages('#type/book')
	.where(y => y.author == null)
	.length;
	
// --- Count quotes in WITHOUT AUTHORS 
var count_quotes = dv.pages('#type/quote')
	.where(y => y.author == null)
	.length;
	
// --- Count terms in WITHOUT DEFINITIONS 
var count_definitions = dv.pages('#type/term')
	.where(y => y.lead == null)
	.length;
	
var sum_notes = 
	count_timestamp + count_lead + count_visual + count_books + count_quotes + count_definitions;

// === FOLDERS ===
// --- Count notes in WRONG FOLDERS
var count_term = dv.pages('#type/term AND !"4_References"').length;
var count_quote = dv.pages('#type/quote AND !"4_References"').length;
var count_book = dv.pages('#type/book AND !"4_References"').length;
var count_tool = dv.pages('#type/tool AND !"4_References"').length;
var sum_folders = 
	count_term + count_quote + count_book + count_tool;

// === LINKS ===
// --- Count notes with MISSING LINKS
var count_orphan = dv.pages('"3_Permanent Notes"')
	.where(s => s.file.outlinks.length == 0)
	.where(t => t.file.inlinks.length == 0)
	.length;
	
var count_zero_out = dv.pages('"3_Permanent Notes"')
	.where(s => s.file.outlinks.length == 0)
	.where(s => s.file.inlinks.length != 0)
	.length;

// --- Count unresolved links
var InterestLevel = 1; 
var r = Object.entries(dv
	.app.metadataCache.unresolvedLinks) 
	.filter( ( [k,v] )=> Object.keys( v ).length ) 
	.flatMap( ( [k,v] ) => Object.keys( v )
	.map(x => dv.fileLink( x )));  
var count_unresolved_links = 
	dv.array( r )
	    .groupBy( t => t )
	    .where( t => t.rows.length > InterestLevel )
		.length;

var sum_links =
	count_orphan + count_zero_out + count_unresolved_links;
	
// === TAGS ===
// --- Count notes WITHOUT TAGS
var count_tags = dv.pages('"3_Permanent Notes"')
	.where(s => s.file.tags.length == 0).length;
var count_tag_type = dv.pages('"3_Permanent Notes"')
	.where(p => p.file.tags.length != 0)
	.where(f => !f.file.tags.includes('#type'))
	.length;
var count_tag_theme = dv.pages('"3_Permanent Notes"')
	.where(p => p.file.tags.length != 0)
	.where(f => !f.file.tags.includes('#theme'))
	.length;
var sum_tags =
	count_tags + count_tag_type + count_tag_theme;

// === Summarize NOTES ===
var sum_count = 
	sum_workflow + sum_notes +
	sum_folders +
	sum_links + sum_tags;

// === Count TASKS ===
var count_tasks = dv.pages('"3_Permanent Notes"').file.tasks.length;
var count_reference_tasks = dv.pages('"4_References"').file.tasks.length;
var count_structure_tasks = dv.pages('"5_Structures"').file.tasks.length;
var count_project_tasks = dv.pages('"6_Project Notes"').file.tasks.length;

// === Summarize TASKS ===
var sum_tasks = 
	count_tasks + count_reference_tasks + count_structure_tasks + 
	count_project_tasks;

// === LOST AND FOUND
// --- Count UN-MODIFIED NOTES
var count_unmodified = dv.pages('"3_Permanent Notes"')
	.where(s => s.modified == s.created)
	.length;
	
var count_zero_in = dv.pages('"3_Permanent Notes"')
	.where(s => s.file.inlinks.length == 0)
	.where(s => s.file.outlinks.length != 0)
	.length;
	
var count_orphan_2 = dv.pages('"3_Permanent Notes" OR "4_References" OR "5_Structures"')
	.where(s => s.file.tags.length == 0)
	.where(s => s.file.outlinks.length == 0)
	.where(t => t.file.inlinks.length == 0)
	.length;


// === Show results ===
dv.paragraph(
	'**Workflow**<br>' +
		count_fleeting + ' - [Fleeting Notes to be processed](Fleeting%20Notes%20to%20be%20processed.md)<br>' +
		count_literature + ' - [Literature Notes to be processed](Literature%20Notes%20to%20be%20processed.md)<br>' +
		count_onenote + ' - [Imported Notes to be processed](Imported%20Notes%20to%20be%20processed.md)<br>' +
		count_daily  + ' - [Daily Notes to be processed](Heatmap%20Calendar%20with%20Tasks.md)<br><br>' +

	'**Notes**<br>' +
		count_timestamp + ' - [Permanent Notes without timestamp](Notes%20without%20timestamps.md) <br>'	+
		count_lead + ' - [Permanent Notes without lead](Notes%20without%20lead.md) <br>'	+		
		count_visual + ' - [Sketchnotes without visual](Sketchnotes%20without%20visual.md) <br>'	+
		count_books + ' - [Books without author](Books%20without%20Authors.md) <br>'	+
		count_quotes + ' - [Quotes without author](Quotes%20without%20Authors.md) <br>'	+
		count_definitions + ' - [Terms without definition](Terms%20without%20Definitions.md) <br><br>' +

	'**Folders**<br>' +
		sum_folders + ' - [Notes in wrong folders](Notes%20in%20wrong%20folders.md)<br><br>' +
 
	'**Links**<br>' +
		count_orphan  + ' - [Permanent Notes without any links](Permanent%20Notes%20without%20any%20links.md) <br>' +
		count_zero_out  + ' - [Permanent Notes without out-links](Permanent%20Notes%20without%20out-links.md)<br>' +
		count_unresolved_links + ' - [Permanent Notes with unresolved links](Permanent%20Notes%20with%20unresolved%20links.md)<br><br>' +


	'**Tags**<br>' +
		count_tags  + ' - [Permanent Notes without any tags](Permanent%20Notes%20without%20any%20tags.md)<br>'  +
		 	count_tag_type + ' - [Permanent Notes without TYPE tag](Permanent%20Notes%20without%20type%20tag.md)<br>' +
 		count_tag_theme + ' - [Permanent Notes without THEME tag](Permanent%20Notes%20without%20theme%20tag.md)<br><br>' +

// ===
	'= **' + sum_count  + ' - Note elements to be processed or completed**<br><hr>' +
// ===

	'**Tasks**<br>' +
		count_tasks  + ' - [Tasks from Permanent Notes to be finished](Permanent%20Notes%20with%20tasks%20to%20be%20finished.md)<br>'  +
		count_reference_tasks  + ' - [Tasks from References to be finished](Reference%20tasks%20to%20be%20finished.md)<br>'  +
		count_structure_tasks  + ' - [Tasks from Structures to be finished](Structure%20tasks%20to%20be%20finished.md)<br>'  +
		count_project_tasks  + ' - [Tasks from Project Notes to be finished](Project%20Note%20tasks%20to%20be%20finished.md)<br><br>'  +

// ===
	'= **' + sum_tasks +  ' - Tasks to be finished**<br><hr>' +
// ===

	'**Lost and found**<br>' +
		count_unmodified  + ' - [Permanent Notes never been modified](Permanent%20Notes%20never%20modified.md) <br>' +
		count_zero_in  + ' - [Permanent Notes never referenced](Permanent%20Notes%20without%20in-links.md)<br>' +
		count_orphan_2  + ' - [Orphans to be integrated](Orphans%20to%20be%20integrated.md) <br>'
	);
```

***

## Burndown
```dataviewjs 

// --- collect data ---
var labels = [
	"2023-10-28", "2023-10-29", "2023-10-30", "2023-10-31", "2023-11-01",
	"2023-11-02", "2023-11-03", "2023-11-04", "2023-11-05", "2023-11-06",
	"2023-11-08", "2023-11-10", "2023-11-11", "2023-11-12", "2023-11-13",
	"2023-11-14", "2023-11-15", "2023-11-16", "2023-11-17", "2023-11-18",
	"2023-11-19", "2023-11-20", "2023-11-21", "2023-11-24", "2023-11-25",
	"2023-11-26", "2023-11-27", "2023-11-28", "2023-12-01", "2023-12-02", 
	"2023-12-31"
	];
var	data_1 = [
	988, 985, 1037, 1035, 1027,
	1022, 1188, 1176, 1153, 1150,
	1106, 1266, 1484, 1469, 1431,
	1393, 1384, 1208, 1143, 1299,
	1262, 1498, 1453, 1440, 2161,
	2145, 2126, 2059, 2038, 2085,
	]; 
var	data_2 = [
	393, 392, 391, 391, 392,
	393, 399, 400, 403, 404,
	407, 407, 407, 407, 408,
	409, 414, 415, 415, 415,
	417, 417, 417, 420, 420,
	420, 420, 421, 426, 426,
	]; 
	
var	data_3 = [
	,,,,, 
	,,,,, ,,1484,,,
	,,,,, ,,,,,
	,,,,,
	0
	]; 
var	data_4 = [
	,,,,,
	,,,,, ,,407,,,
	,,,,, ,,,,,
	,,,,,
	0
	]; 

// --- define chart colors ---
const CHART_COLORS = {
	  red: '#B51A00',
	  orange: 'rgb(255, 159, 64)',
	  yellow: '#FAC141',
	  green: 'rgb(75, 192, 192)',
	  blue: '#417CFA',
	  black: '#000000',
	  grey: '#CCCCCC',
	  white: '#FFFFFF'
	}

// --- create the charts ---
const burndownChart = { 
	type: 'line', 
	data: { 
	labels: labels,
	datasets: [
		{ 
		label: 'Notes to be processed', 
		data: data_1, 
		backgroundColor: CHART_COLORS.yellow, 
		borderColor: CHART_COLORS.yellow, 
		borderWidth: 1 
		},
		{ 
		label: 'Tasks to be finished', 
		data: data_2, 
		backgroundColor: CHART_COLORS.black, 
		borderColor: CHART_COLORS.black, 
		borderWidth: 1 
		},
		{ 
		label: 'Notes burndown', 
		data: data_3, 
		backgroundColor: CHART_COLORS.white, 
		borderColor: CHART_COLORS.grey, 
		borderWidth: 1,
		borderDash: [5],
		spanGaps: true 
		},
		{ 
		label: 'Tasks burndown', 
		data: data_4, 
		backgroundColor: CHART_COLORS.white, 
		borderColor: CHART_COLORS.grey, 
		borderWidth: 1,
		borderDash: [5],
		spanGaps: true 
		}
		]
	},
	options: {
		scales: {x: {
					type: 'time',
					time: {unit: 'day'}
					},
				y:  {
					min: 0
					}
				},
		plugins: {
//			title: {
//				text: "Work remaining", 
//				display: true, 
//				position: "left", 
//				font: {weight: "bold"}
//			},
			legend: { 
				display: true,
				position: "right",
				title: {
					text: "Legend", 
					display: true, 
					font: {weight: "bold"}
				}
			}
		}	
	}
} 

// --- render chart ---
window.renderChart(burndownChart, this.container); 

// --- chart configuration see Obsidian Charts ---
dv.paragraph('<small>_Configuration: [Obsidian Charts - Plugin](Obsidian%20Charts%20-%20Plugin.md)_ </small><br><br><br>');
```
## Modified Today
```dataview
table without id 
	file.link as "Permanent Notes", 
	modified as Modified,
	created as Created,
	file.folder as Folder 
FROM "3_Permanent Notes"
WHERE (file.mday = date(today)) AND (file.cday != date(today))
SORT file.mday desc
```
***
## Tools for Gardening
- [Inspect and Adapt - Tools for Gardening](Inspect%20and%20Adapt%20-%20Tools%20for%20Gardening.md)

---

## Simple Rules for Gardening
- [Inspect and Adapt - Simple Rules for Gardening](Inspect%20and%20Adapt%20-%20Simple%20Rules%20for%20Gardening.md)


***

# Back Matter
## Source
<!-- Always keep a link to the source. --> 
- 

## Tasks
<!-- What remains to be done with this note? --> 
- 

## Questions
<!-- What remains for you to consider? --> 
- 

## Terms
<!-- Links to definition pages -->
- [Burndown chart](Burndown%20chart.md)

## References
<!-- Links to pages not referenced in the content -->
- [6 - Review and Revise Your Notes - e1](6%20-%20Review%20and%20Revise%20Your%20Notes%20-%20e1.md)
- [8 - Inspect and Adapt Your Process - e1](8%20-%20Inspect%20and%20Adapt%20Your%20Process%20-%20e1.md)
- [Review unresolved links](Review%20unresolved%20links.md)
- [Orphans to be integrated](Orphans%20to%20be%20integrated.md)
- [Simple Rules](Simple%20Rules.md)
- [7 essential tools for Zettelkasten](7%20essential%20tools%20for%20Zettelkasten.md)
- [KonMari Method](KonMari%20Method.md)
- [How to use Marie Kondos 5 steps for a Zettelkasten](How%20to%20use%20Marie%20Kondos%205%20steps%20for%20a%20Zettelkasten.md)

**Dataview**
- [Dataviewjs examples using WHERE](Dataviewjs%20examples%20using%20WHERE.md)

**Line Chart**
- [Line Chart | Chart.js](https://www.chartjs.org/docs/latest/charts/line.html)

**Burndown**
- Schwaber, Ken. Agile Project Management with Scrum. Microsoft Press, 2004, 11-12.

**Target**
- https://forum.obsidian.md/t/inspect-and-adapt-how-to-use-zettelkasten-analytics/36799/17
- [Inspect and Adapt. How to use Zettelkasten Analytics - Knowledge management - Obsidian Forum](https://forum.obsidian.md/t/inspect-and-adapt-how-to-use-zettelkasten-analytics/36799/20?u=edmund)
- [Inspect and Adapt - Why You Need Empirical Process Control for Your Zettelkasten — Zettelkasten Forum](https://forum.zettelkasten.de/discussion/2471/inspect-and-adapt-why-you-need-empirical-process-control-for-your-zettelkasten)

