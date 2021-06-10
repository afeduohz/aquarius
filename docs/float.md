Float
-

### The API of `Float` module:

+ [==](#==)
+ [!=](#!=)
+ [to_s](#to_s)
+ [to_b](#to_b)
+ [type](#type)
+ [:](#:)

### The API of `float` value:

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
+ [negate](#negate)
+ [to_f](#to_f)
+ [to_i](#to_i)


#### ==

```aquarius
(Float == any) -> bool
```

#### !=

```aquarius
(Float != any) -> bool
```

#### to_s

```aquarius
(Float to_s) -> string
```

#### to_b

```aquarius
(Float to_b) -> true
```

#### type

```aquarius
(Float type) -> string
```

#### :
Return 0.0.
```aquarius
(Float :) -> float
```

#### +
Return `Float`+`others`.
```aquarius
(Float + others(numeric)...) -> float
```

#### -
Return `Float`-`others`.
```aquarius
(Float - others(numeric)...) -> float
```

#### *
Return `Float`*`others`.
```aquarius
(Float * others(numeric)...) -> float
```

#### /
Return `Float`/`others`. It returns an `error`, if any.
```aquarius
(Float / others(numeric)...) -> float
```

#### **
Return `Float`**`y`, the base-Float exponential of y.
```aquarius
(Float ** y(numeric)...) -> float
```

#### \>
Return `Float`>`i`. `i` will first be converted to `numeric`.
```aquarius
(Float > i(any)) -> bool
```

#### \>=
Return `Float`>=`i`. `i` will first be converted to `numeric`.
```aquarius
(Float >= i(any)) -> bool
```

#### <
Return `Float`<`i`. `i` will first be converted to `numeric`.
```aquarius
(Float < i(any)) -> bool
```

#### <=
Return `Float`<=`i`. `i` will first be converted to `numeric`.
```aquarius
(Float <= i(any)) -> bool
```

#### abs
Return the absolute value of `Float`.
```aquarius
(Float abs) -> float
```

#### negate
Return the inverse of `Float`.
```aquarius
(Float negate) -> float
```

#### to_f
Return `Float` self.
```aquarius
(Float to_f) -> float
```

#### to_i
Transfer to [Int](int.md)
```aquarius
(Float to_i) -> int
```