# Booleans

Booleans refers to a system of logic using the value TRUE and FALSE. You are going to transcribe your thinking into your code! You will want very often to perform some operations requiring to evaluate if a statement is true or false. For instance, you might want to look for the expression of CD19 if you are treating B-cell samples or of CD4 if treating T-cell samples. The way to translate this logical thought is to code: "If my sample is of type B-cell, retrieve expression of CD19, else if my sample is of type T-cell, retrieve expression of CD4". Let's take one step further, from now on you have to think with **TRUE** and **FALSE**. The previous statement can be reformulated with: "If B-cell is TRUE, check CD19, else check CD4". Sounds efficient isn't it?
  
**Vocabulary: Boolean denotes the values TRUE/FALSE. In R, the type of these values is 'logical'. Try the command is(TRUE) and is(FALSE) in your console.**
