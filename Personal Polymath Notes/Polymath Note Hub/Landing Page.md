___
**Tasks**
```tasks
not done
path includes Polymath Note Hub
sort by due
```

___
**Most Recent Notes**
```dataview
TABLE NoteType, NoteTags, NoteCreation
FROM "Polymath Note Hub/Notes"
SORT file.ctime
LIMIT 3
```
___
![[Learning Board]]
___
![[Projects]]
___
**Annotations**
```dataview
TABLE NoteType, NoteTags, NoteCreation
FROM "Polymath Note Hub/Notes"
WHERE NoteType = "Annotations"
SORT file.ctime
LIMIT 3
```

---
**Theory**
```dataview
TABLE NoteType, NoteTags, NoteCreation
FROM "Polymath Note Hub/Notes"
WHERE NoteType = "Theory"
SORT file.ctime
LIMIT 3
```
---
**Practice**
```dataview
TABLE NoteType, NoteTags, NoteCreation
FROM "Polymath Note Hub/Notes"
WHERE NoteType = "Practice"
SORT file.ctime
LIMIT 3
```
___
**Periodic Notes**
```dataview
TABLE NoteType, NoteTags, NoteCreation
FROM "Polymath Note Hub/Notes"
WHERE NoteType = "Daily Notes" OR "Weekly Notes" OR "Monthly Notes" OR "Quarterly Notes" OR "Yearly Notes"
SORT file.ctime
LIMIT 3
```
