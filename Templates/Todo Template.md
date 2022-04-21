---
creation date: <% tp.file.creation_date() %>
tags: DailyNote <% tp.file.title.split('-')[0] %>
---

modification date: <%+ tp.file.last_modified_date("dddd Do MMMM YYYY HH:mm:ss") %> // This doesn't currently work in front matter, hoping that gets fixed.

# <% tp.file.title %>

<< [[<% tp.date.now("YYYY-MM-DD", -1, tp.file.title, "YYYY-MM-DD") %>]] | [[<% tp.date.now("YYYY-MM-DD", 1, tp.file.title, "YYYY-MM-DD") %>]]>>

## Tasks

#### Over Due

```tasks
not done
due before <% tp.date.now("YYYY-MM-DD") %>
```

#### Due Today

```tasks
not done
due on <% tp.date.now("YYYY-MM-DD") %>
```

#### New Today
- [ ]

## Meeting Log

### 0000:

## Daily Log



## Daily Check List

### Start of Day

- [ ] Check Email
- [ ] Check Teams
- [ ] Check showing online
- [ ] Check Calendar - Time Block

### End of Day

- [ ] Show Offline
- [ ] Clean Unused Headings in Daily Log
- [ ] Check tomorrow's calendar

## Other Tasks

#### No Due Date

```tasks
not done
no due date
```

#### Done Today

```tasks
done on <% tp.date.now("YYYY-MM-DD") %>
```