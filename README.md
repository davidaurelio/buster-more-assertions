referee-more-assertions
======================

Additional assertions for [referee][].

Matchers
--------

At the moment, only matchers for arrays and array-like objects are provided.

### Array / Sequence Matchers

#### Contains by Identity (`===`)

Similar to `assert.contains`, the following assertions are provided:

- `assert.containsOnce(array, element)` passes if `array` contains `element`
  exactly once.

- `assert.containsInOrder(array, a, b, c, ...)` passes if array contains all
  passed-in values in that order.

#### Contains by Match

The following assertions check for *matching* elements. See the [documentation
of `assert.match`][match] to understand how referee matches.

- `assert.containsMatch(array, matcher)` passes if any element in `array`
  matches `matcher`.

- `assert.containsMatchOnce(array, matcher)` passes if exactly one element in
  `array` matches `matcher`.

- `assert.containsMatchesInOrder(array, matcherA, matcherB, ...)` passes if
  elements matching the passed-in matchers are contained in the given order.

#### Contains by Equality

These assertions check sequence elements by *equality.* Read the [documentation
of `assert.equals`][equals] to understand how referee checks for equality.

- `assert.containsEqual(array, value)` passes if any element in  `array` equals
  `value`.

- `assert.containsEqualOnce(array, value)` passes if exactly one element in
  `array` equals `value`.

- `assert.containsEqualsInOrder(array, valueA, valueB, ...)` passes if elements
  equaling the passed-in values are contained in the given order.

#### Contains Substring

This assertion checks whether a string (or string representation of an object)
contains a substring.


Contribute
----------

Contributions welcome! Please make sure that your assertion functions are
properly tested. Don’t test `assert.myAssert()`, but only the
assertion function.

[referee]: http://docs.busterjs.org/en/latest/modules/referee/
[match]: http://docs.busterjs.org/en/latest/modules/referee/#match
[equals]: http://docs.busterjs.org/en/latest/modules/referee/#equals

