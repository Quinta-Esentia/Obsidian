# Example kibble

```r
kbl(df_table, # data to output as table
    booktabs = T, # makes it pretty
    # position = "h!", # weak position hold
    col.names = df_long_names # custom column names
    ) %>% kable_styling(latex_options = c("striped", "scale_down", "HOLD_position"))
```

```r
kbl(df_table, # data to output as table
    booktabs = T, # makes it pretty
    # position = "h!",  # weak position hold
    col.names = df_long_names  # custom column names
    ) %>% 
  kable_styling(
      latex_options = c(
        "striped", 
        "scale_down", # fit onto pdf page
        "HOLD_position" # 
        )
      )
```
# Table Gets Cut Off When Knitting to PDF
[Question Source](https://stackoverflow.com/questions/70815981/table-gets-cut-off-when-knitting-to-pdf)
[Solution Source](https://haozhu233.github.io/kableExtra/awesome_table_in_pdf.pdf)

Solution
```r
library(knitr) # for kable() table
library(kableExtra) # for kable_styling, kbl
df_table %>% kbl() %>% kable_styling(latex_options = c("scale_down"))
```


# Kable forces my table above my text in R
[Question Source](https://stackoverflow.com/questions/53153537/rmarkdown-setting-the-position-of-kable)
[Answer Source]()

```r
df_table %>% kbl() %>% kable_styling(latex_options = c("HOLD_position"))
```

# Wrap column name in pdf table, from knitr::kable
[Question Source](https://forum.posit.co/t/wrap-column-name-in-pdf-table-from-knitr-kable/3278)
[Answer Source](http://haozhu233.github.io/kableExtra/best_practice_for_newline_in_latex_table.pdf)

Solution
```r
dt %>% # table with long column names
	kable("latex", booktabs = T)) %>%
	column_spec(2:3, width = "5cm") # fix column width
```