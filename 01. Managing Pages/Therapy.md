---
tags: "#moc #therapy "
type: moc
date: 07/11/2023
banner: "![[therapy banner.webp]]"
banner_y: 0.096
banner_lock: true
---


# Therapy MOC

```dataview
TABLE
dateformat(file.ctime, "MMMM"+ " 'de" + "' yyyy") AS "Date",
mood as "Mood",
objetives-accomplished as "Accomplished"
FROM #therapy
WHERE file.name != "Therapy" AND file.name != "Homepage"
```

>[!note]- Actual MOC
> - Novembro de 2023
> 	- [[Psychologist Session 2023_11_07]]