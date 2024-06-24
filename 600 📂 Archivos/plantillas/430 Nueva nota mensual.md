---
Año: '[[Año <% tp.date.now("YYYY", 1, tp.file.title, "YYYY-MM") %>]]'
---
<% tp.date.now("MMMM YYYY", 0, tp.file.title, "YYYY-MM") %>
<< [[<% tp.date.now("YYYY-MM", "P-1M", tp.file.title, "YYYY-MM") %>]] || [[<% tp.date.now("YYYY-MM", "P1M", tp.file.title, "YYYY-MM") %>]] >>
***
## Objetivos de este mes

## 🌞 Días
```dataviewjs
let days = dv.pages("#📖").where(p => dv.date(p.file.name) >= dv.date('<% moment(tp.file.title, "YYYY-MM").startOf("month").format("YYYY-MM-DD") %>') && dv.date(p.file.name) <= dv.date('<% moment(tp.file.title, "YYYY-MM").endOf("month").format("YYYY-MM-DD") %>')).sort(p => p.file.name, 'desc')

dv.table(["Día"],
		days
		.map(p => [
		p.file.link])
		)
```