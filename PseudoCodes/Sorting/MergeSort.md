Merge Sort
----
<p>

```sh
1   # split in half
2   m = n / 2
3
4   # recursive sorts
5   sort a[1..m]
6   sort a[m+1..n]
7
8   # merge sorted sub-arrays using temp array
9   b = copy of a[1..m]
10  i = 1, j = m+1, k = 1
11  while i <= m and j <= n,
12      a[k++] = (a[j] < b[i]) ? a[j++] : b[i++]
13      → invariant: a[1..k] in final position
14  while i <= m,
15      a[k++] = b[i++]
16      → invariant: a[1..k] in final position
```