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

## Merge two sorted arrays into one
https://www.codewars.com/kata/5899642f6e1b25935d000161/train/javascript/6055528fc53bb40023224e5b

```JS
function mergeArrays(arr1, arr2) {
  
let newArr =  arr1.concat(arr2)

return [...new Set(newArr)].sort((a,b) => a-b)

}
```

## Get Planet Name By ID
https://www.codewars.com/kata/515e188a311df01cba000003/train/javascript/6049679f45de11001039f7e5

The function is not returning the correct values. Can you figure out why?

```JS
function getPlanetName(id){
  var name;
  switch(id){
 
    case 1:
      return 'Mercury'
       
    case 2:
      return 'Venus'
       
    case 3:
      return 'Earth'
       
    case 4:
      return 'Mars'
       
    case 5:
      return 'Jupiter'
       
    case 6:
      return 'Saturn'
       
    case 7:
      return 'Uranus'
       
    case 8:
      return 'Neptune'
      
  }
  
  return name;
}
```

### Is it even
https://www.codewars.com/kata/555a67db74814aa4ee0001b5/train/javascript

In this Kata we are passing a number (n) into a function.

Your code will determine if the number passed is even (or not).

The function needs to return either a true or false.

Numbers may be positive or negative, integers or floats.

Floats are considered UNeven for this kata.

```JS
function testEven(n) {
   return (n%2 == 0)? true : false
}
testEven(1)
```

### Short Long Short
https://www.codewars.com/kata/50654ddff44f800200000007/train/javascript

Given 2 strings, a and b, return a string of the form short+long+short, with the shorter string on the outside and the longer string on the inside. The strings will not be the same length, but they may be empty ( zero length ).

```JS
function solution(a, b){
  return (b.length > a.length) ? `${a}${b}${a}` : `${b}${a}${b}`
}
```


### Grasshopper - Terminal game move function
https://www.codewars.com/kata/563a631f7cbbc236cf0000c2/train/javascript

In this game, the hero moves from left to right. The player rolls the die and moves the number of spaces indicated by the die two times.

```JS
function move (pos, roll) {
  return pos + roll * 2 
}
```

### L1: Set Alarm
https://www.codewars.com/kata/568dcc3c7f12767a62000038/train/javascript

Write a function named setAlarm which receives two parameters. The first parameter, employed, is true whenever you are employed and the second parameter, vacation is true whenever you are on vacation.

```JS
function setAlarm(emp, vac){
  return (emp == true && vac == false) ? true : false
}
```


### Grasshopper - Check for factor
https://www.codewars.com/kata/55cbc3586671f6aa070000fb/train/javascript

```JS
function checkForFactor (base, factor) {
  return (base % factor === 0) ? true : false
}
checkForFactor(653,7)
```

### 5 without numbers !!
https://www.codewars.com/kata/59441520102eaa25260000bf/train/javascript

Write a function that always returns 5

Sounds easy right? Just bear in mind that you can't use any of the following characters: 0123456789*+-/

```JS
function unusualFive() {
  return ['a','a','a','a','a'].length
}
unusualFive()
```


### What's the real floor?
https://www.codewars.com/kata/574b3b1599d8f897470018f6/train/javascript

Write a function that given a floor in the american system returns the floor in the european system.

With the 1st floor being replaced by the ground floor and the 13th floor being removed, the numbers move down to take their place. In case of above 13, they move down by two because there are two omitted numbers below them.

Basements (negatives) stay the same as the universal level.

```JS
function getRealFloor(n) {

  if(n<=0){
    return n
  } else if(n<13){
    return n-1
  } else if(n>13){
    return n-2
  }

}

getRealFloor(1)
```

### Sum The Strings
https://www.codewars.com/kata/5966e33c4e686b508700002d/train/javascript

Create a function that takes 2 nonnegative integers in form of a string as an input, and outputs the sum (also as a string):

```JS
function sumStr(a,b) {

return (Number(a) + Number(b)).toString()

}
sumStr("4","5")
```


### Powers of 2
https://www.codewars.com/kata/57a083a57cb1f31db7000028/train/javascript

Complete the function that takes a non-negative integer n as input, and returns a list of all the powers of 2 with the exponent ranging from 0 to n (inclusive).

```JS

function powersOfTwo(n){
  var result = [];
  for (var i = 0; i <= n; i++) {
    result.push(Math.pow(2, i));
  }
  return result;
}

```



### Well of Ideas 
https://www.codewars.com/kata/57f222ce69e09c3630000212/train/javascript/5dfb64151f177f00192c3a7d

In this kata you need to check the provided array (x) for good ideas 'good' and bad ideas 'bad'. If there are one or two good ideas, return 'Publish!', if there are more than 2 return 'I smell a series!'. If there are no good ideas, as is often the case, return 'Fail!'.

```JS 
function well(test){

let num =  test.filter(a => a == 'good').length

if(num > 0 && num <= 2){
  return 'Publish!'
}else if(num > 2){
  return 'I smell a series!'
}else{
  return 'Fail!'
}
  
}
```


### Lario and Muigi Pipe Problem
https://www.codewars.com/kata/56b29582461215098d00000f/train/javascript

Given the a list of numbers, return the list so that the values increment by 1 for each index up to the maximum value.
```JS
function pipeFix(num){

let arr = []
let stop = num.pop()

if(num == false){
  return [2]
}else{
  for (let i=num[0]; i <= stop; i++){
      arr.push(i)
    }
    return arr
  }
}


pipeFix([1,7])
```


### Thinkful - Logic Drills: Traffic light
https://www.codewars.com/kata/58649884a1659ed6cb000072/train/javascript/60b548c23961d20055d96e69

You're writing code to control your town's traffic lights. You need a function to handle each change from green, to yellow, to red, and then to green again.

Complete the function that takes a string as an argument representing the current state of the light and returns a string representing the state the light should change to.

```JS
function updateLight(cur) {
  
  if(cur == 'green'){
    return 'yellow'
  }else if(cur =='yellow'){
    return 'red'
  }else if(cur =='red'){
    return 'green'
  }

}
```

### Grasshopper - Terminal game combat function
https://www.codewars.com/kata/586c1cf4b98de0399300001d/train/javascript

Create a combat function that takes the player's current health and the amount of damage recieved, and returns the player's new health. Health can't be less than 0.

```JS
function combat(health, damage) {
   return (health - damage < 0) ? 0 : health - damage
}
```


### The Wide-Mouthed frog!
https://www.codewars.com/kata/57ec8bd8f670e9a47a000f89/train/javascript

Your goal in this kata is to create complete the mouth_size method this method take one argument animal which corresponds to the animal encountered by frog. If this one is an alligator (case insensitive) return small otherwise return wide.

```JS
function mouthSize(animal) {
  return (animal.toLowerCase() === 'alligator')? "small" : "wide"
}
mouthSize('alligator')
```


### Generate range of integers
https://www.codewars.com/kata/55eca815d0d20962e1000106/train/javascript/60ad04b931f2850049046153

Implement a function named generateRange(min, max, step), which takes three arguments and generates a range of integers from min to max, with the step. The first integer is the minimum value, the second is the maximum of the range and the third is the step. (min < max)

```JS
function generateRange(min, max, step){

  let arr = []

  for(i = min; i <= max; i += step){
    arr.push(i)
  }

   return arr

}

generateRange(1, 10, 3)
```

### Is it a palindrome?
https://www.codewars.com/kata/57a1fd2ce298a731b20006a4/train/javascript/601322d38c0712002c5ac457

Write function isPalindrome that checks if a given string (case insensitive) is a palindrome.

```JS
function isPalindrome(x) {
  let reverse = x.toLowerCase().split('').reverse().join('')

  return (reverse == x.toLowerCase()) ? true : false


}
isPalindrome('nope')
```


### Drink about
https://www.codewars.com/kata/56170e844da7c6f647000063/train/javascript/6029ab05213d22002b975f39

Make a function that receive age, and return what they drink.

```JS
function peopleWithAgeDrink(old){


switch(true){
 case old < 14: 
  return 'drink toddy';

  case old < 18: 
    return 'drink coke';

  case old < 21: 
    return 'drink beer';

  case old >= 21: 
    return 'drink whisky';

}


}peopleWithAgeDrink(30)
```

## Is the string uppercase?
https://www.codewars.com/kata/56cd44e1aa4ac7879200010b/train/javascript/5fa5ad844a969500327dc354

```JS
String.prototype.isUpperCase = function() {

return this
.split('')
.map(a => (a == a.toUpperCase())? true : false)
.includes(false) ? false : true

}
```

## N-th Power
https://www.codewars.com/kata/57d814e4950d8489720008db/train/javascript/6042eb3c6e8341001d23c186

You are given an array with positive numbers and a non-negative number N. You should find the N-th power of the element in the array with the index N. If N is outside of the array, then return -1. Don't forget that the first element has the index 0.

```JS
function index(arr, n){
return (arr.length <= n) ? -1 : Math.pow(arr[n], n) 
}
```

## Removing Elements
https://www.codewars.com/kata/5769b3802ae6f8e4890009d2/train/javascript

Take an array and remove every second element from the array. Always keep the first element and start removing with the next element.

```JS
function removeEveryOther(arr){
return arr.filter((a,i) => i%2 == 0)

}
```

## All Star Code Challenge #18
https://www.codewars.com/kata/5865918c6b569962950002a1/train/javascript/5f908924fb73960014526881

This Kata is intended as a small challenge for my students

All Star Code Challenge #18

Create a function called that accepts 2 string arguments and returns an integer of the count of occurrences the 2nd argument is found in the first one.

If no occurrences can be found, a count of 0 should be returned.

```JS
function strCount(str, letter){  

 return str.split('').filter(a => a == letter).length
}

```

## Sort and Star
https://www.codewars.com/kata/57cfdf34902f6ba3d300001e/train/javascript/60147576e7b8680008133762

You will be given a vector of strings. You must sort it alphabetically (case-sensitive, and based on the ASCII values of the chars) and then return the first value.

The returned value must be a string, and have "***" between each of its letters.

You should not remove or add elements from/to the array.

```JS
function twoSort(s) {

return s.sort().shift().split('').map(a => a +  '***').join('').slice(0,-3)

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

## Is he gonna survive?
https://www.codewars.com/kata/is-he-gonna-survive/train/javascript/5dfb605e0d5bc90028975f0b

A hero is on his way to the castle to complete his mission. However, he's been told that the castle is surrounded with a couple of powerful dragons! each dragon takes 2 bullets to be defeated, our hero has no idea how many bullets he should carry.. Assuming he's gonna grab a specific given number of bullets and move forward to fight another specific given number of dragons, will he survive?

Return True if yes, False otherwise :)

```
function hero(bullets, dragons){
return (bullets >= dragons*2)? true : false
}
```

## DNA to RNA Conversion
https://www.codewars.com/kata/5556282156230d0e5e000089/train/javascript

Create a function which translates a given DNA string into RNA.

```JS
function DNAtoRNA(dna) {
  return dna.split('').map(a => a.replace('T','U')).join('')

}
```


## Twice as old
https://www.codewars.com/kata/5b853229cfde412a470000d0/train/javascript

Сalculate how many years ago the father was twice as old as his son (or in how many years he will be twice as old).

```JS
function twiceAsOld(dadYearsOld, sonYearsOld) {
  return Math.abs((sonYearsOld*2)-dadYearsOld)
}

```


## Exclamation marks series #11: Replace all vowel to exclamation mark in the sentence
https://www.codewars.com/kata/57fb09ef2b5314a8a90001ed/train/javascript/5dfb62547a364400145f0c89

```JS
function replace(str){

return str.replace(/[aeiouAEIOU]/gi, "!")
  
}
```

### The Feast of Many Beasts
https://www.codewars.com/kata/5aa736a455f906981800360d/train/javascript/5f3d805268cd2b00249afeb7

```JS
function feast(beast, dish) {
let beastL = beast.split('').pop()
let dishL = dish.split('').pop()

return (beast[0] == dish[0] && beastL == dishL ) ? true : false


}
```


### Quarter of the year
Given a month as an integer from 1 to 12, return to which quarter of the year it belongs as an integer number.

```JS
const quarterOf = (month) => {
  
  switch(month){
        case 1:
       case 2:
       case 3:
    return 1;
    break;

       case 4:
       case 5:
       case 6:
    return 2;
    break;

       case 7:
       case 8:
       case 9:
    return 3;
    break;
       case 10:
       case 11:
       case 12:
    return 4;
    break;

  default:
  return 'not sure';

  }
  
}
quarterOf(1)
```

## I love you, a little , a lot, passionately ... not at all
https://www.codewars.com/kata/57f24e6a18e9fad8eb000296/train/javascript/5c25849166559804690002ba

When the last petal was torn there were cries of excitement, dreams, surging thoughts and emotions.

Your goal in this kata is to determine which phrase the girls would say for a flower of a given number of petals, where nb_petals > 0.

```JS
function howMuchILoveYou(n) {
       let arr = ['I love you',
'a little',
'a lot',
'passionately',
'madly',
'not at all'] 
  
  
  return (n% 6 == 0)? 'not at all' : arr[n%6-1]
}
```

### Grasshopper - Grade book
https://www.codewars.com/kata/55cbd4ba903825f7970000f5/train/javascript/5fa5bbd7662218001932dc7b

Complete the function so that it finds the mean of the three scores passed to it and returns the letter value associated with that grade.

```JS
function getGrade (s1, s2, s3) {

let arr = []

arr.push(s1,s2,s3)

let score =  arr.reduce((a,b) => a+b)/3

switch(true){
  case 90 <= score: return 'A'
 
  case 80 <= score: return 'B'

  case 70 <= score: return 'C'
 
  case 60 <= score: return 'D'

  case  0 <= score: return 'F'

    }

}

```

## Count by X
https://www.codewars.com/kata/5513795bd3fafb56c200049e/train/javascript

Create a function with two arguments that will return an array of the first (n) multiples of (x).

Assume both the given number and the number of times to count will be positive numbers greater than 0.

Return the results as an array (or list in Python, Haskell or Elixir).

```JS
function countBy(x, n) {

arr= []

for(i=x; i<=x*n; i+=x ){
arr.push(i)
 
}
return arr

}
```

## Can we divide it?
https://www.codewars.com/kata/5a2b703dc5e2845c0900005a/train/javascript

Your task is to create functionisDivideBy (or is_divide_by) to check if an integer number is divisible by each out of two arguments.

```JS
function isDivideBy(num, a, b) {
  return (num%a == 0 && num%b == 0) ? true: false
}
```


##Fake Binary
https://www.codewars.com/kata/fake-binary/train/javascript/5d77e95d760cfd001e1c52a3

Given a string of digits, you should replace any digit below 5 with '0' and any digit 5 and above with '1'. Return the resulting string.

```JS
function fakeBin(num){
return num.split('').map(a => (a>=5) ?'1' : '0').join('')
}
```

## altERnaTIng cAsE <=> ALTerNAtiNG CaSe
https://www.codewars.com/kata/56efc695740d30f963000557/train/javascript/5deee3a0df8a1200163a9d65

Define String.prototype.toAlternatingCase (or a similar function/method such as to_alternating_case/toAlternatingCase/ToAlternatingCase in your selected language; see the initial solution for details) such that each lowercase letter becomes uppercase and each uppercase letter becomes lowercase. For example:

```JS
String.prototype.toAlternatingCase = function () {
    return this.split('').map(a => a === a.toLowerCase()? a.toUpperCase():  a.toLowerCase() ).join('')
}
```


## Find numbers which are divisible by given number
https://www.codewars.com/kata/55edaba99da3a9c84000003b/train/javascript/5f7c8ce6adfe0d000f67e7f1

Complete the function which takes two arguments and returns all numbers which are divisible by the given divisor. First argument is an array of numbers and the second is the divisor.

```JS
function divisibleBy(numbers, divisor){
return numbers.map(a => (a == 0)? a :(a%divisor == 0 )? a: null ).filter(a => a !== null)
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

## Hello, Name or World!
https://www.codewars.com/kata/57e3f79c9cb119374600046b/train/javascript

Define a method hello that returns "Hello, Name!" to a given name, or says Hello, World! if name is not given (or passed as an empty String).

Assuming that name is a String and it checks for user typos to return a name with a first capital letter (Xxxx).

```JS
function hello(name) {


  if( name == null || !name.length){
    return 'Hello, World!'
  }else{

let arr = name.toLowerCase().split('')
let first =  arr[0][0].toUpperCase()
arr.splice(0,1)

 let newName  = first.split('').concat(arr).join('')


return !name.length ? 'Hello, World!' : `Hello, ${newName}!`  

  }
}
hello()
```

## Pre-FizzBuzz Workout #1
https://www.codewars.com/kata/569e09850a8e371ab200000b/train/javascript/5f864e21c00bae002e4b3f4a

Your inputs: a positive integer, n, greater than or equal to one. n is provided, you have NO CONTROL over its value.

```JS
function preFizz(n) {
let arr = []


for(i=1; i<=n; i++){
  arr.push(i)
}
return arr
  
}
```

## Grader
https://www.codewars.com/kata/53d16bd82578b1fb5b00128c/train/javascript/5f25b9a223c9aa002e1bdc4f

Create a function that takes a number as an argument and returns a grade based on that number.

```JS
function grader(score) {
   switch(true){
    case  score > 1.00 : 
    return 'F';
      break;

    case  score >= 0.9 : 
    return 'A';
      break;

    case  score >= 0.8 : 
    return 'B';
      break;

     case score >= 0.7 : 
     return 'C';
      break;

    case  score >= 0.6 : 
    return 'D';
      break;
    
    case  score <= 0.59 : 
    return 'F';
      break;
 

  };
}
```

## NBA full 48 minutes average
https://www.codewars.com/kata/587c2d08bb65b5e8040004fd/train/javascript

An NBA game runs 48 minutes (Four 12 minute quarters). Players do not typically play the full game, subbing in and out as necessary. Your job is to extrapolate a player's points per game if they played the full 48 minutes.

Write a function that takes two arguments, ppg (points per game) and mpg (minutes per game) and returns a straight extrapolation of ppg per 48 minutes rounded to the nearest tenth. Return 0 if 0.

```JS
function pointsPer48(ppg, mpg) {
  
  let pts = Number( ((48/mpg)* ppg).toFixed(1))
  
return (isNaN(pts)) ? 0: pts


}
```


## Count of positives / sum of negatives
https://www.codewars.com/kata/576bb71bbbcf0951d5000044/train/javascript/5ab4598f6a176b73dc0000b4

Given an array of integers.

Return an array, where the first element is the count of positives numbers and the second element is sum of negative numbers.

If the input array is empty or null, return an empty array.

```JS
function countPositivesSumNegatives(arr) {

  if(arr == null || !arr.length ){
    return []
  }else{

    let pos =  arr.filter(a => a>0 ).length

    let neg =  arr.filter(a => a<0 ).reduce((a,b)=> a+b);

    return [pos,neg]
  }
}
```



## L1: Bartender, drinks!
https://www.codewars.com/kata/568dc014440f03b13900001d/train/javascript/5f3e927d28bb8e001046fe14

Write a function getDrinkByProfession/get_drink_by_profession() that receives as input parameter a string, and produces outputs according to the following table:

```JS
function getDrinkByProfession(param){

switch(param.toLowerCase()){
    case "jabroni" : return	"Patron Tequila"

    case "school counselor": return "Anything with Alcohol"

    case "programmer": return "Hipster Craft Beer"

    case "bike gang member": return "Moonshine" 

    case "politician": return "Your tax dollars" 

    case "rapper": return "Cristal" 

  default: return "Beer"

}
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

## Area or Perimeter
https://www.codewars.com/kata/5ab6538b379d20ad880000ab/train/javascript
You are given the length and width of a 4-sided polygon. The polygon can either be a rectangle or a square.
If it is a square, return its area. If it is a rectangle, return its perimeter.

```JS
const areaOrPerimeter = function(l , w) {
 return (l == w) ? l * w : l*2 + w*2
};
areaOrPerimeter(4,6)
```

## Third Angle of a Triangle
https://www.codewars.com/kata/5a023c426975981341000014/train/javascript
You are given two angles (in degrees) of a triangle.

```
function otherAngle(a, b) {
  return 180-(a+b)
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

## Will there be enough space?
https://www.codewars.com/kata/5875b200d520904a04000003/train/javascript/5cd81813accbd30018210051

Bob is working as a bus driver. However, he has become extremely popular amongst the city's residents. With so many passengers wanting to get aboard his bus, he sometimes has to face the problem of not enough space left on the bus! He wants you to write a simple program telling him if he will be able to fit all the passengers.

```JS
function enough(cap, on, wait) {
let dif = Math.abs((cap - on)-wait)

return (on + wait < cap) ? 0: dif
}
enough(10,5,5)
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

