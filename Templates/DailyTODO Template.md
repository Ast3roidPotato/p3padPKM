---
creation date: <% tp.file.creation_date() %>
tags: DailyNote <% tp.file.title.split('-')[0] %>
---


# <% tp.file.title %>

<< [[<% tp.date.now("YYYY-MM-DD", -1, tp.file.title, "YYYY-MM-DD") %>]] | [[<% tp.date.now("YYYY-MM-DD", 1, tp.file.title, "YYYY-MM-DD") %>]]>>

## Tasks

### CSSE230

### CSSE332

### ECE180

### ECE203

### MA222

### EP490

### Other

### Start of Day
- [ ] #task Check Gmail  📅<%tp.date.now("YYYY-MM-DD")%>
- [ ] #task Check Outlook  📅<%tp.date.now("YYYY-MM-DD")%>




#### Done Today

```tasks
done on <% tp.date.now("YYYY-MM-DD") %>
```