# Characters

You probably guessed what is covered in this section. You can also affect letters, words, and even sentences to your variables! This can be very useful: What if you want to perform operations on DNA or protein sequences? R can do it for you! Before using R to search DNA sequences or to generate reverse complements, let's start with simple manipulations. 

```
> ## Declare a variable 'a' containing the letter (character) 'b'
> a <- 'b'
> a
```

** Exercise 3:**

  + Use double quotes to affect b to a and see the result
  + Give 'a' a sentence
  + What would happen if you have a quote inside your quote? Try affecting the sentence - it's a R workshop - to a variable

<br>

The solution to the last question is to use backslash:

```
> test <- 'it\'s a R workshop'
> test
> test <- "it\'s a R workshop"
> test
```
