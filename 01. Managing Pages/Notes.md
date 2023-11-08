---
tags: "#moc #notes"
type: MOC
banner: "![[zettel banner.png]]"
banner_y: 0.204
banner_lock: True
---
# Notes:

## MOC by Category

```dataview
LIST rows.file.link
FROM #note AND -#hub
WHERE file.name != "Notes Template"
GROUP BY category AS CAT
SORT CAT DESC
```

## MOC by PKM

```dataview
LIST rows.file.link
FROM #note AND -#hub
WHERE file.name != "Notes Template"
SORT file.name ASC
GROUP BY trap-system AS TRAP
SORT TRAP DESC
```
`button-note`

>[!important]+ Actual MOC
> - Technology 🖥️:
>     - [[How to Templater]]
> - Self-Improvement 🌱:
>     - [[What Do I Know About Me]]
> - Sexuality 🌶️:
>     - [[What turns me on]]
>     - [[Intimacy]]
> - Communication 💬:
>     - [[Let Be Inspired]]
> - Personal and Emotions 💜:
> 	- [[Physical World - Magick Relationship]]
