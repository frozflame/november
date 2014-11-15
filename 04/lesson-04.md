
Lesson 4
--------

Today we talk about logic control.







Let's loop. But wait. Python is different.

#### List ####

These are containers. For example

    names = ['Alice', 'Bob', 'Cecilia', 'Sophie']
    
is a list contains three items: `'Alice'`, `'Bob'` and `'Sophie'`. You can get
the first member with

    names[0]

and the second

    names[1]

and the last

    names[-1]

Note that the indexes (numbers in the brackets, `[]`) start from zero, resembling C/C++. There are many
advantages using zero-based indexes, which will be talked later.

You can add more items to an existing list

    names.append('John')
    names.append('Ray')
    names.insert(0, 'Albert')
    names.insert(0, 'Lucy')
    
You can add two lists

    names + ['James', 'Jack']

Another thing you should learn about lists are called _slicing_. It selects a
contiguous portion of an existing list.

    names[0:3]
    names[1:3]
    names[:3]
    names[1:]

=======================================

#### for-loop ####

Python's for-loop is different from C/C++. It is easier to write and more
elegent to read. Simple example

    for name in names:
        print("Hello", name)

Same story for numbers

    for i in [3, 6, 9]:
        print(i**2)

But what if I want `i` to loop from 0 to 1000? A function named `range` will
help you

    for i in range(1000):
        print(i**2)

Here, `range(1000)` returns a list-like object, which behaves almost identical
to `[0, 1, 2, ..., 999]`. Note that 0 is included but 1000 is not.

=======================================

#### True or False ####

Similar to many other languages, including C/C++, Python has while-loops.

    while <condition>:
        ...
         



In Python, all integers except 0 is considered True




