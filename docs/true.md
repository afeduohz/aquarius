True
-

### The API of `True` module:

+ [==](#==)
+ [!=](#!=)
+ [to_s](#to_s)
+ [to_b](#to_b)
+ [type](#type)
+ [:](#:)

### The API of `true` value:

+ [==](#==)
+ [!=](#!=)
+ [to_s](#to_s)
+ [to_b](#to_b)
+ [type](#type)
+ [&](#&)
+ [|](#|)
+ [^](#^)
+ [!](#!) alias `not`


#### ==

```aquarius
(True == any) -> bool
```

#### !=

```aquarius
(True != any) -> bool
```

#### to_s

```aquarius
(True to_s) -> string
```

#### to_b

```aquarius
(True to_b) -> true
```

#### type

```aquarius
(True type) -> string
```

#### :

```aquarius
(True:) -> true
```

#### &

```aquarius
(true & any...) -> bool
```

#### |

```aquarius
(true | any...) -> true
```

#### ^

```aquarius
(true ^ any...) -> bool
```

#### !

```aquarius
(true !) -> false
(true not) -> false
```