http/Response
-

### The API of `http/Response` module:

+ [==](#==)
+ [!=](#!=)
+ [to_s](#to_s)
+ [to_b](#to_b)
+ [type](#type)

### The API of `http/Response` value:

+ [==](#==)
+ [!=](#!=)
+ [to_s](#to_s)
+ [to_b](#to_b)
+ [type](#type)
+ [status](#status)
+ [status_code](#status_code)
+ [header](#header)
+ [proto](#proto)
+ [proto_major](#proto_major)
+ [proto_minor](#proto_minor)
+ [text](#text)
+ [json](#json)
+ [>>](#>>)


#### ==

```aquarius
(http/Response == any) -> bool
```

#### !=

```aquarius
(http/Response != any) -> bool
```

#### to_s

```aquarius
(http/Response to_s) -> string
```

#### to_b

```aquarius
(http/Response to_b) -> true
```

#### type

```aquarius
(http/Response type) -> string
```


#### status

Returns http response status, such as `200 OK`.

```aquarius
(response status) -> string
```

#### status_code

Returns http response status code, such as `200`.

```aquarius
(response status_code) -> int
```

#### header

Returns header map keys to values.

```aquarius
(response header) -> dict
```

#### proto

Returns version `HTTP/1.1`.

```aquarius
(response proto) -> string
```

#### proto_major

Returns version major part `1`.

```aquarius
(response proto_major) -> int
```

#### proto_minor

Returns version minor part `1`.

```aquarius
(response proto_minor) -> int
```

#### text

Returns response body.

```aquarius
(response text) -> string
```

#### json

Returns response body parsed as json.

```aquarius
(response json) -> any
```

#### >>

Call lambda `f`, and `response` as parameter of `f`, return its result.

```aquarius
(response >> f(lambda)) -> any
```