# Primality Test

A prime number is an integer greater than 1 that cannot be formed by multiplying two smaller natural numbers. A primality test is an algorithm for determining whether an input number is prime or not.

![Prime Numbers](https://www.timvandevall.com/wp-content/uploads/2014/04/Prime-Number-Chart.jpg)

## Solution

3. Write a function called isPrime() that returns a boolean depending on whether or not a given number is a prime number or not. For example, isPrime(5) should return true, whereas isPrime(4) should return false.
   
   ```js
    const isPrime = (n) => {
        // If number is less than one then by definition, it isn't prime.
        if (n <= 0) {
            return false;
        } else if (n <= 3) {
            // All numbers from 2 to 3 are prime.
            return true;
        }
        // If the number is not divisible by 2 then we can eliminate all further even divisors.
        if (n % 2 === 0) {
            return false;
        }
        // If there is no divisors up to square root of n then there is no higher divisors as well.
        const dividerLimit = Math.sqrt(n);
        for (let i = 3; i <= dividerLimit; i += 2) {
            if (n % i === 0) {
              return false;
            }
        }
        return true
    }
    isPrime(5)
    isPrime(6)
   ```
