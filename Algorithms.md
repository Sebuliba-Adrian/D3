## Algorithms

1. ### Breadth First Search (BFS)

    Breadth-first search is an algorithm for traversing unweighted graph data structures. BFS visits all the nodes at the same level first before moving on to the next. 
    A queue data structure is used to enable.
    Steps: Start at some arbitrary node of a graph and explore the neighbor nodes first, before moving to the next level neighbors 
    Use a queue data structure to track which node to visit next. 
    It runs with a time complexity of O(V + E)
 
 2. ### Depth First Search (DFS)
     
    All nodes in a certain direction from origin are visited together( before switching directions).
    We go deeper in the direction that we originally chose before visiting other nodes in other directions.
    Once all nodes in one direction are exhaustively visted then we can switch directions(backtracking) and visit other nodes in other directions
    Time complexity is O(V + E)
    
3.  ### A* Search 
     
      Is an algorithm for traversing weighted graph data structures using informed search. This algorithm is used to find the shortest path between the start node and the goal node.
      At each search iteration, A*Search uses an evaluation function f*(n) to select a board state n from open whose f*(n) has the smallest value. f*(n) has the distinctive structure f*(n)=g*(n)+h*(n), where

      g*(n) estimates shortest sequence of moves from the initial state to n
      h*(n) estimates shortest sequence of moves from n to the goal state
      f*(n) estimates shortest sequence of moves from initial state to goal state through n


      The algorithm starts from an initial state in a search tree and a goal state that must be reached. It assumes that it can 
      (a) iterate through all valid moves for a given  state, and 
      (b) compute the evaluation function f*(n) on a board state n.
      
      I have the Implementation of A* search: https://github.com/Sebuliba-Adrian/Algorithms/blob/master/sketch.js 

4.  ### Sorting 
       
       Merge Sort. Uses the divide and conquer strategy:
       
       (1) divides the array into two equally sized sub array
       (2) sort each sub array 
       (3) merge two sorted arrays into final array.
       (4) the resultant array will be sorted
       
       O(nlogn) — Is the time complexity
       
       Quick Sort. Uses the divide and conquer strategy: 
       
       (1) Select an item in the unsorted array as pivot 
       (2) Divide array into 2 smaller arrays, one contains elements smaller than pivot while the other contains elements greater than the pivot 
       (3) Sort the smaller lists, and combine the results into final sorted array.
       
       O(nlogn) — Is the time complexity
       
       Insertion Sort:
       Iterates through unsorted array while populating a sorted array. 
       For each value in an unsorted array, find appropriate place in sorted array and insert it.
       
       The time comlexity of insertion sort is O(n²).
       
       Heap Sort:
         (1) Build a min or max heap from the unsorted array 
         (2) Remove the root node repeatitively from the heap and put into the sorted array until you run out of nodes.
         (3) The resulting list will be sorted
          O(nlogn) — Is the time complexity
          
          
          
5. ### Hashing:
         MD5
          MD5 is a Message Digest hashing algorithm that creates a fingerprint of the data input to the hashing function.
          Message-Digest algorithms are mathematical functions that transform a data string of arbitrary length into a second string of data of fixed length (128 bits, in this case). 
          The resultant of the data is often referred to as the “fingerprint” of the original data.
          Uses:
          It is commony used commonly used to check the integrity of files.
          For instance, when uploading or downloading a file you need to ensure that the downloaded or uploaded file is exactly the same as that of the original one.
          In this scenario, the MD5 hash can become handy. All you have to do is generate MD5 hash (or MD5 check-sum) for the intended file on your server.
          - After you download the file onto your local machine, again generate MD5 hash for the downloaded file.
           Compare these two hashes and if they match, that means the file is downloaded perfectly without any data loss.
          - So MD5 hash can be used to uniquely identify a file.
          - MD5 can also be used to check the integrity of messages sent in a chatting application. In this case the hashes of the sent and received n]messages are compare to ensure that the messages have not been tapere with  
          - Also When storing passwordi to the database in a web application. MD5 can be used to hash the password stored in the database and that is in turn comapred with the password hash of a user logging into the application
          
         Collisions:
              A collision is when two distinct input values to the hashing function produce the same hash. This is a problem, because if there are collisions then the algorithm can be compromised.
              
         Linear probing: used resolving collisions in hash tables, data structures for maintaining a collection of key–value pairs and looking up the value associated with a given key.
    
    
    
