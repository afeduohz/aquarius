Dict
-
Dict implements part of the [Ruby's Hash API](https://ruby-doc.org/core-2.7.3/Hash.html).

### The API of `Dict` module:

+ [==](#==)
+ [!=](#!=)
+ [to_s](#to_s)
+ [to_b](#to_b)
+ [type](#type)
+ [:](#:)

### The API of `dict` value:

+ [==](#==)
+ [!=](#!=)
+ [to_s](#to_s)
+ [to_b](#to_b)
+ [type](#type)
+ [<<](#<<)
+ [any?](#any?)
+ [all?](#all?)
+ [clear](#clear)
+ [clone](#clone)
+ [delete](#delete)
+ [delete_if](#delete_if)
+ [each](#each)
+ [empty?](#empty?)
+ [fetch](#fetch)
+ [keep_if](#keep_if)
+ [key](#key)
+ [keys](#keys)
+ [key?](#key?)
+ [include?](#include?)
+ [member?](#member?)
+ [size](#size)
+ [merge](#merge)
+ [merge!](#merge!)
+ [replace](#replace)
+ [reject](#reject)
+ [reject!](#reject!)
+ [select](#select)
+ [select!](#select!)
+ [shift](#shift)
+ [to_l](#to_l)
+ [value?](#value?)
+ [values](#values)
+ [values@](#values@)


#### ==

```aquarius
(Dict == any) -> bool
```

#### !=

```aquarius
(Dict != any) -> bool
```

#### to_s

```aquarius
(Dict to_s) -> string
```

#### to_b

```aquarius
(Dict to_b) -> true
```

#### type

```aquarius
(Dict type) -> string
```

#### :
Create and return a new `Dict` value.
```aquarius
(Dict :) -> dict
```

#### <<
Store a new pair of `key`-`value` into dict. If `value` is not
provided, `nil` is default value.
```aquarius
(Dict << key(string) [value(any)]) -> string
```

#### any?
Passes each dict `key`-`value` pair into `f` as first and second
parameter to evaluate a value which will be converted to true/false.
Any of `true` result of `f` will stop loop call and return `true`,
otherwise return `false`.
```aquarius
(Dict any? [f(lambda)]) -> bool
```

#### all?
Passes each dict `key`-`value` pair into `f` as first and second
parameter to evaluate a value which will be converted to true/false.
Return `true` if all results are `true`, or `false`.
```aquarius
(Dict all? [f(lambda)]) -> bool
```

#### clear
Remove all `key`-`value` pairs from `Dict`, and return itself.
```aquarius
(Dict clear) -> self
```

#### clone
Return a new copy of `Dict`.
```aquarius
(Dict clone) -> dict
```

#### delete
Delete `key` from `Dict`, and return `value` if `key` is existing key or `nil`.
```aquarius
(Dict delete key(string)) -> any
```

#### delete_if
Passes every `key` and `value` pair to `f` to evaluate. It will delete `key` 
from `Dict` if result is `true`.
```aquarius
(Dict delete_if f(lambda)) -> self
```

#### each
Passes each `key` and `value` pair to `f` to evaluate. returns `Dict` itself.
```aquarius
(Dict each f(lambda)) -> self
```

#### empty?
Test if the `Dict` has no key.
```aquarius
(Dict empty?) -> bool
```

#### fetch
Looks up `key` in `Dict`. If the `key` exists, the `value` is returned.
Otherwise, it returns `default`. There is a special case of `default`. 
If `default` is a `Lambda`, the `value` will be passed to `default` 
`lambda` as a parameter, and then return the final result of `lambda`.
```aquarius
(Dict fetch key(string) [default(any)]) -> any
```

#### keep_if
Passes every `key` and `value` pair to `f` to evaluate. It will delete `key`
from `Dict` if result is `false`.
```aquarius
(Dict keep_if f(lambda)) -> self
```

#### key
If `value` is stored value in `Dict` then return the corresponding `key`.
Otherwise, return `nil`.
```aquarius
(Dict key value(any)) -> string
```

#### keys
Returns [List](list.md) of all keys.
```aquarius
(Dict keys) -> list
```

#### key?
Test if `key` is a key in `Dict`.
```aquarius
(Dict key? key(string)) -> bool
```

#### include?
It is an alias of [key?](#key?)
```aquarius
(Dict include? key(string)) -> bool
```

#### member?
It is an alias of [key?](#key?)
```aquarius
(Dict member? key(string)) -> bool
```

#### size
Return the number of `key`-`value` pairs.
```aquarius
(Dict size) -> int
```

#### merge
Returns a new [Dict](dict.md) merged from `Dict` and `d`. If
a `key` exists in both dict, the `value` in the `Dict` is retained.
If `f` is provided, then `value` will be passed to `f` as a parameter,
and then the calculation result of `f` will replace the `value`.
```aquarius
(Dict merge d(dict) [f(lambda)]) -> dict
```

#### merge!
Combine `d` into `Dict`. If the `key` does not exist in `Dict`. it will
be merged directly. If the key already exists and `f` is provided, then
the `value` corresponding to the `key` is as a parameter to calculate `f`, 
and the result is as the `value` in the `Dict`. 
```aquarius
(Dict merge! d(dict) [f(lambda)]) -> self
```

#### replace
Replace all `key`-`value` pairs of `Dict` with the pairs of `d`. 
```aquarius
(Dict replace d(dict)) -> dict
```

#### reject
Create a new dict with `key`-`value` pairs copied from `Dict` which
passes to `f` as first and second parameters, and is evaluated to `false`.
```aquarius
(Dict reject f(lambda)) -> dict
```

#### reject!
Remove the `key`-`value` pairs from `Dict` which passes to `f` as first 
and second parameters, and is evaluated to `true`.
```aquarius
(Dict reject! f(lambda)) -> self
```

#### select
Create a new dict with `key`-`value` pairs copied from `Dict` which
passes to `f` as first and second parameters, and is evaluated to `true`.
```aquarius
(Dict select f(lambda)) -> dict
```

#### select!
Remove the `key`-`value` pairs from `Dict` which passes to `f` as first
and second parameters, and is evaluated to `false`.
```aquarius
(Dict select! f(lambda)) -> self
```

#### shift
Pop up a `key`-`value` pair as 2-element list, where first is `key` and 
second is `value`.
```aquarius
(Dict shift) -> [string, any]
```

#### to_l
Returns a list of 2-element list of `key`-`value` pair.
```aquarius
(Dict to_l) -> list
```

#### value?
Test if `value` is stored in `Dict`.
```aquarius
(Dict value? value(any)) -> bool
```

#### values
Returns a list of all `value` stored in `Dict`.
```aquarius
(Dict values) -> list
```

#### values@
Return a list containing the `value` corresponding to all `key`.
If `key` does not exist, `value` will be `nil`.
```aquarius
(Dict values@ key(string)...) -> list
```