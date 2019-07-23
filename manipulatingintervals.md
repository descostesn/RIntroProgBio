# Manipulating Intervals


It is useful to be able to compare collections of information. For instance, you would like two sets of genes to be ordered in the same way, to perform the intersection or the union of your genes. For the first aim, you need to retrieve the indexes enabling to order a dataset according to a reference one with the function **match**. For the two other aims, it is pretty straightforward:


```
> ## Re-ordering vec1 according to vec2
> vec1 <- c("CD19", "CD4", "CD86")
> vec2 <- c("CD86", "CD19", "CD4")
> indexes <- match(vec1, vec2)
> vec1[indexes]
```

<br>

**Exercise 18:**

  + Create a vector vec3 <- c("Nanog", "CD19", "Oct4")
  + Perform the intersection of vec1 and vec3 with *intersect*.
  + Perform the	union of vec1 and vec3 with *union*.
  