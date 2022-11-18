### 3.1 
**Q:** 
Explain why problem formulation must follow goal formulation.

**A:**

### 3.2
**Q:** 
Your goal is to navigate a robot out of a maze. The robot starts in the center of the maze
facing north. You can turn the robot to face north, east, south, or west. You can direct the
robot to move forward a certain distance, although it will stop before hitting a wall.
a. Formulate this problem. How large is the state space?
b. In navigating a maze, the only place we need to turn is at the intersection of two or
more corridors. Reformulate this problem using this observation. How large is the state
space now?
c. From each point in the maze, we can move in any of the four directions until we reach a
turning point, and this is the only action we need to do. Reformulate the problem using
these actions. Do we need to keep track of the robot’s orientation now?
d. In our initial description of the problem we already abstracted from the real world,
restricting actions and removing details. List three such simplifications we made.

**A:**

### 3.3
**Q:**

**A:**

### 3.4 
**Q:**
Show that the 8-puzzle states are divided into two disjoint sets, such that any state is
reachable from any other state in the same set, while no state is reachable from any state in
the other set. (Hint: See Berlekamp et al. (1982).) Devise a procedure to decide which set a
given state is in, and explain why this is useful for generating random states.

**A:**

### 3.5 
**Q:**
Consider the n-queens problem using the “efficient” incremental formulation given on
page 72. Explain why the state space has at least √3 n! states and estimate the largest n for
which exhaustive exploration is feasible. (Hint: Derive a lower bound on the branching factor
by considering the maximum number of squares that a queen can attack in any column.)

**A:**

### 3.6 
**Q:**
Give a complete problem formulation for each of the following. Choose a formulation
that is precise enough to be implemented.
a. Using only four colors, you have to color a planar map in such a way that no two
adjacent regions have the same color.
b. A 3-foot-tall monkey is in a room where some bananas are suspended from the 8-foot
ceiling. He would like to get the bananas. The room contains two stackable, movable,
climbable 3-foot-high crates.
c. You have a program that outputs the message “illegal input record” when fed a certain
file of input records. You know that processing of each record is independent of the
other records. You want to discover what record is illegal.
d. You have three jugs, measuring 12 gallons, 8 gallons, and 3 gallons, and a water faucet.
You can fill the jugs up or empty them out from one to another or onto the ground. You
need to measure out exactly one gallon.

**A:**

### 3.7 
**Q:**
Consider the problem of finding the shortest path between two points on a plane that has
convex polygonal obstacles as shown in Figure ### 3.31. This is an idealization of the problem
that a robot has to solve to navigate in a crowded environment.
a. Suppose the state space consists of all positions (x, y) in the plane. How many states
are there? How many paths are there to the goal?
b. Explain briefly why the shortest path from one polygon vertex to any other in the scene
must consist of straight-line segments joining some of the vertices of the polygons.
Define a good state space now. How large is this state space?
c. Define the necessary functions to implement the search problem, including an ACTIONS
function that takes a vertex as input and returns a set of vectors, each of which maps the
current vertex to one of the vertices that can be reached in a straight line. (Do not forget
the neighbors on the same polygon.) Use the straight-line distance for the heuristic
function.
d. Apply one or more of the algorithms in this chapter to solve a range of problems in the
domain, and comment on their performance.

**A:**

### 3.8 
**Q:**
On page 68, we said that we would not consider problems with negative path costs. In
this exercise, we explore this decision in more depth.
a. Suppose that actions can have arbitrarily large negative costs; explain why this possibility would force any optimal algorithm to explore the entire state space.
b. Does it help if we insist that step costs must be greater than or equal to some negative
constant c? Consider both trees and graphs.
c. Suppose that a set of actions forms a loop in the state space such that executing the set in
some order results in no net change to the state. If all of these actions have negative cost,
what does this imply about the optimal behavior for an agent in such an environment?
d. One can easily imagine actions with high negative cost, even in domains such as route
finding. For example, some stretches of road might have such beautiful scenery as to
far outweigh the normal costs in terms of time and fuel. Explain, in precise terms,
within the context of state-space search, why humans do not drive around scenic loops
indefinitely, and explain how to define the state space and actions for route finding so
that artificial agents can also avoid looping.
e. Can you think of a real domain in which step costs are such as to cause looping?

**A:**

### 3.9
**Q:**
 The missionaries and cannibals problem is usually stated as follows. Three missionaries and three cannibals are on one side of a river, along with a boat that can hold one or
two people. Find a way to get everyone to the other side without ever leaving a group of missionaries in one place outnumbered by the cannibals in that place. This problem is famous in
AI because it was the subject of the first paper that approached problem formulation from an
analytical viewpoint (Amarel, 1968).
a. Formulate the problem precisely, making only those distinctions necessary to ensure a
valid solution. Draw a diagram of the complete state space.
b. Implement and solve the problem optimally using an appropriate search algorithm. Is it
a good idea to check for repeated states?
c. Why do you think people have a hard time solving this puzzle, given that the state space
is so simple?

**A:**

### 3.10
**Q:**
Define in your own words the following terms: state, state space, search tree, search
node, goal, action, transition model, and branching factor.

**A:**

### 3.11 
**Q:**
What’s the difference between a world state, a state description, and a search node?
Why is this distinction useful?

**A:**

### 3.12 
**Q:**
An action such as Go(Sibiu) really consists of a long sequence of finer-grained actions:
turn on the car, release the brake, accelerate forward, etc. Having composite actions of this
kind reduces the number of steps in a solution sequence, thereby reducing the search time.
Suppose we take this to the logical extreme, by making super-composite actions out of every
possible sequence of Go actions. Then every problem instance is solved by a single supercomposite action, such as Go(Sibiu)Go(Rimnicu Vilcea)Go(Pitesti)Go(Bucharest). Explain
how search would work in this formulation. Is this a practical approach for speeding up
problem solving?

**A:**

### 3.13 
**Q:**
Prove that GRAPH-SEARCH satisfies the graph separation property illustrated in Figure ### 3.9. (Hint: Begin by showing that the property holds at the start, then show that if it holds
before an iteration of the algorithm, it holds afterwards.) Describe a search algorithm that
violates the property.

**A:**

### 3.14 
**Q:**
Which of the following are true and which are false? Explain your answers.
a. Depth-first search always expands at least as many nodes as A∗ search with an admissible heuristic.
b. h(n)=0 is an admissible heuristic for the 8-puzzle.
c. A∗ is of no use in robotics because percepts, states, and actions are continuous.
d. Breadth-first search is complete even if zero step costs are allowed.
e. Assume that a rook can move on a chessboard any number of squares in a straight line,
vertically or horizontally, but cannot jump over other pieces. Manhattan distance is an
admissible heuristic for the problem of moving the rook from square A to square B in
the smallest number of moves.

**A:**

### 3.15 
**Q:**
Consider a state space where the start state is number 1 and each state k has two
successors: numbers 2k and 2k + 1.
a. Draw the portion of the state space for states 1 to 15.
b. Suppose the goal state is 11. List the order in which nodes will be visited for breadthfirst search, depth-limited search with limit 3, and iterative deepening search.
c. How well would bidirectional search work on this problem? What is the branching
factor in each direction of the bidirectional search?
d. Does the answer to (c) suggest a reformulation of the problem that would allow you to
solve the problem of getting from state 1 to a given goal state with almost no search?
e. Call the action going from k to 2k Left, and the action going to 2k + 1 Right. Can you
find an algorithm that outputs the solution to this problem without any search at all?

**A:**

### 3.16 
**Q:**
A basic wooden railway set contains the pieces shown in Figure ### 3.32. The task is to
connect these pieces into a railway that has no overlapping tracks and no loose ends where a
train could run off onto the floor.
a. Suppose that the pieces fit together exactly with no slack. Give a precise formulation of
the task as a search problem.
b. Identify a suitable uninformed search algorithm for this task and explain your choice.
c. Explain why removing any one of the “fork” pieces makes the problem unsolvable.
d. Give an upper bound on the total size of the state space defined by your formulation.
(Hint: think about the maximum branching factor for the construction process and the
maximum depth, ignoring the problem of overlapping pieces and loose ends. Begin by
pretending that every piece is unique.)

**A:**

### 3.17 
**Q:**
On page 90, we mentioned iterative lengthening search, an iterative analog of uniform cost search. The idea is to use increasing limits on path cost. If a node is generated
whose path cost exceeds the current limit, it is immediately discarded. For each new iteration, the limit is set to the lowest path cost of any node discarded in the previous iteration.
a. Show that this algorithm is optimal for general path costs.
b. Consider a uniform tree with branching factor b, solution depth d, and unit step costs.
How many iterations will iterative lengthening require?
c. Now consider step costs drawn from the continuous range [, 1], where 0 << 1. How
many iterations are required in the worst case?
d. Implement the algorithm and apply it to instances of the 8-puzzle and traveling salesperson problems. Compare the algorithm’s performance to that of uniform-cost search,
and comment on your results.

**A:**

### 3.18 
**Q:**
Describe a state space in which iterative deepening search performs much worse than
depth-first search (for example, O(n2) vs. O(n)).

**A:**

### 3.19 
**Q:**
Write a program that will take as input two Web page URLs and find a path of links
from one to the other. What is an appropriate search strategy? Is bidirectional search a good
idea? Could a search engine be used to implement a predecessor function?

**A:**

### 3.20 
**Q:**
Consider the vacuum-world problem defined in Figure 2.2.
a. Which of the algorithms defined in this chapter would be appropriate for this problem?
Should the algorithm use tree search or graph search?
b. Apply your chosen algorithm to compute an optimal sequence of actions for a 3 × 3
world whose initial state has dirt in the three top squares and the agent in the center.
c. Construct a search agent for the vacuum world, and evaluate its performance in a set of
3 × 3 worlds with probability 0.2 of dirt in each square. Include the search cost as well
as path cost in the performance measure, using a reasonable exchange rate.
d. Compare your best search agent with a simple randomized reflex agent that sucks if
there is dirt and otherwise moves randomly.
e. Consider what would happen if the world were enlarged to n × n. How does the performance of the search agent and of the reflex agent vary with n?

**A:**

### 3.21 
**Q:**
Prove each of the following statements, or give a counterexample:
a. Breadth-first search is a special case of uniform-cost search.
b. Depth-first search is a special case of best-first tree search.
c. Uniform-cost search is a special case of A∗ search.

**A:**

### 3.22 
**Q:**
Compare the performance of A∗ and RBFS on a set of randomly generated problems
in the 8-puzzle (with Manhattan distance) and TSP (with MST—see Exercise ### 3.30) domains.
Discuss your results. What happens to the performance of RBFS when a small random number is added to the heuristic values in the 8-puzzle domain?

**A:**

### 3.23
**Q:**
Trace the operation of A∗ search applied to the problem of getting to Bucharest from
Lugoj using the straight-line distance heuristic. That is, show the sequence of nodes that the
algorithm will consider and the f, g, and h score for each node.

**A:**

### 3.24 
**Q:**
Devise a state space in which A∗ using GRAPH-SEARCH returns a suboptimal solution
with an h(n) function that is admissible but inconsistent.

**A:**

### 3.25 
**Q:**
The heuristic path algorithm (Pohl, 1977) is a best-first search in which the evalu- HEURISTIC PATH
ALGORITHM
ation function is f(n) = (2 − w)g(n) + wh(n). For what values of w is this complete?
For what values is it optimal, assuming that h is admissible? What kind of search does this
perform for w = 0, w = 1, and w = 2?

**A:**

### 3.26 
**Q:**
Consider the unbounded version of the regular 2D grid shown in Figure ### 3.9. The start
state is at the origin, (0,0), and the goal state is at (x, y).
a. What is the branching factor b in this state space?
b. How many distinct states are there at depth k (for k > 0)?
c. What is the maximum number of nodes expanded by breadth-first tree search?
d. What is the maximum number of nodes expanded by breadth-first graph search?
e. Is h = |u − x| + |v − y| an admissible heuristic for a state at (u, v)? Explain.
f. How many nodes are expanded by A∗ graph search using h?
g. Does h remain admissible if some links are removed?
h. Does h remain admissible if some links are added between nonadjacent states?

**A:**

### 3.27 
**Q:**
n vehicles occupy squares (1, 1) through (n, 1) (i.e., the bottom row) of an n × n grid.
The vehicles must be moved to the top row but in reverse order; so the vehicle i that starts in
(i, 1) must end up in (n − i + 1, n). On each time step, every one of the n vehicles can move
one square up, down, left, or right, or stay put; but if a vehicle stays put, one other adjacent
vehicle (but not more than one) can hop over it. Two vehicles cannot occupy the same square.
a. Calculate the size of the state space as a function of n.
b. Calculate the branching factor as a function of n.
c. Suppose that vehicle i is at (xi, yi); write a nontrivial admissible heuristic hi for the
number of moves it will require to get to its goal location (n − i + 1, n), assuming no
other vehicles are on the grid.
d. Which of the following heuristics are admissible for the problem of moving all n vehicles to their destinations? Explain.

**A:**

### 3.28 
**Q:**
Invent a heuristic function for the 8-puzzle that sometimes overestimates, and show
how it can lead to a suboptimal solution on a particular problem. (You can use a computer to
help if you want.) Prove that if h never overestimates by more than c, A∗ using h returns a
solution whose cost exceeds that of the optimal solution by no more than c.

**A:**

### 3.29 
**Q:**
Prove that if a heuristic is consistent, it must be admissible. Construct an admissible
heuristic that is not consistent.

**A:**

### 3.30 
**Q:**
The traveling salesperson problem (TSP) can be solved with the minimum-spanningtree (MST) heuristic, which estimates the cost of completing a tour, given that a partial tour
has already been constructed. The MST cost of a set of cities is the smallest sum of the link
costs of any tree that connects all the cities.
a. Show how this heuristic can be derived from a relaxed version of the TSP.
b. Show that the MST heuristic dominates straight-line distance.
c. Write a problem generator for instances of the TSP where cities are represented by
random points in the unit square.
d. Find an efficient algorithm in the literature for constructing the MST, and use it with A∗
graph search to solve instances of the TSP.

**A:**

### 3.31 
**Q:**
On page 105, we defined the relaxation of the 8-puzzle in which a tile can move from
square A to square B if B is blank. The exact solution of this problem defines Gaschnig’s
heuristic (Gaschnig, 1979). Explain why Gaschnig’s heuristic is at least as accurate as h1
(misplaced tiles), and show cases where it is more accurate than both h1 and h2 (Manhattan
distance). Explain how to calculate Gaschnig’s heuristic efficiently.

**A:**

### 3.32 
**Q:**
We gave two simple heuristics for the 8-puzzle: Manhattan distance and misplaced
tiles. Several heuristics in the literature purport to improve on this—see, for example, Nilsson (1971), Mostow and Prieditis (1989), and Hansson et al. (1992). Test these claims by
implementing the heuristics and comparing the performance of the resulting algorithms.

**A:**