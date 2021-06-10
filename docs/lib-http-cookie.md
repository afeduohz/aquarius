http/Cookie
-

### The API of `http/Cookie` module:

+ [==](#==)
+ [!=](#!=)
+ [to_s](#to_s)
+ [to_b](#to_b)
+ [type](#type) 
+ [:](#:)

### The API of `http/Cookie` value:

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
(http/Cookie == any) -> bool
```

#### !=

```aquarius
(http/Cookie != any) -> bool
```

#### to_s

```aquarius
(http/Cookie to_s) -> string
```

#### to_b

```aquarius
(http/Cookie to_b) -> true
```

#### type

```aquarius
(http/Cookie type) -> string
```


#### :

Create a http/Cookie value.

```aquarius
(http/Cookie : key(string) val(string)) -> cookie
```

#### expire

Sets the `expire` time of cookie.

```aquarius
(cookie expire time(time)) -> self
```

#### path

Sets the `path` time of cookie.

```aquarius
(cookie path data(string)) -> self
```

#### domain

Sets the `domain` time of cookie.

```aquarius
(cookie domain data(string)) -> self
```
