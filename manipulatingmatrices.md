# Manipulating Matrices


You have already seen some functions that you can use on matrices:


```
> ## Creation of a matrix with vectors
> gene1 <- c(8,9,15)
> gene2 <- c(17,12,13)
> gene3 <- c(11,15,7)
> gene4 <- c(5,12,19)
> matrix1 <- matrix(c(gene1, gene2, gene3, gene4), nrow=4, ncol=3, byrow=T)
> matrix1
```

<br>
**Exercise 19:**

  + Define the names of the rows of matrix1 as 'gene1 to gene4' and columns as 'condition1 to condition3'
  + Print the number of rows and columns of matrix1 (one command)
  + Print the number of rows
  + Print the number of columns
  + Print the row names
  + print the col names
<br>


Below are some other useful functions:


```
> ## Retrieve the mean value of each row and columns
> rowMeans(matrix1)
> colMeans(matrix1)
>
> ## Retrieve the sum of each row and columns
> rowSums(matrix1)
> colSums(matrix1)
>
> ## Get the transpose of a matrix
> t(matrix1)
```

You can also combine matrices by rows or columns:


```
> ## Creation of a matrix with vectors
> gene5 <- c(84,4,5)
> gene6 <- c(18,22,31)
> gene7 <- c(211,115,47)
> gene8 <- c(54,112,1219)
> matrix2 <- matrix(c(gene5, gene6, gene7, gene8), nrow=4, ncol=3, byrow=T)
> matrix2
```

<br>

**Exercise 20:**

  + Combine matrix 1 and 2 by row using 'rbind'
  + Combine matrix 1 and 2 by column using 'cbind'



