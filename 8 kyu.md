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

