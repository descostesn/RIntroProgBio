# Exercise 1:

```
## Enter a number
42
## Enter a decimal number
42.1
##Perform addition
39 + 3
## Perform subtraction
58 - 16
## Perform multiplication
6 * 7
## Perform division
8 / 3
## Compute the remainder (modulo: 10 = (3x3) + 1)
10 %% 3
## Use power
5^3
## Combine operators
((10 + 15) / 5) - 3*2
```

# Exercise 2

```
## Change the value of 'a'
a <- 8
# Display the value of 'a'
a
## Perform an addition and use the result in a division
a <- 3 + 5
b <- a/4
## What is now the value of b?
b
```

# Exercise 3

```
## Using double quotes works too
a <- "b"
a
## Give 'a' a sentence
a <- 'Hello World'
a
## What is happening if you use a quote inside a sentence?
test <- 'it's a R workshop'
```

# Exercise 4

```
## Let's use variables to combine vectors
vector1 <- c(1,2,3)
vector2 <- c(8,9,10)
vector3 <- c(vector1, vector2)
vector3

## Create a vector with values from 11 to 25
vector1 <- 11:25
vector1
## Access the first element
vector1[1]
# Modify the 5th element
vector1[5] <- 100
vector1
```

# Exercise 5

```
##  Create 4 vectors 'gene1', 'gene2', 'gene3',	'gene4'	each containing 3 numeric values of expression
gene1 <- c(8,9,15)
gene2 <- c(17,12,13)
gene3 <- c(11,15,7)
gene4 <- c(5,12,19)

## Combine the	vectors	with 'c' and create a matrix 'matrix1' with each line containing a gene
matrix1 <- matrix(c(gene1, gene2, gene3, gene4), nrow=4, ncol=3, byrow=T)
matrix1

## Define the names of rows and columns
rownames(matrix1) <- c("gene1","gene2", "gene3", "gene4")
colnames(matrix1) <- c("condition1", "condition2", "condition3")
matrix1

```

# Exercise 6:

```
> ## Access the values of gene 1 and 2 in the third condition using row and column names
> matrix1[c("gene1", "gene2"), "condition3"]
> ## Now same thing using numbers (called indexes)
> matrix1[1:2,3]
```
