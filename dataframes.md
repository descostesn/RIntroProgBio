# Dataframes

 With matrices, we entered the second dimension. However, they are limited in what they can contain (only numerics or characters). Data frames can contain data of different types (numeric and characters). Below, please ignore the "stringsAsFactors = FALSE" options. We will see in a next lesson what factors and booleans are. 

  
```
> ## Create a data frame of differentially expressed genes like you would get 
> ## in DESeq2
> DEgenes <- data.frame(geneName = c("Tfcp2l1", "Ulk1", "Atp9a", "Esrrb", 
+ "Jam2", "Lap3"),
+ baseMean = c(13565.269, 4993.927, 1115.084, 7989.630, 3022.796, 7035.433), 
+ log2FoldChange = c(7.633774, 3.486161, 2.933659, 7.161020, 9.992639, 
+ 2.089235),  
+ pvalue = c(6.250339e-157, 2.930542e-152, 2.676439e-101,  2.657022e-98,  
+ 1.521128e-94, 3.774027e-93), stringsAsFactors = FALSE)
> DEgenes
```

**Remark: You do not need to type '+', it appears in the console when you go to the next line.**


You just have obtained a "matrix" containing two different types. Below is how to access and modify this data frame. **Spoiler Alert**: You do it exactly as you did with matrices!


```
> ## Give the p-value of the gene Ulk1 and Jam2 (try each method)
> DEgenes[c(2,5), 4]
> DEgenes[c(2,5), "pvalue"]
> DEgenes[c("Ulk1","Jam2"), "pvalue"]
```

The indexing system of the second command uses both numeric and characters! Do you see the advantage of this structure? Well, there is an additional way to access the elements of a dataframe:


```
> ## Give the p-value of the gene Ulk1 and Jam2
> DEgenes$pvalue[c(2,5)]
```

As you see, we can now access the elements like in a vector. The reason is that 'DEgenes$pvalue' is indeed a vector. You can now think about a dataframe as a collection of vectors that can be of different types!

