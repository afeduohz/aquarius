List
-
List implements part of the [Ruby's Array API](https://ruby-doc.org/core-2.7.3/Array.html).

### The API of `List` module:

+ [==](#==)
+ [!=](#!=)
+ [to_s](#to_s)
+ [to_b](#to_b)
+ [type](#type)
+ [:](#:)

### The API of `list` value:

+ [==](#==)
+ [!=](#!=)
+ [to_s](#to_s)
+ [to_b](#to_b)
+ [type](#type)
+ [+](#+)
+ [-](#-)
+ [*](#*)
+ [|](#|)
+ [&](#&)
+ [<<](#<<)
+ [push](#push)
+ [unshift](#unshift)
+ [>>](#\>>)
+ [@](#@)
+ [any?](#any?)
+ [all?](#all?)
+ [clear](#clear)
+ [map](#map)
+ [map!](#map!)
+ [compact](#compact)
+ [compact!](#compact!)
+ [count](#count)
+ [cycle](#cycle)
+ [delete@](#delete@)
+ [delete](#delete)
+ [delete_if](#delete_if)
+ [drop](#drop)
+ [drop_if](#drop_if)
+ [each](#each)
+ [reverse_each](#reverse_each)
+ [empty?](#empty?)
+ [fetch](#fetch)
+ [fill](#fill)
+ [index](#index)
+ [rindex](#rindex)
+ [first](#first)
+ [include?](#include?)
+ [insert](#insert)
+ [join](#join)
+ [keep_if](#keep_if)
+ [last](#last)
+ [size](#size)
+ [pop](#pop)
+ [shift](#shift)
+ [reject](#reject)
+ [reject!](#reject!)
+ [reverse](#reverse)
+ [reverse!](#reverse!)
+ [sample](#sample)
+ [select](#select)
+ [select!](#select!)
+ [slice](#slice)
+ [slice!](#slice!)
+ [sort](#sort)
+ [sort!](#sort!)
+ [take](#take)
+ [take_if](#take_if)
+ [uniq](#uniq)
+ [uniq!](#uniq!)
+ [values@](#values@)
+ [zip](#zip)


#### ==

```aquarius
(List == any) -> bool
```

#### !=

```aquarius
(List != any) -> bool
```

#### to_s

```aquarius
(List to_s) -> string
```

#### to_b

```aquarius
(List to_b) -> true
```

#### type

```aquarius
(List type) -> string
```

#### :
Return a new list containing item `s`.
```aquarius
(List : s(any)) -> list
```

#### +
Return a new [List](list.md) containing `List` and all elements in `l`.
```aquarius
(List + l(list)...) -> list
```

#### -
Returns a new [List](list.md) that is a copy of the original `List`, 
removing all occurrences of any item that also appear in `l`.
```aquarius
(List - l(list)...) -> list
```

#### *
If `t` is [String](string.md), return a new string connected by `t`; If 
`t` is [Int](int.md), returns a new list built by concatenating the `t` 
copies of self.
```aquarius
(List * t(string|int)) -> string|list
```

#### |
Returns a new list contains elements that are union of `List` and `l`.
```aquarius
(List | l(list)) -> list
```

#### &
Returns a new list contains elements that are intersection of `List` and `l`.
```aquarius
(List & l(list)) -> list
```

#### <<
Append `data` in the end of list, and return itself.
```aquarius
(List << data(any)...) -> self
```

#### push
It is an alias of [<<](#<<).
```aquarius
(List push data(any)...) -> self
```

#### unshift
Prepend `data` in the heading of list, and return itself.
```aquarius
(List unshift data(any)...) -> self
```

#### \>>
Pop up `n` elements from the end of `List`, and return itself.
if `n` is not provided, it is 1 by default; `n` is in [1, [size](#size)).
```aquarius
(List >> [n(int)]) -> self
```

#### @
Returns the element at index `i`. A negative index counts from the end of self. 
Raise [Error](error.md) if the index is out of range.
```aquarius
(List @ [i(int)]) -> any
```

#### any?
Passes each item into `f` as first parameter to evaluate a value 
which will be converted to true/false. Any of `true` result of `f` 
will stop loop call and return `true`, otherwise return `false`.
```aquarius
(List any? f(lambda)) -> bool
```

#### all?
Passes each item into `f` as first parameter to evaluate a value 
which will be converted to true/false. Return `true` if all results 
are `true`, or `false`.
```aquarius
(List all? f(lambda)) -> bool
```

#### clear
Remove all elements from `List`, and return itself.
```aquarius
(List clear) -> self
```

#### map
Returns a new list with the results of running `f` once 
for every item in `List`.
```aquarius
(List map f(lambda)) -> list
```

#### map!
Replace each item with the result of running `f` once for it, 
and return itself.
```aquarius
(List map! f(lambda)) -> self
```

#### compact
Returns a copy of `List` with all `nil` elements removed.
```aquarius
(List compact) -> list
```

#### compact!
Removes `nil` elements from `List`, and return itself.
```aquarius
(List compact!) -> self
```

#### count
Returns the number of elements.
If `i` is provided, counts the number of `i`.
```aquarius
(List count [i(any)]) -> int
```

#### cycle
Calls the given `f` for each item `n` times, and return `List` itself.
```aquarius
(List cycle n(int) f(lambda)) -> self
```

#### delete@
Deletes the element at the specified index `i`, returning that element, 
or raise [Error](error.md) if the index is out of range;
or `nil` if `List` is empty.
```aquarius
(List delete@ i(int)) -> any
```

#### delete
Deletes all elements from self that are equal to `data`.
Returns `data`, or `nil` if no matching item found.
```aquarius
(List delete data(any)) -> any
```

#### delete_if
Deletes every element of self for which `f` evaluates to `true`.
```aquarius
(List delete_if f(lambda)) -> self
```

#### drop
Drops first `n` elements from `List` and returns the rest of the elements 
in an array. `n` is 1 by default.
```aquarius
(List drop [n(int)]) -> list
```

#### drop_if
Return a new list contains elements which passes to `f` and evaluate 
to `false`.
```aquarius
(List drop_if f(lambda)) -> list
```

#### each
Calls `f` once for each element in self, passing that element as a parameter. 
Returns itself.
```aquarius
(List each f(lambda)) -> self
```

#### reverse_each
Same as [each](#each), but traverses self in reverse order.
```aquarius
(List reverse_each f(lambda)) -> self
```

#### empty?
Returns `true` if `List` contains no elements.
```aquarius
(List emtpy?) -> bool
```

#### fetch
Returns the element at index `i`, or `nil` if it does not exsit. If `default`
is provided and is a `Lambda`, then `default` is called with `i` as parameter
and return the result; otherwise return `default`.
```aquarius
(List fetch i(int) [default(any)]) -> any
```

#### fill
`start` is `0` by default; 
`count` is [size](#size) by default;
Fill the `List` `count` elements from `start` with `data` or evaluate `data` 
with parameter of index if `data` is `Lambda`.
```aquarius
(List fill data(any) [start(int)] [count(int)]) -> self
```

#### index
Returns the index of the first element in `List` such that the element is equal
to `data` or `data` evaluates to `true` if `data` is `Lambda`.
If no match, returns `nil`.
```aquarius
(List index data(any)) -> int
```

#### rindex
Returns the last index of the first element in `List` such that the element is equal
to `data` or `data` evaluates to `true` if `data` is `Lambda`.
If no match, returns `nil`.
```aquarius
(List rindex data(any)) -> int
```

#### first
Return first `n` elements. `n` is 1 by default.
If `List` is empty, returns `nil`.
```aquarius
(List first [n(int)]) -> list
```

#### include?
Returns `true` if the `data` is present in self, otherwise returns false.
```aquarius
(List include? data(any)) -> bool
```

#### insert
Inserts from `i` all of the `data` in sequence, and return itself.
If `i` is negative, index will calculate from the end.
```aquarius
(List insert i(int) data(any)...) -> self
```

#### join
Returns a string join all elements of `List` by `sep`, which is empty 
string by default.
```aquarius
(List join [sep(string)]) -> string
```

#### keep_if
Deletes every element of self for which `f` evaluates to false, 
and returns self.
```aquarius
(List keep_if f(lambda)) -> self
```

#### last
Return last `n` elements. `n` is 1 by default.
If `List` is empty, returns `nil`.
```aquarius
(List last [n(int)]) -> list
```

#### size
Return the count of elements.
```aquarius
(List size) -> int
```

#### pop
Removes the last `n` elements from `List` and returns it. </br>
If [size](#size) < `n`, returns entire `List` copy. </br>
If [size](#size) > `n` > 1, returns a list. </br>
If `n` == 1, returns the last element. </br>
If `n` < 1, returns []. </br>
If `List` is empty, return nil.
```aquarius
(List pop [n(int)]) -> any
```

#### shift
Removes the first `n` elements from `List` and returns it. </br>
If [size](#size) < `n`, returns entire `List` copy. </br>
If [size](#size) > `n` > 1, returns a list. </br>
If `n` == 1, returns the last element. </br>
If `n` < 1, returns []. </br>
If `List` is empty, return nil.
```aquarius
(List shift [n(int)]) -> any
```

#### reject
Returns a new list containing the items in self for which 
the `f` is `false`.
```aquarius
(List reject f(lambda)) -> list
```

#### reject!
Deletes every element of self for which the block evaluates to `true`, 
if no changes made returns `nil`.
```aquarius
(List reject! f(lambda)) -> self
```

#### reverse
Returns a new list containing self‘s elements in reverse order.
```aquarius
(List reverse) -> list
```

#### reverse!
Reverses self in place.
```aquarius
(List reverse!) -> self
```

#### sample
Choose a random element or n random elements from `List`.
```aquarius
(List sample) -> any
```

#### select
Returns a new list containing all elements of `List` for which 
`f` returns `true`.
```aquarius
(List select f(lambda)) -> list
```

#### select!
Invokes `f` passing in successive elements from self, deleting 
elements for which `f` returns `false`.
```aquarius
(List select! f(lambda)) -> self|nil
```

#### slice
Returns the element at index `i`, or returns a list starting at 
the start index `i` and continuing for `c` elements.
```aquarius
(List slice i(int) [c(int)]) -> list|nil
```

#### slice!
Deletes the element(s) given by an index `i`.
Returns the deleted object (or objects), or `nil` 
if the index is out of range,
or `List` is empty.
```aquarius
(List slice! i(int) [c(int)]) -> list|nil
```

#### sort
Returns a new list created by sorting self.
```aquarius
(List sort [f(lambda)]) -> list
```

#### sort!
Sorts self in place.
```aquarius
(List sort! [f(lambda)]) -> self
```

#### take
Returns first `n` elements from `List`.
```aquarius
(List take n(int)) -> list
```

#### take_if
Return a new list contains the elements that passed to `f` 
and evaluate to `true`.
```aquarius
(List take_if f(lambda)) -> list
```

#### uniq
Returns a new list by removing duplicate values in self.
```aquarius
(List uniq) -> list
```

#### uniq!
Removes duplicate elements from self.
```aquarius
(List uniq!) -> self
```

#### values@
Returns a list containing the elements in self corresponding 
to the indices `i`. If index `i` is out of range, `nil` is filling.
```aquarius
(List values@ i(int)...) -> list
```

#### zip
Converts any arguments to list, then merges elements of self with 
corresponding elements from each argument.
If the size of any argument is less than the size of the initial list, 
`nil` values are supplied.
```aquarius
(List zip) -> list
```