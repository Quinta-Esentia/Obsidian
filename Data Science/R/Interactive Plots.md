
## Simple Example
From [stackoverflow](https://stackoverflow.com/questions/34580095/using-r-and-plot-ly-how-do-i-script-saving-my-output-as-a-webpage)
```r
library(plotly)
set.seed(100)
d <- diamonds[sample(nrow(diamonds), 1000), ]
p <- plot_ly(d, x = ~carat, y = ~price, text=~paste("Clarity : ", clarity))
htmlwidgets::saveWidget(as_widget(p), "index.html")
```

# Resources
1. [Plotly: Saving and embedding HTML](https://plotly-r.com/saving)
2. [Crosstalk](https://rstudio.github.io/crosstalk/)
3. 