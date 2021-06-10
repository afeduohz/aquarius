puts
-

### The API of `puts` lambda:

+ [==](#==)
+ [!=](#!=)
+ [to_s](#to_s)
+ [to_b](#to_b)
+ [type](#type)
+ [:](#:)

#### ==

```aquarius
(puts == any) -> bool
```

#### !=

```aquarius
(puts != any) -> bool
```

#### to_s

```aquarius
(puts to_s) -> string
```

#### to_b

```aquarius
(puts to_b) -> bool
```

#### type

```aquarius
(puts type) -> string
```

#### :

`puts` display all parameters in sequence into stdout.

```aquarius
(puts: any...) -> nil
```