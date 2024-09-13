
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


## 오늘의 일감

> [!todo]+ Today
> ```tasks
> not done
> happens today
> hide recurrence rule
> hide due date
> hide scheduled date
> sort by priority
> ```

> [!danger]+ Overdue 
> ```tasks
> not done
> happens after yesterday) AND (priority is above none)
> (tags include #M4) OR (tags include #M5)
> sort by due date
> ```

> [!tip]- Next two weeks
> ```tasks
> not done
> (happens after yesterday) AND (happens before in two weeks)
> hide recurrence rule
> hide due date
> no scheduled date









# {{ Date }} 체크해야 할 일감
### 미 완료된 항목중 Tag #M4  일감 검색
```dataviewjs 
dv.taskList(dv.pages('#M4 and -"Template"').file.tasks.where(t => t.text.includes("M4")).where(t => !t.completed) )
```
-------------------

###  Tag #update  일감 검색
```dataviewjs 
dv.taskList(dv.pages('-"Template"').file.tasks.where(t => t.text.includes("#update")))
```

-------------
### Tag #런칭  일감 검색
```dataviewjs 
dv.taskList(dv.pages('-"Templete"').file.tasks.where(t => t.text.includes("#런칭"))) 
```

--------------------------------