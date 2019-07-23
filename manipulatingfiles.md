# Manipulating Files

In this section we will create a directory and several files that we will manipulate. Follow the instructions and see in your file browser what they do:


```
> ## Create a directory
> dir.create("training_files_manipulation")
>
> ## Change your working environment to the just created directory
> setwd("./training_files_manipulation")
```

**Exercise 23**

  + Create an empty file 'test_1.txt' with *file.create*.
  + Verify if 'test_1.txt' and 'test_2.txt' exist with *file.exists*.
  + Remove 'test_1.txt' with *file.remove*
  + Create again 'test_1.txt'.
  + Copy 'test_1.txt' to the destination file 'test_2.txt' with *file.copy*.
  + Rename 'test_2.txt' to 'test_3.txt' with *file.rename*.
  + Retrieve the directory path of "/home/my_name/Documents/myfile.txt" with *dirname*.
  + Retrieve the above file name with *basename*.
  + Go up one folder with *setwd("..")*.
  + List the files of the directory 'training_files_manipulation' with *list.files*.
  + Delete the 'training_files_manipulation' directory with *unlink*.

I mostly use **file.list** with the option full.names = TRUE to load the paths to the files that I want to process, **dir.create** with the option recursive = TRUE to create output folders, and the functions **dirname/basename**.

Important functions to always have in mind are those used to read and write files. The files can be of different formats and you need to know a couple of tricks. Below is a full example creating content and writing it to files. The different files are then read and their content is displayed. 


```
> ## Use the DESEQ table that we used in session 1
> DEgenes <- data.frame(geneName = c("Tfcp2l1", "Ulk1", "Atp9a", "Esrrb", 
+ "Jam2", "Lap3"),
+ baseMean = c(13565.269, 4993.927, 1115.084, 7989.630, 3022.796, 7035.433), 
+ log2FoldChange = c(7.633774, 3.486161, 2.933659, 7.161020, 9.992639, 
+ 2.089235),  
+ pvalue = c(6.250339e-157, 2.930542e-152, 2.676439e-101,  2.657022e-98,  
+ 1.521128e-94, 3.774027e-93), stringsAsFactors = FALSE)
> rownames(DEgenes) <- paste0("gene_", seq_len(nrow(DEgenes)))
>
> ## Writing it in a tabulation separated text file (see ?write.table)
> write.table(DEgenes, file="DEgenes.txt", sep="\t", quote=FALSE, 
row.names = TRUE, col.names = TRUE)
```

**Exercise 24**:

  + Write *DEgenes* to a csv file (DEgenes.csv) with *write.csv*.
  + Read *DEgenes.txt* with *read.table*. Look at the options sep, header and row.names in ?read.table.
  + Read the 'DEgenes.csv' file with *read.csv*.
  + Read the lines of 'DEgenes.txt' with *readLines*.
  + Delete the files 'DEgenes.txt' and 'DEgenes.csv' in one command with file.remove (create a vector with the file names)



