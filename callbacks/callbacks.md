Callbacks and Higher-Order Functions
====================================

*   ### Challenge 1
    
    Create a function `addTwo` that accepts one input and adds 2 to it.
*   ### Challenge 2
    
    Create a function `addS` that accepts one input and adds an "s" to it.
*   ### Challenge 3
    
    Create a function called `map` that takes two inputs:  
    
    1.  an array of numbers (a list of numbers)
    2.  a 'callback' function - a function that is applied to each element of the array (inside of the function 'map')
    
    Have `map` return a new array filled with numbers that are the result of using the 'callback' function on each element of the input array.  
    
    map(\[1,2,3,4,5\], multiplyByTwo); //-> \[2,4,6,8,10\]  
    multiplyByTwo(1); //-> 2  
    multiplyByTwo(2); //-> 4
      
    
*   ### Challenge 4
    
    Create a function called `forEach` that takes an array and a callback, and runs the callback on each element of the array. `forEach` does not return anything.
    
    let alphabet \= '';
    const letters \= \['a', 'b', 'c', 'd'\];
    forEach(letters, function(char) {
      alphabet += char;
    });
    console.log(alphabet);   //prints 'abcd'
    
*   ### Challenge 5
    
    In challenge 3, you've created a function called `map`. In this challenge, you're going to rebuild the `map` function by creating a function called `mapWith`. This time you're going to use `forEach` inside of `mapWith` instead of using a `for` loop.
*   ### Challenge 6
    
    Create a function called `reduce` that takes an array and reduces the elements to a single value. For example it can sum all the numbers, multiply them, or any operation that you can put into a function.
    
    const nums \= \[4, 1, 3\];
    const add \= function(a, b) { return a + b; }
    reduce(nums, add, 0);   //-> 8
    
    Here's how it works. The function has an "accumulator value" which starts as the `initialValue` and accumulates the output of each loop. The array is iterated over, passing the accumulator and the next array element as arguments to the `callback`. The callback's return value becomes the new accumulator value. The next loop executes with this new accumulator value. In the example above, the accumulator begins at 0. `add(0,4)` is called. The accumulator's value is now 4. Then `add(4, 1)` to make it 5. Finally `add(5, 3)` brings it to 8, which is returned.
*   ### Challenge 7
    
    Construct a function `intersection` that takes in an array of arrays, compares the inner arrays, and returns a new array with elements found in all of them. BONUS: Use reduce!
*   ### Challenge 8
    
    Construct a function `union` that takes in an array of arrays, compares the inner arrays, and returns a new array that contains all elements. If there are duplicate elements, only add it once to the new array. Preserve the order of the elements starting from the first element of the first array. BONUS: Use reduce!
*   ### Challenge 9
    
    Construct a function `objOfMatches` that accepts two arrays and a callback. `objOfMatches` will build an object and return it. To build the object, `objOfMatches` will test each element of the first array using the callback to see if the output matches the corresponding element (by index) of the second array. If there is a match, the element from the first array becomes a key in an object, and the element from the second array becomes the corresponding value.
*   ### Challenge 10
    
    Construct a function `multiMap` that will accept two arrays: an array of values and an array of callbacks. `multiMap` will return an object whose keys match the elements in the array of values. The corresponding values that are assigned to the keys will be arrays consisting of outputs from the array of callbacks, where the input to each callback is the key.
*   ### Challenge 11
    
    Construct a function `objectFilter` that accepts an object as the first parameter and a callback function as the second parameter. `objectFilter` will return a new object. The new object will contain only the properties from the input object such that the property's value is equal to the property's key passed into the callback.
*   ### Challenge 12
    
    Create a function `majority` that accepts an array and a callback. The callback will return either `true` or `false`. `majority` will iterate through the array and perform the callback on each element until it can be determined if the majority of the return values from the callback are `true`. If the number of `true` returns is equal to the number of `false` returns, `majority` should return `false`.
*   ### Challenge 13
    
    Create a function `prioritize` that accepts an array and a callback. The callback will return either `true` or `false`. `prioritize` will iterate through the array and perform the callback on each element, and return a new array, where all the elements that yielded a return value of `true` come first in the array, and the rest of the elements come second.
*   ### Challenge 14
    
    Create a function `countBy` that accepts an array and a callback, and returns an object. `countBy` will iterate through the array and perform the callback on each element. Each return value from the callback will be saved as a key on the object. The value associated with each key will be the number of times that particular return value was returned.
*   ### Challenge 15
    
    Create a function `groupBy` that accepts an array and a callback, and returns an object. `groupBy` will iterate through the array and perform the callback on each element. Each return value from the callback will be saved as a key on the object. The value associated with each key will be an array consisting of all the elements that resulted in that return value when passed into the callback.
*   ### Challenge 16
    
    Create a function `goodKeys` that accepts an object and a callback. The callback will return either `true` or `false`. `goodKeys` will iterate through the object and perform the callback on each value. `goodKeys` will then return an array consisting only the keys whose associated values yielded a `true` return value from the callback.
*   ### Challenge 17
    
    Create a function `commutative` that accepts two callbacks and a value. `commutative` will return a boolean indicating if the passing the value into the first function, and then passing the resulting output into the second function, yields the same output as the same operation with the order of the functions reversed (passing the value into the second function, and then passing the output into the first function).
*   ### Challenge 18
    
    Create a function `objFilter` that accepts an object and a callback. `objFilter` should make a new object, and then iterate through the passed-in object, using each key as input for the callback. If the output from the callback is equal to the corresponding value, then that key-value pair is copied into the new object. `objFilter` will return this new object.
*   ### Challenge 19
    
    Create a function `rating` that accepts an array (of functions) and a value. All the functions in the array will return `true` or `false`. `rating` should return the percentage of functions from the array that return `true` when the value is used as input.
*   ### Challenge 20
    
    Create a function `pipe` that accepts an array (of functions) and a value. `pipe` should input the value into the first function in the array, and then use the output from that function as input for the second function, and then use the output from that function as input for the third function, and so forth, until we have an output from the last function in the array. `pipe` should return the final output.
*   ### Challenge 21
    
    Create a function `highestFunc` that accepts an object (which will contain functions) and a subject (which is any value). `highestFunc` should return the key of the object whose associated value (which will be a function) returns the largest number, when the subject is given as input.
*   ### Challenge 22
    
    Create a function, `combineOperations`, that takes two parameters: a starting value and an array of functions. `combineOperations` should pass the starting value into the first function in the array. `combineOperations` should pass the value returned by the first function into the second function, and so on until every function in the array has been called. `combineOperations` should return the final value returned by the last function in the array.
*   ### Challenge 23
    
    Define a function `myFunc` that takes an array and a callback. `myFunc` should pass each element from the array (in order) into the callback. If the callback returns true, `myFunc` should return the index of the current element. If the callback never returns true, `myFunc` should return -1;
*   ### Challenge 24
    
    Write a function `myForEach` that accepts an array and a callback function. Your function should pass each element of the array (in order) into the callback function. The behavior of this function should mirror the functionality of the native `.forEach()` JavaScript array method as closely as possible.