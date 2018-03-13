
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
