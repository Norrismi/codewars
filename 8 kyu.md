# 8 kyu

## Find Maximum and Minimum Values of a List

https://www.codewars.com/kata/find-maximum-and-minimum-values-of-a-list/train/javascript/5a73965bba1bb5b5ea000089

Your task is to make two functions, max and min (maximum and minimum in PHP) that take a(n) array/vector of integers list as input and outputs, respectively, the largest and lowest number in that array/vector.

```JS
var min = function(list){

return Math.min(...list);
}

var max = function(list){

return Math.max(...list);

}
```

## Find something in an Array
https://www.codewars.com/kata/find-something-in-an-array/train/javascript/5b58e26c05f04b70ef00003e

Create a find function that takes a string and an array as arguments. If the string is in the array, return true.

```JS
var find = function(string, array) {
  return (array.includes(string))? true : false
};
```

##Fake Binary
https://www.codewars.com/kata/fake-binary/train/javascript/5d77e95d760cfd001e1c52a3

Given a string of digits, you should replace any digit below 5 with '0' and any digit 5 and above with '1'. Return the resulting string.

```JS
function fakeBin(num){
return num.split('').map(a => (a>=5) ?'1' : '0').join('')
}
```

## A Needle in the Haystack

https://www.codewars.com/kata/a-needle-in-the-haystack/train/javascript/5ace59ee23c8186cae0001c6

Can you find the needle in the haystack?

Write a function findNeedle() that takes an array full of junk but containing one "needle"

After your function finds the needle it should return a message (as a string) that says:

"found the needle at position " plus the index it found the needle.

```JS

function findNeedle(haystack) {
 return haystack.includes('needle')?  `found the needle at position ${haystack.indexOf('needle')}`: null
}
```

## Transportation on vacation
https://www.codewars.com/kata/transportation-on-vacation/train/javascript/5c158d137f06271801000016

After a hard quarter in the office you decide to get some rest on a vacation. So you will book a flight for you and your girlfriend and try to leave all the mess behind you.

You will need a rental car in order for you to get around in your vacation. The manager of the car rental makes you some good offers.

Every day you rent the car costs $40. If you rent the car for 7 or more days, you get $50 off your total. Alternatively, if you rent the car for 3 or more days, you get $20 off your total.

Write a code that gives out the total amount for different days(d).

```JS
function rentalCarCost(d) {
let total = 40*d

return (total >=280)? total-50:
( total>=120)?  total-20: total
}
```

## Abbreviate a Two Word Name
https://www.codewars.com/kata/abbreviate-a-two-word-name/train/javascript/5c259198dd392c2c7800014f

Write a function to convert a name into initials. This kata strictly takes two words with one space in between them.

The output should be two capital letters with a dot seperating them.

It should look like this:

Sam Harris => S.H

Patrick Feeney => P.F

```JS
function abbrevName(name){
  let arr =  name.split(' ')
  let first = arr[0][0].toUpperCase()
  let last = arr[1][0].toUpperCase()
  return `${first}.${last}`

}

```
## Remove Duplicates From List
https://www.codewars.com/kata/remove-duplicates-from-list/train/javascript/5b58e4456dc79e9f7000003c
Define a function that removes duplicates from an array of numbers and returns it as a result.

The order of the sequence has to stay the same.

```JS

function distinct(arr) {
   return [...new Set(arr)]
   
}
distinct([1,3,1,3,4,5,6])
```

## Grasshopper - If/else syntax debug
https://www.codewars.com/kata/grasshopper-if-slash-else-syntax-debug/train/javascript/5cd62b0e385bfb002846181b
If/else syntax debug
While making a game, your partner, Greg, decided to create a function to check if the user is still alive called checkAlive/CheckAlive. Unfortunately, Greg made some errors while creating the function.

checkAlive/CheckAlive should return true if the player's health is greater than 0 or false if it is 0 or below.

checkAlive receives one parameter health which will always be a whole number between -10 and 10.
```JS
function checkAlive (health) {
 return (health <= 0) ? false : true

}
checkAlive(5)

```

## Bin to Decimal
https://www.codewars.com/kata/bin-to-decimal/train/javascript/5c38b74a23e1fc2b6e219f8c

Complete the function which converts a binary number (given as a string) to a decimal number.
```JS
function binToDec(bin){
  return parseInt(bin,2)
}
```

## Filter out the geese

https://www.codewars.com/kata/filter-out-the-geese/train/javascript/5c3f452ece5d8242a03fe16a

Write a function, gooseFilter/goose_filter/GooseFilter, that takes an array of strings as an argument and returns a filtered array containing the same elements but with the 'geese' removed.

```JS
function gooseFilter (birds) {
  let geese = ["African", "Roman Tufted", "Toulouse", "Pilgrim", "Steinbacher"];
  
 return birds.filter(a => !geese.includes(a))

}
```

## Squash the bugs
https://www.codewars.com/kata/squash-the-bugs/train/javascript/5d1a6810c459270017c17b0d
Simple challenge - eliminate all bugs from the supplied code so that the code runs and outputs the expected value. Output should be the length of the longest word, as a number.

There will only be one 'longest' word.

```JS
function findLongest(str){
  
  return Math.max(...str.split(' ').map(a => a.length))
   
}
findLongest("Lets all go on holiday")
```

## get character from ASCII Value
https://www.codewars.com/kata/get-character-from-ascii-value/train/javascript/5cc8e9c20cbae00013a01a0a
Get character from ASCII Value
Write a function getChar/GetChar/get_char which takes a number and returns the corresponding ASCII char for that value.

```JS
function getChar(c){

  return String.fromCharCode(c)
}
getChar(65)
```

## Are You Playing Banjo?
https://www.codewars.com/kata/are-you-playing-banjo/train/javascript/5c282436662e2f00091333a7

Create a function which answers the question "Are you playing banjo?".
If your name starts with the letter "R" or lower case "r", you are playing banjo!

The function takes a name as its only argument, and returns one of the following strings:

name + " plays banjo" 
name + " does not play banjo"

```JS
function areYouPlayingBanjo(name) {
  let cut = name.split('')
  
  return (cut[0] == 'R' || cut[0] == 'r')
  ? `${name} plays banjo` 
  : `${name} does not play banjo`
  
}
```

## Correct the mistakes of the character recognition software
https://www.codewars.com/kata/correct-the-mistakes-of-the-character-recognition-software/train/javascript/5c338013fdcefd647d71c803

Character recognition software is widely used to digitise printed texts. Thus the texts can be edited, searched and stored on a computer.

When documents (especially pretty old ones written with a typewriter), are digitised character recognition softwares often make mistakes.

```JS
function correct(string){

let str = string.split('')
return str.map(a => (a === '5')
  ? 'S': (a === '0')
  ? 'O': (a === '1')
  ? 'I': a).join('')
 }

```

## Beginner - Lost Without a Map
https://www.codewars.com/kata/beginner-lost-without-a-map/train/javascript/5d13fb7ec4592700219374a2
Given an array of integers, return a new array with each value doubled.

```JS
function maps(x){
 return x.map(a => a*2)
}
```

## Capitalization and Mutability
https://www.codewars.com/kata/capitalization-and-mutability/train/javascript/5d1a3ffd0e313ea65c52b6d0
Your coworker was supposed to write a simple helper function to capitalize a string (that contains a single word) before they went on vacation.

Unfortunately, they have now left and the code they gave you doesn't work. Fix the helper function they wrote so that it works as intended (i.e. make the first character in the string "word" upper case).

Don't worry about numbers, special characters, or non-string types being passed to the function. The string lengths will be from 1 character up to 10 characters, but will never be empty.

```JS
function capitalizeWord(word) {
  let sp = word.split('')
  let start = sp[0].toUpperCase()

    sp.splice(0,1)
    sp.unshift(start)
    return sp.join('')
  
}
capitalizeWord('glasses')
```

## Return Negative
https://www.codewars.com/kata/return-negative/train/javascript/5abebd2830488fa54d00011e

In this simple assignment you are given a number and have to make it negative. But maybe the number is already negative?

Example:

makeNegative(1); // return -1
makeNegative(-5); // return -5
makeNegative(0); // return 0

```JS
function makeNegative(num) {
  return (num > 0) ? parseInt(`-${num}`,10) : num

}
```

##Sum Mixed Array
https://www.codewars.com/kata/sum-mixed-array/train/javascript/5d1ba54b52d8e1001138251c

Given an array of integers as strings and numbers, return the sum of the array values as if all were numbers.

```JS
function sumMix(arr){

return arr.map(a => parseInt(a)).reduce((a,b) => a+b)

}
```

## Will there be enough space?

https://www.codewars.com/kata/will-there-be-enough-space/train/javascript/5cd62c9ef446b00012c1c449

You have to write a function that accepts three parameters:

cap is the amount of people the bus can hold excluding the driver.
on is the number of people on the bus.
wait is the number of people waiting to get on to the bus.
If there is enough space, return 0, and if there isn't, return the number of passengers he can't take.

```JS
function enough(cap, on, wait) {
  total = on + wait
  
  return (on + wait > cap)? total - cap : 0 
}
enough(10,5,5)
```


## Jenny's secret message

https://www.codewars.com/kata/jennys-secret-message/train/javascript/5a9eb286fd8c06475f000113

Jenny has written a function that returns a greeting for a user. However, she's in love with Johnny, and would like to greet him slightly different. She added a special case to her function, but she made a mistake.

```JS
function greet(name){
  if(name == 'Johnny'){
    return "Hello, my love!"
  }else{
    return "Hello, "+ name+ "!"
  }

}
```

## Simple multiplication
https://www.codewars.com/kata/583710ccaa6717322c000105/train/javascript

This kata is about multiplying a given number by eight if it is an even number and by nine otherwise.

```JS
function simpleMultiplication(num) {
    return (num % 2 == 0) ? num * 8: num * 9
}
```

## If you can't sleep, just count sheeps!!
https://www.codewars.com/kata/if-you-cant-sleep-just-count-sheeps/train/javascript/5b0e9a2d41e66a87390000d7

Given a number, 3 for example, return a string with a murmur: "1 sheep...2 sheep...3 sheep..."

```JS
var countSheep = function (num){
let  text =   ``

for(var i=1; i<=num; i++){
   text += `${i} sheep...`
}
return text
}
```


## Keep up the hoop

https://www.codewars.com/kata/keep-up-the-hoop/train/javascript/5a9d6a66ba1bb55b5800019e

Alex just got a new hula hoop, he loves it but feels discouraged because his little brother is better than him

Write a program where Alex can input (n) how many times the hoop goes round and it will return him an encouraging message :)

-If Alex gets 10 or more hoops, return the string "Great, now move on to tricks".

-If he doesn't get 10 hoops, return the string "Keep at it until you get it".


```JS
function hoopCount (n) {
   if(n>=10){
  return "Great, now move on to tricks"
}   else{
  return "Keep at it until you get it"
}
}

```



## String repeat

https://www.codewars.com/kata/string-repeat/train/javascript/5a9d664a373c2ea4bb00031a

Write a function called repeatStr which repeats the given string string exactly n times.

```JS
function repeatStr (n, str) {
  return str.repeat(n)
  }

```


## Remove String Spaces

https://www.codewars.com/kata/remove-string-spaces/train/javascript/5a850ff40025e96850000091

Simple, remove the spaces from the string, then return the resultant string.

```JS
function noSpace(x){
  return x.split(' ').join('');
}

```

## Calculate BMI
https://www.codewars.com/kata/calculate-bmi/train/javascript/5b606e668f47bdcbe3000035
Write function bmi that calculates body mass index (bmi = weight / height ^ 2).
if bmi <= 18.5 return "Underweight"
if bmi <= 25.0 return "Normal"
if bmi <= 30.0 return "Overweight"
if bmi > 30 return "Obese"

```JS
function bmi(w,h) {
 let bmi = w/(h*h)
    if (bmi <= 18.5){
      greeting = "Underweight"
    }
    else if ( bmi <= 25){
      greeting = "Normal"
    }
    else if ( bmi <= 30){
      greeting = "Overweight"
    }
        else{
      greeting = "Obese"
    }
    return greeting
    
}
```


## Remove First and Last Character

https://www.codewars.com/kata/remove-first-and-last-character/train/javascript/5a7643314a6b34a32f000021

It's pretty straightforward. Your goal is to create a function that removes the first and last characters of a string. You're given one parameter, the original string. You don't have to worry with strings with less than two characters.

```JS
function removeChar(str){
let arr = str.split('')

  arr.shift()
  arr.pop();
  return arr.join('');

};

```


## Even or Odd
https://www.codewars.com/kata/even-or-odd/train/javascript/5a7394ec0025e90a54000063

Create a function that takes an integer as an argument and returns "Even" for even numbers or "Odd" for odd numbers.

```JS
function even_or_odd(integer) {
  if(integer % 2 == 0){
    return "Even"
  }else{
    return "Odd";
  }
}

```

## Multiply



The code does not execute properly. Try to figure out why.

```JS
function multiply(a, b){
  return a * b
}

```

## How good are you really?
https://www.codewars.com/users/Norrismi/completed_solutions

There was a test in your class and you passed it. Congratulations!
But you're an ambitious person. You want to know if you're better than the average student in your class.
You got an array with your colleges' points. Now calculate the average to your points!

Return True if you're better, else False!

Note:
Your points are not included in the array of your classes points. For calculating the average point you may add your point to the given array!

```JS
function betterThanAverage(classPoints, yourPoints) {
  let a = classPoints.reduce((a,b) => a+b)/classPoints.length
  return (yourPoints > a) ? true : false
}
```

### Calculate average
https://www.codewars.com/kata/calculate-average/train/javascript/5aafebaefd5777dfab0000ce

Write function avg which calculates average of numbers in given list.

```JS
function find_average(array) {
  return array.reduce((a,b) => a+b)/array.length
}
```

### Is n divisible by x and y?
https://www.codewars.com/kata/is-n-divisible-by-x-and-y/train/javascript/5baa4a97c22b79f517000273

Create a function isDivisible(n, x, y) that checks if a number n is divisible by two numbers x AND y. All inputs are positive, non-zero digits.

```JS
function isDivisible(n, x, y) {
  return (n%x === 0 && n%y === 0 ) ? true : false
}
```


### Remove exclamation marks
https://www.codewars.com/kata/remove-exclamation-marks/train/javascript/5af60e1186d0756d9500004a

Write function RemoveExclamationMarks which removes all exclamation marks from a given string.

```JS
function removeExclamationMarks(s) {
  return s.replace(/!/g, '')
}

```

Convert a Number to a String!
https://www.codewars.com/kata/convert-a-number-to-a-string/train/javascript/5c1820275065a94a6a00006f
We need a function that can transform a number into a string.

What ways of achieving this do you know?
```JS
function numberToString(num) {
  return num.toString()
}
```

### Opposite Number
https://www.codewars.com/kata/opposite-number/train/javascript/5a78bbb0fd577718e80000b5

Very simple, given a number, find its opposite.

Examples:

1: -1
14: -14
-34: 34

```JS
function opposite(number) {
  return (number > 0)? number-number-number : Math.abs(number)
}
```

### Reverse Words in a String
https://www.codewars.com/kata/reversing-words-in-a-string/train/javascript/5ab53216206a29839e000046

You need to write a function that reverses the words in a given string. A word can also fit an empty string. If this is not clear enough, here are some examples:

As the input may have trailing spaces, you will also need to ignore unneccesary whitespace.

reverse('Hello World') === 'World Hello'
reverse('Hi There.') === 'There. Hi'

```JS
function reverse(str){
  return str.split(' ').reverse().join(' ')
}
```

