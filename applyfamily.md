# Apply Family


We saw in session 2 how to parse structures of data with "for" loops. As a reminder, this is how you would print the column mean values of a matrix and of a list using "for":


```
> ## Creation of a matrix
> mat <- matrix(data=1:6, nrow=2, ncol=3, byrow=T)
>
> ## Display the column mean values
> for(i in seq_len(ncol(mat))){
+ cat(mean(mat[,i]), "\n")
+ }
>
> ## Creation of a list with two elements
> mylist <- list(c(23,24,56), c(89,45,65))
>
> ## Display the mean value of each vector of the list
> for(i in seq_len(length(mylist))){ 
+ cat(mean(mylist[[i]]), "\n")
+ }
```

If you remember, I warned you that using "for" is not a good idea because of its poor computational performances. Instead, the function **apply** enables to do the same thing. It takes three main arguments: the matrix, the MARGIN and the function. MARGIN should take the value 1 if the matrix should be read by row, or the value 2 by column. The function used below is the same as in the example above: **mean**. Enter ?apply in your console to read the documentation of this function.


```
> apply(mat, MARGIN = 2, mean)
```

That much more efficient isn't it? The same thing can be done on list with the function **lapply** (apply on list, l = list). Because a list does not have 2 dimensions, the option MARGIN is not used:


```
> result <- lapply(mylist, mean)
```

Now let see what is the type of the result returned by **lapply**:


```
> result
> is(result)
> length(result)
```

"result" is a list of two elements each containing a mean value. As you would want to perform further operations on this means, you would like to transform them to a numeric vector. As you saw before you could use **unlist** or **as.numeric**:


```
> unlist(result)
> as.numeric(result)
```

A third possibility is to use **sapply** which is doing the same thing than lapply but returns a vector:


```
> result <- sapply(mylist, mean)
> result
> is(result)
```

Finally, the last example of this section shows you how to use **lapply/sapply** on more than one structure. For that, you can use **mapply** where 'm' strands for 'multiple'. You understand now why **mapply** is the multiple version of **lapply** and **sapply**. It runs apply on multiple lists or vectors:


```
> ## Creation of two lists with two elements
> mylist1 <- list(c(23,24,56), c(89,45,65))
> mylist2 <- list(c(65,12,78), c(23,79,32))
>
> ## Display the mean value of each vector of the lists
> mapply(function(x, y){
cat("The mean value of ", x, " is ", mean(x), "\n")
cat("The mean value of ", y, " is ", mean(y), "\n")
}, mylist1, mylist2)
```

<br>

**Exercise 18:**

   + Create two numeric vectors of equal size
   + Use mapply to perform a 2 by 2 sum of values
   + Could you use a more clever solution?
   