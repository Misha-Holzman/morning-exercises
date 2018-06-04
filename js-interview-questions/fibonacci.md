# Fibonacci Number

In mathematics, Fibonacci numbers are characterized by 
the fact that every number after the first two is the sum of the two 
preceding ones; this is known as the Fibonacci sequence:

`0, 1, 1, 2, 3, 5, 8, 13, 21, 34, 55, 89, 144, ...`

A tiling with squares whose side lengths are successive Fibonacci numbers

![Fibonacci](https://upload.wikimedia.org/wikipedia/commons/d/db/34%2A21-FibonacciBlocks.png)

## Solution

2. Write a function called fibonacci() that takes a number n and returns the fibonacci sequence as an array up to the nth element (or, an array of n elements). For example, fibonacci(5) should return [0, 1, 1, 2, 3]:

   _Note:_ We know that the Fibonacci number is the sum of the previous two sequence numbers, so let's start our loop at index two (i = 2) which is the third element in the array. The first two numbers in our sequence are zero and one which we've stored into an array called `sequence`. With every loop iteration we are summing the previous two sequence values, then pushing the element into the `sequence` array.
   
   ```js
   const fibonacci = (n) => {
    let sequence = [0, 1];
    let sum;
        for (let i = 2; i < n; i++) {
            sum = sequence[sequence.length - 1] + sequence[sequence.length - 2];
            sequence.push(sum);
        }
        return sequence;
   }
   fibonacci(5)
   ```
    
    ### Ehsanul's Solution (using a while loop)
   ```js
    const fibbonacci = n => {
        let arr = [0];
        let val = 1;
        while (arr[arr.length - 1] < n) {
            arr.push((arr[arr.length - 1] + (val)));
            val = arr[arr.length - 2];
        }
        console.log(arr);
    };
    fibbonacci(5);
   ```

## References

[Wikipedia](https://en.wikipedia.org/wiki/Fibonacci_number)
