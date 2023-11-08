---

type: MOC
tags: "#books #moc"
---

# My Books:
---
```dataviewjs

const Book1 = {
	title: "Filhos da Degradação",
	author: "Felipe Castilho",
	genre: "Fantasy",
	year: 2017,
	pagesRead: 15,
	pages: 	440
}
const Book2 = {
	title: "A Lenda de Ruff Ghanor 3",
	author: "Leonel Caldela",
	genre: "Fantasy",
	year: 2018,
	pagesRead: 0,
	pages: 	634
}
const Book3 = {
	title: "Bruxa Natural",
	author: "Arin Murphy-Hisgock",
	genre: "Witchcraft",
	year: 2021,
	pagesRead: 242,
	pages: 	242
}

function progress(Book) {
	let value;
	value = (Book.pagesRead * 100) / Book.pages
	return ` <progress value="${parseInt(value)}" max="100"></progress> | ${parseInt(value)} %`
}

dv.span(`
>[!table|wtall]
>| **Book Title** | **Author**  | **Genre** | **Year** | **Read Pages** | **Pages** | **Progress** | **Percentage**
>| :--- | :--- | :--- | :--- | :--- | :--- |:--- |:---:|
>| ${Book1.title} | ${Book1.author} | ${Book1.genre} | ${Book1.year} | ${Book1.pagesRead} | ${Book1.pages}  | ${progress(Book1)}
>| ${Book2.title} | ${Book2.author} | ${Book2.genre} | ${Book2.year} | ${Book2.pagesRead} | ${Book2.pages}  | ${progress(Book2)}
>| ${Book3.title} | ${Book3.author} | ${Book3.genre} | ${Book3.year} | ${Book3.pagesRead} | ${Book3.pages}  | ${progress(Book3)}
`)

```
