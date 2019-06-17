# Manipulating Numbers


Different operations can be performed on numbers such as rounding (**abs**, **ceiling**, **floor**, **round**), square rooting (**sqrt**), retrieving the minimum and maximum (**min**, **max**) and performing logarithmic transformation (**log**, **log10**, **log2**). On numeric vectors, one could generate random values (**sample**), compute the **sum** or the cumulative sum (**cumsum**), perform sorting (**sort**, **order**), generate series of numbers (**seq**, **seq_len**), or summarize values (**summary**).   


```
> ## Retrieve the absolute value of x
> x <- -2.849
> abs(x)
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
> ## Find the square root of 9
> x <- 9
> sqrt(x)
```

** Exercise 12**: Using the functions indicated in bold in the previous paragraph, try to:

  + Round number to upper or lower integer with 'ceiling(x)' and 'floor(x)' of  x <- 2.849
  + Round including one digit. Look at the documentation of 'round' with '?round'
  + Compute natural, base 2 and base 10 logarithms of x <- 5
  + Find the square root of  x <- 9

On vectors:


```
> ## Generate a vector containing 10000 random numbers
> ## The logic here is to extract 10000 values from the vector 1 to 1000000
> randomvec1 <- sample(1:1000000, 10000)
> head(randomvec1)
```

**Exercise 13:**

  + Extract the minimum and maximum values of randomvec1 with 'min' and 'max'
  + Compute the cumulative sum with 'cumsum' of the vector vec1 <- c(1,2,3,4,5) and store the result in the variable 'result_cumsum'
  + Create a vector of 10 random values between 1 and 1 000 000. Look at the 'sample'
  + Sort the values with the function 'sort'
  + Retrieve the indexes for sorting the values with the function 'order'
  + Generate values from 1 to 10 by 2 with the function ?seq
  + Try generating all values now and do the same thing with the function ?seq_len. Put the result in the variable vector_10.
  + Repeat the number 5 ten times with ?rep
  + Reverse elements of vector_10 with 'rev'
  + Compute the 'sum' of all values from 1 to 10 (use vector_10)
  + Compute the 'mean' of all values of vector_10
  + Compute a 'summary' of randomvec1


**Tip:** Try avoiding using ":" to generate series of values. Example: Use seq_len(10) instead of 1:10. The reason is that ':' does not handle correctly the empty sequence case. Try 10:0, it will build a reverse sequence instead of an empty sequence. This is important especially in for loops. Imagine that you want to print all values of a vector, if the vector is empty, seq_len will throw a correct error whereas with ':' it will not.

```
> test_vec <- vector()
> for(i in 1:length(test_vec)) print(test_vec[i])
> for(i in seq_len(test_vec)) print(test_vec[i])
```

**Note**: The brackets can be omitted if a "for" loop contains only one instruction.
