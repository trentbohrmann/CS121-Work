Day 03 Deliverable
===============================================


```r
background <- function(min = 0, max = 100) {
    plot(0, ylim = c(0, 100), xlim = c(0, 100), type = "n", xaxt = "n", yaxt = "n", 
        xlab = "", ylab = "", bty = "n", asp = 1)
}
```

 so: background(0,100)
 

```r
circle <- function(x, y, r, ...) {
    angs <- seq(0, 2 * pi, length = 100)
    xpts <- x + r * cos(angs)
    ypts <- y + r * sin(angs)
    polygon(xpts, ypts, ...)
}
```


then: 
      polygon(x=c(15,48,63),y=c(20,60,44),col="yellow", border= "yellow")
              &
      polygon(x=c(10,10,20,20), y=c(10,20,20,10), col="light blue", border="blue")
              &
      circle(66,20,25,color="green",border="green")
              &
      circle(30,70,30, col="orange", border="orange")
              &
      circle(100,100,20, col="purple")
              &
      polygon(x=c(50,50,90,90),y=c(70,90,90,70), col="blue", border="blue")
              et cetera...
      
      

```r
background(0, 100)
polygon(x = c(15, 48, 63), y = c(20, 60, 44), col = "yellow", border = "yellow")
polygon(x = c(10, 10, 25, 25), y = c(10, 25, 25, 10), col = "light blue", border = "blue", 
    lwd = 4)
circle(66, 20, 25, col = "green", border = "green")
circle(30, 70, 30, col = "orange", border = "red", lwd = 1)
circle(100, 100, 20, col = "purple")
polygon(x = c(, 0, 50, 90, 90), y = c(70, 90, 90, 70), col = "blue", border = "blue")
```

```
## Error: argument 1 is empty
```

```r
polygon(x = c(72, 90, 110, 90), y = c(2, 15, 18, -12), col = "red", border = "red")
```

![plot of chunk unnamed-chunk-3](figure/unnamed-chunk-3.png) 

