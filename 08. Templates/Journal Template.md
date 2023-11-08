---
tags:
  - journal
creation date: <% tp.file.creation_date() %>
modification date: <% tp.file.last_modified_date("dddd, DD -  MMMM - YYYY - HH:mm:ss") %>
---

<% await tp.file.move("/03. Journals/"+ tp.file.title) %>
<% await tp.file.rename(tp.file.creation_date("YYYY_MM_DD")+ "_journal") %>


# Journal Date: <font color="green"><%tp.date.now("YYYY_MM_DD")%></font>

---
>[!column| left wsmall no-i c-p-sm]  ## Questions and Doubts
>>[!question| c-p-sm]-

>[!column| no-i] ## Projects, subjects and Ideas
> ## Ideas:
> ## Experiences
> ## People
> ## Readings/Media
> ## Activities
---
>[!column| c-p-sm no-i]+ &nbsp;
> ## Summary
