# Interacting with the environment


R offers important features to have in mind to control your working environment. You can control the directory that you are working in with **getwd()** (get working directory) and **setwd()** (set working directory). As you will read and write data to different folders, it is important to know where you are in your folder tree. This becomes even more useful when your scripts use relative paths instead of absolute paths.

During your programming session, you will create a certain number of variables. To list all variables created during your session, you can use the command **ls()**. Some variables can store results of functions which can run for hours or even days! These results are precious and you will very often do not want to restart the whole process from scratch. Fortunately, R provides the functions **save** and **load** to store and use variables.

A very important feature of R is that it **loads your data to the live memory of your computer**. Be careful not to load data that are too big, your computer will freeze and you will get stuck! To avoid over using the capacity of your computer, you will want to delete some variables containing data that are too big (when you do not need them anymore). To do so, use **rm** and the garbage collector **gc()**. The first takes variable names as parameter to delete them and the second frees the memory after deletion.


```
> ## Get the working directory
> getwd()
> ## Set the working directory
> dir.create("folder_to_enter_in")
> setwd("./folder_to_enter_in")
>
> ## List all variables present in the current session
> ls()
>
> ## Save a variable
> test <- c(1,2,3)
> save(test, file="test.Rdat")
> ## load a variable
> load("test.Rdat")
>
> ## Delete a variable
> rm(test)
> ## Free unused memory
> gc()
```

The power of R stands in the fact that it benefits from a huge community of users. Users make packages available to the community. I mentioned in session 1 two repositories which are [CRAN](https://cran.r-project.org/web/packages/available_packages_by_date.html) and [Bioconductor](https://www.bioconductor.org/packages/release/BiocViews.html#___Software). To install a package from CRAN or Bioconductor, you will do it from the R console (other ways to install packages are not covered here). For CRAN, you will use the function **install.packages** and for Bioconductor, you will use the package [BiocManager](https://cran.r-project.org/web/packages/BiocManager/index.html). A package can be uninstalled with **remove.packages**. Finally, a package is loaded in R with the function **library**.
 
Packages are dependent on the R and/or Bioconductor version. You will see that some code that was running fine on one R version will give you some errors on others. This is because the community is active and publishes updates regularly. R gives a major release every Spring, with several patches along the year, and Bioconductor is updated every 6 months. You can check your R version with **R.Version()** and the version of a particular package with **packageVersion**. 
It is also useful to know where packages are installed,  use **.libPaths()**.  


```
> ## Install a package from CRAN
> install.packages("ggplot2", dependencies = TRUE)
> install.packages("BiocManager", dependencies = TRUE)
>
> ## Load the package BiocManager
> library("BiocManager")
>
> ## Install the Bioconductor package "DESeq2" and "edgeR"
> install("DESeq2")
> install("edgeR")
>
> ## Remove the package edgeR
> remove.packages("edgeR")
>
> ## Check your R version
> R.Version()
>
> ## check edgeR package version
> packageVersion("edgeR")
>
> ## Check where the packages were installed
> .libPaths() 
```

There are different ways to get help in R. You can check the documentation of a particular function with **?myfunction** or **help**. If you do not remember the exact name of a function, you can use **apropos** which will list every function containing the word that you gave as parameter. You can see an example code with the function **example**. You can also use a web browser to look for documentation with **help.start()**. The R community also provides tutorials called **vignette**. You can see a list of vignettes with the function **vignette()** and visualize a particular one with **vignette("mypackagename")**. You can also see all available functions of a package by using the double columns "**mypackage::**" and pressing tab.


```
> ## Load the package DESeq2
> library("DESeq2")
>
> ## Check all the functions available in edgeR (using the tab command)
> DESeq2::
>
> ## Start the R documentation page
> help.start()
>
> ## Get help on the function DESeqDataSetFromMatrix
> ?DESeqDataSetFromMatrix
> help("DESeqDataSetFromMatrix")
>
> ## Visualize an example using DESeqDataSetFromMatrix
> example("DESeqDataSetFromMatrix")
>
> ## Find all functions using the string 'write'
> apropos("write")
>
> ## See all available vignette
> vignette()
> ## Check a particular vignette
> vignette("DESeq2")  
```


Finally, all the commands that you entered can be retrieved with the function **history**. To quit R enter **q()**. If you enter **yes**, you can save your R session which is actually very nice to not have to enter again all your commands.


```
> ## Visualize the last commands entered
> history()
> ## Visualize the 200 last commands entered
> history(200)
> ## Quit session
> q()                                                 
Save workspace image? [y/n/c]: 
```
