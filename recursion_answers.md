## Define and compare recursion and iteration

Recursion is when you call the same function inside of that function to simplify
a problem, and iteration is when you use loops to iterate to simplify a problem.

## Name five algorithms that are commonly implemented by recursion.

Fibonacci sequence, factorial of a number, greatest common divisor, recursive binary
search, linked list print.

## When should you use recursion, and when should you avoid recursion? Give examples for each.

When there are known cases that cause the function to crash or do an infinite loop
its better to use recursion. You should avoid recursion when time is a factor,
recursion runs slower than if iteration was used.

## Compare the recursive and iterative solutions to the three algorithms from the checkpoint (factorial, maximum, and fibonacci). What is similar, and what is different?

They all have base cases that filter the data coming through, they all used if/else
statements, and for loops.

## Given a multi-dimensional collection (such as an array) where the number of dimensions is unknown, write a recursive algorithm to count the number of items in the entire collection.
```
var arrayOfArrays = [[1,2,3],[4,5,6],[7, [8, 9],[[10, 11, 12],[13, 14, 15], 16]]];
var count = 0;

function countArrayItems(arr){
  if(!Array.isArray(arr)){
     count++;
  } else {
    for(var i = 0; i < arr.length; i++){
      countArrayItems(arr[i]);
    }
  }
  return count;
}

console.log(countArrayItems(arrayOfArrays));
```

## A palindrome is a word or phrase whose spelling is the same either direction (e.g., racecar). Write a recursive algorithm to determine if a given word or phrase is a palindrome.
```
function CheckPalindrom(word){
  if (word.length <= 1) {
    return true;
  }
  else if (word[0] === word[word.length -1]) {
    return CheckPalindrom(word.slice(1, word.length -1) );
  }
  return false;
};

console.log(CheckPalindrom("racecar"));
console.log(CheckPalindrom("bloc!"));
console.log(CheckPalindrom("madam"));
```

## Google Easter Egg: Google the term "recursion". Google will prompt you with "Did you mean: recursion". Explain why this behavior exhibits properties of recursion.

This is like recursion because we keep clicking on "did you mean" and when we
do that its like we are running the same function again and again and again.
