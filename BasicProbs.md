"write a function which returns hello world irrespective of the args passed to it"

solution:
var createHelloWorld = function() {
    return function(...args) {
        return ("Hello World");
    }
};



Explaination:
The nested function simply returns the string "Hello World". This means that whenever the createHelloWorld function is called,
it will return the nested function that,
when called itself, will always return the string "Hello World".

it is an example of a currying function.
###############################################################################
Given an integer n, return a counter function. This counter function initially returns n and then returns 1 more than the previous value every subsequent time it is called (n, n + 1, n + 2, etc)

Example 1:
Input: 
n = 10 
["call","call","call"]
Output: [10,11,12]
Explanation: 
counter() = 10 // The first time counter() is called, it returns n.
counter() = 11 // Returns 1 more than the previous time.
counter() = 12 // Returns 1 more than the previous time.
Example 2:
 
Constraints:
-1000 <= n <= 1000
At most 1000 calls to counter() will be made

solution:

var createCounter = function(n) {
    let count=n;
    return function() {
       return count++
    };
};

/** 
 * const counter = createCounter(10)
 * counter() // 10
 * counter() // 11
 * counter() // 12
 */


 const counter = createCounter(10)
 counter() // 10
 counter() // 11
 counter() // 12

 Explaination :

 This is an example of closure
