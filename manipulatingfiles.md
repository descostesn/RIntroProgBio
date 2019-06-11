# Manipulating Files

In this section we will create a directory and several files that we will manipulate. Follow the instructions and see in your file browser what they do:


```
> ## Create a directory
> dir.create("training_files_manipulation")
>
> ## Change your working environment to the just created directory
> setwd("./training_files_manipulation")
>
> ## Create an empty file
> file.create("test_1.txt")
>
> ## Verify if a file exists
> file.exists("test_1.txt")
> file.exists("test_2.txt")
>
> ## Remove a file
> file.remove("test_1.txt")
> ## Create an empty file
> file.create("test_1.txt")
>
> ## copy a file
> file.copy("test_1.txt", "test_2.txt")
>
> ## Rename a file
> file.rename("test_2.txt", "test_3.txt")
>
> ## Retrieve directory of file
> mock_example <- "/home/my_name/Documents/myfile.txt"
> dirname(mock_example)
>
> ## Retrieve file name from file path
> basename(mock_example)
>
> ## Lists files into a directory
> setwd("..") ## Go up in the directory tree
> list.files("./training_files_manipulation")
> list.files("./training_files_manipulation", full.names = TRUE)
>
> ## Dete directory
> unlink("./training_files_manipulation", recursive = TRUE)
```

I mostly use **file.list** with the option full.names = TRUE to load the paths to the files that I want to process, **dir.create** with the option recursive = TRUE to create output folders, and the functions **dirname/basename**.

Important functions to always have in mind are those used to read and write files. The files can be of different formats and you need to know a couple of tricks. Below is a full example creating the content and writing it to files. The different files are then read and their content is displayed. 


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
>
> ## Writing it in a csv file (same as before, only the function name changes)
> write.csv(DEgenes, file="DEgenes.csv")
>
> ## Reading the text file
> fi_txt <- read.table("DEgenes.txt", sep="\t", header = TRUE, row.names = 1, 
+ stringsAsFactors = FALSE)
> fi_txt
>
> ## Reading the csv file
> fi_csv <- read.csv("DEgenes.csv", header = TRUE, row.names = 1)
> fi_csv
>
> ## Reading the lines of a file
> fi_lines <- readLines("DEgenes.txt")
> fi_lines
>
> ## Deleting files
> file.remove(c("DEgenes.txt", "DEgenes.csv")) 
```
