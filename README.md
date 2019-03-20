
# All The Coding Challenges I've Ever Solved (And Created)

## 30. Ceaser's Cipher

One of the simplest and most widely known ciphers is a Caesar cipher, also known as a shift cipher. In a shift cipher the meanings of the letters are shifted by some set amount.

A common modern use is the ROT13 cipher, where the values of the letters are shifted by 13 places. Thus 'A' ↔ 'N', 'B' ↔ 'O' and so on.

Write a function which takes a ROT13 encoded string as input and returns a decoded string.

All letters will be uppercase. Do not transform any non-alphabetic character (i.e. spaces, punctuation), but do pass them on.

Source: https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/javascript-algorithms-and-data-structures-projects/caesars-cipher

```javascript
const alphabet = 'ABCDEFGHIJKLMNOPQRSTUVWXYZ';
//console.log(alphabet.length)

function rot13(str) { // LBH QVQ VG!

  const org = str
  console.log(str.length)

  let newStr = ''
  str = str.split(' ')

  for (const i of str){
    for(const char of i){
      // Catch symbols
      if(char.match(/\!|\?|\./)){
        newStr += char
      }else{
      //console.log(char)
      let index = alphabet.indexOf(char)
      index = index+13

      if(index >= 26)
      index = index -26

      //console.log(alphabet[index])
      newStr += alphabet[index]
      }
    }

    if(newStr.length!==org.length)
    newStr += ' '
  }
  return newStr;
}

// Change the inputs below to test
console.log(rot13("SERR PBQR PNZC"));
```

## 29. Roman Numeral Converter

## 28. Palindrome Checker

Return true if the given string is a palindrome. Otherwise, return false.

A palindrome is a word or sentence that's spelled the same way both forward and backward, ignoring punctuation, case, and spacing.

Source: https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/javascript-algorithms-and-data-structures-projects/palindrome-checker

```javascript
function palindrome(str) {
  // lowercase
  str = str.toLowerCase()
  // Remove unwanted characters
  str = str.replace(/\W/g,'')
  str = str.replace(/\_/g,'')
  // Ready to check
  console.log(str)

  for(let i = 0; i , str.length; i += 1){
    if(str[i] !== str[str.length-i-1]) return false
  }

  return true;
}
console.log(palindrome("race car")); // true
console.log(palindrome("A man, a plan, a canal. Panama")) // true
```

## 27. Missing Letters

Find the missing letter in the passed letter range and return it.

If all letters are present in the range, return undefined.

```javascript
const alphabet = 'abcdefghijklmnopqrstuvwxyz';

function fearNotLetter(str) {
  
  const firstLetterIndex = alphabet.indexOf(str.charAt(0))

  let index = firstLetterIndex;
  
  for(const char of str){

    if(alphabet[index] !== char)
    return alphabet[index]

    index += 1;
  }

}

console.log(fearNotLetter("abce"));
```

Source: https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/intermediate-algorithm-scripting/missing-letters

## 26. Sorted Union

Write a function that takes two or more arrays and returns a new array of unique values in the order of the original provided arrays.

In other words, all values present from all arrays should be included in their original order, but with no duplicates in the final array.

The unique numbers should be sorted by their original order, but the final array should not be sorted in numerical order.

```javascript
function uniteUnique() {
  let newArr = [];
  for(const arr of arguments){
    //console.log(JSON.stringify(arr))
    for(const item of arr){
      //console.log(item)
      if(newArr.indexOf(item) === -1)
      newArr.push(item)
    }
  }
  return newArr;
}
```

Source: https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/intermediate-algorithm-scripting/sorted-union

## 25. DNA Pairing

The DNA strand is missing the pairing element. Take each character, get its pair, and return the results as a 2d array.

Base pairs are a pair of AT and CG. Match the missing element to the provided character.

Return the provided character as the first element in each array.

For example, for the input GCG, return [["G", "C"], ["C","G"],["G", "C"]]

The character and its pair are paired up in an array, and all the arrays are grouped into one encapsulating array.

```javascript
function pairElement(str) {
  
  let result = [];
  for(const el of str){
    
    if(el.match(/G/))
    result.push(['G','C'])

    if(el.match(/C/))
    result.push(['C','G'])

    if(el.match(/A/))
    result.push(['A','T'])

    if(el.match(/T/))
    result.push(['T','A'])
    
  }

  return result;
}
```

Source: https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/intermediate-algorithm-scripting/dna-pairing

## 24. Everything Be True

Check if the predicate (second argument) is truthy on all elements of a collection (first argument).

In other words, you are given an array collection of objects. The predicate pre will be an object property and you need to return true if its value is truthy. Otherwise, return false.

In JavaScript, truthy values are values that translate to true when evaluated in a Boolean context.

Solution: https://codesandbox.io/s/ooom6qwjz5

Source: https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/intermediate-algorithm-scripting/everything-be-true

## 23. Binary To ASCII (And Back)

Return an English translated sentence of the passed binary string.

The binary string will be space separated.

Solution: https://codesandbox.io/s/n5ozj51o3m

Source: https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/intermediate-algorithm-scripting/binary-agents

## 22. Smallest Common Multiple

Find the smallest common multiple of the provided parameters that can be evenly divided by both, as well as by all sequential numbers in the range between these parameters.

The range will be an array of two numbers that will not necessarily be in numerical order.

For example, if given 1 and 3, find the smallest common multiple of both 1 and 3 that is also evenly divisible by all numbers between 1 and 3. The answer here would be 6.

(weird) Solution: https://codesandbox.io/s/xppl4n3rmw

Source: https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/intermediate-algorithm-scripting/smallest-common-multiple

## 21. Sum All Primes

Sum all the prime numbers up to and including the provided number.

A prime number is defined as a number greater than one and having only two divisors, one and itself. For example, 2 is a prime number because it's only divisible by one and two.

Solution: https://codesandbox.io/s/1zk5oyvxo4

Source: https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/intermediate-algorithm-scripting/sum-all-primes

## 20. Sum All Odd Fibonacci Numbers

Given a positive integer num, return the sum of all odd Fibonacci numbers that are less than or equal to num.

Solution: https://codesandbox.io/s/30r5146qw1

Source: https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/intermediate-algorithm-scripting/sum-all-odd-fibonacci-numbers

## 19. Search And Replace

Perform a search and replace on the sentence using the arguments provided and return the new sentence.

First argument is the sentence to perform the search and replace on.

Second argument is the word that you will be replacing (before).

Third argument is what you will be replacing the second argument with (after).

Solution: https://codesandbox.io/s/4rvovn2r4x

Source: https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/intermediate-algorithm-scripting/search-and-replace/

## 18. Pig Latin

Translate the provided string to pig latin.

Pig Latin takes the first consonant (or consonant cluster) of an English word, moves it to the end of the word and suffixes an "ay".

If a word begins with a vowel you just add "way" to the end.

Input strings are guaranteed to be English words in all lowercase.

Solution: [TODO] https://codesandbox.io/s/qvwn1q8nr9

Source: https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/intermediate-algorithm-scripting/pig-latin

## 17. Spinal Tap Case

Convert a string to spinal case. Spinal case is all-lowercase-words-joined-by-dashes.

Solution: https://codesandbox.io/s/l7l2p3qww9

Source: https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/intermediate-algorithm-scripting/spinal-tap-case

## 16. Advanced List Filtering

Make a function that looks through an array of objects (first argument) and returns an array of all objects that have matching name and value pairs (second argument). Each name and value pair of the source object has to be present in the object from the collection if it is to be included in the returned array.

Solution: https://codesandbox.io/s/84qw68lkj2

Source: https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/intermediate-algorithm-scripting/wherefore-art-thou

## 15. Difference Of Two Arrays

Compare two arrays and return a new array with any items only found in one of the two given arrays, but not both. In other words, return the symmetric difference of the two arrays.

Solution: https://codesandbox.io/s/2x7w0mx9jp

Source: https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/intermediate-algorithm-scripting/diff-two-arrays

## 14. Sum All Numbers In A Range

We'll pass you an array of two numbers. Return the sum of those two numbers plus the sum of all the numbers between them.

The lowest number will not always come first.

Solution: https://codesandbox.io/s/j9q37z115

Source: https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/intermediate-algorithm-scripting/sum-all-numbers-in-a-range

## 13. [TODO] Average Score (How To Use Reduce)

Array.prototype.reduce(), or simply reduce(), is the most general of all array operations in JavaScript. You can solve almost any array processing problem using the reduce method.

This is not the case with the filter and map methods since they do not allow interaction between two different elements of the array. For example, if you want to compare elements of the array, or add them together, filter or map could not process that.

The reduce method allows for more general forms of array processing, and it's possible to show that both filter and map can be derived as a special application of reduce.

However, before we get there, let's practice using reduce first.

Solution: https://codesandbox.io/s/7ww34y1nk1

Source: https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/functional-programming/use-the-reduce-method-to-analyze-data

## 12. Chunky Monkey

Write a function that splits an array (first argument) into groups the length of size (second argument) and returns them as a two-dimensional array.

Solution: https://codesandbox.io/s/4w7zoj5xlw

Source: https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/basic-algorithm-scripting/chunky-monkey

## 11. Where Do I Belong?

Return the lowest index at which a value (second argument) should be inserted into an array (first argument) once it has been sorted. The returned value should be a number.

For example, getIndexToIns([1,2,3,4], 1.5) should return 1 because it is greater than 1 (index 0), but less than 2 (index 1).

Likewise, getIndexToIns([20,3,5], 19) should return 2 because once the array has been sorted it will look like [3,5,20] and 19 is less than 20 (index 2) and greater than 5 (index 1).

Solution: https://codesandbox.io/s/720jkzry11

Source: https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/basic-algorithm-scripting/where-do-i-belong

## 10. Falsy Bouncer

Remove all falsy values from an array.
(Falsy values in JavaScript are false, null, 0, "", undefined, and NaN.)

```javascript
function isTruthy(v){
  return v
}

function bouncer(arr) {
  return arr.filter(isTruthy);
}

bouncer([7, "ate", "", false, 9]);
//[7, "ate", 9].
```

Source: https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/basic-algorithm-scripting/falsy-bouncer

## 9. Slice And Splice

You are given two arrays and an index.

Use the array methods slice and splice to copy each element of the first array into the second array, in order.

Begin inserting elements at index n of the second array.

Return the resulting array. The input arrays should remain the same after the function runs.

Solution: https://codesandbox.io/s/02lj1v46p

Source: https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/basic-algorithm-scripting/slice-and-splice/


## 8. Title Case A String

```javascript
function titleCase(str) {
  return str.toLowerCase().replace(/(^|\s)\S/g, (L) => L.toUpperCase());
}
```
Source: https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/basic-algorithm-scripting/title-case-a-sentence

## 7. Copy Machine (Understanding the spread operator)

We have defined a function, copyMachine which takes arr (an array) and num (a number) as arguments. The function is supposed to return a new array made up of num copies of arr. We have done most of the work for you, but it doesn't work quite right yet. Modify the function using spread syntax so that it works correctly (hint: another method we have already covered might come in handy here!).

Source: https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/basic-data-structures/copy-an-array-with-the-spread-operator/

## 6. What is a basic useful regex example?

A more practical use of lookaheads is to check two or more patterns in one string. Here is a (naively) simple password checker that looks for between 3 and 6 characters and at least one number:

```javascript
let samplePw = "astronaut";
let pwRegex = /(?=\w{5,})(?=\D*\d{2})/;
let result = pwRegex.test(samplePw);
```
Source: https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/regular-expressions/positive-and-negative-lookahead

How many double s ('ss') does 'Mississipi' contain?

```javascript
const difficultSpelling = "Mississippi";
const myRegex = /ss/g; // Change this line
const result = difficultSpelling.match(myRegex);
console.log(result.length)
```

Find all vowels within a string using regex.

```javascript
const testString = "We are all made of stardust.";
const vowelRegex = /[aeiou]/gi;
const notVowelRogex = [^aeiou]/gi;
const result = testString.match(vowelRegex);
```
Source: https://app.codesignal.com/challenge/u8fmjEnYDRp3kZ2tt

## 5. How Many Sundays? Or What The Heck Is "neduit"?

Write a function that returns the amount of sundays for a given period(n-days) starting from a specific day(d).

```javascript
https://codesandbox.io/s/8l0ym669ql
```
Source: https://app.codesignal.com/challenge/u8fmjEnYDRp3kZ2tt

### 4. [Self] Write a function that checks if two arrays contain identical data (in the same order).

```javascript
function compareArrays(array1, array2) {
  let same = true;
  array1.forEach((a, i) => {
    if (!same) return;
    same = a === array2[i];
  });
  return same;
}
```
Source: https://codesandbox.io/s/xv782x12ko

## 3. Is Palindrome

```javascript
function checkPalindrome(inputString) {
    
    const array = [ ...inputString];
    const arrayReverse = [ ...inputString].reverse();
    
    let check = true;
    array.forEach((a,i) => {
        if(check === false) return;
        check = a === arrayReverse[i];
    })
    
    return check;
}
```
Source: https://app.codesignal.com/arcade/intro/level-1/s5PbmwxfECC52PWyQ

## 2. Century Of A Year

```javascript
function centuryFromYear(year){
  return Math.ceil(year/100);
}
```

Source: https://app.codesignal.com/arcade/intro/level-1/egbueTZRRL5Mm4TXN

## 1. Sum Of Two Values

```javascript
function sum(value1, value2){
  return value1 + value2;
}
```

Source: https://app.codesignal.com/arcade/intro/level-1/jwr339Kq6e3LQTsfa
