
namedtuple
======

[<<<](https://github.com/ttltrk/PRG/blob/master/PY/DOC/OPYM/07_MOD_PACK/MOD_PACK/MOD_PACK.MD)

[jupyter](https://nbviewer.jupyter.org/github/jmportilla/Complete-Python-Bootcamp/blob/master/Collections%20Module.ipynb)

```python
t = (1, 2, 3)

print(t[0])

>>>
1
>>>
```


```python
from collections import namedtuple

Dog = namedtuple('Dog', 'age breed name')
sam = Dog(age=2, breed='Lab', name='Sammy')

Cat = namedtuple('Cat', 'fur claws name')
c = Cat(fur='Fuzzy', claws=False, name='Kitty')

print(sam)
print(sam.age)
print(sam[0])
print(sam[1])

print(c)
print(c.name)
print(c[2])

>>>
Dog(age=2, breed='Lab', name='Sammy')
2
2
Lab
Cat(fur='Fuzzy', claws=False, name='Kitty')
Kitty
Kitty
>>>
```
