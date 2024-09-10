

-------

creation date: {{ Date }}:{{ Time }}

--------


tags: #daily_note  #Notes #매일매일
  
# {{Created Date}} 
- [ ] TBU  
- [ ] TBU  
  
  
<< yesterday | tomorrow >>


---  
# 매일매일 

- [ ] 브랜치 동기화 🔁 every day when done ⏳ [[<% tp.date.now("YYYY-MM-DD") %>]] 
	- [ ] update branch  🔁 every day when done ⏳ [[<% tp.date.now("YYYY-MM-DD", -1) %>]]
	- [ ] resources branch  🔁 every day when done ⏳ [[<% tp.date.now("YYYY-MM-DD", -1) %>]]
	- [ ] 3d art branch  🔁 every day when done ⏳ [[<% tp.date.now("YYYY-MM-DD", -1) %>]]



--------

# 일감 감옥  

### 완료된 항목중 Tag #M4  일감 검색

```dataviewjs 
dv.taskList(dv.pages('#M4').file.tasks.where(t => !t.completed)) 
```


