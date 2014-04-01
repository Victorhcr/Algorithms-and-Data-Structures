Merge Sort
----
<p>

```sh
1    function quicksort(array)
2        if length(array) ≤ 1
3            return array  // an array of zero or one elements is already sorted
4        select and remove a pivot element pivot from 'array'  // see '#Choice of pivot' below
5        create empty lists less and greater
6        for each x in array
7            if x ≤ pivot then append x to less
8            else append x to greater
9        return concatenate(quicksort(less), list(pivot), quicksort(greater)) // two recursive calls
```