
-------

creation date: [[<% tp.date.now("YYYY.MM.DD") %>]] 

--------

tags: #daily_note  #Notes #매일매일

---  
# 매일매일 반복작업 
- [ ] #매일매일 브랜치 동기화 🔁 every day when done ⏳ [[<% tp.date.now("YYYY-MM-DD") %>]] 
	- [ ] #매일매일 update branch  🔁 every day when done ⏳ [[<% tp.date.now("YYYY-MM-DD") %>]]
	- [ ] #매일매일 resources branch  🔁 every day when done ⏳ [[<% tp.date.now("YYYY-MM-DD") %>]]
	- [ ] #매일매일 3d art branch  🔁 every day when done ⏳ [[<% tp.date.now("YYYY-MM-DD") %>]]

--------






# [[<% tp.date.now("YYYY.MM.DD") %>]]  체크해야 할 일감
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