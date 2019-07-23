# Conversions


It can be very useful to convert between types. For instance, you will very often use a function returning a list that you will want to convert to a matrix. Below are some examples of type conversion:


```
> charvec <- c("1", "2", "2", "3", "3", "4", "5")
> numvec <- c(1, 2, 2, 3, 3, 4, 5)
> is(charvec)
> is(numvec)
>
> ## Conversion of vector types
> numvec_conv <- as.numeric(charvec)
> is(numvec_conv)
>
> ## Creation of a matrix
> mat <- matrix(data=1:6, nrow=2, ncol=3, byrow=T)
```

<br>

**Exercise 21**:

  + Convert *numvec_conv* to characters with *as.character*
  + Convert *numvec_conv* to a factor with &*as.factor*
  + Convert *mat* to a dataframe with *as.data.frame*
  + Convert the result back to a matrix with as.****** (you can guess what to use at this point :)
  + Convert *mat* to a list
  
