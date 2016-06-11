# parnas

## Abstract

> modularization as a mechanism for improving the flexibility and comprehensibility of a system while allowing the shortening of its development time.

> effectiveness of a "modularization" is dependent upon the criteria used in dividing the system into modules.

## Intro

Opens with a quote from:

Gauthier, Richard, and Pont, Stephen. Designing Systems
Programs, (C), Prentice-Hall, Englewood Cliffs, N.J., 1970

* well-defined segmentation of the project effort ensures system modularity
* each task forms a separate, distinct program module
* each module and its inputs and outputs are well-defined
* integrity of the module is tested independently

No one is talking about the _criteria_ that we should use to split up the system into modules.

## Status Report

Major advancement of modular programming are techniques that:

1. allow one module to be written with little knowledge of code in another module,
2. allow modules to be reassembled and replaced without reassembly of the whole system.

This is valuable for large pieces of code, but most examples of _problem systems_ are highly modularized using above techniques.

## Expected benefits of modular programming

1. managerial - less dev time. different people can work on different parts.
2. product flexibility - make drastic changes to one module without effecting others.
3. comprehensibility - possible to study the system one module at a time. whole system is thus better understood.

## What is Modularization?

def. _module_ - a responsibility assignment rather than a sub-program.

Modularizations are design decisions made before work on the modules begin.

### Ex. System 1 - KWIC Index Production System

def. KWIC Index System
input: accepts an ordered set of lines, each line is an ordered set of words, and each word is an ordered set of characters.
modifier: any line can be _circularly shifted_ by repeatedly removing the first word and appending it at the end of the line.
output: a listing of all circular shifts of all lines in alphabetical order.

Since this is a small system none of the difficulties that motivate modular programming are important for this system. For the sake of this paper it treats this as a large system.

#### Modularization 1

modules:
1. input - reads lines from input and stores them in core for processing by the other modules.
2. circular shift - called after the input module has completed work. prepares an index which gives the address of the first character of each circular shift and the original index of the line in the array from module 1. output is placed into core with words in pairs.
3. alphabetizing - takes input as arrays from modules 1 & 2. alphabetizes array.
4. output - produces nicely formatted output
5. master control - controls sequencing between other 4 modules. handles error messages, space, allocation, etc.

This is what most proponents of modular programming would mean by modularization. modules have well defined interfaces, are small enough to understand fully.

#### Modularization 2

modules:
1. Line Storage: contains a number of functions.
  `CHAR(r, w, c)` - return a value as an int representing the cth character in the wth word on the rth line.
  `SETCHAR(r, w, c, d)` - sets cwr to d
  `WORDS(r)` - returns the number of words in line r

  if restrictions are violated functions "trap" to an error handling function provided by the user of the module.

  `DELINE` and `DELWRD` are provided to delete portions of lines which have already been stored.

2. Input: reads input and calls line storage to store them internally
3. Circular Shift
4. Alphabetizer: 2 functions `ALPH` and `ITH`.
5. Output: print set of lines or circular shifts
6. Master Control: similar to modularization 1.

### Comparison of Two Modularizations

Both systems work. Both reduce to small managable modules. Differences between the 2 are the way they are divided into work assignments and the interfaces between the modules. Algorithms used may be identical.

### Changability


## Information Hiding

> the principle of segregation of the design decisions in a computer program that are most likely to change, thus protecting other parts of the program from extensive modification if the design decision is changed. The protection involves providing a stable interface which protects the remainder of the program from the implementation (the details that are most likely to change).

## Conclusion

It is almost always incorrect to begin decomposition of a system into modules on the basis of a flowchart.

Instead one should begin with a list of difficult design decisions which are likely to change. Each module then can hide those decisions from the other modules. <--- information hiding

In most cases design decisions transcend time of execution, modules will not correspond to steps in processing.

To keep things efficient we must abandon the assumption that a module is one or more functions. Instead allow programs to be assembled collections of code from various modules.
