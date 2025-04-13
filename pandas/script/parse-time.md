# CH03/03 Parse Time¶

Let's load our Data Frame. So we import pandas and we read the CSV and we display the data types. For each column. You can see the latitude, longitude and height are floats and the **time is an object, which usually means a string in panels**. In some cases it's OK for data to be a string, but in our case you expect some kind of a timestamp, unlike JSON and other formats, CSV don't have type information embedded with the data. Which means that everything comes out as a string. Pandas does a good job at guessing types, but here it needs our help in parsing the time. 


There are many ways to write time as a string. **Pandas parser know most of the common formats.** If you **need to write time as a string**, do yourself a favor and use a known **format such as RFC 3339**. Also pick a format without spaces in it. And have the **year first, so sorting time as a string will work as intended**. 

Let's take a look at the **read CSV method**. It has many many arguments. One of these arguments. Is past dates where you can pass a list of columns to be passed as times.

This is where our initial look at the data came handy. You know before loading which column you'd like to pass this time. **We're doing load pandas with CSV file and tell it to pass the dates.** With only a single column which is a time column. And run the cell and now we see that the time is daytime64[ns] which means a 64 bit timestamp in a nanosecond resolution on your machine. This might be a little bit different.
