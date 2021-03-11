# String
## s.join(list)
opposite of split(), joints the elements in the give list together using the string s as the delimiter
```python
>>> s = '-'
>>> list = ['aa', 'bb', 'cc']
>>> s.join(list)
'aa-bb-cc'
```
## s.split(char)
without char, s.split() will split on al whitespace chars
```python
>>> s = 'aa bb cc'
>>> s.split()
['aa', 'bb', 'cc']
```
## s.strip()
returns a string with whitespace removed from the start and end
```python
>>> s = ' aabbcc '
>>> s.strip()
'aabbcc'
```
## s[start:end]
for elements [start, end)
```python
>>> s = 'abcdef'
>>> s[1:4]
'bcd'
```
if start and end is empty, like s[:], it returns a copy of the entire original string. (A pythonic way to copy a sequence like string or list)
```python
>>> s = 'abcdef'
>>> s[:]
'abcdef'
```
This works even for negative n or n out of bounds: `s[n:] + s[:n] == s`
## String Formatting
* %s: string or object can be formatted as a string
* %d: integer
* %f: float

```python
>>> name = 'hafei'
>>> "Hello %s" % name
'Hello hafei'
```
```python
>>> list = [1, 2, 3]
>>> "The list is %s" % list
'The list is [1, 2, 3]'
```
```python
>>> name = 'hafei'
>>> age = 18
>>> "%s is %d years old" % (name, age)
'hafei is 18 years old'
```
```python
>>> name = 'hafei'
>>> money = 6.66
>>> "%s has only $%f" % (name, money)
'hafei has only $6.660000'
```
## Unicode string
A unicode string is a different type of object from regular "str" string, but the unicode string is compatible (they share the common superclass "basestring"), and the various libraries such as regular expressions work correctly if passed a unicode string instead of a regular string.
```python
>>> ustring = u'A unicode \u018e string \xf1'
>>> ustring
u'A unicode \u018e string \xf1'
```
## Loop string
The string acts like a list of its chars
```python
>>> s = 'abcde'
>>> for char in s: print char
... 
a
b
c
d
e
```
