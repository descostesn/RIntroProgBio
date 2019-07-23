# Manipulating Characters


Many functions enable to manipulate characters. Here only a few are presented. To illustrate their utility, DNA sequences will be manipulated.


```
> simpleDNASeq <- "AACATGACAGTTAGGACAGATACAATAATATATACAGAGACAGACAGACAGATTATATAC"
>
> ## Separate the characters wih the function strsplit
> simpleDNASeq_vec <- unlist(strsplit(simpleDNASeq,""))
```

**Exercise 14:**

Using the simpleDNASeq	character string:

  + Find the indexes of 'A' with *grep*.
  + Try the same command with *grepl* and see what it does.
  + Find a submotif 'AA' with the *gregexpr* command.
  + Replace the first occurrence of "A" by "C" with *sub*.
  + Replace all occurrences of "A" by "C" with *gsub*.
  + Extract nucleotides from position 4 to 8 with *substr*.
  + Concatenate two sequences with *paste*. Look at *?paste0* and replace the previous command with it.