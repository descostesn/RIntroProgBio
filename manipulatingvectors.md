# Manipulating Vectors


Several functions enable to compare and manipulate vectors:


```
> vec1 <- c(1,2,3,4)
> vec2 <- c(2,3,4,5)
> vec3 <- c(1,2,5,6)
> vec4 <- c(2,4,5,5,4,1)
> vec5 <- c("A", "A", "C", "T", "G", "T")
>
> ## Verify if all the values of vec2 are higher than the values of vec1
> vec2 > vec1
> all(vec2 > vec1)
>
> ## Verify if all the values of vec3 are equal to the values of vec1
> vec1 == vec3
> all.equal(vec1, vec3)
> isTRUE(all.equal(vec1, vec3))
> all.equal(vec1, vec1)
>
> ## Get the number of elements of a vector (or a list)
> length(vec2)
```
<br>

**Exercise 14:**

  + Create a list 'list_vec' with the vectors vec1 to vec4
  + Use a for loop to print each vector
  + Modify the for loop to print from vec2 to vec4 (omitting vec1)
  + Do a 2 by 2 comparison of the equality of the vectors using a double for loop


<br>
**TIP**: If you want to compare two values, use also the isTRUE(all.equal()) form. The reason is that the way R stores floating values in memory can be tricky. Test the code below:
<br>

```
> x = seq(0,1,by=0.2)
> y = c(0.0, 0.2, 0.4, 0.6, 0.8, 1.0)
>
> x
> y
>
> x == y
> all(x == y)
> all.equal(x,y)
>
> x[4] == y[4]
> all.equal(x[4],y[4])
```

Going back to our vectors:


```
> ## Are Some Values TRUE
> vec3 > vec1
> any(vec3 > vec1)
>
> ## Are some values duplicated
> duplicated(vec4)
> anyDuplicated(vec4)
> anyDuplicated(vec5)
>
> ## Remove duplicated values
> unique(vec4)
> unique(vec5)
>
>## Make the element of a vector unique
> make.unique(vec5) 
```

R represents missing values by NA (**N**ot **A**vailable). You will very often find NA values when reading public data or your own table. The reasons for having missing values can be multiple: Lack of experimental data, error in reading functions, etc. A lot of functions in R have a parameter to handle missing values, usually it is denoted by 'na.rm' (rm = remove). Two important functions for handling NA values are **is.na** and **anyNA**:


```
> x <- NA
> y <- 10
> z <- 32
> vec6 <- c(x,y,z)
> is.na(x)
> is.na(y)
> is.na(z)
> is.na(vec6)
> anyNA(vec6)
```

**Exercise 15:**

  + Remove duplicated values from vec5 and display it in reverted order
  + Add vec6 to list_vec
  + Using a for loop, display the vector of list_vec having missing values


Very often it is necessary to find the elements of a vector satisfying a particular condition. The function which is very useful to achieve such goal is **which**:


```
> ## Find the elements of vec4 that are higher than 3
> which(vec4 > 3)
> ## Find the elements of vec4 that are higher than 3 and lower than 5
> which(vec4 > 3 & vec4 < 5)
>
> ## Find the index of the minimum and maximum of vec4
> which.min(vec4)
> which.max(vec4)
```
