---
tags:
  - 🏷️
---
```dataviewjs
const {fieldModifier: f} =
this.app.plugins.plugins["metadata-menu"].api;
let paginas = dv.pages(dv.current().file.link + "").filter(p => !p.tags.includes("📝"))

let notas = dv.pages(dv.current().file.link + "").filter(p => p.tags.includes("📝"))

if (notas.length > 0){
	dv.table(["Nombre", "Estado"], notas
		.sort(b => b.file.name)
		.map(b => [b.file.link, f(dv, b, "Estado")]))
	dv.el("br", "")
}

if (paginas.length > 0){
	dv.table(["Nombre", "Tipo"], paginas
		.sort(b => b.file.name)
		.map(b => [b.file.link, f(dv, b, "Tipo")]))
}
```
