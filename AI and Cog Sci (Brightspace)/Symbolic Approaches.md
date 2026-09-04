PSSH informed methods toward AI. General Problem Solver (GPS) was able to solve simple _toy_ problems (Tower of Hanoi, Sliding Tile Puzzle) but couldn't handle real world problems due to too much information. This eventually developed into a common model of cognition, i.e., SOAR architecture. 

**Problem Solving**: the process of _searching_ through the _problem space_ until a _goal state_ is found. We start with an _initial state_, and go through _operators_ (transform given a state to another state) until we reach our _goal state_.

**Problem space**: (a.k.a. the search space) is the set of all possible problem "states". This can be represented via a graph, tree, etc.

A state is a representation of the problem in some "degree" of solution. But the path from the initial state to the goal state represents the solution.  To get the solution, a AI operates on the according to the _search strategy_, applying the relevant operators. The search strategy determines in what order states are tested to see if they are the goal. 

An algorithm is the "recipe" in which the task can be accomplished. We have _uninformed search_ and _informed search_.  
	**Uninformed search**: no domain-specific knowledge is used. Unfortunately, this means it can take a very long time to reach solutions.
		Breadth first search (BFS): tests all the nodes in a given level of the solution tree to see if each is the goal before continuing on to the next level. This is akin to a "queue" or FIFO (first in, first out data structure). Applications of BFS include solving games and puzzles, web crawling, social networking.
		Depth first search (DFS): goes deep first, then broad: it iteratively expands the left-most child down all levels. This is akin to a "stack" or LIFO (last in, first out data structure). 
			
	**Informed search**: heuristics are used to simplify the search.
			Not every heuristic is _admissable_. We don't want them that overestimate the true cost or distance to reach the goal state. Manhattan Difference (MD) = absolute difference between the x-coordinates and y-coordinates of two points. |x1-x2| + |y1-y2|
	