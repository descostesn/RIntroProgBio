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
## Find the indexes of 'A' with *grep*
grep("A", simpleDNASeq_vec)

## Try the same command with *grepl* and see what it does
## The command answers: Is A present at a particular location
 grepl("A", simpleDNASeq_vec)

## Find a submotif 'AA' with the *gregexpr* command
gregexpr("AA", simpleDNASeq)

## Replace the first occurrence of "A" by "C" with sub
sub("A", "C", simpleDNASeq)

## Replace all occurrences of "A" by "C" with gsub
gsub("A", "C", simpleDNASeq)

## Extract nucleotides from position 4 to 8 with substr
substr(simpleDNASeq,4,8)

## Concatenate two sequences with paste and paste0
paste("AA", "CT", sep="")
paste("AA", "CT", sep=";")
paste0("AA", "CT")
```


# Exercise 15:

```
##  Verify if all the values of vec2 are higher than the values of vec1	with *all*
vec2 > vec1
all(vec2 > vec1)

## Verify if all the values of vec3 are equal to the values of vec1 with *all.equal*
vec1 == vec3
all.equal(vec1, vec3)
isTRUE(all.equal(vec1, vec3))
all.equal(vec1, vec1)

## Verify if any of the value of vec3 is higher than the values of vec1 with *any*
vec3 > vec1
any(vec3 > vec1)

## Find the duplicated	values of vec4 with *duplicated*
duplicated(vec4)

## Find if any	of the values of vec4 or vec5 are duplicated with *anyDuplicated*
anyDuplicated(vec4)
anyDuplicated(vec5)

## Remove duplicated values from vec4 and vec5	with *unique*
unique(vec4)
unique(vec5)

## Make the elements of vec5 unique with *make.unique*
make.unique(vec5)

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

#  Exercise 16:

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

# Exercise 17:

```
## Find the elements of vec4 that are higher than 3 and lower than 5
which(vec4 > 3 & vec4 < 5)

## Find the index of the minimum and maximum of vec4 with *which.min* and *which.max*
which.min(vec4)
which.max(vec4)
```

# Exercise 18:

```
## Create a vector vec3 <- c("Nanog", "CD19", "Oct4")
vec3 <- c("Nanog", "CD19", "Oct4")

## Perform the	intersection of	vec1 and vec3 with *intersect*
intersect(vec1, vec3)

## Peform union on vectors
union(vec1, vec3)
```


# Exercise 19:

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

# Exercise 20:

```
## Combine matrix 1 and 2 by row
rbind(matrix1, matrix2)

## Combine matrix 1 and 2 by column
cbind(matrix1, matrix2)
```

# Exercise 21:

```
## Convert *numvec_conv* to characters	with *as.character*
charvec_conv <- as.character(numvec_conv)
is(charvec)

## Convert *numvec_conv* to a factor with *as.factor*
as.factor(numvec)

## Convert *mat* to a dataframe with *as.data.frame*
df_conv <- as.data.frame(mat)
is(df_conv)

## Convert the	result back to a matrix
mat_conv <- as.matrix(df_conv)
is(mat_conv)

## Convert *mat* to a list
list_conv <- as.list(mat)
is(list_conv)
```

# Exercise 22:

```
## Create two numeric vectors
vec1 <- c(1,2,3,4)
vec2 <- c(5,6,7,8)

## Use mapply to perform a 2 by 2 sum of values
mapply(function(x,y) return(x+y), vec1, vec2)

## A more clever solution is to use vectorisation
vec1 + vec2
```

<br>

# Exercise 23:

```
## Create an empty file 'test_1.txt' with *file.create*.
file.create("test_1.txt")

## Verify if 'test_1.txt' and 'test_2.txt' exist with *file.exists*
file.exists("test_1.txt")
file.exists("test_2.txt")

## Remove 'test_1.txt' with *file.remove*
file.remove("test_1.txt")

## Create again 'test_1.txt'
file.create("test_1.txt")

## Copy 'test_1.txt' to the destination file 'test_2.txt' with	*file.copy*
file.copy("test_1.txt", "test_2.txt")

## Rename 'test_2.txt' to 'test_3.txt' with *file.rename*
file.rename("test_2.txt", "test_3.txt")

## Retrieve the directory path of "/home/my_name/Documents/myfile.txt" with *dirname*
mock_example <- "/home/my_name/Documents/myfile.txt"
dirname(mock_example)

## Retrieve the above file name with *basename*
basename(mock_example)

## Go up one folder with *setwd("..")*
setwd("..")

## List the files of the directory 'training_files_manipulation' with *list.files*
list.files("./training_files_manipulation")
list.files("./training_files_manipulation", full.names = TRUE)

##  Delete the 'training_files_manipulation' directory with *unlink*
unlink("./training_files_manipulation", recursive = TRUE)
```

# Exercise 24:

```
## Write *DEgenes* to a csv file (DEgenes.csv) with *write.csv*
write.csv(DEgenes, file="DEgenes.csv")

## Read *DEgenes.txt* with *read.table*. Look at the options sep, header and row.names in ?read.table.
fi_txt <- read.table("DEgenes.txt", sep="\t", header = TRUE, row.names = 1,
 stringsAsFactors = FALSE)
fi_txt

## Read the 'DEgenes.csv' file	with *read.csv*
fi_csv <- read.csv("DEgenes.csv", header = TRUE, row.names = 1)
fi_csv

## Read the lines of 'DEgenes.txt' with *readLines*
fi_lines <- readLines("DEgenes.txt")
fi_lines

## Delete the files 'DEgenes.txt' and 'DEgenes.csv' in	one command with file.remove (create a vector with the file names)
file.remove(c("DEgenes.txt", "DEgenes.csv"))
```

# Exercise 25:

```
## List all variables present in the current session with *ls()*
ls()

## Save a variable test <- c(1,2,3) with *save*. Look at the options *?save*
test <- c(1,2,3)
save(test, file="test.Rdat")

## Load the saved variable into the environment with *load*
load("test.Rdat")

## Delete the variable	with *rm*
rm(test)

## Free the unused memory with	*gc()* (garbage collector)
gc()
```


# Exercise 26:

```
## Load the package BiocManager with *library*
library("BiocManager")

## Install the Bioconductor package "DESeq2" and "edgeR" with *install*
install("DESeq2")
install("edgeR")

## Remove the package edgeR with *remove.packages*
remove.packages("edgeR")

## Check your R version with *R.Version()*
R.Version()

## Check 'DESeq2' package version with	*packageVersion*
packageVersion("DESeq2")

## Check where the packages were installed with '.libPaths()'
.libPaths()
```

# Exercise 27:

```
## Start the R documentation page with	*help.start()*
help.start()

## Get help on the function DESeqDataSetFromMatrix with *?* or	*help*
?DESeqDataSetFromMatrix
help("DESeqDataSetFromMatrix")

## Visualize an example using DESeqDataSetFromMatrix with *example*
example("DESeqDataSetFromMatrix")

## Find all functions using the string 'write'	with *apropos*
apropos("write")

## See all available vignette
vignette()

## Check the DESeq2 vignette with *vignette*
vignette("DESeq2")
```

