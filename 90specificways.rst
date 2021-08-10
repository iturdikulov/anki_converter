idioms, language
================
The idioms of programming language are defined by its {{c1::users}}

.. answer

The idioms of programming language are defined by its users

A programming idiom is the usual way to code a task in a specific language

pep, lay-out
============
Which PEP (Python Enhancement Proposals) code lay-out know?

.. answer

* lines should be 79 characters or less
* continuations of long expressions onto additional lines should be indented by 4 extra spaces
* functions and classes separated by 2 blank lines

pep, naming
===========
Which PEP (Python Enhancement Proposals) naming conventions you know?

.. answer

* functions, variables and attributes - lowercase
* protected instance attributes - _leading_underscore
* private instance attributes - __double_leading
* classes - Capitalized
* module-level constants - ALL_CAPS
* instance methods - should use self
* class methods - should use cls

expressions, statements
======================
How format expressions and statements?

.. answer

* use inline negotiation if a is not b (instead if not a is b)
* don't check for empty containers or sequences by length
* avoid single line statements
* split long lines (> 79 characters)
* prefer surrounding with parentheses

imports
=======
How deal with imports?

.. answer

* place imports at the top of a file
* always use absolute names for modules - from ... import ..., instead relative to current module
* if you must do relative import, use the explict method - from . import foo

pep
====
What benefits you receive by following PEP style guide

.. answer

Using consistent style makes it easier to modify later

utf, bytes
==========
What difference between bytes and str instances in Python 3?

.. answer

* Instances of bytes contains raw, 8-bit values - sequences of Bytes

* Instances of str contains Unicode code points - sequences of Characters

* Byte objects are in machine readable form internally, Strings are only in human readable form.

* Since Byte objects are machine readable, they can be directly stored on the disk. Whereas, Strings need encoding before which they can be stored on disk.

utf, bytes
==========
How support different encoding in typical python program? Which helpers functions you need?

.. answer

The core of your program should use str type, containing Unicode data, but can accept different encoding - Latin1, Big5 from interfaces

Use helper function to ensure the inputs you operate on are the type of character sequence that you expect

bytes
==========
If you need read and write binary data, open it in {{c1::rb}} or {{c1::rw}} mode.

.. answer

If you need read and write binary data, open it in rb or rw mode.

utf8
==========
What are the pitfalls when opening text files (with open...)?

.. answer

If you want to read or write Unicode data be careful about system encoding. Explicit pass the encoding parameter to open statement if you want to avoid surprises.

f-string
========
Which string formatting method prefer to use?
Which format you can use?

.. answer

Prefer interpolated F-Strings

* formatted = f'{key!r:<10} = {value:.2f}'
* {key!r} - raw
* {key:<10} - left order (minimal horizontal width) - 10 characters
* {value:.2f} - precision formatting
* f'my number is {number:.{places}f}' - nested formatting

F-strings are succinct yet powerful because they allow for arbitrary Python expressions to be directly embedded within format specifiers

pep
====
How deal with complex expressions?

.. answer

Write helpers functions instead of complex expressions

Move complex expressions into helper functions, especially if you need to use the same logic repeatedly

pep
====
Why recommended avoid write single line expressions?

.. answer

Python syntax makes it easy to write single line expressions that are overly complicated and difficult to read

style
=====
What prefer if/else expressions or "or/and" boolean operators in expressions?

.. answer

An if/else expression provides a more readable alternative to using the Boolean operators "or/and" in expressions.

algo
====
How you can Implement bubble sort algorithm?

.. answer

I need iterate some list, and compare adjacent elements and swap them if they are in wrong order.

unpack
======
How unpack multiple values and assign them?

.. answer

Python has special syntax called unpacking for assigning multiple values in a single statement - *

unpack
======
What can be unpacked in Python?

.. answer

Unpacking is generalized in Python and can be applied to any iterable, including many levels of iterables within iterables

unpack
======
How to avoid explicit indexing into sequences?

.. answer

Reduce visual noise and increase code charity by using unpacking to avoid explicit indexing into sequences

enumerate
=========
What providing enumerate?

.. answer

Enumerate provides concise syntax for looping over an iterator and getting the index of each itm from the iterator as you go

enumerate
=========
Which alternative prefer over a range and indexing into a sequence?

.. answer

Prefer enumerate instead of looping over a range and indexing into a sequence

enumerate
=========
You can supply a {c1::second} parameter to {c1::enumerate}

.. answer

Prefer enumerate instead of looping over a range and indexing into a sequence

zip
====
How zip function working?

.. answer

The zip built-in function can be used to iterate over multiple iterators in parallel

Zip creates a lazy generator that produced tuples, so it can be used an infinity long inputs

zip
====
What if we pass 2 different size iterator into zip function?

.. answer

Zip truncates its output silently to the shortest iterator if you supply it with iterators of different lengths

But you can use zip_longest function from itertools built-in module, if you want to use zip on iterators of unequal lengths without truncation

for
=====
How skip else block in for loop?

.. answer

Using break statement in a loop actually skips the else block

for
=====
How run else block immediately in for loop?

.. answer

Else block runs immediately if you loop over an empty sequences or loop are initially false

for
=====
Why recommended using else block in for loop?

.. answer

Avoid using else block after loops because their behavior isn't intuitive and can be confusing
