# My Psychopy Debug Experiences

## JS cannot compile (20230604)
- the deepest error says: 
```
File "...\psychopy3\versions\psychopy\data\utils.py", line 357, in importConditions  
    ws = wb.worksheets[0]  
IndexError: list index out of range
```

- The problem was that two of the control files were in .csv format and I re-saved them into .xlsx format. 
- I found the solution with respect to [this thread](https://stackoverflow.com/questions/62800822/openpyxl-cannot-read-strict-open-xml-spreadsheet-format-userwarning-file-conta). By re-saving the .csv file into .xls in MS Excel and then re-save the .xls file into .xlsx format will solve the problem. 
