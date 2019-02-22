## What is time complexity and what is its relation to algorithms?

Time complexity is how long a function should run and is expressed as a function.
Algorithms and time complexity are related because they both tell you how ling
it takes to do something.  

## What is runtime?

Runtime is the real time that it takes for a function to run. Example would be
1 minute, 2, minutes.

## How is the runtime of an algorithm calculated?

By seeing how long it takes for the algorithm to run.

## Name the six types of algorithm growth rates we saw in this checkpoint and list them in order of most efficient to least efficient. Now Google another algorithmic growth rate not covered and place it in the correct spot in your list.

O(1), O(log n), O(n),  O(n log n), O(n^2), O(2^n), and O(n!)

## Choose one of the algorithmic growth rates from the last question and make a comparison to a real-life situation.

In a class of 100 students, I let someone borrow my pen. If all the students know who has my pen and I don't, I can split the class in half of 50-50 students. If the students tell me I picked the right half, I can then split the students again, and continue doing so until I find the student who borrowed my pen. This is an example of O(log n).

## Determine the time complexity of the following snippet of code. It is commonly known as a linear search.

```
FUNCTION linearSearch(array, target)
 FOR each number in the array
   IF number = target THEN
     RETURN true
   END IF
 END FOR
 RETURN false
END FUNCTION
```
O(n);

## Determine the time complexity of the following snippet of code.

```
FUNCTION foo(array)
 FOR each number in the array
   FOR each number in the array
     print "Hello"
   END FOR
 END FOR
END FUNCTION
```
O(n^2);

## Determine the time complexity of the following snippet of code. It is commonly known as the Fibonacci sequence.

```
IF number < 1 THEN
   ERROR
 ELSE IF number = 1 or 2 THEN
   RETURN 1
 ELSE
   CALL fibonacci WITH number - 2 RETURNING twoBack
   CALL fibonacci WITH number - 1 RETURNING oneBack
   RETURN twoBack + oneBack
 END IF
```

O(2^n);

## Out of the code snippets you just saw, which is the most time efficient?
The first one.
