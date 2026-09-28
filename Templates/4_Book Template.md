---
tags: 
  - type/project
  - type/chapter 
  - theme/xyz
  - target/ebook 
visual: "![[IMAGE.png]]"
title_short: "e1"
rule: +++ Add simple rule here +++
chapter: "0.0"
version: "0.1"
book_version: 0.19
status: draft
word_count: 0
bar: <progress max=100 value=0></progress><br>0% first ideas
created: {{DATE:YYYY-MM-DD, HH:mm}}
modified: {{DATE:YYYY-MM-DD, HH:mm}}
published:
views: 0
feedbacks: 0
template_type: Book
template_version: "1.31"
---
<!--  
status: draft, final, published, revised 
bar: <progress max=100 value=0></progress><br>0% first ideas 
	10% takeaway promised, 20% used for teaching, 30% value offered  
	40% front-loaded value, 50% high value-per-page, 60% value tested
	70% feedback received, 80% value improved, 90% finally polished, 100% recommended 
-->

# {{Title}} - e1
<!--  Clear and descriptive title -->

```dataviewjs 
var progress_bar = (dv.current().bar);
var note_status = (dv.current().status);
dv.paragraph(progress_bar + ', ' + note_status);
```

<!-- My sketchnote if available -->
```dataviewjs 
dv.paragraph(dv.current().visual);
```

<!-- Motivational quote if available -->

<!-- Main content of this chapter -->

<!-- Simple rule to remember  -->
```dataviewjs 
dv.paragraph('> ' + dv.current().rule);
```

<!-- References in footnote  -->



---
# Back Matter

**_Sources_**
<!-- always keep a link to the [[source]] --> 
- based_on::

**_References_**
<!-- see: [[permanent note]] because <reason> -->
- see:: 

**_Context_**
<!-- the scene at capture — see Subjective Context Principle. Optional but preferred. -->
- scene:: 

**_Terms_**
<!-- optional link to [[literature note]] with term & definition. -->
- term::

**_Targets_**
<!-- optional link to [[project note]] or published content. -->
- used_in::

**_Template Help_**
<!-- link to external help pages on GitHub. -->
- [GitHub - Obsidian-Templates for Zettelkasten.](https://github.com/groepl/Obsidian-Templates)

<!--  © 2022-2026 by Edmund Gröpl under CC BY-NC-SA 4.0 -->
