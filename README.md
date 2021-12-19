# Python-Intro3

## Operators
* Operator is operations pseudonym
* Operators type:
  1. `Unary` - 1 operand, Example: -number
  2. `Binary` - 2 operand, Example: number1 + number2
  3. `Ternary` - 3 operand, Example: x if condition else y

## Ternary if
x if condition else y, if condition is true that x, else y

## Numbers Operators
Like many other languages supports operators for working with numbers: +, -, *, /, %, **, etc.
Operators have priority (* has higher priority than +),
() can be used for grouping operations

## Division Operator
There are 2 types of division:
1. / - division that result floating point
2. // - division that rounds result down to integer if operands are whole numbers and results floating-point in other case.

## Expressions of Mixed Types
* Python expressions can include numbers of different types than values are converted to the most complex type from them.
* Complexity rule: int < float < complex

## Booleans
* Bool type has 2 values: True and False
* True and False are just 1 and 0 with some additional features
* Other values can be converting to boolean using truth testing procedure with bool() function
* By default, an object is considered true unless its class defines either a __ bool __ method that returns False or 
__ len __() method that returns zero
* bool is subclass for int

## Boolean Expression
* Logicsl expressions using comparison operators
* Comparison operators: >, <, ==, !=
* We can use mixed types of numbers for comparison

## Boolean Specific Operators
* and 
* or
* not

## Complex Comparison
* Python allows to compound comparison operators
* It allows to check the range

## False Values (Falsy)
* None, False, Zero of any numeric type, Empty sequences and collections

## Unfixed size whole numbers
* Python allows declaring as big whole numbers as memory allows.

## Numbres of Different Notations
* Python store number by default in decimal notation, but also allows to store numbers in hexadecimals, octal or binary
notations.

## Operators Overriding
* Each operator can perform different operation in case of different type values
* We can override operator for our custom type to define how it will perform
* Overriding is based on polymorphism.

## Decimals
* Decimals - allows defining floating-point numbers with fixed number of digits after dot.
* To use decimals we need first import module
* Simple float has problems with results because of hardware limitations, in this cases decimals also can be useful

## Fraction
* Fraction - allows to define rational numbers (numerator and denominator)
* First we need to import module
* We can perform mathematical expressions for such valeus using =, -, etc.

## External Numeric Libraries
Numpy - is one of the powerful external libraries for performing different operation with vectors, matrixes, etc.

## None vs NaN vs Undefined
* if variable doesn't exist (not defined or deleted) it is undefined
* When variable is created it can have value, be NaN or None
* Working with undefined variable generates error, thus better to assign None or np.nan if we don't have the value yet.

## Container Data Types
* Objects that can contain reference to other objects are called container objects
* Array type objects are container objects

## Array
* Array - is ordered sequence of elements
* Array components:
  1. Index (starts from 0)
  2. Elements
* Python arrays main representation are Strings, Lists, Tuples

## Lists
* List - is ordered flexible (mutable) array of objects that can have different types
* List size is flexible
* List can be modified

## Extended Slicing (Defining step)
* We can define the step with which elements will be extracted to subarray from original array
* arr[start:end:step] - extract elements from start to end indexes with step

## Lists Mutability
* Lists are mutable, so they can be modified
* When modifying the list itself is changed
* list() function allows to create a list from iterable object.

## Memory Handling in Python
* Python Interpreter mostly manages the memory
* We should not reserve memory, clear memory, etc.
* Python deletes unwanted object (built-in types or class instances) automatically to free the memory space. The process
by which Python periodically frees and reclaims blocks of memory that no longer are in use is called Garbage Collection

## Memory Addressing Management
* Besides returning unique object identifier id() returns starting address working with CPython
* Python doesn't support pointers (variables that store addresses of another variable)
* In pypy on Jython it's just identifier

## == vs is
* == compares string character by character
* is compare the identifier

## References to object
* one object can have multiple references to it

## Increasing/Decreasing Object references count
* An object's reference count increases when it is assigned a new name of placed in a container (list, tuple, dictionary)
* The object's reference count decrease when it's deleted with del, it's reference is reassigned, or its reference goes
out of scope
* Local identifiers are automatically deleted
* Global identifiers should be freed manually (decrease global identifiers' usage)

## How GC decides to remove object
* GC checks if references count is 0
* GC also checks if existing references are cyclical references (object refers to itself, then counter will never be 0 
and memory leaks are possible if not to check such situation)

## Garbage Collector checking Regularity
* New objects are checked very often
* not so new objects are checked more rarely
* old objects are checked very rarely

## Memory Optimization: Python Interning
* Interning is re-using the object on-demand instead of creating new objects.
* The CPython implementation of Python pre-allocates shared values, certain ranges of commonly-used immutable types.
* When Python is instructed to instaintiate a new immutable object, it first checks to see if an identical object already
exists as a shared object.

## Strings Interning Runtime/Compile Time
* A string will not be interned unless it is loaded at compile time as a constant string. This includes strings defined
as expressions - remember that an expression is evaluated first before an object is instantiated.
* Any string constructed at runtime will not be interned.

## Mutable/Immutable object IDS
* The value of an immutable (unchangeable) object is tied to its identity - if the value changes, the object changes
* The value of a mutalbe (changeable) object is not tied to its identity - identity is retained across changes made to
the object.