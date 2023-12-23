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
## How can I create a label encoder utilizing only numpy (and not sklearn LabelEncoder)?
[stackoverflow](https://stackoverflow.com/questions/60955014/how-can-i-create-a-label-encoder-utilizing-only-numpy-and-not-sklearn-labelenco)

```
arr = np.array([['hi', 'there'], ['scott', 'james'],
                ['hi', 'scott'], ['please', 'there']])

np.column_stack([np.unique(arr[:, i], return_inverse=True)[1] for i in range(arr.shape[1])])

array([[0, 2],
       [2, 0],
       [0, 1],
       [1, 2]], dtype=int64)
```
Or applying along the axis:
```
np.column_stack(np.apply_along_axis(np.unique, 0, arr, return_inverse=True)[1])
```
