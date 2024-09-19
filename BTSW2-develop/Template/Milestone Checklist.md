


### 미 완료된 항목중 Tag #M4  일감 검색
```dataviewjs 
dv.taskList(dv.pages('#M4 and -"Template" and -"TODO"').file.tasks.where(t => t.text.includes("M4")).where(t => !t.completed) )
```
-------------------



###  Tag #update  일감 검색
```dataviewjs 
dv.taskList(dv.pages('-"Template" and -"TODO"').file.tasks.where(t => t.text.includes("#update")))
```



-------------
### Tag #런칭  일감 검색
```dataviewjs 
dv.taskList(dv.pages('-"Templete" and -"TODO"').file.tasks.where(t => t.text.includes("#런칭"))) 
```

--------------------------------

