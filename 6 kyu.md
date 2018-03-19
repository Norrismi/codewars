
6 kyu
==========


## Sum of Digits/Digital Root

https://www.codewars.com/kata/sum-of-digits-slash-digital-root/train/javascript/5a922c60fd577731ad00004c

In this kata, you must create a digital root function.

A digital root is the recursive sum of all the digits in a number. Given n, take the sum of the digits of n. If that value has two digits, continue reducing in this way until a single-digit number is produced. This is only applicable to the natural numbers.

```JS
function digital_root(n) {
  let result = (''+n).split('').reduce((a,b) => parseInt(a,10) + parseInt(b, 10))
  if((''+result).split('').length>1) {
    return digital_root(result)
  }
  return parseInt(result, 10)
}

```

## Find the unique number
https://www.codewars.com/kata/find-the-unique-number-1/train/javascript/5aa7e781ba1bb5a1ba00013a

There is an array with some numbers. All numbers are equal except for one. Try to find it!

findUniq([ 1, 1, 1, 2, 1, 1 ]) === 2
findUniq([ 0, 0, 0.55, 0, 0 ]) === 0.55
It’s guaranteed that array contains more than 3 numbers.

The tests contain some very huge arrays, so think about performance.

```JS
function findUniq(arr) {
  let newArr = []
  arr.sort()
  return (arr[0] !== arr[1]) ?  arr[0] : arr.pop()
}
```

## Reverse Words
https://www.codewars.com/kata/reverse-words/train/javascript/5aa93722fd8c0676ca0000d6

Write a reverseWords function that accepts a string a parameter, and reverses each word in the string. Any spaces in the string should be retained.

Example:

reverseWords("This is an example!"); // returns  "sihT si na !elpmaxe"
reverseWords("double  spaces"); // returns  "elbuod  secaps"

```JS
function reverseWords(str) {
  return  str.split('').reverse().join('').split(' ').reverse().join(' ')
}
```

## Create Phone Number
https://www.codewars.com/users/Norrismi/completed_solutions

Write a function that accepts an array of 10 integers (between 0 and 9), that returns a string of those numbers in the form of a phone number.

Example:
createPhoneNumber([1, 2, 3, 4, 5, 6, 7, 8, 9, 0]) // => returns "(123) 456-7890"
The returned format must be correct in order to complete this challenge. 
Don't forget the space after the closing parentheses!

```JS
function createPhoneNumber(num){

return `(${num[0]}${num[1]}${num[2]}) ${num[3]}${num[4]}${num[5]}-${num[6]}${num[7]}${num[8]}${num[9]}`

}
```
