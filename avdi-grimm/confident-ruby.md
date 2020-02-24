# [Confident Code](https://www.youtube.com/watch?v=T8J0j2xJFgQ) [00:31:24] by **Avdi Grimm** (2012)

Every method does:
1-Gather Input
2-Perform Work
3-Deliver Result
4-Handling Errors

-----------------------

1-Gather Input
  * Duck typing is treat the object as a duck, assumes that if is not it will complaint
  * The opposite of dick typing is switch statement smell
  * How can my method trust that input objects(or data) allways respond to the interface I need?

  If you find yourself doing these __over the input__:
    * Switch over a type of an object
    * Checking for method existence
    * Check for nil
  Then you can:
  __Coerce Input__
    * __validate type preconditions__ by calling `.to_s`, `.to_i`, `Array()` on the types that you expect.

__Decorate Input__
    * Enclose the switch over the object and introduce special case object,
       making sure that for all cases conforms to the same interface

__Reject invalid Input__
  * If you cannot wrap the input with a switch for special cases, then validate preconditions.
  * ( raise error | return do-nothing) if precondition not met

__Do nothing with NullObject__
  * return a NullObject which means do-nothing
  * The NullObject returns self for all method calls
  * A useful constructor for NullObject is Maybe() method

__Use default values__
  * Another way of handling nil cases is defining a defalut value

2-Perform Work
* JQuery Style
* Chaining over an arryfied result
* This avoid error handling by doing-nothing when some step in the chain returns empty

3-Deliver Result
* Don't return nil
* Return special-case or null-object
* Or raise an error

4-Handling Errors
* Isolate error handling with a bouncer method(raise error or do-nothing)
* Use checked_xxxx methods where xxxx represents a side-effect that can raise errors
