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

## References

[Wikipedia](https://en.wikipedia.org/wiki/Factorial)
