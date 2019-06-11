# Dataframes


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

