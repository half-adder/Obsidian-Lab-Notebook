---
cssclass: dashboard
---

>[!Experiments]+
> - # In-Progress
>
> 	  ```dataview
> 	  LIST rows.file.link FROM "lab_notebook" AND #experiment WHERE contains(status, "in-progress")
> 	  FLATTEN tags
> 	  GROUP BY tags
> 	  sort file.mtime desc
> 	  ```
>
> - # Done (Last 10)
>
>   ```dataview
>   LIST FROM "lab_notebook" AND #experiment 
>   WHERE contains(status, "done") OR contains(status, "failed")
>   sort file.name desc
>   LIMIT 10

> [!To Do Today]+
>
> ```tasks 
> (happens today) OR ((happens before today) AND (not done))
> group by filename
> short mode
> ```

>[!Week Ahead]+
>
>```tasks
> ((due before in 7 days) AND (due after today)) OR ((due before today) AND (not done))
>group by due
>group by filename
>short mode

>[!Inbox]+
> ```tasks
> not done
> path does not include templates
> no due date
> group by filename
> short mode