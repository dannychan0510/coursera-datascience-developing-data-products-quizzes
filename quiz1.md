# Question 1
Consider the following code for the cars data set

`library(manipulate)
myPlot <- function(s) {
    plot(cars$dist - mean(cars$dist), cars$speed - mean(cars$speed))
    abline(0, s)
}`

And weights given by

`w <- c(2, 1, 3, 1)`

Give the value of μ that minimizes the least squares equation

## Solution to Question 1

```
> x <- c(0.18, -1.54, 0.42, 0.95)
> w <- c(2, 1, 3, 1)
> optimize(function(u){ sum(w*(x-u)^2)}, interval=c(-100,100))
$minimum
[1] 0.1471429

$objective
[1] 3.716543
```
