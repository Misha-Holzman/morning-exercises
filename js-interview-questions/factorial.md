# Factorial

In mathematics, the factorial of a non-negative integer `n`, 
denoted by `n!`, is the product of all positive integers less 
than or equal to `n`. For example:

```
5! = 5 * 4 * 3 * 2 * 1 = 120
```

## Solution
1. Write a function called factorial() that takes a number and multiplies up all numbers from 1 through that number. Example: factorial(5) should equal 1 * 2 * 3 * 4 * 5.

   ```js
    const factorial = function(num) {
        let result = 1;
        for (let i = 2; i <= num; i++) {
            result *= i;
        };
        return result;
    };
   ```

# Recursion

![Inception](https://media.giphy.com/media/7pHTiZYbAoq40/giphy.gif)

Simply put, recursion is the ability for a function to call on itself. A function calling itself means that inside the body of the function we will have a call to the same function. When we use recursion it will go on until it reaches a certain desired state. In some cases we must call the function a fixed amount of times. In other cases it will continue running until a conditional check tells it to stop. Either way, we **MUST** have a well-defined stop condition in order to prevent the recursion from running forever (and overheating your computer).

## Recursive Solutions (Simon, Jesica & Yaakov)

   ```js
   factorial = num => {
     if(num === 0 || num === 1)
       return 1;
     else if (num > 1)
       return num * factorial(num - 1);
     else
       return undefined;
   }
   console.log(factorial(10));  // 3628800
   console.log(factorial(0));   // 1
   console.log(factorial(-10)); // undefined
   ```

   ```js
   const factorial = function(num) {
     if (num >= 1) {
       return num * factorial(num - 1);
     }  else {
         return 1;
     }
   };
   console.log(factorial(7));
   console.log(factorial(0));
   console.log(factorial(-2));
   ```

   ```js
   const factorial = function(n) {
     if (n <= 0) { 
       return 1;
     } else { 
       return (n * factorial(n - 1));
     }
   };
   factorial(3); // 6
   ```

## References

##### Learn and Understand Recursion in Javascript

[Medium – Learn and Understand Recursion in Javascript](https://codeburst.io/learn-and-understand-recursion-in-javascript-b588218e87ea)

##### Harvard CS50 Recursion Video (_click on image_)

[![Harvard CS50 Recursion](https://i.ytimg.com/vi/mz6tAJMVmfM/maxresdefault.jpg)](https://youtu.be/mz6tAJMVmfM)
