Final
==========================

```r
require(mosaic)
```

```
## Loading required package: mosaic Loading required package: grid Loading
## required package: lattice
## 
## Attaching package: 'mosaic'
## 
## The following objects are masked from 'package:stats':
## 
## D, IQR, binom.test, cor, cov, fivenum, median, prop.test, sd, t.test, var
## 
## The following object is masked from 'package:base':
## 
## max, mean, min, print, prod, range, sample, sum
```

```r
require(plyr)
```

```
## Loading required package: plyr
## 
## Attaching package: 'plyr'
## 
## The following object is masked from 'package:mosaic':
## 
## count
```

```r
fetchData("COMP121/word-hints.R")
```

```
## Retrieving from http://www.mosaic-web.org/go/datasets/COMP121/word-hints.R
```

```
## [1] TRUE
```



```r
letterProportion <- function(x) {
    return(as.data.frame(sort(table(strsplit(x, "")), decreasing = TRUE)))
}
```


# This One Works!!

```r
letterProportionBeta <- function(x) {
    first <- (as.data.frame(sort(table(strsplit(x, "")), decreasing = TRUE)))
    second <- (nchar(x))
    return(first/second)
}

```

```r
letterProportionBeta("HelloWorld")
```

```
##   sort(table(strsplit(x, "")), decreasing = TRUE)
## l                                             0.3
## o                                             0.2
## H                                             0.1
## W                                             0.1
## d                                             0.1
## e                                             0.1
## r                                             0.1
```





```r
freqCompare <- function(x) {
    table <- letterProportionBeta(x)
    table2 <- table(English)
    return(mutate(table, LANG = table2))
}

```




```r
whichLanguage <- function(x) {
    table <- freqCompare(x)
    table2 <- sort(table(X^2), decreasing = TRUE)
    return(table2)
}
```
