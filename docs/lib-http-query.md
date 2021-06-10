http/Query
-

### The API of `http/Query` module:

+ [==](#==)
+ [!=](#!=)
+ [to_s](#to_s)
+ [to_b](#to_b)
+ [type](#type) 
+ [:](#:)

### The API of `http/Query` value:

+ [==](#==)
+ [!=](#!=)
+ [to_s](#to_s)
+ [to_b](#to_b)
+ [type](#type)
+ [get](#get)
+ [gets](#gets)
+ [set](#set)
+ [add](#add)
+ [delete](#delete)
+ [encode](#encode)


#### ==

```aquarius
(http/Query == any) -> bool
```

#### !=

```aquarius
(http/Query != any) -> bool
```

#### to_s

```aquarius
(http/Query to_s) -> string
```

#### to_b

```aquarius
(http/Query to_b) -> true
```

#### type

```aquarius
(http/Query type) -> string
```


#### :

Create a http/Query value.

```aquarius
(http/Query :) -> query
```

#### get

Gets the first value associated with the given `key`. 
If there are no values associated with the key, returns 
the empty string. To access multiple values, use [gets](#gets).

```aquarius
(query get key(string)) -> string
```

#### gets

Gets the values associated with the given `key`.
If there are no values associated with the key, returns []. 
To access the first value, use [get](#get).

```aquarius
(query get key(string)) -> string
```

#### set

Sets the `key` to `val`. It replaces any existing values.
Returns `nil`.

```aquarius
(query set key(string) val(string)) -> nil
```

#### add

Adds the `val` to `key`. It appends to any 
existing values associated with `key`. Returns `nil`.

```aquarius
(query add key(string) val(string)) -> nil
```

#### delete

Deletes the values associated with `key`. Returns `nil`.

```aquarius
(query delete key(string)) -> nil
```

#### encode

Encodes the values into “URL encoded” form 
("bar=baz&foo=quux") sorted by key.

```aquarius
(query encode) -> string
```
