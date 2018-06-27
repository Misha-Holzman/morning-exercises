# Fibonacci Number

In mathematics, Fibonacci numbers are characterized by 
the fact that every number after the first two is the sum of the two 
preceding ones; this is known as the Fibonacci sequence:

`0, 1, 1, 2, 3, 5, 8, 13, 21, 34, 55, 89, 144, ...`

A tiling with squares whose side lengths are successive Fibonacci numbers

![Fibonacci](https://upload.wikimedia.org/wikipedia/commons/d/db/34%2A21-FibonacciBlocks.png)

## Solution

2. Write a function called fibonacci() that takes an integer n and returns the fibonacci sequence as an array up to the nth element (or, an array of n elements). For example, fibonacci(5) should return [0, 1, 1, 2, 3]:

   _Note:_ We know that the Fibonacci number is the sum of the previous two sequence numbers, so let's say our Fibonacci sequence is 0-indexed and starts with 0. The first two numbers in our sequence are zero and one which we've stored into an array called `sequence`. With every loop iteration we are summing the previous two sequence values, then pushing the element into the `sequence` array.
   
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
   // [0, 1, 1, 2, 3]
   ```
    
    ### Ryan's Solution (using a while loop)
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

# Recursion

![Inception](https://media.giphy.com/media/7pHTiZYbAoq40/giphy.gif)

Simply put, recursion is the ability for a function to call on itself. A function calling itself means that inside the body of the function we will have a call to the same function. When we use recursion it will go on until it reaches a certain desired state. In some cases we must call the function a fixed amount of times. In other cases it will continue running until a conditional check tells it to stop. Either way, we **MUST** have a well-defined stop condition in order to prevent the recursion from running forever (and overheating your computer).

## Recursive Solution (Simon)

   ```js
   // Return the nth number in the Fibonacci sequence
   fibonacci = n => {
     if(n === 0) // Base Step 1
       return 0;
     else if(n === 1) // Base Step 2
       return 1;
     else if(n > 1) // Recursive Step/Pattern
       return fibonacci(n - 1) + fibonacci(n - 2);
     else
       return undefined;
   }
   // Array with first 10 numbers in the Fibonacci sequence
   let fibNums = [];
   for(let num = 0; num < 10; num++) {
     console.log(`Fibonacci(${num}) = ${fibonacci(num)}`);
     fibNums.push(fibonacci(num));
   }
   console.table(fibNums);
   ```

## References

[Wikipedia](https://en.wikipedia.org/wiki/Fibonacci_number)
