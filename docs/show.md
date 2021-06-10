show
-

### The API of `show` lambda:

+ [==](#==)
+ [!=](#!=)
+ [to_s](#to_s)
+ [to_b](#to_b)
+ [type](#type)
+ [:](#:)

#### ==

```aquarius
(show == any) -> bool
```

#### !=

```aquarius
(show != any) -> bool
```

#### to_s

```aquarius
(show to_s) -> string
```

#### to_b

```aquarius
(show to_b) -> bool
```

#### type

```aquarius
(show type) -> string
```

#### :

`show` display all parameters with info in sequence into stdout.

```aquarius
(show: any...) -> nil
```