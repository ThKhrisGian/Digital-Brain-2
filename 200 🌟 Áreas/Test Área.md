---
tags:
  - 🌟
---
## Descripción

## MOCs destacados

## Recursos destacados

## 💼 Proyectos
```dataviewjs
const {fieldModifier: f} =
this.app.plugins.plugins["metadata-menu"].api;
let paginas = dv.pages(dv.current().file.link + " and #💼")

if (paginas.length > 0){
	dv.table(["Nombre", "Fecha Límite", "Estado"], paginas
		.sort(b => b["Estado"], "asc")
		.map(b => [b.file.link, f(dv, b, "F-limite"),f(dv, b, "Estado")]))
} else{
	dv.el("span", "No hay proyectos")
}
```
