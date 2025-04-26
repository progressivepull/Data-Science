# CH02 / 02_04

Sometimes you'd like to select parts of an array not by indices, but by some logic, say all the values that are bigger than some threshold.

For this, we're going to use Boolean indexing. Let's see how it works. So we import Numpy and create an array with three elements. Let's run it.

You can index an array with another array in the same shape containing Boolean values true or false. So here's the array and I'm adding it in index with true, false, true and I'm going to run it. I'm going to get only the elements where the index was true. For now this does not seem that helpful, but let's see one more thing.

And this will make it super useful if I'm doing array bigger or equal to one. I'm going to get a Boolean array with false through and through and now I can combine these two and say array at the location where the array is bigger or equal to.

And I'm getting one and two, but not the zero.

You can combine these conditions or masks using Boolean operators. However these are not the normal Boolean operators that we have in Python. You're going to use ampersand (&) for AND the vertical bar (|) for OR and the tilde(~) for NOT.

So I have a bigger array now with 10 and I'm saying all the elements that are bigger than two and smaller than seven. Note that the parenthesis here is mandatory.

So everything that is not bigger than 7 usually going to write it as everything that is smaller or equal to 8. And here is an example of negation.

Let's do a more realistic example. We're going to find outliers using the standard score.

First, we're going to create our data. So I'm going to create. And array of 1000 elements with values between 0 and 10 with the normal distribution and then I'm going to add 2 outliers at location 33 and location 832.

Now I'm going to calculate my mask so the mask is where the absolute value of the value itself minus the mean, meaning the distance from the mean is bigger than two times the standard deviation inside the array, and then I'm going to calculate the values in the mask. I'm going to see exactly my outliers.

Over there I can even use this mask to change the values, let's say to the mean of the current array. This is an example for the power of Boolean indexing. You can do a lot of things in a very few line apart from the cool effect. This is also very fast. In numerical Python you try hard not to do any follow-ups. This method of computation is called vectorization and once you use it, everything runs at the C. For photon level of Numpy.

