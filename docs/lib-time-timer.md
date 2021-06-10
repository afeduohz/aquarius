time/Timer
-

### The API of `time/Timer` module:

+ [==](#==)
+ [!=](#!=)
+ [to_s](#to_s)
+ [to_b](#to_b)
+ [type](#type)

### The API of `time/Timer` value:

+ [==](#==)
+ [!=](#!=)
+ [to_s](#to_s)
+ [to_b](#to_b)
+ [type](#type)
+ [>>](#>>)


#### ==

```aquarius
(time/Timer == any) -> bool
```

#### !=

```aquarius
(time/Timer != any) -> bool
```

#### to_s

```aquarius
(time/Timer to_s) -> string
```

#### to_b

```aquarius
(time/Timer to_b) -> true
```

#### type

```aquarius
(time/Timer type) -> string
```

#### \>>

`lambda` will be executed with [Time](./Time.md) value as the first parameter, after duration of time/Timer expired.

```aquarius
(time/Timer >> lambda) -> nil
```