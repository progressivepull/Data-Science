## CH3/03_02 Loading CSV Files

We're going to have a look at the log of one of my runs a few years back. 

We'll start by looking at the data which is in **CSV format**. Pandas is going to load the whole CSV into memory and it's a **good idea to have a quick look at the data before you load some corrupted data or a file** that is too big to fit in memory. If you **don't have enough memory on your computer, you can spin a machine in the cloud** with a lot of memory, do your work, and then tear it down. This approach is usually very cost effective and much easier than using a big data platform. If you think your data is too big, remember that you can spin a machine with several terabytes of memory. 

![data_four_columns](https://github.com/browntruck246/Data-Science/blob/main/Data-Science-Foundations-Python/pandas/images/data_four_columns.png)


So here's our data. We have 4 columns, time, latitude, longitude and height.

So let's start. First, let's look at the size of the file on disk, so I'm going to use path Lib and then define what is kilobyte. Define the CSV file and **use the stat method to get the size and divide it by kilobyte as the size is in bytes**. So let's run this one so 426 kilobytes. 

You can do the same thing with the **shell command**, so we start with the bank sign telling Ipython or the interactive prompt to run a shell command, and this **is an extension to Python And you pass the name of the CSV file prefixed by the dollar sign as a variable**. Note that this command will work only on Linux or a Mac, not on. Windows. Now let's see how many lines we have. 

So we do with CSV file open and you should **open always file with a with statement**. This makes sure that they are closed when you are done with them. So we're going to run it, **count the lines** and also **print the 1st 5 lines**. 

And we can do the same with the Shell command. First the head utility to see the 1st 5 lines and then the WC -l to see how many lines we have in there. 

Now we can load the data frame into pandas, so we import pandas as pd and the df is pd read CSV. The variable holding the **dataframe is traditionally called df**.

We are going to print how many rows are in the data frame so len of df. And now we are going to get 740 while wc showed us 741, pandas is loading the 1st row as the column names and counting only the rest of the rows which are the data rows. 

Let's have a look at the column. So df.columns and we see we have time, latitude, longitude and height which matches what we actually see in the CSV. 

We can also run the info method to get some **information about every column**, so the column how many non values we have and what is the data type of every. We see that the first column is an object, which means the string and then we have floats for latitude, longitude and height. 

You can also find the **described method which will give you information** about numerical columns. So only the latitude and longitude and height you'll get the **count, the mean, standard deviations and other interesting statistics**.
