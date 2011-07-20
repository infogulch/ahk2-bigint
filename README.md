BigInt
======

Arbitrary precision integer library for AutoHotkey v2 (alpha)

Requirements
============

These are the requirements for all changes.

* A user function may NOT modify `this` or any args passed. Use 
  `obj.clone()` or `new BigInt(...)` instead, and `return` a 
  different BigInt object
* Any additions or changes to the library must pass all current 
  unit tests, include unit tests relevant to the change,
  AND prove that it does not modify the original objects.
  (see BigIntUnitTest.ahk2 for examples)
* If possible, accept arguments that can be either BigInt 
  instances OR normal ahk numbers.
  
Usage Examples
==============

Regular Math:

    x := new BigInt(55)
    
    MsgBox % x.div(new BigInt(5)).__string()
    
    MsgBox % x.mult(33).__string()
    
    y := new BigInt(0x800)
    
    MsgBox % y.shl().__string()
    
    MsgBox % y.shr().__string()
    

Take a really big number, and square it a bunch of times: 

    x := new BigInt("abcdef123456789", "hex")
    
    loop 10
        x := x.pow(2)
        
    msgbox % x.__string()
