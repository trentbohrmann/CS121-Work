Day08- reverser and such patterns
========================================================

# Reverser

```r
Reverser <- function(x) {
    reverse <- strsplit(x, "")[[1]]
    reverse2 <- reverse[rev(1:nchar(x))]
    paste(reverse2, collapse = "")
}
```



```r
Reverser("racecar")
```

```
## [1] "racecar"
```

```r
Reverser("trent")
```

```
## [1] "tnert"
```


# Scrambler

```r
Scrambler <- function(x) {
    scram <- strsplit(x, "")[[1]]
    scram2 <- scram[sample(1:nchar(x))]
    paste(scram2, collapse = "")
}
```



```r
Scrambler("ohmygosh")
```

```
## [1] "ohghysom"
```


#  VowelBleeper

```r
VowelBleeper <- function(word) {
    gsub("[aeiouAEIOU]", "*", word)
}
```



```r
VowelBleeper("refridgerator")
```

```
## [1] "r*fr*dg*r*t*r"
```


# L33t

```r
L33t <- function(x) {
    v <- gsub("[Ee]", "3", x)
    w <- gsub("[Oo]", "0", v)
    y <- gsub("[Ss]", "5", w)
    gsub("[Gg]", "9", y)
}
```



```r
L33t("soccer goal")
```

```
## [1] "50cc3r 90al"
```


# Cypher

```r
cypher <- function(input) {
    cypher <- chartr("abcdefghijklmnopqrstuvwxyz", "mnopqrstuvwxyzabcdefghijkl", 
        input)
    return(cypher)
}
```



```r
cypher("programming")
```

```
## [1] "bdasdmyyuzs"
```

