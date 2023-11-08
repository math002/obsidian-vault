---
tags:
  - note
  - obsidian
  - plug-in
creation date: 2023-09-15 13:35
category: Technology 🖥️
trap-system: Topic
moc: "[[Notes]]"
modification date: Friday, 15 -  September - 2023 - 13:35:18
---




# Using Templater to automatically rename and move a file.

## Steps:

1. First, install Templater from the community plugin page.

![Templater](https://imgur.com/nQ5nohc.png)

2. Create a template and in the settings for templates, set the folder where you will create your templates.

    - Example of your Templates Folder.

	![Templates Folder](https://imgur.com/qAehqEe.png)
    
    - Setting the right folder in the Templates settings
 
	![Templater-Settings](https://imgur.com/esDSK0z.png)

---
3. You need to also set it in Templater 

![Setting Templater](https://imgur.com/r1pTmD5.png)


5. Then, here is the tricky part, in the template you create you have to use the Templater unique source code style.

    - Code Examples
    ![Source Code](https://imgur.com/BROKRsE.png)


### Notes

1. As you can see, the source code always starts with `<%` and finishes with `%>` for this example I first set the file new path with the built-in key word `file.move`, it will automatically make the document created by the Templates setting go to `/Journals/` folder I set, for this example, I kept the file with the same name on this line, using the key word `file.title`, but if you need to change it right away, use a string like `<% await tp.file.move("/Your Folder/" + "file_name.md")%>`, as an example. 
2. I did it this way because I want to rename my file on the next line, though. let's break it down, the line is.
     - `<% await tp.file.rename(tp.file.creation_date("YYYY_MM_DD")+ "_journal") %>`
     - For the first part I use the built-in function `file.creation_date`, it generates a string on the chosen format `YYYY_MM_DD` to generate a string of the file's creation date. Then I concatenate it with the string `"_journal"` to complete the name
3. **Result:**
      - My Journals Folder:
       ![Journals](https://imgur.com/Ox20l5X.png)
       
4.  For further enhancement:
     - I also created a file using Dataview and Buttons to automatically create a file using said template.
     - Here is the page:
     ![Journal Page](https://imgur.com/2AGBX3Y.png)
     
5. **Journals main page source codes:**
     - For the dataview:
```
	```dataview
	LIST rows.file.link
	FROM #journal AND -#hub
	WHERE file.ctime.year = 2023 AND file.name != "Journal Template"
	GROUP BY dateformat(file.ctime, "MMMM"+ " 'de" + "' yyyy") AS MON
	SORT MON ASC
	```
```

   - For the Button:
```
	```button
	name Create Journal
	type command
	action Templater: Create new note from template
	class grad_button btn_green tiny
	```
	^journal-button
```

6. When clicking this button it will automatically open the Templater command in command palette and you will choose the template you just created:
	![Templater Command](https://imgur.com/9C0N5ef.png)

7. Select the template and it should create automatically create the new file where you want and with the name you want. That's just an example based on my configurations, any doubt feel free to ask and feel free to modify it to better fit your needs.
