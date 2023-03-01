# Obsidian Tutorial
## Basic note taking
[[Not-work-stuff]]


[https://help.obsidian.md/How+to/Basic+note+taking]

A thing   
	- another thing   
		- a third thing  
			- all the way down  
		- and back again  

## Internal links
https://help.obsidian.md/How+to/Internal+link

## How to #format your notes

https://help.obsidian.md/How+to/Format+your+notes 

Task List
- [x] ==item1== 
- [ ]  `x = item 2`
- [ ] 

Table 

First Column | Second | Third
----------|----------|--------
content for cell 1 | [[Not-work-stuff#I also like Nujabes\|Nujabes is cool]] | cell 33


Use colon | to justify tables
:----------|---------:
cell 1 | cell 2
cell 3 | cell 4



# Code chunks
1. You can put code inline with text using backtics, such as `import pandas as pd` this example. 
2. You can tab in twice (8 spaces) to create a code block:
 
		import pandas as pd      
        df = read_csv("file.csv")
3. You can use tripple backtics and define the language used. This is the best method and supports R, Python, and SQL syntax highlighting
```R
library(tidyverse)
df <- read_csv('file')
df %>% count(Column1)
x <- 100
```

```python
import pandas as pd
df = read_csv('file')
x = 100
```

```sql
SELECT * 
FROM TABLE 
WHERE COLUMN1 == 'value'	
```


# Look into zotero
