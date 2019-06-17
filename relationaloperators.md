# Relational operators

Before writing the code to perform the selection of CD19 or CD4, let start playing a bit with logicals. **Relational operators** enable performing comparisons:


        <        lower than
        >        greater than
        <=       less than or equal to
        >=       greater than or equal to
        ==       equal to
        !=       not equal to


For instance:

```
> ## Define two genes variables gene1 and gene2 containing expression values 
> gene1 <- 5
> gene2 <- 16
> ## Check if gene1 expression is lower than gene2 expression
> gene1 < gene2
```

**Exercise 8**:

  + Check if gene1 expression is greater than gene2 expression
  + Check if gene1 expression is less than or equal to 5
  + Check if gene2 expression is greater than or equal to 20
  + Check if gene2 expression is equal to 16
  + Check if gene1 expression is different (not equal to) than 5

<br>

 The beauty of R is that it is a **vectorized language**. Therefore, the relational operators are also working on vectors. You might want to compare the expressions of specific genes in two conditions. For that, we use again the genes that we saw in the 'vectors' section: "CHD8","MALAT1","HoxC","Nanog".


```
> ## Define the expression values of the 4 genes in condition 1
> condition1 <- c(34,52,88,65)
> ## Define the expression values of the 4 genes in condition 2
> condition2 <- c(24,82,81,69)
> ## Define the names of the genes for each condition
> names(condition1) <- c("CHD8","MALAT1","HoxC","Nanog")
> condition1
> names(condition2) <- c("CHD8","MALAT1","HoxC","Nanog")
> ## Check if the genes are more highly expressed in condition1
> condition1 > condition2
```

**Question: What would happen if your vectors do not have the same number of values?**
