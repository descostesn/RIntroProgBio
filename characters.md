# Characters

You probably guessed what is covered in this section. You can also affect letters, words, and even sentences to your variables! This can be very useful, what if you want to perform operations on DNA or protein sequences? R can do it for you! Before using R to search DNA sequences or to generate reverse complements, let's start with simple manipulations. 
  

```
> ## Declare a variable 'a' containing the letter (character) 'b'
> a <- 'b'
> a
> ## Using double quotes works too
> a <- "b"
> a
> ## Give 'a' a sentence
> a <- 'Hello World'
> a
> ## What is happening if you use a quote inside a sentence?
> test <- 'it's a R workshop'
> test <- 'it\'s a R workshop'
> test
> test <- "it\'s a R workshop"
> test
```
