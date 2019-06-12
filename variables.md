# Variables

On a practical point of view, variables are just letters or words that you use in your program to stock values. More formally, the memory of a computer is organized as a grid made of cases. A 'simple' variable, for instance storing a numeric value, will write this value in one case of the memory grid. More complex variables, storing for instance your cell line table, will occupy several cases. In summary, a variable is just a structure of the R language that enables to store (and re-use) values in your computer memory. The word 'variable' is also used in other programming languages (Python, Java, C, etc) and is therefore not specific to R.

**Why would I want to store values in my computer?** Well, as we saw, you would want to compute for instance an addition, and use the result in a division!

In order to store values along your program, you need to '**assign**' your value to a variable. The term used in Programming is to '**declare**' a variable. Here is how you do it:

```
> ## Declare a variale 'a' containing the value 42
> a <- 42
> ## Display the value of 'a'
> a
```

**Exercise 2:**

  + Change the value of 'a' to 8
  + Display the value of 'a'
  + Perform an addition and use the result in a division
  + Display the result

<br>    
BAM! You got to the next level! Declaring and using variables in your program.

*NB: To declare a variable you can also use the symbol '=' but do not do it. This is very very ugly! Yes, there are weird programmers deciding about coding style practice :o. The real reason is to distinguish between variable declaration and parameters. You will understand this later.*


There are few rules to respect in naming variables:

  * It should start by a letter
  * The variables are case sensitive (A is not the same than a)
  * The variables **should not** take names already used by R (Ex: You should not declare a variable 'bind')

