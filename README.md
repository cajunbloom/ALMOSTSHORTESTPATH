
<h1>Dijkstra’s Algorithm </h1>



<h2>Description</h2>The program is a Knapsack Problem variant. OBI (Brazilian Organization of Facilities) is a company that produces pipes and fitters. The production technique used at OBI always produces long pipes, which are then cut to satisfy client needs.

Their clients have different applications, so they need pipes with different lengths. When the company was small and the clients were few, all the pipe cut planning process (to maximize profit) was done by a very dedicated employee. However, with the increase on the number of orders, it became prohibitive. That's where you come in: hired by OBI, your task is to write a program that, given the relation between the pipes' length and its respective sales value, determine the greatest possible value that can be obtained by cutting and selling a pipe with a determined initial length. Pipe lengths can be repeated, and there can be leftovers.

Input
The first line of input has two integers: N (0 ≤ N ≤ 1000) that indicates the number of different pipe sizes and T (0 ≤ T ≤ 2000), that is the size of each pipe produced by OBI.

Each of the following N lines has two integers: Ci and Vi (1 ≤ Ci, Vi ≤ 5000, 1 ≤ i ≤ N), representing, respectively, the lenght and the sales value of a client ordered pipe i.

Output
For each test case, print in one line the greatest possible value that can be obtained by cutting and selling a pipe with original length T.
<br />


<h2>Languages Used</h2>

- <b>Java</b> 

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
