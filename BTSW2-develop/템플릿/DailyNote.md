


>[!todo]- Today
>```tasks
>not done
>happens {{DATE:YYYY-MM-DD}}
>sort by priority
>```
>>[!todo]- Done
>>```tasks
>>done
>>happens {{DATE:YYYY-MM-DD}}
>>group by due
>>sort by priority
>>```


















<< [[{{yesterday}}|yesterday]] || [[{{date:YYYY-MM}}|month]] || [[{{tomorrow}}|tomorrow]] >>

# {{date:dddd, MMMM Do, YYYY}}

<% tp.web.daily_quote() %>

## Agenda

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
> (due before) OR ((happens before) AND (priority is above none))
> hide recurrence rule
> sort by due date
> ```

> [!tip]- Next two weeks
> ```tasks
> not done
> happens after {{date:YYYY-MM-DD}}
> happens before {{date+14d:YYYY-MM-DD}}
> hide recurrence rule
> hide due date
> hide scheduled date
> group by happens
>