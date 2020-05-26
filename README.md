# AI TRIMESTER 9 MIT-WPU
<pre>
*************************************************************
Practical 1: [A Star Algorithm for 8/16 Puzzle Problem]
Algorithm Used: A-Star is an informed search algorithm
f(n) = g(n) + h(n)
f(n) -> Estimated cost of cheapest solution
g(n) -> Cost to reach node n from search state
h(n) -> Cost to reach from node n to goal node

Advantages of Informed Search:
Good Solution in reasonable time
More useful for large search space

Disadvantages of Informed Search:
Bad Space Complexity
Good Heuristic functions are hard to define
Complex heuristic functions slow down the search

Time Complexity: Time complexity is O(E), where E is the number of edges in the graph
Space Complexity: Worst case is O(V), where V is the total number of vertices.

Procedure:
1. Accept starting state
2. Accept goal state
3. Create open list
4. Insert Start state in openlist
5. Set first node in open list as current node
6. Generate children for current node, calculate heuristic for each child
7. Close current node
8. Sort open list by heuristic value
9. Check if goal reached if no go to 5
10. End

We have used hamming distance as heuristic
*************************************************************
Practical 2: [MiniMax Theorem for Tic-Tac-Toe]
Algorithm Used: MiniMax Algorithm is a recursive backtracking algorithm

Advantages:
Optimal choice selected always
Works very well on less complex games

Disadvantages:
Not space efficient
Trees can run deep
O(b^m) time complexity
Not good for games like chess and stuff

Time Complexity: O(b^m) where b is branching factor, m is depth of tree
Space Complexity: O(bm) where b is branching factor, m is depth of tree

Procedure:
1. Get Human Input
2. For every empty space run minimax with maximising disabled
3. Check if either side is winning 
4. If maximising is enabled set best score = -infinity else goto 7
5. For every empty space run minimax with maximising disabled
6. Get max score from all iterations
7. If maximising is disabled set best score = infinity
8. For every empty space run minimax with maximising disabled
9. Get min score from all iterations
10. Return best score and hence the best position to play
11. Check if AI is winning else if empty position on board goto 1 else declare tie

*************************************************************
Practical 3: [Constraint Satisfaction Problem]
Algorithm Used: Problems are modelled like CSPs and then solved using either backtracking or by tree search

Advantages:
Simplest to understand, implement
Allows sytematic searches

Disadvantages:
Thrashing, i.e., repeated failure due to the same reason.
Redundant Work
Detects conflict too late

Time Complexity: Research Topic, CSPs often exhibit high complexity, requiring a combination of heuristics and combinatorial search methods to be solved in a reasonable time.
Space Complexity: It is a backtracking algorithm so space requirement is quite heavy.

Procedure:
1. Create a general contraint class with abstract satisfied method
2. Create a CSP Scaffold with ability to add constraints, Check Consistency (All constraints), Backtrack search
3. Add new SEND+MORE=MONEY Constraint by inheriting from constraint class, define satisfied method 
4. Accept Letters -> Variables and accept possible digits -> Domains
5. Create CSP object
6. Add constraint made in Step 3
7. Initiate Backtracking

*************************************************************
Practical 4: [Unification Problem]
Algorithm Used: Most General Unifier Algorithm

Advantages:
Helps in formation of relations
Works well for small strings

Disadvantages: 
Time consuming for longer strings
Hard to implement a robust, reasonable complexity unification algorithm

Time Complexity: Literal length n O(n)	//For our implementation
Space Complexity: Literal storage 

Procedure:
1. Accept Two literal strings
2. Set substitution set empty
3. If literals have brackets extract content from the brackets in tuple format
4. Match Lengths of the new literals
5. If they match proceed else end
6. For every tuple match tuple[0] item with other tuples[0] item
7. On match add (tuple1[1]/tuple2[1]) to substitution set if tuple1[1] not in tuple2[1]
8. End

*************************************************************
Practical 5: [Implementation of Neural Network]
Algorithm Used: Artificial Neural Network

Advantages:
Can produce output even with incomplete information
Fault Tolerant
Self learning
Parallel Processing ability

Disadvantages:
Dependant on hardware
Blackbox functioning (Never know if its looking for the right things)
No specific rules for good results
Translate all parameters to numeric form
No fixed value of epochs

Time Complexity: O(No. of weights * No. of training samples * No. of Epochs) (Heavily improved due to vectorization and exclusion of for loops)
Space Complexity: -

Procedure: 
1. Remove missing values from data
2. Select relevant features from data
3. Encode Categorical Variables 
4. Do train test split
5. Scale values
6. Create network Architecutre
7. Perform grid search for best params for certain no. of epochs
8. Make network with best params and then save the weights for later use

*************************************************************

</pre>

























