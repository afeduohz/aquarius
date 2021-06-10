Range
-

### The API of `Range` module:

+ [==](#==)
+ [!=](#!=)
+ [to_s](#to_s)
+ [to_b](#to_b)
+ [type](#type)
+ [:](#:)

### The API of `range` value:

+ [==](#==)
+ [!=](#!=)
+ [to_s](#to_s)
+ [to_b](#to_b)
+ [type](#type)
+ [begin](#begin)
+ [end](#end)
+ [count](#count)
+ [>>](#\>>)
+ [<<](#<<) 
+ [>>>](#>>>) 
+ [<<<](#<<<) 
+ [sample](#sample) 



#### ==

```aquarius
(Range == any) -> bool
```

#### !=

```aquarius
(Range != any) -> bool
```

#### to_s

```aquarius
(Range to_s) -> string
```

#### to_b

```aquarius
(Range to_b) -> true
```

#### type

```aquarius
(Range type) -> string
```

#### :
Return a new Value of `Range`.
`begin` is left bound, and optional `end` is right bound.
```aquarius
(Range: begin(int) [end(int)]) -> Range
```

#### begin
Return the first number of `Range`.
```aquarius
(Range begin) -> int
```

#### end
Return the last number of `Range`.
```aquarius
(Range end) -> int
```

#### count
Return length of `Range`.
```aquarius
(Range count) -> int
```

#### \>> 
`Range` walk through `begin` to `end` and return itself.
`f` is called for each step.
```aquarius
(Range >> f(lambda)) -> self
```

#### << 
`Range` walk reversely from `end` to `begin` and return itself.
`f` is called for each step.
```aquarius
(Range << f(lambda)) -> self
```

#### \>>>
`Range` walk through `begin` to `end` and return itself.
`s` indicates the step width, and `f` is called for each step.
```aquarius
(Range >>> s(int) f(lambda)) -> self
```

#### <<<
`Range` walk reversely from `end` to `begin` and return itself.
`s` indicates the step width, and `f` is called for each step.
```aquarius
(Range <<< s(int) f(lambda)) -> self
```

#### sample
Return random number between the `begin` and `end`.
```aquarius
(Range sample) -> self
```