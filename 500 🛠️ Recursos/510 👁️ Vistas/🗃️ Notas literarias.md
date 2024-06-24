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
action QuickAdd: Nueva nota literaria
```
^button-x675
```dataviewjs
const {fieldModifier: f} =
this.app.plugins.plugins["metadata-menu"].api;

dv.table(["Tipo", "Nombre", "De"],
		dv.pages("#🗃️")
		.sort(p => p.file.ctime, "desc")
		.filter(p => !p.file.path.includes("plantillas"))
		.map(p => [
		p["Tipo"],
		p.file.link,
		p["De"]
		])
		)
```