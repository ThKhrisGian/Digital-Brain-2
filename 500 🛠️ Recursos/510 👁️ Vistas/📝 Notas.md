---
cssclasses:
  - hide-metadata--r
  - banner
  - table-lines
  - table-numbers 
tags:
  - 👁️
---
![[banner-gif01.gif|banner]]
```button
name + Nueva nota
type command
action QuickAdd: Nueva nota
color default
```
^button-xpnv
```dataviewjs
const {fieldModifier: f} =
this.app.plugins.plugins["metadata-menu"].api;

dv.table(["Nombre"],
		dv.pages('#📝')
		.filter(p => !p.file.path.includes("plantillas"))
		.filter(p => !p.file.path.includes("fileClass"))
		.sort(p => p.file.ctime, "desc")
		.map( p => [
		p.file.link]
		)
		)
```
