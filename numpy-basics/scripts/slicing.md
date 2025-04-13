# CH02 / 02_03

Python lists support slicing. Here's an example. Nums is a list of 1,2,3,4,5 and we do a slice from 2 to 4. It's going to run it. We're going to get 3 and 4. We start with the index 2 and index 3 and up two, but not including index 4.

These are half open ranges. You can do the same for Numpy arrays, so we create a vector with a range and then get a slice of this vector. Matrix slicing is useful since many times you'd like to take a subset of your data for training, testing, and other tasks.

Numpy takes slicing to a whole new level. Let's have a look. Let's create an array with three rows and four columns.

When we take the array at location 0, we are going to get the 1st row.

We can also say the second element in the 2nd row and this is 5 .

What happens if you want a column? We're going to use slicing. Say we want all the rows, but only the second element for every row, and now we're going to get 1, 5 and 9, which is the first column. Note that we get a flat array and not an array of ones.

If you want to get the full array of ones you will need to reshape.So now we get it in a vertical format.

You can do slicing on both axes, so all the rows from the 2nd row and the columns from the third column.

You can also use slicing to set values, so I'm doing the slicing as before, but now equals 7 and now when I'm looking at the array I'm seeing that the bottom right is all 7.
