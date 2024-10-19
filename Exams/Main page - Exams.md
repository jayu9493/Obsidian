---
tags:
  - Homepage
related:
  - Exams
---
```dataview
TABLE file.name as "Note Title", Finished, Exam_date,file.mtime as "Last Modified"
FROM ""
WHERE Exam="Yes" AND "NO"
SORT file.mtime desc
```




## Subject preparation:
```dataview
TABLE  subject,Exam, playlist, created as "Date Created"
FROM ""
WHERE Exam != "Yes" AND Exam != "No" AND Exam != null
SORT created desc
```
