assert
-

### The API of `assert` lambda:

+ [==](#==)
+ [!=](#!=)
+ [to_s](#to_s)
+ [to_b](#to_b)
+ [type](#type)
+ [:](#:)

#### ==

```aquarius
(assert == assert) -> bool
```

#### !=

```aquarius
(assert != 1) -> bool
```

#### to_s

```aquarius
(assert to_s) -> string
```

#### to_b

```aquarius
(assert to_b) -> bool
```

#### type

```aquarius
(assert type) -> string
```

#### :

`assert` expect the `any` as `true`, or it raises an error, with 
message `string` if provided.

```aquarius
(assert: [any [string]]) -> nil
```