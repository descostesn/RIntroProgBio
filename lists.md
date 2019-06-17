# Lists


  With matrices we were limited in the number of types to use (numeric or characters). The dataframes tackle this problem but is still limited in the number of dimensions (like matrices, you need each row to have the same number of elements). 
  
  Lists enable you to do whatever you want. You can mix types and number of dimensions. You can also mix data structures. You can create for instance a list with a character vector, a matrix and a dataframe! But be careful, they are a little bit particular in the
sense that accessing and modifying elements asks a different methodology. 

In the example below, let's create a list that contains different information about a particular gene, "CHD8". To keep it simple, the first element contains the name of the gene, the second a vector of aliases, and the third a dataframe of accession IDs.
Because you are now a R pro, we are going to use variables to create the list.


```
> ## First element is a character representing the gene name
> geneName <- "CHD8"
> ## The second element is a vector of aliases
> aliases <- c("Chromodomain Helicase DNA Binding Protein", 
+ "Helicase With SNF2 Domain", "ATP-Dependent Helicase CHD8", "HELSNF1", 
+ "Chromodomain-Helicase-DNA-Binding Protein", "Axis Duplication Inhibitor")
> ## The third element is a dataframe of accession IDs
> accessionID <- data.frame(database = c("HGNC", "Entrez_Gene", "Ensembl", 
+ "OMIM"), number = c(20153, 57680, 00000100888, 610528)) 
> ## Create the list of CHD8 information
> chd8Info <- list(geneName, aliases, accessionID)
> chd8Info
> ## Give a name to each element
> names(chd8Info) <- c("Name", "Description", "Database")
> chd8Info
```

If you have tested each line, you saw that before giving names to the list, each element was referenced with "[[". As we used "[" to access an element of a vector, we will use "[[" to access the elements of a list.

**Attention**: If you try to access an element of a list with '[' it will work. But you do not actually access the element! Try the following commands:


```
> chd8Info[[1]]
> chd8Info[1]
> is(chd8Info[[1]])
> is(chd8Info[1])
```


