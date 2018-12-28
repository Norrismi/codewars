5 kyu
==========

## Moving Zeros To The End

https://www.codewars.com/kata/moving-zeros-to-the-end/train/javascript/5ace60f73a33e62d1c00021a

```JS
var moveZeros = function (arr) {
return arr.filter(a => a !== 0 ).concat(arr.filter(a => a === 0 ))
}
```

## Simple Pig Latin

https://www.codewars.com/kata/simple-pig-latin/train/javascript/5a7a6ccbfd8c06d91100005c

Move the first letter of each word to the end of it, then add "ay" to the end of the word. Leave punctuation marks untouched.

```JS
function pigIt(str){
  var words = str.split(' ')
  var backward = words.map(function(word){
        return word.substr(1) + word.charAt(0) + 'ay'
  })
  return backward.join(' ')
}

```

## Regex Password Validation
https://www.codewars.com/kata/regex-password-validation/train/javascript/5c2675e5f3e92460b5ab4be9
You need to write regex that will validate a password to make sure it meets the following criteria:

At least six characters long
contains a lowercase letter
contains an uppercase letter
contains a number
Valid passwords will only be alphanumeric characters.

```JS 
function validate(password) {
  return /(^(?=.*[a-z])(?=.*[A-Z])(?=.*\d)[a-zA-Z\d]{6,}$)/.test(password);
}
```



