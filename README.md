
# All The Coding Challenges I've Ever Done


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
