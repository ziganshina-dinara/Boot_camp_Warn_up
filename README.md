In order to solve each of the following problems: finding a motif in DNA, genome assembly with perfect coverage, Bellman-Ford algorithm, finding connected components and quick sorting algorithm - the functions were written. These functions are presented in warn_up.ipynb. Below I will describe how every function can be used for solving problem.

 ## Problem 1. Finding a Motif in DNA.

**Function**: kmp(string, substring)

This function finds all locations of substring in string. Function applies Knuth–Morris–Pratt algorithm.

**Parametrs**:
 * string: string, in which the substring is going to be found
 * substring: string, which is going to be found in the string

**Return**: string with all locations (space-separated) of substring in string

**Example**
```
>>> kmp('GATATATGCATATACTT','ATAT')
'2 4 10'
```

 ## Problem 2. Genome Assembly with Perfect Coverage.

**function**: circular_string(set_string)

Return a cyclic superstring of minimal length containing the getting reads.
    
**Parametrs**:

 * set_string: list of strings, which are DNA k-mers (k<50) taken from the same strand of a circular chromosome. All k-mers from this strand of the chromosome are present, and their de Bruijn graph consists of exactly one simple cycle.

**Return**: the string - cyclic superstring of minimal length containing the reads (thus corresponding to a candidate cyclic chromosome).

**Example**
```
>>> set_string=['ATTAC','TACAG','GATTA', 'ACAGA','CAGAT','TTACA', 'AGATT']
>>> circular_string(set_string)
'ATTACAG'
```

 ## Problem 3. Bellman-Ford Algorithm.

**Function**: func_ford_bellman(list_edges)

Compute shortest distances  from the vertex 1 to the all vertexs in a directed simple graph with possibly negative edge weights (but without negative cycles). Function applies Bellman-Ford algorithm.

**Parametrs**:
 * list_edges : The first line contains two numbers, the number of vertices n and the number of edges m, each of the following m lines contains an edge given by two vertices and its weight. 

**Return**: An array D[1..n] where D[i] is the length of a shortest path from the vertex 1 to the vertex i (D[1]=0). If i is not reachable from 1 set D[i] to x

**Example**
```
>>> list_edges="9 13\n1 2 10\n3 2 1\n3 4 1\n4 5 3\n5 6 -1\n7 6 -1\n8 7 1\n1 8 8\n7 2 -4\n2 6 2\n6 3 -2\n9 5 -10\n9 4 7"
>>> func_ford_bellman(list_edges)
[0, 5, 5, 6, 9, 7, 9, 8, 'x']
```
 ## Problem 4. Connected Components.

**Function**: solve_DFS (edge_list)

Compute the number of connected components in a given undirected graph. The function applies depth-first search algorithm.

**Parametrs**:
 * edge_list: The first line contains two numbers, the number of vertices n and the number of edges m, each of the following m lines contains an edge given by two vertices.

**Return**: the number of connected components in the graph

**Example**
```
>>> edge_list="12 13\n1 2\n1 5\n5 9\n5 10\n9 10\n3 4\n3 7\n3 8\n4 8\n7 11\n8 11\n11 12\n8 12"
>>> solve_DFS(edge_list)
3
```
 ## Problem 5. Quick Sort.

**Function**: QuickSort(array)

This function sorts array. Function applies quick sort algorithm.

**Parametrs**:
 * array: array [1..n] of integers from −10^5 to  10^5

**Return**:  sorted array [1..n]

**Example**
```
>>> QuickSort([5, -2, 4, 7 ,8, -10, 11])
[-10, -2, 4, 5, 7, 8, 11]
```
