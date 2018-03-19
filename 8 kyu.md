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
