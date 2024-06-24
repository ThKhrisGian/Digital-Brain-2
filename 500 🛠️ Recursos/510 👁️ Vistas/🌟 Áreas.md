---
cssclasses:
  - hide-metadata--r
  - banner
tags:
  - 👁️
---
![[banner01.jpg|banner]]
```button
name + Nueva área
type command
action QuickAdd: Nueva área
```
^button-hj37
```dataviewjs
const {fieldModifier: f} =
this.app.plugins.plugins["metadata-menu"].api;

dv.table(["Nombre"],
		dv.pages('#🌟')
		.filter(p => !p.file.path.includes("plantillas"))
		.filter(p => !p.file.path.includes("fileClass"))
		.sort(p => p.file.name)
		.map( p => [
		p.file.link]
		)
		)
```