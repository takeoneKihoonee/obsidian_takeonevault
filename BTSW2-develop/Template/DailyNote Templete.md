
-------

creation date: {{ Date }}:{{ Time }}

--------

tags: #daily_note  #Notes #매일매일

---  
# 매일매일 반복작업 
- [ ] #매일매일 브랜치 동기화 🔁 every day when done ⏳ [[<% tp.date.now("YYYY-MM-DD") %>]] 
	- [ ] #매일매일 update branch  🔁 every day when done ⏳ [[<% tp.date.now("YYYY-MM-DD") %>]]
	- [ ] #매일매일 resources branch  🔁 every day when done ⏳ [[<% tp.date.now("YYYY-MM-DD") %>]]
	- [ ] #매일매일 3d art branch  🔁 every day when done ⏳ [[<% tp.date.now("YYYY-MM-DD") %>]]


--------


# 오늘 추가할 일감
- [ ] #런칭 로그 작업 






# {{ Date }} 체크해야 할 일감
### 완료된 항목중 Tag #M4  일감 검색
```dataviewjs 
dv.taskList(dv.pages('#M4 and !"Template"').file.tasks.where(t => t.text.includes("M4"))) 
```


### 완료된 항목중 Tag #update  일감 검색
```dataviewjs 
dv.taskList(dv.pages('#매일매일 and "Template"').file.tasks.where(t => !t.completed))
```


### Tag #런칭  일감 검색
```dataviewjs 
dv.taskList(dv.pages('#런칭').file.tasks.where(t => t.text.includes("#런칭"))) 
```

