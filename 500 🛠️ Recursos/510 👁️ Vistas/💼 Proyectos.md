---
cssclasses:
  - hide-metadata--r
  - banner
  - table-numbers
  - table-lines
  - max
tags:
  - 👁️
---
![[banner01.jpg|banner]]
```button
name + Nuevo proyecto
type command
action QuickAdd: Nuevo proyecto
```
^button-6k78
````tabs
tab: 🟡

```dataviewjs
const {fieldModifier: f} =
this.app.plugins.plugins["metadata-menu"].api;

dv.table(["Nombre", "Fecha Inicio", "Fecha Límite", "Estado", "Progreso"],
		 dv.pages("#💼")
		 .filter(p => !p.file.path.includes("plantillas"))
		 .filter(p => p["Estado"] == "🟡 en proceso")
		 .map(p => {
            const totalTasks = p.file.tasks.length;
            const completedTasks = p.file.tasks.filter(task => task.completed).length;
            const progressValue = totalTasks > 0 ? Math.round((completedTasks / totalTasks) * 100) : 0;
            return [
                p.file.link,
                f(dv, p, "F-inicio"),
                f(dv, p, "F-limite"),
                f(dv, p, "Estado"),
                `<progress value="${progressValue}" max="100"></progress><br>${progressValue}% completedo`
            ];
        }))
```

tab: 🔴

```dataviewjs
const {fieldModifier: f} =
this.app.plugins.plugins["metadata-menu"].api;

dv.table(["Nombre", "Fecha Inicio", "Fecha Límite", "Estado", "Progreso"],
		 dv.pages("#💼")
		 .filter(p => !p.file.path.includes("plantillas"))
		 .filter(p => p["Estado"] == "🔴 no iniciado")
		 .map(p => {
            const totalTasks = p.file.tasks.length;
            const completedTasks = p.file.tasks.filter(task => task.completed).length;
            const progressValue = totalTasks > 0 ? Math.round((completedTasks / totalTasks) * 100) : 0;
            return [
                p.file.link,
                f(dv, p, "F-inicio"),
                f(dv, p, "F-limite"),
                f(dv, p, "Estado"),
                `<progress value="${progressValue}" max="100"></progress><br>${progressValue}% completedo`
            ];
        }))
```

tab: ⏸️

```dataviewjs
const {fieldModifier: f} =
this.app.plugins.plugins["metadata-menu"].api;

dv.table(["Nombre", "Fecha Inicio", "Fecha Límite", "Estado", "Progreso"],
		 dv.pages("#💼")
		 .filter(p => !p.file.path.includes("plantillas"))
		 .filter(p => p["Estado"] == "⏸️ en pausa")
		 .map(p => {
            const totalTasks = p.file.tasks.length;
            const completedTasks = p.file.tasks.filter(task => task.completed).length;
            const progressValue = totalTasks > 0 ? Math.round((completedTasks / totalTasks) * 100) : 0;
            return [
                p.file.link,
                f(dv, p, "F-inicio"),
                f(dv, p, "F-limite"),
                f(dv, p, "Estado"),
                `<progress value="${progressValue}" max="100"></progress><br>${progressValue}% completedo`
            ];
        }))
```

tab: 🟢

```dataviewjs
const {fieldModifier: f} =
this.app.plugins.plugins["metadata-menu"].api;

dv.table(["Nombre", "Fecha Inicio", "Fecha Límite", "Estado", "Progreso"],
		 dv.pages("#💼")
		 .filter(p => !p.file.path.includes("plantillas"))
		 .filter(p => p["Estado"] == "🟢 finalizado")
		 .map(p => {
            const totalTasks = p.file.tasks.length;
            const completedTasks = p.file.tasks.filter(task => task.completed).length;
            const progressValue = totalTasks > 0 ? Math.round((completedTasks / totalTasks) * 100) : 0;
            return [
                p.file.link,
                f(dv, p, "F-inicio"),
                f(dv, p, "F-limite"),
                f(dv, p, "Estado"),
                `<progress value="${progressValue}" max="100"></progress><br>${progressValue}% completedo`
            ];
        }))
```

tab: ⛔

```dataviewjs
const {fieldModifier: f} =
this.app.plugins.plugins["metadata-menu"].api;

dv.table(["Nombre", "Fecha Inicio", "Fecha Límite", "Estado", "Progreso"],
		 dv.pages("#💼")
		 .filter(p => !p.file.path.includes("plantillas"))
		 .filter(p => p["Estado"] == "⛔ cancelado")
		 .map(p => {
            const totalTasks = p.file.tasks.length;
            const completedTasks = p.file.tasks.filter(task => task.completed).length;
            const progressValue = totalTasks > 0 ? Math.round((completedTasks / totalTasks) * 100) : 0;
            return [
                p.file.link,
                f(dv, p, "F-inicio"),
                f(dv, p, "F-limite"),
                f(dv, p, "Estado"),
                `<progress value="${progressValue}" max="100"></progress><br>${progressValue}% completedo`
            ];
        }))
```

````