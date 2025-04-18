# 03/04 Access rows and columns (access.py)

Let's access some data.So first we'll load our dataframe. 

To get a column, you can use the **square bracket and the name of the column, so df lat** and I'm getting the whole latitude column. 

You can also use df.lat like an attribute access, but I don't recommend using the dot notation in some cases column names have spaces in them and then you can't use the documentation. Anyway, so **getting the habit of using square brackets, which always.** 

You can select **more than a single column**, so here I'm passing a list with two column names and I'm going to get back a data frame with two columns. 

If you want a specific value, you can first select the column and then the row. **So selecting the latitude column and then the first value.** Remember that Python is 0. Based and not one based. The first item is at 0 location. 

If you want an **entire row you can use the dot loc access** so dot loc and now we get the row.  

So we see the time, latitude, longitude and height look and also work with **slices as well**. So from 2 to. 7 unlike slicing in Python, which are half open, the dot lock in pandas slices from the start to the end, including the end. 

You can also combine slices and column selection, so we're **selecting only the latitude and longitude columns, and then getting from 2 to 7.** This time Panda is going to use the Python style slicing which is 1/2 open range, meaning you get the 1st. Index up to but not including the last one. 

I know it's a bit confusing. The best way to make these things sink in is to practice take some data frames, **slice and dice them until you get comfortable** with the results and you'll be just fine. 

**Every column in pandas is a series.** One of the differences between series and regular Python. **Lists is that they have a labeled axis called an index.** 

All the columns in the data frame show the same index, so we can do **df.index and then run the cell and this is a range index starting from zero until 740 with steps of one.** 

Let's create a small example. So we **create a data frame.** We have some values with Numpy, a range of five rows and two columns. We specify the columns and. **Then we say the index is ABCD and E.** We're going to run this code. You see now that the index here is ABCD and E.


And now, if you're going to use dot lock 0, **this is going to fail because there's no row labeled 0, but there is a row labeled A**.

So I can do DfT lock a I can also slice between A&D and pandas can handle it just as well. A side note, labels. Don't have to be unique if there are repeating labels you will get all the rows with this label. Sometimes you'd like to access the 1st row regardless of the label. In this case you can use the iloc accessor, which works by position, so DF, iloc at location 0. And this is going to work and bring us. The first row. Another kind of index you can have is time based index. So let's change the data frame index which currently if we look at it is a range index and we are going to set it to the time. And have a look at it and now it is a daytime index with all of these. Values. Now, if you're going to run the lock zero, we're going to see that it's going to fail because we don't have any row that is labeled with zero. Now, however, I can access a row by time, and I can pass the time as a string and pandas is fine with it. You can even access time index with the time unit, so here we're going to access. Everything that is at 348 and we're going to get all the rows that fall in this minute. By the way, I'm not jogging at these crazy times. These times are in UTC and I'm at Israel, which means the time was actually 6:48 AM. Still early, but not that early.
