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



