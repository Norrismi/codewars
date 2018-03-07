5 kyu
==========


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