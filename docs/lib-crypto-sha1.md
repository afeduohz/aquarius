crypto/sha1
-

### The API of `crypto/sha1` lambda:

+ [==](#==)
+ [!=](#!=)
+ [to_s](#to_s)
+ [to_b](#to_b)
+ [type](#type)
+ [:](#:)

#### ==

```aquarius
(crypto/sha1 == any) -> bool
```

#### !=

```aquarius
(crypto/sha1 != any) -> bool
```

#### to_s

```aquarius
(crypto/sha1 to_s) -> string
```

#### to_b

```aquarius
(crypto/sha1 to_b) -> bool
```

#### type

```aquarius
(crypto/sha1 type) -> string
```

#### :

`crypto/sha1` calculate the sha1 result of `string`.

```aquarius
(crypto/sha1: string) -> string
```