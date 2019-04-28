
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

## Reversed Words
https://www.codewars.com/kata/reversed-words/train/javascript/5af4a1ee86d0752199000152

Complete the solution so that it reverses all of the words within the string passed in.

Example:

reverseWords("The greatest victory is that which requires no battle")
// should return "battle no requires which that is victory greatest The"

```JS
function reverseWords(str){
  return str.split(' ').reverse().join(' ')
}
```

## Find The Parity Outlier
https://www.codewars.com/kata/find-the-parity-outlier/train/javascript/5a850fe1b17101b5ab00008b

You are given an array (which will have a length of at least 3, but could be very large) containing integers. The array is either entirely comprised of odd integers or entirely comprised of even integers except for a single integer N. Write a method that takes the array as an argument and returns this "outlier" N.

```JS
function findOutlier(int){

let even = int.filter(a => a%2 === 0)
let odd = int.filter(a => a%2)

return (even.length > 1)? parseInt(odd) : parseInt(even)

}
```

## Format a string of names like 'Bart, Lisa & Maggie'.
https://www.codewars.com/kata/format-a-string-of-names-like-bart-lisa-and-maggie/train/javascript/5aafc2a9ba1bb5e11a0000f7

Given: an array containing hashes of names
Return: a string formatted as a list of names separated by commas except for the last two names, which should be separated by an ampersand.

```JS
function list(arr){

let count =  arr.length
let last = arr.map(a => a.name).slice(-1)
let name = arr.map(a => a.name).toString()
let names = arr.map(a =>a.name).slice(0,-1).join(', ')+ `${' &'} ${last}`

return (count>1)? names : name

}
list([{name: 'Bart'},{name: 'Lisa'}, {name: 'Doug'}])
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
