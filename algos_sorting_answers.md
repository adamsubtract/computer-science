>Write pseudocode for bubble sort.
```
procedure bubbleSort( list : array of items )

   loop = list.count;

   for i = 0 to loop-1 do:
      swapped = false

      for j = 0 to loop-1 do:

         /* compare the adjacent elements */   
         if list[j] > list[j+1] then
            /* swap them */
            swap( list[j], list[j+1] )		 
            swapped = true
         end if

      end for

      /*if no number was swapped that means
      array is sorted now, break the loop.*/

      if(not swapped) then
         break
      end if

   end for

end procedure return list
```


>Write pseudocode for quicksort.

```
FUNCTION partition(collection, low, high){
     SET pivot to collection[low]
     SET leftwall to low

     FOR each item in collection
         IF collection[i] < pivot THEN
             swap collection[i] with collection[leftwall + 1]
             SET leftwall to leftwall + 1
         END IF
     END FOR
     swap WITH pivot, collection[leftwall]

    RETURN leftwall
```

>We talked about time complexity in a previous checkpoint, and how to get an idea of the efficiency of an algorithm. After looking at the pseudocode for the above sorting methods, identify why merge sort and quick sort are much more efficient than the others. Walking through each algorithm with a few sample collections may help.

Merge sort is more efficient because it can break down and organize bigger collections faster. It keeps cutting the collection in half until it cant and micro organizes the collection when returning which is way faster than selection and insertion which have to
iterate over all of the collection.
Quick sort is efficient because it sorts multiple parts of the collection at once. Once it finds where to split the collection it does the same thing until its sorted.
Also both have better time complexity than the other sorts.



>All of the sorts addressed in this checkpoint are known as comparison sorts. Research bucket sort and explain how it works. What is the ideal input for bucket sort?

Bucket sort takes a collection and puts each item into different buckets or different
containers. It then sorts the items in the bucket and combines all the buckets
together in one collection.
