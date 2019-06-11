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
> charvec_conv <- as.character(numvec_conv)
> is(charvec)
>
> ## Conversion of a numeric vector into a factor
> as.factor(numvec)
>
> ## Creation of a matrix
> mat <- matrix(data=1:6, nrow=2, ncol=3, byrow=T)
>
> ## Conversion of matrix to data.frame
> df_conv <- as.data.frame(mat)
> is(df_conv)
>
> ## Conversion of a data.frame to a matrix
> mat_conv <- as.matrix(df_conv)
> is(mat_conv)
>
> ## Conversion of a matrix to a list
> list_conv <- as.list(mat)
> is(list_conv) 
```
