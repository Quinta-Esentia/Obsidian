[Advanced R - by Hadley Wickham: Functional programming](http://adv-r.had.co.nz/Functional-programming.html)
## Example: print head and tail of data together
```r
library(magrittr)

df %>% {
    rbind( head(., 4), tail(., 4) )
    } 
```

In this code, `{` and `}` are used to create an anonymous function block. The `.` inside the block refers to the object being passed through the `%>%` pipe (`df` in this case)

[StackedOverflow](https://stackoverflow.com/a/59757656)
[magrittr Pipe documentation](https://magrittr.tidyverse.org/reference/pipe.html) (see: *Using lambda expressions with `%>%`*)





#coding