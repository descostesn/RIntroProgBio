# Manipulating Characters


Many functions enable to manipulate characters. Here only a few are presented. To illustrate their utility, DNA sequences will be manipulated.


```
> simpleDNASeq <- "AACATGACAGTTAGGACAGATACAATAATATATACAGAGACAGACAGACAGATTATATAC"
> ## Separate the characters wih the function strsplit
> simpleDNASeq_vec <- unlist(strsplit(simpleDNASeq,""))
>
> ## Find the indexes of 'A'
> grep("A", simpleDNASeq_vec)
> ## Is A present at a particular location
> grepl("A", simpleDNASeq_vec)
>
>## Find a submotif in the sequence
> gregexpr("AA", simpleDNASeq)
>
> ## Replace the first occurrence of "A" by "C"
> sub("A", "C", simpleDNASeq)
> ## Replace all occurrences of "A" by "C"
> gsub("A", "C", simpleDNASeq)
>
> ## Extract nucleotides from position 4 to 8
> substr(simpleDNASeq,4,8)
>
> ## Concatenate two sequences
> paste("AA", "CT", sep="")
> paste("AA", "CT", sep=";")
> ## paste0 avoids using the empty separator
> paste0("AA", "CT")
```
