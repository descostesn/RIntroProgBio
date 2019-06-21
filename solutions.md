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

# Exercise 7:

```
## Create the list in one command (without intermediate variables)
chd8Info <- list(Name = "CHD8",
 Description = c("Chromodomain Helicase DNA Binding Protein",
 "Helicase With SNF2 Domain", "ATP-Dependent Helicase CHD8", "HELSNF1",
 "Chromodomain-Helicase-DNA-Binding Protein", "Axis Duplication Inhibitor"),
 Database = data.frame(database = c("HGNC", "Entrez_Gene", "Ensembl", "OMIM"),
 number = c(20153, 57680, 00000100888, 610528)))
chd8Info

## Display the gene name of chd8Info.
chd8Info[[1]]
chd8Info$Name

## Display the second alias (Description) of Chd8.
chd8Info[[2]][2]
chd8Info$Description[2]

##Display the third and fifth alias (Description) of Chd8.
chd8Info[[2]][c(3,5)]
chd8Info$Description[c(3,5)] 

## Retrieve the Entrez gene ID of CHD8.
chd8Info[[3]][2,]
chd8Info$Database[2,]
```

# Exercise 8:

```
## Check if gene1 expression is greater than gene2 expression
gene1 > gene2
## Check if gene1 expression is less than or equal to 5
gene1 <= 5
## Check if gene2 expression is greater than or equal to 20
gene2 >= 20
## Check if gene2 expression is equal to 16
gene2 == 16
## Check if gene1 expression is different than 5
gene1 != 5
```

# Exercise 9:

```
TRUE && FALSE
FALSE && FALSE
TRUE || FALSE
FALSE || FALSE
!FALSE
!FALSE || FALSE
(TRUE || FALSE) && (TRUE && FALSE)

x <- 5
y <- 6
(x > 5 && y > 5) || (x == y)

mutation1 <- "Tyr1"
mutation2 <- "Ser5"
organism1 <- "yeast"
organism2  <- "mammals"
mutation1 == "Ser5"
organism2 != "mammals"
mutation2 == "Ser5" && organism2 == "mammals"
```

# Exercise 10:

```
if(current_sample == "B-cell"){
       print(expression_values[["CD19"]])
}
```

# Exercise 11:

```
iris
head(iris)

output <- character(nrow(iris))

for(i in c(1:nrow(iris))){
	
  if(iris$Sepal.Length[i] > 5){
	
	output[i] <- "greater than 5"
	
  }else{		
	output[i] <- "lesser than 5"		
  }	
}
```

# Exercise 12:

```
x <- 2.849
## Round number to upper or lower integer
ceiling(x)
floor(x)

## Round including digits
round(x, digits=1)
## Compute natural, base 2 and base 10 logarithms
x <- 5
log(x)
log2(x)
log10(x)
## Find the square root of 9
x <- 9
sqrt(x)
```

# Exercise 13:

```
## Extract the minimum and maximum values
min(randomvec1)
max(randomvec1)

## Compute the cumulative sum of the vector
vec1 <- c(1,2,3,4,5)
result_cumsum <- cumsum(vec1)
result_cumsum


## Compute the cumulative sum of the vector vec1 <- c(1,2,3,4,5)
vec1 <- c(1,2,3,4,5)
result_cumsum <- cumsum(vec1)
result_cumsum

## Create a vector of 10 random values between 1 and 1000000
randomvec2 <- sample(1:1000000, 10)
randomvec2
## sort the values
sort(randomvec2)
## Retrieve the indexes for sorting the values
order(randomvec2)
randomvec2[order(randomvec2)]

## Generate values from 1 to 10 by 2
seq(from = 1, to = 10, by = 2)
## Generate values from 1 to 10
seq(from = 1, to = 10)
vector_10 <- seq_len(10)

## Repeat the number 5 ten times
rep(5, 10)

## Reverse elements
rev(vector_10)

## Compute the sum of all values from 1 to 10
sum(vector_10)

## Compute the mean of all values
mean(vector_10)

## Summarize all values (min, max, etc)
summary(randomvec1)
```

# Exercise 14:

```
## Create a list 'list_vec' with the vectors vec1 to vec4
vec1 <- c(1,2,3,4)
vec2 <- c(2,3,4,5)
vec3 <- c(1,2,5,6)
vec4 <- c(2,4,5,5,4,1)
list_vec <- list(vec1, vec2, vec3, vec4)

## Use a for loop to print each vector
for(i in seq_len(length(list_vec))) print(list_vec[[i]])

## Modify the for loop to print from vec2 to vec4 (omitting vec1)
for(i in 2:length(list_vec) ) print(list_vec[[i]])

## Do a 2 by 2 comparison of the equality of the vectors using a double for loop
for(i in seq_len(length(list_vec)-1))
  for(j in 2:length(list_vec))
    print(isTRUE(all.equal(list_vec[[i]], list_vec[[j]])))
```

#  Exercise 15:

```
## Remove duplicated values from vec5 and display it in reverted order
rev(vec5[-duplicated(vec5)])

## Add vec6 to list_vec
x <- NA
y <- 10
z <- 32
vec6 <- c(x,y,z)
list_vec[[5]] <- vec6

## Using a for loop, display the vector of list_vec having missing values
for(i in seq_len(length(list_vec)))
 if(anyNA(list_vec[[i]]))
 print(list_vec[i])
```


# Exercise 16:

```
## Define the names of rows and columns
rownames(matrix1) <- c("gene1","gene2", "gene3", "gene4")
colnames(matrix1) <- c("condition1", "condition2", "condition3")
matrix1

## Print the number of	rows and columns of matrix1 (one command)
dim(matrix1)

## Print the number of	rows
nrow(matrix1)

## Print the number of	columns
ncol(matrix1)

## Print the row names
rownames(matrix1)

## print the col names
colnames(matrix1)
```

# Exercise 17:

```
## Combine matrix 1 and 2 by row
rbind(matrix1, matrix2)

## Combine matrix 1 and 2 by column
cbind(matrix1, matrix2)
```


# Exercise 18:

```
## Create two numeric vectors
vec1 <- c(1,2,3,4)
vec2 <- c(5,6,7,8)

## Use mapply to perform a 2 by 2 sum of values
mapply(function(x,y) return(x+y), vec1, vec2)

## A more clever solution is to use vectorisation
vec1 + vec2
```
