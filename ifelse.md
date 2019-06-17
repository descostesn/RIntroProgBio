# if-else


The basic structure is:

	if(condition){
		block of code
	}else{
		block of code
	}

Let's now use the above structure to "formulate" a biological problem. If my sample is of type B-cell, retrieve expression of CD19, else retrieve CD4 (the sample is T-cell). Remember that YOU tell the program what to do with the knowledge that YOU have. Translating this statement into a code is super easy too:


```
> ## Now retrieve CD19 expression only if the current sample is B-cell
> if(current_sample == "B-cell"){
+ 	print(expression_values["CD19"])
+ }else{
+ 	print(expression_values["CD4"])
+}
```

** Exercise**: Change the value of current_sample to "T-cell" and see the difference


**Alert**: If I have more than two cell-types, I am stuck! You are right, let's add a third cell-type 'macrophage' for which we want to know the expression of the marker CD86.


```
> ## Create the variables containing genes expression and cell type
> expression_values <- c(100, 200, 300)
> names(expression_values) <- c("CD19", "CD4", "CD86")
> current_sample <- "B-cell"
> ## Now retrieve CD19 expression only if the current sample is B-cell
> if(current_sample == "B-cell"){
+ 	print(expression_values["CD19"])
+ }else if(current_sample == "T-cell"){
+ 	print(expression_values["CD4"])
+ }else{
+ 	print(expression_values["CD86"])
+}
```

As you probably understood, you can keep adding conditions. You can add even one million conditions if you want to use one million different cells! But do not worry, bioinformaticians made some resources and databases for you to avoid coding everything. **The aim of programming (with R) is to perform some complex tasks with a minimum number of code lines.** To formalize the code above, you can think about the structure:


	if(condition 1){
		block of code 1
	}else if(condition 2){
		block of code 2
	}else{
		block of code 3
	}

