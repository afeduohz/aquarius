Int
-

### The API of `Int` module:

+ [==](#==)
+ [!=](#!=)
+ [to_s](#to_s)
+ [to_b](#to_b)
+ [type](#type)
+ [:](#:)

### The API of `int` value:

+ [==](#==)
+ [!=](#!=)
+ [to_s](#to_s)
+ [to_b](#to_b)
+ [type](#type)
+ [+](#+)
+ [-](#-)
+ [*](#*)
+ [/](#/)
+ [%](#%)
+ [**](#**)
+ [>](#\>)
+ [>=](#\>=)
+ [<](#<)
+ [<=](#<=)
+ [abs](#abs)
+ [&](#&)
+ [|](#|)
+ [^](#^)
+ [~](#~)
+ [<<](#<<)
+ [>>](#\>>)
+ [negate](#negate)
+ [even?](#even?)
+ [odd?](#odd?)
+ [next](#next)
+ [pred](#pred)
+ [..](#..)
+ [times](#times)
+ [to_f](#to_f)
+ [to_i](#to_i)


#### ==

```aquarius
(Int == any) -> bool
```

#### !=

```aquarius
(Int != any) -> bool
```

#### to_s

```aquarius
(Int to_s) -> string
```

#### to_b

```aquarius
(Int to_b) -> true
```

#### type

```aquarius
(Int type) -> string
```

#### :
Return 0.
```aquarius
(Int :) -> int
```

#### +
Return `Int`+`others`.
```aquarius
(Int + others(numeric)...) -> numeric
```

#### -
Return `Int`-`others`.
```aquarius
(Int - others(numeric)...) -> numeric
```

#### *
Return `Int`*`others`.
```aquarius
(Int * others(numeric)...) -> numeric
```

#### /
Return `Int`/`others`. It returns an `error`, if any.
```aquarius
(Int / others(numeric)...) -> numeric
```

#### %
Return `Int`%`others`. It returns an `error`, if any.
```aquarius
(Int % others(int)...) -> int
```

#### **
Return `Int`**`y`, the base-Int exponential of y.
```aquarius
(Int ** y(numeric)...) -> float
```

#### \>
Return `Int`>`i`. `i` will first be converted to `numeric`.
```aquarius
(Int > i(any)) -> bool
```

#### \>=
Return `Int`>=`i`. `i` will first be converted to `numeric`.
```aquarius
(Int >= i(any)) -> bool
```

#### <
Return `Int`<`i`. `i` will first be converted to `numeric`.
```aquarius
(Int < i(any)) -> bool
```

#### <=
Return `Int`<=`i`. `i` will first be converted to `numeric`.
```aquarius
(Int <= i(any)) -> bool
```

#### abs
Return the absolute value of `Int`.
```aquarius
(Int abs) -> int
```

#### &
Calculate the result of bitwise AND of `Int` and `i`.
```aquarius
(Int & i(int)) -> int
```

#### |
Calculate the result of bitwise OR of `Int` and `i`.
```aquarius
(Int | i(int)) -> int
```

#### ^
Calculate the result of bitwise XOR of `Int` and `i`.
```aquarius
(Int ^ i(int)) -> int
```

#### ~
Calculate the result of bitwise NOT of `Int`.
```aquarius
(Int ~) -> int
```

#### <<
Left shift operation on `Int`. `i` should be non-negative.
```aquarius
(Int << i(int)) -> int
```

#### \>>
Right shift operation on `Int`. `i` should be non-negative.
```aquarius
(Int >> i(int)) -> int
```

#### negate
Return the inverse of `Int`.
```aquarius
(Int negate) -> int
```

#### even?
Test whether `Int` is even.
```aquarius
(Int even?) -> bool
```

#### odd?
Test whether `Int` is odd.
```aquarius
(Int odd?) -> bool
```

#### next
Return `Int`+1.
```aquarius
(Int next) -> int
```

#### pred
Return `Int`-1.
```aquarius
(Int pred) -> int
```

#### ..
Return a new [Range](range.md). `Int` is `begin` and `0` is
default `end` if `i` is not provided.
```aquarius
(Int .. i(int)) -> int
```

#### times
Call `f` (`Int` abs)-1 times, and cursor from 0 to 
(`Int` abs)-1 as the parameter of `f`.
```aquarius
(Int times f(lambda)) -> self
```

#### to_f
Transfer to [Float](float.md)
```aquarius
(Int to_f) -> float
```

#### to_i
Return `Int` self.
```aquarius
(Int to_i) -> int
```