
<h1>Dijkstra’s Algorithm </h1>



<h2>Description</h2>Finding the shortest path that goes from a starting point to a destination point given a set of points and route lengths connecting them is an already well known problem, and it’s even part of our daily lives, as shortest path programs are widely available nowadays.

Most people usually like very much these applications as they make their lives easier. Well, maybe not that much easier.

Now that almost everyone can have access to GPS navigation devices able to calculate shortest paths, most routes that form the shortest path are getting slower because of heavy traffic. As most people try to follow the same path, it’s not worth it anymore to follow these directions.

With this in his mind, your boss asks you to develop a new application that only he will have access to, thus saving him time whenever he has a meeting or any urgent event. He asks you that the program must answer not the shortest path, but the almost shortest path. He defines the almost shortest path as the shortest path that goes from a starting point to a destination point such that no route between two consecutive points belongs to any shortest path from the starting point to the destination.

For example, suppose the figure below represents the map given, with circles representing location points, and lines representing direct, one-way routes with lengths indicated. The starting point is marked as S and the destination point is marked as D. The bold lines belong to a shortest path (in this case there are two shortest paths, each with total length 4). Thus, the almost shortest path would be the one indicated by dashed lines (total length 5), as no route between two consecutive points belongs to any shortest path. Notice that there could exist more than one possible answer, for instance if the route with length 3 had length 1. There could exist no possible answer as well.

​

Input
The input contains several test cases. The first line of a test case contains two integers N (2 ≤ N ≤ 500) and M (1 ≤ M ≤ 104), separated by a single space, indicating respectively the number of points in the map and the number of existing one-way routes connecting two points directly. Each point is identified by an integer between 0 and N -1. The second line contains two integers S and D, separated by a single space, indicating respectively the starting and the destination points (S ≠ D; 0 ≤ S, D < N). Each one of the following M lines contains three integers U, V and P (U ≠ V; 0 ≤ U, V < N; 1 ≤ P ≤ 103), separated by single spaces, indicating the existence of a one-way route from U to V with distance P. There is at most one route from a given point U to a given point V, but notice that the existence of a route from U to V does not imply there is a route from V to U, and, if such road exists, it can have a different length. The end of input is indicated by a line containing only two zeros separated by a single space.

Output
For each test case in the input, your program must print a single line, containing -1 if it is not possible to match the requirements, or an integer representing the length of the almost shortest path found.
Input
The first line of input has two integers: N (0 ≤ N ≤ 1000) that indicates the number of different pipe sizes and T (0 ≤ T ≤ 2000), that is the size of each pipe produced by OBI.

Each of the following N lines has two integers: Ci and Vi (1 ≤ Ci, Vi ≤ 5000, 1 ≤ i ≤ N), representing, respectively, the lenght and the sales value of a client ordered pipe i.

Output
For each test case, print in one line the greatest possible value that can be obtained by cutting and selling a pipe with original length T.
<br />


<h2>Languages Used</h2>

- <b>Python</b> 

<h2>Program walk-through:</h2>
The overall framework to solve the problem:
Read in a graph.
Run Dijkstra’s Algorithm to get a subgraph consist of all the shortest paths.
Remove the subgraph via BFS algorithm.
Dijkstra’s Algorithm again.

<p align="center">
TEST CODE INPUT:
 <br>
7  9
 <br>
0 6
 <br>
0 1 1
 <br>
0 2 1
 <br>
0 3 2
 <br>
0 4 3
 <br>
1 5 2
 <br>
2 6 4
 <br>
3 6 2
 <br>
4 6 4
<br>
5 6 1
<br>
4 6
<br>
0 2
<br>
0 1 1
<br>
1 2 1
<br>
1 3 1
<br>
3 2 1
<br>
2 0 3
<br>
3 0 2
<br>
6 8
<br>
0 1
<br>
0 1 1
<br>
0 2 2
<br>
0 3 3
<br>
2 5 3
<br>
3 4 2
<br>
4 1 1
<br>
5 1 1
<br>
3 0 1
<br>
0 0
 <br>
EXPECTED OUTPUT:
 5
-1
6
 </br>


<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
