# Question 1
Consider the following code for the cars data set

```
library(manipulate)
myPlot <- function(s) {
    plot(cars$dist - mean(cars$dist), cars$speed - mean(cars$speed))
    abline(0, s)
}
```

This function plots distance versus speed, each de-meaned and an associated line of slope s. Which of the following code will make a manipulate plot that creates a slider for the slope?

## Solution to Question 1

```
manipulate(myPlot(s), s = slider(0, 2, step = 0.1))
```

# Question 2
Which of the following code uses the `rCharts` package to create a sortable and searchable data table for the `airquality` data set? Assume the `rCharts` package and the `airquality` data set have already been loaded into R.

## Solution to Question 2
```
# Installing rCharts package
install.packages("devtools")
install.packages("Rcpp")
library(devtools)
library(Rcpp)
install_github('ramnathv/rCharts')

# Loading relevant libraries for this question
library("rCharts")

# Answer to the question
dTable(airquality, sPaginationType = "full_numbers")
```


