# Factors

  Factors are in some way similar to vectors. They also contain several values but have some interesting additional properties. Firstly, factors are mainly used to store **qualitative** values, i.e. values that have a descriptive information and not a quantitative one.
For instance, going back to our example of gene expression in different conditions, the expression values are **quantitative** and the conditions are **qualitative**.

  More precisely, factors can contain different types of data: It can contain numerics or characters (or boolean, see next section). More importantly, it has **levels** which are values that each element of the factor can take. Not very clear, I know, keep reading. 

  Factors are close to vectors in the way that they contain a collection of elements, but each element has a limited number of values that it can take. Factors are widely used in Bioinformatics. It increases a lot the speed of computation for some given tasks. **Factors are very useful for summary statistics, plots and regression**.

  I can feel your brain getting high in temperature. Let's cool it down, they are in fact super easy to use:


```
> ## Create a vector describing treatment conditions for several of your samples
> condition_values <- c("WT", "KO", "WT", "WT", "KD", "KD", "KO")
> ## Create a factor with these values
> condition_factor <- factor(condition_values)
> ## Pay a close attention to the result of the command below
> condition_factor
```

  You can see that displaying the "condition_factor" not only gives the elements that it contains, but also the different levels composing the factor. **Levels is an ordered vector of the unique values of the factor**.
If you did not understand the previous sentence, just have a look at the vector "condition_values"; order it alphabetically and remove the duplicated values. BAM! you obtained the levels of your factor.

  In mathematics, you probably heard about the "Universe" of the data. A universe is all the possible values that your data can take. Therefore, the levels of a factor is the universe of its elements. Remember that they can only take a limited number of values. Going back to the example above, imagine that you perform a study of the transcription factor Myb. Because you are like mega smart, you build a system to have its conditional expression upon induction with Dox. On top of that, to publish in Nature or Science, and become super famous and super rich with a big villa in Santa Barbara, you perform a knock-down and a knock-out. The **universe** of your samples is "WT", "KO", "KD" and "Dox". Now you want to compare the WT with the KO but you want to use your universe to build your reports:


```
> ## Create a vector describing treatment conditions for several of your samples
> condition_values <- c("WT", "KO")
> ## Create a factor with these values
> condition_factor <- factor(condition_values, levels=c("WT", "KO", "KD", "Dox"))
> ## Pay a close attention to the result of the command below
> condition_factor
```

 Still don't see the point? ok. Imagine now that you have 500 samples in an excel spreadsheet, one column is the name of the condition, one column is the sample and one is the number of expressed genes. And now, you are not the super scientist but the student who came two years after, and who was asked to reanalyze your data while you are putting your golfbag in your Mercedes to rush to the clubhouse to see the pictures of the new house of your best friend Arnold. That would be super nice if you could know the different conditions of the experiment in a few lines. For that, you typically can use factors. We are now going to see examples showing why **factors are very useful for summary statistics and plots**.
 
**ALERT: In the following example, we will use some functions! Do not worry, you already used plenty of them: 5^3 (power), vector(), LETTERS, ':' (suite of numeric), names(), matrix(), rownames(), colnames(), data.frame() and list()**.

Download the file samplecondition.txt [here](https://github.com/descostesn/RIntroProgBio/blob/master/samplecondition.txt)

```
> ## Read the table containing the two columns condition and sample
> fi <- read.table("samplecondition.txt", header=TRUE)
> ## Visualize the first lines of the table
> head(fi)
> ## Count the number of rows
> nrow(fi)
> ## Count the number of columns
> ncol(fi)
> ## Get the number of rows and columns at once
> dim(fi)
> ## Get the column names
> colnames(fi)
> ## Get the type of fi
> is(fi)
> ## Get the type of each column
> is(fi$condition)
> is(fi$sample)
> is(fi$geneExpressed)
```

The two first columns of your table are factors! Now we are going to see why it is super useful:


```
> summary(fi)
```

Bam! In one command you can see that there are 171 KD samples, 173 KO samples and 156 WT samples. You are now going to make your first plot. We want to represent the number of gene expressed in function of the conditions. 


```
 > plot(fi$geneExpressed~fi$condition, xlab="condition", ylab="Nb Expressed",
 + main="Nb of Gene expressed per condition")
```

This command is decomposed into the following actions:

* **plot**: Is the command to plot something (you did not expect that right?).
* **fi\$geneExpressed\~fi\$condition**: This is a formula. What is on the left is the response and on the right the explanatory variable. You can read it as "plot the number of genes expressed per condition".
* **xlab**: Defines the label to display on the x-axis.
* **ylab**: Defines the label to display on the y-axis.
* **main**: Defines the title of the plot.


