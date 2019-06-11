# Matrices


  So far we have worked in only one dimension. Matrices are tables with two dimensions: It contains rows and columns:


![Matrix with rows, horizontal, and columns, vertical \label{figure=4}](matrix.png)

**IMPORTANT**: Matrices can contain only **one** type of element: numeric or character (you will see the boolean later.. oops, a new word here :). All lines should have the same number of elements!

Below is how to create matrices:


```
> ## Creation of a matrix mat
> mat <- matrix(nrow=2, ncol=3)
> mat
> ## Creation of the matrix mat with values
> mat <- matrix(data=1:6, nrow=2, ncol=3, byrow=T)
> mat
> ## Creation of a matrix with vectors
> gene1 <- c(8,9,15)
> gene2 <- c(17,12,13)
> gene3 <- c(11,15,7)
> gene4 <- c(5,12,19)
> matrix1 <- matrix(c(gene1, gene2, gene3, gene4), nrow=4, ncol=3, byrow=T)
> matrix1
> ## Define the names of rows and columns
> rownames(matrix1) <- c("gene1","gene2", "gene3", "gene4")
> colnames(matrix1) <- c("condition1", "condition2", "condition3")
> matrix1
```

BAM! You have a matrix of gene expression in different conditions! Now is how to access and modify it:


```
> ## Access the expression value of gene2 in the third conditon (second row, 
> ## third column)
> matrix1[2,3]
> ## Modify the expression value of gene 3 in the second condition
> matrix1[3,2] <- 154
> matrix1
> ## You can also access the expression value using names!
> matrix1["gene3", "condition1"]
```

Powerful isn't it? Almost ready to perform your differential expression analysis!


```
> ## Access the values of gene 1 and 2 in the third condition
> matrix1[c("gene1", "gene2"), "condition3"]
> ## Now same thing using numbers (called indexes)
> matrix1[1:2,3]
```
