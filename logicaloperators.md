# Logical operators


  Logical operators enable to carry out boolean operations such as AND, OR, NOT. This is very useful if you want several conditions to be true or false. For instance, you might want to consider a set of cells dead if the Ser5 amino-acid of RNA Polymerase II was mutated AND the type of cell is mammalian. Again, before seeing how to code that, let'start with simple examples.
\newline

```
> ## The AND operation is done with the symbol '&&'
> TRUE && TRUE
> TRUE && FALSE
> FALSE && FALSE
> ## The OR operation is done with the symbol '||'
> TRUE || TRUE
> TRUE || FALSE
> FALSE || FALSE
> ## The NOT operation is done with the symbol '!'
> !TRUE
> !FALSE 
> !FALSE || FALSE
> ## You can use parentheses to create logical groups
> (TRUE || FALSE) && (TRUE && FALSE) 
```
  
**Exercise**

 - Define two variables x and y with the values 5 and 6. Can you guess the result of (x > 5 && y > 5) || (x == y) ?

 - Define the following variables: mutation1 <- "Tyr1", mutation2 <- "Ser5", cellType1 <- "yeast", cellType2  <- "mammals". Code and verify the following statement:
  * mutation1 EQUAL "Ser5"
  * cellType2 DIFFERENT THAN "mammals"
  * mutation2 EQUAL "Ser5" AND cellType2 EQUAL "mammals"      

<br><br>
Keep in mind the following rules when coding:

| Statement | Result |
|-----------|--------|
| TRUE && FALSE | FALSE |
| TRUE &#124;&#124; FALSE | TRUE |

<br>
**Why?** Think about the following analogy: AND is multiplication and OR is addition. 1 is TRUE and 0 is FALSE. Then you replace the value in the table above: 

| Statement | Result |
|-----------|--------|
| 1 * 0 | 0 |
| 1 + 0 | 1 |


  You can also apply the logical operators on vectors **but** there is a subtlety. You need element-wise operators which are **simple** '|' or '&' (we used double '||' and '&&' which are **not** element-wise operators). Try the following code:

  
```
> ## Define two logical vectors
> vec1 <- c(TRUE, FALSE, TRUE)
> vec2 <- c(FALSE, FALSE, FALSE)
> ## Try the previous commands and see the results  (double symbols) 
> vec1 && vec2
> vec1 || vec2
> ## Now use the element-wise operators
> vec1 & vec2
> vec1 | vec2
> ## Finally try the negation operator
> !vec1
> !vec2 
> ## Can you predict the output of the following command?
> !vec1 & vec2
```

**Exercise: Put a different number of values in vec1 and vec2 and see what do you obtain.**
    
  In summary, the logic operators are:

| Operator | Description |
|----------|-------------|
| !        | Logical NOT |
| &        | Element-wise logical AND |
| &&       | Logical AND |
| &#124;        | Element-wise logical OR |
| &#124;&#124;       | Logical OR |

  