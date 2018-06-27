# Palindromes

## Solution

4. Write an efficient function that checks whether any permutation of an input string is a palindrome. A palindrome is a string that's the same when read forward and backward; for example: civic, mom, racecar, kayak
   
   ### Ehsanul's Solution

   ```js
    const isPalindrome = (str) => {
        let array = str.split("");
        array.reverse();
        let newString = array.join('');
        if (newString === str){
            return true
        }else{
            return false
        }   
    }
    isPalindrome('racecar')
    isPalindrome('rally')
   ```
