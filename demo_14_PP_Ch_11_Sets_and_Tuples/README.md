<<<<<<< HEAD
# PP_Ch_11_Set_Tuple_Dict

# Storing Data Using Other Collection Types

## Storing Data Using Sets

=======
# Chapter 11: Storing Data Using Other Collection Types

By now, we have some experience with collections of data 
such as lists and arrays. 
In this session, we will consider other types of data collections. 
We will focus on sets and tuples and postpone the material on dictionaries 
as an introduction to databases. 

## Storing Data Using Sets

A *set* is an *unordered* collection of *distinct* items. 
That a set is *unordered* means that all that matters is that 
an element is either in the set or it is not: 
you do not index the values along a sequence of, say, integers, 
as you would with lists. 
That the elements are *distinct* means that there are no duplicates:
all that matters is whether an element is in the set--a binary relationship-- 
as there is no sense of the strength or degree of membership. 

In python, the type called a *set* allows us to store 
*mutable* collections of unordered items.
An example is the set of strings representing the lower-case vowels. 
>>>>>>> b547526f67c43d0fe65376f280e8f2e31939c3e0

```python 
>>> vowels = {'a', 'e', 'i', 'o', 'u'}
>>> vowels
{'a', 'u', 'o', 'i', 'e'}
<<<<<<< HEAD

``` 

=======
``` 

If the elements are repeated in the definition of the set, 
python organizes the set in an efficient way,
to contain only the information that defines a set. 

>>>>>>> b547526f67c43d0fe65376f280e8f2e31939c3e0
```python 
>>> vowels = {'a', 'e', 'a', 'a', 'i', 'o', 'u', 'u'}
>>> vowels
{'u', 'o', 'i', 'e', 'a'}
<<<<<<< HEAD

``` 

=======
``` 

The duplicate vowels ```'a'``` and ```'u'``` are anly listed once each. 
Moreover, the two sets are considered equal: 
>>>>>>> b547526f67c43d0fe65376f280e8f2e31939c3e0

```python 
>>> {'a', 'e', 'i', 'o', 'u'} == {'a', 'e', 'a', 'a', 'i', 'o', 'u', 'u'}
True
<<<<<<< HEAD

``` 






=======
``` 

The variable ```vowels``` refers to an object of type ```set```.
>>>>>>> b547526f67c43d0fe65376f280e8f2e31939c3e0



```python 
>>> type(vowels)
<class 'set'>
>>> type({1, 2, 3})
<class 'set'>
<<<<<<< HEAD
>>> type({})
<class 'dict'>
=======
```

Although braces, the ones that look like curly brackets ```{}```,
are often used to represent sets on the blackboard, 
these are used to define *dictionaries* in python. 
We will talk about these later, before we introduce databases. 

```python 
>>> type({})
<class 'dict'>
``` 

As an alternative notation, python reserves a function called ```set()``` to define sets. 


```python 
>>>>>>> b547526f67c43d0fe65376f280e8f2e31939c3e0
>>> set()
set()
>>> type(set())
<class 'set'>
<<<<<<< HEAD

``` 
=======
``` 
As with other objects, there exists an empty set.
>>>>>>> b547526f67c43d0fe65376f280e8f2e31939c3e0

```python 
>>> set()
set()
``` 
<<<<<<< HEAD
=======
The ```set``` function expects either no arguments 
or a single argument that is some collection of objects, 
such as a list. 
>>>>>>> b547526f67c43d0fe65376f280e8f2e31939c3e0


```python 
>>> set([2, 3, 2, 5])
{2, 3, 5}
``` 
<<<<<<< HEAD

=======
Perhaps, somewhat confusingly, the set itself is printed to screen in braces, 
as it would be in standard mathematical notation. 

If you try to pass multiple arguments, python will throw an error. 
>>>>>>> b547526f67c43d0fe65376f280e8f2e31939c3e0

```python 
>>> set(2, 3, 5)
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError: set expected at most 1 arguments, got 3

``` 

<<<<<<< HEAD

=======
Again, ```set``` is fine with a list and, as above, 
the repeated values are eliminated. 
>>>>>>> b547526f67c43d0fe65376f280e8f2e31939c3e0

```python 
>>> set([3, 5, 2])
{2, 3, 5}
>>> set([2, 3, 5, 5, 2, 3])    
{2, 3, 5}
``` 
<<<<<<< HEAD
=======
In a diagram in page 204 of *Practical Programming*, 
we see that the duplicate instances of elements point to the same 
locations in memory as the first instance of each one, 
thus reducing the memory required to store the set. 

You can also pass other types of collections, 
including dictionaries, defined by braces ```{}```, 
and, again, the notation is somewhat confusing, 
with the double meaning of braces. 
>>>>>>> b547526f67c43d0fe65376f280e8f2e31939c3e0

```python 
>>> vowels = {'a', 'e', 'a', 'a', 'i', 'o', 'u', 'u'}
>>> vowels
{'i', 'a', 'u', 'e', 'o'}
>>> set(vowels)
{'i', 'a', 'u', 'e', 'o'}
>>> set({5, 3, 1})
{1, 3, 5}

``` 
<<<<<<< HEAD

=======
A ```range``` object can also be converted to a set. 
>>>>>>> b547526f67c43d0fe65376f280e8f2e31939c3e0

```python 
>>> set(range(5))
{0, 1, 2, 3, 4}
``` 

<<<<<<< HEAD

### Set Operations



=======
Later, we will introduce the type *tuples*, which you can also pass to ```set```, 
but by now, you get the idea. 


### Set Operations

Now that you have a set in memory, what can you do with it? 
Python provides a number of operations to change the contents of a set. 
In essence, these commands take advantage of the fact that sets are *mutable*. 

For example, you might recall from grade-school grammar class that 
the set of vowels includes the first five and sometimes  ```'y'```.
>>>>>>> b547526f67c43d0fe65376f280e8f2e31939c3e0

```python 
>>> vowels = {'a', 'e', 'i', 'o', 'u'}
>>> vowels
{'o', 'u', 'a', 'e', 'i'}
>>> vowels.add('y')
>>> vowels
{'u', 'y', 'e', 'a', 'o', 'i'}
<<<<<<< HEAD

``` 


=======
``` 

Let's experiment with the following sets.
>>>>>>> b547526f67c43d0fe65376f280e8f2e31939c3e0


```python 
>>> ten = set(range(10))
>>> lows = {0, 1, 2, 3, 4}
>>> odds = {1, 3, 5, 7, 9}
<<<<<<< HEAD
>>> lows.add(9)
>>> lows
{0, 1, 2, 3, 4, 9}
>>> lows.difference(odds)
{0, 2, 4}
>>> lows.intersection(odds)
{1, 3, 9}
>>> lows.issubset(ten)
True
>>> lows.issuperset(odds)
False
>>> lows.remove(0)
>>> lows
{1, 2, 3, 4, 9}
>>> lows.symmetric_difference(odds)
{2, 4, 5, 7}
>>> lows.union(odds)
{1, 2, 3, 4, 5, 7, 9}
>>> lows.clear()
>>> lows
set()

``` 

=======
```

As above, you can add elements to a set.

```python 
>>> lows.add(9)
>>> lows
{0, 1, 2, 3, 4, 9}
```

The ```difference``` method finds the elements of one set that are not in another.

```python 
>>> lows.difference(odds)
{0, 2, 4}
```
As in set theory, the intersection of two sets is the set of
elements that are in both sets. 

```python 
>>> lows.intersection(odds)
{1, 3, 9}
```

You can determine whether one set is a subset of another
with the ```issubset``` method. 

```python 
>>> lows.issubset(ten)
True
```

You can determine whether one set contains all of another set's items. 

```python 
>>> lows.issuperset(odds)
False
```
but

```python 
>>> ten.issuperset(lows)
True
```

Instead of adding elements, you can remove elements. 

```python 
>>> lows.remove(0)
>>> lows
{1, 2, 3, 4, 9}
```

The symmetric difference returns a set of elements that are each on 
exactly *one* of the two sets, i.e., not in the intersection of the sets. 

```python 
>>> lows.symmetric_difference(odds)
{2, 4, 5, 7}
```

You can form the union of two sets, which will include all elements
of both sets. 

```python 
>>> lows.union(odds)
{1, 2, 3, 4, 5, 7, 9}
```

Finally, you can rest a set to the empty set with the ```clear``` method. 

```python 
>>> lows.clear()
>>> lows
set()
``` 

We have already seen some of these operations in action:
some perform the same function as boolean operators.
Some other operators also work with sets. 

>>>>>>> b547526f67c43d0fe65376f280e8f2e31939c3e0
```python 
>>> lows = set([0, 1, 2, 3, 4])
>>> odds = set([1, 3, 5, 7, 9])
>>> lows - odds            # Equivalent to lows.difference(odds)
{0, 2, 4}
>>> lows & odds            # Equivalent to lows.intersection(odds)
{1, 3}
>>> lows <= odds           # Equivalent to lows.issubset(odds)
False
>>> lows >= odds           # Equivalent to lows.issuperset(odds)
False
>>> lows | odds            # Equivalent to lows.union(odds)
{0, 1, 2, 3, 4, 5, 7, 9}
>>> lows ^ odds            # Equivalent to lows.symmetric_difference(odds)
{0, 2, 4, 5, 7, 9}

``` 

### Set Example: Arctic Birds

<<<<<<< HEAD

=======
In this example, we have a file of observations of birds in the Canadian Arctic. 
The file ```observations.txt``` has one species per line. 
>>>>>>> b547526f67c43d0fe65376f280e8f2e31939c3e0

```python 
canada goose
canada goose
long-tailed jaeger
canada goose
snow goose
canada goose
long-tailed jaeger
canada goose
northern fulmar
<<<<<<< HEAD

``` 

=======
``` 

The following program reads each line, strips the leading and trailing whitespace
and adds the species on that line to the set.

Notice the type annotation ```Set[str]```, 
which indicates that the function returns a set of strings. 
>>>>>>> b547526f67c43d0fe65376f280e8f2e31939c3e0

```python 
from typing import Set, TextIO
from io import StringIO

def observe_birds(observations_file: TextIO) -> Set[str]:
    """Return a set of the bird species listed in observations_file, which has
    one bird species per line.

    >>> infile = StringIO('bird 1\\nbird 2\\nbird 1\\n')
    >>> birds = observe_birds(infile)
    >>> 'bird 1' in birds
    True
    >>> 'bird 2' in birds
    True
    >>> len(birds) == 2
    True
    """
    birds_observed = set()
    for line in observations_file:
        bird = line.strip()
        birds_observed.add(bird)

    return birds_observed

if __name__ == '__main__':
    import doctest
    doctest.testmod()
    with open('observations.txt') as observations_file:
        print(observe_birds(observations_file))

``` 

<<<<<<< HEAD
=======
The resulting set has only four species.
The ```add``` operation has no effect when attempting to 
add a species that was already in the set. 

We can see the contents of the set by looping over the elements. 

>>>>>>> b547526f67c43d0fe65376f280e8f2e31939c3e0

```python 
>>> for species in birds_observed:
...     print(species)
... 
long-tailed jaeger
canada goose
northern fulmar
snow goose
``` 

<<<<<<< HEAD
### Set Contents Must Be Immutable

=======
Note that there is no guarantee of the order in which the elements are printed:
not in alphabetical order, the order they were added or in any other order. 

### Set Contents Must Be Immutable

The benefit of using sets is that checking for set membership is fast. 
The fact that sets are *immutable* greatly increases 
the speed of checking for membership by employing a mathematical technique called *hashing*. 
It means, roughly speaking, that the elements in the set 
are each indexed by a certain lookup code, that works behind the scenes in python. 


A by-product of this design restriction is that 
you can't make sets of items that are themselves mutable, such as lists. 

>>>>>>> b547526f67c43d0fe65376f280e8f2e31939c3e0

```python 
>>> S = set()
>>> L = [1, 2, 3]
>>> S.add(L)
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError: unhashable type: 'set'
<<<<<<< HEAD

``` 


## Storing Data Using Tuples

=======
``` 

This restriction also means that we can't store sets of sets. 
You can, however, use what is called a *frozen set*, 
which means that you commit to the restriction that the 
individual elements of the set cannot be mutated, 
even though their type would normally be mutable. 


## Storing Data Using Tuples

Lists aren't the only kind of ordered sequence in python. 
You have already learned to work with strings. 
Recall that a string is also an immutable sequence of characters. 
These characters are ordered and a string can be indexed and sliced 
like a list to create new strings. 
>>>>>>> b547526f67c43d0fe65376f280e8f2e31939c3e0

```python 
>>> rock = 'anthracite'
>>> rock[9]
'e'
>>> rock[0:3]
'ant'
>>> rock[-5:]
'acite'
>>> for character in rock[:5]:
...     print(character)
...

a
n
t
h
r

``` 

<<<<<<< HEAD
=======
By now, many of you may have inadvertently used *tuples*, 
perhaps without realizing it. 
Tuples are defined with parentheses, 
in contrast to the [square] brackets used to define lists.

Tuples are also immutable and, like strings and lists, 
they can also be subscripted, sliced and looped-over. 

>>>>>>> b547526f67c43d0fe65376f280e8f2e31939c3e0
```python 
>>> bases = ('A', 'C', 'G', 'T')
>>> for base in bases:
...     print(base)
... 
A
C
G
T
``` 
<<<<<<< HEAD

=======
But there's a catch: 
Although empty parentheses ```()``` represent an empty tuple, 
a tuple with one element is not represented by ```(x)``` but rather ```(x,)```. 
The extra comma distinguishes the tuple ```(x,)``` from the bracketed operation
that might calculate an element, such as between ```(2+2,)``` and ```(2+2)```:
one produces a set with one element, the other produces an integer. 
>>>>>>> b547526f67c43d0fe65376f280e8f2e31939c3e0

```python 
>>> (8)   
8
>>> type((8))
<class 'int'>
>>> (8,)
(8,)
>>> type((8,))
<class 'tuple'>
>>> (5 + 3)
8
>>> (5 + 3,)
(8,)
<<<<<<< HEAD

``` 


=======
``` 

Unlike lists, however, once a tuple is created, it cannot be mutated. 
>>>>>>> b547526f67c43d0fe65376f280e8f2e31939c3e0


```python 
>>> life = (['Canada', 76.5], ['United States', 75.5], ['Mexico', 72.0])
>>> life[0] = life[1]
Traceback (most recent call last):
  File "<stdin>", line 1, in ?
TypeError: object does not support item assignment
<<<<<<< HEAD

``` 

=======
``` 

Compare that tuple to the following list. 

>>>>>>> b547526f67c43d0fe65376f280e8f2e31939c3e0
```python 
>>> life = (['Canada', 76.5], ['United States', 75.5], ['Mexico', 72.0])
>>> life[0][1] = 80.0
>>> life
(['Canada', 80.0], ['United States', 75.5], ['Mexico', 72.0])
<<<<<<< HEAD

``` 

=======
``` 

It looks the same on the surface, but the mutability costs in terms of memory use
and computing time. 
It's a trade-off between speed and flexibility. 

Consider the following lists.
>>>>>>> b547526f67c43d0fe65376f280e8f2e31939c3e0

```python 
>>> canada = ['Canada', 76.5]
>>> usa = ['United States', 75.5]
>>> mexico = ['Mexico', 72.0]
<<<<<<< HEAD
=======
```
Now, assemble them into a tuple. 

```python
>>>>>>> b547526f67c43d0fe65376f280e8f2e31939c3e0
>>> life = (canada, usa, mexico)
>>> mexico = ['Mexico', 72.5]
>>> life
(['Canada', 76.5], ['United States', 75.5], ['Mexico', 72.0])
<<<<<<< HEAD
>>> life[0][1] = 80.0
>>> canada
['Canada', 80.0]

``` 


### Assigning to Multiple Values Using Tuples

=======
```

When we tried to change one of the items, the change was ignored. 
We can't switch the object that the list item refers to in memory, 
when we change it after the tuple is formed. 
When a tuple is created, it creates a copy of the items in a separate, 
specifically-designed place in memory. 

On the other hand, we can change the value of the item in the list, 
by accessing it through the index numbers of the list items. 


```python
>>> life[0][1] = 80.0
>>> canada
['Canada', 80.0]
``` 
Then the change was made to the opject in memory containing the list ```Canada```.
The rules are different for each type of collections of objects.
This additional complexity pays off in the flexibility
to choose python objects that are best suited to your application. 

### Assigning to Multiple Values Using Tuples

Tuples are useful for many shorthand coding practices.
One of these is the simultaneous assignment to multiple variables. 
>>>>>>> b547526f67c43d0fe65376f280e8f2e31939c3e0

```python 
>>> (x, y) = (10, 20)
>>> x
10
>>> y
20
<<<<<<< HEAD
=======
```
Items separated by a comma are recognized as a tuple. 
Placing a tuple on both sides makes the simultaneous assignment. 

```python 
>>>>>>> b547526f67c43d0fe65376f280e8f2e31939c3e0
>>> 10, 20
(10, 20)
>>> x, y = 10, 20
>>> x
10
>>> y
20
<<<<<<< HEAD
=======
```

Furthermore, multiple assignments work with combinations of lists and sets. 
Python will pull apart the information from any collection. 

```python 
>>>>>>> b547526f67c43d0fe65376f280e8f2e31939c3e0
>>> [[w, x], [[y], z]] = [{10, 20}, [(30,), 40]]
>>> w
10
>>> x
20
>>> y
30
>>> z
40
<<<<<<< HEAD
=======
```
One of the most common applications is that
you can swap assignments between two variables simultaneously.

```python 
>>>>>>> b547526f67c43d0fe65376f280e8f2e31939c3e0
>>> s1 = 'first'
>>> s2 = 'second'
>>> s1, s2 = s2, s1
>>> s1
'second'
>>> s2
'first'
<<<<<<< HEAD

``` 

=======
``` 
Without this capability, you might otherwise use a temporary third variable
to store one item while you assign it to have the other. 
>>>>>>> b547526f67c43d0fe65376f280e8f2e31939c3e0



## Using the ```in``` Operator on Tuples and Sets

<<<<<<< HEAD
=======
On a final note, let's revisit the ```in``` operator. 
This works for sets and tuples just as it does for lists, 
and other types we will encounter elsewhere. 

As we have seen before, the ```in``` operator 
returns a boolean variable that indicates 
whether the object in the left operand
is an element of the collection of objects in the right operand. 
>>>>>>> b547526f67c43d0fe65376f280e8f2e31939c3e0


```python 
>>> odds = set([1, 3, 5, 7, 9])
>>> 9 in odds
True
>>> 8 in odds
False
>>> '9' in odds
False
>>> evens = (0, 2, 4, 6, 8)
>>> 4 in evens
True
>>> 11 in evens
False
<<<<<<< HEAD

``` 
=======
``` 

>>>>>>> b547526f67c43d0fe65376f280e8f2e31939c3e0
