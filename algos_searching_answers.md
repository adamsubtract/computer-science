## What is a real-life scenario that uses linear search?

Going door to door in a hotel hallway.

## What is a real-life scenario that uses binary search?

When we file things in a filing cabinet we don't search through every single file
We look to see where the closets letter is and we search near that letter and
continue the process until we find the letter.

## Given the alphabetically sorted collection in this checkpoint, how many iterations would it take to find the value G using linear search?

three iterations.

## Given the alphabetically sorted collection in this checkpoint, how many iterations would it take to find the value G using binary search?

one.

## Given an unsorted collection of a million items, which algorithm would you choose between linear search and binary search? Explain your reasoning.

linear because to use binary the collection would have to be sorted. ;)


## Given a sorted collection of a million items, which algorithm would you choose between linear search and binary search? Explain your reasoning.

Binary would be the one to use because it cuts the collection in half constantly
which makes it a smaller collection every time.


# Programming Questions

You and a friend have set a wager to see who can find the word "Albatross" in the dictionary the fastest. Write a program to allow you to win the bet.

```var names = ["Albatross", "Baboon", "Cat", "Dog", "Falcon", "Killer Whale"];

function WordSearch(arr, word){
  var low = arr[0];
  var high = arr[arr.length -1];

  while (low <= high) {
    var mid = (arr.indexOf(low) + arr.indexOf(high)) / 2;
    mid = Math.round(mid);

    if(arr[mid] > word) {
      high = arr[mid -1];
    }
    else if (arr[mid] < word) {
      low = arr[mid + 1];
    }
    else {
      return arr[mid];
    }
  }
  return "That name is not in the list";
}

console.log(WordSearch(names, "Albatross"));
```

You work at a pet store, and a child has asked you to net the only white-spotted goldfish from the fish tank. Write a program that will help you net the right fish.

```
var fishTank = ["goldfish", "goldfish", "green swordtail",
			"commmon molly", "goldfish", "platy", "white-spotted goldfish"];

function NetFish(arr, target){
  for(var i = 0; i < arr.length; i++){
    if (arr[i] === target){
      return "You've net the only white-spotted goldfish from the fish tank";
    }
  }
  return "The he only white-spotted goldfish isn't in the tank .";
}

console.log(NetFish(fishTank, "white-spotted goldfish"));
```
