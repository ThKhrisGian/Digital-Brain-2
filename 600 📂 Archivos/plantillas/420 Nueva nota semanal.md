---
Año: '[[Año <% tp.date.now("YYYY", 1, tp.file.title, "gggg-[W]ww") %>]]'
---
<% tp.date.now("[Semana] W [- Año] YYYY", 1, tp.file.title, "gggg-[W]ww") %>
<< [[<% tp.date.now("gggg-[W]ww", "P-1W", tp.file.title, "gggg-[W]ww") %>]] || [[<% tp.date.now("gggg-[W]ww", "P1W", tp.file.title, "gggg-[W]ww") %>]] >>
***
## Objetivos de esta semana
1. Obj. 1

## 🌞 Días
- [[<% tp.date.weekday("YYYY-MM-DD", 0, tp.file.title, "gggg-[W]ww") %>|Lunes]]
- [[<% tp.date.weekday("YYYY-MM-DD", 1, tp.file.title, "gggg-[W]ww") %>|Martes]]
- [[<% tp.date.weekday("YYYY-MM-DD", 2, tp.file.title, "gggg-[W]ww") %>|Miércoles]]
- [[<% tp.date.weekday("YYYY-MM-DD", 3, tp.file.title, "gggg-[W]ww") %>|Jueves]]
- [[<% tp.date.weekday("YYYY-MM-DD", 4, tp.file.title, "gggg-[W]ww") %>|Viernes]]
- [[<% tp.date.weekday("YYYY-MM-DD", 5, tp.file.title, "gggg-[W]ww") %>|Sábado]]
- [[<% tp.date.weekday("YYYY-MM-DD", 6, tp.file.title, "gggg-[W]ww") %>|Domingo]]