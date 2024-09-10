
---  
created: {{date}} {{time}}  
---  
tags: #daily_note  #Notes #매일매일
  
# {{date}}  
- [ ] TBU  
- [ ] TBU  
  
  
[[{{yesterday}}|< yesterday]] | [[{{tomorrow}}|tomorrow >]]  
  
---  
# 일감 감옥  

### 오늘 만기되는 Task

```tasks
not done
due on <% tp.date.now("YYYY-MM-DD") %>
```


## 오늘까지 완료되지 않은 일감검색
```tasks  
not done
hide due date
hide edit button
```



## 완료된 항목중 heading을 일감 이라고 쓴 일감 검색
```tasks
done
heading includes 일감
```

