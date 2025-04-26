# CH02/ 02_06

Let's see what an array can offer us. So import NumPy as np and then create an array of three rows and three columns. Let's run it. 

And I'm going to do V dot. You can see a lot of things that can be accessed. From the array. 

Let's take a look at some of these attributes. So v.T returns the transpose of the matrix. 

Without v.any() will return true since there is at least one element in the array which is true. As a reminder, **everything in Python is true except the 0 value** numbers, empty collections none, and of course false itself. 

We also have v.all() and this one is going to return false. This is because we have one false element at the beginning which is 0.

any() and all() are useful functions, and you'll find out you're going to use them in various situations. 

Note that the truth value of an array is undefined, so if I'm going to if v print OK and run the cell, **I'm going to get an exception.** The Zen Python states that in the face of ambiguity. **Refuse the temptation to guess.** Experience shows that it's better to be safe than get something that will lead to a wrong computation. This is why Numpy refuses to guess the true value of an array, and you will need to be explicit and state either any() or all(). 

Numpy also provides some math method like Min, Max, Min, SD, Sum, Prod, and others. 

Let's take the product of the array, which is 0 because we have 0 at the beginning. 

This method work by default on the whole array, but you can specify which axis you'd like the operation to happen. 

For example, if you do axis equal 1, you will get the sum of the rows and if you do access equals zero you will get the sum of the columns.

This will work with array with more than two dimensions as well.

Just provide the right. Remember we said that Numpy works hard not to copy anything, but sometimes you do want to copy and mutate an array without affecting the original one. 

For this you can use the copy method. So v1 is a copy, we change v1, the 1st element to be -1 and then look at the original 1. And see that nothing has changed.
