Day 05
========================================================

# Outlier

```r
outlier <- function(x) {
    x <- c(0:9)
    outlier <- quantile(x, probs = seq(0.25, 0.75), na.rm = FALSE, names = TRUE, 
        type = 7)
    return(outlier)
}
```


# Numbers and Languages

```r
digitToWord <- function(number, word) {
    dtw <- word[number]
    return(dtw)
}
digitToWord(c(9, 8, 7, 6, 5, 4, 3, 2, 1), c("one", "two", "three", "four", "five", 
    "six", "seven", "eight", "nine"))
```

```
## [1] "nine"  "eight" "seven" "six"   "five"  "four"  "three" "two"   "one"
```


# Crossword Puzzle Help

```r
lettersMatch <- function(words, pattern) {
    small <- c("case", "second", "third", "are")
    match <- grepl("^...$", small)
    return(match)
}
```



```r
lettersMatch("base", 3)
```

```
## [1] FALSE FALSE FALSE  TRUE
```


# Series with Pi

```r
piSeries <- function(n) {
    n <- c(1:n)
    pi <- (4 * sum(((-1)^(n - 1))/(2 * (n - 1) + 1)))
    return(pi)
}
```



```r
piSeries(123456)
```

```
## [1] 3.142
```


# How Close to Pi

```r
howCloseToPi <- function(n) {
    n <- c(1:n)
    pi <- (4 * cumsum(((-1)^(n - 1))/(2 * (n - 1) + 1)))
    plot(n, pi)
    return(pi)
}
```



```r
howCloseToPi(4)
```

![plot of chunk unnamed-chunk-8](figure/unnamed-chunk-8.png) 

```
## [1] 4.000 2.667 3.467 2.895
```

