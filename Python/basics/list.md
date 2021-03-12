# List & Tuple
## list.pop(indedx)
removes and returns the element at the given index.
without the index, list.pop() removes and return the last element
```python
>>> list = [1,2,3,4]
>>> list.pop(2)
3
>>> list
[1, 2, 4]
>>> list.pop()
4
>>> list
[1, 2]
```
## list.remove(elem)
searches and removes the first instance of the given element and removes it
throws ValueError is not present
```python
>>> list = [1,2,3,4,5,1,2,3]
>>> list.remove(2)
>>> list
[1, 3, 4, 5, 1, 2, 3]
>>> list.remove(0)
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
ValueError: list.remove(x): x not in list
```
## list[start:end]
can be used to replace elements (must be iterable)
```python
>>> list = ['1', '2', '3', '4', '5']
>>> list[1:5] = '0'
>>> list
['1', '0']
```
```python
>>> list = [1,2,3,4,5]
>>> list[1:5] = 0
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError: can only assign an iterable
>>> list[1:5] = [0]
>>> list
[1, 0]
```
## list.sort() & sorted(list)
```python
>>> list1 = [2,3,1,5,4]
>>> list1.sort()
>>> list1
[1, 2, 3, 4, 5]
>>> list1.sort(reverse = True)
>>> list1
[5, 4, 3, 2, 1]
>>> list2 = sorted(list1)
>>> list2
[1, 2, 3, 4, 5]
```
use key=func as custom sorting, the func() must return a proxy value which can be sorted
```python
>>> def sort(s):
...     return len(s)
>>> list = ['a', 'ccc', 'bb', 'dddd']
>>> list2 = sorted(list, key=sort)
>>> list2
['a', 'bb', 'ccc', 'dddd']
```
```python
>>> list = ['a', 'ccc', 'dddd', 'bb']
>>> list2 = sorted(list, key=len)
>>> list2
['a', 'bb', 'ccc', 'dddd']
```
```python
>>> list = ['a', 'Bb', 'bB', 'aA', 'AA']
>>> list2 = sorted(list, key=str.lower)
>>> list2
['a', 'aA', 'AA', 'Bb', 'bB']
```
## [expr for var in lsit]
```python
>>> nums = [1,2,3,4]
>>> square = [n*n for n in nums]
>>> square 
[1, 4, 9, 16]
>>> small = [n for n in nums if n<3]
>>> small
[1, 2]
```
## single tuple
```python
>>> tuple = (1, )
>>> tuple
(1,)
>>> len(tuple)
1
```
