# Manipulating Numbers


Different operations can be performed on numbers such as rounding (**abs**, **ceiling**, **floor**, **round**), square rooting (**sqrt**), retrieving the minimum and maximum (**min**, **max**) and performing logarithmic transformation (**log**, **log10**, **log2**). On numeric vectors, one could generate random values (**sample**), compute the **sum** or the cumulative sum (**cumsum**), perform sorting (**sort**, **order**), generate series of numbers (**seq**, **seq_len**), or summarize values (**summary**).   


```
> ## Retrieve the absolute value of x
> x <- -2.849
> abs(x)
> ## Find the square root of 9
> x <- 9
> sqrt(x)
> ## Round number to upper or lower integer
> x <- 2.849
> ceiling(x)
> floor(x)
> ## Round including digits
> round(x, digits=1)
> ## Compute natural, base 2 and base 10 logarithms
> x <- 5
> log(x)
> log2(x)
> log10(x)
```

On vectors:


```
> ## Generate a vector containing 10000 random numbers
> ## The logic here is to extract 10000 values from the vector 1 to 1000000
> randomvec1 <- sample(1:1000000, 10000)
> head(randomvec1)
>
> ## Extract the minimum and maximum values
> min(randomvec1)
> max(randomvec1)
>
> ## Compute the cumulative sum of the vector
> vec1 <- c(1,2,3,4,5)
> result_cumsum <- cumsum(vec1)
> result_cumsum
>
> ## sort the values
> randomvec2 <- sample(1:1000000, 10)
> randomvec2
> sort(randomvec2)
> ## Retrieve the indexes for sorting the values
> order(randomvec2)
> randomvec2[order(randomvec2)]
>
> ## Generate values from 1 to 10 by 2
> seq(from = 1, to = 10, by = 2)
> ## Generate values from 1 to 10
> seq(from = 1, to = 10)
> vector_10 <- seq_len(10)
>
> ## Repeat element 5 ten times
> rep(5, 10)
>
> ## Reverse elements
> rev(vector_10)
>
> ## Compute the sum of all values from 1 to 10
> sum(vector_10)
>
> ## Compute the mean of all values
> mean(vector_10)
>
> ## Summarize all values (min, max, etc)
> summary(randomvec1)  
```

**Tip:** Try avoiding using ":" to generate series of values. Example: Use seq_len(10) instead of 1:10. The reason is that ':' does not handle correctly the empty sequence case. Try 10:0, it will build a reverse sequence instead of an empty sequence. This is important especially in for loops. Imagine that you want to print all values of a vector, if the vector is empty, seq_len will throw a correct error whereas with ':' it will not.


```
> test_vec <- vector()
> for(i in 1:length(test_vec)) print(test_vec[i])
> for(i in seq_len(test_vec)) print(test_vec[i])
```

**Note**: The brackets can be omitted if a "for" loop contains only one instruction.
