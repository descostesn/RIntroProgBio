# On Types


Several functions enable you to verify the type of data that you are dealing with:


```
> ## Creating different data
> ## Create a number
> mynum <- 10
>
> ## Create a character 
> myname <- "Luca"
>
> ## Create a character vector
> condition_values <- c("WT", "KO", "WT", "WT", "KD", "KD", "KO")
>
> ## Create a data.frame
> DEgenes <- data.frame(geneName = c("Tfcp2l1", "Ulk1", "Atp9a", "Esrrb", 
+ "Jam2", "Lap3"),
+ baseMean = c(13565.269, 4993.927, 1115.084, 7989.630, 3022.796, 7035.433), 
+ log2FoldChange = c(7.633774, 3.486161, 2.933659, 7.161020, 9.992639, 
+ 2.089235),  
+ pvalue = c(6.250339e-157, 2.930542e-152, 2.676439e-101,  2.657022e-98,  
+ 1.521128e-94, 3.774027e-93), stringsAsFactors = FALSE)
>
> ## Create a factor
> condition_factor <- factor(condition_values)
>
> ## Create a list
> chd8Info <- list(Name = "CHD8", 
+ Description = c("Chromodomain Helicase DNA Binding Protein", 
+ "Helicase With SNF2 Domain", "ATP-Dependent Helicase CHD8", "HELSNF1", 
+ "Chromodomain-Helicase-DNA-Binding Protein", "Axis Duplication Inhibitor"), 
+ Database = data.frame(database = c("HGNC", "Entrez_Gene", "Ensembl", "OMIM"), 
+ number = c(20153, 57680, 00000100888, 610528)))
>
> ## Create a logical
> mybool <- TRUE
>
> ## Create a matrix
> mat <- matrix(data=1:6, nrow=2, ncol=3, byrow=T)
>
> ## Create an empty value
> NAval <- NA
```

Verify what is the type of each variable:


```
> is(mynum)
> is(myname)
> is(condition_values)
> is(DEgenes)
> is(condition_factor)
> is(chd8Info)
> is(mybool)
> is(mat)
> is(NAval)
> is(NAval)
```

You can also verify if a variable is of a given type:


```
> ## Verify if it is a numeric
> is.numeric(mynum)
>
> ## Verify if it is a character
> is.character(myname)
> is.character(condition_values)
> is.character(mat)
>
> ## Verify if it is a vector
> is.vector(mynum)
> is.vector(myname)
> is.vector(condition_values)
> is.vector(chd8Info)
>
> ## Verify if it is a data.frame
> is.data.frame(condition_values)
> is.data.frame(DEgenes)
>
> ## Verify if it is a factor
> is.factor(condition_values)
> is.factor(condition_factor)
>
> ## Verify if it is a list
> is.list(condition_factor)
> is.list(chd8Info)
>
> ## Verify if it is a logical
> is.logical(chd8Info)
> is.logical(mybool)
>
> ## Verify if it is a matrix
> is.matrix(mybool)
> is.matrix(mat)
>
> Verify if NA
> is.na(mat)
> is.na(NAval)
```

You see that myname and condition_values are of the same type. However, we wanted to create a character and a vector. The reason is that myname is a character vector of length 1 and condition_values is a character vector of length 7. In the same way, mynum is a numeric vector of length 1.
