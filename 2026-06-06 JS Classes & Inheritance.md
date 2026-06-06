# Date: 2026-06-06
## Topic
JS Classes & Inheritance

## What I Did
Implemented task using ES6 classes, ES5 function + prototype and Lazy evaluation.

## Problems / Challenges
- Lazy evaluation
- ES5 style vs ES6 style
- How to deal with edge cases or invalid inputs when there are no requirements?

## Solutions / Attempts
- Lazy evaluation: store called functions in the array (queue), get method triggers calling methods from the queue
one after another passing calculated value further.
- ES5 style is more complicated, methods should be added to Class.prototype = ... while static methods
should be attached directly to the class Class.staticMethos = ...
- Edge cases: decision to follow common sense and some default behaviour.

## What I Learned
Lazy evaluation and how to implement it.
Closure mechanism appears not only when function returns a function, but also in other cases.
Refreshed knowledge about Classes and inheritance in JS.

## Time Spent
~3.5 hours
