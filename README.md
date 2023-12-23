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
## Get pandas.read_csv to read empty values as empty string instead of nan
[stackoverflow](https://stackoverflow.com/questions/10867028/get-pandas-read-csv-to-read-empty-values-as-empty-string-instead-of-nan)

```
pd.read_csv('test.csv', keep_default_na=False)
```
