---
cssclasses:
  - hide-metadata--r
  - banner
tags:
  - 👁️
---
![[banner-gif01.gif|banner]]
```button
name + Nueva nota
type command
action QuickAdd: Nuevo recurso bibliográfico
```
^button-0wbh
```dataviewjs
const {fieldModifier: f} =
this.app.plugins.plugins["metadata-menu"].api;

dv.table(["Tipo", "Nombre", "Estado"],
		dv.pages('#📌')
		.filter(p => !p.file.path.includes("plantillas"))
		.filter(p => !p.file.path.includes("fileClass"))
		.sort(p => p.file.ctime, "desc")
		.map( p => [
		p["Tipo"],
		p.file.link,
		p["Estado"]]
		)
		)
```
