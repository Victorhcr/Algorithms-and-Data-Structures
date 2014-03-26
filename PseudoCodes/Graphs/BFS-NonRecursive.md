Depth First Search - Recursive Version
----
<p>

```sh
1  procedure BFS(G,v) is
2      create a queue Q
3      create a vector set V
4      enqueue v onto Q
5      add v to V
6      while Q is not empty loop
7         t ← Q.dequeue()
8         if t is what we are looking for then
9            return t
10        end if
11        for all edges e in G.adjacentEdges(t) loop
12           u ← G.adjacentVertex(t,e)
13           if u is not in V then
14               add u to V
15               enqueue u onto Q
16           end if
17        end loop
18     end loop
19     return none
20 end BFS
```