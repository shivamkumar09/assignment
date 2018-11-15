# Graph Coloring Research Methodology assignment

Graph Coloring Algorithm

Introduction

Graph Coloring problem is to assign colors to certain elements of a graph subject to certain constraints.

In graph theory, graph coloring is a special case of graph labeling; it is an assignment of labels traditionally called "colors" to elements of a graph subject to certain constraints. In its simplest form, it is a way of coloring the vertices of a graph such that no two adjacent vertices are of the same color; this is called a vertex coloring.

Here, we are considering Vertex. So, our main focus is to color vertex.

Vertex coloring : It is the most common graph coloring problem. The problem is, given m colors, find a way of coloring the vertices of a graph such that no two adjacent vertices are colored using same color. 

The other graph coloring problems like Edge Coloring (No vertex is incident to two edges of same color) and Face Coloring (Geographical Map Coloring) can be transformed into vertex coloring.


Chromatic Number: The smallest number of colors needed to color a graph G is called its chromatic number. For example, the following can be colored minimum 3 colors. 

The problem to find chromatic number of a given graph is NP complete. 


Algorithmic Approach

Basic Graph Coloring Algorithm:

1. Color first vertex with first color.

2. Do following for remaining V-1 vertices.

a)	Consider the currently picked vertex and color it with the
lowest numbered color that has not been used on any previously
colored vertices adjacent to it. If all previously used colors
appear on vertices adjacent to v, assign a new color to it.

Applications

The graph coloring problem has huge number of applications.
1)	Making Schedule or Time Table: Suppose we want to make am exam schedule for a university. We have list different subjects and students enrolled in every subject. Many subjects would have common students (of same batch, some backlog students, etc). How do we schedule the exam so that no two exams with a common student are scheduled at same time? How many minimum time slots are needed to schedule all exams? This problem can be represented as a graph where every vertex is a subject and an edge between two vertices mean there is a common student. So this is a graph coloring problem where minimum number of time slots is equal to the chromatic number of the graph.

2)	 Mobile Radio Frequency Assignment: When frequencies are assigned to towers, frequencies assigned to all towers at the same location must be different. How to assign frequencies with this constraint? What is the minimum number of frequencies needed? This problem is also an instance of graph coloring problem where every tower represents a vertex and an edge between two towers represents that they are in range of each other.

3)	 Sudoku: Sudoku is also a variation of Graph coloring problem where every cell represents a vertex. There is an edge between two vertices if they are in same row or same column or same block.

4)	Register Allocation: In compiler optimization, register allocation is the process of assigning a large number of target program variables onto a small number of CPU registers. This problem is also a graph coloring problem.

5)	 Bipartite Graphs: We can check if a graph is Bipartite or not by coloring the graph using two colors. If a given graph is 2-colorable, then it is Bipartite, otherwise not. 

6)	 Map Coloring: Geographical maps of countries or states where no two adjacent cities cannot be assigned same color. Four colors are sufficient to color any map


Result

// Sample Input Output Format
stdin :
Enter the number of nodes: 4
Enter Adjacency Matrix:
0 1 0 1
1 0 1 0
0 1 0 1
1 0 1 0
stdout :
Possible Solutions are
1 2 1 2 
2 1 2 1 
The chromatic number is 2
The total number of solutions is 2 

N.B – Here chromatic number denotes the minimum number of color needed to color the vertex of a Graph, and the total number of solutions denotes all possible ways of assigning colors to the vertex of a graph.

