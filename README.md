## Data Types

### Atomic 

`int` - integers\
`float` - numbers with a decimal point\
`bool` - either `True` or `False`

### Collection 

`str` - ordered collection of characters\
`list` - ordered collection of objects

## Mutability

The ability of a type to change its state after creation.

**Mutable**: `list`, `dict`, `set`, ...\
**Immutable**: `int`, `str`, `bool`, `float`, `tuple`, ...

## str

Strings in Python are a set of chars enclosed within `'`, `"`, `'''`, or `"""`.

```python
'I\'m a string.'
"I'm a string too!"

'''
I'm a
multi
line
string.
'''

"""
I am
one
too!
"""
```

It's possible to join multiple strings using the `+` operator.
That process is called *concatenation*.

```python
first_name = 'Harry'
last_name = 'Potter'
school = 'Hogwarts'

message = 'Welcome to ' + school + ', ' + first_name + ' ' + last_name + '!'

print(message) # Welcome to Hogwarts, Harry Potter!
```

### f strings

Allow for easier access of variable values inside a string.

> f strings were introduced in Python 3.6,
> so these won't work in earlier versions of Python.

```python
message = f'Welcome to {school}, {first_name} {last_name}!'
```

Wherever a variable's value is needed inside the string,
enclose the variable's name in flower braces.
No hassling around the plusses and spaces!

> Everything inside `{}` of an f string is evaluated to its str.

## list

An ordered collection of items.

```python
e = [] # empty list

avengers = [
    'Ant Man',
    'Iron Man',
    'Hulk',
    'Thor',
    'Wasp',
]

avengers[2] # 'Hulk'
avengers[7] # IndexError

avengers.append('Captain America') # adds CA to the list of Avengers
avengers.append('Spider Man')

avengers.remove('Wasp') # removes Wasp

avengers.insert(2, 'Hawk Eye') # adds Hawk Eye at index 2
```

## tuple

An ordered collection of items. The immutable version of a `list`.

```python
colors = ('RED', 'GREEN', 'BLUE')

colors[0] # 'RED'
colors[3] # IndexError
```

## dict

A collection of key value pairs, built on Hash Tables. Dicts do not preserve order,
but are fast at memberhip checks.

```python
e = {} # empty dict

ryuk = {
    'name': 'Ryuk',
    'type': 'God of Death',
    'age': 672,
}

ryuk['age'] # 672
ryuk['type'] # 'God of Death'
ryuk['fav_food'] # KeyError

ryuk['fav_food'] = 'Apple' # adds a new key 'fav_food' with the value 'Apple'
```

## set

Unordered collection of items that does not allow duplicates.
Same as `dict` except for the fact that it stores only the keys.

```python
e = set() # empty set

vowels = {'a', 'i', 'o', 'u', 'y'}
lower_case_letters = {'g', 'j', 'p', 'k', 'i', 'b', 'l', 'v', 't', 'x', 'u', 'n', 'f', 'y', 'z', 'w', 'd', 'o', 'h', 'e', 'c', 'r', 'q', 'm', 'a', 's'}

vowels.add('a') # does not change the set because 'a' already exists in the set
vowels.add('e') # adds 'e' to the set
vowels.remove('y') # removes 'y' from the set

vowels.intersection(lower_case_letters) # {'u', 'i', 'o', 'a', 'e'}
```


## Dynamic Typing

In Python, we never have to explicitly define a variable's type.
The interpreter decides for itself based on the value assigned to the variable.

Also, variables can change types on the fly (dynamically).

## Functions, Parameters, Arguments

```python
def say_hi(name):
    print(f'Hi, {name}!')

say_hi('Genie') # Hi, Genie!
```

`say_hi` is the *function*.
`name` is its *parameter*.
`'Genie'` is the *argument*.

> When a function is called, the parameters are given references to the arguments.
> `name` will be bound to `'Genie'`.

## Arithmetic Operators

Sign  | Function
:----:|---------
`+`   | add
`-`   | subtract
`*`   | multiply
`/`   | divide
`%`   | modulus
`//`  | integer divide
`**`  | raise to

## Slicing

A technique that allows access to a part of an indexable type (str, list, ...).

```python
message = 'Hello, world!'
natural_numbers = [1, 2, 3, 4, 5, 6, 7]

message[7:12] # 'world'
message[7:] # 'world!'
message[-1] # '!'

natural_numbers[:4] # [1, 2, 3, 4]
natural_numbers[::-2] # [7, 5, 3, 1]
```
