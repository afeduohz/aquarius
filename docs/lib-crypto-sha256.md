crypto/sha256
-

### The API of `crypto/sha256` lambda:

+ [==](#==)
+ [!=](#!=)
+ [to_s](#to_s)
+ [to_b](#to_b)
+ [type](#type)
+ [:](#:)

#### ==

```aquarius
(crypto/sha256 == any) -> bool
```

#### !=

```aquarius
(crypto/sha256 != any) -> bool
```

#### to_s

```aquarius
(crypto/sha256 to_s) -> string
```

#### to_b

```aquarius
(crypto/sha256 to_b) -> bool
```

#### type

```aquarius
(crypto/sha256 type) -> string
```

#### :

`crypto/sha256` calculate the sha256 result of `string`.

```aquarius
(crypto/sha256: string) -> string
```