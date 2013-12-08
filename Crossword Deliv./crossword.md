Crossword Deliverable
===================================

```r
words <- readLines(url("http://dtkaplan.github.io/ScientificComputing/Syllabus/Daily/Day-07/word_list_moby_crossword-flat/word_list_moby_crossword.flat.txt"))

head(words)
```

```
## [1] "aa"     "aah"    "aahed"  "aahing" "aahs"   "aal"
```

```r


determineWords <- function(a) {
    return(length(words[grep(a, words)]))
}

"Number of words of length 1,2, etc."
```

```
## [1] "Number of words of length 1,2, etc."
```

```r

determineWords("^.$")
```

```
## [1] 0
```

```r

determineWords("^..$")
```

```
## [1] 85
```

```r


"Number of words that start with a, b, etc."
```

```
## [1] "Number of words that start with a, b, etc."
```

```r

determineWords("^a")
```

```
## [1] 6557
```

```r

determineWords("^b")
```

```
## [1] 6848
```

```r

determineWords("^x")
```

```
## [1] 82
```

```r

"Words that have q but not a u following it"
```

```
## [1] "Words that have q but not a u following it"
```

```r

determineWords("q[^u]")
```

```
## Warning: closing unused connection 5
## (http://dtkaplan.github.io/ScientificComputing/Syllabus/Daily/Day-07/word_list_moby_crossword-flat/word_list_moby_crossword.flat.txt)
```

```
## [1] 14
```


# Crossword Helper


```r

crossword <- function(pattern) {
    matched <- grep(pattern, words)
    return((words)[matched])
}


crossword("alibi")
```

```
## [1] "alibi"    "alibied"  "alibies"  "alibiing" "alibis"
```




# Better Crossword


```r

betterCrossword <- function(v, numchar) {
    cross <- rep(".", numchar)
    cross[v] <- names(v)
    down <- paste("^", paste(cross, collapse = ""), "$", sep = "")
    result <- grep(down, words)
    return(words[result])
}

betterCrossword(c(s = 1, t = 2))
```

```
## character(0)
```



