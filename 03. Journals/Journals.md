---
tags: #moc
type: MOC
banner: "![[journal-banner.png]]"
banner_x: 0.48041
banner_lock: true
---

# Journals 

```dataview
LIST rows.file.link
FROM #journal AND -#hub
WHERE file.ctime.year = 2023 AND file.name != "Journal Template"
GROUP BY dateformat(file.ctime, "MMMM"+ " 'de" + "' yyyy") AS MON
SORT MON ASC
```

`button-journal`


>[!important]- Actual MOC - #moc
> - setembro de 2023:
>      - [[2023_09_13_journal]] 
>      - [[2023_09_14_journal]]
>      - [[2023_09_15_journal]]
>      - [[2023_09_16_journal]]
>      - [[2023_09_17_journal]]
>      - [[2023_09_18_journal]]
>  - outubro de 2023:
>	- [[2023_10_21_journal]] 
>  - novembro de 2023:
> 	- [[2023_11_04_journal]]
> 	- [[2023_11_05_journal]]