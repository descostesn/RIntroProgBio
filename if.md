# if


The basic structure is:

	if(condition){
		block of code
	}

You already saw in the previous paragraphs how to create 'condition'. You use relational and logical operators!

If my sample is of type B-cell, retrieve expression of CD19. Translating this statement into a code is super easy:


**Important: In the code below, you define an a-priori knowledge. YOU know that the marker of B-cell is CD19 and that the marker of T-cell is CD4. If you wonder how to use a program to retrieve all markers of all cell-types, that something more complicated. You need to learn more about data structures and functions (and packages). Be patient, you will come to it. In this introductory class, we aim at using simple and small examples.

```
> ## Create the variables containing genes expression and cell type
> expression_values <- c(100, 200)
> names(expression_values) <- c("CD19", "CD4")
> current_sample <- "B-cell"
```

<br>
**Exercise 10:**

  + Using the structure at the begining of the page, write a code that retrieve CD19 expression only if the current sample is B-cell. (TIP: use the function 'print(...)' replacing '...' by the "CD19" value of "expression_values").

<br>

BAM! You just made one of the major steps, you start thinking like a programmer, congrats!
