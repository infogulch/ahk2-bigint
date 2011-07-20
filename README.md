BigInt
======

Arbitrary precision integer library for AutoHotkey v2 (alpha)

Requirements
============

These are the requirements for all changes.

* A user function may NOT modify `this` or any args passed. Use 
  `obj.clone()` or `new BigInt(...)` instead, and `return` a 
  new BigInt object
* Any additions or changes to the library must pass all current 
  unit tests, include unit tests relevant to the change,
  AND prove that it does not modify the original objects.
  (see BigIntUnitTest.ahk2 for examples)
* If possible, accept arguments that can be either BigInt 
  instances OR normal ahk numbers.