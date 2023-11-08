---
tags:
  - prompt
creation date: <% tp.file.creation_date() %>
modification date: <% tp.file.last_modified_date("dddd, DD -  MMMM - YYYY - HH:mm:ss") %>
zettel-id: <% tp.file.creation_date("YYYYMMDD")+ "PMT" + tp.file.creation_date("HHmmss") %>
---
<% await tp.file.move("/Prompts/"+ tp.file.title) %>

# Title

## Prompt