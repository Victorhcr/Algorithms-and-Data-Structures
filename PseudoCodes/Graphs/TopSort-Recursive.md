Topological Sorting - Recursive Version
----
<p>

```sh
1   L ← Empty list that will contain the sorted nodes
2   while there are unmarked nodes do
3       select an unmarked node n
4       visit(n) 
5   function visit(node n)
6       if n has a temporary mark then stop (not a DAG)
7       if n is not marked (i.e. has not been visited yet) then
8           mark n temporarily
9           for each node m with an edge from n to m do
10              visit(m)
11          mark n permanently
12          add n to head of L
```