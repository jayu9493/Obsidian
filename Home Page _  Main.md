---
tags:
  - Homepage
related: []
creat: 29/08/2024
---
[[Main Pages - DE]]
### Protection systems study
```dataview
TABLE Completed
FROM #Protectionsys 
```
### All electrical components
```dataview
TABLE completed
FROM  #Electrical 
```
### Most recent 5 notes:

```dataview
TABLE file.mtime as "createdon"
FROM ""
SORT file.mtime desc
LIMIT 5
```

### Most unused one:
```dataview
TABLE file.mtime as "createdon"
FROM ""
WHERE !contains(file.path, "Attachments")
SORT file.mtime asc
LIMIT 5
```
