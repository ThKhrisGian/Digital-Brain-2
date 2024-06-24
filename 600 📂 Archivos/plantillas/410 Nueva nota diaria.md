---
Semana:
  - "[[<% tp.date.now("gggg-[W]ww", "0", tp.file.title, "YYYY-MM-DD") %>]]"
Mes: 
  - "[[<% tp.date.now("YYYY-MM", "0", tp.file.title, "YYYY-MM-DD") %>]]"
cssclasses: 
  - hide-classes--e
tags:
  - 📖
---
<% tp.date.now("dddd -  MMMM Do YYYY", 0, tp.file.title, "(📅) YYYY-MM-DD") %>

<< [[<% tp.date.now("YYYY-MM-DD", -1, tp.file.title, "YYYY-MM-DD") %>]] || [[<% tp.date.now("YYYY-MM-DD", 1, tp.file.title, "YYYY-MM-DD") %>]] >>
***
## 📥 Input
- [ ] Empieza aquí

## ✅ Tareas
### ⭐ Tareas para Hoy
```tasks
due <% tp.date.now("YYYY-MM-DD", 0, tp.file.title, "YYYY-MM-DD") %>
sort by priority
not done
```

### ✔ Completadas Hoy
```tasks
done <% tp.date.now("YYYY-MM-DD", 0, tp.file.title, "YYYY-MM-DD") %>
hide task count
hide backlinks
```

## 📝 Notas

```dataview
table
from #📝 
where date(file.cday) = date(this.file.name)
```