---
limit: 20
mapWithTag: true
icon: package
tagNames:
  - 💼
filesPaths: 
bookmarksGroups: 
excludes: 
extends: 
savedViews: []
favoriteView: 
fieldsOrder:
  - 4aqRP7
  - 7VceKa
  - ukofDh
  - D7fWNT
  - mDTuml
version: "2.26"
fields:
  - name: Estado
    type: Select
    options:
      sourceType: ValuesList
      valuesList:
        "1": 🔴 no iniciado
        "2": 🟡 en proceso
        "3": 🟢 finalizado
        "4": ⏸️ en pausa
        "5": ⛔ cancelado
    path: ""
    id: 4aqRP7
  - name: Área
    type: MultiFile
    options:
      dvQueryString: |-
        dv.pages("#🌟")
        .filter(p => !p.file.path.includes("Plantillas"))
        .filter(p => !p.file.path.includes("fileClass"))
        .sort(b => b.file.link)
    path: ""
    id: 7VceKa
  - name: F-inicio
    type: Date
    options:
      dateShiftInterval: 1 day
      dateFormat: YYYY-MM-DD
      defaultInsertAsLink: false
      linkPath: ""
    path: ""
    id: ukofDh
  - name: F-limite
    type: Date
    options:
      dateShiftInterval: 1 day
      dateFormat: YYYY-MM-DD
      defaultInsertAsLink: false
      linkPath: ""
    path: ""
    id: D7fWNT
  - name: F-terminado
    type: Date
    options:
      dateShiftInterval: 1 day
      dateFormat: YYYY-MM-DD
      defaultInsertAsLink: false
      linkPath: ""
    path: ""
    id: mDTuml
---
