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

### max diff - easy
https://www.codewars.com/kata/588a3c3ef0fbc9c8e1000095/train/javascript/60cbb48b382b9000360c15a8

```JS
function maxDiff(list){
  return (list <= 1) ? 0 : Math.max(...list) - Math.min(...list)

}
```

### Vowel One
https://www.codewars.com/kata/580751a40b5a777a200000a1/train/javascript

```JS
function vowelOne(str){

 return str.toLowerCase().split('').map(x => 
    (x === 'a'|| x == 'e'||x == 'i'||x == 'o'||x == 'u')
    ? 1: 0 ).join("")

}
```

### Maximum Multiple
https://www.codewars.com/kata/5aba780a6a176b029800041c/train/javascript/60478b965fbb3d001ad9f0aa

```JS
function maxMultiple(divisor, bound){
  
return Math.floor(bound/divisor)*divisor

}
```

### Categorize New Member
https://www.codewars.com/kata/5502c9e7b3216ec63c0001aa/train/javascript

```JS
function openOrSenior(data){
 return data.map(a => (a[0] >= 55 && a[1] > 7)? 'Senior': 'Open')
}
```

### Largest Elements
https://www.codewars.com/kata/53d32bea2f2a21f666000256/train/javascript

```JS
function largest(n,arr){

return (n === 0)
  ? []
  : arr.sort((a,b) => b-a).slice(0,n).sort((a,b)=>a-b)
}
```

### Especially Joyful Numbers
https://www.codewars.com/kata/570523c146edc287a50014b1/train/javascript

```JS
function numberJoy(n) {
    let get = n.toString().split('')
    let sum = get.map(a => parseInt(a,10)).reduce((a,b) => a+b)
    let sumR = Number(sum.toString().split('').reverse('').join(''))
    let prod = sum*sumR;
    return (prod == n)? true : false

}
```

### Sum of numerous arguments
https://www.codewars.com/kata/55c5b03f8c28da9a51000045/train/javascript

```JS
function findSum(nums){

  let arr = []

  for(i=0; i<arguments.length; i++){
      arr.push(arguments[i])
  }

  let negs = arr.some(a => (a<0))

  return (!arr.length? 0 : negs? -1 : arr.reduce((a,b) => a+b, 0) )


}
```

### Remove duplicate words
https://www.codewars.com/kata/5b39e3772ae7545f650000fc/train/javascript

```JS
function removeDuplicateWords (s) {

  return [...new Set(s.split(' '))].join(' ')

}
```

### Find the Missing Number
https://www.codewars.com/kata/57f5e7bd60d0a0cfd900032d/train/javascript

```JS
function missingNo(nums) {

  let order = nums.sort((a,b)=> a-b)

  let arr = []

  let get = order.map((a,i)=> (a == i+1)? arr.push(a) :undefined)
  
  return arr[0]-1
  
  if(order.length < 101){
    return 100
  }else{
    return arr[0]-1
  }

```

### Remove anchor from URL
https://www.codewars.com/kata/51f2b4448cadf20ed0000386/train/javascript

```JS
function removeUrlAnchor(url){
  
  let first = url.split('').includes('#')
  let num = url.split('').indexOf('#')
  let sen = url.split('').slice(0,num).join('')
  
  return (!first) ? url : sen
  
}
```

### Stanton measure
https://www.codewars.com/kata/59a1cdde9f922b83ee00003b/train/javascript

```JS
function stantonMeasure(arr){
  let firstArr = [];
  let secArr = []

  
  arr.map(a => (a == 1)? firstArr.push(a): null)

  let sec = firstArr.length
  
  arr.map(a => (a== sec)? secArr.push(a): null)
  
  return secArr.length
  
}
```

### Alternate capitalization
https://www.codewars.com/kata/59cfc000aeb2844d16000075/train/javascript

```JS
function capitalize(s){

  let even = s.split('').map((a,i) => i%2 != 0 
    ? a.toLowerCase(): a.toUpperCase()).join("")

    let odd = s.split('').map((a,i) => i%2 == 0 
    ? a.toLowerCase(): a.toUpperCase()).join("")

  return [even, odd];


};
```

### Smallest value of an array
https://www.codewars.com/kata/544a54fd18b8e06d240005c0/train/javascript
```JS
function min(arr, toReturn) {
	return (toReturn === 'value')? Math.min(...arr) : arr.indexOf(Math.min(...arr))

}
```

### Switcheroo
https://www.codewars.com/kata/57f759bb664021a30300007d/train/javascript
```JS
function switcheroo(x){

  return x.split('').map(a => (a == 'a')? a.replace('a','b'):a.replace('b','a')).join('')
  
}
```

### Multiply Word in String

```JS
function modifyMultiply (str,loc,num) {
  
let arr = [];
let get = str.split(' ')
let word = get[loc]
let count = 0;

  while(count<num){
    arr.push(word)
    count++
  }

return arr.join('-')  
} 
```

### Number of Decimal Digits
https://www.codewars.com/kata/58fa273ca6d84c158e000052/train/javascript

```JS
function digits(n) {
  return n.toString().split('').length
}
```

### 99 Problems, #1: last in list
https://www.codewars.com/kata/57d86d3d3c3f961278000005/train/javascript

```JS
const last = xs =>  (xs.length)? xs.pop(): null
```

### Summy
https://www.codewars.com/kata/599c20626bd8795ce900001d/train/javascript

```JS
function summy(nums){
  return nums.split(' ').map(a => parseInt(a)).reduce((a,b)=> a+b)
}
```


### Reverse list
https://www.codewars.com/kata/57a04da9e298a7ee43000111/train/javascript

```JS
function reverseList(arr) {
  
  
if(!arr.length){
  return []
}else{
  
  let get =  arr.toString().split(',').reverse().join().split(',')
  return get.map(a => parseInt(a))
  }
  
}
```

### Debug Sum of Digits of a Number
https://www.codewars.com/kata/563d59dd8e47a5ed220000ba/train/javascript

```JS
function getSumOfDigits(int) {

  return int.toString().split('').map(a => parseInt(a,10)).reduce((a,b) => a+b)

}
```


### Anagram Detection
https://www.codewars.com/kata/529eef7a9194e0cbc1000255/train/javascript

```JS
var isAnagram = function(test, original) {

	const testS =  test.split('').sort((a,b)=> a.localeCompare(b)).join('').toLowerCase()

	const originalS = original.split('').sort((a,b)=> a.localeCompare(b)).join('').toLowerCase()

	return (testS == originalS) ? true : false
};
```


### Numbers in strings
https://www.codewars.com/kata/59dd2c38f703c4ae5e000014/train/javascript/5deee8fad772160011c598ec

In this Kata, you will be given a string that has lowercase letters and numbers. Your task is to compare the number groupings and return the largest number. Numbers will not have leading zeros.

```JS
function solve(s){

return parseInt(s.replace(/\D/g,' ').split(' ').sort((a,b)=> a-b).pop(), 10)

}
```


### Sum of all the multiples of 3 or 5
https://www.codewars.com/kata/57f36495c0bb25ecf50000e7/train/javascript

Your task is to write function findSum.

Upto and including n, this function will return the sum of all multiples of 3 and 5.

```JS
function findSum(n) {
 
let arr = [];

for(i=n; i>0; i--){
  if(i%5 == 0 || i%3 == 0){
    arr.push(i)
  }
}

  return arr.reduce((a,b)=> a+b)
}
```

### Move 10
https://www.codewars.com/kata/57cf50a7eca2603de0000090/train/javascript

```JS
function moveTen(s){
 return s.split('').map((a) => a.charCodeAt()).map((a) => (a+10<= 122)? a+10 : a+9-25).map(a => String.fromCharCode(a)).join('')
}
```

### Growth of a Population
https://www.codewars.com/kata/563b662a59afc2b5120000c6/train/javascript/5ab178b97c7a53638a000071

In a small town the population is p0 = 1000 at the beginning of a year. The population regularly increases by 2 percent per year and moreover 50 new inhabitants per year come to live in the town. How many years does the town need to see its population greater or equal to p = 1200 inhabitants?

```JS
function nbYear(orgPop, per, inc, endPop) {
 
  
    let years = 0;
    let percent = per/100


    while(orgPop < endPop){
      orgPop += (orgPop * percent) + inc
      years++;
    }
    return years
}
```


### Fizz Buzz
https://www.codewars.com/kata/5300901726d12b80e8000498/train/javascript

If the value is a multiple of 3: use the value "Fizz" instead
If the value is a multiple of 5: use the value "Buzz" instead
If the value is a multiple of 3 & 5: use the value "FizzBuzz" instead

```JS
function fizzbuzz(n){

let arr = []

  for( var i=1; i<=n; i++){
    if(i % 15 == 0){
      arr.push('FizzBuzz')
    }else if(i % 3 == 0){
      arr.push('Fizz')
    }else if(i % 5 == 0){
      arr.push('Buzz')
    }else{
      arr.push(i)
    }
  }

  return arr

}
```

### 
Summing a number's digits
https://www.codewars.com/kata/52f3149496de55aded000410/train/javascript

```JS
function sumDigits(num) {

  if(!num > 0){
    return 0
  }else{

  return  num.toString().split('').filter(a => a>0).map(a => parseInt(a)).reduce((a,b)=> a+b)
  }
}
```


### Factorial
https://www.codewars.com/kata/57a049e253ba33ac5e000212/train/javascript

```JS
function factorial(n){
  let arr = [];

  for(let i=n; i>0; i--){
    arr.push(i)
  }

  return(n == 0)? 1 : arr.reduce((a,b) => a*b)
}
factorial(0)
```


### Find the divisors!
https://www.codewars.com/kata/544aed4c4a30184e960010f4/train/javascript

```JS
function divisors(int) {
  
let arr = []

for(i=int-1; i >= 2; i--){
  arr.push(i)
}

let solution = arr.filter(a => int % a == 0).sort((a,b) => a-b)

return (solution == false) ? `${int} is prime` : solution

};

```

### Count the divisors of a number
https://www.codewars.com/kata/542c0f198e077084c0000c2e/train/javascript/60469185d4e6fd001093b264

```JS
function getDivisorsCnt(n){

   for(var count=0, i=n; i>0; i--){
     if(n%i == 0){
       count++
     }
   }

   return count
}
```

### Find the stray number
https://www.codewars.com/kata/57f609022f4d534f05000024/train/javascript/5cc4ba70701f0d001122b50e

You are given an odd-length array of integers, in which all of them are the same, except for one single number.

Complete the method which accepts such an array, and returns that single different number.

```JS
function stray(num) {


let sort =  num.sort()

if(num[0] !== num[1]){
  
return num.shift()

}else{
  return num.pop()
}


}

```

### Isograms
https://www.codewars.com/kata/54ba84be607a92aa900000f1/train/javascript

An isogram is a word that has no repeating letters, consecutive or non-consecutive. Implement a function that determines whether a string that contains only letters is an isogram. Assume the empty string is an isogram. Ignore letter case.

```JS
function isIsogram(str){
  let lc = str.toLowerCase()
  
  let set = [...new Set(lc)].join('')

  return (set == lc ) ? true : false
}

```

### Form The Minimum
https://www.codewars.com/kata/form-the-minimum/train/javascript/5deedc7f857f8000189dbe57

Given a list of digits, return the smallest number that could be formed from these digits, using the digits only once (ignore duplicates).

```JS
function minValue(values){

let arr = [...new Set(values)]

return parseInt(  arr.sort((a,b)=>a-b).join(''))


}
minValue([4, 7, 5, 7])
```


### Thinkful - String Drills: Repeater
https://www.codewars.com/kata/thinkful-string-drills-repeater/train/javascript/5b58e5004a317ae08d000040

Write a function named repeater() that takes two arguments (a string and an integer), and returns a new string where the input string is repeated that many times.

```JS
function repeater(str, n){
  return str.repeat(n)
}
```

### Responsible Drinking
https://www.codewars.com/kata/5aee86c5783bb432cd000018/train/javascript/5f98c141c230710028fbaadc

Codewars Bar recommends you drink 1 glass of water per standard drink so you're not hungover tomorrow morning.

Your fellow coders have bought you several drinks tonight in the form of a string. Return a string suggesting how many glasses of water you should drink to not be hungover.

```JS
function hydrate(s) {

let split =  s.split(' ')

let num =  split.filter(a => !isNaN(a) ? Number(a) : null)

let final =  num.map(a => Number(a)).reduce((a,b)=> a+b)

return (final == 1)? `${final} glass of water` : `${final} glasses of water`

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

## You're a square!
https://www.codewars.com/kata/54c27a33fb7da0db0100040e/train/javascript/5c258c9eb26767341100015f

```JS
var isSquare = function(n){
let sq =  Math.sqrt(n).toFixed(4)

return (sq * sq == n)? true : false
}
```

## Exclamation marks series #13: Count the number of exclamation marks and question marks, return the product
https://www.codewars.com/kata/57fb142297e0860073000064/train/javascript/5f39b3ce527185003250b903

```JS
function product(s){

if (!s.length){
  return 0
}else{

let ex = s.split('').map(a => a.match('!')? true : false).reduce((a,b)=> a+b)

let quest = s.split('').map(a => a.match('^[?]+$')? true : false).reduce((a,b)=> a+b)

return  quest*ex
  }

  
}
product('!!??')
```

## Even or Odd - Which is Greater?
https://www.codewars.com/kata/57f7b8271e3d9283300000b4/train/javascript

```JS
function evenOrOdd(str) {


let arr = str.split('')

let even = arr.filter(a => a%2 == 0)
let odd = arr.filter(a => a%2 > 0)

let oddSum = odd.map(a => Number(a)).reduce((a,b)=> a+b)

let evenSum = even.map(a => Number(a)).reduce((a,b)=> a+b)

return (oddSum == evenSum) ? 'Even and Odd are the same' : (oddSum > evenSum) ?  'Odd is greater than Even' : 'Even is greater than Odd' 

}
```

## Fix string case
https://www.codewars.com/kata/5b180e9fedaa564a7000009a/train/javascript/5f3b1f44e36fd40019cc8967

```JS
function solve(s){
let up = 0
let low = 0

 s.split('').map(a => a == a.toUpperCase()? up++ : low++)

 return (up > low)? s.toUpperCase() : s.toLowerCase()

}
```


## Small enough? - Beginner
https://www.codewars.com/kata/57cc981a58da9e302a000214/train/javascript/5f86510085311d000f84b29f
You will be given an array and a limit value. You must check that all values in the array are below or equal to the limit value. If they are, return true. Else, return false.

```JS
function smallEnough(arr, limit){
let m = arr.map((a) => (a <= limit)? true : false)

let sum =  m.reduce((a,b) => a+b)

return (sum ==  arr.length)? true : false



}
```

## Is this a triangle?
https://www.codewars.com/kata/56606694ec01347ce800001b/train/javascript
Implement a method that accepts 3 integer values a, b, c. The method should return true if a triangle can be built with the sides of given length and false in any other case.


```JS
function isTriangle(a,b,c){
let arr = [a,b,c].sort()

return (arr[0] + arr[1] > arr[2]) ? true : false
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

## Find the middle element
https://www.codewars.com/kata/545a4c5a61aa4c6916000755/train/javascript/5c258cc50b744390d9000130

As a part of this Kata, you need to create a function that when provided with a triplet, returns the index of the numerical element that lies between the other two elements.

```JS
var gimme = function (arr) {

return arr.findIndex(number => 
number == arr.filter(a =>  a < Math.max(...arr) && a > Math.min(...arr)))

};
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

## String ends with?
https://www.codewars.com/kata/51f2d1cafc9c0f745c00037d/train/javascript/5d77ddd1091c5e00112cd3b6
Complete the solution so that it returns true if the first argument(string) passed in ends with the 2nd argument (also a string).

```JS
function solution(str, ending){
  
return str.endsWith(ending)
  
}
solution('abcde', 'cde')
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

## Return a string's even characters
https://www.codewars.com/kata/566044325f8fddc1c000002c/train/javascript

Write a function that returns a sequence (index begins with 1) of all the even characters from a string. If the string is smaller than two characters or longer than 100 characters, the function should return "invalid string".

```JS
function evenChars(str) {

return (str.length< 2 || str.length > 100 ) ? "invalid string" 

  : str.split('').filter((a,b) => b%2)
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



