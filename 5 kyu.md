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
