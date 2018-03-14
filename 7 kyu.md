# 7 kyu

## Reversed Strings

https://www.codewars.com/kata/reversed-strings/train/javascript/5a936e6f5084d78d9f00004f

Complete the solution so that it reverses the string value passed into it.

```JS
function solution(str){
  return str.split('').reverse().join('');
}

```


## Binary Addition

https://www.codewars.com/kata/binary-addition/train/javascript/5a78da95fd57773963000102

Implement a function that adds two numbers together and returns their sum in binary. The conversion can be done before, or after the addition.

The binary number returned should be a string.

```JS
function addBinary(a,b) {
  return (a+b).toString(2);
}

```


## Odd or Even?

https://www.codewars.com/kata/odd-or-even/train/javascript/5aa2efd9fd5777ed6200000c

Given an array of numbers, determine whether the sum of all of the numbers is odd or even.

Give your answer in string format as 'odd' or 'even'.

If the input array is empty consider it as: [0] (array with a zero).

```JS
function oddOrEven(array) {
 
return (array.reduce((a, b) => a + b, 0) % 2 === 0)? 'even' : 'odd';

}

```

## Sum of two lowest positive integers
https://www.codewars.com/kata/sum-of-two-lowest-positive-integers/train/javascript/5aa557b6fd57776ef800003b

Create a function that returns the sum of the two lowest positive numbers given an array of minimum 4 integers. No floats or empty arrays will be passed.

For example, when an array is passed like [19, 5, 42, 2, 77], the output should be 7.

[10, 343445353, 3453445, 3453545353453] should return 3453455.

```JS
function sumTwoSmallestNumbers(numbers) {  
 numbers.sort((a,b)=> a-b)
  return numbers[0] + numbers[1];
};

```

## Sort array by string length
https://www.codewars.com/kata/sort-array-by-string-length/train/javascript/5aa5c3d84a6b34e811000079

Write a function that takes an array of strings as an argument and returns a sorted array containing the same strings, ordered from shortest to longest.

For example, if this array were passed as an argument:

["Telescopes", "Glasses", "Eyes", "Monocles"]

Your function would return the following array:

["Eyes", "Glasses", "Monocles", "Telescopes"]

All of the strings in the array passed to your function will be different lengths, so you will not have to decide how to order multiple strings of the same length.

```JS
function sortByLength (array) {

return array.sort((a,b) => a.length - b.length)

};
```

## We Have Liftoff
https://www.codewars.com/kata/we-have-liftoff/train/javascript/5aa6e6d8373c2e71bb00006f

You have an array of numbers 1 through n (where 1 <= n <= 10). The array needs to be formatted correctly for the person reading the countdown of a spaceship launch.

Unfortunately, the person reading the countdown only knows how to read strings. After the array is sorted correctly make sure it's in a format he can understand.

Between each number should be a space and after the final number (n) should be the word 'liftoff!'

```JS
function liftoff(ins){
  return ins.sort((a,b) => b-a).toString().concat(' liftoff!').replace(/,/g,' ')
}

```

## Beginner Series #3 Sum of Numbers
https://www.codewars.com/kata/beginner-series-number-3-sum-of-numbers/train/javascript/5aa6ef917c7a5391c1000131

Given two integers a and b, which can be positive or negative, find the sum of all the numbers between including them too and return it. If the two numbers are equal return a or b.

Note: a and b are not ordered!

```JS
function GetSum( a,b ){
  let arr = [a,b]
  let high = Math.max(a,b)
  let low = Math.min(a,b)+1

for(i= low;i<high;i++){
   arr.push(i)
}
return (a == b) ? a : arr.sort((a,b) => a - b).reduce((a,b) => a + b)
  
}

```

## Average Scores
https://www.codewars.com/kata/average-scores/train/javascript/5aa865a1fd8c064ed5000026

Create a function that returns the average of an array of numbers ("scores"), rounded to the nearest whole number. You are not allowed to use any loops (including for, for/in, while, and do/while loops).

```JS
function average(scores) {
    return Math.round(scores.reduce((a,b)=>a+b)/scores.length)
}
```

## Simple Fun #176: Reverse Letter
https://www.codewars.com/kata/simple-fun-number-176-reverse-letter/train/javascript/5aa86b4a7c7a5362710000bd

Task
Given a string str, reverse it omitting all non-alphabetic characters.

Example
For str = "krishan", the output should be "nahsirk".

For str = "ultr53o?n", the output should be "nortlu".

Input/Output
[input] string str

A string consists of lowercase latin letters, digits and symbols.

[output] a string

```JS
function reverseLetter(str) {
  return str.split('').reverse().join('').replace(/[^A-Za-z]/gi, '')
}
```



