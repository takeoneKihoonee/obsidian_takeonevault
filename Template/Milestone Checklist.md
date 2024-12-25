


### 미 완료된 항목중 Tag #런칭  일감 검색
```dataviewjs 
dv.taskList(dv.pages('#런칭 and -"Template" and -"TODO"').file.tasks.where(t => t.text.includes("런칭")).where(t => !t.completed) )
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

