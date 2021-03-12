# Dict
## dict.get(key)
if key is not in dict, returns a None
dict.get(key, default_value) to specify a default value
```python
>>> dict = {1:'a', 2:'b', 3:'c'}
>>> dict.get(4)
>>> value = dict.get(4)
>>> print(value)
None
>>> value2 = dict.get(4, 'default')
>>> value2
'default'
>>> dict
{1: 'a', 2: 'b', 3: 'c'}
```
## dict.items()
```python
>>> dict
{1: 'a', 2: 'b', 3: 'c'}
>>> dict.items()
[(1, 'a'), (2, 'b'), (3, 'c')]
```
## % operator
% operator can substitue values from a dict into a string by name
```python
>>> hash = {}
>>> hash['word'] = 'paper'
>>> hash['count'] = 42
>>> hash[2] = 's'
>>> hash
{'count': 42, 2: 's', 'word': 'paper'}
>>> s = 'I want %(count)d copies of %(word)s' % hash
>>> s
'I want 42 copies of paper'
>>> s = 'I want %(count)d copies of %(word)s and %(2)s' % hash
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
KeyError: '2'
```
