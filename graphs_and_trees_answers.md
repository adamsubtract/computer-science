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

```
   class TreeNode {
     constructor(data) {
       this.data = data;
       this.left = null;
       this.right = null;
     }
   }

   class Tree {
     constructor() {
       this.root = null;
     }

     searchNode(data) {
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

    nodeDistance(n1, n2){

          function distance(current, data) {
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

          function findLCA(root, n1, n2) {
            var current = root;
            while (current) {
              if (n1 < current.data && n2 < current.data) {
                current = current.left;
              } else if (n1 > current.data && n2 > current.data) {
                current = current.right;
              } else {
                return current;
              }
            }
          }

          var lca = findLCA(this.root, n1, n2);
          var node1 = distance(lca, n1);
          var node2 = distance(lca, n2);

          if (node1 !== false && node2 !== false) {
            var total = node1 + node2;

            return 'the distance is ' + total;
          } else {
            return false;
          }
      }
   }

   /*
        9
       / \
      5   11
     / \
    1   6

   */

   let node6 = new TreeNode(6),
       node1 = new TreeNode(1),
       node5 = new TreeNode(5),
       node9 = new TreeNode(9),
       node11 = new TreeNode(11);

   node9.left = node5;
   node9.right = node11;
   node5.left = node1;
   node5.right = node6;

   let tree = new Tree();
   tree.root = node9;


   console.log(tree.searchNode(9));
   console.log(tree.searchNode(1));
   console.log(tree.searchNode(11));
   console.log(tree.searchNode(13));
   console.log(tree.searchNode(2));

   console.log(tree.nodeDistance(1, 6));
   console.log(tree.nodeDistance(1, 5));
   console.log(tree.nodeDistance(34, 9));
   ```
