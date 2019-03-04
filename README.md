
# All The Coding Challenges I've Ever Solved (And Created)

## 14. Sum All Numbers In A Range

We'll pass you an array of two numbers. Return the sum of those two numbers plus the sum of all the numbers between them.

The lowest number will not always come first.

Code: https://codesandbox.io/s/j9q37z115

Source: https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/intermediate-algorithm-scripting/sum-all-numbers-in-a-range

## 13. [TODO] Average Score (How To Use Reduce)

Array.prototype.reduce(), or simply reduce(), is the most general of all array operations in JavaScript. You can solve almost any array processing problem using the reduce method.

This is not the case with the filter and map methods since they do not allow interaction between two different elements of the array. For example, if you want to compare elements of the array, or add them together, filter or map could not process that.

The reduce method allows for more general forms of array processing, and it's possible to show that both filter and map can be derived as a special application of reduce.

However, before we get there, let's practice using reduce first.

Code: https://codesandbox.io/s/7ww34y1nk1

Source: https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/functional-programming/use-the-reduce-method-to-analyze-data

## 12. Chunky Monkey

Write a function that splits an array (first argument) into groups the length of size (second argument) and returns them as a two-dimensional array.

Code: https://codesandbox.io/s/4w7zoj5xlw

Source: https://learn.freecodecamp.org/javascript-algorithms-and-data-structures/basic-algorithm-scripting/chunky-monkey

## 11. Where Do I Belong?

Return the lowest index at which a value (second argument) should be inserted into an array (first argument) once it has been sorted. The returned value should be a number.

For example, getIndexToIns([1,2,3,4], 1.5) should return 1 because it is greater than 1 (index 0), but less than 2 (index 1).

Likewise, getIndexToIns([20,3,5], 19) should return 2 because once the array has been sorted it will look like [3,5,20] and 19 is less than 20 (index 2) and greater than 5 (index 1).

Code: https://codesandbox.io/s/720jkzry11

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

Code: https://codesandbox.io/s/02lj1v46p

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

## 3. Write a function that checks if a given string is a palindrome.

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

## 2. Write a function that returns the century of a year.

```javascript
function centuryFromYear(year){
  return Math.ceil(year/100);
}
```

Source: https://app.codesignal.com/arcade/intro/level-1/egbueTZRRL5Mm4TXN

## 1. Write a function that returns the sum of two values.

```javascript
function sum(value1, value2){
  return value1 + value2;
}
```

Source: https://app.codesignal.com/arcade/intro/level-1/jwr339Kq6e3LQTsfa
