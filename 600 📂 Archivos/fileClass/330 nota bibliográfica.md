---
fields:
  - name: Tipo
    type: Select
    options:
      sourceType: ValuesList
      valuesList:
        "1": 🎥
        "2": 📚
        "3": 💡
        "4": 📰
        "5": 🎧
    path: ""
    id: UqptS6
  - name: Estado
    type: Select
    options:
      sourceType: ValuesList
      valuesList:
        "1": 🟥
        "2": 🟨
        "3": 🟩
    path: ""
    id: xVTRgR
  - name: Autor
    type: MultiFile
    options: {}
    path: ""
    id: dsLIKP
  - name: URL
    type: Input
    options: {}
    path: ""
    id: GBYtgs
  - name: Etiquetas
    type: MultiFile
    options:
      dvQueryString: |-
        dv.pages("#🏷️")
        .filter(p => !p.file.path.includes("plantillas"))
        .filter(p => !p.file.path.includes("fileClass"))
        .sort(b => b.file.link)
    path: ""
    id: KjyhcS
version: "2.21"
limit: 20
mapWithTag: true
icon: package
tagNames:
  - 📌
filesPaths: 
bookmarksGroups: 
excludes: 
extends: 
savedViews: []
favoriteView: 
fieldsOrder:
  - UqptS6
  - xVTRgR
  - dsLIKP
  - GBYtgs
  - KjyhcS
---
