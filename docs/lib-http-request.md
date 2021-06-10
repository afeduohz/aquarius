http/Request
-

### The API of `http/Request` module:

+ [==](#==)
+ [!=](#!=)
+ [to_s](#to_s)
+ [to_b](#to_b)
+ [type](#type)
+ [OPTIONS](#OPTIONS)
+ [GET](#GET)
+ [POST](#POST)
+ [PUT](#PUT)
+ [PATCH](#PATCH)
+ [DELETE](#DELETE)
+ [HEAD](#HEAD)
+ [TRACE](#TRACE)

### The API of `http/Request` value:

+ [==](#==)
+ [!=](#!=)
+ [to_s](#to_s)
+ [to_b](#to_b)
+ [type](#type)
+ [header@](#header@)
+ [headers@](#headers@)
+ [header](#header)
+ [headers](#headers)
+ [query_string](#query_string)
+ [basic_auth](#basic_auth)
+ [form](#form)
+ [json](#json)


#### ==

```aquarius
(http/Request == any) -> bool
```

#### !=

```aquarius
(http/Request != any) -> bool
```

#### to_s

```aquarius
(http/Request to_s) -> string
```

#### to_b

```aquarius
(http/Request to_b) -> true
```

#### type

```aquarius
(http/Request type) -> string
```


#### OPTIONS

Create a new `OPTIONS` request.

```aquarius
(http/Request OPTIONS url(string)) -> request
```

#### GET

Create a new `GET` request.

```aquarius
(http/Request GET url(string)) -> request
```

#### POST

Create a new `POST` request.

```aquarius
(http/Request POST url(string)) -> request
```

#### PUT

Create a new `PUT` request.

```aquarius
(http/Request PUT url(string)) -> request
```

#### PATCH

Create a new `PATCH` request.

```aquarius
(http/Request PATCH url(string)) -> request
```

#### DELETE

Create a new `DELETE` request.

```aquarius
(http/Request DELETE url(string)) -> request
```

#### HEAD

Create a new `HEAD` request.

```aquarius
(http/Request HEAD url(string)) -> request
```

#### TRACE

Create a new `TRACE` request.

```aquarius
(http/Request TRACE url(string)) -> request
```

#### header@

Gets first `key` header entity first value.

```aquarius
(request header@ key(string)) -> string
```

#### headers@

Gets first `key` header entity values as list.

```aquarius
(request headers@ key(string)) -> []
```

#### header

`override` == `true`, `set` the `key` as `val`;
`override` == `false`, `append` the `key` value `val`.
default `override` is `false`.

```aquarius
(request header key(string) val(string) [override(bool)]) -> self
```

#### headers

Like [header](#header), but `val` is a `list` of string.

```aquarius
(request headers@ key(string) val(list) [override(bool)]) -> self
```

#### query_string

Sets `QueryString` typeof [http/Query](lib-http-query.md) of request. returns itself.

```aquarius
(request query_string qs(query)) -> self
```

#### basic_auth

Sets the request's Authorization header to use HTTP Basic Authentication 
with the provided `username` and `password`. return itself.

```aquarius
(request basic_auth username(string) password(string)) -> self
```

#### form

Sets `form` data of request. the request set header
`Content-Type`: `application/x-www-form-urlencoded`.
returns itself.

```aquarius
(request form data(query)) -> self
```

#### form

Sets `json` data of request. the request set header
`Content-Type`: `application/json`.
returns itself.

```aquarius
(request json data(any)) -> self
```