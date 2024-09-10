
<%*
  let yesterday = tp.date.now("YYYY-MM-DD", -1, tp.file.title, "YYYY-MM-DD")
  let today     = tp.date.now("YYYY-MM-DD",  0, tp.file.title, "YYYY-MM-DD")
  let tomorrow  = tp.date.now("YYYY-MM-DD",  1, tp.file.title, "YYYY-MM-DD")
%>

-------

creation date: <% tp.file.creation_date() %>
modification date: <% tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %>

--------


tags: #daily_note  #Notes #매일매일
  
# <% tp.file.creation_date() %>  
- [ ] TBU  
- [ ] TBU  
  
  
<< [[<% yesterday %>]] | [[<% tomorrow %>]] >>


---  


- [ ] 브랜치 동기화 🔁 every day when done ⏳ [[<% tp.date.now("YYYY-MM-DD", -1) %>]] 
	- [ ] update branch  🔁 every day when done ⏳ [[<% tp.date.now("YYYY-MM-DD", -1) %>]]
	- [ ] resources branch  🔁 every day when done ⏳ [[<% tp.date.now("YYYY-MM-DD", -1) %>]]
	- [ ] 3d art branch  🔁 every day when done ⏳ [[<% tp.date.now("YYYY-MM-DD", -1) %>]]



--------




# 일감 감옥  

### 오늘 만기되는 Task
```tasks
happens on or before today
(not done) OR (done after today)
group by heading
sort by description
```
  

### 오늘까지 완료되지 않은 일감검색
```tasks  
not done
hide due date
hide edit button
```



### 완료된 항목중 heading을 일감 이라고 쓴 일감 검색
```tasks
done
heading includes 일감
```



### 완료된 항목중 Tag #M4  일감 검색
```tasks
not done
tag includes <M4>

```


