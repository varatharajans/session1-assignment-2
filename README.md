# session1-assignment-2
DATA ANALYTICS WITH R, EXCEL AND TABLEAU SESSION 1 ASSIGNMENT 2

 Assignment - 2 
Session 1 – Introduction to Working with R 


Problem Statement 
1. What should be the output of the following Script? 

v <- c ( 2,5.5,6) 
t <- c (8, 3, 4)
print (v%/%t

Ans:-

> v<-c(2,5.5,6)
> t<-c(8,3,4)
> print(v%/%t)
output

[1] 0 1 1


2 You have 25 excel files with names as xx_1.xlsx, xx_2.xlsx,........xx_25.xlsx in a dir.
Write a program to extract the contents of each excel sheet and make it one df.


Ans:-
	setwd("c:/R/mergeme") 0r specific file path name
files=list.files(pattern=".xlsx")
for(i in 1:length(files))
{filename=files[i]
  data=read.xlsx(file = filename,header = T)
  assign(x = filename,value = data)}
#Suppose the columns are the same for each file, 
#you can bind them together in one dataframe with bind_rows from dplyr:
library(dplyr)
#one more option is as follows
df<-lapply(files, read.xlsx) %>% bind_rows()


3 If the above 25 files were csv files, what would be your script to read?



Ans:-

setwd("c:/R/mergeme") 0r specific file path name
files=list.files(pattern=".csv")
for(i in 1:length(files))
{filename=files[i]
  data=read.csv(file = filename,header = T)
  assign(x = filename,value = data)}
#Suppose the columns are the same for each file, 
#you can bind them together in one dataframe with bind_rows from dplyr:
library(dplyr)
#one more option is as follows
df<-lapply(files, read.csv) %>% bind_rows()


 	
Expected Output 
Not Applicable Copyrights© 2017, AcadGild. All Rights Reserved 3 

The Approximate time to complete this task is 20 Minutes.


