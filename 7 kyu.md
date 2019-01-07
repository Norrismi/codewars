# 7 kyu

### Get the Middle Character
https://www.codewars.com/kata/get-the-middle-character/train/javascript/5aa1a0cc373c2eb596000064

You are going to be given a word. Your job is to return the middle character of the word. If the word's length is odd, return the middle character. If the word's length is even, return the middle 2 characters.

```JS
function getMiddle(s){
   
  let evenOdd = s.length % 2 === 0
  let minMid = s.charAt(s.length/2-1)
  let mid = s.charAt(s.length/2)
  
  return (evenOdd == true)? minMid.concat(mid): mid
}
```
### Credit Card Mask
https://www.codewars.com/kata/credit-card-mask/train/javascript/5aa19a904a6b34f9a000003b

Usually when you buy something, you're asked whether your credit card number, phone number or answer to your most secret question is still correct. However, since someone could look over your shoulder, you don't want that shown on your screen. Instead, we mask it.

```JS
function maskify(cc) {
return cc.substring(0, cc.length-4).replace(/[0-9,a-z,A-Z]/g, "#").concat(cc.slice(-4))
}
```
### Thinkful - String Drills: Repeater
https://www.codewars.com/kata/thinkful-string-drills-repeater/train/javascript/5b58e5004a317ae08d000040

Write a function named repeater() that takes two arguments (a string and an integer), and returns a new string where the input string is repeated that many times.

```JS
function repeater(str, n){
  return str.repeat(n)
}
```

### Round to the next multiple of 5
https://www.codewars.com/kata/round-to-the-next-multiple-of-5/train/javascript/5af24e0504a9266773000117

Given an integer as input, can you round it to the next (meaning, "higher") 5?

```JS
function roundToNext5(n){
  return Math.ceil(n/5)*5
}

```
### Square Every Digit
https://www.codewars.com/kata/square-every-digit/train/javascript/5c33542b348b3e000d6ede00

Welcome. In this kata, you are asked to square every digit of a number.

For example, if we run 9119 through the function, 811181 will come out, because 92 is 81 and 12 is 1.

Note: The function accepts an integer and returns an integer

```JS
function squareDigits(num){
  let cut = num.toString().split('')
  let raised = cut.map(a => Math.pow(a,2)).toString()
  
  return parseInt(raised.replace(/,/g, ''))

}

```


## Thinkful - List Drills: Longest word
https://www.codewars.com/kata/thinkful-list-drills-longest-word/train/javascript/5abeb8eaa88ee7b8f4000100

Write a function longest() that takes one argument, a list of words, and returns the length of the longest word in the list.

For example:

>>> words = ['simple', 'is', 'better', 'than', 'complex']
>>> longest(words)
7

```JS
function longest(words) {
  return words.toString().split(',').sort((a,b) => a.length-b.length ).pop().length
}

```

## Sum of a sequence
https://www.codewars.com/kata/sum-of-a-sequence/train/javascript/5c2588780b744390d9000123

Your task is to make function, which returns the sum of a sequence of integers.

The sequence is defined by 3 non-negative values: begin, end, step.

If begin value is greater than the end, function should returns 0

```JS
const sequenceSum = (begin, end, step) => {
  let arr = []

  for (var i=begin; i<=end; i += step){
    arr.push(i)
  }
 return (arr <= 0)? 0: arr.reduce((a,b )=> a+b)
};

```


## Reverse Letters in Sentence
https://www.codewars.com/kata/reverse-letters-in-sentence/train/javascript/5b086a2c908b7e850d000016

Take a sentence (string) and reverse each word in the sentence. Do not reverse the order of the words, just the letters in each word.

If there is punctuation, it should be interpreted as a regular character; no special rules.

If there is spacing before/after the input string, leave them there.

String will not be empty.

```JS

function reverser(sen) {
		return sen.split('').reverse().join('').split(' ').reverse().join(' ')
}

```


## Highest and Lowest
https://www.codewars.com/kata/highest-and-lowest/train/javascript/5ac2dca6a88ee75ee6000013

In this little assignment you are given a string of space separated numbers, and have to return the highest and lowest number.

Example:

highAndLow("1 2 3 4 5"); // return "5 1"
highAndLow("1 2 -3 4 5"); // return "5 -3"
highAndLow("1 9 3 4 -5"); // return "9 -5"

```JS
function highAndLow(numbers){
 let spl =  numbers.split(' ')
 return `${Math.max(...spl)} ${Math.min(...spl)}`
}
```


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


## Breaking chocolate problem
https://www.codewars.com/kata/breaking-chocolate-problem/train/javascript/5c168187ccc95726f70001b8

Your task is to split the chocolate bar of given dimension n x m into small squares. Each square is of size 1x1 and unbreakable. Implement a function that will return minimum number of breaks needed.

For example if you are given a chocolate bar of size 2 x 1 you can split it to single squares in just one break, but for size 3 x 1 you must do two breaks.

If input data is invalid you should return 0 (as in no breaks are needed if we do not have any chocolate to split). Input will always be a non-negative integer.

```JS
function breakChocolate(n,m) {
let choc = [n,m]

return (choc[0] && choc[1]>0)
  ?choc[0]*choc[1]-1
  : 0
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

## Shortest Word
https://www.codewars.com/kata/shortest-word/train/javascript/5aac4907fd5777073800025f

Simple, given a string of words, return the length of the shortest word(s).

String will never be empty and you do not need to account for different data types.

```JS
function findShort(s){
  sorted = s.split(' ').map(a => a.length).sort((a,b)=> a-b)
  return sorted[0]
}
```

## Friend or Foe?
https://www.codewars.com/kata/friend-or-foe/train/javascript/5aaed7d3ba1bb57bae00001a

Make a program that filters a list of strings and returns a list with only your friends name in it.

If a name has exactly 4 letters in it, you can be sure that it has to be a friend of yours! Otherwise, you can be sure he's not...

Ex: Input = ["Ryan", "Kieran", "Jason", "Yous"], Output = ["Ryan", "Yous"]

Note: keep the original order of the names in the output.

```JS
function friend(friends){
  return friends.filter(a => a.length == 4)
}
```



