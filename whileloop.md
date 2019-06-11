# while loop


You probably going to guess the structure:

		while(condition){
			do something
		}

And... You are going to understand why we saw boolean in the previous section. Hopefully you are going to feel a 'click' in your brain pushing you to pronounce the sound 'aaaaaaaahhhhhhhhhh'. ok, the idea of the while loop is to say: **While condition is TRUE, keep doing 'something'**. 

Let's take a super easy example: while i is lower than 4, display the gene name. Since our vector contains only 4 names, it makes sense isn't it?


```
> i <- 1
> while(i <= 4){
+ print(gene_names[i])
+ i <- i + 1
+}
```

**Exercise:** What will happen if I change the condition to i <= 10? What will happen if I remove 'i <- i + 1'? (When you will realize what is going on, click the stop button on the top right corner of the console).
