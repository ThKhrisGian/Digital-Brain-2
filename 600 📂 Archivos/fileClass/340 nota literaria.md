---
fields:
  - name: Tipo
    type: Select
    options:
      sourceType: ValuesList
      valuesList:
        "1": ✍️
        "2": 📃
        "3": 💬
        "4": 🖼️
        "5": 📋
        "6": 🔗
        "7": 📁
    path: ""
    id: rn4vJy
  - name: De
    type: File
    options:
      dvQueryString: |-
        dv.pages("#📌").filter(p => !p.file.path.includes("plantillas"))
        .filter(p => !p.file.path.includes("fileClass")).map(p => p.file.link)
    path: ""
    id: HHTHvx
version: "2.7"
limit: 20
mapWithTag: true
icon: package
tagNames:
  - 🗃️
filesPaths: 
bookmarksGroups: 
excludes: 
extends: 
savedViews: []
favoriteView: 
fieldsOrder:
  - rn4vJy
  - HHTHvx
---
