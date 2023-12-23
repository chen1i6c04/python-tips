# python-tips
 This repository is about tips and tricks for using Python and its packages.

## Removing duplicates from a list of lists
[stackoverflow](https://stackoverflow.com/questions/2213923/removing-duplicates-from-a-list-of-lists)

```
>>> k = [[1, 2], [4], [5, 6, 2], [1, 2], [3], [4]]
>>> import itertools
>>> k.sort()
>>> list(k for k,_ in itertools.groupby(k))
[[1, 2], [3], [4], [5, 6, 2]]
```
