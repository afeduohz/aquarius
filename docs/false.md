False
-

### The API of `False` module:

+ [==](#==)
+ [!=](#!=)
+ [to_s](#to_s)
+ [to_b](#to_b)
+ [type](#type)
+ [:](#:)

### The API of `false` value:

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
(False == False) -> bool
```

#### !=

```aquarius
(False != 1) -> bool
```

#### to_s

```aquarius
(False to_s) -> string
```

#### to_b

> **IMPORTANT**</br>
> only `false` `nil` are evaluated to `false`, others are all to be `true`.

```aquarius
(False to_b) -> true
```

#### type

```aquarius
(False type) -> string
```

#### :

```aquarius
(False:) -> false
```

#### &

```aquarius
(false & any...) -> false
```

#### |

```aquarius
(false | any...) -> bool
```

#### ^

```aquarius
(false ^ any...) -> bool
```

#### !

```aquarius
(false !) -> true
(false not) -> true
```