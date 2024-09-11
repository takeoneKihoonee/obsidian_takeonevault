

-------

creation date: {{ Date }}:{{ Time }}

--------


tags: #daily_note  #Notes #매일매일
  
# {{ Date }} 오늘의 일감
- [ ] TBU  
- [ ] TBU  
  
  
---  
# 매일매일 
- [ ] #매일매일 브랜치 동기화 🔁 every day when done ⏳ [[<% tp.date.now("YYYY-MM-DD") %>]] 
	- [ ] #매일매일 update branch  🔁 every day when done ⏳ [[<% tp.date.now("YYYY-MM-DD") %>]]
	- [ ] #매일매일 resources branch  🔁 every day when done ⏳ [[<% tp.date.now("YYYY-MM-DD") %>]]
	- [ ] #매일매일 3d art branch  🔁 every day when done ⏳ [[<% tp.date.now("YYYY-MM-DD") %>]]



--------

# 일감 감옥  

### 완료된 항목중 Tag #M4  일감 검색
```dataviewjs 
dv.taskList(dv.pages('#M4').file.tasks.where(t => t.text.includes("M4"))) 
```


### 완료된 항목중 Tag #update  일감 검색
```dataviewjs 
dv.taskList(dv.pages('#매일매일').where(t => t.text.include("Daily")).file.tasks.where(t => t.text.includes("#매일매일"))) 
```



