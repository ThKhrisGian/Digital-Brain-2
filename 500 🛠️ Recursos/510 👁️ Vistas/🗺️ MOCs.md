---
cssclasses:
  - hide-metadata--r
  - banner
tags:
  - 👁️
---
![[banner-gif01.gif|banner]]
```button
name + Nuevo MOC
type command
action QuickAdd: Nuevo MOC
```
^button-t5cz
```dataviewjs
const {fieldModifier: f} =
this.app.plugins.plugins["metadata-menu"].api;

dv.table(["Nombre"],
		dv.pages('#🗺️')
		.filter(p => !p.file.path.includes("plantillas"))
		.filter(p => !p.file.path.includes("fileClass"))
		.sort(p => p.file.name)
		.map( p => [
		p.file.link]
		)
		)
```