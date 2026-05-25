# Date: 2026-05-25
## Topic
Deep clone task (recursion)

## What I Did
Finished implementation of deep clone

## Problems / Challenges
- Implementing correct deep copy behavior for methods while preserving this context (Still not sure how to do it correctly)
- Handling getters/setters correctly (Not sure as well)
- Adding WeakMap to support circular references
- Is it really worth to copy all of descriptors for Objects? How this done in real projects?
- Date object - value storage?

## Solutions / Attempts
- WeakMap to track visited objects
- Decided to copy functions by copying references or wrapping them with apply method
- Used Object.getOwnPropertyDescriptors and Object.defineProperty to copy all values with descriptors and getters/setters
- Tested behavior for object from task and additional tests to check more complicated functionality.

## What I Learned
- Property selection: Object.getOwnPropertyNames(obj) - string key properties (with non-enumerable). Object.getOwnPropertySymbols(obj) - symbol key properties
(not in scope of task), Object.getOwnPropertyDescriptors(obj) - full metadata (all descriptors of obj)
- Objects, Functions, Arrays have a lot in common, but still have differences. Pattern how to deal: create different shells and then copy properties in a common way
(DRY principle - one common function for copying descriptors)
- Getter/setter exist as property descriptors
- Sparse arrays (with holes, not undefined values)

## Time Spent
~5 hours of coding + paperwork (writing PR and diary)
