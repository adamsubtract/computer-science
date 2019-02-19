  1. ## What is a binary tree and what makes it unique to other trees?  

     A binary tree is a tree of nodes that have the ability to go left or right to
     another node. It is unique because it takes the greater value and puts it to the
     right.

  2. ## What is a heuristic?  

     "Is a technique designed for solving a problem more quickly when classic methods
     are too slow, or for finding an approximate solution when classic methods fail
     to find any exact solution." -

  3. ## What is another problem besides the shortest-path problem that requires the
     ## use of heuristics?  

     Computers/AI in chess games use heuristics. It would take a very long time for AI
     to calculate every single move and what could happen after that move, so they
     use heuristics to shorten the process and go with the best option.

  4. ## What is the difference between a depth-first search and a breadth-first search?  

     Depth-first will search through each node to it cannot search anymore.
     If what is was looking for was not there, it goes back up to the nearest parent
     node and continue searching in depth.

     Breadth-first will search the first node then go back up to the parent node
     and continue searching.

  5. ## Explain in your own words what an undirected, a-cyclic, unweighted graph is.

     undirected graph: is a graph where things are all connected and there is not
     understanding or meaning of a beginning or end. Things are all just connected

     A-cyclic: A graph that does not loop or have graph cycles.

     unweighted graph: A graph that connects things together but the connection
     between them does not have value.

  6. ## What kind of graph is a binary search tree?
     A-cyclic, unweighted, directed


##Programming Questions

  1. Given a Binary Search Tree and a value, write a function that checks to see
     whether the value exists within the tree.

     Looking at the picture I see that the graph is a Binary tree which means
     that the lesser values got to the left and the greater values go to the right.
     So the first thing to do is check if value is equal to the current node. If
     it is return a true statement. I then would check to see if the value is
     bigger or smaller. If its smaller go to the left node and if its bigger go
     to the right node. In the end if the value does not match with any Nodes
     return a false statement.

        function searchNode(data) {
          let current = this.root;
          while (current) {
            if (data === current.data) {
              return true;
            }
            else if (data < current.data) {
              current = current.left;
            } else {
              current = current.right;
            }
          }
          return false;
        }

2. Given a Binary Search Tree and two nodes, n1 and n2, write a function that
   finds the distance between the two nodes.

   I would use the search function that I made in answer 1 and add a counter
   variable to it. I would run both n1 and n2 through the search function, get the
   distance (or dummy variable), ad them together and return that number.

   function nodeDistance(n1, n2){

       function distance(data) {
         let current = this.root;
         var i = 0
         while (current) {
           if (data === current.data) {
             return i;
           }
           else if (data < current.data) {
             current = current.left;
             i++;
           } else {
             current = current.right;
             i++;
           }
         }
         return false;
       }

       var node1 = distance(n1);
       var node2 = distance(n2);

       var total = node1 + node2;

       return 'the distance is ' + total;
   }
