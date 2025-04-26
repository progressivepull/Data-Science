## CH02/02_07

There are many functions defined in Numpy. How many? Let's see will import Numpy and then look at how many elements the **dir command return**. And you're going to see 603. This might change depending on the Numpy version you have. We are not going to cover all of the 600 plus attributes, but this is start working in Numpy. You'll find the ones useful for you and commit them to memory. However, there's one aspect of Numpy functions I like to discuss. 


So if I'm doing the **sine of 90**, I'm going to return a number. Remember **sine gets its values as radiants and not degrees**. You might wonder why Numpy is defining a function that's already defined in the built in math model. 

The reason is that we can take create a **vector which is np.arange from -3 to 3 and run Numpy sine on that and it's going to work**. We're going to get the sine of every element in the array. The builtin math sine will not work. 

A lot of Numpy functions are **U function or universal function**. It means they **work both on scalars regular numbers and arrays**. This is very handy and lets us work with the same function regardless of the input type. 

What happens if you like to write your own function? Do you need to check the type of the input every time? Well, you can, but Numpy provides an easier way. Let's have a look. So let's define our a ReLu which if **N is less than 0, return 0 otherwise return N** 

if you run it on a **scalar it is going to work**. However, if you try to run it on R vector, this is **going to raise an exception**. It will try to do if N smaller than 0, which is going to return a **Numpy array and the true value of a Numpy array is not defined**.

What you can do is use the np.vectorize the @ symbol at the beginning, meaning we're using the  **np.vectorize as a decorator**. If you're not familiar with decorators, we have several courses on the subject so the same function but now vectorized. 

And now when we run it, we can run it on the vector, but we can also run it on the number. We see something that is not familiar. This is an array with one value. However, this array behaves just like a number so if I'm doing our **function on -2 and removing 7 from it, I'm going to get -7**.

Ufuncs are also NaN aware, which means that if they **see NaN, the special floating value, that means not a number, they will return NaN as well**. So we create an element with NaNs and we get the result with the NaN at that location.


