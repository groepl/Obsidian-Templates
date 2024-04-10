---
tags:
  - type/structure
  - structure/list
  - chart/radar-chart
  - theme/zettelkasten
  - target/forumobsidian
aliases: 
created: 2023-04-08, 18:19
modified: 2024-04-10, 10:56
template_type: Structure
template_version: "1.4"
---

# Wheel of Life - Related Ideas

<!-- Main STRUCTURE of my content -->

```dataviewjs 

// === Notes till yy ===

var yy = "20250101";
var yyyy = moment(yy).format("YYYY-MM-DD");

// === Count notes ===

var count_carrer = dv
	.pages('#theme/work OR #theme/management OR #theme/datastory OR #theme/agile OR #theme/facilitation OR #theme/thinking OR #theme/writing OR #theme/sketchnotes')
	.where (p => p.created < yyyy)
	.length;
	
var count_learn = dv
	.pages('#theme/learning OR #theme/ai OR #theme/pkm OR #theme/zettelkasten OR #theme/obsidian OR #theme/tools')
	.where (p => p.created < yyyy)
	.length;
	
var count_relationships = dv
	.pages('#theme/community OR #theme/family OR #theme/wol OR #theme/socialmedia OR #theme/sketchnotes')
	.where (p => p.created < yyyy)
	.length;

var count_wealth = dv
	.pages('#theme/finance OR #theme/living OR #theme/travel')
	.where (p => p.created < yyyy)
	.length;
	
var count_health = dv
	.pages('#theme/health OR #theme/self OR #theme/sports OR #theme/climbing OR #theme/hiking OR #theme/swimming OR #theme/skiing OR #theme/cooking OR #theme/psychology')
	.where (p => p.created < yyyy)
	.length;
	
// --- Set Colors ---
const CHART_COLORS = {
	  red: '#B51A00',
	  orange: 'rgb(255, 159, 64)',
	  yellow: '#FAC141',
	  yellow_rgb: 'rgb(250, 193, 63, 0.0)',
	  green: 'rgb(75, 192, 192, 0.2)',
	  blue: '#417CFA',
	  black: '#000000',
	  grey: '#d6dcde',
	  grey_rgb: 'rgb(221, 221, 221, 0.2)',
	  light_grey: '#DDDDDD',
	  light_grey_rgb: 'rgb(221, 221, 221, 0.3)',
	  ultralight_grey: '#EEEEEE',
	  dark_grey: '#CCCCCC',
	  white: '#FFFFFF'
	}

const NAMED_COLORS = [
	  CHART_COLORS.red,
	  CHART_COLORS.orange,
	  CHART_COLORS.yellow,
	  CHART_COLORS.green,
	  CHART_COLORS.blue,
	  CHART_COLORS.purple,
	  CHART_COLORS.grey,
	]

// --- Create Chart ---
const chartData = { 
	type: 'radar', 
	data: { 
		labels: [
			'Career', 
			'Learn',
			'Relationships', 
			'Wealth',
			'Health'], 
		datasets: [
			{
			label: 'actual',
			data: [count_carrer, 
					count_learn, 
					count_relationships, 
					count_wealth,
					count_health],
			backgroundColor: [
				CHART_COLORS.yellow_rgb, 
				CHART_COLORS.yellow_rgb, CHART_COLORS.yellow_rgb,
				CHART_COLORS.yellow_rgb, CHART_COLORS.yellow_rgb], 
			borderColor: CHART_COLORS.yellow, 
			borderWidth: 2
			},
			{
			label: '2023',
			data: [539, 560, 368, 31, 152],
			backgroundColor: [
				CHART_COLORS.grey_rgb, 
				CHART_COLORS.grey_rgb, CHART_COLORS.grey_rgb,
				CHART_COLORS.grey_rgb, CHART_COLORS.grey_rgb], 
			borderColor: CHART_COLORS.dark_grey, 
			borderWidth: 2
			},
			{
			label: '2022',
			data: [294, 181, 222, 18, 64],
			backgroundColor: [
				CHART_COLORS.light_grey_rgb, 
				CHART_COLORS.light_grey_rgb, 
				CHART_COLORS.light_grey_rgb,
				CHART_COLORS.light_grey_rgb,
				CHART_COLORS.light_grey_rgb], 
			borderColor: CHART_COLORS.dark_grey, 
			borderWidth: 2
			}
		] 
	},
	options: {
		indexAxis: 'x',
        plugins: {
            title: {
                display: false,
                text: 'Custom Chart Title'
            },
            subtitle: {
                display: false,
                text: 'Custom Chart Subtitle'
            },
            legend: {
	            display: true,
                position: 'right'
            }
        }
    }

} 

window.renderChart(chartData, this.container)

```

> If the ideas in your Zettelkasten don't support the goals on your wish list, it's a call for a purposeful realignment.

**Details**
<!-- Dataview table. Use as example and modify. -->
###### `Career: #theme/work OR #theme/management OR #theme/datastory OR #theme/agile OR #theme/facilitation OR #theme/thinking OR #theme/writing OR #theme/sketchnotes`
```dataview
TABLE WITHOUT ID
	file.link as Career, 
	modified AS "modified", 
	file.folder AS "folder" 
FROM #theme/work OR #theme/management OR #theme/datastory OR #theme/agile OR #theme/facilitation OR #theme/thinking OR #theme/writing OR #theme/sketchnotes
SORT modified DESC
```



###### `Learn: #theme/learning OR #theme/ai OR #theme/pkm OR #theme/zettelkasten OR #theme/obsidian`
```dataview
TABLE WITHOUT ID
	file.link as Learn, 
	modified AS "modified", 
	file.folder AS "folder" 
FROM #theme/learning OR #theme/ai OR #theme/pkm OR #theme/zettelkasten OR #theme/obsidian OR #theme/tools
SORT modified DESC
```



###### `Relationships: #theme/community OR #theme/family OR #theme/wol OR #theme/socialmedia OR #theme/sketchnotes`
```dataview
TABLE WITHOUT ID
	file.link as Relationships, 
	modified AS "modified", 
	file.folder AS "folder" 
FROM #theme/community OR #theme/family OR #theme/wol OR #theme/socialmedia OR #theme/sketchnotes
SORT modified DESC
```





###### `Wealth: #theme/finance OR #theme/living OR #theme/travel`
```dataview
TABLE WITHOUT ID
	file.link as Wealth, 
	modified AS "modified", 
	file.folder AS "folder" 
FROM #theme/finance OR #theme/living OR #theme/travel
SORT modified DESC
```


###### `Health: #theme/health OR #theme/self OR #theme/sports OR #theme/climbing OR #theme/hiking OR #theme/swimming OR #theme/skiing OR #theme/cooking OR #theme/psychology`

```dataview
TABLE WITHOUT ID
	file.link as Wellness, 
	modified AS "modified", 
	file.folder AS "folder" 
FROM #theme/health OR #theme/self OR #theme/sports OR #theme/climbing OR #theme/hiking OR #theme/swimming OR #theme/skiing OR #theme/cooking OR #theme/psychology
SORT modified DESC
```

<!-- Options 
TABLE WITHOUT ID
	file.folder AS ...
	file.link AS ...
	file.name AS ...
	file.etags AS ...
	length(file.outlinks) AS …
	length(file.inlinks) AS …
	length(file.etags) AS …
	dateformat(file.cday, "yyyy-MM-dd") AS Date
	dateformat(file.cday, "yyyy-LLL-dd") AS Date
	dateformat(date(created, "yyyy-mm-dd, HH:MM"), "yyyy-mm-dd") AS "created" ⚡️bug in DataView 


FROM #target/forumzettelkasten  : when using tags
FROM "Books"                                : when using folders
FROM ""                                          : when using all folders
FROM #status/open OR #status/wip

SORT created DESC
SORT file.name ASC

WHERE read = 2023
WHERE status = "open"
WHERE contains(file.name,"LernOS Zettelkasten")
WHERE sketchnote != empty

LIMIT 3

---
More about: 
https://github.com/blacksmithgu/obsidian-dataview/blob/master/docs/docs/queries/query-types.md
https://github.com/blacksmithgu/obsidian-dataview/blob/master/docs/docs/queries/data-commands.md

Source: 
https://github.com/groepl/Obsidian-Templates
-->



---

# Back Matter
**Source**


**Questions**
<!-- What remains for you to consider? --> 
- 


**Terms**
<!-- Links to definition pages -->
- 


**References**
<!-- Links to pages not referenced in the content -->
- [Obsidian Charts - Plugin](Obsidian%20Charts%20-%20Plugin.md)
- [The ideas in your Zettelkasten](The%20ideas%20in%20your%20Zettelkasten.md)
- [8 Categories for Ideas and Wishes](8%20Categories%20for%20Ideas%20and%20Wishes.md)
- [Compared Wheels of Life](Compared%20Wheels%20of%20Life.md)

**Target**
- target:: [Life Map/Compass - #5 by Edmund - Knowledge management - Obsidian Forum](https://forum.obsidian.md/t/life-map-compass/69160/5?u=edmund)