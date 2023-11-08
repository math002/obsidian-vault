---
type: MOC
banner: "![[prompt engineering banner.jpeg]]"
banner_y: 0.32
tags: "#moc #prompt"
---
# Prompts

```dataview
LIST rows.file.link
FROM #prompt AND -#hub
WHERE file.name != "Prompt Template"
GROUP BY dateformat(file.ctime, "MMMM"+ " 'de" + "' yyyy") AS MON
SORT MON ASC
```

`button-prompt`

>[!important]+ Real MOC
> - [[Shyleen]]
> - [[Grin Dark RPG]]