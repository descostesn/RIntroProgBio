# Vectors

 Feeling a bit limited in what you can do so far? No worries, let's level up our programming skills. You probably heard about vectors in high-school, probably in Physics and Mathematics. Remember, this arrow having a length and a direction? Well, forget about it :). Vectors in R have nothing to do with this. What is nice is that they are more simple, much more simple!

**Vocabulary**: A vector is the simplest R data structure consisting of a collection of numeric or character values (there are other types of vectors but that will not be covered here).

In the examples below, you will see different manners to create vectors and to access their elements.


```
> ## A first way to declare numeric vector
> vector("numeric", 10)
> ## And character vectors
> vector("character", 5)
```

Maybe you would like to control what is inside your vector:


```
> ## Generate a serie of numbers from 5 to 15
> 5:15
> ## Generate letters from A to D
> ## The function LETTERS generate A-Z
> LETTERS
> ## Now subselect the first four letters
> LETTERS[1:4]
```

BAM! You just have used a R function with subsetting the vector! We will talk about R functions later in this course. Let's go back to simple operations:


```
> ## Generate vectors with combine
> c(1,2,3)
> c("A", "B", "C")
> ## Let's use variables to combine vectors
> vector1 <- c(1,2,3)
> vector2 <- c(8,9,10)
> vector3 <- c(vector1, vector2)
> vector3
```

We are going now to see how to access and modify particular elements of a vector:


```
> ## Create a vector with values from 11 to 25 
> vector1 <- 11:25
> vector1
> ## Access the first element
> vector1[1]
> # Modify the 5th element
> vector1[5] <- 100
> vector1
```

Finally, let' see how to combine numbers and characters:


```
> genes <- c(100,205,348,345)
> names(genes) <- c("CHD8","MALAT1","HoxC","Nanog")
> genes
> genes[2]
> genes["HoxC"]
```

**Exercise**: What would happen if you give more names than values?
