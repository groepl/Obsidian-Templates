---
tags: 
- type/chapter 
- theme/xyz
- target/ebook 
aliases:
visual: "![[IMGAGE.png]]"
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
template_type: Ebook
template_version: "1.23"
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

**Source**
<!-- Always keep a link to the source- --> 
- based_on::

**Tasks**
<!-- What remains to be done do get the final version? --> 

- [ ] Prepare final version 
- [ ] Publish on GitHub
- [ ] Review and revise

**Feedback**
<!-- What remains for you to consider in the draft version? --> 
**0.14**
- 

**Table of Content**
<!-- Links to chapters from e-book -->
- [004 - Contents](004%20-%20Contents.md)


**References**
<!-- Links to pages not referenced in the content -->
- 

**Target**
- target::

**Template Help**
<!-- Links to external help pages on GitHub. -->
- [Basic Template Structure](https://github.com/groepl/Obsidian-Templates#basic-template-structure)
- [How to Use Links](https://github.com/groepl/Obsidian-Templates#how-to-use-links)
- [How to Use Tags](https://github.com/groepl/Obsidian-Templates#how-to-use-tags)
- [How to Search Notes](https://github.com/groepl/Obsidian-Templates#how-to-search-notes)
- [Plugins Needed](https://github.com/groepl/Obsidian-Templates#obsidian-plugins-needed)
- [Find Latest Updates](https://github.com/groepl/Obsidian-Templates)

