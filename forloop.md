# for loop


The structure is:

	for(condition){
		do something
	}

I am going to make the following very confusing statement: 


**DO NOT USE FOR LOOPS IN R UNLESS YOU CANNOT DO OTHERWISE**



**Why? Because -for- is very slow in R! There is much better, you will learn what later! If you cannot wait, look at the functions apply, lapply and sapply.**

**So why having a section about 'for' then? Because the concept of loop is one of the most important in programming and because sometimes you will need to use -for- even if it is not super efficient.**

To understand the concept and utility of looping, try to code the following task yourself without looking at the code below. Create a vector of gene names and print each name on the console (use the function 'print'). To be consistent, re-use the following vector: 

	gene_names <- c("CHD8","MALAT1","HoxC","Nanog").

You probably ended doing something like this:


```
> ## Create the vector
> gene_names <- c("CHD8","MALAT1","HoxC","Nanog")
> ## Visualize it
> gene_names
> ## Display the first gene
> gene_names[1]
> ## Display the second gene
> gene_names[2]
> ## Display the third gene
> gene_names[3]
> ## Display the fourth gene
> gene_names[4]
```

Do you see the problem? That is very repetitive and a lot of code. Fortunately, a loop enables you to do this automatically:


```
> ## Let see first how the 'condition' works
> for(i in 1:4){
+ print(i)
}
> ## Now you have understood what it does, use it to access your gene names
>  for(i in 1:4){
+ print(gene_names[i])
+}
```

**WOW!** Super efficient isn't it? Now that you know how a loop works, you are going to see that using while is also very powerful.

