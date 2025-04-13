Let's start looking into Numpy arrays. So first we import Numpy as np. And now I'm creating an array of three elements with 1, 2 and 3 run this. And we have an array 1, 2 and for starts. Arrays look very much like lists.

So we can ask for the length.

We can get the second element and arrays are 0 based indexing like the rest of Python.

But if you look closer, for example type of the 1st element, we see that it's not a Python integer but a Numpy int32.

For you can ask array what is the data type of the array using the dtype attribute. When you create an array, Numpy will determine the default type for the array for the input. However, you can specify explicitly the data type of the array to be created. This here is saying dtype np.int32 and we're going to get an array of int 32 comparing to any 64. This takes half the memory, but you need to make sure that all of your values fits inside a 32 bit integer.

You can multiply an array by itself. And what you're going to get is an elementwise multiplication, so 1 * 1 = 1, 2 * 2 = 4 and 3 * 3 = 9. I talked about Numpy and being fast. Let's have a look.

So I'm creating 2 arrays, each one with 1,000,000 random elements which are floats, and then I'm going to use the time magic to see how much time it takes. To multiply them and that took 6.27 milliseconds.

If you'd like to get the Dot Product of a matrix. Use the @ sign, which is the Python matrix multiplication operator. If we want to sell now, we're going to see 14, which is a dot product of these two arrays, we can move to more dimensions. So here's an array with three rows and three columns, and we can run this one. And now we can see the. That's a lot of code to write for a small sample metrics.
